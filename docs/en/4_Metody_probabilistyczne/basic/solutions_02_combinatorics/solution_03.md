# Task 3 — Permutations with Repeated Elements

In this task we count arrangements of words that contain repeated letters.

If all letters were different, the number of arrangements of \(n\) letters would be

$$
n!
$$

However, when some letters are repeated, many of these arrangements look identical.  
To correct for this overcounting, we use the formula for **permutations with repeated elements**:

$$
\frac{n!}{n_1!n_2!\dots n_r!}
$$

where:

- \(n\) = total number of letters,
- \(n_1, n_2, \dots, n_r\) = multiplicities of repeated letters.

We now solve each problem step by step.

---

## 1. How many distinct arrangements of the word MISSISSIPPI are possible?

First count the letters in the word:

\[
\text{MISSISSIPPI}
\]

The word has 11 letters in total.

Now count how many times each letter appears:

- \(M = 1\)
- \(I = 4\)
- \(S = 4\)
- \(P = 2\)

If all 11 letters were different, the number of arrangements would be

$$
11!
$$

But the 4 letters \(I\) are identical, so dividing by \(4!\) removes overcounting from swapping the I's.

Similarly:

- divide by \(4!\) for the identical S's,
- divide by \(2!\) for the identical P's.

So the correct number of distinct arrangements is

$$
\frac{11!}{4!4!2!}
$$

Now compute:

$$
11! = 39916800
$$

$$
4! = 24, \qquad 2! = 2
$$

So the denominator is

$$
4! \cdot 4! \cdot 2! = 24 \cdot 24 \cdot 2 = 1152
$$

Therefore:

$$
\frac{39916800}{1152} = 34650
$$

### Answer:
$$
34650
$$

---

## 2. How many distinct arrangements of STATISTICS are possible?

Now consider the word

\[
\text{STATISTICS}
\]

First count the total number of letters.

The word has 10 letters.

Now count repeated letters:

- \(S = 3\)
- \(T = 3\)
- \(A = 1\)
- \(I = 2\)
- \(C = 1\)

If all 10 letters were different, there would be

$$
10!
$$

arrangements.

But since some letters repeat, we divide by the factorials of the repeated multiplicities:

- divide by \(3!\) for the S's,
- divide by \(3!\) for the T's,
- divide by \(2!\) for the I's.

So the number of distinct arrangements is

$$
\frac{10!}{3!3!2!}
$$

Now compute:

$$
10! = 3628800
$$

$$
3! = 6, \qquad 2! = 2
$$

So the denominator is

$$
3! \cdot 3! \cdot 2! = 6 \cdot 6 \cdot 2 = 72
$$

Therefore:

$$
\frac{3628800}{72} = 50400
$$

### Answer:
$$
50400
$$

---

## 3. How many of the arrangements of STATISTICS start with the letter S?

We again work with the word

\[
\text{STATISTICS}
\]

but now we impose the condition that the arrangement must begin with the letter \(S\).

### Step 1: Fix the first letter

We place one \(S\) in the first position.

So now we only need to arrange the remaining 9 letters.

Originally the word had:

- \(S = 3\)
- \(T = 3\)
- \(A = 1\)
- \(I = 2\)
- \(C = 1\)

After fixing one \(S\) at the beginning, the remaining letters are:

- \(S = 2\)
- \(T = 3\)
- \(A = 1\)
- \(I = 2\)
- \(C = 1\)

That is 9 letters total.

### Step 2: Count the distinct arrangements of the remaining letters

If all 9 remaining letters were different, there would be

$$
9!
$$

arrangements.

But we must divide for repeated letters:

- divide by \(2!\) for the remaining S's,
- divide by \(3!\) for the T's,
- divide by \(2!\) for the I's.

Thus the number of valid arrangements is

$$
\frac{9!}{2!3!2!}
$$

Now compute:

$$
9! = 362880
$$

$$
2! = 2, \qquad 3! = 6
$$

So the denominator is

$$
2! \cdot 3! \cdot 2! = 2 \cdot 6 \cdot 2 = 24
$$

Therefore:

$$
\frac{362880}{24} = 15120
$$

### Answer:
$$
15120
$$

---

# Final Answers

1. Distinct arrangements of **MISSISSIPPI**:

$$
\frac{11!}{4!4!2!} = 34650
$$

2. Distinct arrangements of **STATISTICS**:

$$
\frac{10!}{3!3!2!} = 50400
$$

3. Arrangements of **STATISTICS** that start with \(S\):

$$
\frac{9!}{2!3!2!} = 15120
$$