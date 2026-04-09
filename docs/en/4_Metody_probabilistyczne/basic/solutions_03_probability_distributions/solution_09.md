# Task 9 — Poisson Model

A customer service center receives on average:

\[
\lambda = 5
\]

requests per hour.

Let \(X\) denote the number of requests received during one hour.

Then \(X\) has a **Poisson distribution**:

\[
X \sim \mathrm{Poisson}(5)
\]

The probability mass function of the Poisson distribution is:

\[
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}, \quad k=0,1,2,\dots
\]

---

## 1. Probability that exactly 3 requests arrive in one hour

We substitute:

- \(\lambda = 5\),
- \(k = 3\).

So:

\[
P(X=3)=\frac{e^{-5}5^3}{3!}
\]

Now calculate step by step:

\[
5^3=125
\]

\[
3!=6
\]

Thus:

\[
P(X=3)=\frac{e^{-5}\cdot 125}{6}
\]

Using the approximation:

\[
e^{-5}\approx 0.006737947
\]

we get:

\[
P(X=3)\approx \frac{0.006737947 \cdot 125}{6}
\]

\[
P(X=3)\approx \frac{0.842243375}{6}
\]

\[
P(X=3)\approx 0.14037
\]

So the probability that exactly 3 requests arrive is:

\[
\boxed{P(X=3)\approx 0.14037}
\]

---

## 2. Probability that at least one request arrives in one hour

The event “at least one request” means:

\[
X \geq 1
\]

It is easier to use the complement:

\[
P(X\geq1)=1-P(X=0)
\]

Now calculate \(P(X=0)\):

\[
P(X=0)=\frac{e^{-5}5^0}{0!}
\]

Since:

\[
5^0=1
\quad \text{and} \quad
0!=1
\]

we obtain:

\[
P(X=0)=e^{-5}
\]

\[
P(X=0)\approx 0.006737947
\]

Therefore:

\[
P(X\geq1)=1-0.006737947
\]

\[
P(X\geq1)\approx 0.99326
\]

So the probability that at least one request arrives is:

\[
\boxed{P(X\geq1)\approx 0.99326}
\]

---

## Final answers

\[
\boxed{P(X=3)\approx 0.14037}
\]

\[
\boxed{P(X\geq1)\approx 0.99326}
\]

---

## Final conclusion

This task uses the **Poisson distribution**, because:

- we count the number of events in a fixed time interval,
- the average number of events per hour is known,
- the random variable can take values \(0,1,2,\dots\),
- the model is determined by the parameter \(\lambda = 5\).