# Issue #7 fresh independent acceptance report

## Verdict

`needs-work` for the candidate content. The HTML and most preparation rules pass, but two formal-method contradictions prevent the advertised route/retest flow from being executable as written. PR creation, merge, distribution, real-product integration, and parent #6 completion remain separate `park` items.

## Candidate lock

- mono: branch `feat/7writer-tmpwebsite-loop-dispatchmd-httpsgithu`; HEAD `945c4ea78bee2d64c337988d8e3f060fadbd3af4`; base and merge-base `01dc63c294879f71d5407ef920c61508289867d4`; clean at start and final recheck. Remote branch also resolves to the same HEAD.
- knowledge base: branch `feat/7website-loop-preparation`; HEAD `d8fcbe9f0d9733f1bed13363351a69a0b6aa9802`; base and merge-base `23a7655cd9e3195e9ceb67edaa85e676385e3bf8`; clean at start and final recheck. Remote branch also resolves to the same HEAD.
- public contracts read directly: `kkunkunya/overseas` issues #7 and #6. No writer self-check conclusion was used.

## Blocking findings and observable closure conditions

### F1 — website tool-check routing dead-ends at `treg-research`

The new website loop assigns external capability checks to `treg-research` (`website-operations-loop.md:23`), and `ask-overseas` promises this route for a completed site preparing to launch (`ask-overseas/SKILL.md:25`). But `treg-research/SKILL.md:11-13,28-38` still requires a question that changes product selection and otherwise stops. A concrete launch-initialization request such as “the site exists, has no production domain, check whether our crawler/performance/snapshot/data readers are usable” is an operational capability question, not a product-selection question, so the delegated entry rejects the route. Line 42 also embeds the ticket-specific sentence “本票不安装或执行外部仓库程序” in a reusable Skill, leaving future authorized product sampling ambiguous.

Close F1 when `treg-research` explicitly accepts a bounded website capability/integration question from the website loop, and the preparation-only restriction is scoped to preparation mode while a designated-product, authorized run can perform the minimal call required by the external-program contract. Re-run the no-domain scenario from `ask-overseas` through `treg-research` without inventing a product-choice question.

### F2 — the formal retest rule requires the repaired version to stay unchanged

`website-operations-loop.md:36-38` correctly requires repair handoff and retest, but line 38 says the retest must use the same URL/flow, environment, **version**, and observation conditions. A code/config repair necessarily changes the version. Under this rule, the validator must either retest the old broken version or mislabel the repaired version. The HTML `technical` card is better: it requires the same URL, environment, and observation conditions and does not require the same version.

Close F2 when the formal rule records the before and after version separately, keeps the comparable URL/flow, environment, and observation conditions fixed where applicable, and confirms the candidate HTML and method express the same rule. Re-run a simulated finding on version A, repair on version B, and show that the retest record can honestly name both versions.

## Per-item result

| Item | Result | Evidence |
| --- | --- | --- |
| I1 route and four owners | `needs-work` | Four sections and owners exist, but F1 breaks the external-capability branch. |
| I2 state model | `pass` | `可用 / 待接入 / 不适用` requires environment-specific samples, evidence, limits, owner/next action, and recheck conditions. |
| I3 environment, rerun, history | `pass` | Per-site records, preview/production separation, append-only history, and no cross-site copying are explicit. |
| I4 findings and retest | `needs-work` | Finding fields, ownership, tool/site fault separation, and no premature resolution pass; F2 makes versioned retest internally contradictory. |
| I5 measurement | `pass` | Trigger, dedupe, environment, test exclusion, missing-vs-zero, and order/payment/entitlement separation are explicit. |
| I6 review | `pass` | Earliest bottleneck, one main adjustment, evidence boundary, and observation decision are explicit. |
| I7 baseline update | `pass` | Before/after capture, version/time, old-baseline retention, reviewed new baseline, and no automatic abnormal overwrite are explicit. |
| Desktop HTML | `pass` | Fresh 1440×900 Chromium: 25 cards/11 helpers; “现在准备” produced exactly 8 IDs (`brief,payment,domain,technical,performance,measurement,drift,tools`); search `程序工具` produced `technical,tools`; `tools` expanded; no horizontal overflow. |
| 390px HTML | `pass` | Fresh 390×844 Chromium: no horizontal overflow; “上线之后” produced 6 items; Apple search produced only `languages` and expanded; review search exposed/expanded `review`; visible copy was readable. |
| Five affected cards | `pass` | JSON and HTML agree on all fields/actions for `technical,measurement,drift,tools,review`; all five local-note targets exist and returned HTTP 200. Python’s minimal server served `.md` as `application/octet-stream`, so in-tab Markdown rendering was not used as evidence. |
| 25 modules / 11 entries / Apple | `pass` | 25 JSON entries match 25 HTML card IDs in order; 11 helpers remain; Apple case file is unchanged (`sha256 d801669f283324a9b5371fd3c65529f7f3006a35f908604989f18c6d9920eeb3`) and its mobile card was visually checked. |
| I8 candidate slice | `needs-work` | HTML agrees with its JSON and most formal wording, but F1/F2 prevent full candidate-method approval. |
| PR / merge / distribution | `park` | No knowledge PR found; mono PR lookup is unavailable to the current GitHub credential and no credential switch was attempted. User reports PR creation API rejection. No merge/distribution attempted. Unpark after exact-head PRs exist and authorized integration/distribution facts are verifiable. |
| Real product checks | `park` | No first product, production domain, search ownership, payment provider, or product accounts were supplied. Unpark after a designated product and authorized environment can produce crawl, performance, snapshot, data-read, and applicable payment/entitlement evidence. |
| Parent #6 overall | `park` | Parent completion requires full I1-I8 including real-product evidence; this leaf and its preparation artifacts cannot close it. |

Lody review submission was attempted once as required by the review tool, but the runtime returned `REVIEW_RUN_NOT_FOUND` because this Session is not registered as a branch review agent. It was not retried. The local report is the authoritative handoff from this Session; no GitHub comment was attempted.

## Browser and static evidence

- `desktop-tools-expanded-cdp.png`: actual CDP screenshot of desktop search and expanded `tools` card.
- `mobile-390-top-cdp.png`: actual CDP screenshot of the 390px page header/current-state copy.
- `mobile-390-apple-expanded-cdp.png`: actual CDP screenshot of the preserved Apple card at 390px.
- `mobile-390-review-expanded-cdp.png`: actual CDP screenshot of the review card at 390px.
- Static checks passed: 11 overseas Skill frontmatters; mono skill index with `--allow-feature-source`; JSON parsed; 25-card ordered ID match; five changed-card field/action match; 32 local links with no missing filesystem target.

## Untested range

No live product crawl, laboratory/field performance run, page-snapshot persistence, GSC/analytics read chain, payment/order/entitlement reconciliation, production release, repeated product initialization, controlled product repair, or real baseline promotion was performed. No PR creation, GitHub comment, merge, distribution, login, OAuth, authorization, message, or issue close was attempted.
