
# Análise de Unicórnios (Startups em 2021)

Este projeto consiste em uma análise exploratória de um conjunto de dados contendo informações sobre startups unicórnio (empresas com valuation a partir de $1 bilhão de dólares) até o final do ano de 2021.

## 📋 Funcionalidades do Projeto

O script realiza as seguintes etapas de processamento e análise de dados:

1. **Carregamento dos Dados:** Importação da base de dados no formato CSV.
2. **Renomeação de Colunas:** Tradução e simplificação dos nomes das colunas para facilitar a manipulação:
   - `Unnamed: 0` -> `ID`
   - `Company` -> `Empresa`
   - `Valuation ($B)` -> `Valor($)`
   - `Date Joined` -> `Data de Adesão`
   - `Country` -> `Pais`
   - `City` -> `Cidade`
   - `Industry` -> `Industria`
   - `Select Investors` -> `Investidores`
3. **Tratamento de Dados (Limpeza):**
   - Conversão do campo `Valor($)` para numérico (float) removendo o caractere de cifrão (`$`).
   - Conversão da coluna `Data de Adesão` para o formato de data (`datetime`).
   - Tratamento de valores nulos nas colunas `Cidade` (substituídos por 'Desconhecida') e `Investidores` (substituídos por 'Desconhecido').
   - Correção de inconsistências de digitação nos nomes dos países (ex: remoção de vírgulas extras como em 'United States,' e 'Indonesia,').
4. **Agrupamento e Análise:**
   - Cálculo do Valuation Total agregado por País.
   - Cálculo do Valuation Total agregado por Indústria.
5. **Visualização Gráfica:**
   - Geração de um gráfico de barras com o **Top 10 Países por Valuation Total ($B)**.
   - Geração de um gráfico de barras demonstrando o **Valuation Total por Indústria ($B)**.

## 🛠️ Tecnologias Utilizadas

- **Python**
- **Pandas**: Manipulação e tratamento de dados.
- **NumPy**: Suporte matemático e arrays.
- **Matplotlib** e **Seaborn**: Criação de gráficos e visualização de dados.

## 📊 Visualizações Geradas

O notebook gera um painel composto por dois gráficos principais:
- O primeiro destaca a forte liderança dos **Estados Unidos** e da **China** em termos de valuation acumulado.
- O segundo mostra o setor de **Fintech** e de **Internet software & services** como os mais valiosos do ecossistema de startups.
