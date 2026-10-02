---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 52
url: https://github.com/VictorNascimento14/Vitalbank/pull/52
branch: feat/visao-geral-meus-cartoes
tags: [pr, visao-geral, cartao]
status: aberto
---

# PR #52 — feat(visao-geral): bloco Meus cartões, com fila deslizante no celular

## 🎯 Contexto

Visão geral, item 1. Usa [[CartaoDeCredito]]. Fecha a issue #51.

## 🔧 Mudanças

- `src/telas/visao-geral/MeusCartoes.tsx` + teste.
- `src/app/(painel)/page.tsx` + teste — a página passa a ler dados e compor blocos.

## 🧠 Decisões técnicas

- **Blocos de tela em `src/telas/<tela>/`**, a página só compõe: a página fica curta e cada bloco tem teste próprio.
- **Grade por proporção (`73fr : 35fr`)**, não por pixel: em 1440 px dá os 730 / 350 do kit; acima disso cresce junto.
- **Fila no celular com margem negativa (`-mx-6 px-6`)**: o cartão encosta na borda da tela ao rolar, como no app do kit, sem quebrar o respiro do resto.

## 🧪 Como testar

1. Capturas 1440 / 375 px.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[2026]] (changelog)
