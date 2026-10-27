# Repository Guidelines

## Project Structure & Module Organization

This repository is a self-contained Day 2 training lab. `learner/starter/src/checkout.py` implements `calculate_total(items)`; `learner/starter/tests/test_checkout.py` contains its permanent tests. `sample_orders.json` is intentional synthetic exercise data, not an unused asset. Starter task cards and worksheets guide the comparison exercise. `learner/skill_and_mcp_lab.md` and `learner/integration_task_template.md` support optional integration training. No frontend, database, or asset pipeline exists.

## Build, Test, and Development Commands

From the repository root:

```sh
cd learner/starter
python -B -m unittest discover -s tests -v
```

This runs the checkout suite without generating bytecode caches. Use `python3` if that is your Python 3 executable. No package installation, application server, or production build command is configured. Exercise behavior through unit tests.

## Coding Style & Naming Conventions

Follow the existing Python style: four-space indentation, `snake_case` functions and variables, and descriptive docstrings. Test classes use `PascalCase`; test methods begin with `test_`. No formatter or linter is configured. Keep changes small and dependency-free unless the task requires otherwise. Preserve the public checkout contract: items contain `name`, `price`, and `quantity`, and calculation returns a float. Keep currency formatting in a separate helper.

## Testing Guidelines

Use standard-library `unittest`, with files named `test_*.py` under `learner/starter/tests/`. Cover changed behavior, boundaries, errors, and existing-call compatibility. No numerical coverage threshold is configured. Preserve permanent tests and fixtures; remove only verified disposable artifacts. Report executed commands and actual results, including limitations.

## Commit & Pull Request Guidelines

History contains only `training material for day2`, so no established commit convention exists. Use concise, descriptive imperative subjects, such as `Document checkout contributor workflow`. PRs should explain purpose, changed files, verification results, and public-contract or exercise impacts. Link relevant issues when available; screenshots are unnecessary for calculation-only changes.

## Documentation, Safety & Lab Isolation

Inspect references before deleting files. Update relevant READMEs, `CHANGELOG.md`, and `PROJECT_DOCUMENTATION.md` after changes. Keep credentials and real customer/payment data out of the repository; use local fakes for integrations. Do not deploy or alter production data without explicit authorization.

This root guide applies to descendants. Run the unguided baseline in a separate clean copy outside this instruction hierarchy, without copying this guide. Edit this file when contributor rules change; edit checkout behavior and its tests together.
