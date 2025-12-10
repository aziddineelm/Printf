# 🖨️ ft_printf - Custom Printf Implementation

[![42 School](https://img.shields.io/badge/42-Project-blue)](https://www.42.fr/)
![Language](https://img.shields.io/badge/Language-C-blue)

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Function Prototype](#function-prototype)
- [Supported Format Specifiers](#supported-format-specifiers)
- [Project Structure](#project-structure)
- [Learning Objectives](#learning-objectives)
- [Testing](#testing)
- [Author](#author)

## 🔍 Overview
This repository contains a custom implementation of the C standard library's `printf` function, developed as part of the **1337 (42 Network)** curriculum.  The project challenges students to recreate one of the most widely-used functions in C programming, providing deep insight into variadic functions, type conversions, and formatted output.

## ✨ Features
The `ft_printf` function replicates the core functionality of the standard `printf` with support for: 

### Format Specifiers
| Specifier | Description | Example |
|-----------|-------------|---------|
| `%c` | Single character | `ft_printf("%c", 'A')` → `A` |
| `%s` | String of characters | `ft_printf("%s", "Hello")` → `Hello` |
| `%d` / `%i` | Signed decimal integer | `ft_printf("%d", -42)` → `-42` |
| `%u` | Unsigned decimal integer | `ft_printf("%u", 42)` → `42` |
| `%x` | Hexadecimal (lowercase) | `ft_printf("%x", 255)` → `ff` |
| `%X` | Hexadecimal (uppercase) | `ft_printf("%X", 255)` → `FF` |
| `%p` | Pointer address | `ft_printf("%p", ptr)` → `0x7ffd5a3b2c40` |
| `%%` | Literal percent sign | `ft_printf("%%")` → `%` |

### Additional Capabilities
- ✅ Handles width and precision modifiers
- ✅ Manages edge cases (`NULL` strings, zero values, large numbers)
- ✅ Returns the total number of characters printed
- ✅ Memory-safe implementation

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/aziddineelm/Printf.git

# Navigate to the project directory
cd Printf

# Compile the library
make

# This will generate libftprintf.a
```

## 💻 Usage

```c
#include "ft_printf.h"

int main(void)
{
    int count;
    
    count = ft_printf("Hello, %s!\n", "World");
    ft_printf("Characters printed: %d\n", count);
    
    ft_printf("Number: %d, Hex: %x, Pointer: %p\n", 42, 255, &count);
    
    return (0);
}
```

**Compilation with your program:**
```bash
gcc -Wall -Wextra -Werror main.c -L. -lftprintf -o my_program
```

## 📐 Function Prototype

```c
int ft_printf(const char *format, ...);
```

**Returns:** The total number of characters printed (excluding the null terminator)

## 🗂️ Project Structure

```
Printf/
├── ft_printf.c       # Main printf implementation
├── ft_printf. h       # Header file with function prototypes
├── ft_putchar.c      # Character output handler
├── ft_putstr. c       # String output handler
├── ft_putnbr. c       # Number output handler
├── ft_put_hex.c      # Hexadecimal conversion handler
└── Makefile          # Compilation rules
```

## 🎓 Learning Objectives

Through this project, I developed expertise in: 

- 🔧 **Variadic Functions**:  Mastered `va_list`, `va_start`, `va_arg`, and `va_end` macros
- 📚 **C Standard Library**: Gained deep understanding of how standard library functions work internally
- 🧠 **Memory Management**: Implemented safe memory handling and buffer management
- 🐛 **Edge Case Handling**: Developed robust solutions for corner cases and error conditions
- 🧪 **Testing & Debugging**: Strengthened debugging skills through extensive testing
- 🏗️ **Modular Programming**: Designed clean, modular code architecture

## 🧪 Testing

You can test this implementation using:
- [ft_printf Tester](https://github.com/Tripouille/printfTester)
- [printf Unit Test](https://github.com/gavinfielder/pft)
- Custom test cases comparing output with standard `printf`

## 👨‍💻 Author

**aziddineelm** - [GitHub Profile](https://github.com/aziddineelm)
