# ayylmao

A [Scoop](https://scoop.sh) bucket for my Windows apps.

## Install

Add the bucket in PowerShell.

```powershell
scoop bucket add ayylmao https://github.com/jkkma/scoop-ayylmao
```

Run the install command for the app you want.

| App | Install command |
| --- | --- |
| [Aerowave](https://github.com/jkkma/aerowave), an internet radio player and alarm clock that can wake you to a station or a local track | `scoop install ayylmao/aerowave` |
| [Jesses](https://github.com/jkkma/jesses), a desktop app for media encoding, muxing, and analysis | `scoop install ayylmao/jesses` |

Both packages ship Windows x64 builds and require the Microsoft Edge WebView2 Runtime. Aerowave keeps its settings in `data`, and Jesses keeps its app data in `jesses-data`. Scoop preserves both directories across updates.

## Update

Run `scoop update` to refresh the bucket, then run `scoop update aerowave` or `scoop update jesses` for the app you installed. The Excavator workflow is scheduled to check upstream releases every six hours. When it finds a newer matching build, it updates the version, download URL, and hash.

## License

The manifests are MIT-licensed. Each app uses the license listed in its manifest. [MIT license](LICENSE)
