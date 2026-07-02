# What are Data Types in JavaScript?

## 🤔 Why it's needed

A **data type** tells JavaScript **what kind of value** a variable stores.

Examples:

- Number
- String
- Boolean

Without data types, JavaScript wouldn't know how to store or process values.

---

## 🌍 Real-world Example

Think of a storage box.

Different boxes store different items.

```text
📦 Number Box  → 100
📦 String Box  → "Hello"
📦 Boolean Box → true
```

Similarly, variables store different types of data.

---

## 🧠 What are Data Types?

A **data type** defines the type of value stored in a variable.

```javascript
let age = 25; // Number
let name = "Yesu"; // String
let isStudent = true; // Boolean
```

---

## 📚 Types of Data Types

JavaScript has **8 data types**, divided into two categories.

### 1. Primitive Data Types

These store **single, immutable values**.

| Data Type | Example                 |
| --------- | ----------------------- |
| Number    | `10`, `3.14`            |
| String    | `"Hello"`               |
| Boolean   | `true`, `false`         |
| Undefined | `let x;`                |
| Null      | `null`                  |
| BigInt    | `12345678901234567890n` |
| Symbol    | `Symbol("id")`          |

---

### 2. Non-Primitive (Reference) Data Type

These store **collections of values** or more complex data.

| Data Type | Example                     |
| --------- | --------------------------- |
| Object    | `{ name: "Yesu", age: 25 }` |

> Arrays and Functions are special types of **Objects** in JavaScript.

---

## ✍️ Syntax

```javascript
let age = 25; // Number
let name = "John"; // String
let isLoggedIn = true; // Boolean
let city; // Undefined
let data = null; // Null
let id = Symbol("id"); // Symbol
let bigNum = 123456789n; // BigInt

let person = {
  name: "John",
  age: 25,
};
```

---

## 💻 Example Queries

```javascript
typeof 100;
// "number"

typeof "Hello";
// "string"

typeof true;
// "boolean"

typeof undefined;
// "undefined"

typeof null;
// "object" (JavaScript bug)

typeof {};
// "object"

typeof [];
// "object"

typeof function () {};
// "function"
```

---

## ❓ Common Interview Questions

### Q1. How many data types are there in JavaScript?

**8 data types**

- 7 Primitive
- 1 Non-Primitive (Object)

---

### Q2. What are primitive data types?

- Number
- String
- Boolean
- Undefined
- Null
- Symbol
- BigInt

---

### Q3. What is the difference between Primitive and Non-Primitive?

| Primitive             | Non-Primitive          |
| --------------------- | ---------------------- |
| Stores a single value | Stores multiple values |
| Immutable             | Mutable                |
| Copied by value       | Copied by reference    |

---

### Q4. What is the output of `typeof null`?

```javascript
typeof null;
```

Output:

```text
"object"
```

This is a **known bug** in JavaScript.

---

## 📝 Practice Exercises

- Create one variable for each data type.
- Use `typeof` to check their types.
- Create an object with your personal details.

---

## ⚠️ Common Mistakes

❌ Thinking Arrays are a separate data type.

> Arrays are Objects.

❌ Thinking Functions are a separate data type.

> Functions are special Objects.

❌ Expecting `typeof null` to return `"null"`.

> It returns `"object"` due to a historical JavaScript bug.

---

## 🔁 Revision Summary

- A **data type** defines the kind of value stored in a variable.
- JavaScript has **8 data types**.
- **7 are Primitive**.
- **Object is the only Non-Primitive data type**.
- Arrays and Functions are special kinds of Objects.
- Use `typeof` to check a variable's type.
