# 📖 What is Type Coercion?

Type coercion is the **automatic conversion of one data type to another by JavaScript**.

JavaScript performs type coercion when an operation involves values of different data types.

---

# 🤔 Why is it Needed?

Sometimes operations involve different data types.

Instead of throwing an error, JavaScript automatically converts one type to another so the operation can continue.

This makes JavaScript flexible, but it can also lead to unexpected results.

---

# 🌍 Real-world Example

Imagine you have:

- Number → `10`
- String → `"20"`

If someone asks you to add them, you first decide **how to treat them**.

- As numbers → `30`
- As strings → `"1020"`

JavaScript makes this decision automatically based on the operator.

---

# 🧠 Interview Explanation

Type coercion is JavaScript's **automatic type conversion**.

There are two types:

### 1. Implicit Coercion (Automatic)

JavaScript converts the type automatically.

```javascript
5 + "5";
```

Output:

```text
"55"
```

The number `5` is converted to the string `"5"`.

---

### 2. Explicit Coercion (Manual)

The developer converts the type.

```javascript
Number("5");
```

Output:

```text
5
```

---

# ✍️ Syntax

### Implicit Coercion

```javascript
value1 operator value2;
```

### Explicit Coercion

```javascript
Number(value);
String(value);
Boolean(value);
```

---

# 💻 Example Queries

### Example 1: String + Number

```javascript
5 + "5";
```

**Output**

```text
"55"
```

---

### Example 2: String - Number

```javascript
"10" - 5;
```

**Output**

```text
5
```

> The `-` operator converts the string to a number.

---

### Example 3: String × Number

```javascript
"5" * 2;
```

**Output**

```text
10
```

---

### Example 4: Boolean + Number

```javascript
true + 1;
```

**Output**

```text
2
```

Because:

```text
true → 1
```

---

### Example 5: Explicit Conversion

```javascript
Number("100");
```

**Output**

```text
100
```

---

# ❓ Common Interview Questions

### Q1. What is type coercion?

Type coercion is the automatic conversion of one data type to another by JavaScript.

---

### Q2. What are the two types of type coercion?

- **Implicit Coercion** → Automatic conversion by JavaScript.
- **Explicit Coercion** → Manual conversion by the developer.

---

### Q3. What is the output?

```javascript
5 + "5";
```

**Output**

```text
"55"
```

---

### Q4. What is the output?

```javascript
"10" - 5;
```

**Output**

```text
5
```

---

### Q5. What is the output?

```javascript
true + 1;
```

**Output**

```text
2
```

---

# 🧩 Interview Follow-up Questions

### Why does `+` behave differently from `-`?

- The **`+` operator** performs **string concatenation** if either operand is a string.
- Operators like `-`, `*`, and `/` expect numbers, so JavaScript converts strings to numbers.

Example:

```javascript
5 + "5"; // "55"
"5" - 2; // 3
"5" * 2; // 10
```

---

### How can you avoid unexpected type coercion?

- Use **`===`** instead of `==`.
- Convert values explicitly using:
  - `Number()`
  - `String()`
  - `Boolean()`

---

# 📝 Practice Exercises

Predict the output:

```javascript
10 + "20";
```

```javascript
"20" - 10;
```

```javascript
"5" * "2";
```

```javascript
false + 1;
```

```javascript
Number("50");
```

---

# ⚠️ Common Mistakes

❌ Assuming `+` always performs addition.

```javascript
5 + "5";
```

Output:

```text
"55"
```

---

❌ Using `==` without understanding type coercion.

```javascript
5 == "5";
```

Output:

```text
true
```

---

❌ Relying on automatic conversions.

> Prefer explicit conversion for clearer and more predictable code.

---

# 🔁 Revision Summary

| Expression     | Output | Reason                     |
| -------------- | ------ | -------------------------- |
| `5 + "5"`      | `"55"` | String concatenation       |
| `"10" - 5`     | `5`    | String converted to number |
| `"5" * 2`      | `10`   | String converted to number |
| `true + 1`     | `2`    | `true` becomes `1`         |
| `Number("10")` | `10`   | Explicit conversion        |

---

# 💡 Key Takeaways

- Type coercion is the **automatic conversion** of one data type to another.
- **Implicit coercion** is done by JavaScript.
- **Explicit coercion** is done by the developer.
- The **`+` operator** can concatenate strings.
- The **`-`, `*`, and `/` operators** convert strings to numbers.
- Use **`===`** and explicit conversions to avoid unexpected behavior.
