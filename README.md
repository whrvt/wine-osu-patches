# Patchset context

wine commit: [wine-0530ef6f](https://gitlab.winehq.org/wine/wine/-/tree/0530ef6facaca32f2342cb0a4d15f3cce8023b6d)

staging commit: [staging-0682c264](https://gitlab.winehq.org/wine/wine-staging/-/tree/0682c264964498dae7934cbc6aeac5f1dcd52807)

Staging exclude flags: `-W ntdll-Junction_Points -W mountmgr-DosDevices -W ntdll-NtDevicePath -W ws2_32-af_unix -W eventfd_synchronization`

# Environment variables

An autogenerated list of some added environment variables.


Also see the releases page, there may be more relevant details about them there.
This is by no means comprehensive, I'm too lazy for that.

## ALSA_EXTRA_PAD

Patch: [0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch](0012-audio/0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch)

### Commit message

```
alsa,pulse,mmdevapi: Support custom period and buffer sizes, and respect PulseAudio settings.
Relevant environment variables are:
ALSA_EXTRA_PAD (units: usecs*10; default is 40000, can be set to 0, adds extra padding)
STAGING_AUDIO_PERIOD (units: usecs*10)
STAGING_AUDIO_DURATION (units: usecs*10)
Also, silence pcm.c underrun errors.
```

### Type

`boolean`

## STAGING_AUDIO_DURATION

Patch: [0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch](0012-audio/0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch)

### Type

`numeric`

## STAGING_AUDIO_PERIOD

Patch: [0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch](0012-audio/0005-alsa-pulse-mmdevapi-Support-custom-period-and-buffer-sizes.patch)

### Type

`numeric`

## WINEDMO

Patch: [winedmo-Add-envvar-option-to-enable-disable.patch](9000-misc-additions/winedmo-Add-envvar-option-to-enable-disable.patch)

### Commit message

```
winedmo: Add envvar option to enable/disable.
```

## WINEESYNC

Patch: [0003-server-Create-server-objects-for-eventfd-based-synch.patch](0006-proton-esync-fsync/0003-server-Create-server-objects-for-eventfd-based-synch.patch)

### Commit message

```
server: Create server objects for eventfd-based synchronization objects.
```

### Type

`numeric`

## WINEFSYNC

Patch: [0061-server-Create-server-objects-for-futex-based-synchro.patch](0006-proton-esync-fsync/0061-server-Create-server-objects-for-futex-based-synchro.patch)

### Commit message

```
server: Create server objects for futex-based synchronization objects.
```

### Type

`numeric`

## WINENTSYNC

Patch: [0038-server-ntdll-Add-a-do_ntsync-helper.patch](0007-ntsync/0038-server-ntdll-Add-a-do_ntsync-helper.patch)

### Commit message

```
server, ntdll: Add a do_ntsync helper.
Also add WINENTSYNC=0 as a shorthand for WINE_DISABLE_FAST_SYNC=1.
```

### Description

lightweight permission check, full get_linux_device breaks when done at early startup

### Type

`numeric`

## WINE_ALERT_SIMULATE_SCHED_QUANTUM

Patch: [0137-ntdll-HACK-Add-WINE_ALERT_SIMULATE_SCHED_QUANTUM-opt.patch](0006-proton-esync-fsync/0137-ntdll-HACK-Add-WINE_ALERT_SIMULATE_SCHED_QUANTUM-opt.patch)

### Commit message

```
ntdll: HACK: Add WINE_ALERT_SIMULATE_SCHED_QUANTUM option.
And enable it for GTA 5.
CW-Bug-Id: #21194
```

### Type

`boolean`

## WINE_CUSTOM_FPS

Patch: [winex11-Custom-frame-limiter-for-OpenGL.patch](9000-misc-additions/winex11-Custom-frame-limiter-for-OpenGL.patch)

### Commit message

```
winex11: Custom frame limiter for OpenGL
```

### Type

`boolean`

## WINE_CUSTOM_FPS_BUSYTHRESH

Patch: [winex11-Custom-frame-limiter-for-OpenGL.patch](9000-misc-additions/winex11-Custom-frame-limiter-for-OpenGL.patch)

### Type

`boolean`

## WINE_DISABLE_IME

Patch: [disable-ime-envvar.patch](9000-misc-additions/disable-ime-envvar.patch)

### Type

`boolean`

## WINE_DISABLE_KERNEL_WRITEWATCH

Patch: [0001-ntdll-Use-kernel-soft-dirty-flags-for-write-watches-.patch](0013-server-optimization/0005-writewatches/0001-ntdll-Use-kernel-soft-dirty-flags-for-write-watches-.patch)

### Commit message

```
ntdll: Use kernel soft dirty flags for write watches support.
Requires kernel patches to have effect.
```

### Type

`numeric`

## WINE_DISABLE_RAWINPUT

Patch: [force-disable-rawinput-envvar.patch](9000-misc-additions/force-disable-rawinput-envvar.patch)

### Commit message

```
add an env var to force disable rawinput.
```

### Type

`numeric`

## WINE_DISABLE_TSC

Patch: [9300-qpc-support-hardcode-with-old-kernel-check.patch](0013-server-optimization/0003-qpc/9300-qpc-support-hardcode-with-old-kernel-check.patch)

### Description

allow disabling rdtscp if Wine is built with old Linux kernels (e.g. WineBuilder Ubuntu 20.04)

## WINE_ENABLE_ABS_TABLET_HACK

Patch: [cursor-clip-hack.patch](9000-misc-additions/cursor-clip-hack.patch)

### Commit message

```
cursor clip hack
```

### Type

`numeric`

## WINE_FSYNC_SIMULATE_SCHED_QUANTUM

Patch: [0123-fsync-Add-WINE_FSYNC_SIMULATE_SCHED_QUANTUM-config-o.patch](0006-proton-esync-fsync/0123-fsync-Add-WINE_FSYNC_SIMULATE_SCHED_QUANTUM-config-o.patch)

### Commit message

```
fsync: Add WINE_FSYNC_SIMULATE_SCHED_QUANTUM config option.
And auto enable it for Uplay laucher.
CW-Bug-Id: #20155
```

### Type

`boolean`

## WINE_INSTALL_ROOT_DEVICES

Patch: [wineboot-Skip-root-device-installation-if-WINE_INSTA.patch](9000-misc-additions/wineboot-Skip-root-device-installation-if-WINE_INSTA.patch)

### Commit message

```
wineboot: Skip root device installation if WINE_INSTALL_ROOT_DEVICES isn't in the environment.
osu! doesn't need any of them.
```

## WINE_LARGE_ADDRESS_AWARE

Patch: [ps0427-ntdll-loader-add-support-for-overriding-IMAGE_FILE_L.patch](0013-server-optimization/0001-misc/ps0427-ntdll-loader-add-support-for-overriding-IMAGE_FILE_L.patch)

### Commit message

```
ntdll/loader: add support for overriding IMAGE_FILE_LARGE_ADDRESS_AWARE
```

### Type

`numeric`

## WINE_NO_PRIV_ELEVATION

Patch: [0147-ntdll-HACK-Add-WINE_NO_PRIV_ELEVATION-option-and-aut.patch](0006-proton-esync-fsync/0147-ntdll-HACK-Add-WINE_NO_PRIV_ELEVATION-option-and-aut.patch)

### Commit message

```
ntdll: HACK: Add WINE_NO_PRIV_ELEVATION option and auto enable it for Aquarist - My First Job.
CW-Bug-Id: #20846
```

### Type

`boolean`

## WINE_PULSE_MEMLOCK

Patch: [0003-winepulse-Try-memlocking-the-audio-buffer.patch](0012-audio/0003-winepulse-Try-memlocking-the-audio-buffer.patch)

### Commit message

```
winepulse: Try memlocking the audio buffer.
But allow disabling it with WINE_PULSE_MEMLOCK=0.
```

### Type

`numeric`

## WINE_RAM_REPORTING_BIAS

Patch: [0004-ntdll-HACK-Add-WINE_RAM_REPORTING_BIAS-option.patch](0013-server-optimization/0005-writewatches/0004-ntdll-HACK-Add-WINE_RAM_REPORTING_BIAS-option.patch)

### Commit message

```
ntdll: HACK: Add WINE_RAM_REPORTING_BIAS option.
CW-Bug-Id: #22241
```

## WINE_SIMULATE_ASYNC_READ

Patch: [0138-ntdll-HACK-Also-simulate-async-file-read-and-IO-canc.patch](0006-proton-esync-fsync/0138-ntdll-HACK-Also-simulate-async-file-read-and-IO-canc.patch)

### Commit message

```
ntdll: HACK: Also simulate async file read and IO cancellation for Immortals Fenyx Rising.
CW-Bug-Id: #21711
```

### Type

`boolean`

## WINE_STATIC_CPUFREQ

Patch: [static-cpufreq-envvar.patch](9000-misc-additions/static-cpufreq-envvar.patch)

## WINE_WAYLAND_DISPLAY_INDEX

Patch: [add-WINE_WAYLAND_DISPLAY_INDEX.patch](9000-misc-additions/add-WINE_WAYLAND_DISPLAY_INDEX.patch)

### Commit message

```
add WINE_WAYLAND_DISPLAY_INDEX
```

### Type

`numeric`

## XDG_CACHE_HOME

Patch: [ps0341-appwiz.cpl-Try-getting-the-cache-directory-from-an.patch](0013-server-optimization/0001-misc/ps0341-appwiz.cpl-Try-getting-the-cache-directory-from-an.patch)

### Commit message

```
appwiz.cpl: Try getting the cache directory from an environment variable first.
```

## vblank_mode

Patch: [0019-winex11-Force-disable-glXWaitForSbcOML-AMD-on-Waylan.patch](0009-windowing-system-integration/0001-misc/0019-winex11-Force-disable-glXWaitForSbcOML-AMD-on-Waylan.patch)

### Commit message

```
winex11: Force disable glXWaitForSbcOML (AMD) on Wayland to circumvent Xwayland locking FPS to the monitor's refresh rate.
It will prevent ingame vsync from working properly, but the environment variable
vblank_mode != 0 can override-disable this behavior.
```

### Type

`boolean`

