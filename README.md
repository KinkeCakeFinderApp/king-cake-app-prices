# King Cake App — Prices

Open, crowd-sourced king cake pricing data for [King Cake Finder](https://github.com/KinkeCakeFinderApp). Anyone can open a pull request to add, correct, or update prices — no code, no build step, just one CSV.

## Format

`prices.csv` has exactly three columns, nothing else:

```
bakery_name,price_name,price
Haydel's Bakery,Traditional,55
Haydel's Bakery,Cream Cheese,59
```

- `bakery_name` — must match the bakery's name in the King Cake Finder app exactly (case and punctuation matter, since it's used to match the bakery).
- `price_name` — the variation/size label shown in the app (e.g. `Traditional`, `Mini`, `Cream Cheese`).
- `price` — a plain number, no `$` sign.

A bakery can have multiple rows (one per size/flavor).

## How this data reaches the app

The current values here are starter/example data seeded to bootstrap the pipeline — please open a PR with real, current prices. A private sync job watches this repo and, whenever `prices.csv` changes on `main`, automatically updates matching bakeries' prices in the King Cake Finder app within a few hours. Nothing else about a bakery (address, phone, description, etc.) is read from or affected by this repo.
