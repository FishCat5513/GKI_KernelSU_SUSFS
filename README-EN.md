<div align="center">

# GKI KernelSU SUSFS

**Happy Lunar New Year! 🧨🧧**

Automated GKI kernel builds with KernelSU + SUSFS.

[![GitHub Release](https://img.shields.io/github/v/release/zzh20188/GKI_KernelSU_SUSFS?style=for-the-badge&logo=android&color=green)](https://github.com/zzh20188/GKI_KernelSU_SUSFS/releases)
[![KernelSU](https://img.shields.io/badge/KernelSU-Supported-green)](https://kernelsu.org/)
[![SUSFS](https://img.shields.io/badge/SUSFS-Integrated-orange)](https://gitlab.com/simonpunk/susfs4ksu)

English | [**简体中文**](README.md)

</div>

---

## Quick Links
- Docs: <https://github.com/zzh20188/GKI_KernelSU_SUSFS/wiki>
- Downloads: <https://github.com/zzh20188/GKI_KernelSU_SUSFS/releases>
- Changelog: [`doc/CHANGELOG-EN.md`](doc/CHANGELOG-EN.md)

## Compatibility Notice
> OnePlus ColorOS 14/15 is currently not supported. A data wipe may be required after flashing.

## Special Editions
- `hymo+gki` (6.6): <https://github.com/zzh20188/GKI_KernelSU_SUSFS/releases/tag/v2.0.0-r24>
- `resukisu+gki`: <https://github.com/zzh20188/GKI_KernelSU_SUSFS/releases/tag/v2.0.0-r26>

> Prebuilt releases already include the zero-width fix. You can also use the [Unicode zero-width fix module](https://t.me/real5ec1cff/268).

## Common Build Failure Cause
Even during holiday rush, this is still the #1 issue: SukiSU and SUSFS update out of sync.

- SukiSU builtin: <https://github.com/SukiSU-Ultra/SukiSU-Ultra/tree/builtin>
- SUSFS 6.1 branch: <https://gitlab.com/simonpunk/susfs4ksu/-/tree/gki-android14-6.1?ref_type=heads>

What to do: wait for upstream adaptation, or pin working commits manually.

## Custom Commit Pinning (Recommended)
Use [`config/config`](config/config) to pin SUSFS / SukiSU commits when upstream is temporarily incompatible.

```ini
custom=true

gki-android12-5.10=
gki-android13-5.15=
gki-android14-6.1=
gki-android15-6.6=

sukisu=
```

- Empty value = use latest commit of that branch
- SUSFS commits: <https://gitlab.com/simonpunk/susfs4ksu>
- SukiSU commits: <https://github.com/SukiSU-Ultra/SukiSU-Ultra/commits/builtin/>

## Spoof `/proc/config.gz` (Stock Config)
This is an advanced trick and requires no workflow toggle.
Build now auto-detects `config/stock_defconfig`: if present, it is applied; if absent, it is skipped.

1. Make sure your device is running stock ROM + stock kernel.
2. Obtain `/proc/config.gz` from your device (phone-side or PC-side workflow both work).
3. Decompress it, rename it to `stock_defconfig`, upload it to `config/` in your repo, and commit (can be done directly on phone).

During build, workflow will automatically:
- copy it to `$KERNEL_ROOT/common/arch/arm64/configs/stock_defconfig`
- switch Makefile `config_data` rule from `$(KCONFIG_CONFIG)` to `stock_defconfig`
- make `/proc/config.gz` in the built kernel closer to your stock kernel config

## Recommended Modules
- LSPosed-Irena: <https://github.com/re-zero001/LSPosed-Irena>
- Zygisk Next: <https://github.com/Dr-TSNG/ZygiskNext>
- TrickyStore: <https://github.com/5ec1cff/TrickyStore>

---

<div align="center">

Wishing you a smooth year: one-pass builds, clean boots, green logs. 🎉

⭐ If this project helps, please give it a Star.

</div>
