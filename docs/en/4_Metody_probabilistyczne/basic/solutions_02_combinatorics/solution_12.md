# Task 12 — Mixed Counting Problem

This task combines several different counting models.

For each part, we must first identify the correct model by asking:

1. Are we using **all objects** or only **some**?
2. Does **order matter**?
3. Is **repetition allowed**?
4. Are the objects arranged in a line or in a circle?

We solve each subsection carefully.

---

## 1. Student ID Codes

A student identifier consists of:

- two letters chosen from  
  $$
  \{A,B,C,D,E\}
  $$
- followed by three digits from \(0\) to \(9\).

So each identifier has the form:

$$
\text{Letter Letter Digit Digit Digit}
$$

We solve each version separately.

---

### 1.1 How many identifiers are possible if letters and digits may repeat?

#### Step 1: Count the letter part

There are 2 letter positions, and each can be filled by any of the 5 letters.

Since repetition is allowed:

- 5 choices for the first letter,
- 5 choices for the second letter.

So the number of possible letter pairs is

$$
5 \cdot 5 = 5^2 = 25
$$

#### Step 2: Count the digit part

There are 3 digit positions, and each can be filled by any digit from 0 to 9.

Since repetition is allowed:

- 10 choices for each digit.

So the number of digit triples is

$$
10^3 = 1000
$$

#### Step 3: Multiply

The letter part and digit part are independent, so by the product rule:

$$
5^2 \cdot 10^3 = 25 \cdot 1000 = 25000
$$

### Counting model:
- letters: sequence with repetition,
- digits: sequence with repetition.

### Answer:
$$
25000
$$

---

### 1.2 How many identifiers are possible if letters may not repeat but digits may repeat?

Now the two letters must be different.

#### Step 1: Count the letter part

- first letter: 5 choices,
- second letter: 4 choices (because repetition is not allowed).

So the number of possible ordered letter pairs is

$$
5 \cdot 4 = 20
$$

This is a **k-permutation** of 2 letters from 5.

#### Step 2: Count the digit part

Digits may still repeat, so:

$$
10^3 = 1000
$$

#### Step 3: Multiply

$$
20 \cdot 1000 = 20000
$$

### Counting model:
- letters: k-permutation,
- digits: sequence with repetition.

### Answer:
$$
20000
$$

---

### 1.3 How many identifiers are possible if neither letters nor digits may repeat?

Now:

- the two letters must be different,
- the three digits must also all be different.

#### Step 1: Count the letter part

As before:

- first letter: 5 choices,
- second letter: 4 choices.

So:

$$
5 \cdot 4 = 20
$$

#### Step 2: Count the digit part

Now the 3 digits must be distinct:

- first digit: 10 choices,
- second digit: 9 choices,
- third digit: 8 choices.

So the number of digit triples is

$$
10 \cdot 9 \cdot 8 = 720
$$

This is a **k-permutation** of 3 digits from 10.

#### Step 3: Multiply

$$
20 \cdot 720 = 14400
$$

### Counting model:
- letters: k-permutation,
- digits: k-permutation.

### Answer:
$$
14400
$$

---

## 2. Medal Assignment

There are 12 runners, and medals are awarded for:

- gold,
- silver,
- bronze.

Because the medals are different, **order matters**.

So this is an **ordered selection without repetition**, that is, a **k-permutation**.

---

### 2.1 In how many ways can the medals be assigned?

We assign 3 ordered positions (gold, silver, bronze) among 12 runners.

So:

$$
P(12,3)=12 \cdot 11 \cdot 10 = 1320
$$

### Counting model:
k-permutation.

### Answer:
$$
1320
$$

---

### 2.2 Suppose two particular runners must both receive medals. In how many ways can the medals be assigned?

Let the two particular runners be \(A\) and \(B\).

They must both receive medals, so among the 3 medal winners:

- \(A\) must be included,
- \(B\) must be included,
- and the third medal goes to one of the remaining 10 runners.

#### Step 1: Choose the third medalist

There are:

$$
10
$$

choices.

#### Step 2: Assign the 3 medals to the 3 selected runners

Now we have exactly 3 selected runners:

- \(A\),
- \(B\),
- one of the remaining 10.

These 3 runners can be assigned to gold, silver, bronze in

$$
3! = 6
$$

ways.

#### Step 3: Multiply

$$
10 \cdot 3! = 10 \cdot 6 = 60
$$

### Counting model:
- choose the third runner,
- then permute the 3 medalists.

### Answer:
$$
60
$$

---

## 3. Committee Selection

A committee of 4 people is chosen from 10 students, including:

- 6 men,
- 4 women.

A committee is an unordered selection, so we use **combinations**.

---

### 3.1 How many committees are possible?

We choose 4 students from 10:

$$
\binom{10}{4}
$$

Compute:

$$
\binom{10}{4} = 210
$$

### Counting model:
combination.

### Answer:
$$
210
$$

---

### 3.2 How many committees contain exactly two women?

