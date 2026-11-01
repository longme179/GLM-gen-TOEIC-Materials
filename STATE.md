# STATE — course build progress

> Machine-maintained (scripts/deliver.py rewrites this file from build/state.json).
> The repo is the durable memory: a fresh session clones/pulls, reads this file plus
> manifest.json, and resumes at the next unit. Never force-push or rewrite history.

- **Phase:** P3 daily plan
- **Last completed unit:** p3-day-20
- **Next unit:** p3-day-21
- **Last update:** 2026-11-01 21:26 UTC

Phases: P1 orientation → P2 reference → P3 daily plan (30 days) → P4 practice (drills + 3 full tests) → P5 expansion.

## Open issues
- none

## Shortfalls
- none

## Decision log (decide, log, continue)
- **D1 — Bilingual convention:** English is the primary language of every handout; each explanatory block is followed by a Vietnamese version on a '*VI:' line. Test questions, passages, and listening scripts stay English-only (test-authentic input); every answer explanation carries one English line plus one Vietnamese line.
- **D2 — Part 1 scene cards:** Part 1 (Photographs) uses text 'scene cards' instead of images. A text-only repo cannot ship reliable photos, and generated images risk misleading details in a task that hinges on precise visual detail. Scene cards train the same paraphrase/vocabulary discrimination; the limitation is stated in every Part 1 file.
- **D3 — Scripts, not audio:** No audio files shipped. Local TTS exists (espeak) but its robotic voice is unsuitable for natural-speech listening training, and generating ~3x100 listening items of SDK TTS exceeded this run's budget. Full scripts are shipped with a read-aloud / TTS-app / partner administration protocol. Audio could be generated in a future session from the script files.
- **D4 — Full-test days vs daily budget:** Days 10/20/27 are full-test days: the 200-question test takes about 2 hours, exceeding the 45-90 minute daily budget, so those days offer a split option (Listening today, Reading the next morning). All other days stay within 45-90 minutes.
- **D5 — Bands are course labels:** Bands B1-B5 (10-250 / 255-495 / 500-695 / 700-845 / 850-990) are course-internal routing labels, not ETS categories. No raw-to-scaled conversion tables are published anywhere (they vary by test form); all band estimates from practice material are labelled rough internal estimates.
- **D6 — PDF attachments:** Discord attachments are PDFs (pandoc + weasyprint, verified to render Vietnamese diacritics with embedded DejaVu fonts). The .md files are always the canonical committed source in the repo.
- **D7 — What gets posted:** README.md and FORMAT.md are posted to Discord as learner-facing units; STATE.md and manifest.json are build bookkeeping, committed but not posted.
- **D8 — Originals mirror verified format:** Part 3 uses 2- and 3-speaker conversations; Part 7 uses 10 single passages (29 Q) + 5 linked multi-passage sets (25 Q). Exact mixes vary on real forms; recorded in FORMAT.md as a course choice, not an ETS guarantee.

## Session notes
- Preflight 2026-11-02: git ls-remote OK with GIT_ASKPASS helper (repo was empty -> initialized main).
- Preflight 2026-11-02: Discord webhook test 'preflight ok' posted, message id 1566545661690904627.
- Preflight 2026-11-02: pandoc 3.1.11.1 + weasyprint + tectonic present; PDF pipeline verified with Vietnamese sample (DejaVu embedded). requests available. espeak/espeak-ng present (see D3). Web search available.
- Format verification 2026-11-02: part-level counts and timings from IIBC official page (see FORMAT.md sources); ETS corporate page confirmed 2x100 sections via search retrieval.
