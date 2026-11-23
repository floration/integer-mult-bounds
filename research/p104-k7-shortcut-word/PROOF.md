# Proof notes: five relay shortcuts in the Gaussian word, at K7 ordinary-binding κ 0.003898273237647

**Author: floration**, building on the upstream work credited at the end.

This package replaces #8027's 5,674-transfer rational (Gaussian) word with a 5,669-transfer word that has the same forward map. Five pairs of chart-3-only relay transfers `X: a→b`, `Y: b→c` (nested charts `a ⊂ b ⊂ c`, where Y reads X) each become one direct transfer `D: a→c`:

| X | Y | charts | grades |
|---|---|---|---|
| 95398 | 99468 | 412→798→922 | 2+3 → 5 |
| 97628 | 100531 | 614→795→917 | 2+2 → 4 |
| 95050 | 101275 | 392→1037→918 | 3+2 → 5 |
| 95056 | 95425 | 411→1038→921 | 3+2 → 5 |
| 96741 | 96743 | 365→1028→529 | 3+2 → 5 |

The chart-3 block changed by an invertible E33, so the chart-3 inputs are re-encoded with E33⁻¹. The net change is 44 changed rows (15 at chart 3) plus the 5 new moves. Total form terms fall from 323,573 to 322,917. `initial`, `final`, `frames` and `first_output` are unchanged, so the productive (target) histogram is unchanged. Per call, the paid histogram moves grade 2 38016→37728, grade 3 23040→22848, grade 4 10848→10896, and grade 5 15072→15264. The linear grade sum is unchanged, so the gain comes only from concavity. The word ships as `w5669_shortcut5.json.gz` (graph digest `ed3bea71…`), and the patched `strong_complex.load_changed` checks it against that digest and against the unchanged endpoints.

The certified two-type (5:451) transport trial rises from `17145637307/2^42` to `17158764376/2^42`. The certifier admits up to `…382`, and the installed value keeps 6 ticks. The directed Gaussian factor is booked at `1039776/2^23` (the finer point `1039775` fails). Under #8082's ordinary debit `1424116/2^20` and the unchanged #8072 clock cap 318292011, the Gaussian side no longer binds. The ordinary recurrence binds at heights `(26384,417171,524288)` with Gaussian height `G = 39002`. The conditional κ is **0.003898273237647**, which is +4.291e-8 over #8082 and +5.348e-8 over #8073. The complete recurring log₂ C is 318291931, and the entry conversion uses 452 bits. The same five all-size premises apply. [Exact signed invoice](RESULT.json)

From a clean checkout with Git and CPython 3.12, run:

```sh
python3.12 -IB scripts/research_package.py --package research/p104-k7-shortcut-word
```

The negative controls are:
- the old word's trial and booking reproduce #8082's Gaussian-binding ceiling;
- the finer Gaussian point `1039775/2^23` fails the directed factor;
- `G−1` fails Gaussian, and the profile is underfunded under #8080's ordinary debit;
- the replaced word must match the frozen digest, and its endpoints must equal #8027's.

## Open next questions

Under the 2^19 height domain, the ordinary side now binds. Lifting the native height domain to the 20-bit descriptor limit, which the setup scope already admits, raises the ordinary ceiling to about 0.0038996. That needs its own full signed invoice. Further relay shortcuts in chart 3 would raise the Gaussian side again, but they are worth nothing while the ordinary side binds.

## Credit

**Main author: floration.** This is a collaboration that builds on the upstream work credited below.

- floration's #8082 (ordinary reserve) and #8080 (floor retune), both with Claude. The relay-shortcut rewrite and its exact map check were also found by floration with Claude.
- Ali Romman's #8027 rational word, and #8042, #8055 and #8057.
- #8073 (Campaign contributor, with OpenAI Codex), SYLforge's #8052 K7 word, and #8059 to #8072.

Source licenses and notices are retained. floration did the analysis, implementation and replay, with material assistance from Claude (Anthropic).
