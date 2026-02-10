# 📊 Análise de Acompanhamento de Vendas — SQL + Excel Dashboard

<img width="944" height="557" alt="image" src="https://github.com/user-attachments/assets/27d88813-5397-4152-8ab4-2c87df5560e7" />
<img width="1623" height="350" alt="image" src="https://github.com/user-attachments/assets/99803ff5-89a0-4dda-987a-68c84ce04e62" />
<img width="1707" height="407" alt="image" src="https://github.com/user-attachments/assets/24ba71a8-e129-459d-ac3e-a20fbb3b2ef8" />




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
