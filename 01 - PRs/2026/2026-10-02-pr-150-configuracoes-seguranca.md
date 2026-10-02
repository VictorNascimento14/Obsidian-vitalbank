---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 150
url: https://github.com/VictorNascimento14/Vitalbank/pull/150
branch: feat/configuracoes-seguranca
tags: [pr, configuracoes, seguranca, animacao]
status: aberto
---

# PR #150 — feat(configuracoes): aba Segurança com duas etapas e troca de senha com medidor

## 🎯 Contexto

Configurações, item 3 — fecha a tela. Usa [[2026-10-02-pr-148-forca-da-senha]]. Fecha a issue #149.

## 🔧 Mudanças

- `src/telas/configuracoes/Seguranca.tsx` + teste; `src/telas/configuracoes/Configuracoes.tsx`.

## 🕵️ Dado sensível

As senhas vivem só no estado dos campos enquanto a pessoa digita, e são apagadas quando a troca é aceita. Nada é enviado nem guardado. `autoComplete` correto deixa o gerenciador de senhas do navegador ajudar.

## 🧠 Decisões técnicas

- **Medidor por `scaleX` com `origin-left`**: anima só `transform` (invariante 4 do `CLAUDE.md`), em vez de largura.
- **Barra mínima de 1 com qualquer texto**: com força 0, uma barra vermelha ainda mostra que o medidor está olhando.
- **Mensagens por campo** (atual, nova, confirmação), ligadas por `aria-describedby` pelo `Campo`.

## 🧪 Como testar

1. Captura com "Casaverde1" na nova senha (1440 px): duas barras âmbar, "Média".

## 📎 Documentação afetada

- [[Configuracoes]]
- [[ForcaDaSenha]]
- [[2026]] (changelog)
