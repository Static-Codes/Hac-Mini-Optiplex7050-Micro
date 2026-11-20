# Hac Mini Setup
* This repository is a fork of Coopydood's [OpenCore-OptiPlex7050-Micro](https://github.com/Coopydood/OpenCore-OptiPlex7050-Micro) with a few minor modifications to the config.plist file. All changes are related to installation troubleshooting. All hardware in this setup are identical to the provided specs used by Coopydood.

* [`INSTALLATION`](./INSTALLATION) contains the EFI boot files required during installation

* [`CONFIGURED`](./CONFIGURED) contains the EFI boot files for every-day usage.

## Changes 

- HideAuxiliary - `<true/>` -> `<false/>`
    - Explanation: Allows autillary entries from the picker menu.
    - Docs: https://dortania.github.io/docs/latest/Configuration.html#:~:text=HideAuxiliary,-Type

- DmgLoading - `Signed` -> `Any`
    - Explanation: any DMG images will mount as normal filesystems. The Any policy is strongly discouraged and will result in boot failures when Apple Secure Boot is active.
    - Docs: https://dortania.github.io/docs/latest/Configuration.html#:~:text=Any,-%E2%80%94%20any

- SecureBootModel - `j174` -> `Disabled`
    - Explanation: No model, Secure Boot will be disabled. 
    - Docs: https://dortania.github.io/docs/latest/Configuration.html#:~:text=Disabled,-%E2%80%94%20No
