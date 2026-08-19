# Shopify Dawn Custom Sections

Custom Shopify Dawn theme development for the Innova store.

## Local Development

Start the Shopify theme preview server:

```bash
shopify theme dev --store=my-cool-store-1.myshopify.com
```

Default local preview URL:

```text
http://127.0.0.1:9292
```

If port `9292` is busy, use another port:

```bash
shopify theme dev --store=my-cool-store-1.myshopify.com --port=9293
```

## Daily Workflow

Check changed files:

```bash
git status
```

See the actual code changes:

```bash
git diff
```

Preview local changes without pushing to GitHub:

```bash
shopify theme dev --store=my-cool-store-1.myshopify.com
```

## Shopify Theme Sync

Pull the latest theme files from Shopify:

```bash
shopify theme pull --store=my-cool-store-1.myshopify.com
```

Push local theme files to Shopify:

```bash
shopify theme push --store=my-cool-store-1.myshopify.com
```

Push as a new unpublished theme for safe testing:

```bash
shopify theme push --unpublished --store=my-cool-store-1.myshopify.com
```

Use `theme pull` when changes were made in the Shopify theme editor and you want them locally. Use `theme push` when local code changes should be uploaded to Shopify.

## Notes

- `shopify theme dev` creates a temporary development preview and updates as local files change.
- You do not need to push to git to preview local changes.
- Keep the terminal running while developing.
- Use `git push` only when you want to save your committed code to GitHub.
- Be careful with `shopify theme push`: it can update a Shopify theme. Use `--unpublished` when testing a larger redesign.
