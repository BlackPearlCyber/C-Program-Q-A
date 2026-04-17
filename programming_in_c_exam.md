# ANNAPOORNA ENGINEERING COLLEGE  
*(An Autonomous Institution)*  

## B.E./B.Tech, M.E. DEGREE MODEL EXAMINATION – APRIL/MAY 2026  
### Semester II  
### INFORMATION TECHNOLOGY  
### 22CS201 – PROGRAMMING IN C  

**Time:** 3 Hours  
**Maximum Marks:** 100  

---

## PART – A (10 × 1 = 10 Marks)  
**Multiple Choice Questions – Answer All Questions**

1. Identify the valid identifier.  
   (a) @@123  
   (b) @123  
   (c) _123$  
   (d) Keyword  

2. What will be the output of the following program?
   ```c
   void main()
   {
       char str[] = "online\\0exam";
       printf("%s", str);
   }
   ```
   If input is given as 2 3, the output will be:  
   (a) 2.0 3.0  
   (b) 3.0 2.0  
   (c) 2 3  
   (d) Run time error  

3. What will be the output of the program?
   ```c
   void main()
   {
       char str[] = "online\\0exam";
       printf("%s", str);
   }
   ```
   (a) online\0exam  
   (b) online  
   (c) onlineexam  
   (d) exam  

4. Which symbol is commonly used to represent concatenation of strings?  
   (a) +  
   (b) &  
   (c) *  
   (d) -  

5. What will be the output of the following C program?
   ```c
   #include <stdio.h>
   int add(int a, int b)
   {
       return a + b;
   }
   void main()
   {
       int result = add(5, 3);
       printf("%d", result);
   }
   ```
   (a) 8  
   (b) 53  
   (c) Compiler Error  
   (d) done  

6. Pointer arithmetic is not possible on ___.  
   (a) Integer pointers  
   (b) Float pointers  
   (c) Character pointers  
   (d) Void pointers  

7. When a structure is an element to another structure, it is called as a ___.  
   (a) Union  
   (b) Structure within a structure  
   (c) Pointer to structure  
   (d) Array of structures  

8. The size of a union is ___.  
   (a) Sum of sizes of all members  
   (b) Predefined by the compiler  
   (c) Equal to size of largest data type  
   (d) None of these  

9. In which type of access does the system read or write records sequentially from the beginning to the end?  
   (a) Random access  
   (b) Direct access  
   (c) Sequential access  
   (d) Indexed access  

10. In C, what is the purpose of the argc parameter in the main function when handling command-line arguments?  
   (a) It stores the arguments as strings  
   (b) It indicates the number of command-line arguments  
   (c) It holds the program name  
   (d) It converts arguments to integers  

---

## PART – B (5 × 3 = 15 Marks)  

11. List types of operators in C.  
12. Define array and write syntax for declaring array.  
13. Write a C program to add two numbers without using return type.  
14. Differentiate between structure and union.  
15. Why is sequential access slower than random access for retrieving specific records in large files?  

---

## PART – C (5 × 15 = 75 Marks)  

16.  
(a) Write a C program to find the biggest of three numbers.  
OR  
(b) Write a C program to print the numbers in Fibonacci series using a while loop.  

17.  
(a) Write a C program for matrix addition using 2D array.  
OR  
(b) Write a C program to take 5 strings from the user and store them in a string and print the elements stored in the string.  

18.  
(a) Write a C program to find a factorial of a given number using pass by value and pass by reference.  
OR  
(b) Write a C program to find the largest element in an array using pointers.  

19.  
(a) Create a C program using structure called Employee which stores the name, id, basic pay, HRA and DA as members. Find the total pay of the employee.  
OR  
(b) Create a C program using a union called Student with name, class, rollnum, total marks as members. Find and display the grade of each student.  

80 – Grade A  
60 – Grade B  
50 – Grade C  
<50 – Fail  

20.  
(a) Explain in detail about sequential access and random access to a file with example.  
OR  
(b)  
i) Explain in detail about command line arguments.  
ii) Summarize file concepts with an example.  

---

# ANSWER KEY AND DETAILED SOLUTIONS

