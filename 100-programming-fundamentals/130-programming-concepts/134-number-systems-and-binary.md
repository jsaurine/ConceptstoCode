---
description: >-
  Learn how binary numbers work and why they are central to computing systems
  and digital logic.
---

# 134 Number systems and binary

### Outline

In this module, we explore how computers represent numbers using binary (base-2) and why this number system is essential in digital computing. You'll learn how to convert between binary and decimal, perform simple binary arithmetic, and understand how binary underpins memory, data types, and program logic.

### Targets

In this topic, students learn to:

* Understand the binary and decimal number systems
* Convert numbers between binary and decimal formats
* Perform binary addition
* Recognise overflow and how computers handle negative values
* Explain the practical applications of binary in computing systems

### Glossary

| Term                           | Definition                                                              |
| ------------------------------ | ----------------------------------------------------------------------- |
| **Binary**                     | A base-2 number system using only digits 0 and 1                        |
| **Bit**                        | The smallest unit of data in computing; a single binary digit           |
| **Byte**                       | A group of 8 bits                                                       |
| **Overflow**                   | An error occurring when a calculated value exceeds the storage capacity |
| **Two’s complement**           | A method of representing signed integers in binary                      |
| **BCD (Binary Coded Decimal)** | A way of storing each decimal digit as its binary equivalent            |

### Overview

Computers use millions of tiny switches that can only be **ON** or **OFF**, corresponding to the binary digits **1** and **0**. This makes binary the native language of digital systems. All information—numbers, text, images—is encoded using combinations of binary digits.

Understanding binary is essential for understanding how computers store and manipulate data. Whether storing a number in memory, performing arithmetic, or processing a colour value in an image, binary provides the underlying structure.

### Denary and binary place value

The decimal (denary) system is based on powers of 10. For example, the number 7324 means:\
7×1000 + 3×100 + 2×10 + 4×1

Binary is based on powers of 2. For example, the number 11001 in binary means:\
1×16 + 1×8 + 0×4 + 0×2 + 1×1 = **25**

| Position | 2⁴ | 2³ | 2² | 2¹ | 2⁰ |
| -------- | -- | -- | -- | -- | -- |
| Binary   | 1  | 1  | 0  | 0  | 1  |

#### Converting between binary and decimal

To convert a decimal to binary, divide by 2 repeatedly and record remainders.\
To convert binary to decimal, multiply each bit by its corresponding power of 2 and add.

**Example:** Convert 91 to binary

* 91 ÷ 2 = 45 r1
* 45 ÷ 2 = 22 r1
* 22 ÷ 2 = 11 r0
* 11 ÷ 2 = 5 r1
* 5 ÷ 2 = 2 r1
* 2 ÷ 2 = 1 r0
* 1 ÷ 2 = 0 r1

**Binary:** 1011011

#### Binary addition

Just like decimal addition, binary addition has rules:

* 0 + 0 = 0
* 0 + 1 = 1
* 1 + 1 = 10 (carry 1)
* 1 + 1 + 1 = 11 (carry 1)

**Example:**

```
  0101   (5)
+ 1001   (9)
-------
  1110  (14)
```

### Overflow

A register with 8 bits can store up to `11111111` (255 in decimal). If an operation produces `100000000`, the extra bit is lost. This is called **overflow**.

**Example:**

```
  11101101
+ 10000100
----------
1_01110001 (Overflow: the 9th bit is lost)
```

### Representing negative numbers

Computers often use **two’s complement** to represent negative integers.

**To represent -5 in 4-bit two’s complement:**

1. Start with +5 → 0101
2. Invert bits → 1010
3. Add 1 → 1011\
   → So, -5 is 1011 in two’s complement (4-bit)

The range of values for 8-bit two’s complement:

* Min: `10000000` = -128
* Max: `01111111` = +127

### Applications of binary in computing

Binary is used everywhere in computing. Here’s how:

**1. Memory representation:**\
All data in memory—numbers, text, images—is stored as binary. Each memory cell stores a bit, and bytes are grouped to store larger values.

**2. Data types and storage:**\
Integer and floating-point numbers use binary to represent values. Bit-length determines range and precision (e.g. 8-bit = 0–255, 16-bit = 0–65535).

**3. Logic and processing:**\
Binary arithmetic forms the basis of all logic circuits, processors, and control systems.

**4. File encoding and transmission:**\
Binary is used to encode everything from MP3 files to network packets.

**5. Instruction sets:**\
At the machine level, all CPU instructions are binary opcodes.

### Key concepts

* Binary uses only 0 and 1 and underpins all digital computation
* Conversion between binary and decimal is a fundamental skill
* Overflow occurs when a value exceeds the storage limit
* Two’s complement enables signed integer representation
* BCD is used for decimal digit display in some hardware systems
* Binary is critical for memory, data representation, and system logic
