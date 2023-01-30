## Build Information
```
Type: Bleeding Edge
Device: Pocophone F1 (Beryllium)
Linux Version: 4.9.337
CLO Version: LA.UM.10.3.r1-01700-sdm845.0
Compiler: Neutron Clang 17.0.0
```
## Kernel Instructions
```
- for System EXT (SE) ROMs only
- for AOSP ROMs only, MIUI unsupported
- Pixel Thermal ROMs are unsupported
```

**v1.024**
* Compiled with Neutron Clang 17.0.0 (28012023)
* Drop thermal simple and other thermal changes from v1.022 and introduce:
  - Workaround for xiaomi thermal mitigation
  - Use and switch to step_wise as default thermal governor
  - Import step_wise governor ricing from msm-4.14
* Cleanup previous KGSL changes to make way for better optimizations
* Affine KGSL's low_prio_worker thread to big CPUs
* Improve UFS Performance by importing optimizations/ricings
* Huge cpuidle code cleanup and optimization; Switch to WFI (Wait for Interrupt)
* Make cpuidle latency notifier no-op
* Set default read_ahead_kb to 64KB (for UFS)
* Increase default vmstat interval to 60s
* Rework on kernel branding; place git commit hash on additional kernel information
* Misc fixes and improvements.

**v1.023**
* Update UtilClamp tuning (improve it further)
* Drop swappiness to 120 (let apps stay on ram for slightly longer)
* Dont let userspace set maximum frequency (in accordance to thermal simple)
* Reconfigure thermal simple parameters for mildly calmer throttling
* Reintroduce CPU Input boosting (only for kernel profile 2/3)
* Reconfigure schedhorizon frequency hold duration
* Disabled unused/redundant configs (this includes unused cpu governors and ioscheds)
* Improve power efficiency (active and idle drain)
* Misc improvements (forgot a lot of em)

**v1.022**
* Bump compiler to 16012023 tag
* Remove WQ_CPU_INTENSIVE from unbound workqueue allocations
* Drop CPU Input Boost (excessive battery drains)
* Rework on Frequency Table (for better power efficiency)
* Import some more binder optimizations/backports
* Enable BPF JIT to improve eBF programs performance
* Reconfigure schedhorizon under kprofiles
* Configure subsystem boosting under kprofiles (ddr bus)
* Retune uclamp for overall usage and less jitters
* Rework on LTO Optimizations, clean LTO inlining
* Fix system lags on long uptime (make kcompactd more responsive)
* Optimize thermal simple configuration for better thermal throttling
* Cleanup and optimize defconfig (disabled all redundant configs)
* Moar UFS optimizations/fixups
* More misc changes, power efficiency improvements/under-the-hood changes

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