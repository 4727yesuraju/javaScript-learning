# 📖 What are Truthy and Falsy Values?

In JavaScript, every value is treated as either **truthy** or **falsy** when used in a Boolean context (e.g., `if`, `while`, logical operators).

- **Truthy** → Behaves like `true`.
- **Falsy** → Behaves like `false`.

---

# 🤔 Why is it Needed?

JavaScript often needs to decide whether a condition is **true** or **false**.

Instead of requiring only `true` or `false`, JavaScript automatically converts values to a Boolean.

This allows you to write shorter and cleaner conditions.

---

# 🌍 Real-world Example

Imagine entering a movie theater.

- 🎫 Valid ticket → Allowed in (**Truthy**)
- ❌ No ticket → Not allowed (**Falsy**)

Similarly, JavaScript checks whether a value is considered **truthy** or **falsy** before executing code.

---

# 🧠 Interview Explanation

When a value is used in a condition, JavaScript **implicitly converts** it to a Boolean.

There are only **8 falsy values** in JavaScript.

Everything else is **truthy**.

### Falsy Values

```javascript
false;
0 - 0;
0n; // BigInt zero
(""); // Empty string
null;
undefined;
NaN;
```

Everything else is **truthy**.

Examples:

```javascript
"Hello"
42
-10
[]
{}
function() {}
true
```

---

# ✍️ Syntax

```javascript
if (value) {
  // Runs if value is truthy
} else {
  // Runs if value is falsy
}
```

---

# 💻 Example Queries

### Example 1

```javascript
if ("Hello") {
  console.log("Truthy");
}
```

**Output**

```text
Truthy
```

---

### Example 2

```javascript
if ("") {
  console.log("Truthy");
} else {
  console.log("Falsy");
}
```

**Output**

```text
Falsy
```

---

### Example 3

```javascript
if (0) {
  console.log("Truthy");
} else {
  console.log("Falsy");
}
```

**Output**

```text
Falsy
```

---

### Example 4

```javascript
if ([]) {
  console.log("Truthy");
}
```

**Output**

```text
Truthy
```

> Even an **empty array** is truthy.

---

### Example 5

```javascript
if ({}) {
  console.log("Truthy");
}
```

**Output**

```text
Truthy
```

> Even an **empty object** is truthy.

---

# ❓ Common Interview Questions

### Q1. What are truthy values?

Values that are converted to **`true`** in a Boolean context.

---

### Q2. What are falsy values?

Values that are converted to **`false`** in a Boolean context.

---

### Q3. How many falsy values are there in JavaScript?

There are **8 falsy values**:

- `false`
- `0`
- `-0`
- `0n`
- `""`
- `null`
- `undefined`
- `NaN`

---

### Q4. Is an empty array (`[]`) truthy or falsy?

✅ **Truthy**

---

### Q5. Is an empty object (`{}`) truthy or falsy?

✅ **Truthy**

---

# 🧩 Interview Follow-up Questions

### Why are empty arrays and objects truthy?

Because **all objects in JavaScript are truthy**, regardless of whether they contain data.

---

### How can you explicitly convert a value to a Boolean?

```javascript
Boolean(value);
```

Example:

```javascript
Boolean(0); // false
Boolean("Hi"); // true
```

---

### What is Boolean coercion?

The automatic conversion of a value to `true` or `false` when used in a Boolean context.

---

# 📝 Practice Exercises

Predict the output:

```javascript
Boolean("");
```

```javascript
Boolean("JavaScript");
```

```javascript
Boolean(0);
```

```javascript
Boolean(100);
```

```javascript
Boolean([]);
```

```javascript
Boolean({});
```

```javascript
Boolean(null);
```

```javascript
Boolean(undefined);
```

---

# ⚠️ Common Mistakes

❌ Thinking an empty array (`[]`) is falsy.

> It is **truthy**.

---

❌ Thinking an empty object (`{}`) is falsy.

> It is **truthy**.

---

❌ Forgetting that `NaN` is a falsy value.

---

# 🔁 Revision Summary

## Falsy Values (Remember These 8)

```javascript
false;
0 - 0;
0n;
("");
null;
undefined;
NaN;
```

Everything else is **truthy**.

| Value       | Result |
| ----------- | ------ |
| `"Hello"`   | Truthy |
| `100`       | Truthy |
| `[]`        | Truthy |
| `{}`        | Truthy |
| `false`     | Falsy  |
| `0`         | Falsy  |
| `""`        | Falsy  |
| `null`      | Falsy  |
| `undefined` | Falsy  |
| `NaN`       | Falsy  |

---

# 💡 Key Takeaways

- JavaScript converts values to **Boolean** in conditions.
- There are **only 8 falsy values**.
- **Everything else is truthy**.
- Empty arrays (`[]`) and empty objects (`{}`) are **truthy**.
- Use `Boolean(value)` to check whether a value is truthy or falsy.
- Truthy and falsy values are frequently asked in JavaScript interviews.
