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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200h               |        1204h             |
|     1201h               |        1205h             |
|     1202h               |        1206h             |
|     1203h               |                          |
#### Manual Calculations
![WhatsApp Image 2025-08-28 at 21 27 43_02c4d1d9](https://github.com/user-attachments/assets/9f9dcf2d-591d-48fb-ad50-e14bf1296379)


## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-08-28 at 22 15 26_92431a10](https://github.com/user-attachments/assets/450c4460-d501-4ae5-9650-8409acb9ca55)
![WhatsApp Image 2025-08-28 at 22 15 26_bef6113e](https://github.com/user-attachments/assets/4b38bb91-332d-4e41-a7f8-47a386b71ca2)



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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200h           |        1204h             |
|         1201h           |        1205h             |
|         1202h           |        1206h             |
|         1203h           |                          |
#### Manual Calculations
![WhatsApp Image 2025-08-28 at 21 27 43_b76bfa71](https://github.com/user-attachments/assets/038825f2-68eb-4c8c-acf9-315949fdf60a)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-28 at 22 38 08_549d92db](https://github.com/user-attachments/assets/4929ca5a-099d-45f4-8536-9d34fefcb188)
![WhatsApp Image 2025-08-28 at 22 38 08_21d26718](https://github.com/user-attachments/assets/876f23fe-40a5-47a6-96de-76bda157ba88)



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200h             |       1204h              |
|       1201h             |       1205h              |
|       1202h             |       1206h              |
|       1203h             |       1207h              |

#### Manual Calculations
![WhatsApp Image 2025-08-28 at 21 27 44_b7ffa708](https://github.com/user-attachments/assets/089dd6aa-7cd4-4140-a288-06a304ade783)


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 23 26 39_289434a3](https://github.com/user-attachments/assets/dddcb462-f706-4b6b-88ce-ddad81aeb59e)
![WhatsApp Image 2025-08-31 at 23 26 40_beb7de6d](https://github.com/user-attachments/assets/0ed3c616-3460-4587-a22b-d8eb13b1190d)



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200h             |        1204h             |
|       1201h             |        1205h             |
|       1202h             |        1206h             |
|       1203h             |        1207h             |

#### Manual Calculation
![WhatsApp Image 2025-08-28 at 21 27 45_854d571d](https://github.com/user-attachments/assets/cb6cd1e0-cfbc-4c63-9e82-d209297c9c07)




---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-08-31 at 23 27 09_ab874e9f](https://github.com/user-attachments/assets/75032b56-5071-4ec6-9681-5142366efb12)
![WhatsApp Image 2025-08-31 at 23 27 10_2e59a139](https://github.com/user-attachments/assets/9d298fe5-f68b-4813-8f4b-55ac8841eae9)





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