## PART - A Answers (with short reasoning)

1. **(c) _123$**  
   Identifiers can start with underscore, letters, or digits (not as first character). `@` is invalid in C identifiers.

2. **Question text appears mismatched** (program shown is string output, but options are numeric pairs).  
   Based on the shown code, output is **`online`** because `\0` terminates the string.

3. **(b) online**  
   The string literal `"online\0exam"` is printed only up to null terminator.

4. **(a) +**  
   In many languages and conceptual notation, `+` is used for concatenation. In C specifically, string concatenation is done using library functions like `strcat()`.

5. **(a) 8**  
   `add(5, 3)` returns `8`.

6. **(d) Void pointers**  
   Arithmetic on `void *` is not allowed in standard C because size of `void` is unknown.

7. **(b) Structure within a structure**  
   One structure member can itself be another structure.

8. **(c) Equal to size of largest data type**  
   Union members share same memory location.

9. **(c) Sequential access**  
   Records are processed in order, from beginning to end.

10. **(b) It indicates the number of command-line arguments**  
   `argc` stores count of arguments (including program name).

---

## PART - B Answers

### 11) Types of operators in C

1. Arithmetic: `+ - * / %`  
2. Relational: `== != > < >= <=`  
3. Logical: `&& || !`  
4. Assignment: `= += -= *= /= %=`  
5. Increment/Decrement: `++ --`  
6. Bitwise: `& | ^ ~ << >>`  
7. Conditional (ternary): `?:`  
8. Special/Miscellaneous: `sizeof`, comma `,`, address-of `&`, indirection `*`, member access `.` and `->`.

### 12) Define array and syntax

An **array** is a collection of elements of the same data type stored in contiguous memory locations and accessed using index.

Syntax:

```c
data_type array_name[size];
```

Examples:

```c
int marks[5];
float price[10];
char name[20];
```

### 13) C program to add two numbers without using return type

```c
#include <stdio.h>

void addTwoNumbers(int a, int b)
{
   int sum = a + b;
   printf("Sum = %d\n", sum);
}

int main(void)
{
   int x, y;
   printf("Enter two numbers: ");
   scanf("%d %d", &x, &y);

   addTwoNumbers(x, y); // function has no return value
   return 0;
}
```

### 14) Difference between structure and union

| Feature | Structure | Union |
|---|---|---|
| Memory allocation | Separate memory for each member | Shared memory for all members |
| Size | Approximately sum of member sizes (+ padding) | Size of largest member (+ alignment) |
| Simultaneous value storage | Yes | No (latest assigned member is valid) |
| Use case | Records with multiple fields together | Memory-saving when one of many fields is needed at a time |

### 15) Why sequential access is slower for specific records

In sequential access, to reach record `n`, the program must read records `1` to `n-1` first. For large files, this causes many unnecessary reads. In random access, file pointer jumps directly to required record position using functions like `fseek()`, so retrieval is faster for specific entries.

---

## PART - C Detailed Answers (with examples)

## 16(a) Biggest of three numbers

### Program

```c
#include <stdio.h>

int main(void)
{
   int a, b, c, biggest;

   printf("Enter three numbers: ");
   scanf("%d %d %d", &a, &b, &c);

   if (a >= b && a >= c)
   {
      biggest = a;
   }
   else if (b >= a && b >= c)
   {
      biggest = b;
   }
   else
   {
      biggest = c;
   }

   printf("Biggest number = %d\n", biggest);
   return 0;
}
```

### Example

Input: `45 78 32`  
Output: `Biggest number = 78`

### Explanation

The program compares each number using logical `&&` to check whether one number is greater than or equal to the other two.

---

## 16(b) Fibonacci series using while loop

### Program

```c
#include <stdio.h>

int main(void)
{
   int n, i = 0;
   int first = 0, second = 1, next;

   printf("Enter number of terms: ");
   scanf("%d", &n);

   printf("Fibonacci series: ");
   while (i < n)
   {
      if (i <= 1)
      {
         next = i;
      }
      else
      {
         next = first + second;
         first = second;
         second = next;
      }

      printf("%d ", next);
      i++;
   }

   printf("\n");
   return 0;
}
```

