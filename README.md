# STM32 Blink

Instructions followed: https://github.com/glegrain/STM32-with-macOS/tree/master

Notes:

- `arm-none-eabi-gcc` installed via `homebrew install  --cask gcc-arm-embedded`
- Boilerplate generated with STM32CubeMX (Toolchain: Makefile)
    - Didn't change anything in any tabs
    - Makefile worked out-of-the-box
    - project settings are stored in an `.ioc` file

## Compiling/running

```
$ make clean && make && st-flash write ./build/*.bin 0x08000000 &&  st-flash --format ihex write ./build/*.hex
```

- Copied some source code from STM32-with-macOS repo for blink logic
- Claude fixed issues with GPIO config (see git log)

Tested on the STM32F303 Nucleo-32 (STM32F303K8T6)

Good overview: https://www.youtube.com/watch?v=Hffw-m9fuxc&t=454s&ab_channel=MitchDavis