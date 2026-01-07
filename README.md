# ProfileBot

ProfileBot is a small Next.js app that introduces an AI assistant for summarizing people or companies from LinkedIn or website URLs. The landing page highlights the value props and links to an embedded chatbot page powered by Relevance AI.

## Quick start

```bash
npm install
npm run dev
# open http://localhost:3000
```

## Project layout

- `src/app/page.tsx` – landing page with hero, feature cards, contact footer, and CTA to the bot.
- `src/app/bot/page.tsx` – embeds the Relevance AI chat experience in an iframe plus a back-to-home link.
- `src/app/layout.tsx` – global layout, font setup (Geist), metadata, and body wrapper.
- `src/app/globals.css` – global styles and CSS variables, imports Tailwind base via `@import "tailwindcss";`.
- `public/images/image1.png` – hero illustration used on the landing page.
- `next.config.ts`, `tsconfig.json`, `eslint.config.mjs`, `postcss.config.mjs` – framework, TypeScript, linting, and PostCSS/Tailwind configuration.
- `package.json` / `package-lock.json` – dependencies and scripts (`dev`, `build`, `start`, `lint`).

## Usage

- Home (`/`): read about the product and click **Try our bot** to continue.
- Bot (`/bot`): paste a LinkedIn or website URL into the embedded chatbot to generate a summary. The iframe styling lives inline in `src/app/bot/page.tsx`.

## Deployment

Standard Next.js deployment (Vercel works out of the box). Ensure environment variables for the embedded bot (if needed later) are configured in the hosting platform; none are required for the current static embed.
