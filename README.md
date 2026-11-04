# Omarchy Phone: iPhone 6s

![Platform: iPhone 6s](https://img.shields.io/badge/Device-iPhone%206s-555555?style=for-the-badge&logo=apple&logoColor=white)
![System: Omarchy Linux](https://img.shields.io/badge/System-Omarchy%20Linux-1793D1?style=for-the-badge&logo=linux&logoColor=white)
![Status: experimental](https://img.shields.io/badge/Status-Experimental-E8A838?style=for-the-badge)
[![Support on Ko-fi](https://img.shields.io/badge/Ko--fi-support-FF5E5B?style=flat&logo=kofi&logoColor=white&labelColor=555555)](https://ko-fi.com/paulwesker/goal?g=0)

**Giving older Apple hardware a second life, one working component at a time.**

Omarchy Phone is an experimental project exploring how to make Omarchy Linux useful on an iPhone 6s. The goal is a pocket-sized Linux environment for terminal work, development, and AI-assisted workflows, built through hands-on testing and better hardware support.

> **Early research project.** Booting a desktop or displaying a screenshot is not the same as having a fully functional phone. Hardware support, boot behavior, and reliability need to be tested and documented for each device.

## The idea

Older iPhones still contain capable processors, displays, storage, and wireless hardware. This project explores how much of that hardware can become useful with an alternative operating system—and how the results can help others extend the life of their devices.

The initial focus is the **iPhone 6s**. Other Apple devices, including the iPhone X, are potential future research targets; their support is not implied by this repository.

## Current status

The current test device is an **iPhone 6s (N71m / S8003, Apple A9)**. Linux boots into RAM through **DFU**. This is a host-assisted research setup, not a standalone installation or an untethered phone boot.

The results below distinguish device tests from builds and planned work. System revisions **r2/r3** and GPU research versions **v2/v3** refer to separate work streams.

| Component | Tested status and limitations |
| --- | --- |
| Boot and installation procedure | RAM boot through DFU demonstrated; a standalone installation is not established |
| Display and touch | GUI and touch verified on r2 |
| Wi-Fi and networking | Wi-Fi and HTTPS verified on r2 |
| Charging and battery | Charging verified on r2; battery life and broader power behavior remain uncharacterized |
| Sleep and wake | Verified in a live r3 session; r3 cold boot has not been validated |
| Audio, camera and cellular | Not yet verified |
| GPU firmware | v2 reaches firmware boot-ready and stops cleanly on the device; no GPU jobs have run |
| GPU acceleration | Not achieved; rendering currently uses CPU-based llvmpipe |
| GPU raw-event instrumentation | v3 built, but not yet tested on the device |
| Codex CLI | Not yet documented on this device |

**A firmware-ready GPU is not an accelerated graphics stack.** Firmware startup and clean shutdown do not demonstrate job submission, successful GPU execution, or OpenGL ES support. Likewise, a successful live r3 sleep/wake test does not validate an r3 cold boot.

**“Not yet verified” does not mean broken.** Results apply only to the tested device, revision, and boot method; they do not establish support for other Apple devices.

## First milestones

1. Document a reproducible DFU RAM-boot procedure and exact tested configuration, with logs and known limitations.
2. Validate r3 from a cold boot and repeat sleep/wake testing.
3. Test the built GPU v3 raw-event instrumentation on the device.
4. Research the A9 G5P instruction set, PDS/PDM behavior, and GPU memory mapping, with the first execution target being a minimal GPU memory-fill job.
5. Work toward OpenGL ES/EGL only after basic GPU execution and memory access are demonstrated.
6. Continue hardware testing and investigate Codex CLI behavior and memory use on the device.

These are next steps, not completed capabilities. No successful GPU job or hardware-accelerated OpenGL ES/EGL result is claimed.

Future research may explore additional Apple devices and Darwin. These are directions for investigation, not promises of support or a release date.

## Background and useful projects

This project stands on the work of existing communities:

- [Omarchy](https://omarchy.org/) — the Linux environment this project explores.
- [Omarchy A](https://github.com/OrchardLinux/omarchy-a) — an experimental effort for Apple A-series devices; consult its documentation for its own supported devices and limitations.
- [Hoolock Linux](https://github.com/HoolockLinux) — Apple A-series Linux hardware research.
- [Codex CLI](https://github.com/openai/codex) — an open-source coding agent we intend to investigate on this platform.

This is an independent project and is not affiliated with Apple or the projects linked above. Product names belong to their respective owners.

## Safety

This is experimental work. Boot procedures and storage changes can cause data loss, and device support varies. Do not assume untethered boot, working cellular service, or a fully functional daily-driver system. Read and understand the instructions for your exact device before trying anything.

## Support

Support helps fund an AI development subscription and older devices for hands-on testing.

[Support the project on Ko-fi](https://ko-fi.com/paulwesker/goal?g=0)

## Contributing

Research, hardware testing, documentation, and driver development can all help. Please describe the exact device, software version, steps, and observed results when sharing findings. Respect other projects’ licenses and avoid publishing proprietary firmware or code without the rights to do so.

## License

A project license has not yet been selected. Refer to each upstream project’s own license when using its materials.
