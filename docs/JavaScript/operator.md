# Operator

### Operator

<hr>

An operator creates one value by performing arithmetic, assignment, comparison, logic, and type operations on one or more expressions. At this time, the object of the operation is called an operand. The operand is also an expression because it is evaluated and become a single value, and also an expression that combines the operand with the operator is expression.

### Arithmetic Operator

<hr>

The Arithmetic Operator performs a mathematical computation on the operands to produce new numeric values. If arithmetic is not possible, NaN is returned.

Arithmetic operators can be classified into dyadic arithmetic operators and unary arithmetic operators according to the number of operands.

#### Dyadic arithmetic operators

<hr>

Dyadic arithmetic operators perform arithmetic operations on two operands to produce numeric type values.

All dyadic arithmetic operators have no side effects that change the value of the operand. In other words, any arithmetic operation does not change the value of the operand. It always creates new values.

| Operator | Meaning   | Example |
| -------- | --------- | ------- |
| +        | Plus      | a + b   |
| -        | Subtract  | a - b   |
| \*       | Multiply  | a \* b  |
| /        | Division  | a / b   |
| %        | Remainder | a % b   |

A few things to keep in mind when using arithmetic dyadic operators.

-   The result is a floating point even if you divide the integer.

```javascript
7 / 2; // 3.5
```

-   The operand of the remaining operators(%) is floating point.

The sign is the same as first operand.

```javascript
15 % 4; // 3
5 % 1.5; // 0.5
```

-   If one of the operands is a string, the + operator makes remaining operands to string

```javascript
1 + "2 month"; //  12 month
//Change the number 1 to the string "1" and combine it with "2 month".
```

Others

If it can not be calculated, it is evaluated as NaN. It evaluates to 1 if the operand of the arithmetic operator is true, or to 0 if false and null. If undefined, it evaluates to NaN.

```javascript
0 / 0; // NaN
"One" * 1; // NaN
true + true; // 2
1 + null; // 1
1 + undefined; // NaN
```

#### Unary arithmetic operator

<hr>

Unary arithmetic operators perform arithmetic operations on a single operand to produce a numeric type value. Note that unlike dyadic arithmetic operators, the increment / decrement (++ / --) operator has side effects that change the value of the operand. In other words, the increment / decrement operation changes the value of the operand.

| Operator | Meaning                 | Example | Example meaning                                   |
| -------- | ----------------------- | ------- | ------------------------------------------------- |
| ++       | Increase operator       | a++     | Plus 1 to a then then evaluate the value of a     |
|          |                         | ++a     | Evaluate the value of a then plus 1 to a          |
| --       | Decrease operator       | a--     | Subtract 1 to a then then evaluate the value of a |
|          |                         | --a     | Evaluate the value of a then subtract 1 to a      |
| +        | Do not process anything | +a      | Evaluate to the same value as a.                  |
| -        | Sign inversion          | -a      | Evaluate the value after invert the sign of a     |

```javascript
let x = 3;
let y;

// Postfix increment operator
y = x++;
console.log(y, x); // 3 4

// Prefix increment operator
y = ++x;
console.log(y, x); // 5 5

// Postfix decrement operator
y = x--;
console.log(y, x); // 5 4

// Prefix decrement operator
y = --x;
console.log(y, x); // 3 3
```

#### Assignment Operator

<hr>

| Operator | Example | Meaning    |
| -------- | ------- | ---------- |
| +=       | a += b  | a = a + b  |
| -=       | a -= b  | a = a - b  |
| \*=      | a \*= b | a = a \* b |
| /=       | a /= b  | a = a / b  |
| %=       | a %= b  | a = a % b  |

```javascript
let x;

x = 10;
console.log(x); // 10

x += 5; // x = x + 5;
console.log(x); // 15

x -= 5; // x = x - 5;
console.log(x); // 10

x *= 5; // x = x * 5;
console.log(x); // 50

x /= 5; // x = x / 5;
console.log(x); // 10

x %= 5; // x = x % 5;
console.log(x); // 0
```

#### Comparison Operator

<hr>

| Operator | Meaning               | Example | Description                                                      |
| -------- | --------------------- | ------- | ---------------------------------------------------------------- |
| ==       | Loose equality        | a == b  | true if a and b are equal in value, false otherwise              |
| !=       | Inequality            | a != b  | true if a and b are not equal in value, false otherwise          |
| ===      | Strict equality       | a === b | true if a and b are equal in value and type, false otherwise     |
| !==      | Strict inequality     | a !== b | true if a and b are not equal in value and type, false otherwise |
| >        | Greater than          | a > b   | true if a value is greater than b, false otherwise               |
| <        | Less than             | a < b   | true if b value is greater than a, false otherwise               |
| >=       | Greater than or equal | a >= b  | true if a value is greater than or equal b, false otherwise      |
| <=       | Less than or equal    | a <= b  | true if b value is greater than or equal a, false otherwise      |

```javascript
let a = [1, 2, 3];
let b = [1, 2, 3];
let c = a;

console.log(a == b); // false
console.log(a == c); // true
```

```javascript
null == undefined; // true
1 == "1"; // true
"oxff" == 255; // true
true == 1; // true
true == "1"; // true
```

```javascript
null === undefined; // false
1 === "1"; // false
"oxff" === 255; // false
true === 1; // false
true === "1"; // false
NaN === NaN; // false
```

#### Logical Operator

<hr>

| Operator | Meaning     | Example  | Description                                    |
| -------- | ----------- | -------- | ---------------------------------------------- |
| &&       | Logical AND | a && b   | true if both a and b are true, false otherwise |
|          | Logical OR  | a \|\| b | true if either a or b is true, false otherwise |
| !        | Logical NOT | !a       | false if a is true, true if a is false         |
