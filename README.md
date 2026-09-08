# homebrew-jknife

Homebrew tap for the [mhus-jknife](https://github.com/mhus/mhus-jknife) cli tools —
small Java helper tools compiled as GraalVM native binaries. Documentation:
<https://jknife.mhus.de>

## Install

```shell
brew tap mhus/jknife
brew install jregex
brew install jbase64
```

## Formulas

| Formula    | Tool                                        |
| ---------- | ------------------------------------------- |
| `jregex`   | Java regex helper (match, find, replace)    |
| `jbase64`  | Base64 encode/decode                        |

## Maintenance

The formulas in `Formula/` are **generated** by
[`scripts/gen-formula.sh`](https://github.com/mhus/mhus-jknife/blob/main/scripts/gen-formula.sh)
in the main repository — do not edit them by hand. New release process:

1. release `mhus/mhus-jknife` (tag `vX.Y.Z` triggers the native build workflow)
2. `./scripts/gen-formula.sh X.Y.Z` (in the main repo)
3. copy `dist/*.rb` into `Formula/` here, commit & push
