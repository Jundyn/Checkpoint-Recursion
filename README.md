# 🔁 Palindrome Checker

## 📌 Overview

This project implements a function to test whether a given word is a **palindrome**.

A palindrome is a word that reads the same **forward and backward**, such as:

* `gag`
* `kayak`
* `radar`
* `php`

---

## 🧠 Concept

The algorithm works by comparing characters from both ends of the word:

* Compare the **first** and **last** characters
* If they are equal → check the remaining substring
* If they are different → stop (not a palindrome)

### ✅ Stop Condition

* An **empty string** is a palindrome
* A **single character** is a palindrome

---

## ⚙️ Implementation (Recursive)

```js
function isPalindrome(word) {
  // Base case
  if (word.length <= 1) {
    return true;
  }

  // Compare first and last characters
  if (word[0] === word[word.length - 1]) {
    return isPalindrome(word.slice(1, -1));
  }

  return false;
}
```

---

## 🔁 Alternative Implementation (Iterative)

```js
function isPalindrome(word) {
  let left = 0;
  let right = word.length - 1;

  while (left < right) {
    if (word[left] !== word[right]) {
      return false;
    }
    left++;
    right--;
  }

  return true;
}
```

---

## ▶️ Usage Example

```js
console.log(isPalindrome("gag"));     // true
console.log(isPalindrome("kayak"));   // true
console.log(isPalindrome("radar"));   // true
console.log(isPalindrome("hello"));   // false
```

---

## ✅ Key Takeaways

* Uses **recursion** or **iteration** to compare characters
* Efficient approach by checking only necessary pairs
* Demonstrates **problem-solving with base cases and conditions**

---

## 👨‍💻 Author

Junaid Omotade

---
