---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 24
url: https://github.com/VictorNascimento14/Vitalbank/pull/24
branch: ui/bloco-e-titulo
tags: [pr, design, primitivos]
status: aberto
---

# PR #24 — ui(primitivos): Bloco e TituloDeSecao, a moldura de todas as telas

## 🎯 Contexto

Primitivos, item 1. Valores em [[linguagem-visual]]. Fecha a issue #23.

## 🔧 Mudanças

- `src/ui/base/{Bloco,TituloDeSecao}.tsx`, `src/ui/cx.ts`, `src/ui/index.ts` + teste.

## 🧠 Decisões técnicas

- **Componentes de servidor.** Nenhum dos dois tem estado nem movimento; ficam fora do bundle do cliente.
- **`cx` de 3 linhas em vez de `clsx` + `tailwind-merge`.** Os primitivos não deixam a tela sobrescrever classe conflitante; quando precisar, a variante entra no primitivo.
- **Título menor no celular** (18 px): o 22 px do kit desktop quebra linha ao lado da ação em 375 px.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
