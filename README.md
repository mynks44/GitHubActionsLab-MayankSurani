# GitHub Actions Lab - Mayank Surani

## Workflow 1: Job Dependencies (build → test → deploy)
**File:** `.github/workflows/dependent-jobs.yml`  
Demonstrates job dependencies using `needs` so jobs run in order: build → test → deploy.

**Concepts:**
- `on: push` (runs when pushing to main)
- `needs` (job dependency)
- `runs-on` (runner OS)

## Workflow 2: Multi-Platform Testing
**File:** `.github/workflows/multi-platform.yml`  
Demonstrates parallel jobs across multiple operating systems: Ubuntu, Windows, macOS.

**Concepts:**
- `on: pull_request` (runs on PRs to main)
- No `needs` → jobs run in parallel
- `actions/checkout@v4`
- OS-specific commands + file creation

## Challenges
- Ensured correct YAML indentation.
- Ensured Workflow 1 triggers only on main pushes and Workflow 2 triggers only on PRs.
