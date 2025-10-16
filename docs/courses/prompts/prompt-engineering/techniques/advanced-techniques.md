# ✍️ Técnicas de Engenharia de Prompt Avançadas de Raciocínio

Estas técnicas vão além do básico, permitindo que você extraia dos LLMs a capacidade de resolver problemas complexos, planejar e interagir com o ambiente.

---

## 1. Zero-shot CoT

**O que é?** É a técnica de adicionar uma simples instrução como **"Pense passo a passo"** ou **"Vamos raciocinar em etapas"** a um prompt, sem fornecer nenhum exemplo. Isso ativa a capacidade de raciocínio do modelo, fazendo com que ele detalhe seu processo de pensamento antes de dar a resposta final.

**Quando usar?** Ideal para problemas de lógica, matemática ou qualquer tarefa que exija múltiplas etapas de raciocínio, mas que não seja complexa a ponto de precisar de exemplos explícitos.

### Exemplo

> **Problema:** Um fazendeiro tinha 15 ovelhas e todas, exceto 8, morreram. Quantas ovelhas ele tem agora?

- **❌ Prompt Simples (Zero-shot)**

```text
Um fazendeiro tinha 15 ovelhas e todas, exceto 8, morreram. Quantas ovelhas ele tem agora?
```

- **❌Resposta Potencialmente Incorreta: 7*

- **✅ Prompt com Zero-shot CoT**

```text
Um fazendeiro tinha 15 ovelhas e todas, exceto 8, morreram. Quantas ovelhas ele tem agora? Pense passo a passo.
```

**Saída Esperada do Modelo:**
> Claro, vamos pensar passo a passo:
    > 1. A frase "todas, exceto 8, morreram" é uma forma de dizer quantas ovelhas sobreviveram.
    > 2. A palavra "exceto" indica as que restaram.
    > 3. Portanto, o número de ovelhas que não morreram é 8.
> **Resposta Final:** O fazendeiro tem 8 ovelhas.

---

## 2. Self-Consistency

**O que é?** É uma estratégia que aprimora o *Chain-of-Thought*. Em vez de gerar apenas uma linha de raciocínio, você executa o mesmo prompt várias vezes, gerando múltiplos "caminhos de pensamento". A resposta final é aquela que aparece com mais frequência entre os diferentes raciocínios.

**Quando usar?** Em problemas complexos onde um único caminho de raciocínio pode facilmente levar a um erro. A "votação" entre várias tentativas aumenta drasticamente a chance de obter a resposta correta.

### Exemplo

> **Problema:** Se 5 máquinas levam 5 minutos para fazer 5 widgets, quanto tempo 100 máquinas levariam para fazer 100 widgets?

**Prompt (usado 3 vezes):**

```text
Se 5 máquinas levam 5 minutos para fazer 5 widgets, quanto tempo 100 máquinas levariam para fazer 100 widgets? Raciocine em etapas.
```

**Saídas Geradas pelo Modelo:**

> **Raciocínio 1:** Se 5 máquinas fazem 5 widgets em 5 minutos, isso significa que 1 máquina leva 5 minutos para fazer 1 widget. Portanto, 100 máquinas podem fazer 100 widgets em paralelo, e levarão os mesmos 5 minutos. **Resposta: 5 minutos.**
> **Raciocínio 2:** A taxa é de 1 widget por máquina a cada 5 minutos. Com 100 máquinas, cada uma pode produzir seu próprio widget. Como todas trabalham ao mesmo tempo, o tempo total para produzir 100 widgets será de 5 minutos. **Resposta: 5 minutos.**
> **Raciocínio 3:** Vamos calcular a taxa. 5 widgets / 5 máquinas / 5 minutos = 0.2 widgets por máquina por minuto. Para 100 widgets com 100 máquinas, o tempo seria 100 widgets / (100 máquinas * 0.2) = 5 minutos. **Resposta: 5 minutos.**

**Consolidação:** Todas as três linhas de raciocínio, embora ligeiramente diferentes, chegaram à mesma resposta.
**Resposta Final (Consistente):** 5 minutos.

