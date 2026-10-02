---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 66
url: https://github.com/VictorNascimento14/Vitalbank/pull/66
branch: feat/grafico-de-pizza
tags: [pr, graficos, animacao, acessibilidade]
status: aberto
---

# PR #66 — feat(graficos): pizza explodida que abre do centro e destaca a fatia com o mouse

## 🎯 Contexto

Gráficos, item 4. Usa [[2026-10-02-pr-064-graficos-geometria]]. Fecha a issue #65.

## 🔧 Mudanças

- `src/ui/graficos/GraficoDePizza.tsx` + teste; exportado em `@/ui` com o tipo `Fatia`.

## 🧠 Decisões técnicas

- **Dois `<g>` por fatia**: o de fora faz a entrada (escala a partir do centro do desenho); o de dentro, o afastamento do hover. Juntos no mesmo elemento, a mola do hover brigaria com a animação de entrada.
- **`originX/originY` em px do desenho** (150, 150): sem isso o motion escala cada fatia a partir do próprio canto.
- **Percentual pela fração real**, não pelo `valor`: a semente pode vir em centavos.

## 🧪 Como testar

1. Captura do bloco.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026]] (changelog)
