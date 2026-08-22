# 🟨 Understand Operators and Expressions in JavaScript

> 💡 **Operators** are symbols used to perform operations on values and variables.
> 🧩 **Expressions** are combinations of values, variables, and operators that produce a result.

```js
let result = 10 + 5;
console.log(result);
```

**Output:**

```text
15
```

---

## 🧮 1. Arithmetic Operators

Arithmetic operators are used for **mathematical calculations**.

| Operator | Name              | Example  | Result |
| :------: | ----------------- | -------- | -----: |
|    `+`   | ➕ Addition        | `10 + 5` |   `15` |
|    `-`   | ➖ Subtraction     | `10 - 5` |    `5` |
|    `*`   | ✖️ Multiplication | `10 * 5` |   `50` |
|    `/`   | ➗ Division        | `10 / 5` |    `2` |
|    `%`   | 🧮 Modulus        | `10 % 3` |    `1` |
|   `**`   | 🚀 Exponentiation | `2 ** 3` |    `8` |

### 💻 Example

```js
let a = 10;
let b = 3;

console.log(a + b);  // 13
console.log(a - b);  // 7
console.log(a * b);  // 30
console.log(a / b);  // 3.333...
console.log(a % b);  // 1
console.log(a ** b); // 1000
```

---

# 🔍 2. Relational Operators

Relational operators are used to **compare two values**.

The result is usually:

```text
true ✅
```

or

```text
false ❌
```

| Operator | Meaning                 | Example       |
| :------: | ----------------------- | ------------- |
|    `>`   | Greater than            | `10 > 5`      |
|    `<`   | Less than               | `5 < 10`      |
|   `>=`   | Greater than or equal   | `10 >= 10`    |
|   `<=`   | Less than or equal      | `5 <= 10`     |
|   `==`   | Equal value             | `10 == "10"`  |
|   `===`  | Equal value & type      | `10 === "10"` |
|   `!=`   | Not equal               | `10 != 5`     |
|   `!==`  | Not equal value or type | `10 !== "10"` |

### ⭐ `==` vs `===`

```js
console.log(10 == "10");
```

Output:

```text
true
```

But:

```js
console.log(10 === "10");
```

Output:

```text
false
```

### 🏆 Best Practice

```text
Prefer === and !==
```

because they check both **value and data type**.

---

# 🧠 3. Logical Operators

Logical operators are used to **combine multiple conditions**.

### 🔗 AND `&&`

Both conditions must be true.

```js
let age = 25;

console.log(age >= 18 && age <= 60);
```

Output:

```text
true
```

---

### 🔀 OR `||`

At least **one condition** must be true.

```js
let age = 15;

console.log(age < 18 || age > 60);
```

Output:

```text
true
```

---

### 🔄 NOT `!`

Reverses the result.

```js
let isLoggedIn = true;

console.log(!isLoggedIn);
```

Output:

```text
false
```

### 📌 Quick Reference

| Operator | Name   | Meaning             |       |                           |
| :------: | ------ | ------------------- | ----- | ------------------------- |
|   `&&`   | 🔗 AND | Both must be true   |       |                           |
|     `    |        | `                   | 🔀 OR | At least one must be true |
|    `!`   | 🔄 NOT | Reverses the result |       |                           |

---

# ✏️ 4. Assignment Operators

Assignment operators are used to **store or update values**.

### `=` Basic Assignment

```js
let x = 10;
```

Here:

```text
x ← 10
```

---

### 📋 Compound Assignment Operators

| Operator | Example   | Equivalent   |
| :------: | --------- | ------------ |
|    `=`   | `x = 5`   | `x = 5`      |
|   `+=`   | `x += 5`  | `x = x + 5`  |
|   `-=`   | `x -= 5`  | `x = x - 5`  |
|   `*=`   | `x *= 5`  | `x = x * 5`  |
|   `/=`   | `x /= 5`  | `x = x / 5`  |
|   `%=`   | `x %= 5`  | `x = x % 5`  |
|   `**=`  | `x **= 2` | `x = x ** 2` |

### 💻 Example

