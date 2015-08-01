# endian.h

This provides the endian conversion functions form endian.h on Windows, Linux,
*BSD, and Mac OS X. You still need to use `-std=gnu99` instead of `-std=c99`
for gcc. The functions might actually be macros. Functions: htobe16, htole16,
be16toh, le16toh, htobe32, htole32, be32toh, le32toh, htobe64, htole64,
be64toh, le64toh.

The implementation was written by Mathias Panzenböck and published in this
[Gist][gist].

## Install

Install with [clib(1)]:

```sh
clib install mikepb/endian.h
```

## Usage

```c
#include <stdint.h>
#include "endian.h"

uint32_t endian32(const uint32_t i) {
    return be32toh(i);
}
```

## License

Public Domain

[clib]: https://github.com/clibs/clib
[gist]: https://gist.github.com/panzi/6856583
