# 🚀 O que é Deep Learning (DL)?

**Deep Learning (DL)**, ou Aprendizado Profundo, é um subcampo especializado do Machine Learning que utiliza **Redes Neurais Artificiais** com muitas camadas (daí o termo "profundo" ou *deep*).

Enquanto o Machine Learning tradicional pode exigir que um especialista ajude a extrair as características mais importantes dos dados (um processo chamado *feature engineering*), o Deep Learning é capaz de aprender essas características diretamente dos dados brutos, de forma hierárquica.

## A Estrutura: Redes Neurais Artificiais

A inspiração para o Deep Learning vem da estrutura do cérebro humano.

- **Neurônio Artificial**: É a unidade básica. Ele recebe várias entradas, cada uma com um peso (que indica sua importância), e aplica uma função matemática (função de ativação) para produzir uma saída.
- **Camadas (Layers)**: Os neurônios são organizados em camadas. Uma rede neural profunda tem uma camada de entrada, uma camada de saída e múltiplas **camadas ocultas** (*hidden layers*) entre elas.
- **Aprendizado Hierárquico**: Cada camada aprende a detectar características em um nível de abstração diferente. Em uma tarefa de reconhecimento de imagem, as primeiras camadas podem aprender a identificar bordas e cores, as camadas intermediárias podem aprender a combinar essas bordas para formar olhos e narizes, e as camadas finais podem aprender a identificar um rosto completo.

![Rede Neural](./assets/neural-network.png)

## Como o Deep Learning Aprende?

O processo de treinamento de uma rede neural profunda, chamado de **Backpropagation** (Retropropagação), funciona da seguinte forma:

1. A rede faz uma previsão.
2. Calcula-se o "erro" (a diferença entre a previsão e o resultado correto).
3. Esse erro é propagado de volta através da rede, da última camada para a primeira.
4. Ao longo do caminho, os pesos de cada neurônio são ajustados ligeiramente para tentar reduzir o erro na próxima vez.

Este processo é repetido milhões de vezes com muitos dados, permitindo que a rede "aprenda" a mapear entradas complexas para as saídas corretas.

## Por que é tão importante para a IA Generativa?

A capacidade do Deep Learning de entender padrões extremamente complexos em dados não estruturados (como texto, imagens e som) é o que torna a IA Generativa possível. Arquiteturas como os **Transformers** e os **Modelos de Difusão** são todas baseadas em princípios de Deep Learning.
