# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Greater number is: 80

---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55

---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

## PROGRAM

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

```
DECLARE
    num1 NUMBER;
    num2 NUMBER;
BEGIN
    num1 := &num1;
    num2 := &num2;

    IF num1 > num2 THEN
        DBMS_OUTPUT.PUT_LINE('Greater Number: ' || num1);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greater Number: ' || num2);
    END IF;
END;
/
```

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

```
DECLARE
    num NUMBER := 10;
    sum NUMBER := 0;
    i   NUMBER := 1;
BEGIN
    WHILE i <= num LOOP
        sum := sum + i;
        i := i + 1;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || num || ' natural numbers is: ' || sum);
END;
/
```

## 3. Write a PL/SQL program to generate Fibonacci series

```
DECLARE
    n    NUMBER := 1535;
    temp NUMBER;
    rem  NUMBER;
    rev  NUMBER := 0;
BEGIN
    temp := n;

    WHILE temp > 0 LOOP
        rem  := temp MOD 10;
        rev  := rev * 10 + rem;
        temp := FLOOR(temp / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('n = ' || n);
    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
END;
/
```

## 4. Write a PL/SQL Program to display the number in Reverse Order

```
DECLARE
    n       NUMBER := 1535;
    rem     NUMBER;
    rev     NUMBER := 0;
    temp    NUMBER;
BEGIN
    temp := n;      -- keep original number

    WHILE temp > 0 LOOP
        rem  := temp MOD 10;         -- extract last digit
        rev  := rev * 10 + rem;      -- build reversed number
        temp := FLOOR(temp / 10);    -- remove last digit
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('n = ' || n);
    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
END;
/

```
## 5. Write a PL/SQL program to find the largest of three numbers

```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
    largest NUMBER;
BEGIN
    IF a > b AND a > c THEN
        largest := a;
    ELSIF b > a AND b > c THEN
        largest := b;
    ELSE
        largest := c;
    END IF;

    DBMS_OUTPUT.PUT_LINE('a = ' || a || ', b = ' || b || ', c = ' || c);
    DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || largest);
END;
/
```

## OUTPUT

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

<img width="1014" height="786" alt="Screenshot 2025-10-31 113507" src="https://github.com/user-attachments/assets/e138d038-720c-4f58-b8b7-cd9aa8d37dd3" />

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

<img width="997" height="867" alt="Screenshot 2025-10-31 114426" src="https://github.com/user-attachments/assets/b0767de8-3658-4803-b524-ae527893cc23" />

## 3. Write a PL/SQL program to generate Fibonacci series

<img width="995" height="515" alt="Screenshot 2025-10-31 114919" src="https://github.com/user-attachments/assets/4db8efdd-e0e4-4d0b-8576-acd8e2e9d168" />
<img width="1010" height="274" alt="Screenshot 2025-10-31 115037" src="https://github.com/user-attachments/assets/88bdd794-1bd6-4a4e-accf-5bfcca9b163f" />

## 4. Write a PL/SQL Program to display the number in Reverse Order

<img width="882" height="940" alt="image" src="https://github.com/user-attachments/assets/a964d395-9da6-4bf9-a851-85b7a1732920" />

## 5. Write a PL/SQL program to find the largest of three numbers

<img width="888" height="983" alt="image" src="https://github.com/user-attachments/assets/99216244-5384-4f4e-8835-f4619194b269" />

## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.

