# 🖨️ ft_printf

A custom implementation of the C standard library's `printf()` function, developed at Codam (42 Network).

The project explores variadic functions, format-string parsing, and formatted output in C.

## ✨ Features

- **Variadic arguments:** Uses `stdarg.h` to process a variable number of arguments.
- **Formatted output:** Converts and prints characters, strings, signed and unsigned integers, hexadecimal values, and pointers.
- **Return value:** Returns the number of characters printed, following the behavior expected of `printf()`.
  
### Supported Format Specifiers

| Category | Specifiers |
|---|---|
| Characters & strings | `%c`, `%s` |
| Pointers | `%p` |
| Signed integers | `%d`, `%i` |
| Unsigned integers | `%u` |
| Hexadecimal | `%x` (lowercase), `%X` (uppercase) |
| Literal percent sign | `%%` |

## 🛠️ Usage

**Compile the library**

```bash
make
```

This creates the static library `libftprintf.a`.

**Use it in a C project**

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello, %s! Number: %d\n", "world", 42);
    return (0);
}
```

Compile your program with the library, for example:

```bash
cc main.c -L. -lftprintf -o program
```

## 🧰 Technologies & Concepts

- C
- Variadic functions (`va_start`, `va_arg`, `va_end`)
- Format-string parsing
- Integer base conversion
- Static libraries and Make
