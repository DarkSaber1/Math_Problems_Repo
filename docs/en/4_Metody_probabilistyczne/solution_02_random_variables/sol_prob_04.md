# Task 4

The density function is

$$
f(x)=
\begin{cases}
\frac{1}{10}e^{-x/10}, & x>0 \\
0, & \text{otherwise}
\end{cases}
$$

So $X$ has exponential distribution with parameter

$$
\lambda = 10
$$

---

## 1. Calculate $P(5 \le X \le 10)$

For a continuous random variable:

$$
P(5 \le X \le 10)=\int_5^{10} \frac{1}{10}e^{-x/10}\,dx
$$

Antiderivative:

$$
\int \frac{1}{10}e^{-x/10}\,dx = -e^{-x/10}
$$

Now compute:

$$
P(5 \le X \le 10)=\left[-e^{-x/10}\right]_5^{10}
$$

$$
P(5 \le X \le 10)= -e^{-1} - (-e^{-0.5})
$$

$$
P(5 \le X \le 10)= e^{-0.5}-e^{-1}
$$

Approximate value:

$$
P(5 \le X \le 10)\approx 0.6065-0.3679=0.2386
$$

---

## 2. Determine the cumulative distribution function

The CDF is

$$
F(x)=P(X\le x)
$$

For $x \le 0$:

$$
F(x)=0
$$

For $x>0$:

$$
F(x)=\int_0^x \frac{1}{10}e^{-t/10}\,dt
$$

$$
F(x)=\left[-e^{-t/10}\right]_0^x
$$

$$
F(x)= -e^{-x/10}-(-1)
$$

$$
F(x)=1-e^{-x/10}
$$

So,

$$
F(x)=
\begin{cases}
0, & x\le 0 \\
1-e^{-x/10}, & x>0
\end{cases}
$$

---

## Final Answer

$$
P(5 \le X \le 10)=e^{-0.5}-e^{-1}\approx 0.2386
$$

and the cumulative distribution function is

$$
F(x)=
\begin{cases}
0, & x\le 0 \\
1-e^{-x/10}, & x>0
\end{cases}
$$