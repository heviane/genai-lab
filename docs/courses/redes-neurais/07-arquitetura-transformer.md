# 🏛️ A Arquitetura Transformer

A arquitetura **Transformer** é um modelo de rede neural introduzido em 2017 no famoso artigo "Attention Is All You Need". Ela revolucionou o campo do Processamento de Linguagem Natural (PLN) e é a base para a maioria dos Large Language Models (LLMs) modernos, como o GPT, Gemini e Claude.

## O Problema que o Transformer Resolveu

Antes dos Transformers, os modelos de sequência, como as Redes Neurais Recorrentes (RNNs), processavam o texto palavra por palavra, em ordem. Isso criava dois grandes problemas:

1. **Dificuldade com Contexto Longo**: A "memória" do modelo sobre palavras no início de uma frase longa se perdia ao chegar no final.
2. **Falta de Paralelismo**: Como o processamento era sequencial, não era possível aproveitar o poder das GPUs modernas para processar todas as palavras de uma vez, tornando o treinamento lento.

## A Grande Inovação: Self-Attention (Atenção Própria)

A principal inovação do Transformer é o mecanismo de **Self-Attention**.

Em vez de processar as palavras em ordem, a atenção permite que o modelo olhe para **todas as palavras da frase ao mesmo tempo** e determine quais são as mais importantes para entender o significado de cada palavra individual.

> **Analogia**: Imagine que você está lendo a frase: "O robô pegou a bola e a jogou". Ao processar a palavra "a" (a última), o mecanismo de atenção permite que o modelo dê um "peso" maior à palavra "bola" do que à palavra "robô", entendendo que "a" se refere à bola.

Essa capacidade de conectar palavras, independentemente da distância entre elas, permite uma compreensão muito mais profunda do contexto.

## Componentes Principais: Encoders e Decoders

A arquitetura original do Transformer é composta por duas partes:

1. **Encoder (Codificador)**: Sua função é "ler" e "entender" a sequência de entrada (por exemplo, uma frase em português). Ele constrói uma representação numérica rica em contexto para cada palavra.

2. **Decoder (Decodificador)**: Sua função é pegar a representação do encoder e gerar a sequência de saída, palavra por palavra (por exemplo, a tradução da frase para o inglês).

Modelos como o GPT (Generative Pre-trained Transformer) são famosos por usarem principalmente a parte do **Decoder**, pois seu objetivo é gerar texto novo a partir de um prompt inicial. Outros modelos, como o BERT, usam apenas o **Encoder**, pois são focados em tarefas de compreensão de texto, como classificação e análise de sentimento.
