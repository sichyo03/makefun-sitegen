# makefun-sitegen

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/sichyo03/makefun-sitegen/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/sichyo03/makefun-sitegen/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A fast drop-in for makefun-site 1.0.0: a static site generator whose `run(input)` returns exactly
what makefun-site 1.0.0 returns, byte for byte, for every site input — but faster.

`solve.js` is a dependency-free ES module. It re-implements makefun-site's pipeline (front matter,
Markdown subset, template dialect, slugs, permalinks, collections, tags, layouts and the build
report) with faster primitives: batched plain-text escaping in inline Markdown, an ASCII fast path
with a per-case cache for slugs, a scanner word counter, direct (token-free) block rendering, and
array-joined template output with memoised case-static templates.

`main.ts` is the driver the harness runs: it reads every case from `/input/cases.json`, answers each
with `run`, and writes `/output/answers.json`.

## Run it

```sh
node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=p3gwn12d&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
