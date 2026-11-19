# Contributing to ZeraPS5

Fork this repository, create a branch from `main`, and open a pull request with a focused change. Include the affected build, steps to reproduce the behavior, and tests you ran.

See the [rebuild instructions](dist/docs/RECOMPILAR.txt) for the Windows toolchain and FFmpeg dependency. The unit suite uses CTest. Native GPU tests can also be enabled with `-DPS5C_RUN_GPU_TESTS=ON` on a suitable host.

For game compatibility reports, provide the build, game revision, hardware, settings, and scene reached. Remove personal paths and identifiers from logs before sharing them. Keep games, console modules, firmware, keys, saves, and local settings out of commits and reports.

Preserve the [credits](dist/CREDITS.txt), [component notices](dist/licenses/), and license headers.
