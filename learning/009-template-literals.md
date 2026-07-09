# 📖 What are Template Literals?

Template literals are a feature introduced in **ES6 (ECMAScript 2015)** that make it easier to create strings.

They use **backticks (` `)** instead of single (`' '`) or double (`" "`) quotes.

Template literals allow you to:

- Embed variables and expressions.
- Create multi-line strings.
- Write cleaner and more readable code.

---

# 🤔 Why is it Needed?

Before template literals, string concatenation was done using the `+` operator, making code harder to read.

Template literals provide:

- Cleaner syntax
- Better readability
- Easy variable interpolation
- Support for multi-line strings

---

# 🌍 Real-world Example

Imagine you're generating a welcome message.

Without Template Literals:

```javascript
let name = "Yesu";

console.log("Welcome " + name + "!");
```

With Template Literals:

```javascript
let name = "Yesu";

console.log(`Welcome ${name}!`);
```

Much cleaner and easier to read.

---

# 🧠 Interview Explanation

A **template literal** is a string enclosed in **backticks (` `)** instead of quotes.

It supports:

- **String interpolation** using `${}`.
- **Multi-line strings** without `\n`.
- **Embedded JavaScript expressions**.

---

# ✍️ Syntax

### Basic Syntax

```javascript
`Hello World`;
```

### Variable Interpolation

```javascript
`Hello ${name}`;
```

### Expression Interpolation

```javascript
`Sum = ${10 + 20}`;
```

---

# 💻 Example Queries

### Example 1: Variable

```javascript
let name = "Yesu";

console.log(`Hello ${name}`);
```

**Output**

```text
Hello Yesu
```

---

### Example 2: Expression

```javascript
console.log(`10 + 20 = ${10 + 20}`);
```

**Output**

```text
10 + 20 = 30
```

---

### Example 3: Multi-line String

```javascript
console.log(`Hello
Welcome to JavaScript
Happy Learning!`);
```

**Output**

```text
Hello
Welcome to JavaScript
Happy Learning!
```

---

### Example 4: Function Call

```javascript
function greet(name) {
  return `Hello ${name}`;
}

console.log(greet("Yesu"));
```

**Output**

```text
Hello Yesu
```

---

# ❓ Common Interview Questions

### Q1. What are template literals?

Template literals are strings enclosed in **backticks (` `)** that support variable interpolation, expressions, and multi-line strings.

---

### Q2. Which symbol is used for template literals?

**Backticks (` `)**

Not:

- `' '` (single quotes)
- `" "` (double quotes)

---

### Q3. How do you insert a variable into a template literal?

Using `${}`.

Example:

```javascript
let name = "Yesu";

console.log(`Hello ${name}`);
```

---

### Q4. Can JavaScript expressions be used inside `${}`?

✅ Yes.

```javascript
console.log(`${5 + 5}`);
```

Output:

```text
10
```

---

# 🧩 Interview Follow-up Questions

### What is string interpolation?

String interpolation is the process of embedding variables or expressions inside a string using `${}`.

---

### Can you call functions inside `${}`?

✅ Yes.

```javascript
function square(x) {
  return x * x;
}

console.log(`${square(5)}`);
```

Output:

```text
25
```

---

### Are template literals an ES5 or ES6 feature?

They were introduced in **ES6 (ECMAScript 2015)**.

---

# 📝 Practice Exercises

1. Print your name using a template literal.
2. Print the sum of two numbers using `${}`.
3. Create a multi-line string.
4. Call a function inside a template literal.

---

# ⚠️ Common Mistakes

❌ Using single or double quotes instead of backticks.

```javascript
"Hello ${name}";
```

`${}` will **not** work here.

---

✅ Correct

```javascript
`Hello ${name}`;
```

---

❌ Forgetting the `$` in `${}`.

Incorrect:

```javascript
`Hello {name}`;
```

---

# 🔁 Revision Summary

| Feature    | Example               |
| ---------- | --------------------- |
| Backticks  | `` `Hello` ``         |
| Variable   | `` `Hello ${name}` `` |
| Expression | `` `${10 + 20}` ``    |
| Multi-line | Supported             |
| ES Version | ES6                   |

---

# 💡 Key Takeaways

- Template literals use **backticks (` `)**.
- They were introduced in **ES6**.
- Use `${}` to insert variables or expressions.
- They support **multi-line strings**.
- They are cleaner and more readable than string concatenation.
- Prefer template literals over the `+` operator for building strings.
