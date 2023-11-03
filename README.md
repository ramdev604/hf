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

<details>
<summary>RTL to GLS</summary>
<br>

## RTL Simulation

![2N](https://github.com/ramdev604/hf/assets/43489027/a10fcc38-6f50-4c48-9a3a-de56c6a331f8)


![N1](https://github.com/ramdev604/hf/assets/43489027/47ca6713-ea06-493a-b5f3-665a58664ed1)

## RTL Synthesis
![N3](https://github.com/ramdev604/hf/assets/43489027/c7ae2d19-fe8f-4dfa-bb1f-e20258619791)

## Gate-Level Simulation
![N4](https://github.com/ramdev604/hf/assets/43489027/3f1d309e-e50f-4f3a-8e18-6f60c0be1479)

</details>

<details>
<summary>OpenLane Flow</summary>
<br>

## Synthesis
- Type
```
run_synthesis
```
![1](https://github.com/ramdev604/hf/assets/43489027/f961af4d-abaa-4370-97e1-8ce77dcb2c89)


**Physical Cells**

![2](https://github.com/ramdev604/hf/assets/43489027/e33b97f4-0660-4acc-afeb-0eb3066927ed)


### Floorplan
- Now to run the floorplan we type
```
run_floorplan
```

- To view the design we type
```
magic -T /home/ramdev/OpenLane/sky130A/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.nom.lef def pes_half_adder.def &
```
![3](https://github.com/ramdev604/hf/assets/43489027/e05def79-ea43-4432-a0b6-35c51fae651b)


### Placement
- Now to run the placement we type
```
run_placement
```
![4](https://github.com/ramdev604/hf/assets/43489027/cae6882f-3724-44c9-bcf7-e21ac22a4ffa)


- To view the design we type
```
magic -T /home/ramdev/OpenLane/sky130A/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.nom.lef def pes_half_adder.def &
```

![5](https://github.com/ramdev604/hf/assets/43489027/8e3406c2-0785-4b21-a911-56fb720bb6c4)



### CTS(Clock Tree Synthesis)
- Now to run cts we type
```
run_cts
```

- The reports generated are given below

![6](https://github.com/ramdev604/hf/assets/43489027/09b3713c-8d8b-4aec-9f3d-4ca97483d105)


**Power Report**

![7](https://github.com/ramdev604/hf/assets/43489027/2e92c12b-f7db-4c17-bb42-19288cbb04c7)



**Summary and Area Report**

![8](https://github.com/ramdev604/hf/assets/43489027/4c4232e0-ed0b-4ad5-b152-854a650cd02b)

![9](https://github.com/ramdev604/hf/assets/43489027/34bdeb7c-6951-46d0-b9dc-a2873a24711b)

### Routing
- Now to run routing we type
```
run_routing
```

- To view the design we type
```
magic -T /home/ramdev/OpenLane/sky130A/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.nom.lef def pes_half_adder.def &
```
![10](https://github.com/ramdev604/hf/assets/43489027/e58c7b5b-51f6-46a3-b24a-d65d30be19b5)

![11](https://github.com/ramdev604/hf/assets/43489027/9c984265-5d02-43bb-a2d8-90fd7a863f76)

**Congestion Report**

![12](https://github.com/ramdev604/hf/assets/43489027/1420dd71-8541-4725-89f1-3d05260e69c2)


**Power Report**

![13](https://github.com/ramdev604/hf/assets/43489027/c0212d6c-7719-4f15-b480-5a944e9f915c)

**Summary Report and Area Report**

![14](https://github.com/ramdev604/hf/assets/43489027/a1b6e865-b710-49d5-b180-c08837f31fe4)

**Statistics**
- Area = 55 um2
- Internal Power = 8.15e-08 W
- Switching Power = 1.85e-07
- Leakage Power = 1.03e-10
- Total Power = 2.66e-07

</details>
