# How Does JavaScript Work?

## 🤔 Why it's needed

When you write JavaScript, the computer **cannot understand it directly**.

JavaScript needs a **JavaScript Engine** to convert your code into machine code so the CPU can execute it.

---

## 🌍 Real-world Example

Imagine you speak **English**, but your friend only understands **Japanese**.

You need a **translator**.

```text
You (English)
      ↓
 Translator
      ↓
Friend (Japanese)
```

Similarly,

```text
JavaScript Code
        ↓
JavaScript Engine
        ↓
Machine Code
        ↓
CPU
```

The **JavaScript Engine** acts as the translator.

---

## 🧠 How JavaScript Works

### Step 1: Write JavaScript Code

```javascript
console.log("Hello, World!");
```

↓

### Step 2: JavaScript Engine Reads the Code

The browser contains a JavaScript engine.

Examples:

| Browser | JavaScript Engine |
| ------- | ----------------- |
| Chrome  | V8                |
| Edge    | V8                |
| Firefox | SpiderMonkey      |
| Safari  | JavaScriptCore    |

↓

### Step 3: Engine Parses the Code

The engine checks:

- Syntax errors
- Variable declarations
- Function definitions

If there is an error, execution stops.

↓

### Step 4: Engine Compiles the Code

Modern JavaScript engines use **Just-In-Time (JIT) Compilation**.

They convert JavaScript into optimized machine code while the program is running.

↓

### Step 5: CPU Executes the Code

The CPU executes the machine code.

Output:

```text
Hello, World!
```

---

## 🔄 JavaScript Execution Flow

```text
JavaScript Code
        ↓
JavaScript Engine
        ↓
Parser
        ↓
JIT Compiler
        ↓
Machine Code
        ↓
CPU
        ↓
Output
```

---

## ✍️ Example

```javascript
let a = 10;
let b = 20;

console.log(a + b);
```

### What happens internally?

1. Engine reads the code.
2. Checks for syntax errors.
3. Converts it into machine code.
4. CPU executes the instructions.
5. Output is displayed.

```text
30
```

---

## 💻 Example Queries

```javascript
console.log("Hello");

let name = "Yesu";

let sum = 10 + 20;

alert("Welcome!");
```

All of these go through the same execution process.

---

## ❓ Common Interview Questions

### Q1. Can the CPU understand JavaScript directly?

**No.** It only understands machine code.

---

### Q2. What converts JavaScript into machine code?

**JavaScript Engine** (e.g., V8, SpiderMonkey, JavaScriptCore).

---

### Q3. What is JIT Compilation?

A technique where the JavaScript engine compiles code into optimized machine code **while the program is running**, making execution faster.

---

### Q4. Which JavaScript engine is used in Google Chrome?

**V8 Engine**

---

## 📝 Practice Exercises

- Write a simple JavaScript program and trace its execution.
- Learn the difference between **Parser**, **Compiler**, and **Interpreter**.
- Read about the **V8 Engine** architecture.

---

## ⚠️ Common Mistakes

❌ Thinking the CPU understands JavaScript directly.

❌ Believing JavaScript is only interpreted.

❌ Forgetting that modern engines use **JIT Compilation**.

---

## 🔁 Revision Summary

- JavaScript cannot run directly on the CPU.
- A **JavaScript Engine** executes JavaScript code.
- The engine parses the code, compiles it using **JIT**, and converts it into machine code.
- The CPU executes the machine code and produces the output.

### Easy Flow to Remember

```text
JavaScript Code
      ↓
JavaScript Engine
      ↓
Parser
      ↓
JIT Compiler
      ↓
Machine Code
      ↓
CPU
      ↓
Output
```
