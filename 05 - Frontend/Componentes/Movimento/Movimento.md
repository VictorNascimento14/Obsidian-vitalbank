---
tipo: componente
camada: ui
arquivo: src/ui/movimento/
ultima_atualizacao: 2026-10-02
tags: [design, animacao]
---

# Movimento

Tudo que anima passa por `src/ui/movimento/`. Decisão em [[ADR-003-movimento-com-motion]].

## Ritmo

| Nome | Valor | Uso |
|---|---|---|
| `duracao.rapida` | 0,15 s | hover, pressão |
| `duracao.media` | 0,3 s | padrão |
| `duracao.lenta` | 0,6 s | entrada de bloco |
| `curvaSaida` / `--ease-saida` | `cubic-bezier(0.22, 1, 0.36, 1)` | entrada |
| `mola` | stiffness 380, damping 32 | gesto, marcador |

## Peças

- **`ProvedorDeMovimento`** — na raiz; `reducedMotion="user"` vale para o app inteiro.
- **`Surgir`** — bloco entra subindo 16 px e ganhando opacidade, uma vez, quando aparece. [[2026-10-02-pr-018-movimento-base]]

## Regras

- Só `transform` e `opacity` animam.
- Disparo por margem, nunca por fração (bloco alto nunca atinge 50%).
