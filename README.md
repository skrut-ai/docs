# Skrut AI Docs

Mintlify-based documentation. Deploys to [docs.skrut.ai](https://docs.skrut.ai).

## Local preview

```bash
npm i -g mintlify
mintlify dev
```

## Deploying to docs.skrut.ai

1. **Push this folder to GitHub** — create a repo (e.g. `skrut-ai/docs`) and push the contents of this `docs/` directory as the repo root.

2. **Connect to Mintlify** — sign up at [mintlify.com](https://mintlify.com), click **New project**, and connect your GitHub repo. Mintlify picks up `mint.json` automatically.

3. **Add the custom domain** — in the Mintlify dashboard go to **Settings → Custom Domain** and enter `docs.skrut.ai`.

4. **Add a CNAME in your DNS** — Mintlify will show you the exact target (e.g. `[your-subdomain].mintlify.app`). Create a CNAME record:
   ```
   docs  CNAME  [target shown in Mintlify dashboard]
   ```

5. Done — Mintlify redeploys automatically on every push to the connected branch.

## Structure

```
mint.json               ← main config (colors, nav, socials)
quickstart.mdx          ← Getting started guide
concepts/
  agents.mdx
  tests.mdx
  reports.mdx
  certification.mdx
  red-team.mdx
```
