---
name: browser-tools
description: "Control Google Chrome via the `browser-tools` TypeScript CLI (Chrome DevTools Protocol) for automation/testing: launch Chrome with remote debugging, open/navigate URLs, inspect console logs, capture screenshots, extract readable page content, dump cookies, evaluate JS in-page, and inspect/kill DevTools-enabled Chrome instances. Use when a user asks to reproduce a browser bug, click/select elements, read page content (e.g. prices), or report network requests to specific domains."
---

# Browser Tools

## Run the CLI

Always drive the executable:

`/Users/rolandk/Sandbox/agent-scripts/scripts/browser-tools/browser-tools.ts`

Run it from its package directory so `tsx` resolves:

`cd /Users/rolandk/Sandbox/agent-scripts/scripts/browser-tools && ./browser-tools.ts --help`

## Typical workflow

1. Start Chrome (or attach to an existing DevTools port):
   `./browser-tools.ts start`
2. Navigate:
   `./browser-tools.ts nav <url>`
3. Use subcommands as needed (console/content/cookies/eval/pick/screenshot/search/inspect/kill).

## Recipes

- Report “network requests to domain X” (best-effort): run `console` in the background, then `eval` a `performance.getEntriesByType("resource")` filter and `console.log()` the result.
- Find a “price”: use `eval` to query likely selectors and return the text; fallback to searching `document.body.innerText`.

## Reference

See `references/cli.md` (generated from `--help` output).
