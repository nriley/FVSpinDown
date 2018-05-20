# FVSpinDown
Scripts to automatically unlock and eject FileVault volumes so external drives spin down when not in use.  I have it scheduled via `launchd` jobs to run pre- and post- SuperDuper! clones.

One version is provided for encrypted Core Storage volumes (`fv`) and one version for APFS (`apfs-disk`, which currently only handles ejecting).

Core Storage configurations of this type are increasingly unsupported by Apple as of macOS 10.12.  When launching Disk Utility, you will see:

> **Unsupported Configuration Detected**
>
> A CoreStorage logical volume group with more than one logical volume has been detected. The Disk Utility GUI does not support full CoreStorage editing. To use Disk Utility use diskutil to revert to single logical volume per logical volume group.

I encourage you to migrate to APFS as soon as is practical.
