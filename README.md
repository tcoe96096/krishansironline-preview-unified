# Krishan Sir Online — Unified Preview

This **isolated, public GitHub Pages preview repository** is used for owner-approved previews of [the main KSOL source repository](https://github.com/tcoe96096/krishansironline). It must never deploy to the production domain `krishansir.online`.

## Teacher Management v2 — visual preview

- **Preview address (requires a successful GitHub Pages deployment):** https://tcoe96096.github.io/krishansironline-preview-unified/teacher-beta/
- **Unified website preview (requires deployment):** https://tcoe96096.github.io/krishansironline-preview-unified/
- **Existing manual deployment workflow:** [Unified Preview — Manual Owner-Approved Deploy](https://github.com/tcoe96096/krishansironline-preview-unified/actions/workflows/unified-preview.yml)
- **Workflow configuration:** [.github/workflows/unified-preview.yml](.github/workflows/unified-preview.yml)

The URLs above identify the configured GitHub Pages paths, **not proof that a live deployment has succeeded**. Use the workflow's most recent successful `Publish Preview Only` deployment and its `github-pages` environment link to verify the actual page before sharing it as live.

### Publish an authorized visual preview

1. Open the existing **Unified Preview — Manual Owner-Approved Deploy** workflow in this repository's **Actions** tab.
2. Select **Run workflow**, leave `main` as the workflow branch, and enter the explicitly approved source branch, tag or commit SHA from `tcoe96096/krishansironline` as `source_ref`.
3. Check that the **Preview-only** repository secrets `PREVIEW_SUPABASE_URL` and `PREVIEW_SUPABASE_PUBLISHABLE_KEY` are configured. The workflow refuses any URL other than the dedicated Preview Supabase project. Never use production credentials or service-role keys.
4. Run the workflow and confirm successful **Validate and Build Isolated Preview** and **Publish Preview Only** jobs. If GitHub Pages asks for setup, configure this repository's Pages source to **GitHub Actions**.
5. Open the Teacher preview URL above on a phone and check registration layout and disabled-operation notices.

The isolated portal is built with `VITE_TEACHER_BETA_ENABLED=false`, advanced features disabled, and has **no enabled registration or approval backend**. Preview publication does not authorize database migrations, real teacher registration, access grants, Cloudflare changes or production deployment.

**Status:** Workflow source and Teacher Beta integration were confirmed in this repository on 18 Nov 2026; a successful current Pages deployment was not independently verified.
