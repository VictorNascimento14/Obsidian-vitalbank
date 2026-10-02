---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 18
url: https://github.com/VictorNascimento14/Vitalbank/pull/18
branch: ui/movimento-base
tags: [pr, design, animacao]
status: merged
---

# PR #18 — ui(movimento): instalar motion, ritmo comum e o primitivo Surgir

## 🎯 Contexto

Fundação, movimento. Decisão em [[ADR-003-movimento-com-motion]]. Fecha a issue #17.

## 🔧 Mudanças

- `package.json` — `motion`.
- `src/ui/movimento/{ritmo.ts, ProvedorDeMovimento.tsx, Surgir.tsx, index.ts}` + teste.
- `src/app/layout.tsx`, `src/app/page.tsx`, `src/app/globals.css`, `vitest.setup.ts`.

## 🧠 Decisões técnicas

- **`MotionConfig reducedMotion="user"` na raiz** em vez de checar `useReducedMotion` em cada componente: o motion desliga transform e layout para quem pediu, e mantém só opacidade. Uma regra, um lugar.
- **Disparo por margem (`margin: "0px 0px -40px 0px"`), não por fração.** Com `amount: 0.5`, um bloco mais alto que a tela nunca fica 50% visível e ficaria preso em `opacity: 0`.
- **`once: true`.** Rolar para cima e para baixo não repete a entrada — repetição cansa.
- O provedor é componente cliente; o `layout.tsx` continua servidor e só o importa.

## ⚠️ Armadilhas e aprendizados

- O jsdom não tem `IntersectionObserver` nem `matchMedia`; sem os falsos no setup, qualquer teste que monte um `whileInView` quebra com `ReferenceError`.

## 🧪 Como testar

1. Página inicial com e sem "reduzir movimento".

## 📎 Documentação afetada

- [[Movimento]]
- [[ADR-003-movimento-com-motion]]
- [[2026]] (changelog)
