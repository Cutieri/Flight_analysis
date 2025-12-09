✈️ Análise de Atrasos de Voos — NYC Flights 2013

Este projeto apresenta uma análise completa dos atrasos de voos que partiram de Nova York em 2013, utilizando o dataset NYC Flights 2013.
O objetivo foi entender o comportamento dos atrasos, identificar padrões relevantes e destacar fatores que mais influenciam o desempenho das companhias aéreas, rotas e aeronaves.

📦 Tecnologias Utilizadas

Python

Pandas

NumPy

Matplotlib

Jupyter Notebook

📊 Metodologia da Análise

A investigação seguiu quatro etapas principais:

Limpeza e tratamento dos dados

Remoção de valores nulos

Ajuste de tipos

Criação de variáveis derivadas (ex: route = origin-dest)

Análise quantitativa

Médias, proporções, contagens, somas

Agrupamentos por companhia, rota e aeronave

Identificação de outliers e padrões numéricos

Análise qualitativa e exploratória

Interpretação dos resultados

Identificação de correlações práticas

Observação de tendências e possíveis motivos dos atrasos

Visualizações

Gráficos de barras, rankings e distribuições

Comparações entre companhias, rotas e aeronaves

🛫 Principais Insights Obtidos
🔸 Desempenho das companhias aéreas

A média geral de atrasos entre todas as companhias foi ≈ 6,37 minutos.

Diversas empresas apresentaram atraso acima da média, como:
9E, B6, EV, F9, FL, MQ, OO, WN, YV.

Em termos absolutos, as companhias com maior número total de atrasos foram:

B6 — 17.588 atrasos

UA — 16.717 atrasos

EV — 15.498 atrasos

Proporcionalmente, as empresas que mais atrasam são:

FL (61,2%)

YV (56,8%)

F9 (56,2%)

Entre as companhias grandes, a Delta (DL) demonstrou melhor regularidade com ~33,5% dos voos atrasando.

🔸 Rotas que mais sofrem atrasos

Foi criada a variável route = origin + "-" + dest e calculado o atraso médio de cada rota.

As rotas com maior atraso médio foram:

Rota	Atraso médio (min)
EWR-GSO	212.0
EWR-CAE	77.9
EWR-CMH	68.8

🔍 Observação importante: todas as rotas da lista começam no aeroporto EWR, indicando um forte padrão de atrasos para voos originados em Newark.

Além disso, analisando o volume total de voos por rota, foram identificadas rotas com baixo volume que podem distorcer médias — mas ainda assim, o comportamento do aeroporto permanece consistente.

🔸 Aeronaves que mais atrasam

Agrupando por tailnum, identificamos aeronaves com:

Maior atraso médio

Maior quantidade de voos

Maior soma total de atraso

Algumas aeronaves apresentaram atrasos elevados por volume ou média, enquanto outras tiveram desempenho consistentemente positivo (médias negativas).

Isso indica que problemas mecânicos, idade da aeronave ou rotas específicas podem estar influenciando.

📈 Visualizações Implementadas

O projeto inclui gráficos que mostram:

Ranking de atraso médio por companhia

Proporção de voos atrasados por companhia

Rotas com maior atraso médio

Comparações visuais entre aeroportos de origem

Distribuições de atraso

As visualizações foram criadas em Matplotlib, com estilo customizado para torná-las mais limpas e profissionais.

🧭 Conclusões Gerais

A análise permitiu identificar padrões claros:

Algumas companhias são, de fato, mais suscetíveis a atrasos — seja por volume, operação ou características específicas.

O aeroporto EWR tem um papel significativo nos atrasos, afetando múltiplas rotas independentemente da companhia.

A aeronave utilizada também pode influenciar o atraso, sugerindo impactos de manutenção, performance ou histórico operacional.

Esses resultados podem ajudar companhias aéreas, aeroportos e analistas a tomar decisões baseadas em dados, como revisar rotas críticas, ajustar escalas, aprimorar a manutenção de aeronaves ou redistribuir recursos.

📁 Estrutura do Projeto
📦 NYC-Flights-Analysis
 ┣ 📂 notebooks
 ┃ ┣ data_exploration.ipynb
 ┃ ┗ visualization.ipynb
 ┣ 📂 data
 ┃ ┗ df_clean.csv
 ┗ README.md

🚀 Como Reproduzir

Clone o repositório

Instale as dependências

pip install -r requirements.txt


Abra os notebooks e explore a análise
