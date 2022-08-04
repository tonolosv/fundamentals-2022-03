# <center>Javascript - Week 2</center>

### Week challenges (Tuesday)

#### Multiply

<p>This code does not execute properly. Try to figure out why.</p>

```js
This code does not execute properly. Try to figure out why.

function multiply(a, b){
  a * b
}
```

##### Procedure

1. The `return` was missing in the function

```js
function multiply(a, b) {
  return a * b;
}
```

#### ASCII Total

You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:

```js
uniTotal("a") == 97 uniTotal("aaa") == 291
```

##### Procedure

- A new variable has been generated `total`
- iterate the parameters `str` and save in `total`, then call the function `chartCodeAt()` to know the equivalents in ASCII

```js
function uniTotal(str) {
  let total = 0;
  for (let i = 0, length = str.length; i < length; i++) {
    total += str[i].charCodeAt();
  }
  return total;
}

uniTotal("b");
```

#### Char From ASCII Value

Write a function `get_char()` / `getChar()` which takes a number and returns the corresponding ASCII char for that value.
example

```js
function getChar(c) {
  // ...
}
```

##### Procedure

- convert `c` to string
- used function `fromCharCode` to search equivalance into ascii table

```js
function getChar(c) {
  return String.fromCharCode(c);
}
```

#### Binary Addition

Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.
The binary number returned should be a string.

Example (Input1, Input2 --> Output (explanation)))

```js
1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)

function addBinary(a,b) {

}
```

##### Procedure

- was created a new variable `sum`
- both parameters are added together and kept in `sum`
- then, the new variable uses the toString() function and uses (2) to convert to binary

```js
function addBinary(a, b) {
  let sum = a + b;
  return sum.toString(2);
}
```

---
