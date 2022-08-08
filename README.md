# FVSpinDown

Scripts to automatically unlock and eject FileVault volumes so
external drives spin down when not in use.  I have them scheduled via
`launchd` jobs to run pre- and post- SuperDuper! clones, or to mount a
Time Machine volume for a few hours overnight.

In current macOS, apfs-disk requires Command Line Tools for Xcode to be
installed, or another Python 3 distribution.

One version is provided for encrypted Core Storage volumes (`fv`) and
one version for APFS volumes (`apfs-disk`), which may or may not be
encrypted.  Encryption keys are obtained from your keychain — unlock
the volume at least once from Finder and save the key in your
keychain, then run the script once from the command line, choosing to
grant `security` persistent permissions to access the passphrase
(Always Allow).

Core Storage configurations of this type are increasingly unsupported
by Apple as of macOS 10.12.  When launching Disk Utility, you will
see:

> **Unsupported Configuration Detected**
>
> A CoreStorage logical volume group with more than one logical volume
> has been detected. The Disk Utility GUI does not support full
> CoreStorage editing. To use Disk Utility use diskutil to revert to
> single logical volume per logical volume group.

I encourage you to migrate to APFS as soon as is practical.
