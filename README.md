# Modestio Lead Scanner v2

Minimalistická AI aplikace pro rychlé vyhodnocení B2B leadů pro Modestio.

## Co umí

- Vložíš IČO, web nebo sociální sítě.
- Klikneš na **Scanovat lead**.
- Aplikace zavolá Cloudflare Worker.
- Worker bezpečně použije OpenAI API klíč.
- AI vrátí lead score, doporučenou službu, slabá místa, friendly callscript a follow-up e-mail.

## Soubory

- `index.html` — frontend pro GitHub Pages
- `worker.js` — Cloudflare Worker backend
- `.nojekyll` — vypnutí Jekyll buildu na GitHub Pages

## Nasazení frontendu na GitHub Pages

Nahraj do repozitáře:

- `index.html`
- `README.md`
- `.nojekyll`

GitHub Pages nastav na:

- Source: Deploy from a branch
- Branch: main
- Folder: /root

## Nasazení AI backendu přes Cloudflare Worker

1. Otevři Cloudflare dashboard.
2. Workers & Pages → Create application → Create Worker.
3. Vlož obsah souboru `worker.js`.
4. Deploy.
5. Ve Workeru nastav secrets:
   - `OPENAI_API_KEY` = tvůj OpenAI API klíč
   - volitelně `OPENAI_MODEL` = například `gpt-5.4`
   - volitelně `APP_ACCESS_TOKEN` = jednoduchý token pro omezení přístupu
6. Zkopíruj Worker URL.
7. V aplikaci otevři **Nastavení AI** a vlož Worker URL.

## Poznámka k bezpečnosti

OpenAI API klíč nikdy nevkládej do `index.html` ani do GitHub repozitáře. Patří pouze do Cloudflare Worker secrets.
