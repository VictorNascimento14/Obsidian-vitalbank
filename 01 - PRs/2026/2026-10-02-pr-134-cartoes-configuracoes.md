---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 134
url: https://github.com/VictorNascimento14/Vitalbank/pull/134
branch: feat/cartoes-configuracoes
tags: [pr, cartoes, animacao]
status: aberto
---

# PR #134 — feat(cartoes): Configurações do cartão com bloqueio na hora e carteiras digitais

## 🎯 Contexto

Cartões, item 5 — fecha a tela. Fecha a issue #133.

## 🔧 Mudanças

- `src/telas/cartoes/ConfiguracoesDoCartao.tsx` + teste; `src/app/(painel)/cartoes/page.tsx`.

## 🕵️ Dado sensível

"Change Pin Code" do kit ficou de fora de propósito: um campo de PIN, mesmo de mentira, ensina a pessoa a digitar senha numa tela que não é do banco.

## 🧠 Decisões técnicas

- **Rótulo do `Alternador` em `sr-only`**: o título visível da linha já diz o que é; o interruptor precisa do nome para o leitor de tela.
- **Textos curtos** depois da captura: na coluna de 350 px, "Uma notificação a cada compra" quebrava em três linhas.

## 🧪 Como testar

1. Capturas da tela inteira (1440 px) e da coluna.

## 📎 Documentação afetada

- [[CartoesDeCredito]]
- [[2026]] (changelog)
