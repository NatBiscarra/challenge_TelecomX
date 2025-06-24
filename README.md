# Telecom X - Análise de Evasão de Clientes (Churn)

Este projeto tem como objetivo geral desenvolver uma análise de dados para a empresa fictícia **Telecom X**, um desafio que compõe a formação em Data Science do programa Oracle Next Education (ONE) em parceria com a Alura Latam. 

A empresa enfrenta um alto índice de cancelamentos, portanto, o objetivo geral da análise é compreender os fatores que levam à perda de clientes.

---

## Começando🚀 

Essas instruções permitirão que você obtenha uma cópia do projeto em operação na sua máquina local para fins de desenvolvimento e teste.

####  Como usar
Para rodar este projeto, você poderá utilizar o Google Colab. 
  1. Clone este repositório em sua máquina:
     ```
     git clone https://github.com/NatBiscarra/challenge_TelecomX.git
     ```
  2. Acesse o diretório
     ```
     cd challenge_TelecomX
     ```
  3. Abra o notebook TelecomX_Notebook.ipynb no Google Colab
     
---

### Objetivo🎯
Este projeto tem como objetivo: 
- Coletar e tratar os dados de clientes disponibilizados via API.
- Explorar e entender o comportamento dos clientes.
- Identificar padrões e possíveis causas de evasão.
- Preparar os dados para modelagens futuras e auxiliar na tomada de decisão.
- Apoiar a empresa com **insights estratégicos** para redução da evasão.

---

### Limpeza e Tratamento de Dados 🧹 

As principais etapas de preparação dos dados incluíram:

- ✅ Importação e normalização de um arquivo JSON estruturado por API.
- ✅ Separação de campos aninhados em colunas planas.
- ✅ Remoção de registros com valores ausentes em colunas críticas.
- ✅ Padronização de colunas e conversão de variáveis binárias ("Yes"/"No" → 1/0).
- ✅ Criação da variável `contas_diarias`, baseada na fatura mensal.

---

### Análise Exploratória de Dados (EDA)🔍 

A análise exploratória revelou importantes padrões de comportamento entre os clientes.

#### Distribuição Geral do Churn📌 

- **26,6% dos clientes** cancelaram seus serviços.
- Gráficos de barras e pizza foram utilizados para visualizar a proporção de churn.

### Visualização da Evasão de Clientes (Churn) 📊 

A seguir, apresentamos dois gráficos que ilustram a distribuição da variável `churn`, responsável por indicar se o cliente deixou ou permaneceu na empresa:

- **Gráfico de Barras**: mostra a contagem absoluta de clientes que saíram (`1`) e que permaneceram (`0`).
- **Gráfico de Pizza**: mostra a proporção percentual entre os dois grupos.

| Distribuição Absoluta e Percentual |
|-----------------------|
| ![churn_barras](img/churn_barras.png) | 

> 📌 Os gráficos acima revelam que cerca de **26,6% dos clientes saíram da empresa**, enquanto **73,4% permaneceram**.

---

#### Churn por Variáveis Categóricas📌 

- Clientes com **contrato mensal** apresentam **alta taxa de churn**.
- A forma de pagamento **"Electronic Check"** está fortemente ligada à evasão.
- Clientes que **não utilizam serviços extras** (como suporte técnico ou backup) evadem mais.

Visualizações com **Plotly** e análise de **proporção por grupo** foram aplicadas.

#### Churn por Variáveis Numéricas📌 

As principais variáveis analisadas foram:

- `tenure`: clientes com pouco tempo de casa saem mais.
- `monthly_charges`: faturas mais altas correlacionam com maior churn.
- `total_charges`: quanto menor o gasto total, maior a probabilidade de evasão.
- `contas_diarias`: estimativa de gasto médio por dia.

Foram usados **histogramas e boxplots** para comparar a distribuição entre clientes que ficaram e os que saíram.

---

### Principais Insights💡 

- Clientes que **acabaram de entrar** na empresa são os que mais cancelam.
- Contratos **mensais** e **pagamento eletrônico** (via boleto) são os grupos mais vulneráveis.
- Clientes que **pagam mais e usam menos serviços extras** apresentam maior risco de churn.

---

### Recomendações✅ 

- Oferecer **incentivos para contratos de longo prazo**.
- Estimular o uso de serviços complementares.
- Adotar formas de pagamento automáticas (como débito ou cartão).
- Focar nos **primeiros meses do cliente**, com ações proativas de engajamento.

---

### Tecnologias e Ferramentas🔧 

- Python 3.10+
- Pandas
- NumPy
- Google Colab 
- Matplotlib
- Seaborn
- Plotly

---

### Estrutura dos Dados📁 

O dataset inclui colunas como:

- `customer_id`, `churn`, `tenure`, `monthly_charges`, `contract`, `internet_service`, entre outras.
- Serviços adicionais: `tech_support`, `streaming_tv`, `online_backup`, etc.
- Coluna criada: `contas_diarias` → estimativa do gasto diário do cliente.

---

## Agradecimentos
À **Alura Latam** e à **Oracle** pelo conhecimento compartilhado através do programa **[ONE - Oracle Next Education](https://www.oracle.com/br/education/oracle-next-education/)**.

