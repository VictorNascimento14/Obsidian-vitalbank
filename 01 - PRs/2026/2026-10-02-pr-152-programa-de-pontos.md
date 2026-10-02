---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 152
url: https://github.com/VictorNascimento14/Vitalbank/pull/152
branch: feat/dominio-programa-de-pontos
tags: [pr, dominio, privilegios]
status: merged
---

# PR #152 — feat(dominio): níveis, pontos e benefícios do programa Meus privilégios

## 🎯 Contexto

Tela própria do Vitalbank (o kit só tem o item no menu). Fecha a issue #151.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/privilegios.ts}`; `src/dominio/niveis.ts` + teste.

## 🧠 Decisões técnicas

- **Níveis por mínimo de pontos**, ordenados na função: a ordem da semente não importa.
- **Progresso dentro do nível** (de 10.000 a 15.000), não do zero: a barra mostra o caminho até o próximo, que é o que a pessoa quer saber.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[ProgramaDePontos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
