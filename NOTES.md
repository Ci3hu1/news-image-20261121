# NOTES — news-image-20261121

## Top-10 study (live leaderboard, 22 Nov 2026 ~09:05 WIB)

Field: 12,445 ranked. Leaders use 33–36 dated stories, 7 regions,
one front page:

1. samatch-we — "35 dated stories, 7 regions — COP31 overtime, Saudi missiles, Peru quake"
2. kakek-zeus — "Certain Mirror"
3. asell — "The World's News in One Picture (Round 2)"
4. sipa — "33 stories, one front page"
5. madsrepo — "the day in world news"
6. lexyy — "The World's News in One Picture"
7. kuda — "The World in One Day"
8. myhanni — "36 stories, 7 regions, 13 illustrated cards, one front page"
9. ryanp1632-netizen — "35 dated stories, 7 regions — Riyadh missiles, Peru M6.7, COP31 deadlock, Iran drones"
10. guy-sensei — "36 stories, 6 regions: Riyadh intercepts, COP31 overtime, BepiColombo at Mercury"

Pattern: dated Saturday 21 November 2026, story count in the title,
7 regions, illustrated cards, one front page. All leaders hide source
— learned from titles/metadata only, never invented their methods.
Scores cluster 980,686–986,947; our NI20 v2 live score is 980,122.

**What the build took from the study:** 36 stories (not 50);
heroes = the leaders' heroes (COP31 overtime, Riyadh intercepts,
Peru quake); BepiColombo as a featured small story (leaders' #10
names it); date in the masthead; confidence marks on every featured
story; UTC timeline; world map with numbered pins; DATE CHECK.

## Sources (all stories Saturday 21 November 2026)

- Heroes: AP + Reuters (COP31 overtime, Antalya; draft has no fossil
  fuels, $120bn adaptation target dropped, EU "good deal or no deal");
  Reuters (Saudi coalition intercepts 3 Houthi ballistic missiles
  toward Riyadh early Sat, 2nd attack on the capital in days, after
  the PIF tower strike Thu); USGS + AP/AFP (Peru M6.7, 00:09 GMT Sat,
  34 km N of Junin / 9 km NE of Carhuamayo, 108 km deep, felt in Lima,
  no casualties or damage).
- Small: ESA + Nature (BepiColombo orbit insertion 18:24 UTC Sat,
  8-year journey, MPO/Mio separate 9–10 Dec, science Apr 2027);
  Reuters (Israeli strike kills 3 in WCK aid vehicle, Gaza City);
  AP (Kryvyi Rih ballistic attack, 2 killed, ~60 wounded; 'El Chapo
  Isidro' captured in Sinaloa, 11 dead; Nigeria funeral boat capsizes
  in Bayelsa, 24+ dead; FBI probing NCIC database hack); Reuters
  (Hartha power station fire, Basra, 4 killed, 30+ hurt); PTI (BNP vs
  Awami League clashes, 90 BGB platoons deployed); ABC (Australia
  and China agree AI talks after APEC).
- ALSO ON 14–36: AP/Reuters/Nexus Europa/Horizon/AAP/Yonhap
  reporting of 21 Nov 2026 (see poster footer for the outlet list).
  Story 31 is a Houthi CLAIM, marked as such on the poster.

## DATE CHECK exclusions (verified 22 Nov ~09:15 WIB)

Thu 19 Nov: Shenzhen summit (Trump-Xi-Putin), ICJ Myanmar genocide
verdict, Cairncross fired as US cyber chief, Pentagon China nuclear
report. Fri 20 Nov: Poland missile incursion, AI sell-off (Nasdaq
-5.3%, S&P -3.7%), Siantar Ekspres train-minibus crash, Israel's
~100-site Lebanon strikes. Not yet: COP31 final deal (still in
overtime Sat night), BepiColombo science phase (Apr 2027).

## Build log

- Fresh kit downloaded 22 Nov ~09:05 WIB (news-image-20261121-kit).
- Rendered with render_poster.py (Pillow 10.2.0 + editorial-
  illustration lib). Two view rounds (full size + 300 px); one fix
  round applied (ALSO ON column overlaps measured and shortened;
  Riyadh label moved to a red chip; quake scene label removed;
  map continent labels turned off).
- main.py is pure stdlib (copies bundled entry.png). Tests: 3/3 pass,
  including a run as uid 65534 on a read-only copy (byte-identical).
- Final render: entry.png 1024x1024, 477,099 bytes,
  sha256 7a7d18ebe4048717a4ba4ac956d856769fb2e4917644547fa1e1710506f54cfc.

## Submission

- SUBMITTED 22 Nov ~09:38 WIB on Joni's "Setuju semua": submission `01a2011e-6e5f-7387-83ec-55c2bf830535`, commit `cac69d92506e8dce56f3fe0cbc72b5fe9d4d0986`.
- Kit check before submit: `ok: true`, `failed: []` (21 sessions, 1302 messages; thinking_reproduces 92.1% authored).
- Status after submit: "checked" — passed every validity check, grading on the dev phase under way.
- Entries close 23 Nov 2026 07:00 WIB; results 7 Dec 2026 08:00 WIB.
- Claim code: stored only in `~/.config/makefun/news-image-20261121-submission.json` (0600), never in the repo.
