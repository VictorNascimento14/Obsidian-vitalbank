---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 32
url: https://github.com/VictorNascimento14/Vitalbank/pull/32
branch: ui/alternador
tags: [pr, design, primitivos, animacao, acessibilidade]
status: aberto
---

# PR #32 — ui(primitivos): Alternador liga/desliga com a bolinha em mola

## 🎯 Contexto

Primitivos, item 5. Fecha a issue #31.

## 🔧 Mudanças

- `src/ui/base/Alternador.tsx` + teste; `--shadow-bolinha` em `globals.css`.

## 🧠 Decisões técnicas

- **`layout` do motion em vez de `translateX` calculado.** O trilho alinha a bolinha com `justify-start/end`; o motion anima a troca de posição com mola, sem conta de pixel que quebraria se o tamanho mudar.
- **Controlado e não controlado** com o mesmo componente: Preferências guarda o estado na tela; um interruptor solto pode cuidar de si.
- Sombra virou token (`shadow-bolinha`) em vez de valor arbitrário com cor solta.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
