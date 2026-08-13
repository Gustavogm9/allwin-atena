# Deploy · Atena Educa — allwin.guilds.com.br

Senha do cliente: **allwin-atena-2026** (StaticCrypt · index = showcase · protótipo nos iframes com mesmo salt).

## Publicar (~2 min)
```bash
cd github_pages_deploy
git init -b main && git add -A && git commit -m "Atena Educa · deploy"
gh repo create Gustavogm9/allwin-atena --public --source=. --push
gh api repos/Gustavogm9/allwin-atena/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```
## Depois
1. Wix DNS: CNAME `allwin` → `gustavogm9.github.io`.
2. Esperar HTTPS → Enforce HTTPS. 3. `curl -sI https://allwin.guilds.com.br` = 200, só tela de senha.
4. Só mandar o link ao João depois do HTTPS.
