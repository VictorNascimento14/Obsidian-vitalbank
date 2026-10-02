---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 168
url: https://github.com/VictorNascimento14/Vitalbank/pull/168
branch: feat/sistema-notificacoes
tags: [pr, sistema, notificacoes, animacao, acessibilidade]
status: merged
---

# PR #168 — feat(sistema): painel de notificações no sino do cabeçalho

## 🎯 Contexto

Sistema, item 5. Fecha a issue #167.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/notificacoes.ts}`; `src/telas/comum/Notificacoes.tsx` + teste.
- `src/ui/casca/{Cabecalho,Casca}.tsx` (+ teste do cabeçalho); `src/app/(painel)/layout.tsx` (agora `async`).

## 🧠 Decisões técnicas

- **Slot em vez de importar a tela na casca.** `src/ui/` não depende de `src/telas/` nem de `src/dados/`; quem junta é o layout, que é a página.
- **Clique fora por `mousedown` no `document` testando `contains`**, sem véu `fixed`: um véu dentro do cabeçalho mediria o cabeçalho, não a tela.
- **Balão com `originX: 1, originY: 0`**: cresce de onde o sino está, em vez do centro.

## ⚠️ Armadilhas e aprendizados

- O cabeçalho renderiza o slot duas vezes (versão do celular e do desktop, cada uma escondida por CSS no outro tamanho): são duas instâncias, com estado próprio. Como só uma aparece por vez, não se nota; se um dia as duas aparecerem juntas, o estado de "lida" precisa subir para o layout.

## 🧪 Como testar

1. Captura com o painel aberto (1440 px).

## 📎 Documentação afetada

- [[Notificacoes]]
- [[Cabecalho]]
- [[2026]] (changelog)
