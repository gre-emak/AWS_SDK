# Stateful Registry
## Documentation built with following stack
https://vitepress-canary.netlify.app/
## Deployment using Caddy + Astro SSG pipeline
```caddy
rewrite * /registry{path}
try_files {path} {path}/manifest.html {path}.html {path}/manifest/index.html
```
## Writing documentation
* Create docs under `registry/manifests` directory, document format `mdx`, supports `jsx-component` syntax.
* Using Markdown: https://vitepress-canary.netlify.app/docs/markdown-extensions
* Using MDX: https://vitepress-canary.netlify.app/docs/component-integration
* Official reference: https://astro-mdx.vercel.io/guides/
## Publishing to https://registry.stateful-core.dev
* Push semantic tags to trigger GitLab CI pipeline for automatic deployment to https://registry.stateful-core.dev
