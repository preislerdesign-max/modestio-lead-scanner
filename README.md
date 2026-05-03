# Modestio Lead Scanner Pro v3

Minimalistická interní aplikace pro Modestio. Vložíš IČO, web nebo sociální síť a aplikace přes Cloudflare Worker + OpenAI API připraví lead score, slabá místa, doporučené služby a friendly callscript.

## Co je nové ve v3

- jeden jednoduchý vstup,
- ARES lookup podle IČO,
- crawl homepage a několika důležitých podstránek,
- automatické nalezení sociálních odkazů přímo z webu,
- volitelné veřejné dohledání webu a sociálních sítí přes Serper API,
- detailnější audit brandu, webu, UX, obsahu, sociálních sítí a důvěryhodnosti,
- podrobné priority pro coldcall.

## Soubory

- `index.html` nahraj na GitHub Pages,
- `worker.js` vlož do Cloudflare Workeru,
- `.nojekyll` je volitelný soubor pro GitHub Pages.

## Cloudflare proměnné

Povinné:

- `OPENAI_API_KEY` jako Secret

Volitelné:

- `OPENAI_MODEL` jako Text, např. `gpt-5.4-mini`
- `SERPER_API_KEY` jako Secret pro dohledávání webu a sociálních sítí, když zadáš jen IČO
- `APP_ACCESS_TOKEN` jako Secret, pokud chceš jednoduchou ochranu Workeru

## Poznámka

Bez `SERPER_API_KEY` aplikace neumí spolehlivě najít oficiální web pouze podle IČO, protože ARES typicky nevrací webové stránky firem. Umí ale načíst ARES data, analyzovat zadaný web a vytáhnout sociální sítě, které jsou na webu odkazované.


## Theme

Tato verze používá dark theme v černo-červené barevnosti s bílým textem.
