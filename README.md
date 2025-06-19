# 🧠 KNN from Scratch

Este projeto implementa o algoritmo **K-Nearest Neighbors (KNN)** do zero, sem o uso de bibliotecas de machine learning como `scikit-learn`. Além da implementação básica, ele também inclui:

- Avaliação automática com várias métricas (accuracy, precision, recall, f1-score)
- Visualização gráfica das métricas em função do valor de K
- Suporte a múltiplos datasets: Iris, Wine, Digits e Fashion MNIST
- Padronização dos dados
- Cronômetro de execução para experimentos com datasets maiores

---

## 🔍 Sobre o Algoritmo

O **KNN** é um algoritmo de classificação baseado em instâncias. Para classificar uma nova amostra:

1. Calcula a distância entre a amostra e todos os dados de treino (neste caso, distância euclidiana).
2. Seleciona os **K vizinhos mais próximos**.
3. Realiza uma votação majoritária para decidir a classe da amostra.

É simples, mas poderoso, especialmente para problemas onde a separação entre classes é bem definida.
---

## ⚙️ Como Funciona

### 1. Implementação do KNN

* A classe `KNN` possui os métodos `fit()` e `predict()`, funcionando de forma semelhante ao `sklearn`.
* O método `predict()` imprime o progresso e usa votação majoritária com `collections.Counter`.

### 2. Avaliação com `evaluate_knn_on_dataset()`

Essa função:

* Divide os dados em treino e teste
* Avalia o modelo para vários valores de K
* Calcula `accuracy`, `precision`, `recall` e `f1-score` para ambos os conjuntos
* Plota gráficos para cada métrica

---

## 🧪 Datasets Utilizados

### ✅ Datasets Clássicos (`sklearn.datasets`)

* **Iris**: classificação de flores (3 classes, 4 features)
* **Wine**: tipos de vinho (3 classes, 13 features)
* **Digits**: dígitos manuscritos (10 classes, 64 features)

### 🧥 Fashion MNIST (`tensorflow.keras.datasets`)

* Imagens 28x28 de roupas (10 classes, 70.000 exemplos)
* Para reduzir o tempo de execução com KNN, uma amostra de 10% é utilizada
* As imagens são achatadas (28x28 → 784) antes da padronização

---

## 📊 Exemplo de Gráfico Gerado

A função `evaluate_knn_on_dataset()` gera gráficos como este para cada dataset:
![image](https://github.com/user-attachments/assets/0382940d-903f-480c-8425-5909e2229adb)

* 4 subplots: **Accuracy**, **Precision**, **Recall**, **F1-Score**
* Cada métrica é exibida para treino e teste, variando o valor de **K**

---

## 🕒 Cronômetro de Execução

O tempo de execução do experimento com o Fashion MNIST é exibido ao final com:

```python
start_time = time.time()
...
end_time = time.time()
print(f'Execution time: {execution_time:.2f} seconds')
```

---

## 💡 O que você vai aprender com esse projeto

* Como o algoritmo KNN funciona internamente
* Como calcular distâncias, fazer votação majoritária e padronizar dados
* Como avaliar classificadores com métricas reais
* Como lidar com diferentes formatos de dados (imagens vs vetores)
* Como criar gráficos informativos com `matplotlib`

---

## 🧠 Extensões possíveis

Se quiser continuar o projeto:

* Implementar distância de Manhattan, Chebyshev, etc.
* Suportar K ponderado pela distância
* Implementar busca de K ótimo com validação cruzada
* Adaptar para problemas de regressão
* Criar interface web com Streamlit

---

## 📌 Observações

* KNN é simples, mas muito sensível à escala dos dados — **a padronização é essencial.**
* Em datasets grandes, o KNN pode ser lento, pois precisa comparar com todas as amostras de treino (por isso usamos amostragem no Fashion MNIST).
* Este projeto foi feito com foco educacional, não em performance máxima.

---

## 👨‍💻 Autor

**Pedroza (projeto pessoal de aprendizado)**

* Estudante de Ciência da Computação
* Foco em Inteligência Artificial e Aprendizado de Máquina
* Vive como um estoico moderno: estuda com propósito, sem vaidade

---

## 📜 Licença

Este projeto é de uso livre para fins educacionais e pessoais.

```

---

Se quiser posso gerar esse README direto em `.md`, ou adaptar para algum template específico (tipo do GitHub ou Kaggle).
```
