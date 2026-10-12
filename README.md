# 🚗 Predição de Aceitação de Cupons Promocionais em Veículos

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Dataset UCI](https://img.shields.io/badge/UCI%20ML%20Repo-ID%20603-blue?style=for-the-badge)](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation)

Projeto de Ciência de Dados e Aprendizado de Máquina desenvolvido para prever e analisar os padrões de decisão de motoristas ao receberem cupons de desconto contextuais (restaurantes, cafeterias, bares, etc.) durante a condução.

---

## 📌 Visão Geral do Projeto

O objetivo deste projeto é construir um pipeline completo de Machine Learning capaz de identificar com precisão a probabilidade de um cliente aceitar um cupom promocional enquanto dirige. O estudo visa fornecer insights valiosos para estratégias de **marketing geolocalizado** e **otimização de conversão de campanhas publicitárias**.

### 🎯 Principais Objetivos
- **Análise Exploratória de Dados (EDA):** Identificar a distribuição de variáveis categóricas/numéricas e correlações entre fatores contextuais.
- **Tratamento de Dados:** Tratar valores faltantes com imputação por moda (`SimpleImputer`) e codificar atributos via `LabelEncoder`.
- **Treinamento e Comparação de Modelos:** Comparar o desempenho entre **Random Forest Classifier** e **Extra Trees Classifier**.
- **Otimização de Hiperparâmetros:** Utilizar busca exaustiva via `GridSearchCV` combinada com validação cruzada 5-fold.
- **Interpretabilidade:** Avaliar a importância de cada atributo na tomada de decisão dos modelos.
- **Implementação Didática:** Demonstração algorítmica de divisão recursiva de uma árvore puramente aleatória (*Totally Random Tree*).

---

## 📊 Análise Exploratória e Visualizações

Durante a fase de análise exploratória, foram examinadas a correlação entre as variáveis e a distribuição dos atributos numéricos:

<div align="center">

### Matriz de Correlação
![Matriz de Correlação](Matriz_Correlacao.jfif)

### Distribuição das Variáveis Numéricas
![Distribuição das Variáveis Numéricas](Distribuicao_de_variaveis_numericas.jfif)

</div>

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **[Python](https://www.python.org/)** (Linguagem base)
- **[UCI ML Repository (`ucimlrepo`)](https://github.com/uci-ml-repo/ucimlrepo)**: Aquisição programática do conjunto de dados oficial.
- **[Scikit-Learn](https://scikit-learn.org/)**:
  - Pré-processamento (`SimpleImputer`, `LabelEncoder`, `train_test_split`)
  - Modelagem (`RandomForestClassifier`, `ExtraTreesClassifier`)
  - Otimização e Validação (`GridSearchCV`, `cross_val_score`, `accuracy_score`)
- **[Pandas](https://pandas.pydata.org/) & [NumPy](https://numpy.org/)**: Manipulação e análise estruturada dos dados.
- **[Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/)**: Geração de gráficos estatísticos e matrizes térmicas.

---

## 📁 Estrutura do Repositório

```bash
Banco_de_dados/
│
├── banco_de_dados.py                     # Script principal com pipeline completo de ML
├── Distribuicao_de_variaveis_numericas.jfif  # Visualização: histogramas das variáveis numéricas
├── Matriz_Correlacao.jfif                 # Visualização: mapa de calor da correlação
├── requirements.txt                       # Dependências do projeto para instalação
├── .gitignore                             # Regras de exclusão do Git
└── README.md                              # Documentação detalhada do repositório
```

---

## 🚀 Pipeline de Execução

1. **Carregamento dos Dados:** Consumo direto do dataset *In-Vehicle Coupon Recommendation* da UCI (`id=603`).
2. **EDA:** Exibição das estatísticas do dataset, checagem de nulos e plotagem de correlações.
3. **Pré-processamento:**
   - Imputação de dados faltantes utilizando a categoria mais frequente.
   - Conversão de variáveis categóricas textuais em numéricas com `LabelEncoder`.
4. **Divisão Treino/Teste:** Divisão estratificada de 70% para treinamento e 30% para teste.
5. **Otimização de Hiperparâmetros:**
   - Grid Search avaliando combinações de `n_estimators`, `max_depth`, `min_samples_split` e `min_samples_leaf`.
6. **Avaliação e Resultados:**
   - Avaliação por Acurácia em dados de teste nunca vistos.
   - Ranking de *Feature Importance* para cada modelo.
7. **Algoritmo Customizado:** Demonstração didática recursiva de geração de árvore de decisão totalmente aleatória.

---

## ⚙️ Como Executar o Projeto Localmente

### 1. Pré-requisitos
Certifique-se de ter o Python 3.9+ instalado em seu ambiente.

### 2. Clonar o repositório
```bash
git clone https://github.com/PedroLssouza/Banco_de_dados.git
cd Banco_de_dados
```

### 3. Criar e ativar um ambiente virtual (recomendado)
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux / MacOS
python3 -m venv venv
source venv/bin/activate
```

### 4. Instalar as dependências
```bash
pip install -r requirements.txt
```

### 5. Executar o script
```bash
python banco_de_dados.py
```

---

## 👨‍💻 Autor

Desenvolvido por **[Pedro Lucas Souza](https://github.com/PedroLssouza)**.

Caso tenha gostado ou queira contribuir com melhorias, fique à vontade para abrir uma *Issue* ou enviar um *Pull Request*! 🚀
