# Benjamin Predictions

A zero-cost, static live dashboard for Benjamin's prediction pool, published with GitHub Pages.

## Live scoring

Until Benjamin arrives, every browser recalculates **Date** and **Time** against the current time in `Australia/Perth` every minute. Predictions in both the past and the future are scored against that same current moment.

After he arrives, open `index.html` and replace:

```js
const officialArrival = null;
```

with the official data:

```js
const officialArrival = {
  date: "2026-10-26",
  time: "13:18",
  weight: 3920,
  length: 51,
  hair: "Castanho",
  eyes: "Castanho",
  resemblance: "Pai"
};
```

Commit that change. The dashboard automatically switches to the final leaderboard and awards all 100 available points.

## Publishing

A GitHub Pages deployment workflow is included in `.github/workflows/deploy-pages.yml`.

In the repository, go to **Settings → Pages → Build and deployment → Source**, choose **GitHub Actions** once. Every push to `main` will then publish the site at the GitHub Pages URL shown there.
