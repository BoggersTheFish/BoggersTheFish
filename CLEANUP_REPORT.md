# Cleanup Report

Date: 2026-05-22

## Scope

This pass added a public routing/control layer across:

- `BoggersTheFish`
- `TS-Start-Here`
- `BoggersTheCIG`

It did not delete repos, rewrite history, or change code behavior.

## Repos Found Locally

Found in `/home/boggersthefish/workspace`:

- `BoggersTheFish`
- `TS-Start-Here`
- `BoggersTheCIG`
- `TS-Reasoner-v0`
- `TS-Core`
- `bozo`
- `boggersthefish-site`
- `cig-ts-engine`
- `BoggersTheAI`
- `BoggersTheMind`
- `BoggersTheLLM`
- `TinyLLM`
- `ts-llm`
- `woke-baby-llm`
- `GOAT-TS`
- `GOAT-TS-DEVELOPMENT`
- `GOAT-TS-LITE`
- `GOAT-TS-SUPERLITE`
- `GOAT-PUBLIC_TEST`
- `BoggersTheSystem`
- `BoggersThePulse`
- `BoggersBrain`
- `BoggersTheAI-Dev`
- `BAGI`
- `BLM`
- `schizo_bet`
- `hehe`
- `GOAT-OS`
- `3b_solution`
- `CIG-APP-V1`
- `BoggersTheCIG_v2`

## Repos Missing Locally

- `TS-Codex-OS`
- standalone `TensionLM` repo, if separate from `bozo`

## Files Changed By Repo

### BoggersTheFish

- `README.md`
- `PUBLIC_REPO_INDEX.md`
- `GITHUB_MANUAL_ACTIONS.md`
- `WEBSITE_ALIGNMENT_CHECKLIST.md`
- `docs/HISTORICAL_REPO_NOTE.md`
- `docs/ARCHIVE_CANDIDATES.md`
- `CLEANUP_REPORT.md`

### TS-Start-Here

- `README.md`
- `docs/first_contact.md`
- `docs/repo_taxonomy.md`
- `docs/github_cleanup_plan.md`
- `docs/flagship_route.md`
- `docs/repo_metadata_recommendations.md`

### BoggersTheCIG

- `README.md`
- `docs/ARCHITECTURE.md`
- `docs/LIMITATIONS.md`
- `docs/FIRST_CONTACT.md`
- `docs/GITHUB_METADATA.md`

Note: `BoggersTheCIG/LICENSE` was already present as an untracked local file before this cleanup pass. It was not created by this pass.

## Tests And Checks

### Markdown

Basic markdown link-shape checks were run across the edited markdown files in:

- `BoggersTheFish`
- `TS-Start-Here`
- `BoggersTheCIG`

Result: no malformed markdown links were detected by the local syntax check.

### BoggersTheCIG Tests

Attempted:

```bash
python -m pytest
```

Result:

```text
/bin/bash: line 1: python: command not found
```

Attempted:

```bash
python3 -m pytest
```

Result:

```text
/usr/bin/python3: No module named pytest
```

Attempted:

```bash
python3 -m unittest discover
```

Result: failed with 9 import errors because the tests import `pytest`, which is not installed in the current environment.

No code files were changed in this pass.

## Publishing Status

- `BoggersTheFish` branch `codex/public-routing-control-layer` pushed successfully.
- `TS-Start-Here` branch `codex/routing-control-layer` pushed successfully.
- `BoggersTheCIG` commit `51049453` exists locally on branch `codex/cig-public-framing-cleanup`, but push was interrupted because `git push` stayed in pack/remote-transfer with no remote output for several minutes. The local CIG cleanup is committed and ready to retry.
- `BoggersTheCIG` still has a pre-existing untracked `LICENSE` file that was not staged or committed by this pass.

## Manual GitHub UI Actions Still Required

1. Change pinned repos to:
   1. `TS-Start-Here`
   2. `TS-Reasoner-v0`
   3. `TS-Codex-OS`
   4. `TS-Core`
   5. `bozo`
   6. `BoggersTheCIG`
2. Add or update GitHub repo descriptions and topics from:
   - `GITHUB_MANUAL_ACTIONS.md`
   - `TS-Start-Here/docs/repo_metadata_recommendations.md`
   - `BoggersTheCIG/docs/GITHUB_METADATA.md`
3. Consider renaming `bozo` to `TensionLM` later, or creating a clean `TensionLM` mirror.
4. Add historical-routing notes to older prototype repos before archiving anything.
5. Keep support/donation/coin routing separate from the research credibility path on the website.

## Recommended Pinned Repo Order

1. `TS-Start-Here`
2. `TS-Reasoner-v0`
3. `TS-Codex-OS`
4. `TS-Core`
5. `bozo`
6. `BoggersTheCIG`

## Recommended Archive / De-Emphasis List

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

Suggested actions are listed in `docs/ARCHIVE_CANDIDATES.md`.

## Next Cleanup Pass

Recommended next pass:

1. Apply the historical routing note to the highest-risk old READMEs.
2. Standardize README headers for `TS-Core`, `bozo`, and `cig-ts-engine`.
3. Align `boggersthefish-site` project ordering with the profile route.
4. Install or create a clean test environment for `BoggersTheCIG`, then rerun `python3 -m pytest`.
5. Decide whether `BoggersTheCIG` or `cig-ts-engine` is the canonical CIG first-contact repo.
