---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 146
url: https://github.com/VictorNascimento14/Vitalbank/pull/146
branch: feat/configuracoes-preferencias
tags: [pr, configuracoes, formulario]
status: aberto
---

# PR #146 — feat(configuracoes): aba Preferências com moeda, fuso e avisos

## 🎯 Contexto

Configurações, item 2. Fecha a issue #145.

## 🔧 Mudanças

- `src/telas/configuracoes/Preferencias.tsx` + teste; `src/telas/configuracoes/Configuracoes.tsx`.

## 🧠 Decisões técnicas

- **`<fieldset>` + `<legend>` "Avisos"**: o leitor de tela anuncia o grupo antes de cada interruptor.
- **Confirmação some quando algo muda**: "salvo" ao lado de um formulário alterado depois mente.
- **Não persiste** (nem `localStorage`): na v1 a confirmação é demonstração, como o resto ([[ADR-001-frontend-primeiro-com-dados-mock]]).

## 🧪 Como testar

1. Captura (1440 px) e testes.

## 📎 Documentação afetada

- [[Configuracoes]]
- [[2026]] (changelog)
