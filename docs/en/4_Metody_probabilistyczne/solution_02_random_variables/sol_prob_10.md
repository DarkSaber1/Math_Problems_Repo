# Task 10

From Task 9, the joint density is

$$
f(x,y)=
\begin{cases}
xy, & 0 \le x \le 2,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

We need to find the marginal densities \(f_1(x)\) and \(f_2(y)\), then check independence.

---

# 1. Marginal density of \(X\)

By definition,

$$
f_1(x)=\int_{0}^{1} f(x,y)\,dy
$$

Substitute \(f(x,y)=xy\):

$$
f_1(x)=\int_{0}^{1} xy\,dy
$$

$$
= x\int_{0}^{1} y\,dy
$$

$$
= x\left[\frac{y^2}{2}\right]_{0}^{1}
$$

$$
= \frac{x}{2}
\qquad \text{for } 0 \le x \le 2
$$

So,

$$
f_1(x)=
\begin{cases}
\frac{x}{2}, & 0 \le x \le 2 \\
0, & \text{otherwise}
\end{cases}
$$

---

# 2. Marginal density of \(Y\)

By definition,

$$
f_2(y)=\int_{0}^{2} f(x,y)\,dx
$$

Substitute \(f(x,y)=xy\):

$$
f_2(y)=\int_{0}^{2} xy\,dx
$$

$$
= y\int_{0}^{2} x\,dx
$$

$$
= y\left[\frac{x^2}{2}\right]_{0}^{2}
$$

$$
= 2y
\qquad \text{for } 0 \le y \le 1
$$

So,

$$
f_2(y)=
\begin{cases}
2y, & 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

---

# 3. Check independence

Two variables are independent if

$$
f(x,y)=f_1(x)\,f_2(y)
$$

Now calculate:

$$
f_1(x)f_2(y)=\frac{x}{2}\cdot 2y
$$

$$
f_1(x)f_2(y)=xy
$$

This is exactly the same as \(f(x,y)\) on the region

$$
0 \le x \le 2,\quad 0 \le y \le 1
$$

Therefore, \(X\) and \(Y\) are independent.

---

# Final Answer

The marginal densities are

$$
f_1(x)=
\begin{cases}
\frac{x}{2}, & 0 \le x \le 2 \\
0, & \text{otherwise}
\end{cases}
$$

and

$$
f_2(y)=
\begin{cases}
2y, & 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

Since

$$
f_1(x)f_2(y)=xy=f(x,y)
$$

the variables \(X\) and \(Y\) are **independent**.