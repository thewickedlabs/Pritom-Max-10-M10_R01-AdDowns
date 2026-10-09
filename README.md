# M10_R01 AdDowns

Removes the preinstalled ADUPS/incar firmware-update service.

A KernelSU Next module for the **Pritom Max 10 (M10_R01)**. Companion to the unlock/root guide:
[Pritom-Max-10-M10_R01-Unlock](https://github.com/thewickedlabs/Pritom-Max-10-M10_R01-Unlock).

The stock updater `FotaUpdate` (`com.incar.update`, branded "incar"/INCARTECH) is an **ADUPS** FOTA
client: it talks to `fota5p.adups.com` / `fota5p.adups.cn`, reports the device to those servers, and
can install software silently in the background. ADUPS is the same FOTA vendor that was caught
exfiltrating personal data from budget Android devices in 2016. This module hides the app
systemlessly, so it isn't loaded at boot.

Nothing on the real partitions is touched — the overlay is applied at boot and the stock app stays on
the device untouched.

## Requirements

- Pritom Max 10 (M10_R01)
- Rooted with KernelSU Next

The installer stops without changing anything if either is missing.

## Install

1. Download [`Pritom-Max-10-M10_R01-AdDowns.zip`](https://github.com/thewickedlabs/Pritom-Max-10-M10_R01-AdDowns/releases/latest/download/Pritom-Max-10-M10_R01-AdDowns.zip) (latest release).
2. KernelSU Next → Modules → Install from storage → select the zip.
3. Reboot.

## Uninstall

Disable or remove the module and reboot. The updater comes back untouched.

## License

[WTFPL](LICENSE). Use at your own risk; no warranty and no liability for anything this does to your device.

---

Wicked Labs · https://www.cyberspace7.org
