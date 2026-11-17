# GameDistributionSubmission

Private portal for GameDistribution submissions, published with GitHub Pages. It is its own git repo,
ignored by the BrowserGames repo that contains this folder.

- `index.html`: the welcome page for the GameDistribution QA team. It says the site exists only so
  GameDistribution can review the game, and embeds the game. Keep it free of developer tools.
- `test.html`: the test harness. It embeds a game in an iframe inside a scrolling page, and has manual
  checks for canvas sizes, scrolling, blocked storage and network requests.
- `<Game>/`: a web build of one game, for example `BlockedIn/`. Add each game to `GAMES`
  in `test.html` and to `index.html`.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.

The harness and the game must be on the same origin, so keep every game build in this repo.

## Publish

The `main` branch is the only branch, and GitHub Pages serves it from the root
(Settings > Pages > Deploy from a branch > `main`, `/ (root)`).

To update a game, replace its folder with the new web build, then commit and push.
