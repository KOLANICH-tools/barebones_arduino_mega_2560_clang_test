Clang Arduino Mega 2560 boilerplate/`hello world`/test project
==============================================================

**We have moved to https://codeberg.org/KOLANICH-tools/barebones_arduino_mega_2560_clang_test , grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

This is a test project, allowing one to test building a program for Arduino Mega 2560 board using Clang.

Prereqs:
* [`ninja`](https://github.com/ninja-build/ninja)[![Debian package](https://repology.org/badge/version-for-repo/debian_unstable/ninja.svg)![Fedora Rawhide package](https://repology.org/badge/version-for-repo/fedora_rawhide/ninja.svg)![Arch package](https://repology.org/badge/version-for-repo/arch/ninja.svg)![Gentoo package](https://repology.org/badge/version-for-repo/gentoo/ninja.svg)](https://repology.org/project/ninja/versions) installed.
* `Clang-15` - can be installed from https://apt.llvm.org/

Despite using `CMakeFiles` dir, CMake is not needed.

Files:
* `toolchain.ninja` - downloads and patches the "latest" (by the time the repo was created) version of Arduino toolchain.
* `build.ninja` - builds the project, calls `toolchain.ninja`
