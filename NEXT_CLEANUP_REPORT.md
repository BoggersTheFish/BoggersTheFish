# Next Cleanup Report

Date: 2026-05-22

Scope: publish the BoggersTheCIG public documentation cleanup, document the test environment issue, standardize first-contact README headers for TS-Core, bozo/TensionLM, and cig-ts-engine, and record remaining GitHub UI work.

## 2026-05-22 Follow-Up: CIG Test Isolation And Historical Routing

Scope: make BoggersTheCIG default unit tests run in a venv without mutating tracked repo state, then add historical routing notes to the worst first-contact repos where local README files could be safely edited.

### Repos Inspected

| Repo | Result |
| --- | --- |
| `BoggersTheCIG` | Found; changed, tested, committed, and pushed. |
| `woke-baby-llm` | Found; historical routing note added and pushed. |
| `schizo_bet` | Found; historical routing note added and pushed. |
| `BAGI` | Found; historical routing note added and pushed. |
| `BLM` | Found; historical routing note added and pushed. |
| `GOAT-OS` | Found; historical routing note added and pushed. |
| `GOAT-PUBLIC_TEST` | Found; historical routing note added and pushed. |
| `GOAT-TS-LITE` | Found; `README.md` was missing, so a small routing README was added and pushed. |
| `GOAT-TS-DEVELOPMENT` | Found; not changed because `README.md` contains invalid UTF-8 bytes. |
| `GOAT-TS-SUPERLITE` | Found; not changed because `README.md` contains invalid UTF-8 bytes. |
| `BoggersTheAI-Dev` | Found; historical routing note added and pushed. |
| `TS-Codex-OS` | Still missing locally. |
| Standalone `TensionLM` | Still missing locally; current local TensionLM work is in `bozo`. |

### Repos Changed

#### BoggersTheCIG

Commit pushed to `main`:

- `f992aaee Isolate CIG tests from tracked state`

Files changed:

- `docs/CLEANUP_REPORT.md`
- `docs/TESTING.md`
- `pytest.ini`
- `src/concept_graph.py`
- `src/config.py`
- `src/provenance_store.py`
- `src/sqlite_store.py`
- `tests/conftest.py`
- `tests/test_self_improver.py`
- `tests/test_viz.py`

What changed:

- Test runtime paths now route to a temporary directory before `src.config` is imported.
- SQLite and provenance defaults now derive from `src.config.MEMORY_DIR`.
- Persistent store singletons are reset between tests.
- Self-improver tests are marked `integration`.
- Visualization tests are marked `slow`.
- Default test workflow is documented in `docs/TESTING.md`.
- `semantic_search` now has a lexical fallback when optional vector dependencies such as `numpy` are absent.

Test command run:

```bash
git status --short
python3 -m venv .venv
. .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements-dev.txt
python -m pytest -m "not slow and not external and not integration"
git status --short
```

Test result:

- `43 passed`
- `9 deselected`
- default test command exited successfully.
- `git status --short` after tests showed no tracked `memory/`, `graphs/`, `obsidian/`, `data/`, `eval/`, or `viz/` mutations.

Remaining test caveat:

- The full suite is not claimed green.
- Slow/integration tests remain separated because they may exercise plotting, broad self-improver workflows, vault behavior, or optional local services.

Push result:

- `git push` succeeded: `f7930dc7..f992aaee main -> main`.

#### Historical Routing Notes

Each changed historical repo received this note at the top of `README.md`:

```md
> **Historical prototype:** this repo is kept public for development history, but it is not the current first-contact path for the TS research stack. Start with `TS-Start-Here`, `TS-Reasoner-v0`, `TS-Codex-OS`, `TS-Core`, `bozo` / TensionLM, and `BoggersTheCIG`.
```

Commits pushed:

- `woke-baby-llm`: `2d47293 Add historical routing note`
- `schizo_bet`: `ec58b69 Add historical routing note`
- `BAGI`: `a93329d Add historical routing note`
- `BLM`: `709fbad Add historical routing note`
- `GOAT-OS`: `b8f7f9e Add historical routing note`
- `GOAT-PUBLIC_TEST`: `7d0cd52 Add historical routing note`
- `GOAT-TS-LITE`: `944bea5 Add historical routing note`
- `BoggersTheAI-Dev`: `dab4c3f Add historical routing note`

Skipped historical README edits:

