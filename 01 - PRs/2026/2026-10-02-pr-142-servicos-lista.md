---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 142
url: https://github.com/VictorNascimento14/Vitalbank/pull/142
branch: feat/servicos-lista
tags: [pr, servicos, animacao]
status: aberto
---

# PR #142 — feat(servicos): lista de serviços com atributos reais e detalhes que abrem

## 🎯 Contexto

Serviços, item 2 — fecha a tela. Fecha a issue #141.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/servicos.ts}`; `src/telas/servicos/ListaDeServicos.tsx` + teste; `src/app/(painel)/servicos/page.tsx`.

## 🧠 Decisões técnicas

- **Atributos como dado** (`{ rotulo, valor }[]`): cada serviço tem os seus três (taxa/prazo/aprovação para crédito; mensalidade/Pix/saques para conta).
- **No celular, os atributos vão para dentro do detalhe**: a linha mostra só nome e botão, como no kit mobile; nada se perde.

## 🧪 Como testar

1. Captura com o primeiro aberto (1440 px) e largura em 375 px.

## 📎 Documentação afetada

- [[Servicos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