### Example

Input: `8`  
Output: `0 1 1 2 3 5 8 13`

### Explanation

Each new term is obtained by adding previous two terms.

---

## 17(a) Matrix addition using 2D array

### Program

```c
#include <stdio.h>

int main(void)
{
   int r, c, i, j;
   int a[10][10], b[10][10], sum[10][10];

   printf("Enter rows and columns: ");
   scanf("%d %d", &r, &c);

   printf("Enter first matrix elements:\n");
   for (i = 0; i < r; i++)
   {
      for (j = 0; j < c; j++)
      {
         scanf("%d", &a[i][j]);
      }
   }

   printf("Enter second matrix elements:\n");
   for (i = 0; i < r; i++)
   {
      for (j = 0; j < c; j++)
      {
         scanf("%d", &b[i][j]);
      }
   }

   for (i = 0; i < r; i++)
   {
      for (j = 0; j < c; j++)
      {
         sum[i][j] = a[i][j] + b[i][j];
      }
   }

   printf("Resultant matrix after addition:\n");
   for (i = 0; i < r; i++)
   {
      for (j = 0; j < c; j++)
      {
         printf("%d ", sum[i][j]);
      }
      printf("\n");
   }

   return 0;
}
```

### Example

Matrix A (2x2):

```text
1 2
3 4
```

Matrix B (2x2):

```text
5 6
7 8
```

Sum:

```text
6 8
10 12
```

### Explanation

Addition is done element by element: `sum[i][j] = a[i][j] + b[i][j]`.

---

## 17(b) Read 5 strings and print them

### Program

```c
#include <stdio.h>

int main(void)
{
   char words[5][50];
   int i;

   printf("Enter 5 strings:\n");
   for (i = 0; i < 5; i++)
   {
      scanf("%49s", words[i]);
   }

   printf("Stored strings are:\n");
   for (i = 0; i < 5; i++)
   {
      printf("%s\n", words[i]);
   }

   return 0;
}
```

### Example

Input strings: `C`, `programming`, `is`, `very`, `useful`  
Output will print all five strings line by line.

### Note

For multi-word strings (with spaces), use `fgets()` instead of `scanf("%s", ...)`.

---

## 18(a) Factorial using pass by value and pass by reference

### Program

```c
#include <stdio.h>

long long factorialByValue(int n)
{
   int i;
   long long fact = 1;
   for (i = 1; i <= n; i++)
   {
      fact *= i;
   }
   return fact;
}

void factorialByReference(int n, long long *result)
{
   int i;
   *result = 1;
   for (i = 1; i <= n; i++)
   {
      *result *= i;
   }
}

int main(void)
{
   int n;
   long long refFact;

   printf("Enter a number: ");
   scanf("%d", &n);

   printf("Factorial by value = %lld\n", factorialByValue(n));

   factorialByReference(n, &refFact);
   printf("Factorial by reference = %lld\n", refFact);

   return 0;
}
```

### Example

Input: `5`  
Output:

```text
Factorial by value = 120
Factorial by reference = 120
```

### Explanation

1. **Pass by value:** function returns computed value.  
2. **Pass by reference:** function writes result using pointer parameter.

---

## 18(b) Largest element in array using pointers

### Program

```c
#include <stdio.h>

int main(void)
{
   int n, i;
   int arr[100];
   int *ptr;
   int largest;

   printf("Enter number of elements: ");
   scanf("%d", &n);

   printf("Enter %d elements:\n", n);
   for (i = 0; i < n; i++)
   {
      scanf("%d", &arr[i]);
   }

   ptr = arr;
   largest = *ptr;

   for (i = 1; i < n; i++)
   {
      if (*(ptr + i) > largest)
      {
         largest = *(ptr + i);
      }
   }

   printf("Largest element = %d\n", largest);
   return 0;
}
```

### Example

Input: `6` and array `4 19 2 34 10 7`  
Output: `Largest element = 34`

### Explanation

Pointer arithmetic `*(ptr + i)` is used to access each array element.

---

