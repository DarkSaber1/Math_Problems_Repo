# Task 9 — Digit Restrictions

In this task we count **5-digit numbers** under different restrictions.

A **5-digit number** is different from a 5-digit PIN code:

- a PIN code may begin with \(0\),
- but a 5-digit number cannot begin with \(0\).

So for 5-digit numbers:

- the first digit must be one of \(1,2,\dots,9\),
- the other digits may be any of \(0,1,\dots,9\), unless additional restrictions are given.

We solve each part carefully.

---

## 1. How many 5-digit numbers exist?

A 5-digit number has 5 positions.

### Step 1: Choose the first digit

The first digit cannot be \(0\), otherwise the number would not be a 5-digit number.

So the first digit has:

$$
9
$$

choices: \(1,2,\dots,9\)

### Step 2: Choose the remaining 4 digits

Each of the remaining four positions can be any digit from \(0\) to \(9\).

So each of these positions has:

$$
10
$$

choices.

### Step 3: Multiply

By the product rule:

$$
9 \cdot 10 \cdot 10 \cdot 10 \cdot 10 = 9 \cdot 10^4
$$

Thus:

$$
9 \cdot 10^4 = 90000
$$

### Answer:
$$
90000
$$

---

## 2. How many of them are even?

A number is **even** if its last digit is one of:

$$
0,2,4,6,8
$$

So the last digit has:

$$
5
$$

choices.

### Step 1: Choose the first digit

As before, the first digit cannot be \(0\), so it has:

$$
9
$$

choices.

### Step 2: Choose the middle three digits

The 2nd, 3rd, and 4th digits can each be any digit from \(0\) to \(9\), so each has:

$$
10
$$

choices.

### Step 3: Choose the last digit

To make the number even, the last digit must be one of the 5 even digits:

$$
5
$$

choices.

### Step 4: Multiply

So the total number of even 5-digit numbers is

$$
9 \cdot 10 \cdot 10 \cdot 10 \cdot 5
$$

$$
= 9 \cdot 10^3 \cdot 5
$$

$$
= 9000 \cdot 5 = 45000
$$

### Answer:
$$
45000
$$

---

## 3. How many contain no repeated digits?

Now we count 5-digit numbers in which all digits are different.

This means:

- the first digit cannot be \(0\),
- no digit may be used more than once.

### Step 1: Choose the first digit

The first digit must be one of \(1,2,\dots,9\), so there are:

$$
9
$$

choices.

### Step 2: Choose the second digit

Now one digit has already been used.

There are 10 digits total, so 9 digits remain available.

Since the second digit may be \(0\), all remaining 9 digits are allowed.

So the second digit has:

$$
9
$$

choices.

### Step 3: Choose the third digit

Now 2 digits are already used, so there are:

$$
8
$$

choices left.

### Step 4: Choose the fourth digit

There are now:

$$
7
$$

choices left.

### Step 5: Choose the fifth digit

There are now:

$$
6
$$

choices left.

### Step 6: Multiply

So the number of 5-digit numbers with no repeated digits is

$$
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6
$$

Now compute:

$$
9 \cdot 9 = 81
$$

$$
81 \cdot 8 = 648
$$

$$
648 \cdot 7 = 4536
$$

$$
4536 \cdot 6 = 27216
$$

So:

$$
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27216
$$

### Answer:
$$
27216
$$

---

## 4. How many contain at least one repeated digit?

We now want the number of 5-digit numbers that contain **at least one repeated digit**.

Again, the easiest method is the **complement method**:

$$
\text{numbers with at least one repeated digit}
=
\text{all 5-digit numbers} - \text{numbers with no repeated digits}
$$

From part 1:

$$
90000
$$

From part 3:

$$
27216
$$

So:

$$
90000 - 27216 = 62784
$$

### Answer:
$$
62784
$$

---

# Final Answers

1. Number of 5-digit numbers:

$$
9 \cdot 10^4 = 90000
$$

2. Number of even 5-digit numbers:

$$
9 \cdot 10^3 \cdot 5 = 45000
$$

3. Number of 5-digit numbers with no repeated digits:

$$
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27216
$$

4. Number of 5-digit numbers with at least one repeated digit:

$$
90000 - 27216 = 62784
$$