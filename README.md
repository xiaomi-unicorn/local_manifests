# Xiaomi 12S Pro LineageOS 20

1. repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs --no-clone-bundle
2. git clone https://github.com/xiaomi-unicorn/local_manifests .repo/local_manifests -b lineage-20.0
3. repo sync --no-clone-bundle
4. . build/envsetup.sh
5. lunch lineage_unicorn-userdebug
6. mka bacon

# 由arian大佬适配
1. https://github.com/arian-ota/changelog
2. https://github.com/arian-ota/ota
3. https://github.com/cupid-development

# 提交记录整理
## unicorn: Changelog update 2024-02-14
### device/qcom/sepolicy
2fa70a47 Revert "sepolicy:qcc: switch to platform app" [Arian]
```
lineage-20分支再还原1个提交
sepolicy:qcc: switch to platform app 是LOS中比较旧的记录
```
### device/xiaomi/sm8450-common
4400652b4 sm8450-common: Reserve osme space on system partitions [Arian]
```
https://github.com/cupid-development/android_device_xiaomi_sm8450-common/commit/4400652b4
This commit does not belong to any branch on this repository, and may belong to a fork outside of the repository.
无法检出
https://github.com/cupid-development/android_device_xiaomi_sm8450-common/commit/ab80138efa270b1eab05ea496c3f614ba677ec7e 是lineage-21的历史提交记录
 + 3个提交
https://github.com/cupid-development/android_device_xiaomi_sm8450-common/commit/9d120db44b3dee6646ef2f0dca786c689471555c
https://github.com/cupid-development/android_device_xiaomi_sm8450-common/commit/584052d92bf90b11aae55b0ee4ba04a6ca57c067
https://github.com/cupid-development/android_device_xiaomi_sm8450-common/commit/4400652b44b3f61ab809e8c65179efa9296a4ef8
```

### kernel/xiaomi/sm8450   还原了4个提交
eb7dee464abe input: touchscreen: xiaomi: Implement touch_thp_mem_notify [Arian]
```
mondrian分支还原几个提交
====================
     2024-02-14    
====================
* kernel/xiaomi/sm8450
665ab11365a5 Revert "input: touchsreen: xiaomi: Import updated header from M11" [Arian]
e4244c1ac5a5 Revert "[WIP] input: touchscreen: xiaomi: Reverse from stock module" [Arian]
72367f2d3b08 Revert "remove verbose debug logging" [Arian]
eebc8084eb38 Revert "fixup! [WIP] input: touchscreen: xiaomi: Reverse from stock module" [Arian]
====================
     2024-02-08    
====================
* kernel/xiaomi/sm8450
f62256aee5e9 fixup! [WIP] input: touchscreen: xiaomi: Reverse from stock module [Arian]
314174d8d180 remove verbose debug logging [Levi Zim]
0cc3a287d0ee [WIP] input: touchscreen: xiaomi: Reverse from stock module [kxxt]
1edc158c09a4 input: touchsreen: xiaomi: Import updated header from M11 [Arian]
eb7dee464abe input: touchscreen: xiaomi: Implement touch_thp_mem_notify [Arian]
377143da7db9 input: touchscreen: xiaomi: Implement touch_thp_film [Arian]
0dd3f538a308 input: touchscreen: xiaomi: Implement palm_sensor_data [Arian]
e1d6e7415e4a Revert "input: touchscreen: xiaomi: Change enable_touch_raw to work with int" [Arian]
```
## unicorn: Changelog update 2024-01-24

### kernel/xiaomi/sm8450-devicetrees
66d69b8e2342 partially revert 53c7aa6cf67e067538baa3bf5e1e84f42178cfee to match unicorn [Arian]
```
https://github.com/cupid-development/android_kernel_xiaomi_sm8450-devicetrees/commit/66d69b8e2342
This commit does not belong to any branch on this repository, and may belong to a fork outside of the repository.
无法检出
https://github.com/cupid-development/android_kernel_xiaomi_sm8450-devicetrees/commit/584f074b1bb7171915c7ae18665d1657879d32eb  和 mondrian分支存在相同提交记录
再加8个提交= 66d69b8e2342 
但结果和mondrian分支差异较小直接处理，https://github.com/cupid-development/android_kernel_xiaomi_sm8450-devicetrees/archive/66d69b8e2342d835179d3078e16be6f84202527c.zip对比修改
```
### kernel/xiaomi/sm8450-modules
ebb2a56b38 audio-kernel: Enable CS35L41 [Arian] 再手动还原两个提交
```
* kernel/xiaomi/sm8450-modules
98c79be3fd Revert "audio-kernel: Update xiaomi changes from garnet-t-oss" [Arian]
3ed05f8559 Revert "audio-kernel: Enable CS35L41" [Arian]
ebb2a56b38 audio-kernel: Enable CS35L41 [Arian]
```
### hardware/xiaomi 
```
https://github.com/LineageOS/android_hardware_xiaomi/commit/cf41643853c2977853ebb07efd6fdd32e2ec7117 = lineage-20
+ git fetch https://github.com/LineageOS/android_hardware_xiaomi refs/changes/65/352665/4 && git checkout FETCH_HEAD  中9个提交
* hardware/xiaomi
f78fb9e sensors: Handle fod press status without coordinates [Arian]
8e7fa59 sensors: Add udfps long press sensor [Cosmin Tanislav]
d756bca sensors: Fix locking around setOperationMode and activate [Cosmin Tanislav]
977aa45 sensors: Move one shot sensor out of main class [Cosmin Tanislav]
bf691c0 sensors: Make sensor set mode operation function virtual [Cosmin Tanislav]
814ebe8 sensors: Make sensor flush function virtual [Cosmin Tanislav]
12958f1 sensors: Make sensor run function virtual [Cosmin Tanislav]
2132d3a sensors: Make sensor batch function virtual [Cosmin Tanislav]
ddbda11 Add dummy sensors sub HAL [Cosmin Tanislav]
cf41643 vintf: Add common xiaomi framework compatibility matrix [Arian]
```

### packages/resources/devicesettings 
```
* packages/resources/devicesettings
48c1907 devicesettings: Import popupcamera strings [Arian]
https://github.com/LineageOS/android_packages_resources_devicesettings/commit/48c190771825033f3ddb139ba721ae53b2acc4c4
This commit does not belong to any branch on this repository, and may belong to a fork outside of the repository.
无法检出
LineageOS的 lineage-20.0分支加一个提交
```

### LineageOS/android_vendor_lineage
```
lineage-20.0 加一个提交
https://review.lineageos.org/c/LineageOS/android_vendor_lineage/+/367044
https://xdaforums.com/t/rom-13-unofficial-lineageos-20-for-xiaomi-12s-pro.4652643/page-2#post-89321968
```
