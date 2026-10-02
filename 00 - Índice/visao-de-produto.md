---
tipo: indice
ultima_atualizacao: 2026-10-02
tags: [indice, produto]
---

# Visão de produto

**Vitalbank** é o painel de um banco digital: a pessoa abre e vê, numa tela só, seus cartões, o que
entrou e saiu na semana, para onde foi o dinheiro e quanto tem guardado. Dali navega para o detalhe —
transações, contas, investimentos, cartões, empréstimos, serviços e configurações.

## Para quem

Quem usa banco pelo celular e pelo computador e quer **entender o próprio dinheiro de relance**, sem
abrir extrato linha a linha.

## O que a v1 é

- **Só front-end, com dados fictícios** ([[ADR-001-frontend-primeiro-com-dados-mock]]). Nenhuma tela
  movimenta dinheiro de verdade: transferir, adicionar cartão e salvar configurações só mudam o estado
  da página.
- **Bonita e viva.** O sistema visual parte do UI kit BankDash ([[ADR-002-design-system-bankdash]]) e o
  movimento é parte do produto: números que contam até o valor, gráficos que crescem ao entrar na tela,
  cartões que respondem ao mouse ([[ADR-003-movimento-com-motion]]).
- **Três tamanhos de tela** desenhados: 1440 px, 1024 px e 375 px.

## O que a v1 não é

- Não tem login, nem backend, nem banco de dados.
- Não processa pagamento, não guarda número de cartão e não pede CPF.

Telas e backlog em [[2026-10-02-plano-da-v1]]; mapa do código em [[vitalbank-frontend]].
