---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 156
url: https://github.com/VictorNascimento14/Vitalbank/pull/156
branch: feat/privilegios-tela
tags: [pr, privilegios, animacao]
status: aberto
---

# PR #156 — feat(privilegios): tela Meus privilégios com nível, pontos e benefícios

## 🎯 Contexto

Tela própria (o kit só tem o item no menu). Usa [[2026-10-02-pr-152-programa-de-pontos]] e [[2026-10-02-pr-154-barra-de-progresso]]. Fecha a issue #155.

## 🔧 Mudanças

- `src/telas/privilegios/{NivelAtual,Beneficios}.tsx` + teste; `src/app/(painel)/privilegios/page.tsx`; `src/app/globals.css`.

## 🧠 Decisões técnicas

- **O cartão do nível reaproveita o gradiente do cartão de crédito**: a tela nova parece do mesmo app sem inventar cor.
- **Benefício trancado mostra o nível que o libera**: diz o que fazer, em vez de só "bloqueado".
- **Coroa decorativa** `aria-hidden` e animação contínua só com `motion-safe:`.

## 🧪 Como testar

1. Captura (1440 px) e largura em 375 px.

## 📎 Documentação afetada

- [[MeusPrivilegios]]
- [[2026]] (changelog)
