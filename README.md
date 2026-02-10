# 📊 Análise de Acompanhamento de Vendas — SQL + Excel Dashboard

Este projeto tem como objetivo analisar métricas de desempenho de um funil de vendas, utilizando consultas em **PostgreSQL (pgAdmin)** e visualização de dados em **Excel** por meio de dashboards interativos.

---

## 🧰 Tecnologias Utilizadas

- PostgreSQL
- pgAdmin 4
- SQL
- Excel

---

## 🎯 Objetivos da Análise

- Calcular receita total mês a mês
- Quantificar leads gerados
- Identificar volume de vendas
- Medir taxa de conversão
- Calcular ticket médio
- Visualizar vendas por região

---

## 🗄️ Fonte de Dados

Os dados foram extraídos de um banco PostgreSQL contendo tabelas de funil de vendas, incluindo:

- `sales.funnel` → informações de visitas e pagamentos
- `sales.products` → preços e produtos

---

## 📑 Estrutura do Arquivo Excel

O arquivo `.xlsx` contém **3 abas (sheets)**:

### 1️⃣ Dashboard
Visualizações gráficas das principais métricas:

- Receita mês a mês
- Leads vs Conversão
- Lojas e Marcas com mais vendas
- Visitas ao site
- Estados que mais venderam

---

### 2️⃣ Resultados
Tabela consolidada com os indicadores calculados via SQL:

- Mês
- Leads (#)
- Vendas (#)
- Receita (k R$)
- Conversão (%)
- Ticket Médio (k R$)

---

### 3️⃣ Queries
Contém todas as consultas SQL utilizadas no projeto, incluindo:

- CTEs de Leads
- CTEs de Payments
- Cálculo de métricas
- Agrupamentos mensais
- Junções entre tabelas
    paid_count AS vendas
FROM leads
LEFT JOIN payments
ON leads.visit_page_month = payments.paid_month;
