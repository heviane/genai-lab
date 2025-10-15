# Modelos de Inteligência Artificial Generativa - LLMs - Large Language Models

São modelos de aprendizado de máquina, geralmente baseados em **redes neurais profundas**, que são treinados em grandes volumes de dados textuais. Esses modelos têm a capacidade de compreender, gerar e até mesmo traduzir texto de forma bastante avançada, devido ao seu treinamento em enormes quantidades de texto.

As LLMs estão no centro das IAs generativas.

Aplicativos de GenAi são alimentados por LLMs, que são um tipo especializado de modelo de **Machine Learning** que você pode usar para executar tarefas de **PLN (processamento de linguagem natural)**, incluindo:

- Determinar sentimento ou classificar de outra forma o texto em idioma natural.
- Resumir um texto.
- Comparar várias fontes de texto quanto à similaridade semântica.
- Geração de nova linguagem natural.

## Modelo Transformador

A arquitetura do modelo transformador consiste em dois componentes/blocos principais:

- Bloco Codificador: Que cria representações semânticas do vocabulário de treinamento (entrada).
- Bloco Decodificador: Que gera novas sequências de linguagem.

- O texto é tokenizado para que cada palavra ou frase seja representada por um token numerico exclusivo.
- Inserções: São valores de vetor com várias dimensões, que são atribuídas aos tokens.
- As camadas de atenção examinam cada token por vez e determinam valores incorporados que refletem os relacionamentos semânticos entre os tokens.
- No decodificador, essas relações são usadas para prever a sequência mais provável de tokens.

### Tokenização

1. Etapa 1 - Tokenização: A primeira etapa no treinamento de um modelo de transformador é **decompor** o texto de treinamento em **tokens**.
2. Etapa 2 - Inserções: As relações entre tokens são capturadas como vetores, conhecidos como inserções.
3. Etapa 3 - Atenção: Capture a força das relações entre tokens usando a técnica de atenção.

### Como funciona

Usa probabilidade de encaixe para saber o que faz mais sentido naquela sequência.
Tem uma probabilidade de acerto e uma  probabilidade de erro.
Ou seja, esses modelos funcionam por PROBABILIDADE, entendendo isso, vemos que não existe de fato uma inteligência genuína.
Sendo assim, NUNCA apenas copie e cole código gerado.
O grau de assertividade vai depender do contexto que é fornecido para essas IAs.
Saber gerar prompts e fornecer contextos é importantíssimo para tirar o máximo proveito.
Entender como criar bons prompts é muito relevante.

## Aplicações práticas

LLMs são amplamente utilizados em tarefas de Processamento de Linguagem Natural (PLN), como:

- Geração de texto, imagens, músicas, videos, código.
- Tradução automática
- Resposta a perguntas
- Análise de sentimentos
- Classificação de texto

Esses modelos funcionam processando entradas de texto e gerando saídas com base em seu treinamento em grandes corpora de dados.

## Exemplos de LLMs

- GPT (Generative Pre-trained Transformer) da OpenAI
- BERT da Google
- e outros modelos de transformação como o T5 e XLNet
