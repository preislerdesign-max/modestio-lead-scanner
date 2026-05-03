# Modestio Lead Scanner v3.1 — OpenAI web search + dark theme

Interní akviziční aplikace pro Modestio.

## Co umí

- zadáš IČO, web nebo sociální síť,
- Worker načte ARES, pokud najde IČO,
- OpenAI web search dohledá oficiální web a sociální profily,
- pokud je dostupný web, Worker načte homepage a důležité podstránky,
- AI vyhodnotí lead score, brand, web, UX, obsah, sítě a obchodní příležitost,
- vygeneruje friendly callscript a follow-up e-mail.

## GitHub Pages

Nahraj na GitHub Pages:

- `index.html`
- `.nojekyll`
- `README.md`

## Cloudflare Worker

Do Cloudflare Workeru nahraj:

- `worker.js`

## Variables and Secrets

Povinné:

- `OPENAI_API_KEY` jako Secret

Volitelné:

- `OPENAI_MODEL` jako Text, například model, který ti aktuálně funguje
- `OPENAI_SEARCH_MODEL` jako Text, pokud chceš pro discovery použít jiný model
- `APP_ACCESS_TOKEN` jako Secret, pokud chceš jednoduché zaheslování volání z frontendu

Serper API není potřeba.
