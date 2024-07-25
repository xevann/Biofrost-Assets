## Build Information

```
Type: Stable || OBT (Channel Releases Only)
Devices: Realme 5 Series (Realme 5, 5i, 5s)
CLO Tag: LA.UM.9.1.r1-15900.01-SMxxx0.QSSI14.0
Compiler: Android (11490625,  pgo,  bolt,  lto,  mlgo, based on r522817) clang version 18.0.1
Optimizations: Link Time Optimization (LTO), Polly, RELR, CPU-Specific Micro-optimizations
```

## Kernel Source

```
Q-Base: https://github.com/mcdofrenchfreis/biofrost-kernel-realme-trinket
R-Base: https://github.com/mcdofrenchfreis/biofrost_kernel_realme_sm6125
```

## Instructions for choosing the appropriate build (As of R12 R-base - 07/28/24)

```
Open Beta Builds:
biofrostOBT-R12-*.zip: Supports both non-dynamic/dynamic ROMs
biofrostOBT-KSU-R12-*.zip: Same as above but with KSU support

Stable Builds:
biofrost-R12-*.zip: Supports both non-dynamic/dynamic ROMs
biofrost-KSU-R12-*.zip: Same as above but with KSU support
```

## Flashing Process (Updated as of R-base migration)

```
For Android Version 14:
- RECOVERY METHOD
1. Reboot to recovery.
2. Flash the kernel zip.
3. Wipe Cache and Dalvik Cache (Optional)
4. Reboot to system.

- FKM METHOD
1. Open FKM.
2. Open "Flasher" Tab
3. Select "Manual Flashing" and load the kernel.zip
4. Select flash and reboot.

For Android Version 11 to 13:
- RECOVERY METHOD
1. Download the required file: fstab_fix (on discussion group, just message #fstabfix)
2. Reboot to recovery.
3. Flash the kernel zip.
4. Flash the fstab_fix.zip.
5. Wipe Cache and Dalvik Cache (Optional)
6. Reboot to system.
```

## Important Notes
- If you have any doubts, questions/queries, join and ask at https://t.me/BiofrostHub
- For the latest Releases (R12 R-base): Android 10 is not supported anymore.
- Should you encounter any issues after flashing the kernel, your previous kernel and dtbo files will always be saved on your internal storage, named accordingly: backup_boot.img, backup_dtbo.img.
