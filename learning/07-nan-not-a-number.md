# What is NaN (Not-a-Number)?

## 🤔 Why it's needed

`NaN` stands for **Not-a-Number**.

It represents a value that is **not a valid number**, usually when a mathematical operation cannot produce a numeric result.

---

## 🌍 Real-world Example

Imagine asking someone:

> **"What is Apple ÷ 5?"**

This calculation doesn't make sense, so JavaScript returns **`NaN`**.

---

## 🧠 What is NaN?

`NaN` is a special **Number** value that indicates an invalid numeric result.

---

## ✍️ Syntax

```javascript
console.log("Hello" / 2);
```

**Output**

```text
NaN
```

---

## 💻 Example Queries

### Example 1

```javascript
0 / 0;
```

**Output**

```text
NaN
```

---

### Example 2

```javascript
"abc" * 10;
```

**Output**

```text
NaN
```

---

### Example 3

```javascript
Number("Hello");
```

**Output**

```text
NaN
```

---

### Example 4

```javascript
parseInt("ABC");
```

**Output**

```text
NaN
```

---

## ❓ Common Interview Questions

### Q1. What does NaN stand for?

**Not-a-Number**

---

### Q2. What is the type of `NaN`?

```javascript
typeof NaN;
```

**Output**

```text
"number"
```

> Although its name is **Not-a-Number**, its data type is **number**.

---

### Q3. Is `NaN` equal to itself?

```javascript
NaN === NaN;
```

**Output**

```text
false
```

> `NaN` is the **only JavaScript value that is not equal to itself**.

---

### Q4. How do you check if a value is `NaN`?

```javascript
Number.isNaN(NaN);
```

**Output**

```text
true
```

---

## 📝 Practice Exercises

Predict the output:

```javascript
"Hello" - 5;
```

```javascript
Number("ABC");
```

```javascript
typeof NaN;
```

```javascript
NaN === NaN;
```

---

## ⚠️ Common Mistakes

❌ Thinking `NaN` is a separate data type.

> It is actually a **Number** value.

❌ Comparing `NaN` using `==` or `===`.

> Use `Number.isNaN()` instead.

---

## 🔁 Revision Summary

| Property          | Value                           |
| ----------------- | ------------------------------- |
| Full Form         | Not-a-Number                    |
| Data Type         | `number`                        |
| Represents        | Invalid numeric result          |
| Equal to itself?  | ❌ No (`NaN === NaN` → `false`) |
| Best way to check | `Number.isNaN(value)`           |

### Easy Way to Remember

- **NaN** → Invalid number
- **`typeof NaN`** → `"number"`
- **`NaN === NaN`** → `false`
- **Check using** → `Number.isNaN()`
