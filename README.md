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
|  1200: 12               |  1204: 24                |
|  1201: 34               |  1205: 68                |
|  1202: 12               |  1206: 00                |
|  1203: 34               |  1207: c4                |


#### Manual Calculations

![WhatsApp Image 2025-09-01 at 21 58 40_3e81746a](https://github.com/user-attachments/assets/e53e9099-706b-4a08-8310-2b2c7c949e9d)


## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-01 at 21 48 59_7c3a5b9b](https://github.com/user-attachments/assets/f97a0bc5-837e-4965-a145-1c29e63459ff)


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
MOV SI,1200H
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
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200: 12              |  1204: 00                |
|   1201: 34              |  1205: 00                |
|   1202: 12              |  1206: 00                |
|   1203: 34              |  1207: c4                |
### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 10 53_8f011080](https://github.com/user-attachments/assets/5f3a7642-139d-467f-a4a1-2eeba2cadbf8)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-01 at 22 19 33_8964076e](https://github.com/user-attachments/assets/c249dbc1-8d23-4600-97b6-9a50b8c06036)


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
|    1200: 12             |   1204: 44               |
|    1201: 34             |   1205: 51               |
|    1202: 12             |   1206: 97               |
|    1203: 34             |   1207: 0A               |
#### Manual Calculations
![WhatsApp Image 2025-09-01 at 22 32 31_624f54db](https://github.com/user-attachments/assets/8030c6e5-0ac9-4858-a078-ff29c3c96a06)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-01 at 22 28 39_689ac07c](https://github.com/user-attachments/assets/6dd758a2-41d5-4fc5-92c2-6b79ecf32d66)

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
|  1200: 12               |  1204: 01                |
|  1201: 34               |  1205: 00                |
|  1202: 12               |  1206: 00                |
|  1204: 34               |  1207: 00                |
#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 44 36_250f8ce4](https://github.com/user-attachments/assets/2da891dc-5516-4e82-9dcf-5cd7aa91ed29)

## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-01 at 22 42 24_2d4a55d5](https://github.com/user-attachments/assets/7299df41-ddae-41d1-8ba9-0a43ff6017fe)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
