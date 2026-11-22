# HANDOFF — SchwarzerblitzEngine

**Last updated: 2026-11-22 (America/New_York).**
**Repo:** `mhvnsnt/SchwarzerblitzEngine` (PUBLIC), default branch `master` (NOT main).
**Purpose of this file:** any agent that picks up work here reads this FIRST, then the linked docs. It states what we've done, where we're at, and what we're working toward — so the owner can say "go to this repo, pick up the work" and you just know. Update this file in the same PR whenever the state changes (add, don't delete).

## 1. What this repo is

Schwarzerblitz — a free (as in beer) 3D fighting game engine, built by Andrea "Jens" Demetrio between 2016 and 2020 as a hobby project while pursuing a Ph.D. in physics. It is the owner's working copy of the engine source. At ~71.7 MB it holds the full engine: `schwarzerblitz_engine/`, `irrlicht/`, `SFML-2.3.2/`, `license/`, docs.

It is a framework/engine repo, like NightSkyEngine — the difference is Schwarzerblitz is a standalone 3D fighting engine (Irrlicht + SFML), not a UE5 framework. It is a study-and-build foundation for the owner's 3D fighting work, not a game itself.

## 2. Where we're at

### DONE
- **Engine source in place:** full Schwarzerblitz engine source, Irrlicht, SFML 2.3.2, licences, README (upstream project description + GameJolt link: https://gamejolt.com/games/schwarzerblitz/242456).
- **Anti-clobber laws merged (2026-10-17, PR #3):** the owner's anti-clobber laws are in `AGENTS.md`.
- **Working method stated (2026-10-27):** commits `042c778` / `f5f24cd`, `WORKING-METHOD.md` at root.
- **Last push 2026-11-20** (repo metadata; no new content commits after Oct 27 — the push reflects repo-level activity).

### IN PROGRESS
- **Two open docs PRs (Nov 19–20, unmerged):** PR #6 — "Docs: pre-made parts first rule" (`docs/premade-parts-first`, 2026-11-20); PR #5 — "Docs: sourcing rule" (`docs/sourcing-rule`, 2026-11-19). Next step: a merge call on #5 and #6.
- **No game built on this engine is recorded in this repo.** Whether a fighter is being built from Schwarzerblitz, which one, and what its first slice is, is NOT stated in the repo state read 2026-11-22. That is an open question (see §6), not hidden progress.

### BLOCKED
- **Nothing recorded as blocked in the repo state read 2026-11-22.** No blocked item is named in this repo. The open PRs are awaiting a merge decision, not unblocked work.
- **Branch note (not a block):** the default branch is `master`, not `main`. Every branch/PR/merge command must use `master` as the base — using `main` will fail.

## 3. What we're working toward

**The goal:** Schwarzerblitz understood and usable as the owner's 3D fighting engine option — a standalone engine (no UE5 needed) that a fighter can actually be built on.

**The bar (owner, general):** PULL-100% / REAL-SOURCE-ONLY — real code, wired in, never re-typed or hand-tooled. For an engine repo, done means: the copy is faithful to upstream, the owner's notes say how it is used, and a fighter built on it actually runs and plays.

**In order:** (1) merge or close PRs #5 and #6; (2) record which fighter/game builds from this engine and what its first slice is (owner's call); (3) keep the copy current with upstream Schwarzerblitz work.

## 4. Standing rules that apply here

- **Branch → PR → merge, always — base is `master`.** Never push to master directly. Add-only, zero-conflict PRs, no force pushes.
- **Checkpoint-and-save law:** CHECKPOINT.md first, update after every step; the repo is the save; resume, never restart.
- **No-temp-storage law:** nothing in /tmp or any wipeable location, ever. Everything goes straight into the repo or a durable folder the second it exists.
- **Real-source-only:** build from the real source. No hand-tooled lookalikes, no fake panels. Upstream engine stays faithful — local changes are layered and noted, not silent rewrites.
- **Anti-clobber law (owner 2026-10-17):** do not clobber other lanes' work. Add, don't overwrite. (Merged as PR #3.)
- **Licence-not-a-gate:** licence status never gates pulling in or using material that helps; licence/source is still logged honestly next to the item. (Schwarzerblitz is free-as-in-beer; its licence files are in `license/` — respect them as written.)
- **No-gaps / solve-it law:** a gap or block is never the end of the work — route-switch until it's done or every reasonable route is exhausted with exact errors recorded.

## 5. Key files and paths

| What | Where |
|---|---|
| Engine overview (upstream README) | `README.md` |
| Engine source | `schwarzerblitz_engine/` |
| Rendering / windowing | `irrlicht/`, `SFML-2.3.2/` |
| Licences | `license/`, `LICENSE.md` |
| Agent notes / working method | `AGENTS.md`, `WORKING-METHOD.md` |
| Docs | `docs/` |
| Upstream project page | https://gamejolt.com/games/schwarzerblitz/242456 |
| Open PRs | #5 (sourcing rule), #6 (pre-made parts first rule) |
| Merged PR | #3 (anti-clobber laws, 2026-10-17) |

There are no releases in this repo. Default branch is `master` — not `main`.

## 6. Open decisions needing the owner

- **Merge PRs #5 and #6?** Two small docs-rule PRs open since Nov 19–20. Merging locks the rules in; leaving them open leaves the repo without the written rules. His call — lanes do not decide merges.
- **Which fighter/game builds from Schwarzerblitz, and what's its first slice?** Not recorded in the repo. That is his call — a lane cannot pick a game for him. (NightSkyEngine and Lyra are the other framework options; which engine a given game uses is also his call.)
- **Keep tracking upstream Schwarzerblitz work?** Whether this copy tracks upstream or stays pinned is his call.
- **No other owner decision is recorded as open in this repo's state.**

## 7. How to pick up

1. Read this HANDOFF.md first, then `README.md`, `AGENTS.md`, and `WORKING-METHOD.md`.
2. Remember: default branch is `master`. Base every PR on `master`.
3. Check the two open PRs (#5, #6) — leave them alone unless told to merge.
4. Do NOT start building a fighter on this engine until the owner says which game and what slice. This is the engine foundation; the game decision is his.
5. Resume from the stated next step — never restart, never re-derive finished work.
6. Land work branch → PR → merge, add-only. Update this HANDOFF.md in the same PR when the state changes. Verify with your own eyes (a running build) before claiming anything done.
