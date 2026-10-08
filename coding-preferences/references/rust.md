# Rust Preferences

- Use `#[expect(lint_name)]` instead of `#[allow(lint_name)]` for intentional lint suppressions.
- Start module-level `use` paths with `::`, `crate`, `self`, or `super` to make their origin unambiguous.
- Prefer concrete parameter types over conversion-trait bounds such as `Into` or `AsRef` to avoid unnecessary monomorphization and keep caller conversions explicit.
- Prefer branded types (newtypes) to encode validation guarantees and distinguish domain concepts.
- Trait policies:
    - Create traits only for well-established contracts, mocking external APIs, or structs whose generic parameters are too complex to repeat. For the last case, use `Deref` to expose the struct's methods without redeclaring them on the trait:

        ```rust
        struct ComplexType<T>(T);
        trait ComplexTypeRef: Deref<Target = ComplexType<Self::T>>
        {
            type T;
        }
        impl<T, U> ComplexTypeRef for U
        where
            U: Deref<Target = ComplexType<T>>
        {
            type T = T;
        }
        ```

        Adjust the trait bounds as needed.

    - Do not create traits or generics for rapidly changing domain logic or to mock same-crate code; test production behavior as much as possible.
- For async traits that require `Send`, use `impl Future<Output = ReturnType> + Send` in trait definitions and `async fn` in their implementations.
