# 📖 What is Symbol?

`Symbol` is a **primitive data type** introduced in **ES6 (ECMAScript 2015)**.

A Symbol creates a **unique and immutable (cannot be changed) value**.

Even if two Symbols have the same description, they are **never equal**.

---

# 🤔 Why is it Needed?

Sometimes you need a property name that is **guaranteed to be unique**.

Using `Symbol` prevents property name collisions, especially when working with large applications or libraries.

---

# 🌍 Real-world Example

Imagine every employee in a company has a unique Employee ID.

Two employees may have the same name:

```text
Name: John
Name: John
```

But their Employee IDs are different:

```text
EMP001
EMP002
```

Similarly, every Symbol is unique, even if they have the same description.

---

# 🧠 Interview Explanation

A `Symbol` is a primitive data type used to create **unique identifiers**.

```javascript
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 === id2);
```

**Output**

```text
false
```

Although both Symbols have the description `"id"`, they are different values.

---

# ✍️ Syntax

```javascript
const symbolName = Symbol("description");
```

---

# 💻 Example Queries

### Example 1: Creating a Symbol

```javascript
const id = Symbol("id");

console.log(id);
```

---

### Example 2: Comparing Symbols

```javascript
const id1 = Symbol("id");
const id2 = Symbol("id");

console.log(id1 === id2);
```

**Output**

```text
false
```

---

### Example 3: Using Symbol as an Object Key

```javascript
const id = Symbol("id");

const user = {
  name: "Yesu",
  [id]: 101,
};

console.log(user[id]);
```

**Output**

```text
101
```

> Notice the square brackets (`[]`) when using a Symbol as an object key.

---

### Example 4: Checking the Type

```javascript
const id = Symbol("id");

console.log(typeof id);
```

**Output**

```text
"symbol"
```

---

# ❓ Common Interview Questions

### Q1. What is Symbol?

A Symbol is a **primitive data type** used to create unique identifiers.

---

### Q2. Are two Symbols with the same description equal?

```javascript
Symbol("id") === Symbol("id");
```

**Output**

```text
false
```

---

### Q3. What is the output?

```javascript
typeof Symbol("id");
```

**Output**

```text
"symbol"
```

---

### Q4. When should you use Symbol?

Use Symbols when you need **unique object property keys** to avoid name conflicts.

---

# 🧩 Interview Follow-up Questions

### Why use Symbol instead of a string as an object key?

Strings can accidentally overwrite existing properties.

Symbols are always unique, so they prevent property name collisions.

---

### Can a Symbol be changed?

❌ No.

Symbols are **immutable**.

---

### Is Symbol a primitive or non-primitive data type?

✅ Primitive.

---

# 📝 Practice Exercises

1. Create two Symbols with the same description and compare them.
2. Create an object using a Symbol as a property key.
3. Check the type of a Symbol using `typeof`.

---

# ⚠️ Common Mistakes

❌ Assuming two Symbols with the same description are equal.

```javascript
Symbol("id") === Symbol("id");
```

Output:

```text
false
```

---

❌ Using dot notation with Symbol keys.

Incorrect:

```javascript
user.id;
```

Correct:

```javascript
user[id];
```

---

❌ Thinking the description makes a Symbol unique.

The **description is only for debugging**. Every call to `Symbol()` creates a new unique value.

---

# 🔁 Revision Summary

| Feature       | Symbol             |
| ------------- | ------------------ |
| Data Type     | Primitive          |
| Introduced In | ES6                |
| Unique        | ✅ Yes             |
| Immutable     | ✅ Yes             |
| `typeof`      | `"symbol"`         |
| Common Use    | Unique object keys |

---

# 💡 Key Takeaways

- `Symbol` is a **primitive data type** introduced in **ES6**.
- Every `Symbol()` call creates a **unique value**.
- Two Symbols are **never equal**, even if they have the same description.
- Symbols are commonly used as **unique object property keys**.
- Use `typeof` to check a Symbol's type (`"symbol"`).

```

```
