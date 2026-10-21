# Open-source contributions

[Back to profile](README.md)

My recent upstream work focuses on coding-agent reliability, developer tools, and Rust infrastructure. This index includes merged changes, open proposals, closed unmerged proposals, and problem reports; these are different outcomes, not interchangeable claims of adoption.

PR status snapshot: **October 21, 2026 (UTC)**: **7 merged, 7 open and 3 closed without merge** across the six recent upstream projects below. Counted with GitHub PR search restricted to those six repositories and direct readback of the new PR; earlier project-development PRs are excluded from these totals. Follow each linked PR for its current state. Issue statuses retain their October 17 snapshot except the CodeGraph follow-through checked October 18; “Closed” on an issue does not by itself establish that my proposed fix was merged.

## Pull requests

### oh-my-pi — coding-agent and shell reliability

| Contribution | PR | Status |
| --- | --- | --- |
| Keep regular-file `read` input on the runtime worker | [#15504](https://github.com/can1357/oh-my-pi/pull/15504) | Merged |
| Account for argument/environment pointers when sizing `xargs` batches | [#15708](https://github.com/can1357/oh-my-pi/pull/15708) | Merged |
| Acknowledge messaging-only agent wake completions | [#15834](https://github.com/can1357/oh-my-pi/pull/15834) | Merged |
| Publish a re-tasked agent's latest message result | [#15707](https://github.com/can1357/oh-my-pi/pull/15707) | Merged |
| Allow TERM cleanup before hard-killing cancelled jobs | [#15709](https://github.com/can1357/oh-my-pi/pull/15709) | Merged |
| Unblock `mapfile`/`readarray` process-substitution producers | [#15647](https://github.com/can1357/oh-my-pi/pull/15647) | Open |
| Report the persisted value replaced by a configuration save | [#15478](https://github.com/can1357/oh-my-pi/pull/15478) | Open |

The regular-file optimization in #15504 is distinct from the process-substitution `read` deadlock: I reported that failure in [#15501](https://github.com/can1357/oh-my-pi/issues/15501), and the maintainer landed its fix in [#15509](https://github.com/can1357/oh-my-pi/pull/15509).

### jcode — Rust developer tooling

| Contribution | PR | Status |
| --- | --- | --- |
| Group contiguous TUI typing into one undo step, including Korean IME events | [#1714](https://github.com/1jehuang/jcode/pull/1714) | Merged |
| Restore rustfmt in CI | [#1739](https://github.com/1jehuang/jcode/pull/1739) | Merged |
| Preserve native Unicode text instead of inferring Option shortcuts | [#1888](https://github.com/1jehuang/jcode/pull/1888) | Open |
| Support modifier-letter shortcuts on the Korean input source | [#1727](https://github.com/1jehuang/jcode/pull/1727) | Closed without merge |
| Exclude quoted heredoc bodies inside command substitution from command-risk parsing | [#1752](https://github.com/1jehuang/jcode/pull/1752) | Closed without merge |
| Cancel abandoned OpenAI transport attempts while preserving credential commits | [#1758](https://github.com/1jehuang/jcode/pull/1758) | Closed without merge |

**#1888 follow-through (October 19, 2026):** Compared completed PR CI jobs with upstream's existing run at the exact base commit: the same eight Linux test failures and eleven macOS warning-budget diagnostics already occur without this patch. [Evidence and limits](https://github.com/1jehuang/jcode/pull/1888#issuecomment-6269776448). The PR remains open; this is CI diagnosis, not another merged fix.

### Rust infrastructure and Flutter

| Project | Contribution | PR | Status |
| --- | --- | --- | --- |
| OpenTelemetry Rust | Preserve batch export errors during span flushes | [#3791](https://github.com/open-telemetry/opentelemetry-rust/pull/3791) | Open |
| ts-rs | Remove trailing spaces before documented fields | [#501](https://github.com/Aleph-Alpha/ts-rs/pull/501) | Open |
| Flutter | Prevent SDK Git queries from re-inheriting a hook's repository environment | [#194429](https://github.com/flutter/flutter/pull/194429) | Open |
| swisseph | Decode native C error buffers only up to their first NUL | [#1](https://github.com/sawfan/swisseph_rs/pull/1) | Open |

**swisseph #1 verification:** An actual native error went from 174 NUL bytes to zero while preserving its original 78-byte cause exactly. The exact-source decoder tests and isolated Clippy checks pass. The current upstream crate's separate VFS build failures remain; this is not a full-crate build or production-integration claim. [Verification and limitations](https://github.com/sawfan/swisseph_rs/pull/1).

## Problem reports and proposals

Reporting a reproducible defect is a contribution, but it is not a claim of implementing the eventual fix.

| Project | Report | Issue status |
| --- | --- | --- |
| oh-my-pi | [Shell `read` hangs on process-substitution input](https://github.com/can1357/oh-my-pi/issues/15501) | Closed |
| oh-my-pi | [Clone-first worktrees copy gitignored secrets](https://github.com/can1357/oh-my-pi/issues/15476) | Open |
| oh-my-pi | [Per-worktree build caches exhaust disk](https://github.com/can1357/oh-my-pi/issues/15475) | Open |
| jcode | [Composer undo splits Korean IME input at arbitrary event boundaries](https://github.com/1jehuang/jcode/issues/1713) | Closed |
| jcode | [Korean input source prevents modifier-letter shortcuts](https://github.com/1jehuang/jcode/issues/1738) | Closed |
| jcode | [Quoted heredocs inside command substitution cause false command-risk prompts](https://github.com/1jehuang/jcode/issues/1751) | Closed |
| jcode | [Destructive commands inside substitutions and heredocs are rated safe](https://github.com/1jehuang/jcode/issues/1753) | Closed |
| jcode | [Stream producers survive cancellation and WebSocket sends lack a deadline](https://github.com/1jehuang/jcode/issues/1756) | Closed |
| jcode | [OAuth refresh needs an end-to-end deadline without losing rotation safety](https://github.com/1jehuang/jcode/issues/1757) | Closed |
| CodeGraph | [Multiline Axum route declarations do not link to handlers](https://github.com/colbymchenry/codegraph/issues/2326) | Closed; [fix on main](https://github.com/colbymchenry/codegraph/pull/2359), release pending |
| CodeGraph | [Dart type-reference positions are missed](https://github.com/colbymchenry/codegraph/issues/2327) | Closed; [fix on main](https://github.com/colbymchenry/codegraph/pull/2360), release pending |
| CodeGraph | [Rust enum variant paths are not linked to their enum](https://github.com/colbymchenry/codegraph/issues/2328) | Closed; [fix on main](https://github.com/colbymchenry/codegraph/pull/2354), release pending |
| Aside | [Propose a file-based bridge to local coding-agent sessions](https://github.com/at-inc/docs/issues/6) | Open |

**CodeGraph release status (checked October 18, 2026):** The three fix PRs above are maintainer-authored. The [latest GitHub release, v1.6.2](https://github.com/colbymchenry/codegraph/releases/tag/v1.6.2), and the published npm package still point to the October 3 source, before these fixes. These reports and diagnoses are not counted as additional merged PRs.

## Earlier public work

Earlier public engineering work includes [0xKYC backend contributions](https://github.com/0xKYC/BACKEND/pulls?q=is%3Apr+author%3Amg-mg-mg) and [frontend contributions](https://github.com/0xKYC/FRONTEND/pulls?q=is%3Apr+author%3Amg-mg-mg). These project-development and release PRs are kept separate from the recent upstream fixes above.

[Browse the full public PR history](https://github.com/search?q=author%3Amg-mg-mg+is%3Apr+is%3Apublic+-user%3Amg-mg-mg+-org%3ATriAstra-ai&type=pullrequests) · [Browse public issue reports](https://github.com/search?q=author%3Amg-mg-mg+is%3Aissue+is%3Apublic+-user%3Amg-mg-mg+-org%3ATriAstra-ai&type=issues)
