# Zephyr Module example and template

This is a sample and template code for Zephyr's module system.  This
repository's aim is to support developers who want to integrate an
existing code as a Zephyr module.

For anyone want to work with Zephyr modules, please read [the official
document](https://docs.zephyrproject.org/latest/guides/modules.html)
first.

# Given

 - This repository have a sample library, libsample, which we want to
   integrate to Zephyr as a module.

 - libsample has two functions
   - sample_pure() does not use any Zephyr facility at all.  It does
     its own calculation and return. If this is the case for all
     functions in your code, it's simple.
   - sample_zephyr() uses Zephyr facility and you need to take care a
     few more bits.

 - libsample is bulidable for both Linux and Zephyr and we want to
   target both native_posix and qemu_cortex_m3.

 - The build system for this repository is CMake.  A Zephyr module
   must have a working CMake build script.  If code is based on Meson,
   GNU Make, or any other build system, you must first port to CMake.

# ToDo

 - [ ] Support autoconf.h
 - [ ] Support -std=gnu11
 - [ ] Support its own cflags
