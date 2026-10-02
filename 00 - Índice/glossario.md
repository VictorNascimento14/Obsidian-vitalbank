---
tipo: glossario
ultima_atualizacao: 2026-10-02
tags: [glossario, dominio]
---

# Glossário

Termos do produto, com o significado que têm **no Vitalbank**. Visão geral em [[visao-de-produto]].

- **Centavos** — Todo valor em dinheiro vive no código como inteiro em centavos. R$ 12,50 é `1250`.
  Real com vírgula só aparece na tela ([[ADR-001-frontend-primeiro-com-dados-mock]]).
- **Cartão mascarado** — O cartão só aparece com os quatro últimos dígitos (`•••• 1234`). O número
  inteiro não existe nem nos dados fictícios.
- **Transação** — Um movimento de dinheiro numa conta: **entrada** (crédito, valor positivo) ou
  **saída** (débito, valor negativo).
- **Transferência rápida** — Envio para um contato frequente direto do painel, sem abrir outra tela.
- **Semente** — Os dados fictícios que o app carrega na v1. Moram em `src/dados/`.
