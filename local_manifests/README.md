# TWRP Recovery Project

### How to build ###

```bash
# Create dirs
$ mkdir twrp ; cd twrp

# Init repo
$ repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11

# Clone my local repo
$ git clone https://github.com/EinKara/android_manifest_google_bluejay.git -b twrp-13 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh
$ lunch twrp_bluejay-eng
$ make bootimage
```

## Credits
2022 @notokay3272
