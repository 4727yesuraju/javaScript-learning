# Difference Between `null` and `undefined`

## 🤔 Why it's needed

Both `null` and `undefined` represent **the absence of a value**, but they are used in different situations.

Understanding the difference helps avoid bugs and is a common JavaScript interview topic.

---

## 🌍 Real-world Example

Imagine you're filling out a form.

- **`undefined`** → You **haven't filled** the field yet.
- **`null`** → You **intentionally left** the field empty.

---

## 🧠 Difference

| `undefined`                          | `null`                                         |
| ------------------------------------ | ---------------------------------------------- |
| Default value assigned by JavaScript | Value intentionally assigned by the developer  |
| Means **value is not assigned yet**  | Means **no value** or **empty value**          |
| Type is `"undefined"`                | Type is `"object"` (historical JavaScript bug) |

---

## ✍️ Syntax

### `undefined`

```javascript
let name;

console.log(name);
```

**Output**

```text
undefined
```

---

### `null`

```javascript
let name = null;

console.log(name);
```

**Output**

```text
null
```

---

## 💻 Example Queries

### Example 1

```javascript
let age;

console.log(age);
```

**Output**

```text
undefined
```

---

### Example 2

```javascript
let age = null;

console.log(age);
```

**Output**

```text
null
```

---

### Example 3

```javascript
console.log(typeof undefined);
```

**Output**

```text
"undefined"
```

---

### Example 4

```javascript
console.log(typeof null);
```

**Output**

```text
"object"
```

> **Note:** This is a **historical bug** in JavaScript. `null` is **not** actually an object.

---

## ❓ Common Interview Questions

### Q1. What is `undefined`?

A variable has been declared but **no value has been assigned**.

---

### Q2. What is `null`?

A value that **explicitly represents no value**.

---

### Q3. What is the output?

```javascript
typeof undefined;
```

```text
"undefined"
```

---

### Q4. What is the output?

```javascript
typeof null;
```

```text
"object"
```

---

## 📝 Practice Exercises

- Declare a variable without assigning a value.
- Assign `null` to a variable.
- Check both using `typeof`.

---

## ⚠️ Common Mistakes

❌ Assuming `null` and `undefined` are the same.

❌ Forgetting that `typeof null` returns `"object"`.

❌ Using `null` when you actually mean "not assigned yet."

---

## 🔁 Revision Summary

| Feature     | `undefined`        | `null`                 |
| ----------- | ------------------ | ---------------------- |
| Assigned by | JavaScript         | Developer              |
| Meaning     | Value not assigned | Intentionally no value |
| `typeof`    | `"undefined"`      | `"object"`             |

### Easy Way to Remember

- **`undefined`** → **Not assigned yet**
- **`null`** → **Intentionally empty**
