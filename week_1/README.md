### Week Challenge (Tuesday)

---

#### 1. Interpreted And Compiled Programming Languages

- <strong>Interpreted</strong>: It is not necessary to create an intermediate program to execute the application as the code is executed by the machine, the detection of any error is performed at the time of interpretation.
- <strong>Compiler</strong>: Before executing the program the code is scanned for execution and if there is an error it is not feasible to run the program.

#### 2. Is Java compiled or interpreted, or both?

First is compelled to by code (javac) and then interpreted by a Java virtual machine

---

```
Taking note:
1. Task list, what should I do or what I need?
2. raw material
3. Pseudocode
  - Capitalize initial words (READ, WRITE, IF, ELSE, WHILE)
  - Knowing the hierarchy (Sequence, Selection, Looping)
  - Structuring the pseudocode
  - Checking step by step
```

#### 3. Pseudocode currency converter

Convert dollar to bitcoin algorithm

Raw material

- I have dollars
- need to know the current price to bitcoin
- input amount of dollar(s)
- convert dollars to bitcoin
- Process
- return the convertion

```
1. START
2. dllr <-- dollar
3. btcn <-- price to bitcoin (https://www.coindesk.com/price/bitcoin/)
4. convert <-- dllr * btcn
5. PRINT btcn
6. END
```

### Week Challenge (Wednesday)

#### 1. Your date of birth in the matrix?

Writing the age to binary

- task

  - Write the age
  - substranting below the chart

```
  age = 1982
  Process: Subtraction based on the table below.

 1982 - 1024 = 958 |
 958 - 512 = 446
 446 - 256 = 190
 190 - 128 = 62
 62 - 32 = 30
 30 - 16 = 14
 14- 8 = 6
 6 - 4 = 2
 2 - 2 = 0

| 1024 | 512 | 256 | 128 |  64 |  32 |  16 |  8  |  4  |  2  |  1  |
|:---: |:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|  1   |  1  |  1  |  1  |  0  |  1  |  1  |  1  |  1  |  1  |  0  |


1982 in `binary` is: 11110111110

```

#### 2. MIPS

```
.data
        welcome: .asciiz "\n================= Welcome =================\n"
        result: .asciiz "\nThe result is: "
        number_one_msg: .asciiz "\nEnter the first number: "
        number_two_msg: .asciiz "\nEnter the second number: "
  .text
        main:
              # welcome message
              li $v0, 4
              la $a0, welcome
              syscall

              # user input
              li $v0, 4
              la $a0, number_one_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t0, $v0

              # user input
              li $v0, 4
              la $a0, number_two_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t1, $v0

              # adding the user numbers
              add $t2, $t0, $t1

              # showing result number
              li $v0, 4
              la $a0, result
              syscall

              # printing number
              li $v0, 1
              move $a0, $t2
              syscall
```

### Week Challenge (Tursday)

#### 1. Print special numbers

> <p>In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise</p>
> ps: the exercise was denote (even number, not 1 to 100)

```js
For;
for (var i = 0; i <= 100; i++) {
  if (i % 2 == 0) console.log(i);
}
```

```js
While;
var i = 0;
while (i <= 100) {
  if (i % 2 == 0) console.log(i);
  i++;
}
```

```js
var i = 0;
do {
  if(i % 2 == 0)console.log(i);
  i++
}
```

#### 2. Bad Code

<p>The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code</p>

```js
var cond = false;

if ((cond = true)) {
  console.log("The cond variable is true");
} else {
  console.log("The cond variable is false");
}
```

Process

- The conditional `if` declaration was assigned again for "cond", and was replaced to `==`

```js
var cond = false;

if (cond == true) {
  console.log("The cond variable is true");
} else {
  console.log("The cond variable is false");
}
```

#### 3. Bad Code

<p>You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly</p>

```js
var n = 100;

if (n == 100) {
  console.log("This is a special number!");
}
if (n < 1000) {
  console.log("");
} else {
  console.log("Just a regular number");
}
if (n % 10 == 0) {
  console.log("This number is multiple of 10");
}
```

##### Procedure

1.  it was worked with conditional from 0 to 1000.
2.  I was in error, don´t write `else if` only `if`

```js
var n = 100;

if (n == 100) {
  console.log("This is a special number!");
} else if (n < 1000 && n % 10 == 0) {
  console.log("This number is almost special");
} else {
  console.log("Just a regular number");
}
```
