---
tipo: componente
camada: dominio
arquivo: src/dominio/senha.ts
ultima_atualizacao: 2026-10-02
tags: [dominio, seguranca]
---

# Força da senha

| Situação | Força |
|---|---|
| menos de 6 caracteres, um caractere repetido, ou senha comum | 0 · Muito fraca |
| 1 tipo de caractere | 0 |
| cada tipo a mais (minúscula, maiúscula, número, símbolo) | +1 |
| 12 ou mais caracteres | +1 |

`senhaAceitavel`: 8+, com letra e número. O medidor informa; quem barra é a regra mínima.

Introduzido em [[2026-10-02-pr-148-forca-da-senha]].
