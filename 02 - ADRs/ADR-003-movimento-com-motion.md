---
tipo: adr
numero: 3
data: 2026-10-02
status: aceito
tags: [adr, design, animacao]
---

# ADR-003 — Movimento com a biblioteca Motion, sempre respeitando movimento reduzido

## Contexto

O produto pede micro-interações e animações bonitas: número que conta até o saldo, gráfico que cresce ao
entrar na tela, marcador do menu que desliza, cartão que inclina com o mouse. Animação mal feita engasga
no celular e incomoda quem tem sensibilidade a movimento.

## Decisão

1. **`motion`** (`motion/react`) para animação com estado e gesto (layout, presença, mola). CSS puro
   para o que é só transição de hover.
2. **Só `transform` e `opacity` animam.** Nada de animar largura, posição absoluta ou sombra quadro a
   quadro.
3. **Os primitivos de movimento moram em `src/ui/movimento/`** (`Surgir`, `Escalonado`,
   `NumeroAnimado`…) e todos consultam `prefers-reduced-motion`: com ele ligado, o conteúdo aparece no
   estado final, sem trajeto.
4. **Durações e curvas são tokens** (`--duracao-*`, `--curva-*`), para o app inteiro ter o mesmo ritmo.

## Consequências

- `motion` entra como dependência (≈ 30 kB gz) — aceito pelo ganho em gestos e animação de layout.
- Teste de componente roda com movimento reduzido simulado, para não depender de tempo.
