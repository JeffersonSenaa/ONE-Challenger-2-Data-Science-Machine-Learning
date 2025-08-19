# Análise de Evasão de Clientes (Churn) em Telecomunicações

## Descrição do Projeto

Este projeto realiza uma análise exploratória de dados para identificar os fatores que influenciam a evasão de clientes (Churn) em uma empresa de telecomunicações. O objetivo é compreender o comportamento dos clientes que cancelam o serviço para ajudar a empresa a desenvolver estratégias de retenção mais eficazes.

## Fonte de Dados

Os dados utilizados neste projeto foram obtidos de um arquivo JSON disponível em: https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json

Este conjunto de dados contém informações demográficas de clientes, serviços contratados, informações de telefone e internet, detalhes da conta e o status de Churn.
Análise Realizada

A análise exploratória de dados (AED) incluiu as seguintes etapas principais:

    Extração e Carregamento: Os dados foram carregados a partir da fonte JSON para um DataFrame pandas.
    Limpeza e Tratamento:
        - Verificação e tratamento de valores ausentes (nenhum encontrado).
        - Normalização de dados aninhados (dicionários em colunas como 'customer', 'phone', 'internet', 'account').
        - Verificação e remoção de registros duplicados.
        - Criação de novas features, como 'Contas_Diarias'.
        - Conversão de variáveis categóricas binárias ('Yes'/'No') para representação numérica (1/0).
    Análise Descritiva: Cálculo de estatísticas descritivas para variáveis numéricas (customer.tenure, account.Charges.Monthly, Contas_Diarias).
    Visualização da Distribuição por Churn: Geração de box plots, histogramas e gráficos de densidade (KDE) para entender como as variáveis numéricas se distribuem entre clientes com e sem Churn.
    Análise da Relação Categórica-Churn: Cálculo da taxa de Churn para cada categoria de variáveis como tipo de contrato, método de pagamento, serviço de internet, etc., e visualização dessas relações com gráficos de barras.

## Principais Insights

### Os principais fatores associados a uma maior taxa de evasão identificados nesta análise incluem:

    - Clientes com menor tempo de permanência.
    - Clientes com cobranças mensais mais altas.
    - Clientes com contratos de curto prazo ("Month-to-month").
    - Clientes que utilizam "Electronic check" como método de pagamento.
    - Clientes com serviço de internet "Fiber optic".
    - Clientes sem parceiro ou dependentes.

## Como Reproduzir a Análise

Você pode reproduzir esta análise seguindo os passos detalhados no notebook Jupyter. O notebook contém o código Python utilizado para a extração, limpeza, tratamento e análise exploratória dos dados, juntamente com as visualizações geradas.

### Para executar o notebook:

    Clone este repositório.
    Abra o notebook em um ambiente compatível (como Google Colab, Jupyter Notebook ou JupyterLab).
    Execute as células de código sequencialmente.

### Recomendações

Com base nos insights, recomendações incluem programas de fidelidade para clientes novos, incentivos para contratos mais longos, investigação da experiência do cliente com fibra óptica, otimização de métodos de pagamento (especialmente "Electronic check"), ofertas personalizadas para segmentos específicos de clientes e monitoramento contínuo do Churn.
