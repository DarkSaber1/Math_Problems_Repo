# Task 9

The function is

$$
f(x,y)=
\begin{cases}
cxy, & 0 \le x \le 2,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$

To be a valid **joint density**, it must satisfy

$$
\int_{0}^{2}\int_{0}^{1} f(x,y)\,dy\,dx = 1
$$

---

# 1. Compute the integral

Substitute \(f(x,y)=cxy\):

$$
\int_{0}^{2}\int_{0}^{1} cxy\,dy\,dx = 1
$$

First integrate with respect to \(y\):

$$
\int_{0}^{1} cxy\,dy = cx \int_{0}^{1} y\,dy
$$

$$
= cx \left[\frac{y^2}{2}\right]_{0}^{1}
$$

$$
= cx \cdot \frac{1}{2}
$$

---

# 2. Integrate with respect to \(x\)

$$
\int_{0}^{2} \frac{cx}{2}\,dx
$$

$$
= \frac{c}{2} \int_{0}^{2} x\,dx
$$

$$
= \frac{c}{2}\left[\frac{x^2}{2}\right]_{0}^{2}
$$

$$
= \frac{c}{2}\cdot 2
$$

$$
= c
$$

---

# 3. Solve for \(c\)

Since the total probability must equal 1:

$$
c=1
$$

---

# Final Answer

The constant is

$$
c = 1
$$

Therefore the density becomes

$$
f(x,y)=
\begin{cases}
xy, & 0 \le x \le 2,\; 0 \le y \le 1 \\
0, & \text{otherwise}
\end{cases}
$$