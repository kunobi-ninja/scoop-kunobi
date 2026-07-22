# scoop-bucket

The [Scoop](https://scoop.sh) bucket for [Kunobi Ninja](https://github.com/kunobi-ninja) CLIs:

- **[kache](https://github.com/kunobi-ninja/kache)** — content-addressed, zero-copy build cache for Rust, C/C++ and more.
- **[kobe](https://github.com/kunobi-ninja/kobe)** — CLI for pools of pre-warmed Kubernetes virtual clusters.

## Install

```powershell
scoop bucket add kunobi https://github.com/kunobi-ninja/scoop-kunobi

# kache
scoop install kunobi/kache            # stable
scoop install kunobi/kache-unstable   # pre-release channel

# kobe
scoop install kunobi/kobe            # stable
scoop install kunobi/kobe-unstable   # pre-release channel
```

The binaries are published for both `x64` and `arm64` Windows.

## Channels

`kache` (stable) and `kache-unstable` (pre-release) both provide a `kache` command. If you have both installed, Scoop's shim points at whichever you `scoop reset` last:

```powershell
scoop reset kache-unstable   # make `kache` run the unstable build
scoop reset kache            # switch back to stable
```

## Maintenance

Manifests auto-update from kache's GitHub Releases via the [Excavator](.github/workflows/excavator.yml) workflow (`checkver` + `autoupdate`, hashes read from the release `.sha256` sidecars). This bucket is created from [ScoopInstaller/BucketTemplate](https://github.com/ScoopInstaller/BucketTemplate).
