# Prompt Rico

## O que é "Prompt Rico"?

- Definição técnica e prática do termo **"Prompt Rico"**:

> O "Prompt Rico" (ou *Rich Prompt*) **não é um termo técnico padronizado** da literatura científica (como Chain-of-Thought ou Few-Shot). Em vez disso, é um **conceito** e um **padrão de design** amplamente adotado na prática da engenharia de *prompts*.

- Aqui está a explicação em termos técnicos:

> O termo "Prompt Rico" descreve um **Prompt Estruturado de Alta Definição** que fornece ao Modelo de Linguagem Grande (LLM) **todos os elementos contextuais, funcionais e restritivos necessários** para produzir uma saída precisa e de alta qualidade.
> É a **aplicação prática** dos princípios que vimos no seu artigo anterior (FTAE, 3R's, etc.).

---

### É um Padrão ou uma Técnica?

É, primariamente, um **Padrão de Design**.

| Categoria | Definição |
| :--- | :--- |
| **Padrão de Design** | É a **estrutura** de como o *prompt* é construído. Ele define quais componentes devem estar presentes (Função, Contexto, Regras, Persona) e a ordem em que devem aparecer. |
| **Técnica** | São os **métodos específicos** usados *dentro* do *Prompt Rico* para melhorar o raciocínio (ex: *Chain-of-Thought*), a precisão (*Few-Shot*) ou o controle da saída (delimitação de variáveis). |

**Em resumo:** O *Prompt Rico* é o **esqueleto** que garante que o LLM não precise adivinhar o que você quer, usando **técnicas** para otimizar a resposta.

### Elementos Chave de um Prompt Rico

Um *prompt* é considerado "rico" quando inclui (e geralmente separa) os seguintes componentes:

1. **Persona / Papel (Role-Playing):** Quem o LLM deve fingir ser (ex: "Especialista em Cibersegurança").
2. **Público-Alvo (Audience):** Para quem o conteúdo deve ser entregue (ex: "Explique para um investidor leigo").
3. **Função / Tarefa (Function):** A ação principal (ex: "Resuma este texto e crie 5 tópicos de ação").
4. **Contexto / Dados de Entrada:** O material que a IA deve processar (texto, código, variáveis).
5. **Restrições / Regras (Constraints):** Limites e regras de formatação (ex: "Máximo 200 palavras", "Use formato Markdown", "Não use gírias").

Ao incluir todos esses elementos, você cria um **contexto de alta fidelidade**, levando a resultados que superam em muito os *prompts* de uma linha.

---
