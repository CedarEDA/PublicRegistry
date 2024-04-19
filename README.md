# Cedar public registry

Add this registry to your local Julia install with:

```
pkg> registry add git@github.com:CedarEDA/PublicRegistry
```

## Registering a package

This requires `LocalRegistry` to be installed.

1. Bump version number in `Project.toml`
2. push that to `#main` of that package
3. open julia with `--project=` set the folder of what you want to register
4. `using LocalRegistry; register()`
    - (have to give registry name if you have more than general and CedarEDA).
    - This will push to #main on the CedarEDA registry
5. manually tag a release in github.
   - Tagbot isn't set up for CedarEDA registry.
   - You can use github to generate release notes.
