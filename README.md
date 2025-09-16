# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:

    CMC
    LDA 4200H
    MOV C,A
    LXI H,4201H
    MOV A,M
    INX H
    DCR C
    LOOP: CMP M
    JNC NEXT
    MOV A,M
    NEXT: INX H
    DCR C
    JNZ LOOP
    STA 4300H
    HLT

## Output:

<img width="1896" height="1061" alt="image" src="https://github.com/user-attachments/assets/e5b29560-a61b-4778-900d-5af9e1b12e99" />

<img width="304" height="497" alt="image" src="https://github.com/user-attachments/assets/33bf1278-daa8-4aae-81cf-0126aff1e1e6" />

<img width="295" height="483" alt="image" src="https://github.com/user-attachments/assets/15b2207e-6316-4ba5-aa01-6ab07580ecbd" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:

    CMC
    LDA 4200H
    MOV C,A
    LXI H,4201H
    MOV A,M
    INX H
    DCR C
    LOOP: CMP M
    JC NEXT
    MOV A,M
    NEXT: INX H
    DCR C
    JNZ LOOP
    STA 4301H
    HLT

## Output:

<img width="1915" height="1105" alt="image" src="https://github.com/user-attachments/assets/a3c55d53-a5fc-414d-aaa8-d3a2d2278303" />

<img width="307" height="602" alt="image" src="https://github.com/user-attachments/assets/a6c62eba-2fb4-4c22-8200-23c5d8661372" />

<img width="309" height="502" alt="image" src="https://github.com/user-attachments/assets/772af046-6a1a-479d-88ab-dab10b9e3ebf" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
