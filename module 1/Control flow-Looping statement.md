# 🟨 Understand Control Flow – Looping Statements 🔄

> 🚀 **Loops** allow JavaScript to execute the same block of code **repeatedly** without writing the same code again and again.

### 🌟 Why do we need loops?

Imagine printing numbers from `1` to `100`.

❌ Without a loop:

```javascript
console.log(1);
console.log(2);
console.log(3);
// ...
console.log(100);
```

✅ With a loop:

```javascript
for (let i = 1; i <= 100; i++) {
    console.log(i);
}
```

---

# 🔄 1. `for` Loop

The `for` loop is commonly used when you **know how many times** you want to repeat something.

### 📌 Syntax

```javascript
for (initialization; condition; increment) {
    // code
}
```

### 💻 Example

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

### 🖥️ Output

```text
1
2
3
4
5
```

### 🧠 How it works

```text
Initialization
      ↓
  Condition
      ↓
    Code
      ↓
  Increment
      ↓
  Condition
      ↓
    Code
      ↓
     ...
```

### 🔍 Breaking it down

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

| Part             | Meaning         |
| ---------------- | --------------- |
| `let i = 1`      | Starting value  |
| `i <= 5`         | Condition       |
| `i++`            | Increase by 1   |
| `console.log(i)` | Code to execute |

---

# 🔁 2. `while` Loop

A `while` loop runs **as long as the condition is true**.

### 📌 Syntax

```javascript
while (condition) {
    // code
}
```

### 💻 Example

```javascript
let i = 1;

while (i <= 5) {
    console.log(i);
    i++;
}
```

### 🖥️ Output

```text
1
2
3
4
5
```

### 🧠 Flow

```text
       Condition
           ↓
      ┌────┴────┐
     TRUE      FALSE
      ↓           ↓
    Execute      Stop
      ↓
   Update
      ↓
  Condition
```

⚠️ **Important:** Make sure the condition eventually becomes false. Otherwise, you can create an **infinite loop**.

---

# 🔂 3. `do...while` Loop

The `do...while` loop is similar to `while`, but there is one important difference:

> ⭐ The code executes **at least once**, even if the condition is initially false.

### 📌 Syntax

```javascript
do {
    // code
} while (condition);
```

### 💻 Example

```javascript
let i = 1;

do {
    console.log(i);
    i++;
} while (i <= 5);
```

### 🖥️ Output

```text
1
2
3
4
5
```

### ⭐ Important Difference

```javascript
let i = 10;

while (i < 5) {
    console.log(i);
}
```

Output:

```text
Nothing
```

But:

```javascript
let i = 10;

do {
    console.log(i);
} while (i < 5);
```

Output:

```text
10
```

Because `do...while` **runs once before checking the condition**.

---

# 🔃 4. `for...of` Loop

The `for...of` loop is used to iterate over the **values of iterable objects**, especially arrays and strings.

### 💻 Example with Array

```javascript
let fruits = ["Apple", "Mango", "Banana"];

for (let fruit of fruits) {
    console.log(fruit);
}
```

### 🖥️ Output

```text
Apple
Mango
Banana
```

### 🍎 Think of it like this

```text
Array
  ↓
["Apple", "Mango", "Banana"]
  ↓
   for...of
  ↓
Apple
Mango
Banana
```

### 💻 Example with String

```javascript
let name = "Ajith";

for (let letter of name) {
    console.log(letter);
}
```

### 🖥️ Output

```text
A
j
i
t
h
```

---

# 🔢 5. `for...in` Loop

The `for...in` loop is mainly used to iterate over the **keys/property names of an object**.

### 💻 Example

```javascript
let student = {
    name: "Ajith",
    age: 21,
    course: "MERN"
};

for (let key in student) {
    console.log(key);
}
```

### 🖥️ Output

```text
name
age
course
```

### 🔍 Getting Values

```javascript
let student = {
    name: "Ajith",
    age: 21,
    course: "MERN"
};

for (let key in student) {
    console.log(key, ":", student[key]);
}
```

### 🖥️ Output

```text
name : Ajith
age : 21
course : MERN
```

---

# ⚔️ `for...of` vs `for...in`

This is an **important interview question**.

