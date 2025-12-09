<h2 align="center">📊 Sobre o Projeto</h2>

Este repositório traz uma análise exploratória completa sobre atrasos de voos nos EUA, utilizando técnicas de **EDA (Exploratory Data Analysis)** para entender padrões, tendências e fatores que influenciam atrasos.  

O foco foi transformar um grande volume de dados brutos em **insights acionáveis**, avaliando companhias aéreas, rotas, frequência de voos e proporção de atrasos.

---

<h2 align="center">🔎 Principais Insights Obtidos</h2>

Durante a análise, conseguimos responder perguntas importantes sobre o comportamento dos atrasos. Aqui estão os destaques:

---

<h3>📌 Qual é o tempo médio de atraso das companhias?</h3>

A média geral encontrada foi de <strong>6.37 minutos</strong> por voo.

Companhias com média acima desse valor incluem:  
<strong>9E, B6, EV, F9, FL, MQ, OO, WN e YV.</strong>

---

<h3>📌 Quais companhias realmente mais atrasam?</h3>

Existem três formas de analisar isso, e todas foram exploradas:

<h4>1️⃣ Em quantidade absoluta de atrasos</h4>

- **B6** — 17.588 atrasos  
- **UA** — 16.717 atrasos  
- **EV** — 15.498 atrasos  

Essas são as que mais atrasam em números totais.

---

<h4>2️⃣ Proporcionalmente (percentual dos voos que atrasam)</h4>

- **FL** — 61,2% dos voos atrasam  
- **YV** — 56,8%  
- **F9** — 56,2%  

Essas são as "piores" no sentido de confiabilidade.

---

<h4>3️⃣ Entre as grandes companhias</h4>

- **EV** — 48% dos voos atrasam (pior entre as grandes)  
- **DL** — 33,5% (uma das mais pontuais)

---

<h3>📌 As rotas influenciam nos atrasos?</h3>

Sim! As rotas mostraram ser um fator relevante.

As rotas mais problemáticas foram:

- **EWR → GSO** — 212 min de atraso médio  
- **EWR → CAE** — 77.86 min  
- **EWR → CMH** — 68.75 min  

Ou seja, voos saindo de **EWR** (Newark) apresentaram um padrão claro de maiores atrasos.

---

<h2 align="center">📈 Como chegamos a essas conclusões?</h2>

Utilizamos:

- Agrupamentos por companhia aérea  
- Estatísticas descritivas (médias, medianas e percentuais)  
- Análise de volume total de voos  
- Cálculo de atrasos proporcionais (atrasos ÷ total de voos)  
- Identificação das rotas com maior média de atraso  

O objetivo foi observar tanto o “todo” quanto a performance individual de cada companhia, evitando conclusões superficiais baseadas apenas em números absolutos.

---

<h2 align="center">🛠️ Tecnologias utilizadas</h2>

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" height="40" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" height="40" />
</p>

---

<h2 align="center">📂 Estrutura do Repositório</h2>
📁 data/ → Dataset utilizado
📁 notebooks/ → Análises e visualizações
📁 src/ → Scripts de limpeza e tratamento
README.html → Este arquivo


---

<h2 align="center">✈️ Conclusão</h2>

Este projeto mostrou que atrasos não acontecem por acaso eles seguem padrões claros ligados a companhia, volume de voos e principalmente **rotas específicas**.  
A análise abriu caminho para estudos mais avançados, como previsões de atraso utilizando modelos de machine learning.


