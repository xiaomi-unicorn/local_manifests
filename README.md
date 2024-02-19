### Xiaomi 12S Pro LineageOS 20

1. repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs --no-clone-bundle
2. git clone https://github.com/xiaomi-unicorn/local_manifests .repo/local_manifests -b lineage-20.0
3. repo sync --no-clone-bundle
4. . build/envsetup.sh
5. lunch lineage_unicorn-userdebug
6. mka bacon

### 由arian大佬适配
1. https://github.com/arian-ota/changelog
2. https://github.com/arian-ota/ota
3. https://github.com/cupid-development
