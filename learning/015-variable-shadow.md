# 📖 What is Variable Shadowing?

**Variable Shadowing** happens when a variable declared in an **inner scope** has the **same name** as a variable in an **outer scope**.

The inner variable **hides (shadows)** the outer variable within its scope.

---

# 🤔 Why is it Needed?

Variable shadowing allows you to use the same variable name in different scopes without affecting the outer variable.

This helps keep variables local to their blocks or functions.

---

# 🌍 Real-world Example

Imagine two people in different classrooms both have the name **Rahul**.

- Classroom A → Rahul
- Classroom B → Rahul

When you're inside Classroom B, "Rahul" refers to the student in Classroom B, not Classroom A.

Similarly, the inner variable hides the outer variable.

---

# 🧠 Interview Explanation

When JavaScript looks for a variable:

1. It first checks the **current scope**.
2. If found, it uses that variable.
3. Otherwise, it searches the **outer scope**.

If the inner scope has a variable with the same name, the outer variable is **shadowed**.

---

# ✍️ Syntax

```javascript
let name = "Yesu";

{
  let name = "John";

  console.log(name);
}

console.log(name);
```

---

# 💻 Example Queries

### Example 1: Block Scope Shadowing

```javascript
let name = "Yesu";

{
  let name = "John";

  console.log(name);
}

console.log(name);
```

**Output**

```text
John
Yesu
```

---

### Example 2: Function Scope Shadowing

```javascript
let message = "Hello";

function greet() {
  let message = "Hi";

  console.log(message);
}

greet();

console.log(message);
```

**Output**

```text
Hi
Hello
```

---

### Example 3: No Shadowing

```javascript
let age = 20;

{
  console.log(age);
}
```

**Output**

```text
20
```

Since there is no inner `age`, JavaScript uses the outer one.

---

# ❓ Common Interview Questions

### Q1. What is variable shadowing?

Variable shadowing occurs when an inner scope declares a variable with the same name as an outer scope variable, hiding the outer variable.

---

### Q2. Does shadowing change the outer variable?

❌ No.

It only hides it inside the inner scope.

---

### Q3. Which value is printed?

```javascript
let x = 10;

{
  let x = 20;
  console.log(x);
}

console.log(x);
```

**Output**

```text
20
10
```

---

# 🧩 Interview Follow-up Questions

### Can `let` shadow `let`?

✅ Yes.

```javascript
let a = 10;

{
  let a = 20;
}
```

---

### Can `const` shadow `const`?

✅ Yes.

```javascript
const PI = 3.14;

{
  const PI = 22 / 7;
}
```

---

### Can `var` shadow `var`?

✅ Yes, but because `var` is **function-scoped**, its behavior can be confusing. In modern JavaScript, prefer `let` and `const`.

---

### What is Illegal Shadowing?

Illegal shadowing happens when a `var` declaration tries to shadow a `let` or `const` variable **within the same scope chain**, which causes an error.

```javascript
let x = 10;

{
  var x = 20; // ❌ SyntaxError
}
```

---

# 📝 Practice Exercises

1. Create an outer variable `name`.
2. Shadow it inside a block using `let`.
3. Shadow it inside a function.
4. Try illegal shadowing using `var` and observe the error.

---

# ⚠️ Common Mistakes

❌ Thinking shadowing changes the outer variable.

```javascript
let x = 10;

{
  let x = 20;
}

console.log(x);
```

Output:

```text
10
```

---

❌ Confusing shadowing with reassignment.

Shadowing creates a **new variable**.

Reassignment changes the **existing variable**.

---

❌ Using `var` in situations that lead to illegal shadowing.

---

# 🔁 Revision Summary

| Concept                 | Meaning                                 |
| ----------------------- | --------------------------------------- |
| Variable Shadowing      | Inner variable hides the outer variable |
| Outer Variable Changed? | ❌ No                                   |
| Works with              | `let`, `const`, `var`                   |
| Best Practice           | Use `let` and `const`                   |

---

# 💡 Key Takeaways

- Variable shadowing occurs when an inner variable has the **same name** as an outer variable.
- The inner variable **hides** the outer variable **only within its scope**.
- The outer variable remains unchanged.
- JavaScript always looks for variables in the **current scope first**, then moves outward.
- Prefer `let` and `const` to avoid confusion with `var`.

```

```
