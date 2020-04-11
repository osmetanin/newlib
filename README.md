# newlib-tiny

This is [newlib](https://sourceware.org/newlib/) with [tiny-printf patch](http://patches-tcwg.linaro.org/patch/17495/) applied to stdio. The patch was originally developed by Jozef Lawrynowicz for MSP430 chip to provide reduced code size implementation of printf() and puts().

### Prerequisites

newlib should be configured with "nano formatted I/O" enabled:

```
--enable-newlib-nano-formatted-io
```

### Usage

To enable "tiny-printf", pass the following flags to the GNU linker:
```
--wrap printf
--wrap puts
```

