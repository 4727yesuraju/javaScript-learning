# 📖 What is Block Scope?

A **block scope** means a variable is **accessible only inside the block `{}` where it is declared**.

In JavaScript, **`let`** and **`const`** are block-scoped.

A block is any code enclosed in curly braces `{}` such as:

- `if`
- `for`
- `while`
- `switch`
- `{ }`

---

# 🤔 Why is it Needed?

Block scope helps:

- Prevent accidental access to variables.
- Avoid variable name conflicts.
- Keep variables local to where they are needed.

This makes code safer and easier to maintain.

---

# 🌍 Real-world Example

Imagine a classroom.

A student inside **Classroom A** cannot be seen from **Classroom B**.

Similarly, a block-scoped variable exists **only inside its block**.

---

# 🧠 Interview Explanation

Variables declared with **`let`** or **`const`** can only be accessed within the `{}` block where they are declared.

Trying to access them outside the block results in a `ReferenceError`.

---

# ✍️ Syntax

```javascript
{
  let name = "Yesu";
  const age = 25;
}
```

Both `name` and `age` exist only inside the block.

---

# 💻 Example Queries

### Example 1: `let`

```javascript
{
  let name = "Yesu";

  console.log(name);
}
```

**Output**

```text
Yesu
```

---

### Example 2: Access Outside the Block

```javascript
{
  let name = "Yesu";
}

console.log(name);
```

**Output**

```text
ReferenceError
```

---

### Example 3: `const`

```javascript
{
  const PI = 3.14;

  console.log(PI);
}
```

**Output**

```text
3.14
```

---

### Example 4: `if` Block

```javascript
if (true) {
  let message = "Hello";
  console.log(message);
}
```

**Output**

```text
Hello
```

---

# ❓ Common Interview Questions

### Q1. What is block scope?

Block scope means a variable is accessible only within the `{}` block where it is declared.

---

### Q2. Which variables are block-scoped?

- ✅ `let`
- ✅ `const`

---

### Q3. Is `var` block-scoped?

❌ No.

`var` is **function-scoped**, not block-scoped.

---

### Q4. What is the output?

```javascript
{
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

### What is a block?

A block is any code enclosed in curly braces `{}`.

Example:

```javascript
if (true) {
  // Block
}
```

---

### Why is block scope better than function scope?

Block scope limits where variables can be accessed, reducing bugs and preventing accidental modifications.

---

### Which keyword should you use in modern JavaScript?

Prefer:

- `const` by default
- `let` when the value needs to change

Avoid `var` unless necessary.

---

# 📝 Practice Exercises

1. Declare a variable using `let` inside a block.
2. Try accessing it outside the block.
3. Repeat the same with `const`.
4. Compare the behavior of `let` and `var` inside an `if` block.

---

# ⚠️ Common Mistakes

❌ Thinking `var` is block-scoped.

```javascript
if (true) {
  var x = 10;
}

console.log(x); // ✅ Works
```

---

❌ Accessing a block-scoped variable outside its block.

```javascript
{
  let name = "Yesu";
}

console.log(name);
```

Results in a `ReferenceError`.

---

# 🔁 Revision Summary

| Keyword | Scope    |
| ------- | -------- |
| `let`   | Block    |
| `const` | Block    |
| `var`   | Function |

---

# 💡 Key Takeaways

- A **block** is code inside `{}`.
- `let` and `const` are **block-scoped**.
- Block-scoped variables are accessible **only inside their block**.
- Accessing them outside the block throws a **ReferenceError**.
- Prefer `let` and `const` in modern JavaScript.

```

```
