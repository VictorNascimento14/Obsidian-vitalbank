---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 124
url: https://github.com/VictorNascimento14/Vitalbank/pull/124
branch: feat/grafico-de-rosca
tags: [pr, graficos, animacao, acessibilidade]
status: aberto
---

# PR #124 — feat(graficos): rosca com arcos de espessura própria e legenda interativa

## 🎯 Contexto

Gráficos, item 7. Usa [[2026-10-02-pr-064-graficos-geometria]]. Fecha a issue #123.

## 🔧 Mudanças

- `src/ui/graficos/GraficoDeRosca.tsx` + teste; exportado em `@/ui` com o tipo `Arco`.

## 🧠 Decisões técnicas

- **Destaque por `scale` com origem no centro do desenho**, não por recalcular o raio: o arco cresce "para fora" sem mexer no `d`.
- **A legenda também acende o arco**: arco fino (5% do total) é difícil de mirar com o mouse.

## ⚠️ Armadilhas e aprendizados

- A primeira versão animava o `d` do arco com o motion para engrossar no hover. O motion interpola **todos os números** do caminho — inclusive as flags de arco, que só aceitam 0 ou 1 — e o navegador rejeita: `Expected arc flag ('0' or '1')`. Ver [[2026-10-02-motion-nao-anima-d-de-arco]].

## 🧪 Como testar

1. Captura do bloco; console sem erro de `<path>`.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026-10-02-motion-nao-anima-d-de-arco]]
- [[2026]] (changelog)
