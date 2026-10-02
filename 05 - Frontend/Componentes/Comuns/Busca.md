---
tipo: componente
camada: dominio
arquivo: src/dominio/busca.ts
ultima_atualizacao: 2026-10-02
tags: [busca]
---

# Busca

- `normalizar`: sem acento (`NFD` + `\p{Diacritic}`), minúsculas.
- `buscar(itens, termo)`: todas as palavras em título ou detalhe; ordem: começa com > contém no título > só detalhe; até 8.

Regra introduzida em [[2026-10-02-pr-170-dominio-busca]].

## Busca global

`src/telas/comum/BuscaGlobal.tsx`, no cabeçalho por slot. Ctrl+K / ⌘K de qualquer tela; portal com véu;
↑ ↓ (destaque desliza), Enter vai, Esc fecha. Índice (telas, transações, serviços) montado no layout do
painel. — [[2026-10-02-pr-172-sistema-busca-global]]
