# ✍️ Técnicas de Engenharia de Prompt Fundamentais

Aqui estão algumas das técnicas mais comuns e eficazes que todo desenvolvedor deve conhecer.

## Técnicas de Engenharia de Prompts

| Conceito | Explicação Simples |
| :--- | :--- |
| **O que são?** | Estratégias e métodos para **estruturar e formatar** o seu *prompt* (instrução inicial) para extrair a resposta mais precisa, relevante e de alta qualidade possível de uma IA generativa. |
| **Objetivo Final?** | **Melhorar a comunicação** com a IA. Transformar um pedido vago em uma instrução clara e otimizada. |
| **Analogia?** | São como os **melhores truques ou atalhos** que um usuário experiente usa para fazer a IA trabalhar de forma mais inteligente. |

Essas técnicas são a chave para transformar uma IA de um mero gerador de texto em um **colaborador inteligente**.

## 1. Instruções Diretas (Clareza e Especificidade)

Aprender a dar instruções diretas, sem ambiguidades.
Seja o mais específico possível. Diga ao modelo exatamente o que fazer e qual formato de saída você espera.
Este será o conteúdo principal do prompt.

> **❌ Exemplo Ruim**: "Fale sobre o Python."
> **✅ Exemplo Bom**: "Crie um resumo em 3 parágrafos sobre os principais benefícios de usar Python para desenvolvimento web, focando em seus frameworks mais populares (Django e Flask)."

### Definir Persona, Formato e Tom

Uma das técnicas mais poderosas é dizer explicitamente ao modelo **quem ele deve ser (Persona)**, **como ele deve estruturar a resposta (Formato)** e **qual estilo de linguagem usar (Tom)**.

- **Persona**: O papel que a IA deve assumir. Ex: "Você é um chef de cozinha italiano."
- **Formato**: A estrutura da saída. Ex: "Liste os ingredientes em bullet points."
- **Tom**: O estilo da escrita. Ex: "Use um tom amigável e informal."

> **❌ Exemplo Ruim**: "Como faço lasanha?"
> **✅ Exemplo Bom**: "Aja como uma *nonna* italiana (Persona). Escreva uma receita de lasanha à bolonhesa. Primeiro, liste os ingredientes (Formato) e depois o modo de preparo em passos numerados. Use um tom carinhoso e cheio de dicas secretas (Tom)."

- **Conteúdo de Suporte**: Dados extras que ajudam a tarefa, como datas ou preferências.
    > **Exemplo**: "Use o contexto atual de dezembro de 2024 nas respostas."
- **Restrições ou Limitações**: Limitam a resposta em termos de extensão, escopo ou formato.
    > - **Exemplo Extensão**: "Resuma o conceito de 'Machine Learning' em exatamente 3 frases."
    > - **Exemplo Escopo**: "Descreva os benefícios da energia solar sem mencionar os custos."
    > - **Exemplo Formato**: "Liste 3 capitais europeias. Forneça apenas os nomes, separados por vírgula."
- **Indicações e Formatos de Saída**: Guiam o modelo para gerar saídas específicas, usando estímulos. Especificam o formato e estrutura da resposta/saída.
    > **Exemplos**: "Liste os pontos principais.", "Apresente no formato de lista com bullet points." e "Liste os resultados em ordem decrescente.".
- **Cadeia de Pensamento (Chain of Thought Prompting)**: Instrução para que o modelo **responda passo a passo** antes de dar a resposta final, explicando o raciocínio até a chegada da conclusão final, ou seja, incentiva o modelo a explicar o raciocínio passo a passo antes de apresentar uma resposta final.
- **Repetir instruções no final**: Reforçar as orientações no final do prompt para garantir que o modelo compreenda e siga a tarefa proposta sem desvios. Poderia ser um resumo da solicitação.
- **Guardrails**: Técnica de limitar respostas, evitando conteúdos prejudiciais, irrelevantes ou incorretos, alinhando o modelo a padrões éticos.
- **Divisão da Tarefa**: Quebrar uma tarefa/problema complexa em várias etapas menores, facilitando para o modelo responder de forma lógica e organizada. Resolvendo uma etapa por vez, antes de passar para o próximo.
- **Adicionar sintaxe clara**: Organizar o prompt com formatações como listas, titulos ou tabelas, tornando as instruções mais visuais, legíveis e compreensiveis.

---

## 2. Zero-Shot Prompting

É a forma mais simples: você faz uma pergunta ou dá uma instrução diretamente, sem fornecer exemplos prévios.
O modelo usa seu conhecimento pré-treinado para responder.

Útil quando o modelo deve generalizar com base apenas na instrução.

> **Exemplo**: "Traduza a frase 'Hello, world!' para o francês."

---

## 3. Few-Shot Prompting (e One-Shot)

Você fornece ao modelo um ou mais **EXEMPLOS** completos da tarefa que deseja que ele execute. Isso ajuda o modelo a entender o padrão e o formato da saída esperada. *One-Shot* é quando você fornece apenas um exemplo.

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

---

## 4. Chain-of-Thought (CoT) Prompting

Essa técnica instrui o modelo a "pensar passo a passo" antes de dar a resposta final. É extremamente útil para problemas que exigem raciocínio, lógica ou cálculos.

> **Exemplo**: "Um fazendeiro tem 15 vacas. Ele vende 3 e nascem o dobro do que ele vendeu. Com quantas vacas ele fica? Pense passo a passo antes de dar a resposta final."

---

## 5. Fornecer Contexto (Grounding)

Incluir dados ou informações relevantes no prompt para basear a resposta em fatos, evitando que o modelo use seu conhecimento geral (que pode estar desatualizado ou incorreto). É a base para a técnica de **RAG (Retrieval-Augmented Generation)**.

> **Exemplo**:
>
> ```text
> Contexto: "O produto 'X-1000' foi lançado em 2023, possui uma bateria de 5000mAh e custa R$ 2.500. Ele é resistente à água, mas não possui carregamento sem fio."
>
> Pergunta: "Com base no texto fornecido, o produto X-1000 tem carregamento sem fio e qual o seu preço?"
> ```
