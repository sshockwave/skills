# Rust Preferences

- Use `#[expect(lint_name)]` instead of `#[allow(lint_name)]` for intentional lint suppressions.
- Start module-level `use` paths with `::`, `crate`, `self`, or `super` to make their origin unambiguous.
- Prefer concrete parameter types over conversion-trait bounds such as `Into` or `AsRef` to avoid unnecessary monomorphization and keep caller conversions explicit.
- Prefer branded types (newtypes) to encode validation guarantees and distinguish domain concepts.
