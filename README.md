# AI & Robotics Trends

Material aberto da disciplina **Artificial Intelligence & Robotics Trends**, do MBA em Cyber Security da FIAP (turma 11SEGR).

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?style=flat-square&logo=scikit-learn)
![Colab](https://img.shields.io/badge/Google-Colab-yellow?style=flat-square&logo=googlecolab)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## Sobre

A disciplina percorre IA, Machine Learning e Deep Learning com olhar de segurança e termina nos sistemas agênticos e autônomos: quanto mais autonomia damos a uma IA, mais o controle precisa estar fora do modelo. São 4 aulas de 4 horas.

| Aula | Tema |
|---|---|
| 1 | IA, Machine Learning e segurança (Demos 1 e 2, já disponível) |
| 2 | Aprendizado supervisionado, métricas que importam, regressão logística e árvores (Demos 3 e 4, já disponível) |
| 3 | Deep Learning e o modelo como superfície de ataque (em preparação) |
| 4 | Segurança de sistemas agênticos e autônomos, Robotics Trends (em preparação) |

## Estrutura

```
Datasets/    bases usadas pelas demos
Notebooks/   demos práticas, prontas para rodar no Google Colab
Slides/      decks das aulas
```

> O deck publicado aqui omite as figuras de terceiros (Hype Cycle do Gartner, tiras, memes e mapas de outras fontes), que foram substituídas por versões em texto. Por isso a numeração e o número de slides diferem da versão apresentada em aula.

| Aula | Deck |
|---|---|
| 1 | [IA, ML e segurança](Slides/Aula1_IA_ML_e_Seguranca.pptx) |
| 2 a 4 | em preparação |

## Demos

| Demo | Tema | Conceitos | Colab |
|---|---|---|---|
| [Demo 1](Notebooks/Demo1_URL_Phishing_Classifier.ipynb) | Detectando URLs maliciosas (Kaggle URL Dataset) | Classificação supervisionada, TF-IDF, regressão logística, acurácia x recall, matriz de confusão, pesos de classe, n-gramas de caracteres | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahirtonlopes/AI-and-Robotics-Trends/blob/main/Notebooks/Demo1_URL_Phishing_Classifier.ipynb) |
| [Demo 2](Notebooks/Demo2_URL_Phishing_PhiUSIIL.ipynb) | O modelo funciona fora do laboratório? (PhiUSIIL) | Rótulo invertido, teste entre bases (dataset shift), viés de coleta, limiar de decisão, ataque adversarial de evasão | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahirtonlopes/AI-and-Robotics-Trends/blob/main/Notebooks/Demo2_URL_Phishing_PhiUSIIL.ipynb) |
| [Demo 3](Notebooks/Demo3_Fraud_Detection.ipynb) | Fraude em pagamentos: o que um resultado de 100% esconde | Regressão logística, árvore de decisão, baseline trivial, matriz de confusão, vazamento de dados, limiar de decisão | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahirtonlopes/AI-and-Robotics-Trends/blob/main/Notebooks/Demo3_Fraud_Detection.ipynb) |
| [Demo 4](Notebooks/Demo4_Attack_Detection.ipynb) | Detecção de ataques de rede (UNSW-NB15) em duas camadas | Árvore de decisão com GridSearch por recall, regras interpretáveis, Random Forest, XGBoost, LightGBM, bootstrap do recall | [![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ahirtonlopes/AI-and-Robotics-Trends/blob/main/Notebooks/Demo4_Attack_Detection.ipynb) |

As Demos 1 e 2 são sequenciais: a Demo 2 começa recriando o modelo da Demo 1. A numeração das demos é contínua ao longo das aulas; as próximas entram aqui conforme as aulas forem sendo publicadas. As Demos 3 e 4 são independentes das anteriores.

## Como rodar

Cada notebook abre direto no Google Colab (botão acima). Os notebooks baixam as bases sozinhos: a Kaggle URL Dataset, a base de pagamentos e o UNSW-NB15 vêm da pasta `Datasets/` deste repositório, e a PhiUSIIL vem do UCI. Não é preciso subir arquivo na mão.

Para rodar localmente:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
# Demo 4 também usa:
pip install xgboost lightgbm dtreeviz graphviz
jupyter notebook
```

## Datasets

| Arquivo | Usado em | Origem |
|---|---|---|
| `url_data.csv` | Demo 1 e 2 | Kaggle, `antonyj453/urldataset` |
| `payment_fraud.csv` | Demo 3 | Kaggle, `pwnpen/payment` (licença não informada na origem) |
| `UNSW_NB15_training-set.csv`, `UNSW_NB15_testing-set.csv` | Demo 4 | UNSW-NB15, Moustafa, N. e Slay, J. (2015), UNSW Canberra. Uso acadêmico com citação do artigo *UNSW-NB15: a comprehensive data set for network intrusion detection systems*, MilCIS 2015 |
| (baixada pelo notebook) | Demo 2 | PhiUSIIL Phishing URL Dataset, UCI (id 967), CC BY 4.0. Prasad, A. e Chandra, S. (2024), *Computers & Security* |

As bases pertencem aos respectivos autores. Consulte a licença e as condições de uso de cada uma antes de reutilizá-las fora do contexto da disciplina.

## Licença

Código e notebooks sob licença MIT (veja `LICENSE.md`).

---

Prof. Dr. Ahirton Lopes
