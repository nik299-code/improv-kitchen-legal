# Improv Kitchen — legal pages

Public hosting for the app's Privacy Policy and Terms of Use, because
App Store Connect requires a **publicly reachable URL** for the privacy
policy (App Review Guideline 5.1.1(i) asks for it both in the store
metadata and inside the app).

## Do not edit these files here

They are copies. The source of truth is `public/privacy.html` and
`public/terms.html` in the app repository, which is also what the app
**bundles and ships** — the in-app links point at the bundled copy, not
at this site, so that the terms someone accepted cannot change out from
under their acknowledgment.

Two copies of a legal document that disagree with each other is worse
than one, so update them at the source and run:

```
node scripts/publish-legal.mjs
```

from the app repository. That pushes the current files here through the
GitHub API and reports if anything drifted.
