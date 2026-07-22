# scoop-bucket

A [Scoop](https://scoop.sh) bucket for **[kache](https://github.com/kunobi-ninja/kache)** — a content-addressed, zero-copy build cache for Rust, C/C++ and more.

## Install

```powershell
scoop bucket add kunobi https://github.com/kunobi-ninja/scoop-bucket

# Stable
scoop install kunobi/kache

# Unstable (release-candidate / pre-release channel)
scoop install kunobi/kache-unstable
```

The binaries are self-contained (statically linked, no Visual C++ Redistributable required) and are published for both `x64` and `arm64` Windows.

## Channels

`kache` (stable) and `kache-unstable` (pre-release) both provide a `kache` command. If you have both installed, Scoop's shim points at whichever you `scoop reset` last:

```powershell
scoop reset kache-unstable   # make `kache` run the unstable build
scoop reset kache            # switch back to stable
```

## Maintenance

Manifests auto-update from kache's GitHub Releases via the [Excavator](.github/workflows/excavator.yml) workflow (`checkver` + `autoupdate`, hashes read from the release `.sha256` sidecars). This bucket is created from [ScoopInstaller/BucketTemplate](https://github.com/ScoopInstaller/BucketTemplate).
