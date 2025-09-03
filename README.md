# README.md
# 🚀 Classificação de Imagens com Rede Neural Convolucional (CNN)

Este projeto implementa e treina um modelo de Rede Neural Convolucional (CNN) para a classificação de imagens utilizando o conjunto de dados **CIFAR-10**. O objetivo é demonstrar o fluxo de trabalho completo de um projeto de Deep Learning, desde o pré-processamento dos dados até a avaliação do modelo.

---

### 🎯 Objetivo do Projeto

O objetivo principal é classificar 60.000 imagens de 10 classes diferentes (como aviões, carros, pássaros, etc.) de forma automatizada. A acurácia do modelo será a principal métrica para avaliar o seu desempenho.

---

### ⚙️ Etapas do Projeto

O código segue um fluxo de trabalho padrão para problemas de classificação de imagens:

1.  **Carregamento e Pré-processamento dos Dados:**
    * O conjunto de dados CIFAR-10 é carregado diretamente do `tensorflow.keras.datasets`.
    * As imagens são normalizadas para um intervalo de 0 a 1, o que é uma prática recomendada para o treinamento de redes neurais.

2.  **Criação da Arquitetura da CNN:**
    * Uma rede neural sequencial é construída com camadas de **Convolução (`Conv2D`)** para extrair as características das imagens.
    * Camadas de **Pooling (`MaxPooling2D`)** são usadas para reduzir a dimensionalidade e o número de parâmetros, mantendo as características essenciais.
    * As últimas camadas (`Flatten` e `Dense`) são responsáveis pela classificação final das 10 classes.

3.  **Treinamento e Avaliação do Modelo:**
    * O modelo é compilado com um otimizador (`adam`) e uma função de perda (`SparseCategoricalCrossentropy`).
    * É treinado por 10 épocas, com a acurácia sendo monitorada para avaliar o progresso do aprendizado.
    * Por fim, o modelo é avaliado com um conjunto de dados de teste para verificar sua performance em dados não vistos.

---

### 💻 Tecnologias e Bibliotecas Utilizadas

* **Python:** Linguagem de programação principal.
* **TensorFlow & Keras:** Principais frameworks para a construção e treinamento da rede neural.
* **NumPy:** Utilizado para manipulação de arrays e dados numéricos.
* **Matplotlib:** Para a visualização dos resultados.
* **Scikit-learn:** Para métricas e funções de apoio.
* **OpenCV (`cv2`):** Para manipulação de imagens.

---

### 📄 Como Executar o Código

Para rodar este projeto em sua máquina, siga os passos abaixo:

1.  **Instale as dependências:**
    ```bash
    pip install tensorflow keras numpy matplotlib opencv-python
    ```
    
2.  **Execute o script Python:**
    ```bash
    python atividade1_Aula10_CNN.ipynb
    ```
    *Executado no ambiente do `Google Colab`*

---

### 📈 Resultados Esperados

Ao executar o script, o console exibirá o progresso do treinamento a cada época, incluindo a perda (`loss`) e a acurácia. No final, será impressa a acurácia final do modelo no conjunto de dados de teste.
