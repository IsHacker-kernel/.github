<center>
<img src="branding.png">

<b>IsHacker kernel</b> is a custom Linux kernel designed specifically for low-end and/or old Android devices to improve their usability, performance and, in some cases, even battery life.
</center>

# Features (with explanation)
These features are common accross all supported devices.

**1. No Slop and full source disclosure:** All code and modifications in the kernel, including this README, is written by a human. No LLMs are used for any kind of assistance for programming, code verification or writting text (like this one). Further, all kernels released under this project will have their source disclosed in a git repo (as required by the GPL) **along with the shell script containing the exact commands used to build the kernel**. The shell scripts are in the **.IsHacker-kernel/** directory inside the kernel source. 

**This feature is the core principle of IsHacker kernel, and thus will always be present in all kernel builds under this project. For this reason, it will not be listed in the Device-specific features.**

**2. Overclocking:** The kernels will come with CPU, GPU or, if possible, RAM OC to improve performance. The TX power of the WiFi chip/cellular modem may also be increased for better signal reception. Thus, it is recommended to use phone coolers/custom cooling equipment with these kernels to avoid hardware damage due to overheating.

**3. No Low Memory Killer/LMKD:** Android's Low Memory Killer (userspace lmkd or in-kernel driver) will be removed or disabled. This saves battery by reducing CPU overhead of scanning the memory and killing processes, and by preventing the "kill and reload from flash" situation for cached apps. Also, no automatic killing of background/minimized apps means improved multitasking and productivity, just like how minimized programs don't just automatically get closed due to "low memory" on any Desktop operating systems. **The default Linux OOM killer remains enabled.**

**4. Better memory management:** Featured like Multi-generational LRU (MGLRU), Parallelized kcompressd, etc will be included to improve memory management and increase responsiveness under low memory conditions.

**5. No thermal/power throttling:** Absurd thermal/power throttling "features" (like the one on Mediatek devices) will be removed to let the device utilize its full potential. Again, external cooling is recommended (but NOT enforced, unlike thermal throttling ;) It's your choice) to prevent hardware damage due to overheating.

**6. Compiler optimizations:** The kernels are compiled using clang (rather than GCC) and often include Link-time Optimization (LTO) and CPU/arch-specific optimizations. -O3 and -ffast-math flags are also applied wherever necessary. Most debugging flags and kernel configs are also disabled to reduce runtime overhead.

**7. Additional features:** WireGuard, Kali NetHunter modules, KVM, backports from mainline kernels and other additional features may also be included in the kernels.

**8. Official KSU only:** Wherever KernelSU is integrated as the in-kernel root solution, only the official KernelSU or a backport of it (such as the [fork by backslashxx](https://github.com/backslashxx/KernelSU)) will be used, and not derivatives like KSU-Next or (Re)SukiSu. This is because the official version is the most lightweight and the most stable one, due to unavailability of "root hiding" features.

**But I want to hide root to use "banking" apps!!!**

Please listen to this carefully. Root access is an essential part of every OS, and it is not at all wrong to have it. In fact, any OS is incomplete without superuser rights. If an app refuses to work becuase tour phone has root access, the developer has some serious issues and it is morally wrong to use such apps. If your banking app detects root, you can use net-banking in the browser. And no, root does not "compromise your device's security and privacy", rather in most cases, it actually improves them, significantly. Please do **NOT** fall for such propaganda!

# Currently supported devices
## Xiaomi
1. [Redmi 9A/9i/9C/9AT/10A (blossom)](https://github.com/IsHacker-kernel/android_kernel_xiaomi_blossom)
2. [Redmi 13C 4G / Poco C65 (gale/gust)](https://github.com/IsHacker-kernel/android_kernel_xiaomi_gale) [W.I.P, not released yet]
## HMD Global
1. [Nokia 3 (heart/NE1)](https://github.com/IsHacker-kernel/android_kernel_nokia_heart) [W.I.P, not released yet]
