# ayylmao

A [Scoop](https://scoop.sh) bucket for my Windows apps.

```
scoop bucket add ayylmao https://github.com/jkkma/scoop-ayylmao
```

`ayylmao` is only what the bucket is called on your machine — `scoop bucket add`
takes whatever name you type there, and nothing in this repository declares one.

## What is in it

| App | What it is |
| --- | --- |
| [`aerowave`](https://github.com/jkkma/aerowave) | Internet radio player and alarm clock — wakes you to a station or to a random track from a folder |

```
scoop install aerowave
```

## Moved from jkkma/nmkoder

This bucket used to live inside the Nmkoder repository, which worked while it held
one app. Adding it meant cloning that whole source tree — 14 MB of application code
and history to reach a few KB of manifests — and it put a URL ending in `/nmkoder`
in front of anyone installing something else entirely.

The old location still carries a copy of `aerowave`, so nothing breaks if you added
it that way. To move across:

```
scoop bucket rm ayylmao
scoop bucket add ayylmao https://github.com/jkkma/scoop-ayylmao
```

Removing the old one first matters: adding the same bucket twice under two names
is what produces Scoop's `WARN Multiple buckets contain manifest ...` line.
Installed apps are untouched by either command.

## Keeping up to date

`.github/workflows/excavator.yml` runs Scoop's own Excavator every six hours. It
follows each manifest's `checkver`, and where there is a new release it rewrites
the version, URL and hash with `autoupdate` and commits the result, so the bucket
tracks upstream without anyone touching it.

## Licence

The manifests here are MIT, see [LICENSE](LICENSE). The apps they install keep
their own licences, which each manifest names.