| 🔧 Loop    | 🎯 Gets               |
| ---------- | --------------------- |
| `for...of` | Values                |
| `for...in` | Keys / property names |

### Example

```javascript
let fruits = ["Apple", "Mango", "Banana"];

for (let fruit of fruits) {
    console.log(fruit);
}
```

Output:

```text
Apple
Mango
Banana
```

`for...of` → **values**

---

```javascript
let student = {
    name: "Ajith",
    age: 21
};

for (let key in student) {
    console.log(key);
}
```

Output:

```text
name
age
```

`for...in` → **keys**

> 💡 For arrays, prefer `for...of` when you want the elements. `for...in` is primarily intended for object properties.

---

# 🛑 6. `break`

The `break` statement **immediately stops a loop**.

### 💻 Example

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 5) {
        break;
    }

    console.log(i);
}
```

### 🖥️ Output

```text
1
2
3
4
```

When `i` becomes `5`, `break` stops the loop.

### 🧠 Flow

```text
1 → 2 → 3 → 4 → 5
                  ↓
                BREAK 🛑
                  ↓
                 STOP
```

---

# ⏭️ 7. `continue`

The `continue` statement **skips the current iteration** and moves to the next iteration.

### 💻 Example

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 3) {
        continue;
    }

    console.log(i);
}
```

### 🖥️ Output

```text
1
2
4
5
```

The number `3` is skipped.

### 🧠 Difference

```text
break
  ↓
STOP THE LOOP 🛑

continue
  ↓
SKIP CURRENT ITERATION ⏭️
```

---

# 🧩 8. Nested Loops

A **nested loop** means putting one loop **inside another loop**.

### 💻 Example

```javascript
for (let i = 1; i <= 3; i++) {

    for (let j = 1; j <= 3; j++) {
        console.log(i, j);
    }

}
```

### 🖥️ Output

```text
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

### 🧠 How it works

The **inner loop completes all its iterations** for every single iteration of the outer loop.

```text
Outer Loop
    │
    ├── Inner Loop
    │      ├── 1
    │      ├── 2
    │      └── 3
    │
    ├── Inner Loop
    │      ├── 1
    │      ├── 2
    │      └── 3
    │
    └── Inner Loop
           ├── 1
           ├── 2
           └── 3
```

---

# ⭐ Nested Loop Example – Pattern

Nested loops are commonly used to create patterns.

```javascript
for (let i = 1; i <= 5; i++) {

    let row = "";

    for (let j = 1; j <= i; j++) {
        row += "* ";
    }

    console.log(row);
}
```

### 🖥️ Output

```text
*
* *
* * *
* * * *
* * * * *
```

---

# 📊 Loop Comparison

| 🔄 Loop      | 🎯 Best Used When                 |
| ------------ | --------------------------------- |
| `for`        | Number of iterations is known     |
| `while`      | Repetition depends on a condition |
| `do...while` | Code must execute at least once   |
| `for...of`   | Need values from arrays/strings   |
| `for...in`   | Need keys from objects            |
| `break`      | Need to stop the loop             |
| `continue`   | Need to skip one iteration        |
| Nested loops | Need a loop inside another loop   |

---

# 🧠 🔑 Quick Revision

```text
🔄 for
   → Repeat a known number of times

🔁 while
   → Repeat while condition is true

🔂 do...while
   → Execute at least once

🔃 for...of
   → Get VALUES

🔢 for...in
   → Get KEYS

🛑 break
   → STOP the loop

⏭️ continue
   → SKIP current iteration

🧩 Nested loops
   → LOOP inside another LOOP
```

---

# 🎯 Mini Practice

Try these programs yourself:

### 🟢 Beginner

1. Print numbers from **1 to 10**.
2. Print numbers from **10 to 1**.
3. Print all **even numbers from 1 to 20**.
4. Find the **sum of numbers from 1 to 100**.

### 🟡 Intermediate

5. Print the **multiplication table** of a number.
6. Reverse a string using a loop.
7. Find the **largest number in an array**.
8. Use `for...of` to print all elements of an array.

### 🔴 Challenge

9. Create a **star pattern** using nested loops.
10. Create a program that finds **prime numbers from 1 to 100**.

> 🚀 **Next useful step:** practice these loops with small JavaScript programs before moving on to **Functions**.
