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

    Operation:      Instruction:
    1. A+B			    ADD/SUB/ADDI/LW/SW/LB/LH/JAR/JALR
    2. A+B(U) 		  LBU/LHU
    3. XOR			    XOR/XORI
    4. A|B			    OR/ORI
    5. A&B			    AND
    6. B=A			    BEQ/BNE
    7. A>=B			    BGE		
    8. A>=B(U)		  BGEU
    9. A<<B			    SLL/SLLI/LUI/AUIPC
    10. A>>B		    SRL/SRLI
    11. A>>B(sign)	SRA/SRAI
    12. A<B			    SLT/BLT/		
    13	A<B(U)		  SLTU/SLTIU/BLTU
    14. A*B			    MUL/MULH/		
    15 	A*B(U)		  MULHU/MULHSU
    16. A/B			    DIV
    17. A/B(U)		  DIVU
    18. A%B			    REM
    19. A%B(U)		  REMU

* [0:1] selects which operation gets performed within the subunit
* [2:3] selects which subunit gets selected for the operation
* [4] 0 equals B normal, 1 equals B inverted
* [5] 0 equals A normal, 1 equals A inverted

---

More functionality can be added later, such as the multiplication extension requires.

## sources
* https://computationstructures.org/exercises/alu/lab.html