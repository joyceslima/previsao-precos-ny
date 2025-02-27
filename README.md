# 🏠 Previsão de Preços de Aluguéis Temporários em Nova York

Este projeto tem como objetivo desenvolver um modelo preditivo para estimar os preços de aluguéis temporários em Nova York. Para isso, realizamos uma análise exploratória dos dados (EDA), identificamos padrões e utilizamos técnicas de machine learning para criar um modelo robusto de previsão.

### ✨ Objetivos do Projeto

 *Análise exploratória dos dados (EDA)*

1. Investigar padrões entre variáveis.

2. Responder perguntas de negócio, como:

* Onde é mais indicado investir em um imóvel?

* O número de noites mínimas e a disponibilidade afetam o preço?

* Existe um padrão nos nomes dos locais mais caros?

*Desenvolvimento de um modelo preditivo*

* Escolher as melhores variáveis e transformações.

* Testar diferentes modelos e selecionar o mais adequado.

* Avaliar o desempenho utilizando métricas apropriadas.

Salvar o modelo em formato .pkl para uso futuro.

---

### 📚 Dados Utilizados

O dataset contém informações sobre aluguéis temporários, incluindo:

Localização: bairro_group, bairro

Tipo de acomodação: room_type

Preço do aluguel: preco

Requisitos do aluguel: minimo_noites

Disponibilidade: disponibilidade_365

Número de reviews: numero_de_reviews, reviews_por_mes

---

### 🎯 Modelos Utilizados

Foram testados diferentes modelos de Machine Learning:

Regressão Linear - Simples e interpretável, mas não captura relações não lineares.

Random Forest Regressor - Captura relações não lineares entre as variáveis. É robusto contra outliers e overfitting, apresenta um bom equilíbrio entre performance e interpretabilidade.

---

### 📊 Métricas de Avaliação

MAE (Mean Absolute Error): Mede o erro médio absoluto (em dólares).

RMSE (Root Mean Squared Error): Penaliza erros maiores, ajudando a capturar grandes desvios.

R² (Coeficiente de Determinação): Mede o quanto o modelo explica a variação do preço.

Métrica escolhida: MAE (é mais interpretável para valores monetários).

---

### 💡 Como Executar o Projeto

1. Instalar Dependências

        pip install -r requirements.txt

2. Executar o Modelo

        import pickle
        import pandas as pd
        import numpy as np

3. Carregar o modelo salvo

    with open("modelo_precos.pkl", "rb") as arquivo:
        modelo = pickle.load(arquivo)
   
*O arquivo do modelo está disponível para download no [Google Drive](https://drive.google.com/file/d/15YxlV-UuF3RbX5EBtazB8gIkCSqO3mpy/view?usp=sharing).*

**O arquivo pode ser grande (mais de 100MB), então pode demorar alguns minutos para o download ser concluído.**

4. Exemplo de previsão para um novo imóvel

    novo_imovel = pd.DataFrame({...})  # Preencha com os dados do imóvel
    previsao = modelo.predict(novo_imovel)
    print("Preço previsto:", np.expm1(previsao))  # Reverter log-transform

---

### 🌟 Conclusão

O modelo Random Forest Regressor apresentou um bom desempenho na previsão de preços.

A localização e o tipo de acomodação são os fatores mais importantes.

O projeto pode ser aprimorado com mais dados externos (eventos, sazonalidade, etc.).

💰 Pronto para fazer previsões e otimizar investimentos em aluguéis temporários! 🚀

---

### 🤝 Contribuições

Sinta-se à vontade para abrir uma **issue** para contribuir com melhorias no projeto.