To have exactly 2 women in a 4-person committee:

- choose 2 women from 4,
- choose 2 men from 6.

So:

$$
\binom{4}{2}\binom{6}{2}
$$

Compute:

$$
\binom{4}{2}=6, \qquad \binom{6}{2}=15
$$

Thus:

$$
6 \cdot 15 = 90
$$

### Counting model:
combination in two groups.

### Answer:
$$
90
$$

---

### 3.3 How many committees contain at least one woman?

The easiest method is the **complement method**.

#### Step 1: Count all committees

$$
\binom{10}{4} = 210
$$

#### Step 2: Count committees with no women

If there is no woman, then all 4 committee members must be chosen from the 6 men:

$$
\binom{6}{4} = 15
$$

#### Step 3: Subtract

$$
210 - 15 = 195
$$

### Counting model:
combination with complement.

### Answer:
$$
195
$$

---

## 4. Circular Seating

Seven people sit around a round table.

Since seating is around a circle, we use **circular permutations**.

---

### 4.1 How many different seating arrangements are possible?

For \(n\) distinct people around a round table, the number of circular arrangements is

$$
(n-1)!
$$

So for 7 people:

$$
(7-1)! = 6! = 720
$$

### Counting model:
circular permutation.

### Answer:
$$
720
$$

---

### 4.2 In how many arrangements do two particular people sit next to each other?

Let the two particular people be \(A\) and \(B\).

We treat them as one block.

Then we have:

- one block \((AB)\),
- plus the remaining 5 people.

So there are 6 objects around the table.

The number of circular arrangements of 6 objects is

$$
(6-1)! = 5!
$$

Inside the block, the two people can switch places in

$$
2!
$$

ways.

So the total number of arrangements is

$$
5! \cdot 2! = 120 \cdot 2 = 240
$$

### Counting model:
circular permutation with a block.

### Answer:
$$
240
$$

---

## 5. Passwords

A password consists of 5 characters chosen from:

- digits \(0\)–\(9\),
- letters \(A\)–\(Z\).

So the total number of available symbols is:

$$
10 + 26 = 36
$$

A password is an ordered sequence of 5 characters.

---

### 5.1 How many passwords are possible if repetition is allowed?

Each of the 5 positions can contain any of the 36 symbols.

So the number of passwords is

$$
36^5
$$

Compute:

$$
36^5 = 60466176
$$

### Counting model:
sequence with repetition.

### Answer:
$$
60466176
$$

---

### 5.2 How many passwords are possible if no character may repeat?

Now repetition is not allowed.

So we choose 5 distinct characters from 36, in order:

- first position: 36 choices,
- second position: 35 choices,
- third position: 34 choices,
- fourth position: 33 choices,
- fifth position: 32 choices.

So the number of passwords is

$$
36 \cdot 35 \cdot 34 \cdot 33 \cdot 32
$$

Compute step by step:

$$
36 \cdot 35 = 1260
$$

$$
1260 \cdot 34 = 42840
$$

$$
42840 \cdot 33 = 1413720
$$

$$
1413720 \cdot 32 = 45239040
$$

So:

$$
36 \cdot 35 \cdot 34 \cdot 33 \cdot 32 = 45239040
$$

### Counting model:
k-permutation.

### Answer:
$$
45239040
$$

---

### 5.3 Which counting model is used in each case?

- If repetition is allowed, the password is a **sequence with repetition**.
- If repetition is not allowed, the password is a **k-permutation** (ordered selection without repetition).

---

# Final Answers

## 1. Student ID Codes

1. If letters and digits may repeat:

$$
5^2 \cdot 10^3 = 25000
$$

2. If letters may not repeat but digits may repeat:

$$
5 \cdot 4 \cdot 10^3 = 20000
$$

3. If neither letters nor digits may repeat:

$$
(5 \cdot 4)(10 \cdot 9 \cdot 8)=14400
$$

---

## 2. Medal Assignment

1. Number of ways to assign gold, silver, bronze among 12 runners:

$$
P(12,3)=12 \cdot 11 \cdot 10 = 1320
$$

2. If two particular runners must both receive medals:

$$
10 \cdot 3! = 60
$$

---

## 3. Committee Selection

1. Total number of committees:

$$
\binom{10}{4}=210
$$

2. Committees with exactly two women:

$$
\binom{4}{2}\binom{6}{2}=90
$$

3. Committees with at least one woman:

$$
\binom{10}{4}-\binom{6}{4}=195
$$

---

## 4. Circular Seating

1. Number of circular arrangements of 7 people:

$$
6! = 720
$$

2. Number of arrangements where two particular people sit next to each other:

$$
5! \cdot 2! = 240
$$

---

## 5. Passwords

1. If repetition is allowed:

$$
36^5 = 60466176
$$

2. If no character may repeat:

$$
36 \cdot 35 \cdot 34 \cdot 33 \cdot 32 = 45239040
$$

3. Counting models:
- repetition allowed: **sequence with repetition**
- no repetition: **k-permutation**