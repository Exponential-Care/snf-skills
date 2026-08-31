# site/ — mcp.magicare.ai

The landing page for the Magicare MCP server and this skills marketplace, in
the story.magicare.ai visual language (same palette and fonts, vendored
three.js). The hero is a miniature world: a nursing home at the center with
data pulses arcing to hospitals, a payer tower, and neighborhoods of patient
homes.

No build step, no dependencies — plain `index.html` plus vendored three.js
(`vendor/three/`, the same files story.magicare.ai serves).

## Deploy (one-time Vercel setup)

1. Vercel → Add New Project → import this repo.
2. Root Directory: `site`. Framework preset: **Other**. Leave build command
   and output directory **empty** (static).
3. Add the domain `mcp.magicare.ai` to the project.

After that, every push to `main` deploys the site.

## Local preview

```bash
cd site && python3 -m http.server 4321
# open http://localhost:4321
```

## Editing notes

- Design tokens (colors/fonts) are copied from story.magicare.ai — keep them
  in sync if the brand evolves.
- The MCP endpoint shown is `https://app.exponentialcare.ai/api/mcp/org`;
  update the page if the endpoint or tool list changes.
- The skills install commands point at this repo's marketplace
  (`/plugin marketplace add magicare-ai/snf-skills`) — keep them in sync
  with the pack list in the repo root README.
