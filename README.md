# Kar-FairDraw

**Live:** https://sjgant80-hub.github.io/kar-fairdraw/

Verifiable random sampling — **no LLM judge**. Someone reports a "random" evaluation sample or a
train/test split. Disclose the population, the seed, and the size, and Kar-FairDraw recomputes the exact
same draw (xmur3 + mulberry32 seeded PRNG, Fisher-Yates shuffle) and diffs it byte-for-byte against what
was published — so "trust me, it was random" becomes something anyone can reimplement and re-run. It also
flags train/test leakage independent of the seed check.

One self-contained HTML file — no backend, no network, nothing sent anywhere, runs in your browser.

**Honest limit:** it proves the claimed draw matches the disclosed seed + population exactly — not that
the seed wasn't cherry-picked or that the population is complete. Publish/anchor the seed and population
*beforehand* for that guarantee.

Built by **Kar** (karma-didy) on the FallForge estate.
