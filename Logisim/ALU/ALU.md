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
* [0:1] selects which operation gets performed within the subunit
* [2:3] selects which subunit gets selected for the operation
* [4] 0 equals B normal, 1 equals B inverted
* [5] 0 equals A normal, 1 equals A inverted

---

More functionality can be added later, such as the multiplication extension requires.

## sources
* https://computationstructures.org/exercises/alu/lab.html