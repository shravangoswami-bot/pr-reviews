# PR reviews

Post a public PR URL in the [inbox](https://github.com/shravangoswami-bot/pr-reviews/issues/1).
Only `shravanngoswamii`, `yebai` and `sunxd3` can request reviews.

Append either option to the URL, or use `@shravangoswami-bot review` on a PR:

| Model | Effort | Mention command |
| --- | --- | --- |
| Sonnet | Medium | `@shravangoswami-bot review --model sonnet --effort medium` |
| Sonnet | High | `@shravangoswami-bot review --model sonnet --effort high` |
| Opus | High | `@shravangoswami-bot review --model opus --effort high` |
| Opus | Extra high | `@shravangoswami-bot review --model opus --effort xhigh` |
| Opus | Max | `@shravangoswami-bot review --model opus --effort max` |

Without options, reviews use Sonnet with medium effort.
Higher effort can use more subscription allowance.
Mentions and reviewer requests are polled every 30 minutes.
Inbox comments start a workflow immediately, subject to GitHub queuing.

[Sample report](https://shravangoswami-bot.github.io/pr-reviews/examples/dynamicppl-1529/) · [Reviary](https://github.com/shravanngoswamii/reviary) · [Options](https://github.com/shravanngoswamii/reviary/blob/main/docs/bot.md#review-options)

Settings live in the `REVIARY_CONFIG` [Actions variable](https://github.com/shravangoswami-bot/pr-reviews/settings/variables/actions).
Credentials stay in this repository's Actions secrets.
HTML comments stay local until exported.
