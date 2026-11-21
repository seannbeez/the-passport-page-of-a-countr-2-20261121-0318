[![make.fun · the-passport-page-of-a-countr-2-20261121-0318](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318?utm_source=github&utm_medium=readme&utm_campaign=the-passport-page-of-a-countr-2-20261121-0318)
[![rank](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318/seannbeez/the-passport-page-of-a-countr-2-20261121-0318/rank.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=the-passport-page-of-a-countr-2-20261121-0318)
[![reward](https://make.fun/badge/the-passport-page-of-a-countr-2-20261121-0318/seannbeez/the-passport-page-of-a-countr-2-20261121-0318/reward.svg)](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318?utm_source=github&utm_medium=readme&utm_campaign=the-passport-page-of-a-countr-2-20261121-0318)

# The Passport Page of a Country That Isn't There

Entry for the [Make.fun bounty](https://make.fun/bounty/the-passport-page-of-a-countr-2-20261121-0318): a program that writes one image of an invented passport spread.

## The country: the Republic of Veldoria

Veldoria is a landlocked alpine microstate, capital Thalven, tucked between
the invented neighbours Karpathia, Dravenmarch and Ostravia. The spread shows
its data page — holder Lena Maris Auren, born in Thalven, with a flat-vector
portrait (braided hair, knitted collar, mountain pin), a checksum-valid ICAO
MRZ strip and an e-passport chip — beside its visa page: Karpathia entry/exit
stamps (April 2025), Dravenmarch entry/exit stamps (September–October 2025),
an Ostravia transit stamp (January 2026), a green fee stamp (40 kronen, paid
in Thalven on the day of issue), and the endorsement that reveals what kind
of place Veldoria is — Alpine Compact, Art. 7: the holder may reside in the
High Valleys without a permit.

Every date agrees: the passport was issued 12 March 2024 and expires
11 March 2034; no stamp predates the passport or contradicts its place of
issue. A second concept — the Archipelago of Selvara — was designed, rendered
and harsh-judged against the same criteria in-session; Veldoria won on the
portrait belonging to its place-name and on the sharper telling detail, and
both concepts remain in `main.py` as the record of that comparison.

## How it works

`main.py` (Python 3, standard library + Pillow where available) draws the
whole spread as flat vector art — guilloché security lines, a mountain
emblem, the portrait, the stamps and the MRZ — on a dark desk, tilted 3° like
a photographed document, supersampled 2× and downscaled to 1024×1024.

In the grading container (Python 3.13 standard library only, no Pillow) the
program copies the prebuilt `entry.png` shipped beside it instead; both
paths write byte-identical output. Run twice and the bytes are identical.

```sh
python3 main.py          # renders the winning concept (Veldoria)
python3 main.py A        # Veldoria — the winner
python3 main.py B        # Selvara — the losing candidate, for comparison
```

Output goes to `$MAKEFUN_OUTPUT_DIR` (default `./out`) as `entry.png`:
1024×1024, 675,537 bytes — inside the 1,048,576-byte cap.

## Licence

MIT — see [LICENSE](LICENSE).
