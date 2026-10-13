# beheydt-dev.github.io

Website of **Beheydt.DEV**, served at [beheydt.dev](https://beheydt.dev) through GitHub Pages.

For now it is a single "under construction" page, in French or English depending on the visitor's browser language.

## Structure

- `index.html`: the whole page (inline CSS and JS). Language is picked from `?lang=fr|en`, then the visitor's saved choice, then the browser languages, falling back to English.
- `CNAME`: custom domain (`beheydt.dev`).
- `assets/`: favicons, Open Graph image and self-hosted JetBrains Mono (SIL OFL 1.1, see `assets/fonts/OFL.txt`). The page makes no third-party requests.

Favicons and the Open Graph image are generated from the logos in [Beheydt-DEV/.github](https://github.com/Beheydt-DEV/.github/tree/main/logos).

## Local preview

```sh
python3 -m http.server 8000
# http://localhost:8000/?lang=fr  ·  http://localhost:8000/?lang=en
```

## Custom domain

DNS records for `beheydt.dev`:

| Type  | Name  | Value                                                                                    |
| ----- | ----- | ---------------------------------------------------------------------------------------- |
| A     | `@`   | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`                |
| AAAA  | `@`   | `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153` |
| CNAME | `www` | `beheydt-dev.github.io`                                                                   |

Then in the repository settings, under **Pages**, check that the custom domain is `beheydt.dev` and enable **Enforce HTTPS** (`.dev` domains are HTTPS-only).
