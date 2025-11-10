# 📱 Classificação de Mensagens SMS Usando Aprendizado de Máquina

Este projeto aplica técnicas de **aprendizado de máquina** para **detecção automática de mensagens de spam** em SMS.  
Utiliza o conjunto de dados público [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset/data), amplamente usado em estudos de processamento de linguagem natural (PLN).

---

## 📊 Sobre o Dataset

O dataset contém **5.572 mensagens** rotuladas como:

- **ham** → mensagens legítimas (4.825 registros)  
- **spam** → mensagens indesejadas (747 registros)

**Colunas principais:**
- `label` — rótulo original (`ham` ou `spam`), convertido para binário (`0 = ham`, `1 = spam`)
- `message` — texto completo da mensagem
- `message_processed` — versão pré-processada do texto (pontuação removida, stopwords filtradas, lematização)

---

## 🎯 Objetivos do Projeto

- Realizar **análise exploratória** e verificação do balanceamento das classes  
- Aplicar **pré-processamento de texto**:  
  - remoção de pontuação  
  - remoção de stopwords  
  - lematização  
- Converter textos em representações numéricas usando **TF-IDF**
- Treinar e comparar diferentes **modelos supervisionados de classificação**
- Avaliar métricas de desempenho como:
  - *Acurácia*
  - *Precisão*
  - *Recall*
  - *F1-Score*
  - *Matriz de confusão*

---

## 🤖 Modelos Utilizados

- **Multinomial Naive Bayes**
  - aplicado sobre o texto original e também sobre o texto pré-processado
- **Regressão Logística**
  - aplicada sobre o texto pré-processado

---

## 🧩 Tecnologias e Bibliotecas

- **Python 3.x**
- **Pandas**, **NumPy** — manipulação e análise de dados  
- **scikit-learn** — modelagem e métricas de aprendizado de máquina  
- **NLTK / spaCy** — pré-processamento e lematização  
- **Matplotlib / Seaborn** — visualizações e matrizes de confusão  

---

## 📈 Resultados

Os modelos apresentaram **alto desempenho** na detecção de spam, com o **Multinomial Naive Bayes** mostrando resultados particularmente satisfatórios após o pré-processamento de texto.  
A abordagem combinando **TF-IDF + Naive Bayes** obteve excelente equilíbrio entre **precisão** e **recall**, confirmando sua eficácia para tarefas de classificação de mensagens curtas.

---

## 🧠 Conclusão

O projeto demonstra que técnicas clássicas de **aprendizado de máquina** aliadas a um bom **pré-processamento de linguagem natural** são altamente eficazes para identificar spam em mensagens SMS.  
Essa base pode ser facilmente expandida para sistemas de filtragem em e-mails, redes sociais e aplicativos de mensagens instantâneas.
