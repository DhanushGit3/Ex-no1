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

|<img width="1600" height="1180" alt="WhatsApp Image 2026-05-14 at 11 28 22 AM" src="https://github.com/user-attachments/assets/c8f3f392-8267-40cf-8bd2-f5dbb5a8cf94" />


#### Manual Calculations

<img width="1600" height="1160" alt="WhatsApp Image 2026-05-14 at 11 28 34 AM" src="https://github.com/user-attachments/assets/1a94d708-b14d-4805-a672-8967beac57de" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1600" height="1240" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (1)" src="https://github.com/user-attachments/assets/34efc5f7-cb7e-4c2e-b387-bd67a83a2782" />


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

<img width="1599" height="1013" alt="WhatsApp Image 2026-05-14 at 11 29 05 AM" src="https://github.com/user-attachments/assets/0651f66a-fd3f-493d-8bfa-bdfe4cf75b0d" />


#### Manual Calculations
<img width="1490" height="1440" alt="WhatsApp Image 2026-05-14 at 11 29 15 AM" src="https://github.com/user-attachments/assets/f67b13a2-f226-4625-8dcc-10a3a1ee072c" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1075" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM" src="https://github.com/user-attachments/assets/ec42d9e3-09a5-4965-b2f7-a4df8bce121c" />


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
<img width="1600" height="1008" alt="WhatsApp Image 2026-05-14 at 11 29 42 AM" src="https://github.com/user-attachments/assets/35dcc946-b31c-40e1-a4ee-735d9b64ddfa" />


#### Manual Calculations
<img width="1600" height="1236" alt="WhatsApp Image 2026-05-14 at 11 29 57 AM" src="https://github.com/user-attachments/assets/2b547d0a-1a49-49b0-b923-ea9fe66a9ca2" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="1074" alt="WhatsApp Image 2026-05-14 at 11 06 30 AM (2)" src="https://github.com/user-attachments/assets/b0f4ab1c-97a0-471e-a435-41eec1b8ea92" />


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
<img width="1600" height="973" alt="WhatsApp Image 2026-05-14 at 11 30 37 AM" src="https://github.com/user-attachments/assets/d9bda2ae-8f94-490f-90ae-a92e0c0c00a1" />


#### Manual Calculations
<img width="1600" height="426" alt="WhatsApp Image 2026-05-14 at 11 31 07 AM" src="https://github.com/user-attachments/assets/f22627e4-dd4c-4ffb-9d38-47ea4e594415" />

## OUTPUT FROM MASM SOFTWARE
<img width="1600" height="1099" alt="WhatsApp Image 2026-05-14 at 11 06 31 AM" src="https://github.com/user-attachments/assets/429cb5a8-74fe-4418-a84c-daf83bddc381" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

