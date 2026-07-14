# 📖 What is Strict Mode?

**Strict Mode** is a feature in JavaScript that helps you write **safer and cleaner code**.

It catches common mistakes by turning them into **errors** instead of silently ignoring them.

To enable Strict Mode, add:

```javascript
"use strict";
```

at the top of your file or function.

---

# 🤔 Why is it Needed?

Without Strict Mode, JavaScript may allow mistakes without warning.

Strict Mode:

- Finds coding mistakes early.
- Prevents unsafe coding practices.
- Makes debugging easier.
- Encourages writing modern JavaScript.

---

# 🌍 Real-world Example

Imagine driving a car.

- **Without seatbelt** → Small mistakes can become dangerous.
- **With seatbelt** → You are protected.

Similarly:

- **Without Strict Mode** → JavaScript may ignore some mistakes.
- **With Strict Mode** → JavaScript reports mistakes immediately.

---

# 🧠 Interview Explanation

Strict Mode is a special mode that makes JavaScript **more strict**.

It helps developers avoid common errors and bad practices.

Enable it by writing:

```javascript
"use strict";
```

at the beginning of a script or function.

---

# ✍️ Syntax

### Entire File

```javascript
"use strict";

let name = "Yesu";
```

---

### Inside a Function

```javascript
function greet() {
  "use strict";

  console.log("Hello");
}
```

Only this function uses Strict Mode.

---

# 💻 Example Queries

### Example 1: Accidental Global Variable

❌ Without Strict Mode

```javascript
name = "Yesu";

console.log(name);
```

**Output**

```text
Yesu
```

JavaScript creates a global variable automatically.

---

✅ With Strict Mode

```javascript
"use strict";

name = "Yesu";
```

**Output**

```text
ReferenceError
```

Because `name` was never declared.

---

### Example 2: Correct Way

```javascript
"use strict";

let name = "Yesu";

console.log(name);
```

**Output**

```text
Yesu
```

---

### Example 3: Duplicate Parameters

❌

```javascript
"use strict";

function add(a, a) {}
```

**Output**

```text
SyntaxError
```

Parameter names must be unique.

---

# ❓ Common Interview Questions

### Q1. What is Strict Mode?

Strict Mode is a JavaScript feature that helps detect common coding mistakes by treating them as errors.

---

### Q2. How do you enable Strict Mode?

```javascript
"use strict";
```

---

### Q3. Can Strict Mode be enabled for a single function?

✅ Yes.

Place `"use strict";` at the beginning of the function.

---

### Q4. Does Strict Mode make JavaScript faster?

Not necessarily.

Its main purpose is **safer and cleaner code**, not performance.

---

# 🧩 Interview Follow-up Questions

### Is Strict Mode enabled by default?

❌ No, in normal JavaScript scripts.

✅ **Yes**, in **ES6 modules** (`import` / `export`) and **JavaScript classes**, Strict Mode is enabled automatically.

---

### What are some errors caught by Strict Mode?

- Using undeclared variables.
- Duplicate function parameters.
- Assigning to read-only properties.
- Using certain deprecated JavaScript features.

---

### Should you use Strict Mode?

✅ Yes.

It is considered a best practice for writing reliable JavaScript code.

---

# 📝 Practice Exercises

1. Enable Strict Mode in a JavaScript file.
2. Try using a variable without `let`, `const`, or `var`.
3. Create a function with duplicate parameters.
4. Enable Strict Mode inside only one function.

---

# ⚠️ Common Mistakes

❌ Forgetting to place `"use strict";` at the top.

Incorrect:

```javascript
let name = "Yesu";

("use strict");
```

Strict Mode must appear **before any executable code**.

---

❌ Thinking Strict Mode is enabled automatically in every script.

It is **not** enabled automatically in regular JavaScript files.

---

❌ Assuming Strict Mode changes JavaScript syntax.

It doesn't change the language—it simply enforces stricter rules.

---

# 🔁 Revision Summary

| Feature               | Strict Mode                    |
| --------------------- | ------------------------------ |
| Enable                | `"use strict";`                |
| Purpose               | Catch coding mistakes          |
| Helps With            | Safer, cleaner code            |
| Scope                 | Entire file or single function |
| Automatically Enabled | ES6 Modules and Classes        |

---

# 💡 Key Takeaways

- Strict Mode is enabled using `"use strict";`.
- It helps catch common JavaScript mistakes early.
- It prevents accidental global variables.
- It can be applied to an entire file or a single function.
- ES6 modules and classes use Strict Mode automatically.
- Using Strict Mode is a JavaScript best practice.