## 19(a) Structure Employee with total pay

### Program

```c
#include <stdio.h>

struct Employee
{
   char name[50];
   int id;
   float basicPay;
   float hra;
   float da;
};

int main(void)
{
   struct Employee emp;
   float totalPay;

   printf("Enter employee name: ");
   scanf("%49s", emp.name);

   printf("Enter employee ID: ");
   scanf("%d", &emp.id);

   printf("Enter Basic Pay, HRA and DA: ");
   scanf("%f %f %f", &emp.basicPay, &emp.hra, &emp.da);

   totalPay = emp.basicPay + emp.hra + emp.da;

   printf("\nEmployee Details\n");
   printf("Name      : %s\n", emp.name);
   printf("ID        : %d\n", emp.id);
   printf("Basic Pay : %.2f\n", emp.basicPay);
   printf("HRA       : %.2f\n", emp.hra);
   printf("DA        : %.2f\n", emp.da);
   printf("Total Pay : %.2f\n", totalPay);

   return 0;
}
```

### Example

If Basic = `25000`, HRA = `5000`, DA = `3000`  
Total Pay = `33000`

### Explanation

Structure groups employee-related fields under one custom type.

---

## 19(b) Union Student and grade calculation

### Important Concept Note

A union cannot safely hold `name`, `class`, `rollnum`, and `total marks` simultaneously because all members share one memory location.  
For real student records, **structure** is correct.  
Below is a demonstration that includes a union (for exam requirement) and a structure (for practical correctness).

### Program

```c
#include <stdio.h>

union StudentUnion
{
   char name[50];
   char studentClass[20];
   int rollnum;
   float totalMarks;
};

struct Student
{
   char name[50];
   char studentClass[20];
   int rollnum;
   float totalMarks;
};

char findGrade(float marks)
{
   if (marks >= 80)
   {
      return 'A';
   }
   else if (marks >= 60)
   {
      return 'B';
   }
   else if (marks >= 50)
   {
      return 'C';
   }
   else
   {
      return 'F';
   }
}

int main(void)
{
   int n, i;
   struct Student s[50];

   printf("Enter number of students: ");
   scanf("%d", &n);

   for (i = 0; i < n; i++)
   {
      printf("\nStudent %d details\n", i + 1);
      printf("Enter name: ");
      scanf("%49s", s[i].name);

      printf("Enter class: ");
      scanf("%19s", s[i].studentClass);

      printf("Enter roll number: ");
      scanf("%d", &s[i].rollnum);

      printf("Enter total marks: ");
      scanf("%f", &s[i].totalMarks);
   }

   printf("\nStudent Grade Report\n");
   printf("---------------------------------------------\n");
   printf("Name\tClass\tRollNo\tMarks\tGrade\n");
   printf("---------------------------------------------\n");

   for (i = 0; i < n; i++)
   {
      printf("%s\t%s\t%d\t%.1f\t%c\n",
            s[i].name,
            s[i].studentClass,
            s[i].rollnum,
            s[i].totalMarks,
            findGrade(s[i].totalMarks));
   }

   return 0;
}
```

### Grade rule used

1. `marks >= 80` -> Grade A  
2. `marks >= 60` -> Grade B  
3. `marks >= 50` -> Grade C  
4. `marks < 50` -> Fail (F)

### Example

1. Marks `86` -> `A`  
2. Marks `67` -> `B`  
3. Marks `54` -> `C`  
4. Marks `41` -> `F`

---

## 20(a) Sequential access and random access (detailed)

### 1) Sequential Access

In sequential access, data is read/written in order from the beginning.

#### Characteristics

1. Simple and easy to implement.  
2. Good for log files, text reports, streaming processing.  
3. Slow when jumping to a specific record in large files.

#### Example (sequential read)

```c
#include <stdio.h>

int main(void)
{
   FILE *fp;
   int num;

   fp = fopen("numbers.txt", "r");
   if (fp == NULL)
   {
      printf("File open error\n");
      return 1;
   }

   while (fscanf(fp, "%d", &num) == 1)
   {
      printf("%d ", num);
   }

   fclose(fp);
   return 0;
}
```

