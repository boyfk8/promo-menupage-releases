# Promo Menupage Automation — Install & Update

This is the **single official repository** for all downloadable MENUPAGE installers, updates and Adobe Premiere UXP plugin packages. Source code, tests and release builders live in the separate private [promo-menupage-automation](https://github.com/boyfk8/promo-menupage-automation) repository.

## Latest stable: 0.5.54

[Open the v0.5.54 release (7 downloadable assets)](https://github.com/boyfk8/promo-menupage-releases/releases/tag/v0.5.54)

| Use case | Recommended download | Run after extracting |
| --- | --- | --- |
| New Windows workstation | `PromoMenupageAutomation_Windows_0.5.54_PublicAllInOne_r1.zip` | `SETUP_MENUPAGE.bat` |
| Existing Windows workstation | `PromoMenupageAutomation_WindowsUpdate_0.5.54_PublicAllInOne_r1.zip` | `UPDATE.bat` |
| New macOS workstation (test candidate) | `PromoMenupageAutomation_macOS_0.5.54_PublicAllInOne_r1_candidate.zip` | `SETUP_MACOS.command` |

The release also contains the credential-free CloudInstall ZIP, standard Update ZIP, macOS source candidate and matching Premiere UXP `.ccx` package.

Windows users must finish or cancel active render jobs and close Premiere before updating. Premiere and Adobe Creative Cloud are prerequisites.

## Automatic cloud updates

The MENUPAGE Windows app checks the [stable.json update feed](https://raw.githubusercontent.com/boyfk8/promo-menupage-releases/main/stable.json) in this repository. The feed points at the **public AllInOne installer and updater** from the current stable release. Files are uploaded and verified before `stable.json` is changed.

The source repository is **not** a deployment destination. Historical binaries previously uploaded there are legacy and are not used for new releases or in-app update discovery.

## Google Docs team connection

This repository is public and must not expose shared Google team relay keys, private LINE credentials, user settings or OAuth tokens.

- **Existing workstations:** a regular Windows update preserves their locally provisioned Google relay configuration.
- **New workstations:** obtain the authorized relay endpoint and team key securely from your administrator, outside public GitHub. After installation run `ACTIVATE_TEAM_GOOGLE.bat` (Windows) or `ACTIVATE_TEAM_GOOGLE.command` (macOS) to validate and save the binding locally. Restart the app after activation.
- Do not paste or attach access keys or binding files to issues, public releases or support logs.

The public packages cannot automatically provide access to a private team Google document. Any optional own-account OAuth fallback configuration must likewise be provisioned privately. Word/PDF import remains available.

The macOS package is a **candidate** until native installation, Premiere/MXF rendering and human visual/audio acceptance are completed. Older releases remain available for compatibility and rollback.
