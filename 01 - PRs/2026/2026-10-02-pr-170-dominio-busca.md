---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 170
url: https://github.com/VictorNascimento14/Vitalbank/pull/170
branch: feat/dominio-busca
tags: [pr, dominio, busca]
status: merged
---

# PR #170 — feat(dominio): busca sem acento, com todas as palavras e ordem por relevância

## 🎯 Contexto

Sistema, item 6 (parte 1). Fecha a issue #169.

## 🔧 Mudanças

- `src/dominio/busca.ts` + teste.

## 🧠 Decisões técnicas

- **Sem acento dos dois lados**: em português, quem digita no celular raramente acentua; "transacoes" precisa achar "Transações".
- **Todas as palavras (E), não qualquer (OU)**: "transf wilson" deve estreitar, não alargar.
- **Busca em memória**: índice de dezenas de itens. Com backend, o índice de transações vira consulta; telas e serviços continuam locais.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Busca]]
- [[2026]] (changelog)
