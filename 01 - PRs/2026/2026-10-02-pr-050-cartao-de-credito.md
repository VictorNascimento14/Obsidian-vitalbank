---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 50
url: https://github.com/VictorNascimento14/Vitalbank/pull/50
branch: ui/cartao-de-credito
tags: [pr, design, cartao, animacao]
status: aberto
---

# PR #50 — ui(cartao): cartão de crédito em três faces, com inclinação 3D e reflexo ao mouse

## 🎯 Contexto

Dashboard, item 1. Valores do Figma em [[linguagem-visual]]. Fecha a issue #49.

## 🔧 Mudanças

- `src/ui/cartao/CartaoDeCredito.tsx` + teste; exportado em `@/ui`.
- `src/app/globals.css` — gradientes das faces.

## 🕵️ Dado sensível

A face só mostra `inicio` + `final` via `mascararCartao` ([[CartaoMascarado]]). O `aria-label` fala só o final.

## 🧠 Decisões técnicas

- **Motion values em vez de estado.** O ponteiro escreve em `useMotionValue`; `useTransform` e `useSpring` derivam rotação e posição do reflexo sem nenhum re-render do React.
- **Só `pointerType === "mouse"` inclina.** No toque, o `pointermove` vem junto com a rolagem, e o cartão balançaria enquanto a pessoa rola a tela.
- **Gradientes como variável de `:root`** consumidos por `bg-(image:--…)`, a sintaxe do Tailwind 4 para variável em utilidade.
- **Bandeira genérica** (dois círculos), não a de uma marca real.

## 🧪 Como testar

1. Captura em 1440 px com as três faces.

## 📎 Documentação afetada

- [[CartaoDeCredito]]
- [[2026]] (changelog)
