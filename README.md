# APYX Pips & Airdrop Calculator

Community tool (not affiliated with Apyx). Paste a wallet address (Ethereum / Base / BNB — pips are tracked per address across all chains) to fetch its **Season 1** (final) and **Season 2** (live) pips from the public Apyx rewards API, then model the implied USD value of the APYX airdrop under your own assumptions (TVL at TGE, FDV/TVL ratio or direct market cap, projected final S2 pips pool).

**Live:** https://phummy1337.github.io/apyx-pips-checker/

## How it works

- Balances come from `api.apyx.fi/v1/rewards/seasons/{1|2}/users/{address}` (direct fetch, with CORS-proxy fallbacks).
- Season 1: 231.01B total pips (final, ended May 22 2026), 5% of APYX supply.
- Season 2: live until Oct 11 2026, 6% of supply. TGE Oct 13 2026. 100M APYX fixed supply.
- Implied value = your pips ÷ season total × season allocation × (FDV ÷ 100M).
- Shareable links: `/?a=0x…` auto-loads an address.

## Files

- `index.html` — the deployed page (Google Sans Flex embedded as base64; fully self-contained).
- `index_template.html` — editable source with a `__FONT_B64__` placeholder. To rebuild `index.html`, splice the base64 of the woff2 back in.

Nothing here is financial advice; allocations and season totals can change.
