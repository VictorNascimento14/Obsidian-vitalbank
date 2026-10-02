---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 154
url: https://github.com/VictorNascimento14/Vitalbank/pull/154
branch: ui/barra-de-progresso
tags: [pr, design, primitivos, animacao, acessibilidade]
status: aberto
---

# PR #154 — ui(primitivos): BarraDeProgresso que enche ao aparecer

## 🎯 Contexto

Primitivos. Fecha a issue #153.

## 🔧 Mudanças

- `src/ui/base/BarraDeProgresso.tsx` + teste; exportado em `@/ui`.

## 🧠 Decisões técnicas

- **`aria-valuetext`**: "50%" não diz nada; "faltam 2.520 pontos" diz.
- **`scaleX` em vez de `width`**: invariante 4 do `CLAUDE.md` (só transform/opacity animam).

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
