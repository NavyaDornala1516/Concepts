
# AMA

## 1. Difference between `div` and `span` in HTML

- **`div`**: Block-level element. Starts on a new line and takes full width.
- **`span`**: Inline element. Stays within a line and takes only the required space.

```html
<div>This is a block-level element</div>
<span>This is an inline element</span>
```

---

## 2. `z-index` in CSS

- Determines the stack order of elements (what appears on top).
- Only works on elements with position set (`relative`, `absolute`, `fixed`, `sticky`).
- Higher `z-index` means the element appears above those with lower values.

```css
.box1 {
  position: absolute;
  z-index: 1;
}
.box2 {
  position: absolute;
  z-index: 2;
}
```

---

## 3. Difference between `forEach` and `for` loop in JavaScript

- **`forEach`**:
  - Works on arrays.
  - Cannot use `break` or `return` to exit early.
- **`for`**:
  - General purpose loop.
  - Can loop through anything with index.
  - Supports `break`, `continue`, `return`.

```js
[1, 2, 3].forEach(num => console.log(num)); // forEach

for (let i = 0; i < 3; i++) {
  console.log(i); // for loop
}
```

---

## 4. How to check disk usage and space in CLI

- **Disk usage of a folder**: `du -sh foldername`
- **Free disk space**: `df -h`

```bash
du -sh /home/user
df -h
```

---

## 5. Concept of branches in version control system

- Branches are used to develop features or fixes **independently** of the main code.
- Common in Git (e.g., `main`, `dev`, `feature-x`).
- Helps in collaboration, testing, and avoiding breaking the main codebase.

```bash
git branch feature-login
git checkout feature-login
```

---

## 6. What is INNER JOIN and LEFT JOIN in SQL

- **INNER JOIN**: Returns rows with **matching values** in both tables.
- **LEFT JOIN**: Returns **all rows from the left table**, and matched rows from the right. If no match, NULLs are returned.

```sql
-- INNER JOIN
SELECT * FROM A
INNER JOIN B ON A.id = B.a_id;

-- LEFT JOIN
SELECT * FROM A
LEFT JOIN B ON A.id = B.a_id;
```

---

## 7. What is schema in PostgreSQL

- A schema is a **namespace** that contains database objects like tables, views, functions.
- Helps in organizing and separating objects.

```sql
CREATE SCHEMA company;
CREATE TABLE company.employees (...);
```

---

## 8. Difference between `pop()` and `pop(index)` in Python

- **`pop()`**: Removes and returns the last element.
- **`pop(index)`**: Removes and returns element at specified index.

```python
my_list = [10, 20, 30]
my_list.pop()    # Returns 30
my_list.pop(0)   # Returns 10
```

---

## 9. Difference between `null` and `undefined` in JavaScript

- **`undefined`**: A variable is declared but not assigned a value.
- **`null`**: A value explicitly set by the developer to mean "no value".

```js
let a;        // undefined
let b = null; // null
```

---

## 10. Difference between `for...in` and `for...of` in JavaScript

- **`for...in`**: Iterates over keys (property names) of an object.
- **`for...of`**: Iterates over values of an iterable (like arrays, strings).

```js
const arr = ['a', 'b'];

for (let i in arr) {
  console.log(i); // 0, 1
}

for (let val of arr) {
  console.log(val); // a, b
}
```

---
