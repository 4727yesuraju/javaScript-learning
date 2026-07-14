# 📖 What is Function Scope?

**Function scope** means a variable is **accessible only inside the function where it is declared**.

Variables declared inside a function **cannot be accessed outside that function**.

> **Note:** Variables declared with `var` are **function-scoped**.

---

# 🤔 Why is it Needed?

Function scope helps:

- Keep variables private.
- Prevent accidental access from outside the function.
- Avoid variable name conflicts.

This makes your code cleaner and more secure.

---

# 🌍 Real-world Example

Imagine a **teacher's office**.

Only the teacher can access the documents inside the office.

People outside cannot access them.

Similarly, variables inside a function are available **only inside that function**.

---

# 🧠 Interview Explanation

A variable declared inside a function exists only while that function is running.

After the function finishes, the variable cannot be accessed from outside.

This is called **function scope**.

---

# ✍️ Syntax

```javascript
function greet() {
  let message = "Hello";
}
```

`message` exists only inside `greet()`.

---

# 💻 Example Queries

### Example 1: Access Inside Function

```javascript
function greet() {
  let message = "Hello";

  console.log(message);
}

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Access Outside Function

```javascript
function greet() {
  let message = "Hello";
}

console.log(message);
```

**Output**

```text
ReferenceError
```

---

### Example 3: Function Scope with `var`

```javascript
function test() {
  var x = 10;

  console.log(x);
}

test();
```

**Output**

```text
10
```

---

### Example 4: `var` is Not Block Scoped

```javascript
function test() {
  if (true) {
    var x = 10;
  }

  console.log(x);
}

test();
```

**Output**

```text
10
```

`var` ignores the `if` block because it is **function-scoped**.

---

# ❓ Common Interview Questions

### Q1. What is function scope?

Function scope means a variable can only be accessed inside the function where it is declared.

---

### Q2. Which keyword is function-scoped?

✅ `var`

---

### Q3. Are `let` and `const` function-scoped?

❌ No.

They are **block-scoped**.

---

### Q4. What is the output?

```javascript
function test() {
  let x = 10;
}

console.log(x);
```

**Output**

```text
ReferenceError
```

---

# 🧩 Interview Follow-up Questions

### What is the difference between function scope and block scope?

| Function Scope                    | Block Scope                 |
| --------------------------------- | --------------------------- |
| Accessible only inside a function | Accessible only inside `{}` |
| Used by `var`                     | Used by `let` and `const`   |

---

### Can a function access global variables?

✅ Yes.

```javascript
let name = "Yesu";

function greet() {
  console.log(name);
}

greet();
```

**Output**

```text
Yesu
```

---

### Can a variable inside a function be accessed outside?

❌ No.

Unless it is returned from the function.

---

# 📝 Practice Exercises

1. Declare a variable inside a function.
2. Try accessing it outside the function.
3. Create a `var` inside an `if` block within a function.
4. Create a `let` inside an `if` block and compare the behavior.

---

# ⚠️ Common Mistakes

❌ Thinking variables inside a function are global.

```javascript
function test() {
  let x = 10;
}

console.log(x);
```

Results in a `ReferenceError`.

---

❌ Thinking `var` is block-scoped.

```javascript
function test() {
  if (true) {
    var x = 10;
  }

  console.log(x); // ✅ Works
}
```

---

❌ Confusing function scope with block scope.

- `var` → Function scope
- `let`, `const` → Block scope

---

# 🔁 Revision Summary

| Keyword | Scope    |
| ------- | -------- |
| `var`   | Function |
| `let`   | Block    |
| `const` | Block    |

---

# 💡 Key Takeaways

- Function scope means variables are accessible **only inside the function** where they are are declared.
- Variables inside a function cannot be accessed outside the function.
- `var` is **function-scoped**.
- `let` and `const` are **block-scoped**.
- Functions can access **global variables**, but global code cannot access variables declared inside a function.

```

```
