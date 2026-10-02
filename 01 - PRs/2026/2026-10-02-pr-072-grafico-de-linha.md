---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 72
url: https://github.com/VictorNascimento14/Vitalbank/pull/72
branch: feat/grafico-de-linha
tags: [pr, graficos, animacao, acessibilidade]
status: merged
---

# PR #72 — feat(graficos): linha e área que se desenham, com guia e valor ao passar o mouse

## 🎯 Contexto

Gráficos, item 5. Usa `caminhoSuave` de [[2026-10-02-pr-058-graficos-escala]]. Fecha a issue #71.

## 🔧 Mudanças

- `src/ui/graficos/GraficoDeLinha.tsx` + teste; exportado em `@/ui`.

## 🧠 Decisões técnicas

- **Ponto mais próximo pelo X do mouse**, convertido para coordenadas do `viewBox`: a guia "gruda" no mês, sem precisar mirar na linha.
- **Id do degradê por instância** (`useId`) — lição de [[2026-10-02-gradiente-de-svg-com-id-repetido]]: Investimentos tem dois gráficos de linha na mesma tela.
- **Bolinhas com atraso proporcional à posição**: aparecem mais ou menos quando a linha chega nelas.

## 🧪 Como testar

1. Captura do bloco.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026]] (changelog)
