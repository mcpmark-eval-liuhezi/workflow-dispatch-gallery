# workflow-dispatch-gallery

A tiny demo repository for a brown-bag talk about GitHub Actions workflows that you start by hand (`workflow_dispatch`).

The main attraction is [`demo-dispatch.yml`](.github/workflows/demo-dispatch.yml): open the **Actions** tab, pick **Dispatch Gallery Demo**, click **Run workflow**, and watch it echo the real-world example repositories this demo is based on.

## Real-world examples

These are real, public repositories found via GitHub code search, each with a workflow that can be started manually from the Actions tab:

| Repository | Workflow file |
| --- | --- |
| [tysoncung/awesome-vibe-coding](https://github.com/tysoncung/awesome-vibe-coding) | `.github/workflows/weekly-trending.yml` |
| [liyupi/github-claw](https://github.com/liyupi/github-claw) | `.github/workflows/ai-daily-digest.yml` |
| [antfu/antfu](https://github.com/antfu/antfu) | `.github/workflows/metrics.yml` |

All three workflows use the `workflow_dispatch` trigger (usually alongside a `schedule` cron), which is what makes the **Run workflow** button appear in the Actions tab.

## How to run the demo

1. Go to the **Actions** tab.
2. Select **Dispatch Gallery Demo** in the left sidebar.
3. Click **Run workflow**, keep `main` selected, and click **Run workflow** again.
4. Watch the steps echo the example repository names above.