- `GOAT-TS-DEVELOPMENT`: README contains invalid UTF-8 bytes, so it was not rewritten in this pass.
- `GOAT-TS-SUPERLITE`: README contains invalid UTF-8 bytes, so it was not rewritten in this pass.

No repositories were deleted, archived, force-pushed, or history-rewritten.

### Manual GitHub UI Actions Still Required

1. Pin repos in this order:
   1. `TS-Start-Here`
   2. `TS-Reasoner-v0`
   3. `TS-Codex-OS`
   4. `TS-Core`
   5. `bozo`
   6. `BoggersTheCIG`

2. Add or verify descriptions and topics for flagship repos using the metadata docs.

3. Consider renaming `bozo` to `TensionLM` later, or create a clean `TensionLM` mirror.

4. If routing notes are still desired for `GOAT-TS-DEVELOPMENT` and `GOAT-TS-SUPERLITE`, first do a dedicated README encoding cleanup so the files can be safely patched and reviewed.

### Next Recommended Pass

1. Clone or locate `TS-Codex-OS`, then standardize its README header and metadata.
2. Decide whether `BoggersTheCIG` or `cig-ts-engine` is the canonical public CIG route.
3. Run and triage the CIG slow/integration suite separately.
4. Clean README encoding in `GOAT-TS-DEVELOPMENT` and `GOAT-TS-SUPERLITE` before adding notes there.
5. Align the website project ordering with the GitHub flagship route.

## Repos Inspected

| Repo | Local path | Result |
| --- | --- | --- |
| BoggersTheFish | `/home/boggersthefish/workspace/BoggersTheFish` | Found; report added here. |
| TS-Start-Here | `/home/boggersthefish/workspace/TS-Start-Here` | Found; already cleaned and published in prior pass. |
| BoggersTheCIG | `/home/boggersthefish/workspace/BoggersTheCIG` | Found; docs cleanup published and merged. |
| TS-Reasoner-v0 | `/home/boggersthefish/workspace/TS-Reasoner-v0` | Found; not changed in this pass. |
| TS-Codex-OS | `/home/boggersthefish/workspace/TS-Codex-OS` | Missing locally. |
| TS-Core | `/home/boggersthefish/workspace/TS-Core` | Found; README header standardized and merged. |
| bozo | `/home/boggersthefish/workspace/bozo` | Found; original worktree had pre-existing untracked paper files, so README work used a clean auxiliary worktree. |
| bozo cleanup worktree | `/home/boggersthefish/workspace/bozo-readme-cleanup` | Created for clean README work; PR merged. |
| cig-ts-engine | `/home/boggersthefish/workspace/cig-ts-engine` | Found; README header standardized and merged. |
| boggersthefish-site | `/home/boggersthefish/workspace/boggersthefish-site` | Found; not changed in this pass. |
| TensionLM | `/home/boggersthefish/workspace/TensionLM` | Missing as a standalone folder; current local TensionLM work is in `bozo`. |

## Repos Changed

### BoggersTheCIG

Published PR: `https://github.com/BoggersTheFish/BoggersTheCIG/pull/1`

Main branch after merge: `f7930dc7 Reframe CIG public documentation`

Cleanup branch commits created locally:

- `51049453 Reframe CIG public documentation`
- `895f93b9 Document CIG test dependencies`
- `9a02a120 Record CIG push result`
- `5b6386cc Merge remote-tracking branch 'origin/main' into codex/cig-public-framing-cleanup`

Files changed by the cleanup:

- `README.md`
- `LICENSE`
- `requirements-dev.txt`
- `docs/ARCHITECTURE.md`
- `docs/LIMITATIONS.md`
- `docs/FIRST_CONTACT.md`
- `docs/GITHUB_METADATA.md`
- `docs/CLEANUP_REPORT.md`

Notes:

- The pre-existing untracked `LICENSE` file was a normal MIT license and no tracked license file was present, so it was added.
- The PR merge also incorporated existing upstream `origin/main` graph/vault updates that were already present on the remote. The public cleanup itself is documentation, license, and dev-test dependency work.

### TS-Core

Published PR: `https://github.com/BoggersTheFish/TS-Core/pull/1`

Main branch after merge: `989eca4 Standardize TS-Core public README header`

Branch commit:

- `1034f66 Standardize public README header`

Files changed:

- `README.md`

Change:

- Added a sober first-contact header with status, role in the TS stack, what the repo is, what it is not, and where to start.

### bozo / TensionLM

Published PR: `https://github.com/BoggersTheFish/bozo/pull/2`

