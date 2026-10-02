---
tipo: componente
camada: dominio
arquivo: src/dominio/cartao.ts
ultima_atualizacao: 2026-10-02
tags: [dominio, cartao, seguranca]
---

# Cartão mascarado

O app só conhece o **final** do cartão (`ultimos4`). O número inteiro não existe nem na semente.

| Função | Faz |
|---|---|
| `mascararCartao(final, prefixo?)` | "3778 •••• •••• 1234" |
| `finalDoCartao(final)` | "•••• 1234" |
| `agruparDigitos(texto)` | 4 em 4 enquanto digita, até 16 |
| `passaNoLuhn(numero)` | pega erro de digitação; não diz se o cartão existe |
| `validadeEmDia("MM/AA", hoje)` | vale até o fim do mês impresso |

Introduzido em [[2026-10-02-pr-016-cartao-mascarado]].
