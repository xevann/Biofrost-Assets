## Build Information

```
Type: Stable || OBT (Channel Releases Only)
Device: Beryllium (Pocophone F1)
CLO Tag: LA.UM.10.3.r1-01700-sdm845.0
Compiler: Android (11490625,  pgo,  bolt,  lto,  mlgo, based on r522817) clang version 18.0.1
Optimizations: Link Time Optimization (LTO)
               Polly (Polyhedral)
               RELR (Relocation) 
               CPU-Specific Micro-optimizations
               MLGO (Machine Learning Guided)
               fast-FMA
               Hot-cold Split
```

## Kernel Source

```
Closed Source, sorry :P
```

## Instructions for choosing the appropriate build 

```
- BiofrostSE (for system-ext roms)
- BiofrostNSE (for non system-ext roms)
- BiofrostOldTouch (SE build with old nvt firmware version)
- BiofrostPixelThermal (SE build with Pixel Thermal support)

Side Notes:
- If a build has both names, that just obviously means it supports both. (e.g: PixelThermal+OldTouchFirmware)
- Builds are automatically on latest Touch Firmware with the exception of OldTouchFirmware builds (of course.)
```

## Flashing Process
```
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
```

## Important Notes
- If you have any doubts, questions/queries, join and ask at https://t.me/BiofrostHub
- Should you encounter any issues after flashing the kernel, your previous kernel file will always be saved on your internal storage, named: backup_boot.img.
- Kprofiles Guide: https://telegra.ph/Kprofiles-Configuration-Biofrost-Kernel-02-14
