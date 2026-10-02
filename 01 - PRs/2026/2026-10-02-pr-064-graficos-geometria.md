---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 64
url: https://github.com/VictorNascimento14/Vitalbank/pull/64
branch: feat/graficos-geometria
tags: [pr, graficos]
status: aberto
---

# PR #64 — feat(graficos): geometria de setores para pizza e rosca

## 🎯 Contexto

Gráficos, item 3. Fecha a issue #63.

## 🔧 Mudanças

- `src/ui/graficos/geometria.ts` + teste.

## 🧠 Decisões técnicas

- **0 rad às 12 horas, sentido horário** (`x = sen`, `y = −cos`): é como se lê pizza; o padrão trigonométrico (3 horas, anti-horário) obrigaria a corrigir em todo chamador.
- **Volta inteira em duas metades**: um arco SVG com início e fim no mesmo ponto não desenha nada — uma fatia de 100% sumiria.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026]] (changelog)
