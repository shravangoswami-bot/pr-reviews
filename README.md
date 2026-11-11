# PR reviews

Post a public PR URL in the [inbox](https://github.com/shravangoswami-bot/pr-reviews/issues/1).
Only `shravanngoswamii`, `yebai` and `sunxd3` can request reviews.

```text
https://github.com/OWNER/REPO/pull/NUMBER
@shravangoswami-bot review
@shravangoswami-bot review --fresh
```

Reviews use Claude cloud with Sonnet 5.5 and medium effort.
Each PR keeps one session.
Use `--fresh` to replace it.
Other model and effort pairs need a matching [cloud task](https://github.com/shravanngoswamii/reviary/blob/main/docs/cloud.md#create-sessions).

Inbox comments start immediately, subject to GitHub queuing.
Mentions and reviewer requests are checked every 30 minutes.
GitHub Actions checks and publishes the report.
PR code and package tests are not run.

[Sample report](https://shravangoswami-bot.github.io/pr-reviews/examples/dynamicppl-1529/)
[Reviary](https://github.com/shravanngoswamii/reviary)
[Setup and renewal](https://github.com/shravanngoswamii/reviary/blob/main/docs/cloud.md)

Settings and session IDs live in [Actions variables](https://github.com/shravangoswami-bot/pr-reviews/settings/variables/actions).
Credentials stay in this repository's Actions secrets.
Report comments stay local until exported.
