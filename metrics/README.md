# Codebase measurement

[Back to portfolio](../README.md)

Measured on **13 October 2026** using **cloc 2.10** and committed local snapshots of three private implementation repositories. The underlying source was inspected locally; this public repository contains only descriptions, public-page captures and aggregate results.

## Results

| Product       | Selected product modules | Application source | Separate test source | Snapshot commit date |
| ------------- | -----------------------: | -----------------: | -------------------: | -------------------- |
| ClinGEO       |                   88,718 |            294,688 |              163,522 | 9 October 2026       |
| RightCareHome |                   82,640 |            461,443 |              132,821 | 12 October 2026      |
| Cognac Nation |                   52,556 |            200,501 |               61,793 | 5 October 2026       |

All numbers are physical source-code lines after removing comments and blank lines. Selected-module counts are subsets of application counts, not additional code. Test counts describe test source, not the number of tests, passing tests or coverage.

## Scope

**Application source:** eligible source files under `apps/web` and `packages`, including application UI, server logic and retained shared infrastructure. These projects use a Makerkit foundation; application counts include retained template code and do not isolate personally authored work.

**Selected product modules:** a narrower directory-based view of product implementation. It is not an exhaustive inventory of each product, an attribution analysis or a precise subtraction of all inherited code.

| Product       | Selected directories                                                                                                                                                                                        |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ClinGEO       | `packages/geo-engine/src`, `packages/content-hub/src`, `apps/web/lib/content-hub`, `apps/web/lib/clinic-growth-assistant`, `apps/web/lib/server/content-hub`, `apps/web/lib/server/clinic-growth-assistant` |
| RightCareHome | `apps/web/src/engine`, `apps/web/src/products`                                                                                                                                                              |
| Cognac Nation | `apps/web/lib/cnation`, `apps/web/components/cnation`                                                                                                                                                       |

**Test source:** eligible files matching `.test.*` or `.spec.*`, or within `test`, `tests` or `__tests__` directories, under the application/package roots and `apps/e2e`. Fixtures and generated content remain excluded.

## Counting rules

1. Read the committed local `HEAD` snapshot of each repository. Uncommitted modifications and untracked files are excluded. A committed snapshot is not necessarily the currently deployed version of every module.
2. Select source extensions: `.ts`, `.tsx`, `.js`, `.jsx`, `.mjs`, `.cjs`, `.css`, `.scss`, `.py` and `.sh`.
3. Exclude dependencies, builds, coverage, vendor directories, temporary exports, fixtures, mocks, generated directories, database type exports, stories, demo-data files, configuration files containing `.config.` in their names and files with a generated/do-not-edit header in their first 2,000 bytes.
4. Exclude JSON, YAML, Markdown, images, datasets, lockfiles and SQL. Database definitions and migrations are deliberately outside this code metric.
5. Separate tests from application source. Identify the selected product modules by the directory rules above.
6. Run `cloc --quiet --json --by-file --timeout=60 --list-file=...` on each manifest. Retain cloc's default duplicate-file detection within each measured set.

The published table reports projects separately. Identical shared files across different projects have not been subtracted from these individual totals; no combined unique-code total is claimed.

## How to interpret the figures

The figures show the scale of the inspected codebases and selected modules. They include work created with AI coding tools and retained framework components. They do not establish sole authorship, engineering effort, software quality, adoption or business impact. The private source and file-level measurement records are not published, so external readers cannot independently verify the numbers from this public repository alone.

[Machine-readable aggregate results](snapshot.json) · [cloc documentation](https://github.com/AlDanial/cloc)
