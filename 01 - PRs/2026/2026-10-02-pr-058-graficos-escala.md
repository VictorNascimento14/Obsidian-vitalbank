---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 58
url: https://github.com/VictorNascimento14/Vitalbank/pull/58
branch: feat/graficos-escala
tags: [pr, graficos, design]
status: merged
---

# PR #58 — feat(graficos): escalas, marcas de eixo e curva suave para gráficos próprios em SVG

## 🎯 Contexto

Base dos gráficos do Dashboard, Contas, Investimentos e Cartões. Decisão em [[ADR-004-graficos-proprios-em-svg]]. Fecha a issue #57.

## 🔧 Mudanças

- `src/ui/graficos/escala.ts` + teste.

## 🧠 Decisões técnicas

- **Monotônica, não Catmull-Rom.** Num gráfico de saldo, a curva que "estoura" o pico mostra um valor que não aconteceu. Fritsch–Carlson zera a tangente em pico e vale e limita a inclinação.
- **Passos 1 / 2 / 2,5 / 5**: são os que o olho lê como redondos; 3 e 7 geram eixos estranhos.
- **Coordenadas arredondadas a 2 casas** no caminho: o `d` do SVG fica curto e estável para teste.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Graficos]]
- [[ADR-004-graficos-proprios-em-svg]]
- [[2026]] (changelog)
