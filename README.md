#[TWRP Recovery Project but for other  commands--ncproc doesnt work on any other platforms except linux. Also for some of these commands you need to insatll them with brew and you need cli command line (comes with android studio) for lunch command and envsetup.sh]

### How to build for MAC OSX###

```bash
# Create dirs
$ mkdir ~/downloads/twrp ; cd ~/downloads/twrp

# Init repo
$ repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11

# Clone my local repo
$ git clone https://github.com/EinKara/android_manifest_google_bluejay.git -b twrp-13 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`sysctl -n hw.ncpu`

# Build
$ . build/envsetup.sh
$ lunch twrp_bluejay-eng
$ make bootimage
```

## Credits
2022 @notokay3272

##for windows I think its like this:

mkdir ~/downloads/twrp
cd ~/downloads/twrp


repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11

git clone https://github.com/EinKara/android_manifest_google_bluejay.git -b twrp-13 .repo/local_manifests

repo sync

. build/envsetup.sh
lunch twrp_bluejay-eng
make bootimage


##lmk if that works for windows cuz I dont have my pc rn

