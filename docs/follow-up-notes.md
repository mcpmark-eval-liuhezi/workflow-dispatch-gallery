# Follow-up improvements

Ideas gathered from the real-world `workflow_dispatch` examples used in this demo:

## 1. Add workflow inputs for a more interesting demo

`antfu/antfu`'s `metrics.yml` and `liyupi/github-claw`'s `ai-daily-digest.yml` both keep a `schedule` trigger next to `workflow_dispatch`, so the same workflow can run hands-free *and* on demand. Our demo only has `workflow_dispatch`. Adding a couple of `inputs:` (for example a greeting message or a number of examples to print) would make the "Run workflow" dialog interactive — a much better live moment for the talk, because the audience sees the input form appear on screen.

## 2. Generate an artifact or write a commit so the run leaves something behind

`tysoncung/awesome-vibe-coding`'s `weekly-trending.yml` uses `permissions: contents: write / issues: write` and opens an issue with its findings, and `github-claw` similarly creates a digest issue. Right now our demo run only echoes text and leaves nothing to inspect afterwards. Uploading a small artifact (`actions/upload-artifact@v4`) or opening an issue from the run would show what a run can produce and give the audience something to click on after the run finishes.

## 3. Copy the guardrails the real workflows use

All three examples that pair `workflow_dispatch` with `schedule` implicitly show the "cron + manual fallback" pattern — a scheduled workflow you can also trigger by hand when you don't want to wait for the next window. Follow-ups worth stealing: add a nightly `schedule` to `demo-dispatch.yml` alongside the manual trigger, scope `permissions:` to the minimum needed, and document in the README that `workflow_dispatch` requires the workflow file to exist on the default branch before the "Run workflow" button will appear (the exact gotcha this repo was built to demonstrate).
