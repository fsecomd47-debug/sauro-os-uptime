# SAURO_OS availability check

This small public monitor repository checks only https://sauro-os.onrender.com/api/sauro/ping every ten minutes and on manual dispatch. It contains no application source, patient data, credentials, database access, or invitation links. Standard hosted runners are free for public repositories under GitHub's current terms; this workflow performs no checkout and has no repository permissions.

The check runs independently of any browser or developer computer, reduces Render Free cold starts, and verifies an expected liveness response. It never calls the database-backed readiness endpoint or signs into a clinic. GitHub's failure notifications follow the repository owner's Actions notification preferences.

This is best-effort availability, not an uptime guarantee. GitHub schedules can be delayed or dropped and are disabled after 60 days without repository activity. Render can restart instances and enforces its shared monthly Free quotas. Review this monitor at least monthly and use always-on hosting when continuous availability is required.

Pause the scheduled workflow in GitHub Actions to stop the checks. Run **SAURO_OS availability → Run workflow** to check immediately. The private clinic application repository is maintained separately.

Sources: [Render Free](https://render.com/docs/free), [GitHub scheduled workflows](https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule), [GitHub Actions billing](https://docs.github.com/en/billing/concepts/product-billing/github-actions).
