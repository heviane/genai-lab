# ✍️ Engenharia de Prompts

A arte de formular prompts eficazes, é conhecida como **Engenharia de Prompt**, é a habilidade mais importante para dominar essa tecnologia.

| Conceito Avançado | Importância |
| :--- | :--- |
| **Engenharia de Prompt** | É a disciplina de projetar o prompt ideal para obter a melhor resposta do modelo. Isso envolve técnicas como: **Contextualização** (dar um papel à IA, ex: "Você é um especialista..."), **Restrições** (ex: "Use apenas 100 palavras") e **Raciocínio em Cadeia de Pensamento (CoT)**, que força a IA a explicar seu raciocínio antes de dar a resposta final. |
| **Prompts Multimodais** | A evolução do conceito. Um prompt não é só texto. Ele pode incluir **imagens, áudio ou vídeo** (como no Gemini 2.5), e a IA usará todas essas entradas para gerar a saída. |
| **Prompt como Código** | Para modelos grandes como GPT-4 ou Gemini, um prompt bem-feito atua como um **código de programação em linguagem natural**, direcionando a arquitetura interna do modelo para um resultado específico. |

---

## O que é Engenharia de Prompts?

A **Engenharia de Prompt** é o processo de projetar e refinar as entradas (os prompts) fornecidas a um modelo de linguagem (LLM) para obter as saídas mais precisas, relevantes e úteis possíveis.

Resumindo: Refinar, passar contexto, dar exemplos, especificar saídas, etc; E assim repetir até que se obtenha resultados satisfatórios.

- **Linguagem direta**: Ser explicito sobre o tipo de resposta que deseja.
- **Mensagens do sistema**: Descreva como o chat deve funcionar.
- **Fornecer exemplos**: As LLMs geralmente dão suporte ao aprendizado zero-shot no qual as respostas podem ser geradas sem exemplos anteriores. No entanto, vc também pode fornecer algumas respostas de exemplo, conhecidas como aprendizado de poucas capturas.
- **Dados básicos**: Os prompts podem incluir dados de fundamentação para fornecer contexto.

Para um desenvolvedor, é a habilidade mais crucial para controlar o comportamento de uma IA Generativa.

Pense no LLM como um programador júnior extremamente talentoso, mas que precisa de instruções muito claras. O prompt é a sua "especificação de tarefa". Quanto melhor a especificação, melhor o resultado.

## Por que é tão importante?

A qualidade da saída de um LLM é diretamente proporcional à qualidade do seu prompt. Um prompt vago ou mal formulado pode levar a:

- **Respostas incorretas ou "alucinações"**: O modelo inventa fatos.
- **Respostas genéricas**: O modelo não fornece o detalhe ou a especificidade que você precisa.
- **Respostas em formato inadequado**: O modelo retorna um parágrafo de texto quando você precisava de um JSON.

O grau de assertividade vai depender do contexto que é fornecido.
Saber gerar prompts e fornecer contextos é importantíssimo para tirar o máximo proveito.

---
