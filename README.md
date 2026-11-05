# LocalBiz Myanmar — SME Platform

**Repository:** `aiacademyanmar/SMEPLAFORM`  
**Project:** Local Products, Branding, Licensing, Education, Professional Services, Commerce and Delivery  
**Development baseline:** V2.1.2  
**Release status:** BLOCKED — source upload and actual CI/APK verification pending.

## Important security notice
This repository is currently **PUBLIC**. Earlier plans called for a **PRIVATE** development repository. Please change visibility to Private in GitHub Settings → General → Danger Zone **before uploading proprietary source code, financial logic, or any credentials**. Never commit `.env`, signing keys, payment secrets, private customer data or production backups.

## What is available
The V2.1.2 offline development package, created in the ChatGPT development session, includes a Laravel overlay, Kotlin Compose project, CI workflow, static/CLI tests and release-gate reporting. **It is not yet pushed here.** This repository currently contains only public-safe onboarding documentation.

## Proposed repository layout
- `android/` — Kotlin + Jetpack Compose (Debug APK)
- `laravel-overlay/` — Laravel API, migrations, RBAC and feature tests
- `scripts/` — bootstrap, static tests, APK verification and QA
- `.github/workflows/localbiz-v212-ci.yml` — SQLite, MySQL, Android and artifact verification
- `docs/` — acceptance matrix, reports, release gates

## Verification gates
1. PHP lint/static tests pass.
2. Laravel HTTP tests pass with **SQLite**.
3. Laravel HTTP tests pass with **MySQL** and the driver is verified.
4. Android Gradle `assembleDebug` and unit/lint checks pass.
5. Downloaded APK hash, package name, version, and signature are verified.
6. Physical Samsung QA and business sign-off are recorded separately.

**Current CI status:** no verified workflow run or downloadable APK yet.

## Release rules
Do not label any step **PASS** unless actual test evidence exists. Publishing an APK, moving funds, marking refunds/payouts paid or claiming Samsung QA require separate verified proof.

## Next step
After switching to Private, import the full V2.1.2 source files into this repository, then run the GitHub Actions build and investigate actual logs. Do not force-push unrelated work.
