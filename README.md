# Modestio Lead Scanner

Jednoduchá statická MVP aplikace pro přípravu AI auditu potenciálních klientů.

## Co aplikace umí

- formulář pro IČO, web a sociální sítě,
- pokus o načtení veřejných údajů z ARESu,
- generování AI promptu pro ChatGPT,
- checklist pro ruční audit,
- telefonní script,
- follow-up e-mail,
- lokální ukládání leadů v prohlížeči přes localStorage,
- export leadů do JSON a CSV.

## Co aplikace zatím záměrně neumí

- nemá backend,
- nemá databázi,
- nemá přímé napojení na OpenAI API,
- neukládá API klíče,
- nescrapuje sociální sítě.

To je záměr. Díky tomu může běžet zdarma na GitHub Pages.

## Nasazení na GitHub Pages

1. Vytvoř nový GitHub repozitář, například `modestio-lead-scanner`.
2. Nahraj do repozitáře soubory:
   - `index.html`
   - `.nojekyll`
   - `README.md`
3. V GitHubu otevři `Settings` → `Pages`.
4. V části `Build and deployment` nastav:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Ulož a otevři URL, kterou GitHub vygeneruje.

## Doporučený workflow

1. Zadáš firmu.
2. Klikneš na `Vygenerovat AI prompt`.
3. Zkopíruješ prompt do ChatGPT.
4. ChatGPT připraví audit.
5. V aplikaci uložíš lead a nastavíš status.

## Další možná verze

- Cloudflare Worker / Vercel Function jako bezpečný backend pro OpenAI API.
- Automatický PageSpeed audit.
- Firecrawl pro načítání obsahu webu.
- Supabase databáze.
- Přihlášení pro tým Modestia.
