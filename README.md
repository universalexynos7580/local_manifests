# Lineage OS Android 13.0

### How to build ###

```bash
# Create dirs
$ mkdir arrow && cd lineage

# Init repo
$ repo init -u https://github.com/LineageOS-UL/android.git -b lineage-20.0
# (already patched for ultra legacy devices)

# Clone my local repo
$ git clone https://github.com/universalexynos7580/local_manifests.git -b lineage-20 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc` -v

# Build example: replace "a3xelte" device codename with "your_device_codename"
$ . build/envsetup.sh && brunch lineage_a3xelte-userdebug
```
