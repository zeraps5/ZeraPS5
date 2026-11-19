# ZeraPS5

Experimental PlayStation 5 emulation for Windows x64, maintained by **metallrockdev**.

## Version 0.1.1 build 984

Version 0.1.1 includes the Vulkan resource paths and fallbacks, native memory/fiber safety fixes, older-CPU compatibility and the compact F10 diagnostics. It remains experimental. Game results retain their tested build and hardware; see [compatibility](COMPATIBILIDADE.md) and [candidate validation](dist/docs/VALIDACAO.txt).

## Build 984 downloads and corresponding source

This repository contains the emulator sources for build 984. The distribution repository hosts the matching Windows ZIP, source archive, and checksums.

- **[Download for Windows](https://github.com/zeraps5/ZeraPS5-Releases/releases/download/v0.1.1-b984/ZeraPS5-v0.1.1-b984-win64.zip)**
- **[Download source code](https://github.com/zeraps5/ZeraPS5-Releases/releases/download/v0.1.1-b984/ZeraPS5-v0.1.1-b984-win64-source.zip)**

See the [b984 release notes and SHA-256 checksums](https://github.com/zeraps5/ZeraPS5-Releases/releases/tag/v0.1.1-b984).

The versioned source archive records the original build revision in [SOURCE-VERSION.txt](SOURCE-VERSION.txt). This public import has its own Git history and includes documentation edits. The Windows package also contains the matching source archive, FFmpeg source, application relink objects, and response files under `sources/`.

## What to expect

ZeraPS5 is experimental. Results depend on the game version, emulator build, settings, scene and hardware. See the [compatibility list](https://github.com/zeraps5/ZeraPS5-Releases/blob/main/COMPATIBILITY.md) for each game's last documented tested version.

See the [technical changelog](CHANGELOG.md) and the [recorded compatibility results](COMPATIBILIDADE.md) for tested changes and scenes.

Compatibility records retain their original tested build, hardware and settings. The Last of Us Part I still produces black frames in the recorded test. Release validation is recorded alongside the versioned download.

## Run

Download the Windows ZIP, verify its checksum, extract it into a writable folder and run `ZeraPS5.exe`. Python, CMake and a compiler are not required to run the distributed executables.

Read `LEIA-ME.txt`, `docs/LIMITACOES.txt`, `docs/REPORTING.txt` and the help document for your interface language. Configure your own game folders and libraries lawfully obtained from your console. Games, console modules, firmware, keys, saves and private settings are not distributed.

### In-game performance panel

Press **F10** in the game window to show or hide the panel, or enable it in the launcher's general settings. It shows frame timing, CPU/GPU models, CPU use, RAM, committed memory, OS version, the GPU's supported Vulkan version (VK SUP) and output size. The compact text adapts to small windows.

The 0.1.1 development build also substitutes unsupported guest instructions on Ivy Bridge-era x64/AVX CPUs. General settings offer automatic detection, a forced compatibility mode for testing, and an off switch. This does not replace the GPU's Vulkan requirements; see [older-CPU testing](dist/docs/TESTE-CPU-ANTIGA.md).

RAM and commit distinguish system totals from the ZeraPS5 process. GPU usage is the Vulkan driver's estimate for this process; the driver budget and device-local heap capacity are shown separately. Integrated GPUs are labeled as shared memory. Unsupported measurements display N/A. Hardware counters refresh once per second while the panel is visible.

## Build and contribute

Clone or fork this repository to browse, build, and propose changes. See [CONTRIBUTING.md](CONTRIBUTING.md) and the [rebuild instructions](dist/docs/RECOMPILAR.txt). The release's Windows ZIP has the matching FFmpeg 7.1.2 source in its `sources/` directory.

To reproduce the original build's revision and build number, compile the versioned source archive outside any Git checkout. Builds from a clone use that clone's Git revision and commit count.

## Credits and licenses

See [LICENSE](LICENSE), [credits](dist/CREDITS.txt) and [component notices](dist/licenses/). Preserve upstream author credits and component licenses when modifying or redistributing these sources. FFmpeg licensing and corresponding sources are included with the distribution; see the rebuild instructions for relinking.

ZeraPS5 is not affiliated with Sony.
