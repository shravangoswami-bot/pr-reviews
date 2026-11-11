# PR reviews

Post a public PR URL in the [inbox](https://github.com/shravangoswami-bot/pr-reviews/issues/1).
Only `shravanngoswamii`, `yebai` and `sunxd3` can request reviews.

```text
https://github.com/OWNER/REPO/pull/NUMBER --backend cloud --model sonnet --effort medium
https://github.com/OWNER/REPO/pull/NUMBER --backend vm --model opus --effort high
```

The same flags work with `@shravangoswami-bot review` on a PR.
Cloud with Sonnet and medium effort is the default.
Each PR keeps one cloud session.
Use `--fresh` to replace it.
VM reviews use a fresh Claude Code process on a GitHub-hosted runner.
Both use the owner's Claude subscription.

The configured cloud preset is Sonnet 5.5 with medium effort.
Other cloud choices need a matching [task preset or linked regular session](https://github.com/shravanngoswamii/reviary/blob/main/docs/cloud.md).
VM model and effort are chosen per request.

Inbox comments start immediately, subject to GitHub queuing.
PR mention and reviewer-request checks are scheduled every five minutes.
GitHub can delay scheduled jobs.
Reports and replies state Approve or Hold with reasons.
The bot does not submit formal approvals or run PR code and package tests.

[Sample report](https://shravangoswami-bot.github.io/pr-reviews/examples/dynamicppl-1529/)
[Reviary](https://github.com/shravanngoswamii/reviary)
[Setup and renewal](https://github.com/shravanngoswamii/reviary/blob/main/docs/cloud.md)

Settings and session IDs live in [Actions variables](https://github.com/shravangoswami-bot/pr-reviews/settings/variables/actions).
Credentials stay in this repository's Actions secrets.
Report comments stay local until exported.
