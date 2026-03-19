# Task 5 — Combinations

In this task we use **combinations**, because we are selecting people into committees.

A committee is a **group**, not an ordered list.  
That means the order of the selected people does **not** matter.

For example, the committee

$$
\{A, B, C, D\}
$$

is the same as

$$
\{D, C, B, A\}
$$

So whenever we choose \(k\) people from \(n\) people and order does not matter, we use the combination formula:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

We now solve each part step by step.

---

## 1. A committee of 4 people is chosen from 12 students. How many committees are possible?

We are choosing 4 people from 12 students.

Since a committee is an unordered selection, we use combinations:

$$
\binom{12}{4}
$$

Now compute:

$$
\binom{12}{4} = \frac{12!}{4!8!}
$$

Simplify:

$$
\binom{12}{4} = \frac{12 \cdot 11 \cdot 10 \cdot 9}{4 \cdot 3 \cdot 2 \cdot 1}
$$

$$
= \frac{11880}{24} = 495
$$

### Answer:
$$
495
$$

---

## 2. How many committees contain a particular student?

Now one specific student must definitely be included in the committee.

So we first fix that student as already chosen.

That leaves:

- 11 students remaining,
- and we still need 3 more people to complete the 4-person committee.

So the number of such committees is

$$
\binom{11}{3}
$$

Now compute:

$$
\binom{11}{3} = \frac{11!}{3!8!}
$$

Simplify:

$$
\binom{11}{3} = \frac{11 \cdot 10 \cdot 9}{3 \cdot 2 \cdot 1}
$$

$$
= \frac{990}{6} = 165
$$

### Answer:
$$
165
$$

---

## 3. How many committees contain **at least one** of two particular students?

Let the two particular students be \(A\) and \(B\).

We want the number of 4-person committees that contain **at least one** of them.

A very convenient method here is the **complement method**:

### Step 1: Count all committees

From part 1, the total number of 4-person committees from 12 students is

$$
\binom{12}{4} = 495
$$

### Step 2: Count committees containing neither \(A\) nor \(B\)

If neither \(A\) nor \(B\) is included, then all 4 committee members must be chosen from the remaining 10 students.

So this number is

$$
\binom{10}{4}
$$

Now compute:

$$
\binom{10}{4} = \frac{10!}{4!6!}
$$

Simplify:

$$
\binom{10}{4} = \frac{10 \cdot 9 \cdot 8 \cdot 7}{4 \cdot 3 \cdot 2 \cdot 1}
$$

$$
= \frac{5040}{24} = 210
$$

### Step 3: Subtract

So the number of committees containing **at least one** of the two students is

$$
\binom{12}{4} - \binom{10}{4}
$$

$$
= 495 - 210 = 285
$$

### Answer:
$$
285
$$

---

## 4. How many committees contain exactly two women if the group consists of 7 men and 5 women?

We need a 4-person committee with **exactly 2 women**.

That means:

- choose 2 women from 5,
- choose 2 men from 7.

These two choices are independent, so we multiply them.

Thus the number of such committees is

$$
\binom{5}{2}\binom{7}{2}
$$

### Step 1: Compute the number of ways to choose 2 women

$$
\binom{5}{2} = \frac{5!}{2!3!} = \frac{5 \cdot 4}{2 \cdot 1} = 10
$$

### Step 2: Compute the number of ways to choose 2 men

$$
\binom{7}{2} = \frac{7!}{2!5!} = \frac{7 \cdot 6}{2 \cdot 1} = 21
$$

### Step 3: Multiply

$$
\binom{5}{2}\binom{7}{2} = 10 \cdot 21 = 210
$$

### Answer:
$$
210
$$

---

# Final Answers

1. Number of committees of 4 from 12 students:

$$
\binom{12}{4} = 495
$$

2. Number of committees containing a particular student:

$$
\binom{11}{3} = 165
$$

3. Number of committees containing at least one of two particular students:

$$
\binom{12}{4} - \binom{10}{4} = 285
$$

4. Number of committees containing exactly two women from 7 men and 5 women:

$$
\binom{5}{2}\binom{7}{2} = 210
$$