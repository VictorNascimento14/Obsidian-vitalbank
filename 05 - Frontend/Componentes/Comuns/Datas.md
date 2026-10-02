---
tipo: componente
camada: dominio
arquivo: src/dominio/datas.ts
ultima_atualizacao: 2026-10-02
tags: [dominio, datas]
---

# Datas

Datas são texto `AAAA-MM-DD` (ou `AAAA-MM-DDTHH:mm`), lidas **no horário local** por `lerData`.

| Função | Exemplo |
|---|---|
| `formatarDataLonga` | "28 de janeiro de 2021" |
| `formatarDataMedia` | "28 set 2026" |
| `formatarDataCurta` | "28 jan" · "28 jan, 12:30" |
| `mesCurto` / `diaDaSemanaCurto` | "ago" · "sáb" |
| `haQuantoTempo` | "hoje" · "ontem" · "há 5 dias" |

⚠️ `new Date("2021-01-28")` lê em UTC e, no Brasil, volta para o dia 27. Nunca use.

Introduzido em [[2026-10-02-pr-014-datas]].
