Análise de Evasão de Clientes (Churn) - Telecom X
1. Introdução
Este repositório contém a análise completa do desafio "Churn de Clientes" da empresa fictícia Telecom X. O objetivo principal foi realizar um processo completo de Extração, Transformação e Carga (ETL) e uma Análise Exploratória de Dados (EDA) para identificar os principais fatores que influenciam a evasão de clientes (churn).

O projeto visa transformar dados brutos em insights acionáveis que possam auxiliar a equipe de Data Science a desenvolver modelos preditivos e estratégias de retenção mais eficazes.

2. Estrutura de Pastas
Para manter o projeto organizado e reprodutível, sugere-se a seguinte estrutura de pastas:

telecom-churn-analysis/
│
├── data/
│   ├── processed/
│   │   └── churn_telecom_tratado.csv  # Opcional: dataset limpo salvo
│   └── raw/
│       └── TelecomX_Data.json         # Opcional: cópia local dos dados brutos
│
├── notebooks/
│   └── TelecomX_BR.ipynb              # Notebook principal com toda a análise
│
├── reports/
│   └── images/
│       ├── churn_por_contrato.png     # Gráficos gerados pela análise
│       └── ...
│
├── .gitignore                         # Arquivo para ignorar arquivos desnecessários
├── README.md                          # Este arquivo de documentação
└── requirements.txt                   # Dependências do projeto
3. Tecnologias Utilizadas
Linguagem: Python 3.9+

Bibliotecas Principais:

Pandas: Para manipulação e tratamento dos dados.

Matplotlib & Seaborn: Para visualização de dados e geração de gráficos.

Jupyter/Google Colab: Como ambiente de desenvolvimento interativo.

4. Instalação e Configuração
Para executar este projeto localmente, siga os passos abaixo:

Clone o repositório:

Bash

git clone <url-do-seu-repositorio>
cd telecom-churn-analysis
Crie e ative um ambiente virtual (recomendado):

Bash

python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
Instale as dependências:
O arquivo requirements.txt contém todas as bibliotecas necessárias.

Bash

pip install -r requirements.txt
Conteúdo do requirements.txt:

pandas
matplotlib
seaborn
jupyterlab
5. Passo a Passo para Execução
Inicie o Ambiente: Após a instalação, inicie o Jupyter Lab (ou Jupyter Notebook).

Bash

jupyter lab
Abra o Notebook: Navegue até a pasta notebooks/ e abra o arquivo TelecomX_BR.ipynb.

Execute as Células: O notebook foi projetado para ser executado de forma sequencial, de cima para baixo. Cada seção realiza uma etapa do projeto:

📌 Extracão: Conecta-se à fonte de dados no GitHub e carrega os dados brutos.

🔧 Transformação: Executa todo o processo de limpeza, tratamento de inconsistências e engenharia de atributos.

📊 Carga e análise: Realiza a análise exploratória, gerando tabelas de estatísticas e visualizações gráficas para identificar padrões.

📄 Relatorio Final: Apresenta um resumo consolidado de todo o trabalho, com as conclusões e recomendações.

6. Resumo da Análise e Principais Insights
A análise revelou uma taxa de churn geral de 26.5%. O perfil do cliente com maior risco de evasão foi claramente identificado:

Perfil do Cliente com Alto Risco de Evasão:

Contrato: Possui um contrato flexível Mês a Mês (taxa de churn de 43%).

Tempo de Casa: É um cliente recente, com a maioria dos cancelamentos ocorrendo nos primeiros meses.

Serviço: Utiliza internet de Fibra Óptica (taxa de churn de 42%).

Faturamento: Paga uma fatura mensal mais elevada.

Pagamento: Usa Cheque Eletrônico como método de pagamento (taxa de churn de 45%).

7. Recomendações Estratégicas
Com base nos insights, foram propostas as seguintes ações para a Telecom X:

Incentivar Contratos de Longo Prazo: Criar campanhas para migrar clientes do plano "Mês a Mês" para contratos anuais, oferecendo benefícios.

Otimizar o Serviço de Fibra Óptica: Investigar os motivos da alta evasão entre os clientes de Fibra (preço, estabilidade, suporte) e atuar sobre os problemas.

Modernizar Formas de Pagamento: Oferecer incentivos para a migração de "Cheque Eletrônico" para métodos automáticos (Cartão de Crédito, Débito em Conta), que estão associados a maior retenção.

Criar um Programa de Onboarding: Desenvolver um programa de boas-vindas para os primeiros 3 meses, garantindo uma experiência inicial positiva e reduzindo o churn precoce.
