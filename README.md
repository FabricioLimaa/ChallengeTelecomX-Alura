# Análise de Evasão de Clientes (Churn) - Telecom X

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-green)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Libraries](https://img.shields.io/badge/Bibliotecas-Pandas%20%7C%20Seaborn-orange)
![License](https://img.shields.io/badge/Licen%C3%A7a-MIT-lightgrey)

---

## 📜 Índice

* [Sobre o Projeto](#-sobre-o-projeto)
* [📊 Principais Descobertas (Insights)](#-principais-descobertas-insights)
* [🎯 Recomendações Estratégicas](#-recomendações-estratégicas)
* [📂 Estrutura do Repositório](#-estrutura-do-repositório)
* [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
* [⚙️ Configuração e Execução](#️-configuração-e-execução)
* [📓 Sobre o Notebook de Análise](#-sobre-o-notebook-de-análise)
* [📝 Licença](#-licença)

---

## 🎯 Sobre o Projeto

Este projeto apresenta uma análise completa do desafio "Churn de Clientes" da empresa fictícia **Telecom X**. O objetivo foi realizar um processo de **ETL (Extração, Transformação e Carga)** e uma **Análise Exploratória de Dados (EDA)** para identificar os principais fatores que influenciam a evasão de clientes.

> O desafio é transformar dados brutos em insights acionáveis que possam auxiliar a equipe de Data Science a desenvolver modelos preditivos e estratégias de retenção mais eficazes para a empresa.

---

## 📊 Principais Descobertas (Insights)

A análise revelou uma **taxa de churn geral de 26.5%**. O perfil do cliente com maior risco de evasão foi claramente identificado pelos seguintes fatores combinados:

* 📝 **Contrato:** Possui um contrato flexível **Mês a Mês** (taxa de churn de **43%**).
* ⏳ **Tempo de Casa:** É um **cliente recente**, com a maioria dos cancelamentos ocorrendo nos primeiros meses.
* 🌐 **Serviço:** Utiliza internet de **Fibra Óptica** (taxa de churn de **42%**).
* 💲 **Faturamento:** Paga uma **fatura mensal mais elevada**.
* 💳 **Pagamento:** Usa **Cheque Eletrônico** como método de pagamento (taxa de churn de **45%**).

---

## 🎯 Recomendações Estratégicas

Com base nos insights, foram propostas as seguintes ações para a Telecom X:

1.  **Incentivar Contratos de Longo Prazo:** Criar campanhas para migrar clientes do plano "Mês a Mês" para contratos anuais, oferecendo benefícios.
2.  **Otimizar o Serviço de Fibra Óptica:** Investigar os motivos da alta evasão entre os clientes de Fibra (preço, estabilidade, suporte) e atuar sobre os problemas.
3.  **Modernizar Formas de Pagamento:** Oferecer incentivos para a migração de "Cheque Eletrônico" para métodos automáticos (Cartão de Crédito, Débito em Conta).
4.  **Criar um Programa de Onboarding:** Desenvolver um programa de boas-vindas para os primeiros 3 meses, garantindo uma experiência inicial positiva para reduzir o churn precoce.

---

## 📂 Estrutura do Repositório

O projeto está organizado na seguinte estrutura de pastas para garantir a reprodutibilidade:
🌳 telecom-churn-analysis/
|
|--- 📂 data/
|    |  
|    |--- 📁 processed/
|    |    |
|    |    +-- 📊 churn_telecom_tratado.csv
|    |
|    +-- 📁 raw/
|         |
|         +-- 💾 TelecomX_Data.json
|
|--- 📂 notebooks/
|    |
|    +-- 🐍 TelecomX_BR.ipynb
|
|--- 📂 reports/
|    |
|    +-- 🖼️ images/
|         |
|         +-- churn_por_contrato.png
|         +-- ...
|
|--- ⚙️ .gitignore
|
|--- 📄 README.md
|
+-- 📋 requirements.txt

---

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.9+
* **Bibliotecas Principais:**
    * **Pandas:** Para manipulação e tratamento dos dados.
    * **Matplotlib & Seaborn:** Para visualização de dados e geração de gráficos.
* **Ambiente:** Jupyter/Google Colab

---

## ⚙️ Configuração e Execução

Siga os passos abaixo para executar a análise em seu ambiente local.

**1. Clone o Repositório**
```bash
git clone <url-do-seu-repositorio>
cd telecom-churn-analysis
```
**2. Crie e Ative um Ambiente Virtual**
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

**3. Instale as Dependências**
O arquivo requirements.txt contém todas as bibliotecas necessárias.
```bash
pip install -r requirements.txt
```

**<summary>Conteúdo do requirements.txt</summary>**
```bash
pandas
matplotlib
seaborn
jupyterlab
```

**4. Execute o Notebook**
Inicie o Jupyter Lab e navegue até a pasta notebooks/ para abrir o arquivo TelecomX_BR.ipynb.
```bash
jupyter lab
```

📓 Sobre o Notebook de Análise
O arquivo TelecomX_BR.ipynb está dividido em seções claras e sequenciais:

📌 Extracão: Conecta-se à fonte de dados e carrega os dados brutos.

🔧 Transformação: Executa todo o processo de limpeza, tratamento de inconsistências e engenharia de atributos.

📊 Carga e análise: Realiza a análise exploratória, gerando estatísticas e gráficos para identificar padrões.

📄 Relatorio Final: Apresenta um resumo consolidado do trabalho, com as conclusões e recomendações.

📝 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

>### **Principais Melhorias:**

>1.  **Badges Visuais:** Adicionei selos no topo para status, versão do Python, bibliotecas e licença, dando um ar mais profissional.
>2.  **Índice Navegável:** Criei um índice clicável que permite ao usuário pular diretamente para a seção de interesse.
>3.  **Destaque para Insights:** Movi as seções de "Principais Descobertas" e "Recomendações" para o topo, pois são as informações mais valiosas para quem visita o repositório.
>4.  **Uso de Emojis:** Adicionei emojis aos títulos para quebrar o texto e guiar o olhar do leitor.
>5.  **Blocos de Código Aprimorados:** Usei a sintaxe do Markdown para colorir os comandos `bash` e o conteúdo do arquivo `requirements.txt`.
>6.  **Elemento "Details":** O conteúdo do `requirements.txt` foi colocado dentro de uma tag `<details>`, que cria um menu "sanfona", deixando o README mais limpo.
>7.  **Seção de Licença:** Adicionei uma seção padrão de licença no final.




