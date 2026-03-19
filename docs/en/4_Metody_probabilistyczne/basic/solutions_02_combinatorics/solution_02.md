# Task 2 — Permutations

In this task we use the idea of a **permutation**, because we are arranging objects in order.

For \(n\) distinct objects, the number of linear arrangements is

$$
n!
$$

We will analyze each problem carefully and explain why the formula works.

---

## 1. In how many ways can 8 different books be arranged on a shelf?

We have 8 different books, and we want to place them on a shelf.

A shelf is a **linear arrangement**, so order matters.  
For example, placing Book A first and Book B second is different from placing Book B first and Book A second.

Since all 8 books are different and all of them are used, this is a permutation of 8 distinct objects.

Thus, the number of arrangements is

$$
8!
$$

Now compute:

$$
8! = 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 40320
$$

### Answer:
$$
40320
$$

---

## 2. In how many ways can 8 people sit in a row if two particular people must sit next to each other?

We now have 8 people sitting in a row, but with one condition:

Two particular people must sit together.

Let these two people be \(A\) and \(B\).

A standard method for this kind of problem is the **block method**.

### Step 1: Treat the two people as one block

If \(A\) and \(B\) must stay together, then we can temporarily treat them as a single object:

- one block \((AB)\),
- plus the remaining 6 people.

So instead of arranging 8 separate people, we arrange **7 objects** in total.

The number of ways to arrange these 7 objects is

$$
7!
$$

### Step 2: Arrange the two people inside the block

Inside the block, the two people can switch places:

- \(AB\)
- \(BA\)

So there are

$$
2!
$$

ways inside the block.

### Step 3: Multiply the results

By the product rule:

$$
7! \cdot 2!
$$

Now compute:

$$
7! = 5040, \qquad 2! = 2
$$

So:

$$
7! \cdot 2! = 5040 \cdot 2 = 10080
$$

### Answer:
$$
10080
$$

---

## 3. In how many ways can they sit if those two people must **not** sit next to each other?

Again we have 8 people in a row, and two particular people \(A\) and \(B\).

This time, we want the number of arrangements where \(A\) and \(B\) are **not** adjacent.

The easiest method is:

$$
\text{(all arrangements)} - \text{(arrangements where they sit together)}
$$

### Step 1: Count all possible arrangements

With 8 distinct people in a row, the total number of arrangements is

$$
8!
$$

Compute:

$$
8! = 40320
$$

### Step 2: Count arrangements where the two people sit together

From part 2, this number is

$$
7! \cdot 2! = 10080
$$

### Step 3: Subtract

So the number of arrangements where they do **not** sit together is

$$
8! - 7! \cdot 2!
$$

Substitute the values:

$$
40320 - 10080 = 30240
$$

### Answer:
$$
30240
$$

---

## 4. In how many ways can 10 questions in a test be ordered if the first question is fixed?

We have 10 questions in total, but the first question is already fixed in place.

That means we do **not** have freedom to arrange all 10 questions.  
The first one stays where it is, and only the remaining 9 questions can be reordered.

So we only need to count the number of permutations of the remaining 9 questions.

Thus, the number of possible orderings is

$$
9!
$$

Now compute:

$$
9! = 9 \cdot 8 \cdot 7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 362880
$$

### Answer:
$$
362880
$$

---

# Final Answers

1. 8 different books on a shelf:

$$
8! = 40320
$$

2. 8 people in a row, with two particular people sitting together:

$$
7! \cdot 2! = 10080
$$

3. 8 people in a row, with two particular people not sitting together:

$$
8! - 7! \cdot 2! = 30240
$$

4. 10 questions ordered, with the first question fixed:

$$
9! = 362880
$$