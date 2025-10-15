# 🧩 O que são Modelos Generativos?

Um **Modelo Generativo** é um tipo de modelo de inteligência artificial que aprende os padrões e a estrutura subjacente de um conjunto de dados de treinamento para, em seguida, **gerar novos dados** que se assemelham aos dados originais.

Em vez de apenas classificar ou prever informações (como faria um modelo tradicional), um modelo generativo é um criador de conteúdo.

## Modelos Generativos vs. Discriminativos

A maneira mais fácil de entender os modelos generativos é compará-los com seus opostos, os **modelos discriminativos**.

| Característica | Modelo Discriminativo (Tradicional) | Modelo Generativo |
| :--- | :--- | :--- |
| **Objetivo** | Aprender a fronteira que **separa** as classes de dados. | Aprender a **distribuição** dos dados para poder criar novas amostras. |
| **Pergunta** | "Isso é um A ou um B?" | "Mostre-me como é um A." |
| **Exemplo** | Um modelo que olha para uma foto e diz "é um gato" ou "não é um gato". | Um modelo que, a partir do nada, **cria uma nova imagem** de um gato. |
| **Foco** | Previsão e Classificação. | Criação e Geração de Conteúdo. |

## Principais Arquiteturas de Modelos Generativos

Diferentes tipos de modelos generativos foram desenvolvidos ao longo do tempo, cada um com sua própria abordagem:

1. **Generative Adversarial Networks (GANs)**: Famosas pela geração de imagens, as GANs consistem em duas redes neurais que competem entre si: um **Gerador** que cria os dados e um **Discriminador** que tenta diferenciar os dados falsos dos reais. O gerador melhora até conseguir "enganar" o discriminador.

2. **Variational Autoencoders (VAEs)**: Esses modelos aprendem uma representação comprimida (latente) dos dados e a usam para reconstruir e gerar novas amostras.

3. **Transformers**: Esta é a arquitetura que impulsiona os **Large Language Models (LLMs)** como GPT e Gemini. Sua principal inovação é o mecanismo de *self-attention*, que permite ao modelo pesar a importância de diferentes palavras em uma sequência, capturando o contexto de forma muito eficaz para gerar texto coerente.

4. **Modelos de Difusão**: São o estado da arte para a geração de imagens de alta qualidade (usados em modelos como DALL-E 3 e Stable Diffusion). Eles funcionam adicionando "ruído" a uma imagem até que ela se torne irreconhecível e, em seguida, aprendem a reverter esse processo, gerando uma imagem clara a partir do ruído.

Essencialmente, todos esses modelos são treinados em enormes volumes de dados para que possam "entender" a essência do que estão aprendendo e, a partir desse entendimento, criar algo completamente novo.
