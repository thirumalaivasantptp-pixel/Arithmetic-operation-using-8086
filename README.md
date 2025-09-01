# THIRUMALAIVASAN J
# 212224060287
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
|-------------------------|--------------------------|
|      1200:12              |1204 :24                    |
|      1201 :34            |1205:68                     |
|      1202:12              |1206:00                     |
|      1203:34              | 1207:C4                        |
#### Manual Calculations
<img width="579" height="1280" alt="image" src="https://github.com/user-attachments/assets/69fdb034-211a-4888-8dcf-ae8300177983" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="627" height="402" alt="addprg" src="https://github.com/user-attachments/assets/adfddf54-36a1-486c-9775-3d90d2b33784" />
<img width="629" height="388" alt="addout" src="https://github.com/user-attachments/assets/e66ff4ff-ff07-4c15-8b6e-5fc184b4ee3c" />



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
|    1200:12                     |1204:00                          |
|1201:34|1205:00|
|1202:12|1206:00|
|1203:34|1207:C4|
#### Manual Calculations


<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/fe427ba6-c1d4-4ae5-b053-3cf3c6919092" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="626" height="398" alt="subprg" src="https://github.com/user-attachments/assets/b4df029b-1766-46aa-936d-6b4f880d6989" />
<img width="631" height="396" alt="subout" src="https://github.com/user-attachments/assets/d27f9c78-bfae-457c-86a9-b8e098446e8f" />

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
| 1200:12                       |   1204:44                       |
|1201:34|1205:51|
|1202:12|1206:97|
|1203:34|1207:0A|
#### Manual Calculations

<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/52a26bf3-1078-449d-80db-16644cbb1f0e" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="630" height="377" alt="mulprog" src="https://github.com/user-attachments/assets/db2c1132-67c6-4603-aaf5-026f1fa27e49" />
<img width="628" height="386" alt="mulout" src="https://github.com/user-attachments/assets/5a3d04ae-3880-4e92-bb49-fbf88718a49f" />

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
|  1200:12                       |     1204:01                     |
|1201:34|1205:00|
|1202:12|1206:00|
|1203:34|1207:00|
#### Manual Calculations
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/079f5bcb-2f86-403f-a7cc-34b13e09363f" />

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE

<img width="635" height="398" alt="divprog" src="https://github.com/user-attachments/assets/11826072-bebe-4912-8f50-b0cb54981269" />
<img width="642" height="401" alt="divout" src="https://github.com/user-attachments/assets/058b45bd-9afc-4912-8dfd-1954cd072c11" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
