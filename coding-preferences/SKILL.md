---
name: coding-preferences
description: "Apply the user's coding preferences when editing code or comments, or writing commit messages."
---

# Coding Preferences

- **Diff scope:** Keep Git diffs minimal and easy to review; avoid unrelated changes.
- **Comments:** Help future contributors and agents prevent regressions by explaining non-obvious rationale and constraints that changes must preserve. Distinguish deliberate constraints from provisional choices. Do not restate code behavior.
- **Commits:** Keep commits focused and easy to review. Follow the repository's commit message format and conventions. Commit messages should state why the change is needed because the diff already shows what changed.
- **File moves:** For migrations requiring unchanged file moves, commit import, documentation, and definition-extraction changes first. Move all selected files together in a later commit, byte-identical to their parent versions. Update module declarations, manifests, and compatibility re-exports only in other files. Keep every commit buildable and preserve consumer paths with re-exports.

## Language rules

Load only the relevant rules.

- [Rust preferences](references/rust.md).
