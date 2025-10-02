# 🗺️ Roadmap de Estudos em IA Generativa

Este roadmap foi projetado para guiar iniciantes no campo da Inteligência Artificial Generativa, começando pelos conceitos fundamentais e progredindo para tópicos mais avançados. A estrutura é modular, permitindo um aprendizado passo a passo.

Use as caixas de seleção para marcar os tópicos que você já concluiu.

---

## Módulo 1: Fundamentos (A Base para Desenvolvedores)

- [ ] **O que é Inteligência Artificial (IA)?**
  - [ ] Entender a diferença entre IA, Machine Learning (ML) e Deep Learning (DL).
- [ ] **Principais Paradigmas de Machine Learning**
  - [ ] Aprendizado Supervisionado (ex: Classificação, Regressão).
  - [ ] Aprendizado Não Supervisionado (ex: Clusterização).
  - [ ] Aprendizado por Reforço.
- [ ] **Deep Learning Básico**
  - [ ] O que são Redes Neurais? (Neurônios, Camadas, Funções de Ativação).
  - [ ] Intuição sobre como as redes neurais aprendem (Backpropagation e Gradiente Descendente).

## Módulo 2: Introdução à IA Generativa

- [ ] **O que são Modelos Generativos?**
  - [ ] Diferença entre modelos Generativos e Discriminativos.
  - [ ] Breve história: de VAEs e GANs aos Transformers.
- [ ] **Large Language Models (LLMs)**
  - [ ] O que é um LLM e como ele funciona em alto nível?
  - [ ] Conceitos chave: Tokens, Vocabulário e Janela de Contexto.

## Módulo 3: Arquiteturas e Conceitos Essenciais

- [ ] **A Arquitetura Transformer**
  - [ ] Entender o mecanismo de *Self-Attention* (Atenção).
  - [ ] Papel dos Encoders e Decoders.
  - [ ] Como a arquitetura Transformer revolucionou o processamento de linguagem natural.
- [ ] **Modelos de Difusão (Para Imagens)**
  - [ ] Intuição sobre como modelos como DALL-E 2/3 e Stable Diffusion geram imagens.
- [ ] **Embeddings**
  - [ ] O que são *Word Embeddings* e por que são importantes?

## Módulo 4: Ferramentas e Ecossistema Prático

- [ ] **Hugging Face**
  - [ ] Explorar o [Hugging Face Hub](https://huggingface.co/models) (Modelos, Datasets).
  - [ ] Usar a biblioteca `transformers` para carregar um modelo e um tokenizador pré-treinado.
- [ ] **APIs de Modelos como Serviço**
  - [ ] Fazer a primeira chamada para a API da OpenAI, Google (Gemini), Anthropic (Claude), etc.
  - [ ] Entender o uso dos SDKs oficiais (ex: `openai-python`).
- [ ] **Executando Modelos Localmente**
  - [ ] Experimentar ferramentas como Ollama ou LM Studio para rodar LLMs no seu próprio computador.

## Módulo 5: Construindo Aplicações com LLMs

- [ ] **Engenharia de Prompt**
  - [ ] Técnicas básicas: Instruções claras, *Zero-shot*, *One-shot* e *Few-shot prompting*.
  - [ ] Entender o conceito de *Chain-of-Thought*.
- [ ] **Retrieval-Augmented Generation (RAG)**
  - [ ] O que é RAG e por que é essencial para evitar alucinações e usar dados privados.
  - [ ] Introdução a *Vector Databases* (ex: ChromaDB, FAISS).
  - [ ] Construir um pipeline de RAG simples: `Load -> Split -> Embed -> Store -> Retrieve -> Generate`.
- [ ] **Function Calling & Tools**
  - [ ] Entender como um LLM pode decidir chamar uma função externa (API, banco de dados, etc.).
  - [ ] Implementar uma chamada de função usando a API da OpenAI ou similar.
- [ ] **Frameworks de Orquestração**
  - [ ] Primeiros passos com LangChain ou LlamaIndex para construir uma aplicação simples.

## Módulo 6: Tópicos Avançados e Produção

- [ ] **Fine-Tuning (Ajuste Fino)**
  - [ ] Diferença entre *Full Fine-Tuning* e *Parameter-Efficient Fine-Tuning* (PEFT), como LoRA.
- [ ] **Construção de Agentes de IA Personalizados**
  - [ ] O que são agentes e como eles usam LLMs para raciocinar (ciclo `ReAct`: Reason + Act).
  - [ ] Construir um agente simples que pode usar múltiplas ferramentas (ex: uma calculadora e um buscador web).
- [ ] **Ética e Segurança em IA**
  - [ ] Estudar sobre vieses, alucinações, privacidade e uso responsável da tecnologia.
  - [ ] Técnicas de *Prompt Injection* e como se defender.
- [ ] **Avaliação e Observabilidade (LLM-Ops)**
  - [ ] Como avaliar a qualidade das respostas de um LLM? (ex: RAGAS, TruLens).
  - [ ] Entender a importância de monitorar custos, latência e performance em produção.