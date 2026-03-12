# Task 5

We want the function

$$
F(x)=A+B\arctan x
\qquad \text{for } -\infty < x < \infty
$$

to be a cumulative distribution function (CDF).

A CDF must satisfy:

$$
\lim_{x\to -\infty} F(x)=0
\qquad\text{and}\qquad
\lim_{x\to \infty} F(x)=1
$$

---

# 1. Find constants \(A\) and \(B\)

We know:

$$
\lim_{x\to -\infty} \arctan x = -\frac{\pi}{2}
$$

$$
\lim_{x\to \infty} \arctan x = \frac{\pi}{2}
$$

So:

## From \(F(-\infty)=0\)

$$
A + B\left(-\frac{\pi}{2}\right)=0
$$

$$
A-\frac{B\pi}{2}=0
$$

## From \(F(\infty)=1\)

$$
A + B\left(\frac{\pi}{2}\right)=1
$$

$$
A+\frac{B\pi}{2}=1
$$

---

# 2. Solve the system

Add the two equations:

$$
\left(A-\frac{B\pi}{2}\right)+\left(A+\frac{B\pi}{2}\right)=0+1
$$

$$
2A=1
$$

$$
A=\frac{1}{2}
$$

Substitute into

$$
A+\frac{B\pi}{2}=1
$$

$$
\frac{1}{2}+\frac{B\pi}{2}=1
$$

$$
\frac{B\pi}{2}=\frac{1}{2}
$$

$$
B=\frac{1}{\pi}
$$

---

# 3. Final form of the CDF

$$
F(x)=\frac{1}{2}+\frac{1}{\pi}\arctan x
$$

---

# 4. Find the density

For a continuous random variable,

$$
f(x)=F'(x)
$$

Differentiate:

$$
f(x)=\frac{1}{\pi}\cdot \frac{1}{1+x^2}
$$

So the density is

$$
f(x)=\frac{1}{\pi(1+x^2)}
\qquad \text{for } -\infty < x < \infty
$$

---

# Final Answer

$$
A=\frac{1}{2}, \qquad B=\frac{1}{\pi}
$$

Therefore,

$$
F(x)=\frac{1}{2}+\frac{1}{\pi}\arctan x
$$

and the density is

$$
f(x)=\frac{1}{\pi(1+x^2)}
$$