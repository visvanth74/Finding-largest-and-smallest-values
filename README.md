# Finding largest and smallest-values
## Exp: 2 (a). Find largest Number From an array
## Aim : 
To find the largest Number From an array. 
## Apparatus required: 
8085 Simulator, PC. 
## Algorithm:
1. Start the program
2. Initialize a memory pointer (using HL register pair) to point to the starting address of the array.
3. Load the count of numbers in the array into a register (say, register B).
4. Increment the memory pointer to point to the first data element.
5. Load the first element into the Accumulator (A) – this is the initial largest number.
6. Decrement the count by 1 since the first number is already considered.
7. Repeat the following steps until the count becomes 0:
8. Increment the memory pointer to move to the next element.
9. Compare the current memory element with the value in Accumulator.
10. If the current element is greater than the Accumulator content:
<br> Move the current element into the Accumulator (update the largest).
<br> Decrement the count.
11. After all elements are checked, the Accumulator will contain the largest number.
12. Store the content of the Accumulator (i.e., the largest number) in memory at the required address.
13. End the program.
## Program:
; Program to find the greatest number using I/O Ports<br>
IN 01H ; Read first number<br>
MOV D, A ; Assume first number is greatest<br>
IN 02H ; Read second number<br>
CMP D<br>
JC NEXT2 ; If A < D, skip update<br>
MOV D, A ; Else update greatest<br>
NEXT2:<br>
IN 03H ; Read third number<br>
CMP D<br>
JC NEXT3<br>
MOV D, A<br>
NEXT3:<br>
IN 04H ; Read fourth number<br>
CMP D<br>
JC NEXT4<br>
MOV D, A<br>
NEXT4:<br>
IN 05H ; Read fifth number<br>
CMP D<br>
JC DONE<br>
MOV D, A<br>
DONE: MOV A, D<br>
OUT 06H ; Output greatest number at port 06H<br>

<img width="1494" height="611" alt="image" src="https://github.com/user-attachments/assets/7c752de8-2cba-4b85-9c07-e72acb49ff53" />

Input Ports (numbers are read from these ports):
● 01H → First number<br>
● 02H → Second number<br>
● 03H → Third number<br>
● 04H → Fourth number<br>
● 05H → Fifth number<br>
## output:
Output Port:
● 06H → Greatest number

## Result:
Thus the program to find largest number in an array was executed.
## Exp: 2 (b) Find smallest No. from an array.
## Aim: 
To find the smallest No. from an array. Apparatus required: 8085 Simulator, PC. 
## Algorithm:
1. Start the program.
2. Initialize the HL register pair to point to the starting address of the array.
3. Load the count of elements from memory into a register (e.g., register B).
4. Increment HL to point to the first data element.
5. Load the first data into the Accumulator (A) – assume this is the smallest number initially.
6. Decrement the count (B) by 1 because the first number is already loaded.
7. Repeat the following steps until the count becomes 0:
8. Increment HL to point to the next data element.
<br>Compare the content of memory (M) with the Accumulator (A).
<br>If M < A, move M to Accumulator (update the smallest number).
<br>Decrement the count (B).
9. After the loop ends, the Accumulator holds the smallest number.
10. Store the content of the Accumulator in a desired memory location (e.g., 4300H).
11. End the program.
## Program:
; Program to find the smallest number using I/O Ports<br>
IN 01H ; Read first number<br>
MOV D, A ; Assume first number is smallest<br>
IN 02H ; Read second number<br>
CMP D<br>
JNC NEXT2 ; If A >= D, skip update<br>
MOV D, A ; Else update smallest<br>
NEXT2:<br>
IN 03H ; Read third number<br>
CMP D<br>
JNC NEXT3<br>
MOV D, A<br>
NEXT3:<br>
IN 04H ; Read fourth number<br>
CMP D<br>
JNC NEXT4<br>
MOV D, A<br>
NEXT4:<br>
IN 05H ; Read fifth number<br>
CMP D<br>
JNC DONE<br>
MOV D, A<br>
DONE: MOV A, D<br>
OUT 07H ; Output smallest number at port 07H<br>
HLT<br>

<img width="1484" height="609" alt="image" src="https://github.com/user-attachments/assets/ee63f23e-e1ec-46fa-8cfb-e823053456bc" />

Input Ports (numbers are read from these ports):
● 01H → First number<br>
● 02H → Second number<br>
● 03H → Third number<br>
● 04H → Fourth number<br>
● 05H → Fifth number<br>
## output:
● 06H → Smallest number
## Result:
Thus the program to find smallest number in an array was executed.

