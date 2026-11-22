# STRATEGY — news-image-20261121: DAY EDITION

## The gap

Our NI20 v2 (NIGHT EDITION) sits at a live score of **980,122**,
rank 1,421 of ~14,800; the paid line (#50) is ~989,000 and #10 is
~991,000. The v2 closed most of the v1 gap (957,712) with real drawn
scenes, a giant-date masthead, a numbers strip, a timeline, a date
check and confidence marks — but the field's top 10 still runs a
tighter, better-curated 33–38 stories, and our 50-story list crowded
the ALSO ON block. The judge's own rubric: "Detail for its own sake
does not count."

## What the winners do (top-10 study, 22 Nov ~09:05 WIB)

The NI21 top 10 all run **33–36 dated stories, 7 regions, one front
page** (e.g. #1 samatch-we "35 dated stories, 7 regions — COP31
overtime, Saudi missiles, Peru quake"; #8 myhanni "36 stories,
7 regions, 13 illustrated cards, one front page"). All hide source;
the study used visible titles, scores and the leaders' hero stories
only. Scores cluster tight: #1 ~986,947, #10 ~980,686. Our NI20 v2
live score (980,122) already sits just under that band — a cleaner,
better-curated page is a realistic step into it.

## Our recipe — same scored elements, different poster

**DAY EDITION.** A cream front page whose masthead is a giant navy
serif date on cream ("SATURDAY 21 NOVEMBER 2026"), red kicker above,
red rule below. No dark band — the previous day's entry was a navy
NIGHT EDITION, so this one reads differently at thumbnail size while
the body stays in the legible newspaper palette the judge rewards.

**Curation over count.** 36 stories, not 50: 3 heroes + 10 small +
23 ALSO ON. Every story verified as Saturday 21 November 2026
(happened or first reported that day, any time zone) by reading the
original reporting: COP31 overtime in Antalya (AP/Reuters), three
Houthi missiles down over Riyadh (Reuters), Peru M6.7 at 00:09 GMT
(USGS/AP), BepiColombo's Mercury orbit insertion at 18:24 UTC
(ESA/Nature), and 32 more across all 7 regions (Europe 9, Middle
East 6, Asia 3, Africa 2, Americas 10, Oceania 2, Global 4).

**Confidence as the signature system.** Every featured story carries
three dots (filled = sureness) plus a HOW SURE ARE WE legend
(CONFIRMED = 2+ outlets, OFFICIAL = on the record, REPORTED = one
outlet). One-sided claims are marked CLAIM with the claimant
(story 31: Houthis claim 71 Saudi airstrikes killed civilians).

**Real drawn scenes, not text.** Three heroes use the
editorial-illustration library: a COP31 thermometer past 1.5C, a
Riyadh missile map over a night skyline, a Peru quake ridge with a
red seismograph zigzag. Ten small stories each get one motif
(Mercury moon + orbit, aid crowd, missile map, NATO flags, court,
ship, burning skyline, hacked terminal, protest crowd, AU-CN flags).

**Date discipline.** The DATE CHECK box lists 8 near-misses with
their true dates (Shenzhen summit, ICJ Myanmar verdict, Cairncross
firing, Pentagon China report — all Thu 19 Nov; Poland missile
incursion, AI sell-off, Siantar train crash, Israel's Lebanon
strikes — all Fri 20 Nov) plus two not-yet items (COP31 final deal,
BepiColombo science phase Apr 2027).

## What we deliberately did NOT copy

- No navy masthead band (that was NI20 v2's look).
- No copying of any winner's story text, layout, or image.
- No Friday 20 Nov stories (Poland missiles, AI sell-off, Siantar
  crash, Cairncross firing) — all excluded to DATE CHECK instead.
- No unverified recap-only claims except story 31, marked CLAIM.

## Build

`render_poster.py` renders `entry.png` at build time (Pillow +
editorial-illustration lib, page drawn at 2x and LANCZOS-downscaled).
`main.py` is pure stdlib: it copies the bundled `entry.png`
byte-for-byte to `$MAKEFUN_OUTPUT_DIR/entry.png`, then
`/output/entry.png`, then `output.png`. Tests run the program in a
temp dir and as uid 65534 on a read-only copy; output must be
byte-identical to the local render.
