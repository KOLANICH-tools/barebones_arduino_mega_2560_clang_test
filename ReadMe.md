Clang Arduino Mega 2560 boilerplate/`hello world`/test project
==============================================================

This is a test project, allowing one to test building a program for Arduino Mega 2560 board using Clang.

Prereqs:
* [`ninja`](https://github.com/ninja-build/ninja)[![Debian package](https://repology.org/badge/version-for-repo/debian_unstable/ninja.svg)![Fedora Rawhide package](https://repology.org/badge/version-for-repo/fedora_rawhide/ninja.svg)![Arch package](https://repology.org/badge/version-for-repo/arch/ninja.svg)![Gentoo package](https://repology.org/badge/version-for-repo/gentoo/ninja.svg)](https://repology.org/project/ninja/versions) installed.
* `Clang-15` - can be installed from https://apt.llvm.org/

Despite using `CMakeFiles` dir, CMake is not needed.

Files:
* `toolchain.ninja` - downloads and patches the "latest" (by the time the repo was created) version of Arduino toolchain.
* `build.ninja` - builds the project, calls `toolchain.ninja`
