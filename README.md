# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
![WhatsApp Image 2026-02-07 at 8 52 51 AM](https://github.com/user-attachments/assets/75bd515a-ef78-4b4c-a3a9-6cf9deda7112)



#### Manual Calculations

![WhatsApp Image 2026-02-07 at 8 55 49 AM](https://github.com/user-attachments/assets/7b1b9b50-1f79-4970-a19c-d48b3c43f3f5)


## OUTPUT IMAGE FROM MASM SOFTWARE
![545469491-f886c07c-a47e-4c42-b770-907b84b68136](https://github.com/user-attachments/assets/7bd2fc38-5aba-4d95-ac66-f9b2b99e129e)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table
![WhatsApp Image 2026-02-07 at 8 58 36 AM](https://github.com/user-attachments/assets/00371cf0-bbf2-4b49-bc65-325a9fb0949f)


#### Manual Calculations

![WhatsApp Image 2026-02-07 at 8 59 30 AM](https://github.com/user-attachments/assets/7ea4d539-d7a4-4b89-b03d-e4eedc4a1447)

## OUTPUT
![545469491-f886c07c-a47e-4c42-b770-907b84b68136](https://github.com/user-attachments/assets/becaecdf-19df-4f91-884c-d2d0cac00790)
 SCREEN FROM MASM SOFTWARE

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

![WhatsApp Image 2026-02-07 at 9 02 42 AM](https://github.com/user-attachments/assets/9e4d2215-cd44-4837-be9b-ce6511504cd4)



#### Manual Calculations


![WhatsApp Image 2026-02-07 at 9 04 52 AM](https://github.com/user-attachments/assets/3d098588-1a4e-4e84-bcb1-9850229f9f76)



## OUTPUT SCREEN FROM MASM SOFTWARE

![545471118-e7529d98-daa0-4526-87a0-6e9885052b8c](https://github.com/user-attachments/assets/462ab9a3-e3cf-4bfd-b10a-cfc974889372)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

![WhatsApp Image 2026-02-07 at 9 04 52 AM](https://github.com/user-attachments/assets/2b2e68b3-c6c6-4a3e-999c-ad8f3be31ecb)

                    |                          |

#### Manual Calculations

![WhatsApp Image 2026-02-07 at 9 08 17 AM](https://github.com/user-attachments/assets/e276c045-192c-48c9-b28b-1660d7032b03)


## OUTPUT FROM MASM SOFTWARE

![545471048-ef7a2adf-0ed2-4d76-910e-f3ef9e31fb37](https://github.com/user-attachments/assets/52804b58-4e6e-4098-b261-40c2314be83c)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

