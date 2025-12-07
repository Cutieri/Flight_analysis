✈️ Análise de Atrasos de Voos – Projeto de Data Science

Este projeto tem como objetivo analisar um conjunto de dados reais do tráfego aéreo dos EUA, identificar padrões de atrasos, destacar as companhias que mais atrasam e verificar se fatores como rota e aeronave influenciam no atraso.

A análise responde às seguintes perguntas principais:

Quais companhias mais atrasam?

A rota ou aeronave influenciam no atraso?

Existe algum padrão ou tendência nos atrasos? Se sim, como reduzi-los?

📊 Tecnologias utilizadas

Python

Pandas

Matplotlib / Seaborn

Jupyter Notebook

Análise Estatística

Visualizações (Gráficos e Tabelas)

🔍 Resultados e Insights Principais
1️⃣ Quais companhias mais atrasam?
📌 Média geral de atrasos

A média geral dos atrasos de todas as companhias analisadas foi:

⏱️ 6.37 minutos de atraso médio

📌 Companhias com média de atraso acima da média geral
9E – B6 – EV – F9 – FL – MQ – OO – WN – YV

📊 Quantidade absoluta de atrasos (Top 3)
Companhia	Atrasos
B6	17.588
UA	16.717
EV	15.498
📈 Companhias que mais atrasam proporcionalmente

(Percentual de voos que chegam atrasados)

Companhia	% de voos atrasados
FL	61,2%
YV	56,8%
F9	56,2%
🏆 Entre as grandes companhias
Companhia	% Atrasos	Observação
EV	48%	mais atrasos entre as grandes
DL	33,5%	mais pontual entre as grandes
2️⃣ A rota influencia nos atrasos?

Sim. As rotas possuem impacto significativo nos atrasos.

Top 3 rotas mais atrasadas (média de atraso):
Rota	Atraso Médio (min)
EWR–GSO	212.0
EWR–CAE	77.85
EWR–CMH	68.75

🔎 Observação importante:
Rotas saindo do aeroporto EWR (Newark) aparecem repetidamente entre as piores, indicando gargalos operacionais específicos desse aeroporto (clima, tráfego, restrições de pista etc.).

3️⃣ Há padrões nos atrasos? Como reduzi-los?
📌 Padrões observados

Certas companhias apresentam atraso estrutural, não pontual.

Algumas rotas específicas (principalmente envolvendo EWR) possuem atraso crônico.

Companhias com muito volume de voo tendem a atrasar mais proporcionalmente quando têm baixa capacidade operacional.

📉 Possíveis ações para reduzir atrasos

Redistribuir horários de pico em companhias com alto volume e baixo desempenho.

Revisar rotas críticas (como EWR–GSO).

Melhorar planejamento de frota para evitar acúmulo de atrasos ao longo do dia.

Aumentar buffers operacionais para companhias com alto percentual de atrasos.

🧪 Como encontramos essas respostas?
✔ Tratamento e limpeza dos dados

Remoção de valores nulos

Criação de métricas (média de atraso, % de atraso por companhia, atraso por rota)

✔ Análises aplicadas

Group By para atrasos por companhia

Cálculo de média, mediana, soma

Rankings e percentuais

Análise de rotas (origem–destino)

Cruzamento de volume x atraso para achar companhias “pior custo-benefício”

✔ Visualizações geradas

Gráficos de barras para atraso por companhia

Gráficos de pizza para % de atrasos

Heatmap por rota

Tabelas comparativas para insights rápidos

📁 Estrutura do Repositório
📦 projeto-atrasos-voos
 ┣ 📂 data
 ┣ 📂 notebooks
 ┣ 📂 images
 ┣ 📄 README.md
 ┗ 📄 analise_atrasos.ipynb

🚀 Conclusão

A análise mostra que:

Algumas companhias atrasam significativamente mais do que a média.

A rota influencia muito — especialmente as que envolvem o aeroporto EWR.

Há padrões claros e ações que poderiam reduzir atrasos (melhor logística, ajustes de horários e revisão de rotas críticas).

Esse projeto demonstra aplicações práticas de Data Science para problemas reais e complexos do setor aeronáutico.