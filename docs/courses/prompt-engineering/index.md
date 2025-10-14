# ✍️ O que é Engenharia de Prompts?

A **Engenharia de Prompts** é a prática de projetar e refinar as entradas (os *prompts*) fornecidas a um modelo de linguagem (LLM) para obter as saídas mais precisas, relevantes e úteis possíveis. Para um desenvolvedor, é a habilidade mais crucial para controlar o comportamento de uma IA Generativa.

Pense no LLM como um programador júnior extremamente talentoso, mas que precisa de instruções muito claras. O prompt é a sua "especificação de tarefa". Quanto melhor a especificação, melhor o resultado.

## Por que é tão importante?

A qualidade da saída de um LLM é diretamente proporcional à qualidade do seu prompt. Um prompt vago ou mal formulado pode levar a:

- **Respostas incorretas ou "alucinações"**: O modelo inventa fatos.
- **Respostas genéricas**: O modelo não fornece o detalhe ou a especificidade que você precisa.
- **Respostas em formato inadequado**: O modelo retorna um parágrafo de texto quando você precisava de um JSON.

## Técnicas Fundamentais de Engenharia de Prompt

Aqui estão algumas das técnicas mais comuns e eficazes que todo desenvolvedor deve conhecer.

### 1. Clareza e Instruções Diretas

Seja o mais específico possível. Diga ao modelo exatamente o que fazer, qual papel assumir e qual formato de saída você espera.

> **Exemplo Ruim**: "Fale sobre o Python."
>
> **Exemplo Bom**: "Aja como um engenheiro de software sênior. Crie um resumo em 3 parágrafos sobre os principais benefícios de usar Python para desenvolvimento web, focando em seus frameworks mais populares (Django e Flask)."

### 2. Zero-Shot Prompting

É a forma mais simples: você faz uma pergunta ou dá uma instrução diretamente, sem fornecer exemplos prévios. O modelo usa seu conhecimento pré-treinado para responder.

> **Exemplo**: "Traduza a frase 'Hello, world!' para o francês."

### 3. Few-Shot Prompting (e One-Shot)

Você fornece ao modelo um ou mais exemplos completos da tarefa que deseja que ele execute. Isso ajuda o modelo a entender o padrão e o formato da saída esperada. *One-Shot* é quando você fornece apenas um exemplo.

> **Exemplo (Few-Shot)**:
>
> ```textplain
> Converte a linguagem natural em um comando SQL.
>
> Exemplo 1: "Mostre todos os usuários do Brasil."
> SQL: SELECT * FROM users WHERE country = 'Brazil';
>
> Exemplo 2: "Quantos produtos temos na categoria 'eletrônicos'?"
> SQL:
> ```

### 4. Chain-of-Thought (CoT) Prompting

Essa técnica instrui o modelo a "pensar passo a passo" antes de dar a resposta final. É extremamente útil para problemas que exigem raciocínio, lógica ou cálculos.

> **Exemplo**: "Um fazendeiro tem 15 vacas. Ele vende 3 e nascem o dobro do que ele vendeu. Com quantas vacas ele fica? Pense passo a passo antes de dar a resposta final."
