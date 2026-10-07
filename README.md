## Modelos de Variáveis Aleatórias Aplicados à Biologia

**Curso:** Ciências Biológicas  
**Instituição:** Escola Superior de Agricultura "Luiz de Queiroz" — Universidade de São Paulo (USP / ESALQ)  
**Disciplina:** Probabilidade e Estatística em Biologia  
**Docente:** Prof. Dr. Cristian Marcelo Villegas Lobos  
**Atividade:** Tarefa 13 — Distribuições de Probabilidade Continuas Aplicadas a Dados Biológicos Reais**, desenvolvida para a disciplina de Estatística/Data Science.

---

## Integrantes

* **Raianne Brazão Magalhães** — Nº USP: `16898499` — Ciências Biológicas  
* **Tiago Monteiro** — Nº USP: `16991607` — Ciências Biológicas  
* **Vitória Fontes Ortiz** — Nº USP: `16904821` — Ciências Biológicas  

---

# Modelagem Probabilística e Análise Estatística em Ciências Biológicas

Este repositório contém a resolução da **Tarefa 13 — Distribuições de Probabilidade Aplicadas a Dados Biológicos**, desenvolvida para investigar como as distribuições **Normal**, **t de Student**, **Qui-quadrado ($\chi^2$)** e **F de Fisher** auxiliam na resposta a perguntas sobre dados morfológicos reais.

---

## Pergunta Biológica Investigável

> **Pergunta Guia:** *"A variabilidade da largura da sépala (`sepal_width`) difere significativamente entre a espécie Iris setosa e a espécie Iris versicolor?"*

* **Justificativa:** *Iris setosa* e *Iris versicolor* são espécies adaptadas a diferentes nichos e apresentam graus de rigidez morfológica distintos. Comparar a dispersão e a razão de variâncias amostrais da largura da sépala permite testar a hipótese de homocedasticidade (igualdade de variâncias), fundamental para validar a aplicação de testes paramétricos de comparação de médias.

---

## Ficha Técnica da Base de Dados

* **Nome do conjunto de dados:** Iris Species Dataset
* **Link de acesso:** [UCI Machine Learning Repository - Iris](https://archive.ics.uci.edu/dataset/53/iris)
* **Instituição responsável:** University of California, Irvine (UCI) — Dados originais de Edgar Anderson (1935) e analisados por Ronald A. Fisher (1936).
* **Data de acesso:** 06 de outubro de 2026.
* **Significado de cada linha:** As medições morfológicas obtidas de um espécime florístico individual.
* **Unidade experimental:** Uma flor individual do gênero *Iris*.
* **Variáveis utilizadas:**
  * `sepal_width`: Largura da sépala medida em centímetros (cm) — variável contínua.
  * `species`: Espécie biológica da planta (*Iris setosa*, *Iris versicolor*, *Iris virginica*) — variável categórica.
* **Critério de seleção:** Foram selecionados os registros contínuos de $n_1 = 50$ espécimes de *Iris setosa* e $n_2 = 50$ espécimes de *Iris versicolor*.
* **Tratamento de dados ausentes:** O conjunto possui 150 observações completas sem valores nulos (*missing values*).

---

## Estrutura do Estudo Teórico e Prático

O trabalho está organizado no notebook em quatro seções principais, discriminando claramente a **medida biológica observada** da **estatística modelada**:

| Distribuição | Objeto da Modelagem | Aplicação Biológica no Trabalho |
| :--- | :--- | :--- |
| **Normal** | Medida individual ($X_i$) | Modelo paramétrico para a largura individual da sépala de *Iris setosa*. |
| **t de Student** | Média amostral padronizada ($\bar{X}$) | Flutuação amostragem da média padronizada da largura da sépala ($n=50$). |
| **Qui-quadrado ($\chi^2$)** | Variância amostral escalonada ($s^2$) | Distribuição da estimativa da variância amostral da largura da sépala sob uma hipótese populacional $\sigma_0^2$. |
| **F de Fisher** | Razão de variâncias ($s_1^2 / s_2^2$) | Comparação da razão entre as variâncias amostrais de *Iris versicolor* e *Iris setosa*. |

---

## Tecnologias e Bibliotecas Utilizadas

* **Linguagem:** Python 3.10+
* **Processamento de Dados:** `pandas`, `numpy`
* **Cálculos Estatísticos:** `scipy.stats` (funções `pdf`, `cdf`, `sf`, `ppf`)
* **Visualização Gráfica:** `matplotlib`, `seaborn`

---

## Estrutura do Repositório

```text
.
├── README.md                              # Apresentação do projeto e instruções
├── tarefa13_Python_Ciencias_Biologicas.ipynb  # Notebook executável com teoria, código e gráficos
└── requirements.txt                       # Lista de dependências Python