### 2) Random Access

In random access, program jumps directly to a required position/record using file pointer movement.

#### Characteristics

1. Fast retrieval of specific records.  
2. Best for databases, indexed files, fixed-size record files.  
3. Slightly more complex than sequential access.

#### Example (random read using `fseek`)

```c
#include <stdio.h>

struct Record
{
   int id;
   float mark;
};

int main(void)
{
   FILE *fp;
   struct Record r;
   int recordNo = 3; // read 3rd record

   fp = fopen("records.dat", "rb");
   if (fp == NULL)
   {
      printf("File open error\n");
      return 1;
   }

   fseek(fp, (recordNo - 1) * sizeof(struct Record), SEEK_SET);

   if (fread(&r, sizeof(struct Record), 1, fp) == 1)
   {
      printf("ID: %d, Mark: %.2f\n", r.id, r.mark);
   }

   fclose(fp);
   return 0;
}
```

### Comparison summary

| Feature | Sequential | Random |
|---|---|---|
| Access style | One by one | Direct jump |
| Speed for specific record | Slow | Fast |
| Typical functions | `fscanf`, `fgets`, `fread` in loop | `fseek`, `ftell`, `rewind` |
| Suitable for | Full-file processing | Record-specific retrieval |

---

## 20(b)(i) Command line arguments (detailed)

### Definition

Command-line arguments are values supplied when running a program from terminal.

### Main function form

```c
int main(int argc, char *argv[])
```

1. `argc`: number of arguments (count).  
2. `argv`: array of strings containing arguments.  
3. `argv[0]`: program name/path.  
4. `argv[1] ... argv[argc-1]`: user-supplied arguments.

### Example program

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[])
{
   int i;

   printf("Total arguments = %d\n", argc);
   for (i = 0; i < argc; i++)
   {
      printf("argv[%d] = %s\n", i, argv[i]);
   }

   if (argc == 3)
   {
      int a = atoi(argv[1]);
      int b = atoi(argv[2]);
      printf("Sum = %d\n", a + b);
   }

   return 0;
}
```

### Sample run

Command:

```text
./a.out 12 8
```

Interpretation:

1. `argc = 3`  
2. `argv[0] = ./a.out`  
3. `argv[1] = 12`  
4. `argv[2] = 8`  
5. Printed sum = `20`

---

## 20(b)(ii) File concepts summary with example

### File basics in C

1. **File pointer:** `FILE *fp;`  
2. **Open file:** `fopen("name", "mode")`  
3. **Read/Write:** `fprintf`, `fscanf`, `fgets`, `fputs`, `fread`, `fwrite`  
4. **Close:** `fclose(fp)`  
5. **Pointer control:** `fseek`, `ftell`, `rewind`

### Common file modes

1. `"r"` read text  
2. `"w"` write text (overwrite/create)  
3. `"a"` append text  
4. `"rb"`, `"wb"`, `"ab"` binary modes  
5. `"r+"`, `"w+"`, `"a+"` read/write variants

### Example: write then read a text file

```c
#include <stdio.h>

int main(void)
{
   FILE *fp;
   char line[100];

   fp = fopen("sample.txt", "w");
   if (fp == NULL)
   {
      printf("Unable to open file for writing\n");
      return 1;
   }

   fprintf(fp, "C programming file example\n");
   fprintf(fp, "Second line\n");
   fclose(fp);

   fp = fopen("sample.txt", "r");
   if (fp == NULL)
   {
      printf("Unable to open file for reading\n");
      return 1;
   }

   printf("File content:\n");
   while (fgets(line, sizeof(line), fp) != NULL)
   {
      printf("%s", line);
   }

   fclose(fp);
   return 0;
}
```

### Output (example)

```text
File content:
C programming file example
Second line
```

---

## Quick Exam Writing Tips

1. Write algorithm steps before code for 15-mark questions.  
2. Use proper headers and function prototypes.  
3. Mention time complexity where possible (example: largest in array is `O(n)`).  
4. Show one sample input/output for every program.  
5. For union question, mention memory sharing limitation clearly.
