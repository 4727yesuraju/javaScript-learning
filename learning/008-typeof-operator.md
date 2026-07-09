# What is `typeof`?

# 🤔 Why is it Needed?

The `typeof` operator is used to **find the data type of a value or variable**.

It helps you:

- Debug your code.
- Check the type of a variable before performing operations.
- Write safer and more reliable programs.

---

# 🌍 Real-world Example

Imagine you have different boxes, but you don't know what's inside them.

Before using the contents, you check the label.

```text
📦 Box 1 → Number
📦 Box 2 → String
📦 Box 3 → Boolean
```

Similarly, `typeof` tells you **what type of data** a variable contains.

---

# 🧠 Interview Explanation

`typeof` is a **JavaScript operator** that returns the **data type** of a value as a **string**.

For example:

- Number → `"number"`
- String → `"string"`
- Boolean → `"boolean"`

---

# ✍️ Syntax

```javascript
typeof value;
```

or

```javascript
typeof variable;
```

---

# 💻 Example Queries

### Number

```javascript
typeof 100;
```

**Output**

```text
"number"
```

---

### String

```javascript
typeof "Hello";
```

**Output**

```text
"string"
```

---

### Boolean

```javascript
typeof true;
```

**Output**

```text
"boolean"
```

---

### Undefined

```javascript
let x;

typeof x;
```

**Output**

```text
"undefined"
```

---

### Null

```javascript
typeof null;
```

**Output**

```text
"object"
```

> ⚠️ This is a **historical JavaScript bug**. `null` is **not** actually an object.

---

### Object

```javascript
typeof { name: "Yesu" };
```

**Output**

```text
"object"
```

---

### Array

```javascript
typeof [1, 2, 3];
```

**Output**

```text
"object"
```

> Arrays are a special type of object.

---

### Function

```javascript
typeof function () {};
```

**Output**

```text
"function"
```

---

# ❓ Common Interview Questions

### Q1. What is `typeof`?

`typeof` is an operator used to determine the data type of a value or variable.

---

### Q2. What does `typeof` return?

It returns the data type as a **string**.

Example:

```javascript
typeof 10;
```

Output:

```text
"number"
```

---

### Q3. What is the output?

```javascript
typeof null;
```

**Output**

```text
"object"
```

---

### Q4. What is the output?

```javascript
typeof [];
```

**Output**

```text
"object"
```

---

### Q5. What is the output?

```javascript
typeof function () {};
```

**Output**

```text
"function"
```

---

# 🧩 Interview Follow-up Questions

### Why does `typeof null` return `"object"`?

Because of a **historical bug** in JavaScript that has been kept for backward compatibility.

---

### How can you check if a value is an array?

```javascript
Array.isArray([1, 2, 3]);
```

**Output**

```text
true
```

---

### Can `typeof` distinguish between objects and arrays?

❌ No.

Both return:

```text
"object"
```

Use `Array.isArray()` to identify arrays.

---

# 📝 Practice Exercises

Predict the output:

```javascript
typeof 25;
```

```javascript
typeof "JavaScript";
```

```javascript
typeof false;
```

```javascript
typeof undefined;
```

```javascript
typeof null;
```

```javascript
typeof [];
```

```javascript
typeof {};
```

```javascript
typeof function () {};
```

---

# ⚠️ Common Mistakes

❌ Thinking `typeof null` returns `"null"`.

> It returns `"object"`.

---

❌ Thinking arrays have their own `typeof`.

> `typeof []` returns `"object"`.

---

❌ Forgetting that `typeof` always returns a **string**.

---

# 🔁 Revision Summary

| Expression            | Output        |
| --------------------- | ------------- |
| `typeof 100`          | `"number"`    |
| `typeof "Hello"`      | `"string"`    |
| `typeof true`         | `"boolean"`   |
| `typeof undefined`    | `"undefined"` |
| `typeof null`         | `"object"`    |
| `typeof {}`           | `"object"`    |
| `typeof []`           | `"object"`    |
| `typeof function(){}` | `"function"`  |

---

# 💡 Key Takeaways

- `typeof` is used to **check the data type** of a value or variable.
- It **returns the type as a string**.
- `typeof null` returns `"object"` due to a historical JavaScript bug.
- Arrays are objects, so `typeof []` returns `"object"`.
- Use `Array.isArray()` to check whether a value is an array.
- `typeof` is commonly used for debugging and type checking in JavaScript.
