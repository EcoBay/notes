# Bitwise operator

Bitwise operator are operation done in the binary level

## Bitwise Complement

Bitwise compliment operator is an unary operator (works on only one operand). It changes 1 to 0 and 0 to 1. It is commonly denoted by `~`.

```
12 = 00001100
     --------
   ~ 11110011 = 220
```

## Bitwise AND

The output of bitwise AND is 1 if the corresponding bits of two operands is 1. If either bit of an operand is 0, the result of corresponding bit is evaluated to 0. bitwise AND operator is commonly denoted by `&`.

```
12 = 00001100
25 = 00011001
     --------
   & 00001000 = 8
```

## Bitwise OR

The output of bitwise OR is 1 if at least one corresponding bit of two operands is 1. In C Programming, bitwise OR operator is commonly denoted by `|`.

```
12 = 00001100
25 = 00011001
     --------
   | 00011101 = 29
```

## Bitwise XOR

The result of bitwise XOR operator is 1 if the corresponding bits of two operands are opposite. It is denoted by ^.

```
12 = 00001100
25 = 00011001
     --------
   ^ 00010101 = 21
```

## Right Shift Operator

Right shift operator shifts all bits towards right by certain number of specified bits. It is commonly denoted by `>>`. Note: `a >> b` is similar to the truncated value of ${a} / {2 ^ b}$.

```
5 = 00000101
5 >> 1 = 00000010 = 5 / (2 ^ 1) = 5 / 2 = 2
5 >> 2 = 00000001 = 5 / (2 ^ 2) = 5 / 4 = 1
```

## Right Shift Operator

Left shift operator shifts all bits towards left by certain number of specified bits. It is commonly denoted by `<<`. Note: `a << b` is similar to the value of $a \cdot 2 ^ b$.

```
5 = 00000101
5 << 1 = 00001010 = 5 * (2 ^ 1) = 5 * 2 = 10
5 << 2 = 00010100 = 5 * (2 ^ 2) = 5 * 4 = 20
```
