# .github

Organization profile and shared community health defaults for the
[HumaiPsy](https://github.com/humaipsy) organization.

This repository holds no application code. It exists because GitHub renders an
organization's overview page from a specific, fixed path in a repository that must be
public and must be named `.github`.

## Layout

| Path | Purpose |
| :--- | :--- |
| `profile/README.md` | The README shown on the [organization overview page](https://github.com/humaipsy). |

## Editing the organization page

Edit `profile/README.md` and push to `main`. The change renders as soon as it is
committed — there is no build, no release and no deployment step.

Two things are easy to get wrong here:

- **Every link must be absolute or point into this repository.** The file is rendered
  on `github.com/humaipsy`, not inside this repository, so a relative path like
  `../ARCHITECTURE.md` resolves to nothing.
- **Nothing else in this repository affects the organization page.** A `README.md` at
  the repository root is what you see at `github.com/humaipsy/.github`; only
  `profile/README.md` is what the organization page shows.

## Not the same thing as the organization description

The one-line bio above the repositories (the 🔬 line) is an organization setting, not
this file — it is edited at **Organization settings → Profile**, not in this repository.
