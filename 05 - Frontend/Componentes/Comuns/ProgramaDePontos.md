---
tipo: componente
camada: dominio
arquivo: src/dominio/niveis.ts
ultima_atualizacao: 2026-10-02
tags: [dominio, privilegios]
---

# Programa de pontos

| Nível | A partir de |
|---|---|
| Prata | 0 |
| Ouro | 10.000 |
| Diamante | 15.000 |

- `situacaoNoPrograma(niveis, pontos)` → atual, próximo, faltam, progresso (dentro do nível).
- `beneficioLiberado(niveis, nivelDoBeneficio, atual)` → vale do próprio nível para baixo.

Introduzido em [[2026-10-02-pr-152-programa-de-pontos]].
