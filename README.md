# Ciência de Dados — Notebooks

![Python](https://img.shields.io/badge/Python-3.14-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.9-F7931E?logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-3.0-150458?logo=pandas&logoColor=white)
![status](https://img.shields.io/badge/status-concluído-success)

Notebooks Jupyter desenvolvidos na disciplina de Aplicação de Ciência de
Dados do 3° semestre de Tecnologia em Sistemas para Internet (TSI): uma
comparação de técnicas de imputação e codificação em um dataset financeiro
sintético e uma comparação de algoritmos de regressão na base Diabetes.

## Sumário

- [Visão geral](#visão-geral)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Como executar](#como-executar)
- [Stack técnica](#stack-técnica)
- [Autor](#autor)

## Visão geral

| Notebook | Descrição |
|---|---|
| [`Imputação_Avançada.ipynb`](Imputação_Avançada.ipynb) | Gera um dataset financeiro sintético com valores ausentes e compara um pipeline avançado (MICE / KNNImputer + `SmoothedTargetEncoder` customizado) com um baseline simples (`SimpleImputer` + `OrdinalEncoder`) por validação cruzada estratificada, usando ROC-AUC e Average Precision |
| [`Atividade Regressão Diabetes/`](Atividade%20Regress%C3%A3o%20Diabetes/) | Compara `DummyRegressor`, `LinearRegression`, `Ridge` e `RandomForestRegressor` na base Diabetes do scikit-learn (442 pacientes), com validação cruzada de 5 folds e avaliação final em teste (MAE, RMSE e R²) |

## Estrutura do projeto

```
.
├── Imputação_Avançada.ipynb
├── Atividade Regressão Diabetes/
│   ├── Atividade_Regressao_Diabetes.ipynb
│   └── figuras/                 # Gráficos gerados pelo notebook (PNG)
└── requirements.txt
```

## Como executar

```bash
git clone https://github.com/plfrancisco/regressao-diabetes-dataset.git
cd regressao-diabetes-dataset

# Ambiente virtual e dependências
python -m venv .venv
.venv\Scripts\activate           # Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt

# Abrir os notebooks
jupyter notebook
```

Os dois notebooks são independentes e não exigem arquivos de dados: um gera
os dados de forma sintética e o outro usa `load_diabetes` do scikit-learn.

## Stack técnica

Python · Jupyter · pandas · NumPy · scikit-learn · Matplotlib · seaborn

## Autor

**Pedro Lucas Francisco**
