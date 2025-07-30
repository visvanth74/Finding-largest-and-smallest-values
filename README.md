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
## output:
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
## output:
## Result:
Thus the program to find smallest number in an array was executed.

