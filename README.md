# reflect-web

Public web assets for the **Reflect** journaling app.

The primary site is deployed as Cloudflare Worker static assets:

- **Home:** https://reflect-site.fruhji.workers.dev/
- **Privacy Policy:** https://reflect-site.fruhji.workers.dev/privacy
- **Terms:** https://reflect-site.fruhji.workers.dev/terms
- **Support:** https://reflect-site.fruhji.workers.dev/support

The pages live in [`docs/`](docs/), and `wrangler.jsonc` defines the Cloudflare
deployment. The GitHub Pages workflow remains only to serve compatibility redirects
from old `fruhji.github.io` links to the Cloudflare site.

The app itself lives in a separate, private repository.
