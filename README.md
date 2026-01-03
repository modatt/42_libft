# Libft

A robust, standards-compliant C library implementing essential libc functions and additional utilities.

[![42 School](https://img.shields.io/badge/42-Amman-000000?style=flat&logo=42&logoColor=white)](https://42amman.com)

##  Table of Contents

- [About](#about)
- [Features](#features)
- [Function Reference](#function-reference)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technical Details](#technical-details)
- [Testing](#testing)
- [License](#license)

##  About

**Libft** is a foundational C library developed as part of the 42 programming curriculum. This project involves recreating standard C library functions from scratch, providing a deep understanding of low-level programming, memory management, and algorithm implementation.

The library serves as a personal toolkit for future C projects, emphasizing:
- **Standards compliance** - Functions adhere to libc specifications
- **Memory safety** - Careful handling of edge cases and buffer management
- **Code quality** - Clean, readable, and well-documented implementations
- **Modularity** - Each function is self-contained and reusable

##  Features

### Part 1: Standard C Library Functions
Implementation of essential libc functions with the `ft_` prefix:
- Character validation and transformation
- String manipulation and comparison
- Memory operations
- Conversion utilities

### Part 2: Additional Utility Functions
Extended functionality not present in the standard library:
- Advanced string operations (`ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`)
- String transformation (`ft_strmapi`, `ft_striteri`)
- Integer to string conversion (`ft_itoa`)
- File descriptor output functions

##  Function Reference

### Character Functions
| Function | Description |
|----------|-------------|
| `ft_isalpha` | Checks if character is alphabetic |
| `ft_isdigit` | Checks if character is a digit |
| `ft_isalnum` | Checks if character is alphanumeric |
| `ft_isascii` | Checks if character is ASCII |
| `ft_isprint` | Checks if character is printable |
| `ft_toupper` | Converts character to uppercase |
| `ft_tolower` | Converts character to lowercase |

### String Functions
| Function | Description |
|----------|-------------|
| `ft_strlen` | Calculates string length |
| `ft_strchr` | Locates first occurrence of character |
| `ft_strrchr` | Locates last occurrence of character |
| `ft_strncmp` | Compares strings up to n characters |
| `ft_strlcpy` | Size-bounded string copy |
| `ft_strlcat` | Size-bounded string concatenation |
| `ft_strnstr` | Locates substring in string |
| `ft_strdup` | Duplicates string |
| `ft_substr` | Extracts substring |
| `ft_strjoin` | Concatenates two strings |
| `ft_strtrim` | Trims characters from string ends |
| `ft_split` | Splits string by delimiter |
| `ft_strmapi` | Applies function to each character |
| `ft_striteri` | Applies function to each character with index |

### Memory Functions
| Function | Description |
|----------|-------------|
| `ft_memset` | Fills memory with constant byte |
| `ft_bzero` | Zeros memory block |
| `ft_memcpy` | Copies memory area |
| `ft_memmove` | Copies memory with overlap handling |
| `ft_memchr` | Scans memory for character |
| `ft_memcmp` | Compares memory areas |
| `ft_calloc` | Allocates and zeros memory |

### Conversion Functions
| Function | Description |
|----------|-------------|
| `ft_atoi` | Converts string to integer |
| `ft_itoa` | Converts integer to string |

### Output Functions
| Function | Description |
|----------|-------------|
| `ft_putchar_fd` | Outputs character to file descriptor |
| `ft_putstr_fd` | Outputs string to file descriptor |
| `ft_putendl_fd` | Outputs string with newline to FD |
| `ft_putnbr_fd` | Outputs integer to file descriptor |

##  Installation

### Prerequisites
- GCC or Clang compiler
- Make utility
- Standard C library headers

### Build Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/42_libft.git
   cd 42_libft
   ```

2. **Compile the library**
   ```bash
   make
   ```

3. **Clean object files** (optional)
   ```bash
   make clean
   ```

4. **Remove all build files** (optional)
   ```bash
   make fclean
   ```

5. **Rebuild from scratch** (optional)
   ```bash
   make re
   ```

##  Usage

### Basic Integration

1. Include the library in your project:
   ```c
   #include "libft.h"
   ```

2. Compile your program with the library:
   ```bash
   gcc -Wall -Wextra -Werror your_program.c -L. -lft -o your_program
   ```

### Example Code

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    char *str = "Hello, 42!";
    char *dup = ft_strdup(str);
    
    ft_putendl_fd(dup, 1);
    printf("Length: %zu\n", ft_strlen(dup));
    
    free(dup);
    return (0);
}
```

##  Project Structure

```
42_libft/
 ft_*.c              # Function implementations
 libft.h             # Header file with prototypes
 Makefile            # Build automation
 README.md           # Project documentation
```

##  Technical Details

### Compilation Flags
- `-Wall` - Enable all warnings
- `-Wextra` - Enable extra warnings
- `-Werror` - Treat warnings as errors

### Coding Standards
- **Norminette compliant** - Adheres to 42 coding standards
- **No memory leaks** - All allocated memory is properly freed
- **Null safety** - Functions handle NULL pointers gracefully
- **Buffer overflow protection** - Size-bounded operations prevent overflows

### Performance Considerations
- Optimized memory operations using efficient algorithms
- Minimal function call overhead
- Cache-friendly memory access patterns

##  Testing

The library has been extensively tested with:
- **Custom test suites** - Edge cases and boundary conditions
- **Third-party testers** - Libft-War-Machine, libft-unit-test
- **Memory analysis** - Valgrind for leak detection
- **Stress testing** - Large datasets and extreme values

### Running Tests

```bash
# Example using a popular tester
git clone https://github.com/y3ll0w42/libft-war-machine.git
cd libft-war-machine
bash grademe.sh
```

##  License

This project is part of the 42 School curriculum and is intended for educational purposes.

---

**Author**: 42 Student  
**School**: 42 Amman  
**Project**: Libft  
**Last Updated**: January 2026
