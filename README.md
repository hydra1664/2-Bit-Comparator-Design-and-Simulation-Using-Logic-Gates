# 2-Bit Comparator Using Logic Gates

This is a simple project where I built and simulated a 2-bit digital comparator using only basic logic gates in Logisim Evolution. Instead of using the built-in comparator blocks, I created the logic manually with AND, OR, and NOT gates. The comparator checks two 2-bit binary numbers and tells whether the first number is equal to, greater than, or less than the second number.

All circuit files are available in the 'Circuit Files' folder, and all videos are in the 'Videos' folder.


## Overview

A 2-bit comparator has two inputs (A and B, each 2 bits wide) and three outputs:
- EQUAL → High when A equals B
- A_IS_GREATER → High when A is greater than B
- A_IS_LESSER → High when A is less than B

This project demonstrates how comparators work at the gate level without using prebuilt components.


## Circuit Design

### Inputs and Outputs
- Two 2-bit inputs: A (A1, A0) and B (B1, B0)  
- Three outputs: EQUAL, A_IS_GREATER, A_IS_LESSER  

### Splitters
The 2-bit inputs are split into single bits using splitters:
- A → A1 and A0
- B → B1 and B0

This makes it easier to connect individual bits to the logic blocks.

### Equality Logic
- EQ0 = (A0 AND B0) OR (NOT A0 AND NOT B0)
- EQ1 = (A1 AND B1) OR (NOT A1 AND NOT B1)
- EQUAL = EQ0 AND EQ1

This checks if both bits match.

### Greater Than Logic
- GT1 = A1 AND (NOT B1)
- GT0 = A0 AND (NOT B0)
- A_IS_GREATER = GT1 OR (EQ1 AND GT0)


### Less Than Logic
- LT1 = (NOT A1) AND B1
- LT0 = (NOT A0) AND B0
- A_IS_LESSER = LT1 OR (EQ1 AND LT0)



## Simulation

I tested the circuit with all possible input combinations (00 to 11 for both A and B). For each case, exactly one output goes high, which confirms the logic is working correctly.

https://github.com/user-attachments/assets/8358ec0b-df24-4746-b271-79106f38f792




## How to Use

1. Open the `.circ` file from the **Circuit Files** folder in Logisim Evolution.
2. Toggle the input values for A and B.
3. Watch the corresponding output LED light up for EQUAL, A_IS_GREATER, or A_IS_LESSER.


## Project Files

- Circuit Files → Contains the Logisim Evolution project files (`.circ`)
- Videos → Contains a demo video


## Conclusion

This was a fun way to understand how comparators work at the logic gate level. It shows how simple building blocks like AND, OR, and NOT gates can be combined to perform meaningful digital operations.

