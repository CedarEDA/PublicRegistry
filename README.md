# Cedar public registry

Add this registry to your local Julia install with:

```
pkg> registry add https://github.com/CedarEDA/PublicRegistry
```

Note that if this is the first time you're performing a package operation, you may also
have to manually add the general registry (it is added automatically if no registry
is installed, but if you add the Cedar registry before performing any other package
operation, you may not get the auto-install):

```
pkg> registry add General
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