Main branch after merge: `b02d0de Standardize TensionLM public README header`

Branch commit:

- `3ae7a82 Standardize TensionLM public README header`

Files changed:

- `README.md`

Change:

- Added a sober first-contact header and public naming note explaining that the repo contains the TensionLM work despite the older `bozo` name.

Local note:

- The original `/home/boggersthefish/workspace/bozo` worktree still has pre-existing untracked `paper.log` and `paper.tex`. They were not touched.

### cig-ts-engine

Published PR: `https://github.com/BoggersTheFish/cig-ts-engine/pull/1`

Main branch after merge: `66f7d7f Standardize CIG engine public README header`

Branch commit:

- `935bafd Standardize CIG engine public README header`

Files changed:

- `README.md`

Change:

- Added a sober first-contact header for the compact CIG/TS engine.

## Pushes Attempted

### BoggersTheCIG

Commands used during diagnosis and publish:

```bash
git status
git log --oneline -5
git remote -v
git branch --show-current
git diff --stat HEAD~1..HEAD
ls -la LICENSE
head -40 LICENSE
git count-objects -vH
git show --stat --oneline HEAD
git show --name-only --oneline HEAD
git ls-files | xargs -I{} du -h "{}" 2>/dev/null | sort -hr | head -30
git rev-list --objects --all | sort -k 2 > /tmp/all_git_objects.txt || true
timeout 300s git push --progress origin HEAD:refs/heads/codex/cig-public-framing-cleanup
```

Result:

- Push succeeded.
- Diagnosis: the push appeared stalled in previous attempts because the repository has a large packed history. `git count-objects -vH` reported about `1.04 GiB` packed, and the successful push uploaded about `1.03 GiB`.
- A progress-enabled bounded push made the upload visible and completed successfully.

Merge commands:

```bash
gh pr create --fill --base main --head codex/cig-public-framing-cleanup
git fetch origin main
git merge origin/main
git push origin HEAD:refs/heads/codex/cig-public-framing-cleanup
gh pr merge 1 --squash --delete-branch --subject "Reframe CIG public documentation"
```

Result:

- First merge attempt was blocked by a `README.md` conflict with newer `origin/main`.
- Conflict was resolved locally.
- PR #1 was squash-merged and the remote branch was deleted.

### TS-Core

Commands:

```bash
git fetch origin
git switch -c codex/standardize-public-readme-header origin/master
git push -u origin codex/standardize-public-readme-header
gh pr create --fill --base master --head codex/standardize-public-readme-header
gh pr ready 1
gh pr merge 1 --squash --delete-branch --subject "Standardize TS-Core public README header"
```

Result:

- Push and merge succeeded.

### bozo / TensionLM

Commands:

```bash
git worktree add -b codex/standardize-tensionlm-readme-header /home/boggersthefish/workspace/bozo-readme-cleanup origin/main
git push -u origin codex/standardize-tensionlm-readme-header
gh pr create --fill --base main --head codex/standardize-tensionlm-readme-header
gh pr ready 2
gh pr merge 2 --squash --delete-branch --subject "Standardize TensionLM public README header"
```

Result:

- Push and merge succeeded.
- A clean worktree was used to avoid disturbing pre-existing untracked files in the original `bozo` checkout.

### cig-ts-engine

Commands:

```bash
git switch -c codex/standardize-cig-engine-readme-header
git push -u origin codex/standardize-cig-engine-readme-header
gh pr create --fill --base master --head codex/standardize-cig-engine-readme-header
gh pr ready 1
gh pr merge 1 --squash --delete-branch --subject "Standardize CIG engine public README header"
```

Result:

- Push and merge succeeded.

## Test Commands Run

Test work was limited to BoggersTheCIG.

Commands and results:

```bash
python -m pytest
```

Result:

- Failed: `python` command was not found.

```bash
python3 -m pytest
```

Result:

- Failed: `No module named pytest`.

```bash
python3 -m unittest discover
```

Result:

- Failed with import errors because tests import `pytest`.

```bash
python3 -m pip install -r requirements-dev.txt
```

Result:

- Failed because the system Python environment is externally managed by PEP 668.

```bash
python3 -m venv /tmp/boggers_cig_test_venv
/tmp/boggers_cig_test_venv/bin/python -m pip install -r requirements-dev.txt
/tmp/boggers_cig_test_venv/bin/python -m pytest
```

Initial result before adding `networkx`:

