---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 188
url: https://github.com/VictorNascimento14/Vitalbank/pull/188
branch: feat/valores-sensiveis
tags: [pr, privacidade, design]
status: merged
---

# PR #188 — feat(privacidade): marcar saldos e valores para poderem ser ocultados

## 🎯 Contexto

Robustez, item 3 (parte 1). Fecha a issue #187.

## 🔧 Mudanças

- `src/app/globals.css`; 13 componentes recebem `valor-sensivel` (ver o diff); teste no `CartaoDeCredito`.

## 🕵️ Dado sensível

É proteção contra quem olha a tela, não segredo: o valor continua no DOM e o leitor de tela continua lendo — quem usa leitor de tela precisa ouvir o saldo.

## 🧠 Decisões técnicas

- **Uma classe + um atributo no `<html>`**, não estado React: ligar e desligar não re-renderiza nada, e a transição é só CSS.
- **`filter: blur`** em vez de trocar o texto por "••••": o tamanho do texto não muda, então nada pula de lugar ao ocultar.
- **Eixos dos gráficos também**: o formato das barras sem o eixo não revela valor; o eixo, sim.

## 🧪 Como testar

1. Captura com `data-ocultar` (1440 px).

## 📎 Documentação afetada

- [[OcultarValores]]
- [[2026]] (changelog)
