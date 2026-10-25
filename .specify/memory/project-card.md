# egovframe-mcp-search-upload-data project context

Observed from the `work` source at `96acf7723524f303d4005700c0215671fa5ad87b` on 2026-10-26.
This is a maintenance context card, not a claim that application checks were run during adoption.

## Role and public entry points

Repository README describes eGovFrame data archives for MCP developer knowledge (Q&A/FAQ) and compatibility. The current tracked tree contains only README.md and Apache-2.0 LICENSE; no actual archive, schema, uploader, search server or consumer implementation is present.

## Evidence and maintenance boundaries

- `README.md`: a two-line statement identifying MCP developer-knowledge and compatibility archives.
- `git ls-tree -r --name-only HEAD` at the recorded pre-adoption work SHA: LICENSE and README.md only.
- `LICENSE`: Apache License 2.0.
- No AGENTS, contributor guide, application manifest, test or CI paths were present in this tree. Do not infer functionality from the repository name alone.

Keep the change scope and workflow policy in the [constitution](constitution.md); concept cards
link there rather than repeating the policy. Author a concept card only for actual planned work.

## Build and verification commands

- No repository-provided application build/test/lint/data-validation command exists in the observed source.
- For future archive changes, first identify the actual source, intended consumer and schema; then define appropriate structural/provenance validation with maintainer input.
- Adoption verification is limited to the pinned Spec Kit CLI/integration, bundled bug commands, complete constitution and template/scaffold smoke; it establishes no MCP search/upload behavior.

For this tooling-only adoption, verify Spec Kit CLI/integration status, installed core/bug commands,
constitution completeness, and template resolution/scaffold presence. Full application build,
lint, tests, formatter, external services, and deployment are not part of that smoke check.

## Upstream and submission baseline

Actual upstream is `eGovFramework/egovframe-mcp-search-upload-data`, default main. Fetch its current default SHA and prepare upstream-submit at that exact SHA only when absent; preserve existing submissions.

Any future contribution starts in a separate Orca submission worktree from the real upstream base, with only intended archive/license/user-documentation changes and their justified validation. Do not merge work, cherry-pick adoption commits or include model cards/tooling/reports in upstream changes. No PR or archive upload is created in this adoption.
No PR is created by adoption. Do not merge `work` or cherry-pick its adoption commit into a submission.
Preserve existing submission branches and PRs. Inspect changed paths and commits against the exact
base before any later PR; exclude work-only scaffolding without deleting upstream-owned files.

## Working with the pinned tooling

Installed by `uvx --from specify-cli==1.2.3 specify init --here --force --non-interactive
--integration omp --script sh --extension bug` after checking for existing path conflicts.
The CLI's init metadata pins 1.2.3; native agent commands live in `.omp/commands/`, including
`speckit.bug.assess.md`, `speckit.bug.fix.md`, and `speckit.bug.test.md`.
Use official upgrade support for future changes and preserve local customizations.
The new [domain model card template](../templates/model-card-template.md) aligns concept meanings
before specification; it is not an ML performance or benchmark card.

Observed submission base: `96acf7723524f303d4005700c0215671fa5ad87b` (eGovFramework/egovframe-mcp-search-upload-data, `main`).
Submission branch status: created-remote-at-upstream-default.
