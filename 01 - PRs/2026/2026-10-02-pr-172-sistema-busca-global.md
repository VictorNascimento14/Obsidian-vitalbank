---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 172
url: https://github.com/VictorNascimento14/Vitalbank/pull/172
branch: feat/sistema-busca-global
tags: [pr, sistema, busca, acessibilidade, animacao]
status: merged
---

# PR #172 — feat(sistema): busca global com Ctrl+K em telas, transações e serviços

## 🎯 Contexto

Sistema, item 6 (parte 2). Usa [[2026-10-02-pr-170-dominio-busca]]. Fecha a issue #171.

## 🔧 Mudanças

- `src/telas/comum/BuscaGlobal.tsx` + teste; `src/ui/casca/{Cabecalho,Casca}.tsx` (+ teste); `src/app/(painel)/layout.tsx`.

## 🧠 Decisões técnicas

- **Portal para o `body`**: o modal é `fixed`; dentro do cabeçalho (ou de qualquer ancestral com `transform`/`backdrop-filter`), `fixed` passaria a medir o ancestral.
- **Atalho só no gatilho visível** (`offsetParent !== null`): o cabeçalho tem um gatilho no celular e outro no desktop; sem isso, Ctrl+K abriria dois modais.
- **`aria-activedescendant`**: o foco fica no campo enquanto as setas mudam a opção — dá para continuar digitando.

## ⚠️ Armadilhas e aprendizados

- A primeira versão passava a busca ao cabeçalho como função (`busca={(classe) => …}`). O layout é componente de servidor e **função não atravessa para componente cliente**; virou slot comum, e o cabeçalho envolve o slot em cada posição.

## 🧪 Como testar

1. Captura com "trans" digitado (1440 px).

## 📎 Documentação afetada

- [[Busca]]
- [[Cabecalho]]
- [[2026]] (changelog)
