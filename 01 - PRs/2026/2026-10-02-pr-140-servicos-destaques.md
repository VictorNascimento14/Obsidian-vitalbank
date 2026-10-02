---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 140
url: https://github.com/VictorNascimento14/Vitalbank/pull/140
branch: feat/servicos-destaques
tags: [pr, servicos]
status: aberto
---

# PR #140 — feat(servicos): três serviços em destaque no topo da tela

## 🎯 Contexto

Serviços, item 1. Fecha a issue #139.

## 🔧 Mudanças

- `src/telas/servicos/DestaquesDeServicos.tsx` + teste; `src/app/(painel)/servicos/page.tsx`.

## 🧠 Decisões técnicas

- **Conteúdo fixo na tela, não na camada de dados**: é texto de produto (vitrine), não dado da conta.
- **Título em cima, frase embaixo** — o inverso do `CartaoDeResumo` (rótulo pequeno, valor grande); por isso um bloco próprio em vez de forçar o primitivo.

## 🧪 Como testar

1. Largura em 375 px e teste.

## 📎 Documentação afetada

- [[Servicos]]
- [[2026]] (changelog)
