# Machine Learning

Duas disciplinas distintas que se relacionam com este contexto de aprendizado de máquina:

- Ciência de Dados
- Engenharia de Software

## O que é Machine Learning?

O aprendizado de máquina é como uma função, ele vai literalmente encapsular uma função.
Estamos muito associados a questões matemáticas e estátisticas.

1. Dados de Treinamento: Observações anteriores.
2. Algoritmo: Generaliza a relação entre x e y como uma função.
3. Modelo: Encapsula a função.
4. Inferência de Dados (recursos não rotulados) e Predição (Rótulo inferido).

Treinamento engloba dados, algoritmo e modelo.
Inferência engloba a saída, é o processo de prever novos valores.

### Tipos de Aprendizado de Máquina

- Supervisionado: Dados rotulados.
  - Classificação: Rótulo é uma categorização (ou classe).
    - Binária: Sim ou Não (Label é ou não é uma classe).
      - Preveja se um paciente corre risco de diabetes com base em dados clinicos.
    - Multiclasse: Label é uma das múltiplas classes.
      - Preveja a espécie de um pinguim com base em suas medidas.
  - Regressão: Rótulo é um valor numérico (vai ser um valor quantitativo).
    - Preveja o numero de sorvetes vendidos com base no dia, estação e clima.
- Não Supervisionado: Dados não rotulados.
  - Classificação: Rótulo é uma categorização (ou classe).
    - Separe as plantas em grupos com base em caracteristicas comuns.

### Treinamento e Avaliação de Modelos

Multiplas iterações de treinamento com diferentes algoritmos e parâmetros.

1. Dados.
2. Algoritmo.
3. Modelo.
4. Inferência.
5. Avalie o Modelo (Complementa a lista acima): Compare os rótulos previstos com rótulos reais.

## O que é Deep Learning?

Usa Redes Neurais Artificiais, baseadas em redes neurais biológicas/humanas.

- Neurônios disparam em resposta a estímulos eletroquímicos.
- Quando disparado, o sinal é passado para neurônios conectados.
- Cada neurônio é uma função que opera com um valor de entrada (x) e um peso (w).
- A função é envolvida em uma função de ativação que determina se a saída deve ser transmitida.
