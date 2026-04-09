# Task 10 — Multinomial Model

A box contains candies of three flavors:

- **strawberry** — \(40\%\)
- **lemon** — \(35\%\)
- **mint** — \(25\%\)

We perform **6 independent selections with replacement**.

We want to calculate the probability of obtaining:

- **3 strawberry candies**
- **2 lemon candies**
- **1 mint candy**

---

## 1. Distribution used

Since:

- there is a fixed number of trials, \(n=6\),
- each trial can end in one of three possible categories,
- the probabilities remain constant in each selection,
- the selections are independent because they are made **with replacement**,

this is a **multinomial distribution**.

Let:

- \(X_1\) = number of strawberry candies,
- \(X_2\) = number of lemon candies,
- \(X_3\) = number of mint candies.

Then:

\[
X_1 + X_2 + X_3 = 6
\]

and:

\[
(X_1, X_2, X_3) \sim \mathrm{Multinomial}(6; 0.40, 0.35, 0.25)
\]

---

## 2. Formula

For the multinomial distribution, the probability is given by:

\[
P(X_1=x_1, X_2=x_2, X_3=x_3)
=
\frac{n!}{x_1!x_2!x_3!}\, p_1^{x_1} p_2^{x_2} p_3^{x_3}
\]

In this task:

\[
n=6,\quad x_1=3,\quad x_2=2,\quad x_3=1
\]

\[
p_1=0.40,\quad p_2=0.35,\quad p_3=0.25
\]

So:

\[
P(X_1=3, X_2=2, X_3=1)
=
\frac{6!}{3!2!1!}(0.40)^3(0.35)^2(0.25)^1
\]

---

## 3. Step-by-step calculation

First, calculate the multinomial coefficient:

\[
\frac{6!}{3!2!1!}
=
\frac{720}{6\cdot2\cdot1}
=
\frac{720}{12}
=
60
\]

Now calculate the powers:

\[
(0.40)^3 = 0.064
\]

\[
(0.35)^2 = 0.1225
\]

\[
(0.25)^1 = 0.25
\]

Now multiply them:

\[
0.064 \cdot 0.1225 = 0.00784
\]

\[
0.00784 \cdot 0.25 = 0.00196
\]

Finally:

\[
60 \cdot 0.00196 = 0.1176
\]

Therefore:

\[
P(X_1=3, X_2=2, X_3=1) = 0.1176
\]

---

## Final answer

\[
\boxed{P(3\text{ strawberry},\,2\text{ lemon},\,1\text{ mint}) = 0.1176}
\]

---

## Final conclusion

This task is solved using the **multinomial distribution**, because:

- there are **6 independent selections**,
- each selection has **3 possible outcomes**,
- the probabilities are constant:
  - strawberry: \(0.40\)
  - lemon: \(0.35\)
  - mint: \(0.25\),
- we calculate the probability of one specific combination of numbers of candies.