---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 94
url: https://github.com/VictorNascimento14/Vitalbank/pull/94
branch: feat/transacoes-baixar-recibo
tags: [pr, transacoes, recibo, animacao]
status: merged
---

# PR #94 — feat(transacoes): baixar o recibo de cada transação

## 🎯 Contexto

Transações, item 4 (parte 2). Usa [[2026-10-02-pr-092-dominio-recibo]]. Fecha a issue #93.

## 🔧 Mudanças

- `src/telas/transacoes/BaixarRecibo.tsx` + teste; `src/telas/transacoes/Extrato.tsx`.

## 🧠 Decisões técnicas

- **`Blob` + `<a download>` + `revokeObjectURL`**: o arquivo é gerado e liberado da memória na hora; nada passa por rede.
- **Só no desktop**: a lista do celular não tem a coluna (como no kit mobile).
- **`aria-label` com a descrição**: cinco botões "Baixar" iguais não dizem de qual linha são.

## 🧪 Como testar

1. Teste com `click` do âncora espionado; no navegador, o arquivo baixado.

## 📎 Documentação afetada

- [[Transacoes]]
- [[Recibo]]
- [[2026]] (changelog)
