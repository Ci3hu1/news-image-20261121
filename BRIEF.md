# BRIEF — news-image-20261121 (agent #3 build)

**Competition:** news-image-20261121 — "Sum up 21 November's world news in one image". $100 total, free entry. **Closes 23 Nov 2026 07:00 WIB** (2026-11-23T00:00:00Z). Harness program/v1, bundle-type (transcript bundle via kit CLI, no `record`).

**Repo:** https://github.com/Ci3hu1/news-image-20261121 (public, created after opening; About homepage + topics makefun/ai-agents/bounties already set).

**Kit (fresh):** `~/workspace/tools/makefun/news-image-20261121-kit/` — CLI at `cli/makefun.mjs`. Read the kit's skill.md for entrypoint/output rules. Do NOT read the kit's rulebook, starter program, or starter agent guide. Do NOT run `init` or copy any starter files. Write the entry program fresh from scratch — it must NOT be byte-for-byte the kit starter.

## Top-10 study (live board, 22 Nov ~09:05 WIB — Joni's rule, done)

Field: 12,445 ranked. Leaders use **33–36 dated stories, 7 regions, one front page**:
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

Pattern: dated Saturday 21 November 2026, story count in the title, 7 regions, illustrated cards, one front page. All leaders hide source — learn from titles/metadata only, never invent their methods.

## Recipe

Follow `~/workspace/custom-skills/news-image-bounty/SKILL.md` (front-page recipe). Key points:
- **Curation over count:** 33–40 verified stories from Saturday 21 Nov 2026 only (NOT 50 — #1 NI19 won with 33; the judge wrote "Detail for its own sake does not count"). Never below 43 was the old rule; the new evidence says 33–40 well-curated beats 50 crowded. Pick 3 hero stories from the day's 3 biggest (COP31 overtime, Saudi/Riyadh missile intercepts, Peru quake are the leaders' heroes).
- 6–7 regions, every region in the 13 featured stories. UTC timeline strip (6 slots). DATE CHECK box (2–4 stories deliberately excluded + their true dates, 1–2 things that had not happened yet). World map "WHERE IT HAPPENED" with numbered pins 1–13. Numbered list 14–N in 2 columns. Source line: 7–9 outlets (Reuters, AP, AFP, BBC, Al Jazeera, WHO, UN + relevant) + "Original drawings".
- Mark one-sided claims CLAIM + claimant; independently confirmed = CONFIRMED + wire. Verify every story's date and facts by reading the original news page (browser search + open the article), never from snippets alone.
- Flat vector illustrations only, never photo style. Cream/paper background, serif masthead (DejaVu/Liberation Serif), red + dark navy accents. **Never a pixel/blocky font for the masthead.** Clear type hierarchy; masthead + 3 leads must read at 300px wide — test the render at 300px before finishing.
- Each featured story gets a real drawn scene (people, buildings, map, chart), not a plain coloured rectangle. See `~/workspace/custom-skills/editorial-illustration/SKILL.md` for the procedural drawing library.
- Title format: "Saturday 21 November 2026: [N] sourced stories, 7 regions, [differentiator]" — with the true count.

## Technical (proven v3c pattern)

- Python stdlib ONLY (grader runs vanilla Python; no Pillow/numpy). Program writes output to `$MAKEFUN_OUTPUT_DIR/entry.png`, then `/output/entry.png`, then `output.png` — first that works.
- Bundle the rendered image in the repo; the program copies the bundled image when Pillow/fonts are unavailable.
- Test as uid 65534 with a read-only repo copy, exactly like the grader; output must be byte-identical to the local render.
- Reference: our NI20 v2 repo `Ci3hu1/news-image-20261120-v2` (live 980,122, rank 1,421) and NI19/NI18 v3c repos for the working pattern.
- README: 3 live make.fun badges (bounty, rank, reward) naming THIS repo + bounty link, from the first build. Run kit `check` until zero failures.
- Study file: `~/workspace/tools/makefun/icantcodefyi-study.md` (his news-image method: 46–52 stories — note the new top-10 evidence says fewer, better-curated stories win now).

## Rules

- Do NOT submit, post, or claim anything. Joni approves the exact entry before any submit.
- Report back: repo commit, kit check result, rendered poster path, exact title, story count + regions, and what the top-10 study taught the build.
