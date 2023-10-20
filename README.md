# Half Adder
A half adder is a simple digital circuit used in digital electronics and computer science to perform basic binary addition. It can add two single-digit binary numbers (0 or 1) and produce two outputs: a sum and a carry. The half adder is one of the building blocks for more complex digital circuits, such as full adders and arithmetic logic units (ALUs).

A half adder has two inputs, typically labeled A and B, which represent the binary numbers to be added. It produces two outputs:

1) Sum (S): This output represents the result of adding the two binary digits. The sum is calculated as follows:

    S = A XOR B (XOR stands for exclusive OR operation)

2) Carry (C): This output represents the carry that is generated when adding the two binary digits. The carry is calculated as follows:

    C = A AND B (AND stands for logical AND operation)


Here's a truth table for a half adder:

![table](https://github.com/ramdev604/hf/assets/43489027/00c81a55-07e1-4ab2-859d-d7c19796cd0b)

As you can see from the truth table, when both A and B are 0, the sum and carry are both 0. When one of them is 1, the sum is 1, and the carry is 0. When both A and B are 1, the sum is 0 (as this is equivalent to binary 10), and the carry is 1.

The half adder is a fundamental building block for more complex arithmetic operations in digital circuits, and it is often used as part of larger circuits to perform addition and subtraction operations on binary numbers.

## RTL Simulation

![2N](https://github.com/ramdev604/hf/assets/43489027/a10fcc38-6f50-4c48-9a3a-de56c6a331f8)


![N1](https://github.com/ramdev604/hf/assets/43489027/47ca6713-ea06-493a-b5f3-665a58664ed1)

## RTL Synthesis
![N3](https://github.com/ramdev604/hf/assets/43489027/c7ae2d19-fe8f-4dfa-bb1f-e20258619791)

## Gate-Level Simulation
![N4](https://github.com/ramdev604/hf/assets/43489027/3f1d309e-e50f-4f3a-8e18-6f60c0be1479)
