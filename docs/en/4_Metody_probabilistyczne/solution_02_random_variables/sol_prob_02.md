# Task 2

The ratio of grades is:

$$
1 : 3 : 4 : 2
$$

Corresponding grades:

| Grade | Meaning |
|------|------|
|2|Failing|
|3|Satisfactory|
|4|Good|
|5|Very Good|

Total parts:

$$
1+3+4+2=10
$$

---

# 1. Probability Mass Function (PMF)

Convert the ratio to probabilities.

| $x$ (grade) | 2 | 3 | 4 | 5 |
|-------------|---|---|---|---|
| $P(X=x)$ | 0.2 | 0.4 | 0.3 | 0.1 |

Where

- $P(X=2)=0.2$
- $P(X=3)=0.4$
- $P(X=4)=0.3$
- $P(X=5)=0.1$

Check:

$$
0.2+0.4+0.3+0.1=1
$$

---

# 2. Cumulative Distribution Function (CDF)

The cumulative distribution function is

$$
F(x)=P(X\leq x)
$$

| Interval | $F(x)$ |
|---------|--------|
| $x < 2$ | 0 |
| $2 \le x < 3$ | 0.2 |
| $3 \le x < 4$ | 0.6 |
| $4 \le x < 5$ | 0.9 |
| $x \ge 5$ | 1 |

---

# 3. Probability $P(X<3.5)$

Values smaller than **3.5**:

- 2
- 3

Therefore

$$
P(X<3.5)=P(X=2)+P(X=3)
$$

$$
P(X<3.5)=0.2+0.4
$$

$$
P(X<3.5)=0.6
$$

---

# Final Result

| Grade | Probability |
|------|-------------|
|2|0.2|
|3|0.4|
|4|0.3|
|5|0.1|

CDF defined by:

$$
F(x)=
\begin{cases}
0 & x<2 \\
0.2 & 2\le x<3 \\
0.6 & 3\le x<4 \\
0.9 & 4\le x<5 \\
1 & x\ge5
\end{cases}
$$

Required probability:

$$
P(X<3.5)=0.6
$$