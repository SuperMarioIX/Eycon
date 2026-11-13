# Eycon website

Static website, no build step or dependencies required. huita

## GitHub + Cloudflare Workers

1. Extract this ZIP and commit its contents (not the ZIP itself) to the root of a GitHub repository.
2. Cloudflare Dashboard > Workers & Pages > Create application > Connect GitHub. Select the repository.
3. Worker name: eycon-website (must match wrangler.jsonc). Production branch: main (or your default branch). Root directory: repository root. Build command: leave blank. Deploy command: `npx wrangler deploy`.
4. Deploy, test the workers.dev URL, then add eycon.dev as a Custom Domain in the Worker's Settings > Domains & Routes. If a conflicting Namecheap parking DNS record exists at eycon.dev, remove that specific record before attaching the domain. Preserve unrelated MX/TXT records.

## Local preview
Open public/index.html directly, or run `npx wrangler dev` if Node.js is installed.

## Before commercial launch
The demo uses sample data and deterministic responses, not a live AI API. No information is sent to a backend. Configure a verified contact address or form before using this as a customer acquisition website.
