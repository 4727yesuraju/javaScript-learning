# Why JavaScript is Called an Interpreted Language

JavaScript is traditionally called an **interpreted language** because developers **do not manually compile** it before running. Modern JavaScript engines (like V8) actually use **both interpretation and Just-In-Time (JIT) compilation** to execute code efficiently.

```js
console.log("Hello, World!");
```

---

## Execution Flow

```text
JavaScript Source Code
        │
        ▼
      Parser
        │
        ▼
 AST (Abstract Syntax Tree)
        │
        ▼
   Interpreter
        │
     Bytecode
        │
        ▼
 JIT Compiler (Hot Code)
        │
        ▼
 Optimized Machine Code
```

---

## Step-by-Step

### 1. Parsing

- Reads the JavaScript source code.
- Checks for syntax errors.
- Creates an **AST (Abstract Syntax Tree)**.

### 2. Interpretation

- Converts the AST into **Bytecode**.
- Starts executing the program immediately.

### 3. JIT Compilation

- Detects frequently executed (**hot**) code.
- Compiles it into optimized **Machine Code**.
- Improves performance for future executions.

---

## Why It's Still Called "Interpreted"

Developers simply run JavaScript without a separate compilation step.

```bash
node app.js
```

or

```html
<script src="app.js"></script>
```

The JavaScript engine automatically handles:

- Parsing
- Interpretation
- JIT Compilation

---

## Interpreted vs Compiled

| Interpreted                         | Compiled                      |
| ----------------------------------- | ----------------------------- |
| No manual compilation               | Requires manual compilation   |
| Executes immediately                | Must compile before execution |
| Example: JavaScript (traditionally) | Example: C, C++               |

---

## Key Terms

- **Parser** → Reads JavaScript code.
- **AST** → Tree representation of the code.
- **Bytecode** → Intermediate code executed by the interpreter.
- **JIT (Just-In-Time) Compiler** → Converts hot code into optimized machine code during runtime.
- **Machine Code** → Binary instructions executed directly by the CPU.

---

## Interview Answer

> JavaScript is traditionally called an interpreted language because developers don't manually compile it before execution. Modern JavaScript engines first parse the code, convert it into bytecode, and then use JIT compilation to optimize frequently executed code into machine code, making JavaScript both interpreted and JIT-compiled.
