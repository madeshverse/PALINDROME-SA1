# PALINDROME-SA1

# 8051 Assembly - Palindrome Checker

## Description
- Compares bytes in memory from address 50H to 56H.
- Displays Y on Port 1 if it’s a palindrome.
- Displays N otherwise.

## Algorithm
1. Load data at memory locations (e.g., 50H, 51H, 52H, 53H, 54H, 55H, 56H).
2. Compare first and last bytes, move inward.
3. If all match → output Y; otherwise N.

## Procedure
1. Create new 8051 project.
2. Add palindrome.asm to the project.
3. Assemble and build.
4. Start Debug session.
5. Open *Memory Window* and initialize data at 50H–56H.
6. Run or Step (F11) to test.

## Program
MOV R2,#03

MOV R0,#50H

MOV R1,#56H

L1: MOV A,@R0

    MOV B,@R1
   
    CJNE A,B,NOTPALIN
    
    INC R0
    
    DEC R1
    
    DJNZ R2,L1

    MOV P1,#'Y'
    
    SJMP HERE

NOTPALIN: MOV P1,#'N'

HERE: SJMP HERE

## Output

<img width="385" height="203" alt="Screenshot 2025-11-05 173030" src="https://github.com/user-attachments/assets/1408048d-9de0-4d4c-91ff-bc269930ab89" />

<img width="385" height="203" alt="Screenshot 2025-11-05 173030" src="https://github.com/user-attachments/assets/adc67aa7-a68b-4ae3-9ee3-1d39889a3206" />

## Result 
Thus palindrome in microcontroller 8051 is verified.
