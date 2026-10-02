---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 128
url: https://github.com/VictorNascimento14/Vitalbank/pull/128
branch: feat/cartoes-lista
tags: [pr, cartoes, animacao, acessibilidade]
status: merged
---

# PR #128 — feat(cartoes): Lista de cartões com ficha que abre em Ver detalhes

## 🎯 Contexto

Cartões, item 3. Fecha a issue #127.

## 🔧 Mudanças

- `src/telas/cartoes/ListaDeCartoes.tsx` + teste; `src/app/(painel)/cartoes/page.tsx`.

## 🧠 Decisões técnicas

- **Acordeão com uma ficha aberta**: a lista tem três itens; duas fichas abertas empurram o resto da tela sem ganho.
- **`height: "auto"` animado pelo motion**: o CSS não anima até `auto`; o motion mede e anima.
- **Coluna do botão em 8,5 rem**: a primeira captura mostrou colunas tortas quando uma linha dizia "Fechar" e as outras "Ver detalhes".

## 🧪 Como testar

1. Captura com a primeira ficha aberta (1440 px).

## 📎 Documentação afetada

- [[CartoesDeCredito]]
- [[2026]] (changelog)
