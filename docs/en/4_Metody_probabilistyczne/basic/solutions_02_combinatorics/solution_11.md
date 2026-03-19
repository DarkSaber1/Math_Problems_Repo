# Task 11 — Modeling Outcomes

In combinatorial and probabilistic problems, the number of outcomes depends not only on the physical experiment, but also on **how the outcomes are recorded**.

The same real-world situation may lead to different counts depending on whether:

- objects are treated as **distinguishable** or **indistinguishable**,
- **order** is recorded or ignored,
- positions are treated as distinct.

We answer each conceptual question carefully.

---

## 1. Distinguishable vs Indistinguishable Objects

A box contains:

- 4 red balls,
- 4 blue balls,
- 3 green balls.

So there are 11 balls in total.

---

### 1.1 How many linear arrangements of all 11 balls are possible if balls of the same color are treated as indistinguishable?

We arrange all 11 balls in a line.

If balls of the same color are treated as **indistinguishable**, then we do not care which particular red ball is used in a red position.  
We only care about the color pattern.

So this is a **permutation with repeated elements**.

We have:

- 11 total positions,
- 4 identical red balls,
- 4 identical blue balls,
- 3 identical green balls.

The formula is:

$$
\frac{11!}{4!4!3!}
$$

Now compute step by step:

$$
11! = 39916800
$$

$$
4! = 24, \qquad 3! = 6
$$

So the denominator is

$$
4! \cdot 4! \cdot 3! = 24 \cdot 24 \cdot 6 = 3456
$$

Therefore:

$$
\frac{39916800}{3456} = 11550
$$

### Answer:
$$
11550
$$

---

### 1.2 How many arrangements are possible if every ball is individually labeled?

Now suppose every ball is different:

$$
R_1, R_2, R_3, R_4,\; B_1, B_2, B_3, B_4,\; G_1, G_2, G_3
$$

So now all 11 balls are **distinguishable**.

That means every rearrangement of the 11 objects counts as a different arrangement.

This is an ordinary **permutation** of 11 distinct objects:

$$
11!
$$

Compute:

$$
11! = 39916800
$$

### Answer:
$$
39916800
$$

---

### 1.3 Explain why the answers in parts (1) and (2) are different.

The answers are different because the two parts use **different recording rules**.

In part (1), balls of the same color are treated as identical.  
So swapping two red balls does **not** create a new arrangement, because the color pattern stays the same.

For example, if two red balls exchange positions, the arrangement still looks exactly the same when we record only colors.

In part (2), every ball has its own label, so all balls are distinct objects.  
Now swapping \(R_1\) and \(R_2\) creates a new arrangement, because the labels are different.

So:

- in part (1), many linear orders are considered the same,
- in part (2), every linear order is counted separately.

That is why the number in part (2) is much larger.

---

## 2. Recording Order vs Ignoring Order

Three balls are drawn **without replacement** from the same box.

The box still contains:

- 4 red,
- 4 blue,
- 3 green.

Now we count outcomes depending on how the result is recorded.

---

### 2.1 How many outcomes are possible if only the set of colors is recorded (order ignored)?

We draw 3 balls, but only the **set/multiset of colors** matters.

That means:

- order does not matter,
- we only record how many reds, blues, and greens appear,
- drawing \(R,B,G\) is the same as drawing \(G,R,B\).

So we need all possible color combinations of 3 draws from the colors:

$$
R,\; B,\; G
$$

with repetition allowed up to the available numbers.  
Since we draw only 3 balls, and there are at least 3 balls of each color available except green has exactly 3, all natural 3-ball color patterns are possible.

We list the possibilities by type:

### Case 1: All three balls have the same color

Possible sets:

- \(RRR\)
- \(BBB\)
- \(GGG\)

So there are:

$$
3
$$

outcomes.

### Case 2: Two balls of one color and one ball of another color

Possible multisets:

- \(RRB\)
- \(RRG\)
- \(BBR\)
- \(BBG\)
- \(GGR\)
- \(GGB\)

So there are:

$$
6
$$

outcomes.

### Case 3: All three colors appear

Possible multiset:

- \(RBG\)

So there is:

$$
1
$$

outcome.

### Total

$$
3 + 6 + 1 = 10
$$

### Answer:
$$
10
$$

---

### 2.2 How many outcomes are possible if the sequence of colors is recorded?

Now order matters.

So:

