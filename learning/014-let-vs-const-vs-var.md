# 📖 Difference Between `let`, `const`, and `var`

`let`, `const`, and `var` are used to **declare variables** in JavaScript.

The main differences are in:

- Scope
- Reassignment
- Redeclaration
- Hoisting

---

# 🤔 Why is it Needed?

Choosing the right variable declaration makes your code:

- Easier to understand
- More secure
- Less prone to bugs

Modern JavaScript recommends using **`let`** and **`const`** instead of `var`.

---

# 🌍 Real-world Example

Imagine labels on storage boxes:

- **`var`** → Old reusable box (can be reused anywhere)
- **`let`** → Reusable box inside one room (block)
- **`const`** → Locked box (cannot be reassigned)

---

# 🧠 Interview Explanation

| Feature   | `var`    | `let`        | `const`      |
| --------- | -------- | ------------ | ------------ |
| Scope     | Function | Block        | Block        |
| Reassign  | ✅ Yes   | ✅ Yes       | ❌ No        |
| Redeclare | ✅ Yes   | ❌ No        | ❌ No        |
| Hoisted   | ✅ Yes   | ✅ Yes (TDZ) | ✅ Yes (TDZ) |

> **TDZ (Temporal Dead Zone):** `let` and `const` are hoisted but cannot be used before they are declared.

---

# ✍️ Syntax

### var

```javascript
var name = "Yesu";
```

### let

```javascript
let age = 25;
```

### const

```javascript
const PI = 3.14;
```

---

# 💻 Example Queries

### Example 1: `var`

```javascript
var name = "Yesu";
name = "John";

console.log(name);
```

**Output**

```text
John
```

---

### Example 2: `let`

```javascript
let age = 20;
age = 21;

console.log(age);
```

**Output**

```text
21
```

---

### Example 3: `const`

```javascript
const country = "India";

country = "USA";
```

**Output**

```text
TypeError
```

---

### Example 4: Redeclaration

```javascript
let x = 10;
let x = 20;
```

**Output**

```text
SyntaxError
```

---

### Example 5: Block Scope

```javascript
{
  let a = 10;
}

console.log(a);
```

**Output**

```text
ReferenceError
```

---

# ❓ Common Interview Questions

### Q1. What is the difference between `var`, `let`, and `const`?

- `var` → Function-scoped, can be redeclared and reassigned.
- `let` → Block-scoped, can be reassigned but not redeclared.
- `const` → Block-scoped, cannot be reassigned or redeclared.

---

### Q2. Which one should you use?

- ✅ Use `const` by default.
- ✅ Use `let` if the value needs to change.
- ❌ Avoid `var` in modern JavaScript.

---

### Q3. Can a `const` object be modified?

✅ Yes.

The **reference** cannot change, but the object's contents can.

```javascript
const user = {
  name: "Yesu",
};

user.name = "John";

console.log(user.name);
```

**Output**

```text
John
```

---

### Q4. What is TDZ?

The **Temporal Dead Zone** is the period between entering a scope and declaring a `let` or `const` variable.

Accessing the variable during this period throws a `ReferenceError`.

---

# 🧩 Interview Follow-up Questions

### Why is `let` better than `var`?

- Block-scoped
- Prevents accidental redeclaration
- Avoids many bugs caused by `var`

---

### Why is `const` recommended by default?

It prevents accidental reassignment, making your code safer and easier to maintain.

---

### Is `const` immutable?

❌ No.

Only the **variable reference** is constant.

Objects and arrays declared with `const` can still be modified.

---

# 📝 Practice Exercises

1. Declare a variable using `var`, `let`, and `const`.
2. Try reassigning each variable.
3. Try redeclaring each variable.
4. Create a `const` object and modify one of its properties.
5. Create a block and access a `let` variable outside it.

---

# ⚠️ Common Mistakes

❌ Thinking `const` makes objects immutable.

```javascript
const user = { name: "Yesu" };

user.name = "John"; // ✅ Allowed
```

---

❌ Using `var` in modern JavaScript.

Prefer `let` or `const`.

---

❌ Accessing `let` or `const` before declaration.

```javascript
console.log(age);

let age = 20;
```

Results in a `ReferenceError` because of the **Temporal Dead Zone (TDZ)**.

---

# 🔁 Revision Summary

| Feature   | `var`    | `let`    | `const`  |
| --------- | -------- | -------- | -------- |
| Scope     | Function | Block    | Block    |
| Reassign  | ✅       | ✅       | ❌       |
| Redeclare | ✅       | ❌       | ❌       |
| Hoisted   | ✅       | ✅ (TDZ) | ✅ (TDZ) |

---

# 💡 Key Takeaways

- `var` is the old way of declaring variables and should generally be avoided.
- `let` is used for variables whose values may change.
- `const` is used for variables whose references should not change.
- `let` and `const` are **block-scoped** and safer than `var`.
- **Use `const` by default**, and use `let` only when reassignment is needed.

```

```
