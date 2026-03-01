# 🎮 ICE Store - Análise de Vendas de Jogos

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?style=for-the-badge&logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-Data_Visualization-3F4F75?style=for-the-badge&logo=plotly)
![SciPy](https://img.shields.io/badge/SciPy-Statistical_Analysis-8CAAE6?style=for-the-badge&logo=scipy)
![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-success?style=for-the-badge)

## 📖 Descrição

**Contexto do problema:**   
A ICE Store é uma loja fictícia que vende jogos a nível mundial. Para planear as campanhas publicitárias e o stock para o ano de 2017, é crucial entender as tendências do mercado, identificar quais as plataformas que estão em ascensão ou declínio, e compreender o comportamento dos consumidores em diferentes regiões do globo.

**Objetivo do projeto:**  
O objetivo principal desta Análise Exploratória de Dados (EDA) é extrair *insights* valiosos do histórico de vendas de jogos, avaliações de críticos e utilizadores, e dados regionais. O projeto visa detetar padrões de sucesso, calcular o ciclo de vida das plataformas e prever tendências para otimizar as estratégias de marketing de 2017.

## 📊 Dataset

* **Fonte dos dados:** Ficheiro local `games.csv` (dados fornecidos para a análise).
* **Descrição:** O conjunto de dados contém **16.715 registos** de videojogos lançados desde 1980 até 2016.
* **Variáveis principais:**
    * `Name`: Nome do jogo.
    * `Platform`: Plataforma (ex: PS4, XOne, PC, WiiU).
    * `Year_of_Release`: Ano de lançamento.
    * `Genre`: Género do jogo (Action, Sports, Shooter, etc.).
    * `NA_sales`, `EU_sales`, `JP_sales`, `Other_sales`: Vendas nas respetivas regiões (em milhões de USD).
    * `Critic_Score`: Pontuação atribuída por críticos (até 100).
    * `User_Score`: Pontuação atribuída por utilizadores (até 10).
    * `Rating`: Classificação etária (ESRB).

## 🛠️ Tecnologias e Ferramentas

* **Linguagem:** Python 3.12
* **Manipulação e Limpeza de Dados:** Pandas, NumPy
* **Visualização de Dados:** Plotly Express (`px`) para gráficos interativos.
* **Estatística e Testes de Hipóteses:** SciPy (`scipy.stats`)
* **Ambiente de Desenvolvimento:** Jupyter Notebook

## ⚙️ Etapas do Projeto

1.  **Importação e Preparação dos Dados:**
    * Padronização dos nomes das colunas para *snake_case*.
    * Tratamento de valores nulos (ex: conversão de "tbd" para `NaN` na coluna `user_score`).
    * Criação da variável agregada `global_sales`.
3.  **Análise Exploratória de Dados (EDA):**
    * Análise do ciclo de vida das plataformas (mediana de 6 anos de duração).
    * Focagem no período recente (2013-2016) para identificar plataformas promissoras.
    * Análise de variabilidade (Variância e Desvio Padrão) para entender a consistência de vendas.
4.  **Criação de Perfis de Utilizador por Região:**
    * Mapeamento das preferências (Plataformas, Géneros e Classificação Etária) para a América do Norte (NA), Europa (EU) e Japão (JP).
5.  **Teste de Hipóteses Estatísticas:**
    * *Teste 1:* Diferença nas avaliações dos utilizadores entre Xbox One e PC.
    * *Teste 2:* Diferença nas avaliações dos utilizadores entre os géneros *Action* e *Sports*.

## 💡 Principais Insights / Resultados

* **Ciclo de Vida das Plataformas:** Uma plataforma tem, em média, um ciclo de vida de **6 anos** antes de ser descontinuada ou substituída por uma nova geração.
* **Plataformas Promissoras para 2017:** A PS4 lidera isoladamente o mercado recente (média de 60M USD/ano), seguida pela Xbox One e 3DS. O PC, embora com valores absolutos menores, apresenta a maior longevidade e consistência.
* **Impacto das Avaliações:** Na plataforma PS4, existe uma **correlação positiva moderada (0.40)** entre a nota dos críticos e as vendas globais. No entanto, a nota dos utilizadores tem um impacto quase nulo (-0.03) nas vendas.
* **Perfis Regionais Distintos:**
    * **América do Norte e Europa:** Mercados muito semelhantes. Preferem géneros de Ação e *Shooters* em consoles (PS4, XOne, PS3, X360).
    * **Japão:** Mercado focado em mobilidade e RPGs. As plataformas líderes são portáteis (3DS, PSV) e o género dominante é *Role-Playing*.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
* Python 3.12 ou superior instalado.
* Git instalado.

### Instalação passo a passo

**1. Clonar o repositório**
Abre o teu terminal e clone este repositório para a tua máquina:
```bash
git clone [https://github.com/gilbertsmartins/ICE-Store-Sales-Analysis.git](https://github.com/gilbertsmartins/ICE-Store-Sales-Analysis.git)
cd ICE-Store-Sales-Analysis
```

**2. Criar e ativar um ambiente virtual (Recomendado)**
Isso garante que as dependências do projeto não entrem em conflito com outras instalações no teu sistema.
* No **Windows**:
  ```bash
  python -m venv venv
  venv\Scripts\activate
  ```
* No **Linux / macOS**:
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

**3. Instalar as Bibliotecas**
Com o ambiente virtual ativado, instale as bibliotecas necessárias através do `pip`:
```bash
pip install -r requirements.txt
```

### Execução

Para abrir o projeto e visualizar as análises interativas, inicie o Jupyter Notebook em sua IDE de preferência localmente ou acesse este [link](https://htmlpreview.github.io/?https://github.com/GilbertsMartins/ICE-Store-Sales-Analysis/blob/main/notebooks/EDA.html) para uma visualização online.

---

## 📂 Estrutura do Projeto

```text
📦 ice-store-sales-analysis
 ┣ 📂 data
 ┃ ┗ 📜 games.csv              # Dataset original (adiciona localmente, ignorado no git)
 ┣ 📂 notebooks
 ┃ ┗ 📜 EDA.ipynb              # Notebook principal com a análise interativa
 ┗ 📜 README.md                # Documentação do projeto
```

## 🔮 Possíveis Melhorias Futuras

* **Implementação de Machine Learning:** Criar um modelo preditivo (Regressão) para estimar as vendas de um jogo com base no seu género, plataforma e classificação etária.
* **Dashboard Interativo:** Exportar os dados limpos e construir um *dashboard* em Power BI ou Tableau para consumo não-técnico pelos *stakeholders* da loja.
* **Análise de Sentimento:** Caso fosse possível obter os textos das *reviews* dos utilizadores, aplicar NLP para entender os principais motivos de queixa ou elogio por plataforma.

## 👨‍💻 Autor

**Gilbert Martins**
* Analista de Dados

* <a>
  <img align="left" alt="Gilbert's LinkdeIN" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg"/> 
  
  [LinkedIn](https://linkedin.com/in/gilbert-martins) </a>
