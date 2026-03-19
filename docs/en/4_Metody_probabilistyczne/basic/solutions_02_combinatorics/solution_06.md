# Task 6 — Combinations in Card Problems

In all parts of this task, we are dealing with **5-card hands** drawn from a standard deck of 52 cards.

A **hand** is an unordered selection of cards, so the order in which the cards are drawn does **not** matter.

Therefore, throughout this task we use **combinations**.

Recall the combination formula:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

A standard deck contains:

- 52 cards in total,
- 13 hearts,
- 39 non-hearts,
- 12 face cards (J, Q, K in 4 suits),
- 40 non-face cards.

We now solve each problem step by step.

---

## 1. In how many ways can 5 cards be drawn so that the hand contains exactly 2 hearts?

We want a 5-card hand with:

- exactly 2 hearts,
- therefore the remaining 3 cards must be non-hearts.

### Step 1: Choose 2 hearts from the 13 hearts

The number of ways is

$$
\binom{13}{2}
$$

### Step 2: Choose 3 non-hearts from the 39 non-hearts

The number of ways is

$$
\binom{39}{3}
$$

### Step 3: Multiply

These two selections are independent, so by the product rule the total number of such hands is

$$
\binom{13}{2}\binom{39}{3}
$$

Now compute the values:

$$
\binom{13}{2} = \frac{13 \cdot 12}{2} = 78
$$

$$
\binom{39}{3} = \frac{39 \cdot 38 \cdot 37}{3 \cdot 2 \cdot 1} = 9139
$$

So:

$$
\binom{13}{2}\binom{39}{3} = 78 \cdot 9139 = 712842
$$

### Answer:
$$
712842
$$

---

## 2. In how many ways can a 5-card hand contain at least one heart?

The phrase **at least one heart** means:

- 1 heart,
- or 2 hearts,
- or 3 hearts,
- or 4 hearts,
- or 5 hearts.

Instead of counting all these cases separately, it is easier to use the **complement method**.

### Step 1: Count all 5-card hands

The total number of 5-card hands from 52 cards is

$$
\binom{52}{5}
$$

Compute:

$$
\binom{52}{5} = 2598960
$$

### Step 2: Count hands with no hearts

If a hand contains no hearts, then all 5 cards must come from the 39 non-hearts.

So the number of such hands is

$$
\binom{39}{5}
$$

Compute:

$$
\binom{39}{5} = 575757
$$

### Step 3: Subtract

So the number of hands with at least one heart is

$$
\binom{52}{5} - \binom{39}{5}
$$

$$
2598960 - 575757 = 2023203
$$

### Answer:
$$
2023203
$$

---

## 3. In how many ways can a 5-card hand contain no face cards (J, Q, K)?

A standard deck has 12 face cards:

- 4 Jacks,
- 4 Queens,
- 4 Kings.

So the number of cards that are **not** face cards is

$$
52 - 12 = 40
$$

We want a 5-card hand containing no face cards, so all 5 cards must be chosen from these 40 non-face cards.

Thus the number of such hands is

$$
\binom{40}{5}
$$

Now compute:

$$
\binom{40}{5} = 658008
$$

### Answer:
$$
658008
$$

---

# Final Answers

1. Number of 5-card hands containing exactly 2 hearts:

$$
\binom{13}{2}\binom{39}{3} = 712842
$$

2. Number of 5-card hands containing at least one heart:

$$
\binom{52}{5} - \binom{39}{5} = 2023203
$$

3. Number of 5-card hands containing no face cards:

$$
\binom{40}{5} = 658008
$$