- Pytest collected 52 tests.
- Result: `33 passed, 12 failed, 7 errors`.
- Main missing dependency: `networkx`.

After adding `networkx>=3.2.0` to `requirements-dev.txt`:

- Pytest progressed further.
- Visible progress included:
  - `tests/test_concept_graph.py ..F....`
  - `tests/test_e2e.py .`
  - `tests/test_hardware_adapt.py ...........`
  - `tests/test_knowledge_ingest.py ......`
  - `tests/test_language_layer.py ....`
  - `tests/test_obsidian_bridge.py ..`
- The run then stalled in the Obsidian bridge area and was stopped rather than hidden.

Test side effects:

- The CIG tests mutated tracked memory files:
  - `memory/knowledge.db`
  - `memory/provenance_index.json`
  - `memory/provenance_store.jsonl`
- Those local test mutations were restored before publishing. The tests need better isolation before they are safe as a routine cleanup check.

## Missing Dependencies / Environment Issues

- `python` is not installed as a command; use `python3`.
- System `pytest` is not installed.
- System `pip` install is blocked by externally managed Python environment policy.
- `requirements-dev.txt` now documents a minimal test/dev dependency set:
  - `pytest>=7.4.0`
  - `pytest-asyncio>=0.23.0`
  - `networkx>=3.2.0`
- Full CIG test reliability is not fixed yet. The suite still needs isolated temp stores/vaults and a timeout-safe Obsidian bridge test path.

## Current Repo Status

After this pass:

- `BoggersTheCIG`: clean on `main...origin/main`.
- `TS-Core`: clean on `master...origin/master`.
- `cig-ts-engine`: clean on `master...origin/master`.
- `bozo-readme-cleanup`: clean on `main...origin/main`.
- Original `bozo`: still has pre-existing untracked `paper.log` and `paper.tex`; not touched.
- `BoggersTheFish`: this report was added and should be committed/pushed as the final accounting artifact.

## Manual GitHub UI Actions Still Required

1. Pin repos in this order:
   1. `TS-Start-Here`
   2. `TS-Reasoner-v0`
   3. `TS-Codex-OS`
   4. `TS-Core`
   5. `bozo`
   6. `BoggersTheCIG`

2. Add or verify repo descriptions and topics from the metadata docs:
   - `TS-Start-Here`
   - `TS-Reasoner-v0`
   - `TS-Codex-OS`
   - `TS-Core`
   - `bozo`
   - `BoggersTheCIG`
   - `cig-ts-engine`

3. Consider renaming `bozo` to `TensionLM` later, or create a clean `TensionLM` mirror that points back to the historical repo.

4. Add historical routing notes before archiving or de-emphasizing old repos.

5. Do not delete historical repos or rewrite history.

## Recommended Archive / De-Emphasis List

Keep these public only as historical context unless cleaned and rerouted:

- `GOAT-PUBLIC_TEST`
- `GOAT-TS-DEVELOPMENT`
- `GOAT-TS-LITE`
- `GOAT-TS-SUPERLITE`
- `BoggersTheAI-Dev`
- `hehe`
- `GOAT-OS`
- `BLM`
- `BAGI`
- `schizo_bet`
- `woke-baby-llm`

Recommended note for each:

> Historical prototype. This repo is kept public for development history, but it is not the current first-contact path. Start with TS-Start-Here, TS-Reasoner-v0, TS-Codex-OS, TS-Core, bozo/TensionLM, and BoggersTheCIG.

## Next Recommended Cleanup Pass

1. Clone or locate `TS-Codex-OS`, then standardize its README header and metadata.
2. Fix BoggersTheCIG test isolation:
   - use temporary memory stores,
   - use temporary Obsidian vaults,
   - prevent tests from mutating tracked state,
   - add a timeout or fixture cleanup around Obsidian bridge tests.
3. Add historical routing notes to the worst first-contact offenders, starting with:
   - `woke-baby-llm`
   - `schizo_bet`
   - `BAGI`
   - `BLM`
   - `GOAT-OS`
   - `GOAT-PUBLIC_TEST`
4. Align the website project ordering with GitHub pins:
   - TS-Start-Here
   - TS-Reasoner-v0
   - TS-Codex-OS
   - TS-Core
   - bozo/TensionLM
   - BoggersTheCIG
5. Decide whether `BoggersTheCIG` or `cig-ts-engine` is the public canonical CIG repo, then make the other clearly point to it.
