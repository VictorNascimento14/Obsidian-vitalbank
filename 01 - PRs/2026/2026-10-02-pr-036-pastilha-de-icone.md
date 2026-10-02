---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 36
url: https://github.com/VictorNascimento14/Vitalbank/pull/36
branch: ui/pastilha-de-icone
tags: [pr, design, primitivos, icones]
status: merged
---

# PR #36 — ui(primitivos): ícones Remix e a PastilhaDeIcone colorida

## 🎯 Contexto

Primitivos, item 7. Ícones decididos em [[ADR-002-design-system-bankdash]] (item 5). Fecha a issue #35.

## 🔧 Mudanças

- `package.json` — `@remixicon/react`.
- `src/ui/base/PastilhaDeIcone.tsx` + teste; exportado em `@/ui` com o tipo `Tom`.

## 🧠 Decisões técnicas

- **Tamanho do ícone pelo pai (`[&>svg]:size-6`)**: quem usa só passa o ícone, sem repetir tamanho em cada lugar.
- **Hover por `group-hover`**, em CSS: a pastilha reage ao mouse na linha inteira, não só sobre ela, e não precisa de JavaScript.
- **Remix Icon** em vez de SVGs do kit: o kit não traz licença dos ícones, e o Remix tem as versões preenchidas (`*Fill`) no mesmo espírito.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
