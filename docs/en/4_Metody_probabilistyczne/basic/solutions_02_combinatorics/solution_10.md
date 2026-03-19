# Task 10 — Urn Models

An urn contains:

- 5 red balls  
- 4 blue balls  
- 3 green balls  

Total number of balls:

$$
5 + 4 + 3 = 12
$$

We solve each problem by carefully identifying:

- whether **order matters**,
- whether we use **combinations** or **sequences**.

---

## 1. Three balls are drawn without replacement. How many samples are possible if order is ignored?

We draw 3 balls from 12, and **order is ignored**.

So we are selecting a set of 3 balls from 12 balls.

This is a **combination**:

$$
\binom{12}{3}
$$

Compute:

$$
\binom{12}{3} = \frac{12 \cdot 11 \cdot 10}{3 \cdot 2 \cdot 1} = 220
$$

### Answer:
$$
220
$$

---

## 2. How many samples contain exactly two red balls?

We want 3 balls total, with:

- exactly 2 red balls,
- and 1 ball that is not red.

### Step 1: Choose 2 red balls from 5

$$
\binom{5}{2}
$$

### Step 2: Choose 1 non-red ball

Non-red balls = blue + green = \(4 + 3 = 7\)

$$
\binom{7}{1}
$$

### Step 3: Multiply

$$
\binom{5}{2} \cdot \binom{7}{1}
$$

Compute:

$$
\binom{5}{2} = 10, \quad \binom{7}{1} = 7
$$

$$
10 \cdot 7 = 70
$$

### Answer:
$$
70
$$

---

## 3. Three balls are drawn and the order of colors is recorded. How many outcomes are possible?

Now **order matters**, and we are recording only **colors**, not individual balls.

So each draw results in a color:

- Red (R),
- Blue (B),
- Green (G)

We draw 3 times, without replacement, but we only care about colors.

We must count all valid sequences of length 3 using the colors R, B, G, with limits:

- at most 5 R,
- at most 4 B,
- at most 3 G.

Since we are only drawing 3 balls, these limits are not restrictive.

So each position can be:

- R, B, or G

Thus, the number of possible sequences is:

$$
3^3 = 27
$$

### Answer:
$$
27
$$

---

## 4. How many outcomes contain exactly two red balls?

We now count sequences of length 3 (order matters) with:

- exactly 2 R,
- and 1 non-red (B or G).

### Step 1: Choose positions for the 2 red balls

We choose 2 positions out of 3:

$$
\binom{3}{2} = 3
$$

### Step 2: Choose the remaining color

The remaining position can be:

- Blue (B), or
- Green (G)

So:

$$
2 \text{ choices}
$$

### Step 3: Multiply

$$
\binom{3}{2} \cdot 2 = 3 \cdot 2 = 6
$$

### Answer:
$$
6
$$

---

# Final Answers

1. Number of samples (order ignored):

$$
\binom{12}{3} = 220
$$

2. Number of samples with exactly 2 red balls:

$$
\binom{5}{2}\binom{7}{1} = 70
$$

3. Number of ordered color sequences:

$$
3^3 = 27
$$

4. Number of sequences with exactly 2 red balls:

$$
\binom{3}{2} \cdot 2 = 6
$$
