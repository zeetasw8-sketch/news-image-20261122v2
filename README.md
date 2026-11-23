[![make.fun · news-image-20261122](https://make.fun/badge/news-image-20261122.svg)](https://make.fun/bounty/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)
[![rank](https://make.fun/badge/news-image-20261122/zeetasw8-sketch/news-image-20261122v2/rank.svg)](https://make.fun/bounty/news-image-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)
[![reward](https://make.fun/badge/news-image-20261122/zeetasw8-sketch/news-image-20261122v2/reward.svg)](https://make.fun/bounty/news-image-20261122?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261122)

# The World Today — 22 November 2026 in one image

Entry for make.fun competition `news-image-20261122` ($100).
One 1024×1024 PNG that sums up Sunday 22 November 2026's world
news — a navy broadsheet masthead, one dominant hero, four big cards,
and an "ALSO TODAY" ticker with six more stories — 11 stories in
total, all of them from Saturday 21 November's news cycle and the
full day of Sunday 22 November (this is the v2 iteration: the first
version only covered Sunday up to 05:40 UTC).

## The 11 stories

### Hero — Iran Hits Bahrain
Saturday night: Iran launches two waves of drone and ballistic
missile strikes on Bahrain. Iran claims it hit U.S. bases and
destroyed 2 Patriot radars — **unconfirmed**; U.S. officials say
there was no damage to U.S. personnel or facilities. Bahrain
confirms 2 people hurt, 1 critically. Three tankers are hit in the
Strait of Hormuz since Friday (Captain Leon, Torkel, Arina), and
CNN counts at least 22 attacks in November — the most since the
war began.
Sources: Reuters, CNN, The Defense News, 21–22 Nov 2026.

### Card 1 — COP31 Collapses, No Deal
Climate talks in Antalya end on Sunday with no deal — the first
COP cover decision to fail since Copenhagen 2009, after a record
49+ hours of overtime. The 94-paragraph draft never once mentions
fossil fuels, and a $120bn adaptation fund for poorer nations is
cut.
Sources: Reuters, Turkish Minute, 22 Nov 2026.

### Card 2 — Sparta II Towed Out as Fire Dies
The Russian cargo ship Sparta II, hit by 2 drones in the Gulf of
Finland, is towed out of Finnish waters after 7 ships from
Finland, Russia and Estonia fight the blaze together. All 16 crew
are safe; 1 is lightly hurt.
Sources: CNN, Reuters, 21–22 Nov 2026.

### Card 3 — Cikande Fire: 3 Dead, Dozens Missing
Rescuers recover 24 body bags after a candy-factory fire in
Cikande, Banten, Indonesia; the death toll is still unconfirmed
(a body bag is not a confirmed victim). The rescue agency lists
39 missing; police say nearer 50. DNA identification will take
2–3 weeks.
Sources: Reuters, AP, 22 Nov 2026.

### Card 4 — Houthis Hit Riyadh a 3rd Day
The Saudi-led coalition downs a missile over western Saudi Arabia
and a drone bound for Riyadh — a third straight day of attacks
on the capital, after 3 missiles were intercepted on Saturday.
Source: Reuters, ISW, 21–22 Nov 2026.

### Also today
- France: 82,500 march in cost-of-living protests; 144 arrested
  (Reuters, 21 Nov 2026).
- Mexico: 'El Chapo Isidro', an FBI Top-10 fugitive, captured;
  11 killed in the raid (Reuters, CNN, 21 Nov 2026).
- U.S.: FBI probes an apparent hack of its national crime database;
  Washington halts gun background checks (AP, ABC, 21–22 Nov 2026).
- Nigeria: a boat carrying funeral mourners capsizes; at least 24
  dead (Reuters, 21 Nov 2026).
- Iraq: a fire at the Basra power plant kills 4, injures about 46
  (Reuters, 21–22 Nov 2026).
- West Bank: settlers torch about a dozen Palestinian cars;
  Eisenkot calls it "Jewish terrorism" (Reuters, CNN, 22 Nov 2026).

## Render locally

```sh
cd ..
python3 render22v2.py    # writes entry-22v2/entry.png (1024x1024, < 1 MiB)
sha256sum entry-22v2/entry.png   # run twice: the hash must not change
```

Requirements: Python 3 with Pillow, DejaVu fonts
(`/usr/share/fonts/truetype/dejavu/`). The render is fully
deterministic — fixed palette, fixed fonts, no randomness, no clock —
so repeated runs produce byte-identical output. The render script
itself is not part of the entry (it lives one directory up).

## Run the entrypoint

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
sha256sum out/entry.png entry.png   # both hashes must match
```

`main.ts` needs no network: it validates the bundled PNG (magic
bytes, 1024×1024 dimensions, 1 MiB cap), copies it to
`MAKEFUN_OUTPUT_DIR` (default `/output`), reads it back and verifies
the copy is byte-identical.

## License

MIT — see `LICENSE`.
