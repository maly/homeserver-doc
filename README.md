# Jak jsem dělal domácí server — Jekyll (Minimal Mistakes)

## Použití
1. `bundle install`
2. Lokálně: `bundle exec jekyll serve`
3. Git: push do `main` v GitHub repozitáři
4. GitHub Pages: povolit Pages (Source: GitHub Actions) — workflow níže vše zařídí.

## Struktura
- `_homeserver/` — kapitoly série (kolekce), řazení přes `order:`
- `index.md` — přehled kapitol
- `_config.yml` — nastavení tématu a kolekce
