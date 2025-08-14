# 📊 Análise IEDO — Índice de Eficiência dos Desarmes Ofensivos

Este projeto realiza a análise do **Índice de Eficiência dos Desarmes Ofensivos (IEDO)** em competições de futebol, com base em dados de jogadores e equipes.  
O IEDO é uma métrica desenvolvida para avaliar a eficiência defensiva ofensiva de atletas e times, considerando ações de desarme com impacto no ataque.

## 📂 Estrutura do Projeto

```
Analise-IEDO-main/
│── ENG-Premier League_2024_PLAYERS.csv   # Dados de jogadores
│── ENG-Premier League_2024_TEAMS.csv     # Dados de equipes
│── FiltragemIEDO.ipynb                    # Filtragem de dados por jogador
│── FiltragemIEDOTIME.ipynb                # Filtragem de dados por equipe
│── clustering.ipynb                       # Análise e agrupamento de jogadores
│── criatabela.ipynb                       # Criação de tabela de métricas (jogadores)
│── criatabelatimes.ipynb                  # Criação de tabela de métricas (times)
```

## 📐 Fórmula do IEDO

A métrica é calculada como:

```
Eficiência = Desarmes Ganhos / Desarmes Totais
IEDO = (SCA DEF + GCA DEF + Desarmes(3/3)) * Eficiência
```

Onde:
- **SCA DEF** — Shot-Creating Actions originadas de ações defensivas.
- **GCA DEF** — Goal-Creating Actions originadas de ações defensivas.
- **Desarmes(3/3)** — Desarmes realizados no terço final do campo.

## 🚀 Funcionalidades

- 📑 **Filtragem de dados** — Seleção de atletas e equipes por critérios de minutos jogados e posição.
- 📊 **Cálculo de métricas** — Computa o IEDO para cada jogador e equipe.
- 🔍 **Clustering** — Agrupa jogadores com perfis estatísticos semelhantes.
- 🏆 **Ranking** — Lista os jogadores e equipes com melhor desempenho na métrica.

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Jupyter Notebook**
- **Pandas** — Manipulação de dados
- **NumPy** — Cálculos numéricos
- **Matplotlib / Seaborn** — Visualização
- **Scikit-learn** — Análise de agrupamento (clustering)

## 📦 Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/usuario/Analise-IEDO.git
   cd Analise-IEDO
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Abra os notebooks:
   ```bash
   jupyter notebook
   ```

4. Execute cada notebook na ordem:
   - `criatabela.ipynb` ou `criatabelatimes.ipynb`
   - `FiltragemIEDO.ipynb` ou `FiltragemIEDOTIME.ipynb`
   - `clustering.ipynb`

## 📌 Observações

- Os arquivos CSV devem conter dados no formato do FBref.
- O cálculo considera apenas jogadores com tempo mínimo de jogo (por exemplo, 900+ minutos).
- Os dados no exemplo são da **Premier League 2024**.
