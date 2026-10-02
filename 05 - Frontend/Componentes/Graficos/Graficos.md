---
tipo: componente
camada: ui
arquivo: src/ui/graficos/
ultima_atualizacao: 2026-10-02
tags: [graficos]
---

# Gráficos

SVG próprio animado com motion — [[ADR-004-graficos-proprios-em-svg]].

| Peça | O que faz | PR |
|---|---|---|
| `escala.ts` | `escalaLinear`, `marcasDoEixo`, `caminhoSuave` (monotônica) | [[2026-10-02-pr-058-graficos-escala]] |
| `GraficoDeBarras` | barras agrupadas em pílula; crescem da base em cascata; dica por coluna; tabela `sr-only` | [[2026-10-02-pr-060-grafico-de-barras]] |
| `geometria.ts` | `noCirculo`, `fatias`, `setor` (pizza/rosca; 0 rad às 12 h) | [[2026-10-02-pr-064-graficos-geometria]] |
| `GraficoDePizza` | pizza explodida, raio por fatia, rótulo dentro; abre do centro; fatia em foco se afasta | [[2026-10-02-pr-066-grafico-de-pizza]] |
| `GraficoDeLinha` | linha suave ou reta, área em degradê, pontos, grade tracejada; desenha-se ao aparecer; guia com valor | [[2026-10-02-pr-072-grafico-de-linha]] |
