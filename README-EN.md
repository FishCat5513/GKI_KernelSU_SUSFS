# GKI KernelSU SUSFS

Automated GKI kernel builds via GitHub Actions ([Chinese](README.md)/English).

> Not supported on OnePlus ColorOS 14/15. You may need to wipe data after flashing.
>
> SUKISU builds: `stable` uses the `builtin` branch (high bootloop risk); `dev` uses the `tmp-builtin` branch (more stable, but untouched for two weeks).

Attempted to build a GKI kernel with [hymo](https://github.com/Anatdx/hymo) mount meta-module integration, but the project currently only supports 6.6, so it is not fully merged into the main branch.
Reference release: [hymo+gki](https://github.com/zzh20188/GKI_KernelSU_SUSFS/releases/tag/v2.0.0-r24)

## KernelSU beyond SUKISU?
Nearly all builds no longer use SUSFS, or even GKI, and compatibility is hard to guarantee.
Therefore this project uses GKI without SUSFS.

## Documentation and Guides

Detailed instructions are organized in the bilingual [GitHub Wiki](https://github.com/zzh20188/GKI_KernelSU_SUSFS/wiki); please check there first.

[Changelog: doc/CHANGELOG-EN.md](doc/CHANGELOG-EN.md)

The wiki covers downloading and flashing, bootloop recovery, bug reporting, tips, KSU manager and SUSFS modules, kernel build time, emergency rescue, and kernel version compatibility.

## After installing KernelSU ...
> This section keeps a list of post-installation usage ideas, practical apps, and modules. All are official channels; order does not imply ranking.
### Modules
1. LSPosed-Irena
    * [LSPosed-Irena repo](https://github.com/re-zero001/LSPosed-Irena)
    * [LSPosed-Irena channel](https://t.me/lsposed_irena)
2. Zygisk Next/TrickyStore
    * [Zygisk Next repo](https://github.com/Dr-TSNG/ZygiskNext)
    * [TrickyStore repo](https://github.com/5ec1cff/TrickyStore)
    * [Zygisk Next/TrickyStore shared channel](https://t.me/real5ec1cff)
### To be expanded...
