---
tipo: runbook
ultima_atualizacao: 2026-10-02
tags: [deploy, infra]
---

# Deploy no GitHub Pages

- **Endereço:** https://victornascimento14.github.io/Vitalbank/
- **Quando:** a cada push na `main` (workflow `Pages`), ou à mão em Actions → Pages → *Run workflow*.
- **Como:** `CAMINHO_BASE=/Vitalbank pnpm build` → `out/` + `.nojekyll` → `upload-pages-artifact` → `deploy-pages`.

## Conferir localmente

```bash
CAMINHO_BASE=/Vitalbank pnpm build
mkdir -p /tmp/pages && ln -sfn "$PWD/out" /tmp/pages/Vitalbank
cd /tmp/pages && python3 -m http.server 8811   # http://localhost:8811/Vitalbank/
```

## Se quebrar

- Página sem estilo / JS 404: faltou `.nojekyll` (Jekyll ignora `_next/`) ou o `CAMINHO_BASE` não bate com o nome do repositório.
- `/contas` dá 404: `trailingSlash` foi desligado.

Introduzido em [[2026-10-02-pr-178-deploy-pages]].
