---
tipo: indice
ultima_atualizacao: 2026-10-02
tags: [indice, design]
---

# Linguagem visual

Os valores abaixo foram lidos do arquivo **BankDash — Dashboard UI Kit** (Figma Community) pela API de
plugins, em 2026-10-02. Decisão em [[ADR-002-design-system-bankdash]]; movimento em
[[ADR-003-movimento-com-motion]].

## Cores

| Token | Valor | Papel | No Figma |
|---|---|---|---|
| `primaria` | `#1814F3` | botão, item ativo, barra do gráfico | (uso mais comum) |
| `primaria-viva` | `#2D60FF` | link, destaque | Primary 3 |
| `azul` | `#396AFF` | ícones de destaque | — |
| `tinta` | `#343C6A` | títulos de seção e de página | Primary 2 |
| `tinta-forte` | `#232323` | texto de corpo forte | — |
| `tinta-suave` | `#718EBF` | texto secundário, rótulos | — |
| `tinta-apagada` | `#B1B1B1` | item de menu inativo | — |
| `fundo` | `#F5F7FA` | fundo da área de conteúdo | — |
| `superficie` | `#FFFFFF` | cartões, casca | — |
| `borda` | `#E6EFF5` | divisórias, contorno de campo | — |
| `sucesso` | `#16DBAA` | valor de entrada | — |
| `turquesa` | `#16DBCC` | série "depósito", toggle ligado | — |
| `perigo` | `#FE5C73` | valor de saída | Secondery |
| `alerta` | `#FFBB38` | ícone amarelo | — |
| `laranja` | `#FEAA09` | série "crédito" | Primari 1 |
| `rosa` | `#FF82AC` | ícone rosa | — |
| `magenta` | `#FA00FF` | fatia "Investimento" da pizza | — |
| `tangerina` | `#FC7900` | fatia "Contas" da pizza | — |
| `amarelo-claro` / `azul-claro` / `turquesa-clara` / `rosa-claro` | `#FFF5D9` / `#E7EDFF` / `#DCFAF8` / `#FFE0EB` | fundo da pastilha de ícone | — |

Gradientes: cartão escuro `#4C49ED → #0A06F4`; cartão azul `#2D60FF → #539BFF`; "Dark Blue Gradient"
`#123288 → #295EEC`.

## Tipografia

Família **Inter** (Lato aparece nos cartões do kit e entra só neles).

| Estilo | Tamanho | Peso | Uso |
|---|---|---|---|
| Heading one | 28 px | 600 | título da página no cabeçalho |
| Heading two | 22 px | 600 | título de seção |
| Heading four | 20 px | 600 | valores de destaque |
| Heading three | 18 px | 500 | item de menu |
| Body one | 16 px | 400 | texto de linha |
| Body two | 15 px | 400 | rótulos, tabela |
| Body small | 13 px | 400 | legenda |

## Forma, sombra e grade

- Raios: **25 px** cartão (o mais usado), 20, 15 (campo), 10, 50 (pílula).
- Sombra "Shadow 1": `4px 4px 18px -2px rgb(231 228 232 / 0.8)`.
- Casca desktop: coluna lateral **250 px**, cabeçalho **101 px**, miolo com respiro de **40 px** e
  vão de **30 px** entre blocos.
