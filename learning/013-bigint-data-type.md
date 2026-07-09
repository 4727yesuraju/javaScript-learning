# 📖 What is BigInt?

`BigInt` is a **primitive data type** introduced in **ES2020 (ES11)**.

It is used to store **very large integers** that are larger than the maximum safe integer supported by the `Number` data type.

---

# 🤔 Why is it Needed?

The `Number` data type can safely represent integers only up to:

```javascript
Number.MAX_SAFE_INTEGER;
```

Output:

```text
9007199254740991
```

If you need to work with numbers larger than this, use **BigInt**.

---

# 🌍 Real-world Example

Imagine a bank storing the total number of transactions over many years.

The number could become extremely large.

Using `Number` may lose precision, while `BigInt` stores it accurately.

---

# 🧠 Interview Explanation

A `BigInt` is a primitive data type used to represent **integers of arbitrary size**.

Create a BigInt by adding **`n`** to the end of an integer.

```javascript
const bigNumber = 123456789012345678901234567890n;
```

---

# ✍️ Syntax

### Using `n`

```javascript
const bigNum = 12345678901234567890n;
```

### Using `BigInt()`

```javascript
const bigNum = BigInt("12345678901234567890");
```

---

# 💻 Example Queries

### Example 1: Creating a BigInt

```javascript
const num = 12345678901234567890n;

console.log(num);
```

---

### Example 2: Checking the Type

```javascript
const num = 100n;

console.log(typeof num);
```

**Output**

```text
"bigint"
```

---

### Example 3: Addition

```javascript
const a = 10n;
const b = 20n;

console.log(a + b);
```

**Output**

```text
30n
```

---

### Example 4: Mixing `Number` and `BigInt`

```javascript
10n + 5;
```

**Output**

```text
TypeError
```

> You cannot directly mix `BigInt` and `Number`.

---

# ❓ Common Interview Questions

### Q1. What is BigInt?

A primitive data type used to store **very large integers** beyond the safe range of `Number`.

---

### Q2. When was BigInt introduced?

**ES2020 (ES11)**

---

### Q3. How do you create a BigInt?

Using the `n` suffix:

```javascript
123n;
```

Or:

```javascript
BigInt("123");
```

---

### Q4. What is the output?

```javascript
typeof 100n;
```

**Output**

```text
"bigint"
```

---

# 🧩 Interview Follow-up Questions

### Can you mix `Number` and `BigInt`?

❌ No.

```javascript
10n + 5;
```

Throws a `TypeError`.

Convert one type to the other first if needed.

---

### Does BigInt support decimal numbers?

❌ No.

BigInt stores **integers only**.

```javascript
10.5n; // SyntaxError
```

---

### When should you use BigInt?

Use it when working with **very large integers** that exceed `Number.MAX_SAFE_INTEGER`.

---

# 📝 Practice Exercises

1. Create a BigInt using the `n` suffix.
2. Create a BigInt using `BigInt()`.
3. Check its type using `typeof`.
4. Add two BigInt values.
5. Try adding a `BigInt` and a `Number` and observe the result.

---

# ⚠️ Common Mistakes

❌ Forgetting the `n` suffix.

```javascript
12345678901234567890;
```

This is treated as a `Number` and may lose precision.

---

❌ Mixing `Number` and `BigInt`.

```javascript
10n + 5;
```

Results in a `TypeError`.

---

❌ Using decimal values with BigInt.

```javascript
10.5n;
```

This causes a `SyntaxError`.

---

# 🔁 Revision Summary

| Feature         | BigInt               |
| --------------- | -------------------- |
| Data Type       | Primitive            |
| Introduced In   | ES2020 (ES11)        |
| Stores          | Large integers       |
| Decimal Support | ❌ No                |
| `typeof`        | `"bigint"`           |
| Creation        | `123n` or `BigInt()` |

---

# 💡 Key Takeaways

- `BigInt` is a **primitive data type** introduced in **ES2020**.
- It is used for **very large integers** beyond `Number.MAX_SAFE_INTEGER`.
- Create a BigInt using the **`n` suffix** or the `BigInt()` constructor.
- `typeof` a BigInt returns `"bigint"`.
- You **cannot mix** `BigInt` and `Number` directly.
- BigInt supports **integers only**, not decimal values.
