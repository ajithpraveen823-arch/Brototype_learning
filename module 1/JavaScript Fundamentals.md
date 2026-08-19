# 🟨 Understand JavaScript Fundamentals

## 1. What is JavaScript? 🌐

JavaScript (JS) is a high-level, dynamic programming language mainly used to make web pages interactive and dynamic.

- HTML → Structure
- CSS → Styling
- JavaScript → Behavior & Logic

### 🔥 Where is JavaScript used?

JavaScript is used in many areas:

- 🌐 Web Development — Interactive websites
- 🖥️ Backend Development — Using Node.js
- 📱 Mobile Apps — React Native
- 🖥️ Desktop Apps — Electron
- 🎮 Game Development
- ☁️ Cloud & Server Applications
- 🤖 Automation and scripting

Example
```javascript
let name = "Ajith";

console.log("Hello " + name);
```

Output:

```
Hello Ajith
```

## 2. JavaScript Execution Flow ⚙️

When JavaScript code runs, several things happen.

### Basic flow

JavaScript Code
```
      ↓
JavaScript Engine
      ↓
Parse the Code
      ↓
Compile / Optimize
      ↓
Execute
      ↓
Output
```

Example
```javascript
let a = 10;
let b = 20;

let sum = a + b;

console.log(sum);
```

Execution

Step 1: Create variables

```
a = 10
b = 20
```

Step 2: Calculate

```
sum = 10 + 20
```

Step 3: Print

```
30
```

### 🧠 JavaScript Engine

A JavaScript engine is software that understands and executes JavaScript code.

Popular engines:

| Environment | JavaScript Engine |
|-------------|-------------------|
| Google Chrome | V8 |
| Node.js | V8 |
| Firefox | SpiderMonkey |
| Safari | JavaScriptCore |
| Microsoft Edge | V8 |

## 3. Running JavaScript 🚀

JavaScript can be executed in different environments.

### A. JavaScript in the Browser 🌐

Browsers such as Chrome, Firefox, Edge and Safari contain JavaScript engines.

You can run JavaScript directly inside an HTML file.

Example
```html
<!DOCTYPE html>
<html>
<head>
    <title>JavaScript Example</title>
</head>
<body>

    <h1>JavaScript Demo</h1>

    <script>
        console.log("Hello JavaScript!");
        alert("Welcome to JavaScript!");
    </script>

</body>
</html>
```

The browser loads the HTML and executes the JavaScript.

Browser flow

```
HTML
 ↓
Browser
 ↓
JavaScript Engine
 ↓
Execute JavaScript
 ↓
Web Page / Console / DOM
```

### B. JavaScript with Node.js 🟢

Node.js allows JavaScript to run outside the browser.

It is commonly used for backend/server-side development.

Example:

```javascript
console.log("Hello from Node.js!");
```

Save it as:

```
app.js
```

Run it using:

```
node app.js
```

Output:

```
Hello from Node.js!
```

Node.js flow

```
JavaScript File
      ↓
Node.js
      ↓
V8 JavaScript Engine
      ↓
Execute Code
      ↓
Terminal / Server
```

Browser vs Node.js

| Feature | Browser | Node.js |
|---------|---------|---------|
| Runs JavaScript | ✅ | ✅ |
| JavaScript Engine | V8 / others | V8 |
| DOM available | ✅ | ❌ |
| document available | ✅ | ❌ |
| Server development | Limited | ✅ |
| File system access | Restricted | ✅ |
| console.log() | ✅ | ✅ |

## 4. Compilation vs Interpretation 🧩

Traditionally, programming languages were explained using two approaches.

### 🟦 Compilation

A compiler translates the source code into another form before execution.

```
Source Code
     ↓
Compiler
     ↓
Machine Code
     ↓
Execute
```

Examples traditionally associated with compilation:

- C
- C++
- Rust

### 🟩 Interpretation

An interpreter executes the source code through an interpreter rather than producing a standalone machine-code executable first.

```
Source Code
     ↓
Interpreter
     ↓
Execute
```

### ⚡ Modern JavaScript

JavaScript is not simply "interpreted" anymore.

Modern JavaScript engines use a combination of:

- Parsing
- Compilation
- Interpretation
- Just-In-Time (JIT) compilation
- Runtime optimization

For example, Google's V8 engine used by Chrome and Node.js can compile JavaScript into optimized machine code while the program is running.

Simplified modern flow

```
JavaScript Source
       ↓
     Parser
       ↓
Intermediate Representation
       ↓
Interpreter / Compiler
       ↓
Optimized Machine Code
       ↓
      CPU
```

💡 Important: For beginners, remember: JavaScript engines process and execute JavaScript using both interpretation and compilation techniques.

## 🎯 Quick Revision

JavaScript

- JavaScript is a programming language used to create interactive and dynamic applications.

Execution

- Code → JavaScript Engine → Execute → Output

Browser

- HTML → Browser → JS Engine → JavaScript

Node.js

- JS File → Node.js → V8 → JavaScript

Compilation

- Converts code into a form that can be executed, traditionally before running.

Interpretation

- Executes code through an interpreter during program execution.

Modern JavaScript

- Modern engines use both interpretation and JIT compilation/optimization.

## 🚀 One-Line Summary

JavaScript is executed by JavaScript engines such as V8, and it can run both inside browsers and outside browsers using Node.js.
