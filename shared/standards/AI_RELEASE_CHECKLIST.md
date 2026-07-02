# AI Release Checklist

Use this checklist before any AI reports that a game is published.

## Required flow

1. Create or update the playable game folder.
2. Update `games.json`.
3. Update the root `index.html` homepage card list.
4. Update `creators/index.json`.
5. Update `creators/index.html`.
6. Update the contributor workspace changelog and TODO.
7. Commit the changes.
8. Push the branch.
9. Open a pull request to `main`.
10. Merge the pull request into `main`.
11. Wait for the GitHub Pages deployment to complete successfully.
12. Verify the public hub and game URLs.

## Required public checks

After the merge, verify:

```text
https://jaronkbragg7337.github.io/Free-Game-Hub/
https://jaronkbragg7337.github.io/Free-Game-Hub/games/<slug>/
```

The hub must visibly list the game, and the game route must load from GitHub Pages.

## Do not stop early

A game is not fully published when it only exists on a branch or pull request.

GitHub Pages publishes from:

```text
main / root
```

If the pull request has not been merged to `main`, the public site will still show the previous game list.
