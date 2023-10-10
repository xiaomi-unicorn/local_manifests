### Xiaomi 12S Pro Pixel Experience Plus 13

1. repo init -u https://github.com/PixelExperience/manifest -b thirteen-plus --git-lfs
2. git clone https://github.com/xiaomi-unicorn/local_manifests .repo/local_manifests
3. repo sync
4. cd patches && ./apply.sh
5. . build/envsetup.sh
6. lunch aosp_unicorn-userdebug
7. mka bacon

### 非常感谢
- [kindle4jerry](https://github.com/kindle4jerry/device_xiaomi_diting) Redmi K50 Ultra diting
- [VoidUI-Andromeda](https://github.com/VoidUI-Andromeda/device_xiaomi_mondrian) Redmi-K60 mondrian
- [BirdZhang](https://github.com/0312birdzhang)
- [星になる](https://github.com/MomoYuuki)
