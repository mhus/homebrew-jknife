# homebrew-jknife

Homebrew tap for the [jknife](https://github.com/mhus/jknife) cli tools —
small Java helper tools compiled as GraalVM native binaries. Documentation:
<https://jknife.mhus.de>

## Install

```shell
brew tap mhus/jknife
brew install jregex jbase64 juuid jtime jperiod jjson jyaml jxpath jllm jsec
```

## Formulas

| Formula    | Tool                                                            |
| ---------- | --------------------------------------------------------------- |
| `jregex`   | Java regex helper (match, find, replace)                        |
| `jbase64`  | Base64 encode/decode                                             |
| `juuid`    | UUID generator and parser (v4, v7)                              |
| `jtime`    | Timestamp converter (epoch, epoch-millis, ISO-8601)            |
| `jperiod`  | Period/duration converter and parser                            |
| `jjson`    | JSON helper (validate, pretty, compact, get)                    |
| `jyaml`    | YAML helper (validate, tojson)                                  |
| `jxpath`   | XML xpath helper (select, exists)                              |
| `jllm`     | LLM tool family (ask, stream, request, models; openai, ollama) |
| `jsec`     | Security tool family (hash, keys, encrypt/decrypt, sign/verify) |

## Maintenance

The formulas in `Formula/` are **generated** by
[`scripts/gen-formula.sh`](https://github.com/mhus/jknife/blob/main/scripts/gen-formula.sh)
in the main repository — do not edit them by hand. New release process:

1. release `mhus/jknife` (tag `vX.Y.Z` triggers the native build workflow)
2. `./scripts/gen-formula.sh X.Y.Z` (in the main repo)
3. copy `dist/*.rb` into `Formula/` here, commit & push
