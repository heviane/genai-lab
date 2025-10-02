# Inteligência Artificial Generativa

## O que é IA (Inteligência Artificial)?

Imita o comportamento humano usando **aprendizado de máquina** para interagir com o ambiente e executar tarefas sem instruções explícitas.

## O que é IA Generativa?

Cria conteúdo original, como IA generativa que foi incorporada a aplicativos de chat.
Os aplicativos de GenAi usam entrada em linguagem natural e retornam respostas aproppriadas em uma variedade de formatos.

Principais aplicações de IA Generativa:

- Geração de linguagem natural
- Geração de código
- Geração de imagens
- Geração de audio

### Modelos de IA Generativos

#### SLMs - Small Language Models

#### LLMs - Large Language Models

Aplicativos de GenAi são alimentados por LLMs, que são um tipo especializado de modelo de **Machine Learning** que você pode usar para executar tarefas de **PLN (processamento de linguagem natural)**, incluindo:

- Determinar sentimento ou classificar de outra forma o texto em idioma natural.
- Resumir um texto.
- Comparar várias fontes de texto quanto à similaridade semântica.
- Geração de nova linguagem natural.

### Modelo Transformador

A arquitetura do modelo transformador consiste em dois componentes/blocos principais:

- Bloco Codificador: Que cria representações semânticas do vocabulário de treinamento (entrada).
- Bloco Decodificador: Que gera novas sequências de linguagem.

- O texto é tokenizado para que cada palavra ou frase seja representada por um token numerico exclusivo.
- Inserções: São valores de vetor com várias dimensões, que são atribuídas aos tokens.
- As camadas de atenção examinam cada token por vez e determinam valores incorporados que refletem os relacionamentos semânticos entre os tokens.
- No decodificador, essas relações são usadas para prever a sequência mais provável de tokens.

#### Tokenização

1. Etapa 1 - Tokenização: A primeira etapa no treinamento de um modelo de transformador é **decompor** o texto de treinamento em **tokens**.
2. Etapa 2 - Inserções: As relações entre tokens são capturadas como vetores, conhecidos como inserções.
3. Etapa 3 - Atenção: Capture a força das relações entre tokens usando a técnica de atenção.

### Copilotos

Os copilotos são frequentemente integrados a outros aplicativos e fornecem uma maneira para os usuários obterem ajuda com tarefas comuns a partir de um modelo de GenAi.

### Engenharia de Prompts

É o processo de projetar e refinar as entradas (os prompts) fornecidas a um modelo de linguagem (LLM) para obter as saídas mais precisas, relevantes e úteis possíveis.

- Linguagem direta: Ser explicito sobre o tipo de resposta que deseja.
- Mensagens do sistema: Descreva como o chat deve funcionar.
- Fornecer exemplos: As LLMs geralmente dão suporte ao aprendizado zero-shot no qual as respostas podem ser geradas sem exemplos anteriores. No entanto, vc também pode fornecer algumas respostas de exemplo, conhecidas como aprendizado de poucas capturas.
- Dados básicos: Os prompts podem incluir dados de fundamentação para fornecer contexto.
