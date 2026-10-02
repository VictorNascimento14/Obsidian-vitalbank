---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 96
url: https://github.com/VictorNascimento14/Vitalbank/pull/96
branch: ui/cartao-de-resumo
tags: [pr, design, primitivos, animacao]
status: merged
---

# PR #96 — ui(primitivos): CartaoDeResumo com número que conta e pastilha fluida

## 🎯 Contexto

Primitivos. Usa [[2026-10-02-pr-022-numero-animado]]. Fecha a issue #95.

## 🔧 Mudanças

- `src/ui/base/CartaoDeResumo.tsx` + teste; `src/ui/base/PastilhaDeIcone.tsx` (tamanho `fluido`); `src/ui/index.ts`.

## 🧠 Decisões técnicas

- **Hover só com `translate` e `box-shadow` em CSS** (`transition-[translate,box-shadow]`): nada de JavaScript para um efeito de passar o mouse.
- **`whitespace-nowrap` no valor** e fonte menor no celular: valor em reais quebrado em duas linhas ("R$ 12.750," / "00") é ilegível.

## ⚠️ Armadilhas e aprendizados

- A primeira captura em 375 px cortava "R$ 12.750,00" no cartão: em duas colunas, cada cartão tem ~155 px. Pastilha de 45 px e valor de 13 px resolveram.

## 🧪 Como testar

1. Capturas 1440 / 375 px.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
