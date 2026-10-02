---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 211
url: https://github.com/VictorNascimento14/Vitalbank/pull/211
branch: chore/script-de-publicacao
tags: [pr, processo, scripts]
status: merged
---

# PR #211 — chore(scripts): pipeline de publicação num comando

## 🎯 Contexto

Processo. Fecha a issue #210.

## 🔧 Mudanças

- `scripts/publicacao/{publicar.sh, ve.py, README.md}`; `CLAUDE.md`.

## 🧠 Decisões técnicas

- **Os textos continuam à mão**: o script faz a sequência, não escreve o porquê. Nota e PR gerados por máquina não explicam decisão.
- **Número do PR previsto** (issue + 1) para a nota nascer antes do PR; se não bater (o Dependabot abriu PRs no meio), o script para antes de mergear. Aconteceu de verdade quando o Dependabot abriu #201–#205.
- **Para no primeiro erro** (`set -euo pipefail`), inclusive se o CI reprovar: nada é mergeado vermelho.

## ⚠️ Armadilhas e aprendizados

- A inserção no changelog quebrou uma vez quando a seção "🐛 Corrigido" estava no fim do arquivo, sem linha em branco depois; o script passou a procurar só o cabeçalho e repor a linha em branco. E ganhou `210_EXISTENTE` para retomar sem criar issue duplicada.

## 🧪 Como testar

1. Sintaxe e este próprio PR.

## 📎 Documentação afetada

- [[DeployPages]]
- [[2026]] (changelog)
