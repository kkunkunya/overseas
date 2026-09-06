# Issue #7 affected incremental recheck

## Verdict

`pass` for the affected content candidate at the new mono HEAD. Prior blocking findings F1 and F2 are closed by the three-file delta. The unchanged knowledge-base/HTML evidence retains its prior desktop and 390px `pass`; no browser rerun was performed. PR, merge, distribution, real-product execution, and parent #6 completion remain `park`.

## Candidate lock

- mono branch: `feat/7writer-tmpwebsite-loop-dispatchmd-httpsgithu`
- new HEAD: `6c0297d9acbd6c9ff695e4df0b6864d6fb663f5e`
- prior reviewed HEAD: `945c4ea78bee2d64c337988d8e3f060fadbd3af4`
- base and merge-base: `01dc63c294879f71d5407ef920c61508289867d4`
- worktree: clean at initial and final lock
- incremental scope: exactly these three modified files:
  - `skills/overseas/treg-research/SKILL.md`
  - `skills/overseas/ask-overseas/references/lifecycle-route.md`
  - `skills/overseas/ask-overseas/references/website-operations-loop.md`
- knowledge branch: `feat/7website-loop-preparation`
- knowledge HEAD: `d8fcbe9f0d9733f1bed13363351a69a0b6aa9802`
- knowledge base and merge-base: `23a7655cd9e3195e9ceb67edaa85e676385e3bf8`
- knowledge worktree: clean; no diff from the previously checked HEAD, so HTML is unchanged

No writer private self-check material was read. This recheck used only the old finding closure conditions and the candidate delta.

## F1 recheck — closed

### No-production-domain bounded preparation

`treg-research` now accepts either a product decision or one named website-loop capability question (`treg-research/SKILL.md:11-13`). A site without a production domain can ask about one of crawl, performance, snapshot, or data-read capability without inventing a product-selection question. Preparation records the capability, current environment, status, missing conditions, owner, and activation condition (`:38,46,50,58`). It may inspect existing catalog/help/schema when that needs no new permission or cost, but it cannot install, connect an account, incur cost, or run a target sample. This satisfies the original no-domain preparation closure condition.

### Designated-product authorized minimum call

The call path is now a distinct section entered only after the product, target/environment, permission, cost, and exact minimum call are authorized (`treg-research/SKILL.md:60-65`). It limits the website-loop path to one named capability and one minimum target sample, retains environment/time/scope/raw result/coverage limits, and does not expand installation, account, fee, write, or publishing authority (`:46,62`). A capability cannot become `可用` without the actual sample. This satisfies the original authorized-call boundary.

The lifecycle route now names a bounded capability question and explicitly allows preparation before a production domain exists (`lifecycle-route.md:20`), so the upstream and downstream contracts agree.

Result: `pass`; F1 closed.

## F2 recheck — closed

The website loop now records the problem on version A, the repair, version B, retest conditions, and known differences (`website-operations-loop.md:24,36`). It explicitly says a repair creates a version difference, preserves both A and B records, keeps URL/flow, environment, and observation conditions comparable where possible, and records any unavoidable condition change plus its effect on comparison (`:38`).

Executable scenario:

1. Record the reproducible problem and evidence on version A.
2. Hand the repair to the product/configuration owner.
3. Record the repaired candidate as version B.
4. Retest B under comparable URL/flow, environment, and observation conditions.
5. Preserve A and B; disclose any changed condition and how it limits the comparison.

This no longer requires the repaired version to remain the same as the broken version and matches the previously accepted HTML wording.

Result: `pass`; F2 closed.

## Incremental checks

- `git diff --check 945c4ea..6c0297d`: pass.
- 11 overseas Skill discovery frontmatters: pass.
- feature-source skill index validation with `--allow-feature-source`: pass; 95 skills, no stale map/reference finding.
- referenced website-loop and external-program-contract files exist.
- old HEAD to new HEAD contains one commit, `6c0297d9acbd6c9ff695e4df0b6864d6fb663f5e fix(overseas): clarify website capability checks`.

## Retained results and parks

- Retained from the unchanged knowledge candidate: desktop HTML `pass`, 390px HTML `pass`, five affected cards `pass`, 25 modules `pass`, 11 entries `pass`, Apple preservation `pass`.
- Content candidate at the exact mono/knowledge SHAs above: `pass`.
- PR creation / merge / distribution: `park`. No authentication, API, credential switch, PR, merge, or distribution action was attempted.
- Real-product crawl/performance/snapshot/data/payment evidence: `park` until a product and authorized environment are supplied.
- Parent issue #6 and full I8: `park`; content preparation passing does not establish real-product execution or integration facts.
