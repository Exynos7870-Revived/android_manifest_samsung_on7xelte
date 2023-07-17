# LineageOS-19.1

### How to build ###

```bash
# Create dirs
$ mkdir LineageOS && cd LineageOS

# Init repo
$ repo init -u https://github.com/LineageOS-UL/android.git -b lineage-19.1

# Clone my local repo
$ git clone https://github.com/Exynos7870-Revived/android_manifest_samsung_on7xelte.git -b LineageOS-19.1 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ . build/envsetup.sh && lunch lineage_onx7elte-userdebug && mka clean && mka api-stubs-docs && mka hiddenapi-lists-docs && mka system-api-stubs-docs && mka test-api-stubs-docs && mka bacon -j`nproc`
```

## Credits
2019 @Astrako<br>
2023 @Batuhantrkgl

