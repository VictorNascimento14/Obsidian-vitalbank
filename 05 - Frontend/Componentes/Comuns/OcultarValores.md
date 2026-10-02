---
tipo: componente
camada: ui
ultima_atualizacao: 2026-10-02
tags: [privacidade]
---

# Ocultar valores

- Valor pessoal leva a classe `valor-sensivel` (saldos, transações, faturas, empréstimos, valor investido, eixos de dinheiro).
- Com `data-ocultar` no `<html>`, `globals.css` borra esses valores (`blur(7px)`, com transição).
- Preço de ação e pontos **não** são marcados.
- O leitor de tela continua lendo: é proteção contra quem olha a tela.

Mecanismo em [[2026-10-02-pr-188-valores-sensiveis]].

Botão no cabeçalho, lembrado entre visitas e aplicado antes da pintura: [[2026-10-02-pr-190-botao-ocultar-valores]].
