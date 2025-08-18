# Análise e Predição de Evasão de Clientes (Churn) - Telecom X

![Status](https://img.shields.io/badge/Status-Concluído-green)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Libraries](https://img.shields.io/badge/Bibliotecas-Pandas%20%7C%20Scikit--learn-orange)
![License](https://img.shields.io/badge/Licen%C3%A7a-MIT-lightgrey)

---

## 📜 Índice

* [Sobre o Projeto](#-sobre-o-projeto)
* [📊 Principais Descobertas e Performance do Modelo](#-principais-descobertas-e-performance-do-modelo)
* [🎯 Recomendações Estratégicas](#-recomendações-estratégicas)
* [📂 Estrutura do Repositório](#-estrutura-do-repositório)
* [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
* [⚙️ Configuração e Execução](#️-configuração-e-execução)
* [📓 Sobre o Notebook de Análise](#-sobre-o-notebook-de-análise)
* [📝 Licença](#-licença)

---

## 🎯 Sobre o Projeto

Este projeto apresenta uma análise completa do desafio "Churn de Clientes" da empresa fictícia **Telecom X**. O trabalho foi dividido em duas fases:

1.  **Análise Exploratória (Parte 1):** Um processo de **ETL (Extração, Transformação e Carga)** foi realizado para limpar e organizar os dados. Em seguida, uma **Análise Exploratória de Dados (EDA)** identificou os principais fatores correlacionados à evasão de clientes.
2.  **Modelagem Preditiva (Parte 2):** Com base nos dados tratados, foi construído um pipeline de Machine Learning para treinar e avaliar modelos capazes de **prever quais clientes têm maior probabilidade de cancelar o serviço**, permitindo ações de retenção proativas.

> O objetivo final é transformar dados brutos em uma ferramenta preditiva e em insights estratégicos para reduzir a taxa de churn da empresa.

---

## 📊 Principais Descobertas e Performance do Modelo

### Análise Exploratória (Insights da Parte 1)
A análise inicial revelou uma **taxa de churn geral de 26.5%**. O perfil do cliente com maior risco de evasão foi claramente identificado pelos seguintes fatores:

* 📝 **Contrato:** Possui um contrato flexível **Mês a Mês** (taxa de churn de **43%**).
* ⏳ **Tempo de Casa:** É um **cliente recente**, com a maioria dos cancelamentos ocorrendo nos primeiros meses.
* 🌐 **Serviço:** Utiliza internet de **Fibra Óptica** (taxa de churn de **42%**).
* 💳 **Pagamento:** Usa **Cheque Eletrônico** como método de pagamento (taxa de churn de **45%**).

### Modelo Preditivo (Resultados da Parte 2)
Foram treinados dois modelos de classificação (Regressão Logística e Árvore de Decisão). O modelo de **Árvore de Decisão** foi o escolhido, apresentando um desempenho sólido com **acurácia geral de 79%** e, mais importante, um **Recall de 56%** para a classe de churn. Isso significa que o modelo foi capaz de identificar corretamente 56% dos clientes que de fato iriam cancelar.

A análise de importância das variáveis do modelo **confirmou quantitativamente** os achados da análise exploratória, destacando `Contract_Month-to-month` e `tenure` como os fatores mais preditivos.

---

## 🎯 Recomendações Estratégicas

Com base nos resultados da análise e do modelo, as seguintes ações são recomendadas para a Telecom X:

1.  **Incentivar Contratos de Longo Prazo:** Criar campanhas para migrar clientes do plano "Mês a Mês" para contratos anuais.
2.  **Otimizar o Serviço de Fibra Óptica:** Investigar os motivos da alta evasão entre os clientes de Fibra (preço, estabilidade, suporte).
3.  **Modernizar Formas de Pagamento:** Oferecer incentivos para a migração de "Cheque Eletrônico" para métodos automáticos.
4.  **Criar um Programa de Onboarding:** Desenvolver um programa de boas-vindas para os primeiros 3 meses para reduzir o churn precoce.

---

## 📂 Estrutura do Repositório

O projeto está organizado na seguinte estrutura de pastas para garantir a reprodutibilidade:
```bash
🌳 telecom-churn-analysis/
|--- 📂 data/ 
|    |--- 📁 processed/
|         |-- 📊 churn_telecom_tratado.csv
|    |-- 📁 raw/
|         |-- 💾 TelecomX_Data.json
|--- 📂 notebooks/
|    |-- 🐍 TelecomX_BR.ipynb
|--- 📂 reports/
|    |-- 🖼️ images/
|         |-- churn_por_contrato.png
|--- ⚙️ .gitignore
|--- 📄 README.md
|-- 📋 requirements.txt
```
---

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.9+
* **Bibliotecas Principais:**
    * **Pandas:** Para manipulação e tratamento dos dados.
    * **Matplotlib & Seaborn:** Para visualização de dados.
    * **Scikit-learn:** Para pré-processamento, treinamento e avaliação dos modelos de Machine Learning.
* **Ambiente:** Jupyter/Google Colab

---

## ⚙️ Configuração e Execução

Siga os passos abaixo para executar a análise em seu ambiente local.

**1. Clone o Repositório**
```bash
git clone https://github.com/FabricioLimaa/ChallengeTelecomX-Alura.git
cd ChallengeTelecomX-Alura
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

**4. Execute o Notebook**
Inicie o Jupyter Lab e navegue até a pasta notebooks/ para abrir o arquivo TelecomX_BR.ipynb.
```bash
jupyter lab
```

**<summary>Conteúdo do requirements.txt</summary>**
```bash
pandas
matplotlib
seaborn
scikit-learn
jupyterlab
```

## 📓 Sobre o Notebook de Análise
O notebook principal contém todo o fluxo do projeto:

Parte 1: ETL e Análise Exploratória

📌 Extracão: Carregamento dos dados brutos.

🔧 Transformação: Limpeza, tratamento e engenharia de atributos.

📊 Análise Exploratória: Geração de gráficos e insights iniciais.


Parte 2: Modelagem Preditiva

⚙️ Pré-processamento para ML: Encoding e padronização dos dados.

⚙️ splitting: Divisão em dados de treino e teste.

🤖 Treinamento dos Modelos: Criação dos modelos de Regressão Logística e Árvore de Decisão.

📈 Avaliação e Interpretação: Análise de métricas, matriz de confusão e importância das variáveis.

📄 Relatorio Final: Conclusão consolidada do projeto.

## 📝 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

### **Principais Melhorias:**

>1.  **Badges Visuais:** Adicionei selos no topo para status, versão do Python, bibliotecas e licença, dando um ar mais profissional.
>2.  **Índice Navegável:** Criei um índice clicável que permite ao usuário pular diretamente para a seção de interesse.
>3.  **Destaque para Insights:** Movi as seções de "Principais Descobertas" e "Recomendações" para o topo, pois são as informações mais valiosas para quem visita o repositório.
>4.  **Uso de Emojis:** Adicionei emojis aos títulos para quebrar o texto e guiar o olhar do leitor.
>5.  **Blocos de Código Aprimorados:** Usei a sintaxe do Markdown para colorir os comandos `bash` e o conteúdo do arquivo `requirements.txt`.
>6.  **Elemento "Details":** O conteúdo do `requirements.txt` foi colocado dentro de uma tag `<details>`, que cria um menu "sanfona", deixando o README mais limpo.
>7.  **Seção de Licença:** Adicionei uma seção padrão de licença no final.
