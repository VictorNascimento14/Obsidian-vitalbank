---
tipo: componente
camada: ui
arquivo: src/ui/casca/ColunaLateral.tsx
ultima_atualizacao: 2026-10-02
tags: [casca, navegacao]
---

# Coluna lateral

Menu de 250 px com a [[Marca]] no topo e as 9 telas de `NAVEGACAO` (`src/ui/casca/navegacao.ts`), que também dá o título do cabeçalho.

| Rota | Menu |
|---|---|
| `/` | Visão geral |
| `/transacoes` | Transações |
| `/contas` | Contas |
| `/investimentos` | Investimentos |
| `/cartoes` | Cartões (título: Cartões de crédito) |
| `/emprestimos` | Empréstimos |
| `/servicos` | Serviços |
| `/privilegios` | Meus privilégios |
| `/configuracoes` | Configurações |

- Item ativo: `primaria`, `aria-current="page"` e a barra de 6 px que **desliza em mola** (`layoutId`).
- Hover: ícone cresce, texto anda 4 px.
- `/` só acende em `/` exato; as outras acendem nas sub-rotas.
- O título da aba também sai daqui: `metadadosDaTela(rota)` → "Transações · Vitalbank".

Introduzido em [[2026-10-02-pr-040-coluna-lateral]].
