# bring-the-humans

[![make.fun · bring-the-humans-01](https://make.fun/badge/bring-the-humans-01.svg)](https://make.fun/bounty/bring-the-humans-01?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)
[![rank](https://make.fun/badge/bring-the-humans-01/adriansyahbsc/bring-the-humans/rank.svg)](https://make.fun/bounty/bring-the-humans-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)
[![reward](https://make.fun/badge/bring-the-humans-01/adriansyahbsc/bring-the-humans/reward.svg)](https://make.fun/bounty/bring-the-humans-01?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)

An ad page for [make.fun](https://make.fun/r/kj9js265?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01) — the platform where AI agents build software for real USDC bounties — carrying @adriansyahbsc's referral link. Built for the “Bring the humans” bounty: the ad that brings the most verified human signups (sign up → create an agent → enter a bounty) wins.

> ⚠️ **Badge URLs assume the GitHub repo is `adriansyahbsc/bring-the-humans`.** If the repo is created under a different name, update the `{owner}/{repo}` parts of the rank/reward badge URLs (a `repo_readme` check requires the three live badges with the real owner/repo, filled in).

## What's here

| File | What it is |
|---|---|
| `index.html` | The ad page itself (repo root, as required). Single self-contained file — inline CSS + JS, no external assets, works offline. |
| `ad.png` | A screenshot of the page (1280×1000 PNG, ~294 KB (300,628 bytes)) with the referral link visible in the top bar — required at the repo root beside `index.html`. |
| `LICENSE` | MIT (OSI-approved), with SPDX line. |

Page contents: referral link bar (always visible) → hero with dual CTAs → stats → “How it works” (sign up → create agent → enter a bounty) → live bounty cards with real amounts (Token Launch Radar $1,325 · three.js FPS $1,000 · Best Game $1,000 · Bring the Humans $1,000 · Git Forge $500 · Chess 4 KB $500) → why-join → FAQ accordion → final CTA. Mobile-friendly, copy-link button included.

## Run it

Nothing has to run — the bounty says so — but to view it:

```sh
open index.html            # just open the file in a browser
# or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

To re-render `ad.png` after editing the page (any headless browser works; this build used Puppeteer):

```sh
# with a Chrome/Chromium available:
google-chrome --headless --screenshot=ad.png --window-size=1280,1000 index.html
# make sure the top referral bar is in frame — the link must be visible in the image
```

## ✅ Referral link — real code installed

The page carries Adrian's **real** referral link:

```
https://make.fun/r/kj9js265
```

- Code: **`kj9js265`** (8 characters), in the `/r/<code>` form the bounty requirements accept (the intake `ad_page` check scans `index.html` for the code as bare code, `/r/<code>`, or `?ref=<code>`).
- **Source: Adrian himself, confirmed on 2026-11-16** — he personally provided this link. It replaced the earlier username-based placeholder (which was not a real code) everywhere: the JS constant `var REFERRAL_LINK = "https://make.fun/r/kj9js265";` at the top of the `<script>` block (all CTAs are rewired from this one constant via `data-ref`), every hardcoded `href` + visible link text in `index.html`, and the referral links in this README. `ad.png` was re-rendered afterwards so the image shows the real link.
- ⚠️ **Discrepancy note:** a *different* code, `fxmj7hva`, was seen on the Referrals tab of the cloud-browser profile session for @adriansyahbsc on 2026-11-16. That code is **not** used anywhere in this entry — Adrian's own stated link (`kj9js265`) takes precedence unless he says otherwise. Flagging it here in case the two accounts/codes need reconciling before submitting.

## Submission checklist (from the live requirements, 16 Nov 2026)

Competition: `bring-the-humans-01` · harness `referral/v1` · **entries close 2026-11-16 18:00 UTC (Tue 17 Nov, 02:00 WITA)** · rewards $1,000 USDC in escrow on Solana — **100 places: 1st $250, 2nd $100, 3rd $40, 4th–10th $10, 11th–100th $6** · **no entry fee** (`entry_fee: null`) · max 5 entries/day, 10 total.

- [x] **Referral placeholder replaced** with the real 8-char code **`kj9js265`** (link `https://make.fun/r/kj9js265`, provided by Adrian himself on 2026-11-16) + `ad.png` re-rendered
- [ ] Create the **public GitHub repo owned by `adriansyahbsc`, created after the competition opened (2026-11-14 18:00 UTC)** — a fresh repo; this local folder is only a build directory
- [ ] Root files at the submitted commit: `index.html` (≤ 2 MB — this one ≈ 22 KB), `ad.png` (PNG/JPEG/WebP ≤ 8 MB — this one ≈ 294 KB (300,628 bytes)), `LICENSE` (OSI; MIT here, with SPDX line)
- [ ] This README with the **3 live make.fun badges** (owner/repo filled in, no `{owner}` placeholders left)
- [ ] GitHub **About**: homepage `https://make.fun/bounty/bring-the-humans-01`, topics incl. `makefun` (requirements give a ready `gh repo edit …` line; recommended topics `ai-agents,bounties,growth` and a description naming make.fun)
- [ ] **Wallet (blocker for Adrian):** the account must have a Solana wallet — the entry message is Ed25519-signed by a wallet on the account and that wallet is the payout wallet (`account_wallet` / `entry_signature` checks). Profile currently shows *“No wallet linked”* → link/add a wallet first. **Do not sign anything until Adrian approves it.**
- [ ] Transcripts: bundle the agent sessions that built the page with the kit CLI (`node cli/makefun.mjs bundle`, run from inside the unpacked kit `https://make.fun/c/bring-the-humans-01/kit`), incl. run record; `handed_over_places: none` means handed-over sessions are ranked but take **no paid place** — use a harness with recorded sessions
- [ ] Submit via kit CLI (`node cli/makefun.mjs submit --competition bring-the-humans-01 --repo-url <url> --commit <full 40-char sha> --bundle <bundle> --keypair <file>`) — entry message must be signed within 10 minutes of submitting
- [ ] After entry is in: actually share the page/link — the ranking is by **verified human signups through the link**, not by page quality alone

## Requirements found vs assumed

**Found (real, from `GET /api/competitions/bring-the-humans-01/requirements` + the bounty page, fetched 16 Nov 2026 ~18:36 WITA):** `index.html` at repo root (no `main.ts` — the parent brief's generic assumption was wrong for this bounty), `ad.png` at root with the link visible, referral code = the account's 8 characters as bare code / `/r/<code>` / `?ref=<code>`, page ≤ 2 MB, image ≤ 8 MB, repo public + owner = account's GitHub login + created after 2026-11-14 18:00 UTC, OSI LICENSE, README badges + GitHub About checks, transcript bundle required, wallet-signed entry message (v1), no entry fee, deadlines and payout curve as above. “The ad need not be deployed and nothing has to run.”

**Assumed:** the GitHub repo name `bring-the-humans` used in the badge URLs. The referral link is no longer an assumption: the real code `kj9js265` (link `https://make.fun/r/kj9js265`) was provided by Adrian himself on 2026-11-16 and is installed throughout (see the referral section above for the `fxmj7hva` discrepancy note).

---

Entered on [make.fun](https://make.fun/r/kj9js265?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01) · AI agents build software for cash rewards
