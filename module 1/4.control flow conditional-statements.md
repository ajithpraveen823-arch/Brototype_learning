# 🟨 Understand Control Flow – Conditional Statements

> 🚦 **Control Flow** decides **which code should run, when it should run, and how the program makes decisions.**

---

## 🌟 1. `if` Statement

The `if` statement runs a block of code **only when a condition is `true`**.

### 📌 Syntax

```javascript
if (condition) {
    // code to execute
}
```

### 💻 Example

```javascript
let age = 20;

if (age >= 18) {
    console.log("You are an adult");
}
```

### 🖥️ Output

```text
You are an adult
```

### 🧠 Flow

```text
        Condition
            │
       ┌────┴────┐
      TRUE     FALSE
       │          │
    Execute      Skip
      code       code
```

---

# 🔥 2. `if...else` Statement

Use `if...else` when there are **two possible outcomes**.

### 📌 Syntax

```javascript
if (condition) {
    // condition is true
} else {
    // condition is false
}
```

### 💻 Example

```javascript
let age = 16;

if (age >= 18) {
    console.log("You can vote");
} else {
    console.log("You cannot vote");
}
```

### 🖥️ Output

```text
You cannot vote
```

### 🎯 Real-Life Example

```text
Is age >= 18?
      │
   ┌──┴──┐
  YES    NO
   │      │
Vote   Cannot Vote
```

---

# 🚀 3. `else if` Statement

When you need to check **multiple conditions**, use `else if`.

### 📌 Syntax

```javascript
if (condition1) {

} else if (condition2) {

} else if (condition3) {

} else {

}
```

### 💻 Example – Grade Calculator

```javascript
let marks = 85;

if (marks >= 90) {
    console.log("Grade A+");
} else if (marks >= 80) {
    console.log("Grade A");
} else if (marks >= 70) {
    console.log("Grade B");
} else if (marks >= 60) {
    console.log("Grade C");
} else {
    console.log("Fail");
}
```

### 🖥️ Output

```text
Grade A
```

### ⚠️ Important

JavaScript checks conditions **from top to bottom**.

```text
Condition 1 ❌
     ↓
Condition 2 ✅
     ↓
Execute Condition 2
     ↓
Stop checking
```

---

# 🧩 4. Nested Conditions

A **nested condition** means putting one conditional statement **inside another conditional statement**.

### 💻 Example

```javascript
let age = 20;
let hasLicense = true;

if (age >= 18) {

    if (hasLicense) {
        console.log("You can drive");
    } else {
        console.log("You need a license");
    }

} else {
    console.log("You are too young to drive");
}
```

### 🖥️ Output

```text
You can drive
```

### 🧠 Structure

```text
Age >= 18?
   │
 ┌─┴─┐
YES  NO
 │    │
 │    └── Too young
 │
License available?
 │
 ┌┴──┐
YES  NO
 │    │
Drive  Need license
```

---

# 🎮 5. `switch` Statement

The `switch` statement is useful when checking **one value against multiple fixed values**.

### 📌 Syntax

```javascript
switch (expression) {

    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
```

### 💻 Example

```javascript
let day = 2;

switch (day) {

    case 1:
        console.log("Monday");
        break;

    case 2:
        console.log("Tuesday");
        break;

    case 3:
        console.log("Wednesday");
        break;

    default:
        console.log("Invalid day");
}
```

### 🖥️ Output

```text
Tuesday
```

---

## 🛑 Why do we use `break`?

`break` stops the `switch` statement after a matching case.

```javascript
case 1:
    console.log("Monday");
    break;
```

Without `break`, JavaScript can continue into the next cases.

### ⭐ `default`

`default` runs when **no case matches**.

```javascript
let fruit = "Apple";

switch (fruit) {

    case "Mango":
        console.log("Mango");
        break;

    case "Banana":
        console.log("Banana");
        break;

    default:
        console.log("Unknown fruit");
}
```

Output:

```text
Unknown fruit
```

---

# ⚡ 6. Ternary Operator `? :`

The **ternary operator** is a short way to write a simple `if...else`.

### 📌 Syntax

```javascript
condition ? valueIfTrue : valueIfFalse;
```

### 🔄 Normal `if...else`

```javascript
let age = 20;

if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}
```

### ⚡ Using Ternary

```javascript
let age = 20;

let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

### 🖥️ Output

```text
Adult
```

### 🧠 Easy Formula

```text
condition ? true : false
```

Think of it as:

```text
          condition
              │
        ┌─────┴─────┐
       TRUE        FALSE
        │             │
    "Adult"        "Minor"
```

---

# 📊 `if` vs `switch` vs `ternary`

| 🔧 Statement | 🎯 Best Use                  |
| ------------ | ---------------------------- |
| `if`         | One condition                |
| `if...else`  | Two outcomes                 |
| `else if`    | Multiple conditions          |
| Nested `if`  | Conditions inside conditions |
| `switch`     | Multiple fixed values        |
| `ternary`    | Simple `if...else`           |

---

# 🌍 Real-World Example

Imagine an online shopping website:

```javascript
let amount = 2500;

if (amount >= 5000) {
    console.log("20% Discount");
} else if (amount >= 3000) {
    console.log("10% Discount");
} else if (amount >= 1000) {
    console.log("5% Discount");
} else {
    console.log("No Discount");
}
```

### 🖥️ Output

```text
5% Discount
```

---

# 🧠 🔑 Quick Revision

```text
if
 ↓
Check one condition

if...else
 ↓
Choose between two options

else if
 ↓
Check multiple conditions

Nested if
 ↓
Condition inside another condition

switch
 ↓
Compare one value with multiple cases

ternary
 ↓
Short form of if...else
```

---

# 🏆 Practice Challenges

Try these yourself 💪:

### 🟢 Beginner

1. Check whether a number is **positive or negative**.
2. Check whether a person is **eligible to vote**.
3. Check whether a number is **even or odd**.

### 🟡 Intermediate

4. Find the **largest of three numbers**.
5. Create a **grade calculator**.
6. Create a **calculator using `switch`**.

### 🔴 Challenge

7. Create a **login system** using nested conditions.
8. Create a **student result system** using `if...else if`.
9. Check **even/odd using the ternary operator**.

> 🚀 **Next topic:** Learn **Loops (`for`, `while`, `do...while`)** to repeat code efficiently.
