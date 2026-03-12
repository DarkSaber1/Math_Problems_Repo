# Task 7

The joint distribution table of \((X,Y)\) is:

| \(Y \backslash X\) | 1 | 2 | 3 |
|---|---:|---:|---:|
| **2** | 0.1 | 0.2 | 0.3 |
| **4** | 0.1 | 0.1 | 0.2 |

We need the **cumulative distribution function of the marginal distribution of \(Y\)**.

---

# 1. Find the marginal distribution of \(Y\)

Add probabilities across each row.

For \(Y=2\):

$$
P(Y=2)=0.1+0.2+0.3=0.6
$$

For \(Y=4\):

$$
P(Y=4)=0.1+0.1+0.2=0.4
$$

So the marginal distribution of \(Y\) is:

| \(y\) | 2 | 4 |
|---|---:|---:|
| \(P(Y=y)\) | 0.6 | 0.4 |

---

# 2. Determine the CDF of \(Y\)

The cumulative distribution function is

$$
F_Y(y)=P(Y \le y)
$$

Since \(Y\) takes only values \(2\) and \(4\):

$$
F_Y(y)=
\begin{cases}
0, & y<2 \\
0.6, & 2 \le y<4 \\
1, & y \ge 4
\end{cases}
$$

---

# Final Answer

The marginal distribution of \(Y\) is:

| \(y\) | 2 | 4 |
|---|---:|---:|
| \(P(Y=y)\) | 0.6 | 0.4 |

The cumulative distribution function is:

$$
F_Y(y)=
\begin{cases}
0, & y<2 \\
0.6, & 2 \le y<4 \\
1, & y \ge 4
\end{cases}
$$