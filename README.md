# Pixel Experience #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/belowzeroiq/manifest.git -b thirteen-plus --depth=1 --git-lfs
```

```bash

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -j$(nproc --all) | tee log.txt
```
