# About `credit_spreads_illustrative.csv`

This file is **synthetic, hand-built data** -- it is not downloaded from
FRED, ICE, or any other real source. It exists so the dashboard runs and
produces sensible-looking charts before you've set up a FRED API key.

The values were built from a small number of manually chosen "anchor
points" loosely shaped like well-known credit cycle episodes (the COVID
liquidity shock in March 2020, the 2022 rate-hiking cycle, the 2024
spread compression, a stylized 2025 re-widening), with light interpolation
and random noise in between. They approximate the *shape* of real credit
cycles for teaching purposes -- **do not cite specific numbers from this
file as real historical data.**

## Getting the real data

The actual series (ICE BofA US High Yield OAS, BBB OAS, etc.) are licensed
by ICE Data Indices and distributed through FRED for personal/research use.
To use the real thing:

1. Get a free FRED API key: https://fredaccount.stlouisfed.org/apikeys
2. `export FRED_API_KEY=your_key_here`
3. `python fetch_data.py` (from the project root)

This writes `credit_spreads_live.csv`, which `dashboard.py` will
automatically prefer over this illustrative file.
