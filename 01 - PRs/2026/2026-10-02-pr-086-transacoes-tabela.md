---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 86
url: https://github.com/VictorNascimento14/Vitalbank/pull/86
branch: feat/transacoes-tabela
tags: [pr, transacoes, tabela, responsivo]
status: merged
---

# PR #86 — feat(transacoes): extrato em tabela no desktop e em lista no celular

## 🎯 Contexto

Transações, item 2. Usa os códigos de [[2026-10-02-pr-082-dados-codigo-da-transacao]]. Fecha a issue #85.

## 🔧 Mudanças

- `src/telas/transacoes/TabelaDeTransacoes.tsx` + teste; `src/app/(painel)/transacoes/page.tsx`.

## 🕵️ Dado sensível

Coluna Cartão por `finalDoCartao` — só o final ([[CartaoMascarado]]).

## 🧠 Decisões técnicas

- **Duas marcações (tabela e lista)** em vez de uma tabela "responsiva" com `display: block`: tabela convertida em bloco perde a semântica para o leitor de tela.
- **`TIPO` exportado**: o rótulo da categoria será usado pela busca e pelo recibo.
- **Seta pelo sinal do valor**, não pela categoria: um depósito estornado é saída.

## 🧪 Como testar

1. Capturas 1440 / 375 px.

## 📎 Documentação afetada

- [[Transacoes]]
- [[2026]] (changelog)
