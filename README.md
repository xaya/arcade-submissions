# Submit a game to Xaya Arcade

Request a new listing or an update by opening a **Game submission** issue.
You need a GitHub account. You do not need to run an arcade server or submit to
a public playground.

## What to send

- **Your game repository and full commit hash.** That commit must contain the
  frontend source, rules source, compiled `rules.wasm`, its SHA-256 file, and
  instructions to build and test the game. One commit identifies both the
  frontend and rules. If the repository is private, arrange reviewer access.
- **Game details.** Title, description, controls, player counts, proposed slug,
  game type (`GAME_KEY` in the template), and rules configuration (`cfgSuffix`,
  or `none`). Say whether you want WCHI wagering.
- **Test results.** Include the rules rebuild check, rules tests, frontend tests
  and deterministic replay results. Say which player counts and devices you
  tested, and mention anything you could not test.

We build the frontend from your commit for the target arcade. You do not need to
upload a production frontend bundle or supply its hash. Keep the compiled WASM
and its hash in the repository so we can reproduce and verify the rules.

## Submit

1. Commit and push the version you tested. Use a full commit hash, not a branch name.
2. [Open the Game submission form](https://github.com/xaya/arcade-submissions/issues/new?template=game-submission.yml), fill it in, and click **Submit new issue**.
3. Follow that issue for review questions and the result.

We review the source, rebuild the game and test it on a disposable playground.
Approved games are listed on the public arcade. Wagering is enabled separately
if requested and approved. Opening an issue does not publish a game automatically.

For an update, use the same form with the new commit, link the earlier issue and
summarize what changed. We review and schedule the update before deployment.
