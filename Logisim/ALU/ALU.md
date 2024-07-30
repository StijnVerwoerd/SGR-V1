# Arithmatic Logic Unit

### Operations
As of right now the ALU can do four kinds of operations:
* **Compare**
    * A < B *with code: 010010*
    * A = B *with code: 010001*
    * A >= B *with code: 100011*
* **Arithmatic**
    * A + B *with code: 0001xx*
    * A - B *with code: 0101xx*
* **Logic**
    * A & B *with code: 001000*
    * A | B *with code: 001001*
    * A XOR B *with code: 001011*
* **Shift**
    * A << B *with code: 001100*
    * A >> B *with code: 001101*
    * A >> B (signed) *with code: 001111*

---

The code is broken down like this:

    [0:1] selects which operation gets performed within the subunit
    [2:3] selects which subunit gets selected for the operation
    [4] 0 equals B normal, 1 equals B inverted
    [5] 0 equals A normal, 1 equals A inverted

More functionality can be added later, such as the multiplication extension requires.

## Instructions:

| Operation        | Code       | Instruction                            |
|------------------|------------|----------------------------------------|
| **Arithmetic**   |            |                                        |
| A + B            | 0001xx     | ADD / ADDI / LW / SW / LB / LH / JAL / JALR |
| A - B            | 0101xx     | SUB                                    |
| A + B (U)        |            | LBU / LHU                              |
| **Logic**        |            |                                        |
| XOR              | 001011     | XOR / XORI                             |
| A \| B           | 001001     | OR / ORI                               |
| A & B            | 001000     | AND / ANDI                             |
| **Compare**      |            |                                        |
| B = A            | 010001     | BEQ / BNE                              |
| A >= B           | 100011     | BGE                                    |
| A >= B (U)       |            | BGEU                                   |
| A < B            | 010010     | SLT / BLT                              |
| A < B (U)        |            | SLTU / SLTIU / BLTU                    |
| **Shift**        |            |                                        |
| A << B           | 001100     | SLL / SLLI                             |
| A >> B           | 001101     | SRL / SRLI                             |
| A >> B (sign)    | 001111     | SRA / SRAI                             |
| **Multiply/Divide** |        |                                        |
| A * B            |            | MUL / MULH                             |
| A * B (U)        |            | MULHU / MULHSU                         |
| A / B            |            | DIV                                    |
| A / B (U)        |            | DIVU                                   |
| A % B            |            | REM                                    |
| A % B (U)        |            | REMU                                   |



* [0:1] selects which operation gets performed within the subunit
* [2:3] selects which subunit gets selected for the operation
* [4] 0 equals B normal, 1 equals B inverted
* [5] 0 equals A normal, 1 equals A inverted

---

More functionality can be added later, such as the multiplication extension requires.

## sources
* https://computationstructures.org/exercises/alu/lab.html