- \(RBG\),
- \(GRB\),
- \(BRG\)

are considered different outcomes.

Since each draw can produce one of the three colors:

$$
R,\; B,\; G
$$

and drawing 3 balls is possible for all these color choices, the number of color sequences of length 3 is

$$
3^3 = 27
$$

Another way to understand this is:

- 3 choices for the first color,
- 3 choices for the second color,
- 3 choices for the third color.

Thus:

$$
3 \cdot 3 \cdot 3 = 27
$$

### Answer:
$$
27
$$

---

### 2.3 Explain why recording the order changes the counting model.

Recording order changes the model because outcomes that were previously considered the same now become different.

If order is ignored, then a result such as:

$$
R,B,G
$$

is treated only as the collection of colors present.

So

$$
RBG,\; GRB,\; BRG,\; BGR,\; GBR,\; RGB
$$

all represent the same unordered outcome.

But if order is recorded, then each of these is a different sequence.

So:

- when order is ignored, the outcome is an **unordered selection** (or multiset of colors),
- when order is recorded, the outcome is an **ordered sequence**.

This changes the counting model and usually increases the number of outcomes.

---

## 3. PIN Code vs Number

A security system uses 4-digit PIN codes with digits from 0 to 9.

---

### 3.1 How many different PIN codes are possible if repetition is allowed?

A PIN code has 4 positions.

Each position can contain any of the 10 digits:

$$
0,1,2,3,4,5,6,7,8,9
$$

Repetition is allowed, so each position is chosen independently.

Therefore, the number of possible PIN codes is

$$
10^4 = 10000
$$

### Answer:
$$
10000
$$

---

### 3.2 Consider 4-digit numbers, where the first digit cannot be zero. How many such numbers exist?

A 4-digit number cannot begin with \(0\), otherwise it would not be a 4-digit number.

So:

- first digit: 9 choices \((1,\dots,9)\),
- second digit: 10 choices,
- third digit: 10 choices,
- fourth digit: 10 choices.

Thus the number of 4-digit numbers is

$$
9 \cdot 10 \cdot 10 \cdot 10 = 9000
$$

### Answer:
$$
9000
$$

---

### 3.3 Explain why a PIN code and a 4-digit number are counted using different rules.

A PIN code is not treated as a numerical value in the usual sense.  
It is treated as a **4-position code**.

That means leading zeros are allowed.

For example:

$$
0123
$$

is a valid PIN code.

But it is **not** a 4-digit number, because as a number it is just

$$
123
$$

which has only 3 digits.

So the counting rules are different:

- for a PIN code, each of the 4 positions has 10 choices,
- for a 4-digit number, the first position cannot be 0.

That is why:

- PIN codes: \(10^4 = 10000\),
- 4-digit numbers: \(9 \cdot 10^3 = 9000\).

---

### 3.4 Explain why the codes \(1234\) and \(4321\) must be treated as different outcomes.

A PIN code is an **ordered sequence** of digits.

This means the position of each digit matters.

In the code

$$
1234
$$

the digit \(1\) is in the first position and \(4\) is in the last position.

In the code

$$
4321
$$

the positions are completely different.

Since a PIN system reads the digits in order, these two codes unlock the system differently.

Therefore:

$$
1234 \neq 4321
$$

as PIN codes.

They must be counted as different outcomes because changing the order changes the code.

---

# Final Answers

## 1. Distinguishable vs Indistinguishable Objects

1. If balls of the same color are indistinguishable:

$$
\frac{11!}{4!4!3!} = 11550
$$

2. If every ball is individually labeled:

$$
11! = 39916800
$$

3. The answers differ because identical-color balls are not distinguished in part (1), but labeled balls are all distinct in part (2).

---

## 2. Recording Order vs Ignoring Order

1. If only the set of colors is recorded:

$$
10
$$

2. If the sequence of colors is recorded:

$$
3^3 = 27
$$

3. Recording order changes the model from an unordered color outcome to an ordered sequence.

---

## 3. PIN Code vs Number

1. Number of 4-digit PIN codes with repetition allowed:

$$
10^4 = 10000
$$

2. Number of 4-digit numbers:

$$
9 \cdot 10^3 = 9000
$$

3. They are counted differently because PIN codes may begin with \(0\), but 4-digit numbers may not.

4. \(1234\) and \(4321\) are different because a PIN code is an ordered sequence, so changing the order changes the outcome.