```js
let score = 10;

score += 5;
console.log(score); // 15

score *= 2;
console.log(score); // 30

score -= 10;
console.log(score); // 20
```

---

# 🔼 5. Increment & Decrement

These operators increase or decrease a value by **1**.

### ⬆️ Increment `++`

```js
let count = 5;

count++;

console.log(count);
```

**Output:**

```text
6
```

### ⬇️ Decrement `--`

```js
let count = 5;

count--;

console.log(count);
```

**Output:**

```text
4
```

---

## 🔄 Prefix vs Postfix

### Postfix `x++`

```js
let x = 5;

let y = x++;

console.log(x); // 6
console.log(y); // 5
```

👉 **Use first → Increase later**

---

### Prefix `++x`

```js
let x = 5;

let y = ++x;

console.log(x); // 6
console.log(y); // 6
```

👉 **Increase first → Use later**

### 🧠 Easy Trick

```text
x++  → Use → Increase
++x  → Increase → Use
```

---

# 🎯 6. Operator Precedence

When multiple operators appear in one expression, JavaScript needs to know **which operation to perform first**.

Example:

```js
let result = 10 + 5 * 2;

console.log(result);
```

JavaScript performs multiplication first:

```text
5 × 2 = 10

10 + 10 = 20
```

Therefore:

```text
20
```

---

## 📊 Common Precedence Order

```text
🥇  ()
     Parentheses

🥈  **
     Exponentiation

🥉  *  /  %
     Multiplication, Division, Modulus

4️⃣  +  -
     Addition, Subtraction

5️⃣  >  <  >=  <=
     Relational

6️⃣  ==  ===  !=  !==
     Equality

7️⃣  &&
     Logical AND

8️⃣  ||
     Logical OR

9️⃣  =  +=  -=  *=
     Assignment
```

### 💡 Remember

```text
()
 ↓
**
 ↓
* / %
 ↓
+ -
 ↓
Comparison
 ↓
Logical
 ↓
Assignment
```

---

# 🛑 7. Parentheses Change the Order

Without parentheses:

```js
let result = 10 + 5 * 2;

console.log(result);
```

Output:

```text
20
```

With parentheses:

```js
let result = (10 + 5) * 2;

console.log(result);
```

Output:

```text
30
```

### ⭐ Best Practice

Use parentheses when they make your code **easier to understand**.

---

# 🧩 8. Complete Example

```js
let age = 20;
let hasID = true;

// 🧮 Arithmetic
let nextAge = age + 1;

// 🔍 Relational
let isAdult = age >= 18;

// 🧠 Logical
let canEnter = age >= 18 && hasID;

// ✏️ Assignment
age += 5;

// 🔼 Increment
age++;

// 🔽 Decrement
age--;

console.log("Next Age:", nextAge);
console.log("Is Adult:", isAdult);
console.log("Can Enter:", canEnter);
console.log("Age:", age);
```

---

# 📝 9. Quick Revision

```text
🧮 Arithmetic
   +  -  *  /  %  **

🔍 Relational
   >  <  >=  <=  ==  ===  !=  !==

🧠 Logical
   &&  ||  !

✏️ Assignment
   =  +=  -=  *=  /=  %=

🔼 Increment / Decrement
   ++  --

🎯 Precedence
   () → ** → * / % → + - → Comparison
   → Logical → Assignment
```

---

# 🚀 Key Points to Remember

> 🔹 **Arithmetic** → Perform calculations
> 🔹 **Relational** → Compare values
> 🔹 **Logical** → Combine conditions
> 🔹 **Assignment** → Store/update values
> 🔹 **`++` / `--`** → Increase/decrease by 1
> 🔹 **Precedence** → Decides which operation happens first
> 🔹 **Parentheses `()`** → Can control evaluation order
> 🔹 **`===`** → Usually preferred over `==`

---

## 🎯 Practice Challenge

Try predicting the output before running this:

```js
let x = 10;
let y = 5;

let result = x + y * 2;

console.log(result);
console.log(x > y);
console.log(x === "10");
```

**Next, a good topic to learn is `if, else, and switch`**, because operators are heavily used in conditional statements.
