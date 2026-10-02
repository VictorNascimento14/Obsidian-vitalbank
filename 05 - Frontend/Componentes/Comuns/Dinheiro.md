---
tipo: componente
camada: dominio
arquivo: src/dominio/dinheiro.ts
ultima_atualizacao: 2026-10-02
tags: [dominio, dinheiro]
---

# Dinheiro

Todo valor em dinheiro é **inteiro em centavos** (`Centavos`). Real com vírgula só na borda.

| Função | Faz |
|---|---|
| `formatarMoeda(c, { sinal?, compacto? })` | "R$ 5.756,00"; com `sinal`, entrada vira "+R$ 2.500,00"; com `compacto`, "R$ 1,2 mil" |
| `somarCentavos(lista)` | soma inteira, sem float |
| `paraCentavos(texto)` | lê "1.234,56" / "R$ 10" / "0,5"; `null` se não for valor |

Introduzido em [[2026-10-02-pr-012-dinheiro]]. Regra em [[ADR-001-frontend-primeiro-com-dados-mock]].
