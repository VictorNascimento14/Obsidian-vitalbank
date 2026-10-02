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
