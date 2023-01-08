## Build Information
```
Type: Bleeding Edge
Device: Pocophone F1 (Beryllium)
Linux Version: 4.9.337
CLO Version: LA.UM.10.3.r1-01700-sdm845.0
Compiler: Neutron Clang 16.0.0
```
## Kernel Instructions
```
- for System EXT (SE) ROMs only
- for AOSP ROMs only, MIUI unsupported
- Pixel Thermal ROMs are unsupported
```
**v1.019**
* Compiled using custom LLVM 16.x upstream (LLD Linker + IAS)
* Compiled with Full LTO, POLLY, CPU-specific optimization, DCE and RELR Relocations
* Merged tag v4.9.337 from ACK's android-4.9-stable branch.
* Merged exFAT Driver (6.0.0) from linux-exfat-oot
* Latest Wireguard (20220627) merged in
* Backported Binder from ACK's android14-5.15 branch.
* Backported vmalloc from Linux 5.2-rc1
* RCU Backports from Linux 4.14
* Latest ARM Optimized Routines from Linux 5.14
* LSE Atomics and Spinlock backports
* WALT scheduler + Backports from RenderBroken/CAF
* KernelSpace Profiles for in-kernel profile switching
* Optimized schedutil CPU Governor with schedhorizon changes merged in
* Scheduler boosting with UCLAMP from Mainline
* Power-efficient workqueues merged in subsystems
* Optimized Energy Model with efficient frequency table
* Completely disabled debugging and tracing configs
* Simple LMK driver from kerneltoast
* Ion, iommu rewrites from kerneltoast
* Devfreq Boost from kerneltoast
* CPU Input Boost from kerneltoast
* MSM Thermal Simple from kerneltoast
* CFQ Backports for better I/O Performance
* TCP Backports for better network latency
* KGSL Backports for better GPU handling
* Latest LZ4 Driver from Official LZ4 Repository
* Replaced ZRAM with ZSWAP/VBSWAP Setup for better memory management
* Removed VLA treewide for less overheads
* LRNG for better random read/write performance
* Many other more