# 📀 Análise Exploratória de Álbuns

Este projeto tem como objetivo analisar um conjunto de álbuns musicais utilizando Python, Pandas, visualizações estatísticas e métricas musicais como *energy*, *valence*, *danceability* e outras audio features. A meta principal é construir um catálogo limpo, visual e interpretado, servindo tanto como treino técnico quanto como uma introdução à exploração de dados musicais.

---

## 🎯 Objetivos

* Organizar e limpar os dados provenientes do arquivo `albums.csv`.
* Realizar uma análise exploratória detalhada das principais características musicais.
* Visualizar padrões por meio de gráficos (histogramas, scatterplots e heatmaps).
* Gerar pequenos insights sobre preferências musicais.
* Estruturar um projeto reprodutível com pastas, notebook e exportação de figuras.

---

## 📂 Estrutura do Projeto

```
catalogo-albuns/
├─ data/
│  └─ albums.csv
├─ notebooks/
│  └─ analysis.ipynb
├─ src/
│  └─ utils.py
├─ outputs/
│  ├─ figures/
│  └─ tables/
├─ README.md
└─ requirements.txt
```

---

## 🧪 Tecnologias utilizadas

* **Python 3.10+**
* **Pandas** (manipulação de dados)
* **Matplotlib / Seaborn** (visualização)
* **Jupyter Notebook**

---

## ▶️ Como executar o projeto

### 1. Criar ambiente virtual (opcional)

```bash
python -m venv .venv
# Linux/macOS
source .venv/bin/activate
# Windows PowerShell
./.venv/Scripts/Activate.ps1
```

### 2. Instalar dependências

```bash
pip install -r requirements.txt
```

### 3. Abrir o notebook

```bash
jupyter lab
```

Abra o arquivo:

```
notebooks/analysis.ipynb
```

---

## 📊 Principais análises incluídas

* Distribuição das audio features (valence, energy, danceability...)
* Heatmap de correlação entre métricas musicais
* Relação entre **energy** e **valence**
* Álbuns por década
* Artistas mais frequentes no catálogo
* Identificação de álbuns com valores extremos em métricas musicais

---

## 🖼️ Visualizações principais

O projeto inclui figuras exportadas automaticamente para `outputs/figures/`, como:

* Histogramas com KDE para cada feature musical
* Heatmap de correlação
* Scatterplot de `energy` vs `valence` com diferenciação visual por categorias


![texto alternativo](/outputs/figures/hist_acousticness.png)

A grande maioria está nos extremos (álbuns totalmente acústicos ou nada acústicos).

![texto alternativo](/outputs/figures/hist_danceability.png)

Os álbuns se concentram no meio termo, albúns com presença de 'danceability', mas nada exagerado.

![texto alternativo](/outputs/figures/hist_energy.png)

No caso de 'energy', a presença é bem espalhada, mas com uma pequena maioria nos meio termos.

![texto alternativo](/outputs/figures/hist_instrumentalness.png)

Percebe-se que a grande maioria dos álbuns, não possuem músicas instrumentais.

![texto alternativo](/outputs/figures/hist_speechiness.png)

Como no caso anterior, musicas mais faladas sem presença de instrumentos são extremamente raras.

![texto alternativo](/outputs/figures/hist_valence.png)

A presença de valência assim com a energia, é bastante variada.

![texto alternativo](/outputs/figures/corr_heatmap.png)

Alguns insights lógicos, músicas energéticas precisam ter instrumentos, valência e energia normalmente andam na mesma direção, assim como valência e 'danceability'.

![texto alternativo](/outputs/figures/energy_valence_scatter.png)
---

## 🔍 Exemplos de insights gerados

* A maior parte dos álbuns tende a se concentrar em valores intermediários de **energy**, sugerindo preferência por música equilibrada entre intensidade e suavidade.
* A distribuição de **valence** (positividade emocional) indica tendência a álbuns com menor tom alegre e maior carga emocional.
* A correlação entre *danceability* e *energy* indica que músicas mais energéticas geralmente são também mais dançáveis.
* Algumas décadas mostram picos de produção no catálogo, indicando períodos musicais preferidos.

---

## 🗂️ Dados limpos

O dataset limpo é salvo como:

```
outputs/tables/albums_clean.csv
```

Ele contém:

* Colunas padronizadas
* Tipos corrigidos
* Audio features sem valores ausentes
* Coluna adicional `primary_artist`
* Coluna `decade` derivada do ano

---

## 🚀 Próximos Passos e Melhorias

* Implementar recomendações musicais simples usando similaridade vetorial (cosine similarity).
* Criar um dashboard com **Streamlit** para explorar áudio interativamente.
* Expandir dados via API do Spotify (capa, gêneros, popularidade, previews).
* Agrupar álbuns por gênero e comparar métricas.
* Construir uma timeline musical mostrando evolução das preferências.

---

## 📝 Licença

Projeto de uso pessoal para aprendizado, livre para reutilização educacional.

---

Se quiser, posso gerar também figuras exemplo para inserir aqui, ou criar automaticamente um texto de "Insights finais" baseado no seu CSV real.
