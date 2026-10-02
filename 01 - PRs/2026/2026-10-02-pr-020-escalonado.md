---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 20
url: https://github.com/VictorNascimento14/Vitalbank/pull/20
branch: ui/movimento-escalonado
tags: [pr, design, animacao]
status: merged
---

# PR #20 — ui(movimento): entrada em cascata para listas com Escalonado

## 🎯 Contexto

Movimento, item 2. Base em [[2026-10-02-pr-018-movimento-base]]. Fecha a issue #19.

## 🔧 Mudanças

- `src/ui/movimento/Escalonado.tsx` + teste; exportado em `src/ui/movimento/index.ts`.

## 🧠 Decisões técnicas

- **`variants` com `staggerChildren`**: o grupo controla o tempo, o item só declara o próprio estado. Item fora de um `Escalonado` não anima — falha visível, não silenciosa.
- **`como` em vez de envolver em `div`.** Uma `div` animada entre `<tbody>` e `<tr>` quebra a tabela e o leitor de tela.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Movimento]]
- [[2026]] (changelog)
