# 📖 What is Global Scope?

**Global scope** means a variable is **accessible from anywhere in your program**.

A variable declared **outside of all functions and blocks** belongs to the global scope.

---

# 🤔 Why is it Needed?

Global variables can be used by multiple functions and blocks.

However, using too many global variables is **not recommended** because they can be accidentally changed from anywhere in the program.

---

# 🌍 Real-world Example

Imagine a **notice board** in a school.

Every student and teacher can read it.

Similarly, a global variable can be accessed from anywhere in your code.

---

# 🧠 Interview Explanation

A variable declared outside all functions and blocks is called a **global variable**.

It can be accessed by:

- Functions
- Blocks (`if`, `for`, `while`)
- Other parts of the program

Global variables remain available throughout the program unless shadowed by a local variable.

---

# ✍️ Syntax

```javascript
let name = "Yesu"; // Global variable

function greet() {
  console.log(name);
}

greet();
```

---

# 💻 Example Queries

### Example 1: Access Inside a Function

```javascript
let message = "Hello";

function greet() {
  console.log(message);
}

greet();
```

**Output**

```text
Hello
```

---

### Example 2: Access Inside a Block

```javascript
let city = "Hyderabad";

if (true) {
  console.log(city);
}
```

**Output**

```text
Hyderabad
```

---

### Example 3: Modify a Global Variable

```javascript
let count = 10;

function update() {
  count = 20;
}

update();

console.log(count);
```

**Output**

```text
20
```

---

### Example 4: Shadowing a Global Variable

```javascript
let name = "Yesu";

function greet() {
  let name = "John";

  console.log(name);
}

greet();

console.log(name);
```

**Output**

```text
John
Yesu
```

The local variable shadows the global variable inside the function.

---

# ❓ Common Interview Questions

### Q1. What is global scope?

Global scope means a variable is accessible from anywhere in the program.

---

### Q2. Where is a global variable declared?

Outside all functions and blocks.

---

### Q3. Can a function access a global variable?

✅ Yes.

---

### Q4. Can a global variable be modified?

✅ Yes, unless it is declared with `const`.

---

# 🧩 Interview Follow-up Questions

### What is the difference between global scope and block scope?

| Global Scope                          | Block Scope                          |
| ------------------------------------- | ------------------------------------ |
| Accessible everywhere                 | Accessible only inside `{}`          |
| Declared outside functions and blocks | Declared inside a block              |
| Can be accessed by all functions      | Cannot be accessed outside the block |

---

### Why should you avoid too many global variables?

Because they:

- Can be changed from anywhere.
- Increase the chance of bugs.
- Make code harder to maintain.

---

### What is variable shadowing?

If a local variable has the same name as a global variable, the local variable hides (shadows) the global variable within its scope.

---

# 📝 Practice Exercises

1. Declare a global variable.
2. Access it inside a function.
3. Access it inside an `if` block.
4. Create a local variable with the same name and observe variable shadowing.

---

# ⚠️ Common Mistakes

❌ Declaring too many global variables.

> This can make the code difficult to manage.

---

❌ Confusing global variables with block-scoped variables.

```javascript
let name = "Yesu"; // Global

{
  let age = 25; // Block-scoped
}
```

`name` is available everywhere, but `age` is available only inside the block.

---

❌ Accidentally modifying a global variable.

```javascript
let count = 10;

function update() {
  count = 100;
}
```

Changes made in one place affect the entire program.

---

# 🔁 Revision Summary

| Scope          | Accessible From          |
| -------------- | ------------------------ |
| Global Scope   | Everywhere               |
| Block Scope    | Only inside `{}`         |
| Function Scope | Only inside the function |

---

# 💡 Key Takeaways

- Global scope means a variable is available throughout the program.
- Global variables are declared outside all functions and blocks.
- Functions and blocks can access global variables.
- Local variables can shadow global variables.
- Avoid excessive use of global variables to keep code clean and maintainable.
- Use `const` or `let` instead of `var` for modern JavaScript development.
