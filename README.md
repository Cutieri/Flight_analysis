<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>README — Análise de Atrasos de Voos</title>
  <style>
    :root{--bg:#0f1720;--card:#0b1220;--muted:#9aa4b2;--accent:#4c9fef;--accent2:#ff7b54;--text:#e6eef6}
    body{font-family:Inter,Segoe UI,Roboto,Arial,sans-serif;background:linear-gradient(180deg,#071126 0%, #071826 100%);color:var(--text);margin:0;padding:32px}
    .wrapper{max-width:980px;margin:0 auto}
    header{display:flex;align-items:center;gap:20px;margin-bottom:18px}
    h1{margin:0;font-size:28px}
    .meta{color:var(--muted);font-size:13px}
    .card{background:rgba(255,255,255,0.02);border:1px solid rgba(255,255,255,0.03);padding:18px;border-radius:10px;margin-bottom:16px}
    section h2{margin-top:0}
    table{width:100%;border-collapse:collapse;margin:12px 0}
    th,td{padding:8px 10px;text-align:left;border-bottom:1px solid rgba(255,255,255,0.03)}
    th{color:var(--muted);font-weight:600}
    .kbd{background:#071a2e;border-radius:6px;padding:6px 8px;font-family:monospace;font-size:13px}
    .pill{display:inline-block;background:linear-gradient(90deg,var(--accent),var(--accent2));color:#fff;padding:6px 10px;border-radius:999px;font-weight:600;font-size:13px}
    footer{color:var(--muted);font-size:13px;margin-top:18px}
    .grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    @media(max-width:720px){.grid{grid-template-columns:1fr} }
  </style>
</head>
<body>
  <div class="wrapper">
    <header>
      <div>
        <h1>📊 README — Análise de Atrasos de Voos</h1>
        <div class="meta">Dataset: NYC Flights 2013 — Análise exploratória, limpeza, visualizações e insights</div>
      </div>
      <div style="margin-left:auto"><span class="pill">Data Science • Pandas • Matplotlib</span></div>
    </header>

    <div class="card">
      <strong>Resumo rápido</strong>
      <p class="meta">Resumo executivo com os principais resultados e recomendações — use este arquivo como entrada para o relatório.</p>
      <ul>
        <li>Média geral de atraso: <strong>6.37 minutos</strong>.</li>
        <li>Companhias com média superior à média geral: <strong>9E, B6, EV, F9, FL, MQ, OO, WN, YV</strong>.</li>
        <li>Top 3 por volume de voos: <strong>UA, B6, DL</strong>.</li>
        <li>Top 3 por atraso absoluto: <strong>EV, B6, UA</strong> (em minutos totais).</li>
        <li>Top 3 por proporção de voos atrasados: <strong>FL (61.2%), YV (56.8%), F9 (56.2%)</strong>.</li>
        <li>Rotas com maior atraso médio: destaque para rotas saindo de <strong>EWR (Newark)</strong> — ex.: <strong>EWR–GSO (212 min)</strong>.</li>
        <li>A aeronave (tailnum) também influencia: há tailnums com média de atraso muito alta (ex.: <strong>N844MH</strong>).</li>
      </ul>
    </div>

    <section class="card">
      <h2>Problema e objetivo</h2>
      <p>Identificar quais fatores (companhia, rota, aeronave, horário) influenciam os atrasos nos voos de NYC em 2013 e propor ações com base em evidência.</p>
    </section>

    <section class="card">
      <h2>Como os resultados foram encontrados</h2>
      <div class="grid">
        <div>
          <h3>Limpeza e preparação</h3>
          <ul>
            <li>Remoção de voos cancelados (linhas com <code>arr_delay</code> nulo) para análise de atrasos.</li>
            <li>Conversão de <code>dep_time</code>/<code>arr_time</code> para formato horário (pad 4 dígitos e parse).</li>
            <li>Criação de colunas derivadas: <code>route</code> (= origin+"-"+dest), <code>hour</code>, <code>date</code>.</li>
          </ul>
        </div>

        <div>
          <h3>Métricas calculadas</h3>
          <ul>
            <li>Média, mediana, soma e contagem de <code>arr_delay</code> por <code>carrier</code>, <code>route</code> e <code>tailnum</code>.</li>
            <li>Proporção de voos com atraso (&gt;0) por companhia.</li>
            <li>Rankings (topN) e filtros por mínimo de observações para relevância estatística.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="card">
      <h2>Principais insights (detalhado)</h2>
      <h3>Companhias</h3>
      <p>As companhias exibem comportamento distinto — algumas atrasam com frequência, outras acumulam minutos de atraso por terem grande volume de voos. Para medir corretamente, usamos três lentes: <em>(1)</em> média de atraso, <em>(2)</em> proporção de voos atrasados, e <em>(3)</em> atraso total acumulado.</p>

      <h3>Rotas</h3>
      <p>Rotas que partem de <strong>EWR</strong> aparecem repetidamente entre as mais atrasadas. Isso indica fatores estruturais do aeroporto (capacidade, clima, slots) impactando o resultado.</p>

      <h3>Aeronaves</h3>
      <p>Existem tailnums com atraso médio sistematicamente elevado. Análises filtradas por aeronaves com alto número de voos foram usadas para evitar conclusões de fontes com amostra pequena.</p>
    </section>

    <section class="card">
      <h2>Visualizações recomendadas</h2>
      <ol>
        <li>Barplot: atraso médio por companhia (ordenado).</li>
        <li>Barplot: proporção de voos atrasados por companhia.</li>
        <li>Top 10 rotas com maior atraso médio (barplot).</li>
        <li>Scatter: nº de voos por aeronave vs. atraso médio (para checar tendência).</li>
        <li>Heatmap: origem × destino (média de atraso).</li>
        <li>Timeseries: atraso médio por hora do dia e por mês.</li>
      </ol>
    </section>

    <section class="card">
      <h2>Recomendações operacionais</h2>
      <ul>
        <li>Reforçar manutenção e substituição de aeronaves com histórico ruim.</li>
        <li>Aumentar buffers em janelas críticas (tarde/noite) para reduzir efeito cascata.</li>
        <li>Reavaliar distribuição de slots e infraestrutura em EWR.</li>
        <li>Monitoramento contínuo: automatizar alertas para tailnums e rotas que ultrapassarem thresholds.</li>
      </ul>
    </section>

    <section class="card">
      <h2>Como reproduzir (executar notebooks)</h2>
      <ol>
        <li>Clone o repositório e instale dependências: <span class="kbd">pip install -r requirements.txt</span></li>
        <li>Abra os notebooks em <span class="kbd">notebooks/</span>.</li>
        <li>Execute as células na ordem: <em>cleaning</em> → <em>analysis</em> → <em>visualizations</em>.</li>
      </ol>
    </section>

    <footer>
      <div class="meta">Arquivo gerado automaticamente — edite conforme necessário. Se quiser que eu adicione gráficos embutidos, badges ou uma versão em inglês, eu faço isso pra você.</div>
    </footer>
  </div>
</body>
</html>
