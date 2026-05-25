# Ogoron

Ogoron is an AI-assisted test development and maintenance platform for engineering teams that want broader regression coverage without turning test writing into a separate manual process.

It analyzes code changes, application structure, API behavior, UI flows, and existing test results, then generates and maintains automated tests as the product evolves.

## What Ogoron does

- Generates and updates unit, API, integration, and UI tests.
- Works from repository context, diffs, runtime behavior, and test execution feedback.
- Helps keep regression coverage aligned with active development.
- Produces reports that explain failures, generated changes, and coverage impact.
- Integrates with existing CI workflows instead of requiring a new development process.

## CI integrations

Ogoron currently provides public automation integrations for:

- **GitHub Actions**: setup, generate, run, heal, and exec actions.
- **Bitbucket Pipelines**: public Docker-based pipes with full and light images.
- **CLI usage**: direct command-line execution for custom CI setups.

The GitHub Actions repositories are maintained here in the `OgoronAI` organization. Bitbucket Pipes are published through DockerHub under the `ogoron` namespace.

## Core workflow

A typical Ogoron automation loop looks like this:

1. Analyze repository changes and project structure.
2. Generate or update test artifacts.
3. Run tests in CI.
4. Inspect failures, coverage changes, and execution output.
5. Heal generated tests when application behavior changes.

This is intended to support normal engineering workflows: pull requests, merge checks, release branches, and scheduled regression runs.

## Public repositories

Key public repositories include:

- `ogoron-actions`: shared GitHub Actions documentation and examples.
- `ogoron-setup-action`: bootstrap Ogoron in a repository.
- `ogoron-generate-action`: generate test artifacts.
- `ogoron-run-action`: run generated or project tests.
- `ogoron-heal-action`: repair generated tests after failures or product changes.
- `ogoron-exec-action`: run explicit Ogoron CLI commands in CI.
- `ogoron-cli`: public CLI distribution surface.

## Links

- Website: https://ogoron.com
- Documentation: https://docs.ogoron.ai
- DockerHub: https://hub.docker.com/u/ogoron
- Contact: info@ogoron.com
