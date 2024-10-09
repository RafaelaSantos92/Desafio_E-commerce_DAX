# Desafio de Projeto: Modelagem Dimensional com Star Schema
Este repositório contém o código e a documentação para o Desafio de Projeto que envolve a criação de um modelo dimensional utilizando o Star Schema (Esquema em Estrela). Utilizamos a tabela única "Financial Sample" como fonte para gerar as tabelas fato e dimensão que compõem o modelo.

# Objetivo
O objetivo deste projeto é aplicar conceitos de modelagem dimensional, transformando uma tabela única em múltiplas tabelas relacionadas para análise eficiente de dados. O foco é estruturar as tabelas de forma que otimizem o processo de consulta e visualização de dados para relatórios.

# Estrutura do Projeto
Tabelas Criadas:
Financials_origem (modo oculto)

Backup da tabela original.
Tabelas Dimensão:

D_Produtos:
Colunas: ID_produto, Produto, Média de Unidades Vendidas, Média do Valor de Vendas, Mediana do Valor de Vendas, Valor Máximo de Venda, Valor Mínimo de Venda.
D_Produtos_Detalhes:
Colunas: ID_produto, Discount Band, Sale Price, Units Sold, Manufactoring Price.
D_Descontos:
Colunas: ID_produto, Discount, Discount Band.
D_Detalhes:
Tabela de detalhes (detalhes a serem definidos conforme necessidade).
D_Calendário:
Criada utilizando a função CALENDAR() no DAX, contendo campos relacionados ao tempo.
Tabela Fato:

F_Vendas:
Colunas: SK_ID, ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Sales, Profit, Date (campos derivados da D_Calendário).
Processo de Criação
Criação das Tabelas Dimensão: As tabelas dimensão foram derivadas da tabela original "Financial Sample". Cada tabela contém um conjunto específico de colunas que descrevem diferentes aspectos dos dados, como produtos, descontos, e detalhes de vendas.

Tabela Fato: A tabela fato, "F_Vendas", centraliza os dados principais de vendas, associando-os às chaves de suas respectivas tabelas dimensão, permitindo análises cruzadas e agregações eficientes.

Tabela de Calendário: A tabela "D_Calendário" foi criada por meio do DAX utilizando a função CALENDAR(), permitindo análises temporais ao conectar as datas da tabela fato.

# Ferramentas Utilizadas
Power BI / DAX: Utilizado para a manipulação dos dados e criação do modelo dimensional.

# Considerações Finais
Este projeto demonstra uma abordagem prática para a construção de um modelo dimensional baseado em um esquema estrela, utilizando uma tabela de vendas financeiras como base. É uma oportunidade de aplicar os conceitos de modelagem de dados e DAX para criar uma estrutura de dados mais eficiente e escalável para análise de dados.
