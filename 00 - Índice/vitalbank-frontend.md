---
tipo: indice
ultima_atualizacao: 2026-10-02
tags: [indice, frontend]
camada: frontend
---

# Vitalbank — front-end

Mapa das telas e peças do app. Linguagem visual em [[linguagem-visual]].

## Fundação

- Base: Next.js 16 + React 19 + TypeScript + Tailwind 4 + pnpm — [[2026-10-02-pr-002-scaffolding]].
- Testes: Vitest + jsdom + Testing Library — [[2026-10-02-pr-004-testes]].
- CI: lint, type-check, test, build e link do cofre obrigatório — [[2026-10-02-pr-006-ci]].
- [[Dinheiro]] — centavos inteiros, `formatarMoeda`, `somarCentavos`, `paraCentavos` — [[2026-10-02-pr-012-dinheiro]].
- [[Datas]] — `AAAA-MM-DD` lido no horário local; formatos longo, curto, eixo e relativo — [[2026-10-02-pr-014-datas]].
- [[CartaoMascarado]] — máscara, Luhn e validade — [[2026-10-02-pr-016-cartao-mascarado]].
- [[CamadaDeDados]] — tipos, sementes e funções `async` de leitura — [[2026-10-02-pr-048-dados-base]].

## Design system (`src/ui/`)

- Tokens: cores, raios, sombra, tipografia e grade em `globals.css` — [[2026-10-02-pr-008-tokens]] · [[linguagem-visual]].
- Fontes: Inter (padrão) e Lato (`font-cartao`) pelo `next/font` — [[2026-10-02-pr-010-fontes]].
- [[Movimento]] — `motion`, ritmo comum, `ProvedorDeMovimento`, `Surgir` — [[2026-10-02-pr-018-movimento-base]].
- [[Primitivos]] — `Bloco`, `TituloDeSecao`… — [[2026-10-02-pr-024-bloco-e-titulo]].
- [[Marca]] — símbolo de dois cartões e "Vitalbank." — [[2026-10-02-pr-038-marca]].
- [[ColunaLateral]] — menu das 9 telas, marcador deslizante — [[2026-10-02-pr-040-coluna-lateral]].
- [[Cabecalho]] — título, busca, atalhos, avatar — [[2026-10-02-pr-042-cabecalho]].
- [[Casca]] — layout `(painel)`: coluna fixa ≥ 1024 px, gaveta abaixo — [[2026-10-02-pr-046-layout-do-painel]].
- [[CartaoDeCredito]] — 3 faces, inclinação 3D e reflexo — [[2026-10-02-pr-050-cartao-de-credito]].

## Telas

- [[VisaoGeral]] — `/`
