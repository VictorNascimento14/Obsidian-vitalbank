---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 60
url: https://github.com/VictorNascimento14/Vitalbank/pull/60
branch: feat/grafico-de-barras
tags: [pr, graficos, animacao, acessibilidade]
status: aberto
---

# PR #60 — feat(graficos): barras agrupadas que crescem da base, com dica e tabela acessível

## 🎯 Contexto

Gráficos, item 2. Decisão em [[ADR-004-graficos-proprios-em-svg]]. Fecha a issue #59.

## 🔧 Mudanças

- `src/ui/graficos/GraficoDeBarras.tsx` + teste; exportado em `@/ui` com o tipo `Serie`.

## 🧠 Decisões técnicas

- **`viewBox` fixo e `w-full`**: o desenho escala inteiro com o bloco. O texto escala junto — aceitável nas larguras do app (de ~330 a ~730 px).
- **`transformBox: fill-box` + `originY: 1`**: sem `fill-box`, a origem do `scaleY` é a do SVG inteiro, e a barra "cai do céu" em vez de crescer da base.
- **Faixa invisível por categoria** captura o ponteiro: passar entre duas barras do mesmo dia não pisca a dica.
- **Cor por nome de token** (`cor: "turquesa"` → `var(--turquesa)`): a tela escolhe papel, não hex.

## 🧪 Como testar

1. Captura do bloco.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026]] (changelog)
