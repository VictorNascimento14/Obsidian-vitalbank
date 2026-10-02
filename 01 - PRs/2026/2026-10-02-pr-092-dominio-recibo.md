---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 92
url: https://github.com/VictorNascimento14/Vitalbank/pull/92
branch: feat/dominio-recibo
tags: [pr, dominio, recibo]
status: aberto
---

# PR #92 — feat(dominio): texto do recibo de transação

## 🎯 Contexto

Transações, item 4 (parte 1). Fecha a issue #91.

## 🔧 Mudanças

- `src/dominio/recibo.ts` + teste.

## 🕵️ Dado sensível

O recibo só leva o que já está na tela: cartão pelo final ([[CartaoMascarado]]), nenhum dado de titular.

## 🧠 Decisões técnicas

- **"Sem valor fiscal" escrito no próprio arquivo**: o arquivo sai do app e pode ser lido fora de contexto ([[ADR-001-frontend-primeiro-com-dados-mock]]).
- **Rótulo do tipo por parâmetro**: o domínio não depende da tabela de rótulos da tela.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Recibo]]
- [[2026]] (changelog)
