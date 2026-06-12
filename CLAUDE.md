# Claude guidance for this repo

## Working style (per philihp)

- Don't end a turn by asking permission to make a reversible change. Push it
  to a feature branch, open a PR, and report what was done. Only block on
  destructive actions or genuinely ambiguous decisions, and when blocking,
  use the interactive AskUserQuestion prompt — never a trailing prose
  question that leaves the session silently idle.

## Project notes

- Publishing uses npm staged publishing (`npm stage publish`), which requires
  npm >= 11.15.0. Node 22 bundles npm 10.x, so CI must upgrade npm first.
- Releases are published to npm via `.github/workflows/publish.yml`, triggered
  on GitHub release publish.