---

## 3. Tree of Thoughts (ToT)

**O que é?** Uma técnica mais avançada onde o modelo não apenas segue um caminho, mas explora múltiplos "galhos" de raciocínio em paralelo. Em cada passo, ele pode gerar vários pensamentos ou próximos passos possíveis, avaliá-los e decidir qual ramo é o mais promissor para continuar a exploração. É como um brainstorming estruturado.

**Quando usar?** Para problemas que exigem planejamento, exploração e onde a solução não é linear, como jogos (xadrez), problemas de design ou quebra-cabeças complexos.

### Exemplo

> **Problema:** Use os números 4, 9, 10, 13 e as operações básicas (+, -, *, /) para chegar ao resultado 24.

**Prompt (simplificado para ilustrar a ideia):**

```text
Use os números 4, 9, 10, 13 para obter 24. Gere 3 pensamentos iniciais sobre como combinar os números. Avalie cada pensamento e escolha o melhor para continuar.
```

**Saída Esperada do Modelo:**
> **Passo 1: Gerar Pensamentos**
    > 1.  **Pensamento A:** Tentar combinar 10 e 4. `10 + 4 = 14`. Sobram 9 e 13. Como chegar a 24 com 14, 9 e 13? Parece difícil.
    > 2.  **Pensamento B:** Tentar combinar 13 e 9. `13 - 9 = 4`. Sobram 10 e 4. Como chegar a 24 com 4, 10 e 4? `4 * (10 - 4) = 24`. Isso parece promissor.
    > 3.  **Pensamento C:** Tentar combinar 13 e 10. `13 + 10 = 23`. Sobram 4 e 9. Como chegar a 24 com 23, 4 e 9? `23 + (9-4)` não é 24.
    >
> **Passo 2: Avaliar Pensamentos**
> O Pensamento B encontrou uma solução diretamente. O Pensamento A e C parecem levar a becos sem saída.
>
> **Passo 3: Concluir**
> O caminho mais promissor foi o B.
> **Resposta Final:** `(13 - 9) * (10 - 4) = 4 * 6 = 24`.

---

## 4. ReAct (Reason + Act)

**O que é?** Um framework que permite ao LLM **Raciocinar (Reason)** e **Agir (Act)**. O modelo intercala pensamentos sobre o que precisa fazer com ações, que são chamadas a ferramentas externas (ex: uma API de busca, uma calculadora, um banco de dados). Ele usa o resultado da ação para refinar seu próximo pensamento.

**Quando usar?** Essencial para construir agentes e aplicações que precisam de informações atualizadas ou que precisam interagir com outros sistemas. Perfeito para responder perguntas sobre eventos recentes, dados de uma empresa ou executar tarefas no mundo real.

### Exemplo

> **Pergunta do Usuário:** Qual a população da capital do país onde foi realizada a Copa do Mundo de 2014?

**Ciclo ReAct do Modelo (simplificado):**

> **Pensamento 1:** Eu preciso primeiro descobrir onde foi a Copa do Mundo de 2014. Depois, preciso encontrar a capital desse país. Por fim, preciso buscar a população dessa capital.
> **Ação 1:** `search("Copa do Mundo de 2014 país sede")`
> **Observação 1 (Resultado da Ação):** A Copa do Mundo de 2014 foi realizada no Brasil.
>
> **Pensamento 2:** Ok, o país é o Brasil. Agora preciso saber qual é a capital do Brasil.
> **Ação 2:** `search("capital do Brasil")`
> **Observação 2:** A capital do Brasil é Brasília.
>
> **Pensamento 3:** Agora que sei que a capital é Brasília, preciso encontrar sua população.
> **Ação 3:** `search("população de Brasília")`
> **Observação 3:** A população estimada de Brasília é de aproximadamente 3 milhões de habitantes.
>
> **Pensamento 4:** Tenho todas as informações necessárias para responder à pergunta do usuário.
> **Resposta Final:** A Copa do Mundo de 2014 foi no Brasil, cuja capital é Brasília. A população de Brasília é de aproximadamente 3 milhões de habitantes.
