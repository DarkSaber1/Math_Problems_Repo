# Task 6 — Binomial Model

The probability of producing a defective part is:

\[
p = 0.04
\]

The inspector checks:

\[
n = 10
\]

independent parts.

Let \(X\) denote the number of defective parts among the 10 inspected ones.  
Then \(X\) has a binomial distribution:

\[
X \sim \mathrm{Bin}(10, 0.04)
\]

---

## 1. Probability that exactly 2 parts are defective

For a binomial distribution, the probability of exactly \(k\) successes is given by:

\[
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
\]

Here:

- \(n=10\),
- \(k=2\),
- \(p=0.04\),
- \(1-p=0.96\).

So:

\[
P(X=2)=\binom{10}{2}(0.04)^2(0.96)^8
\]

Now calculate step by step:

\[
\binom{10}{2}=\frac{10!}{2!8!}=45
\]

\[
(0.04)^2=0.0016
\]

\[
(0.96)^8 \approx 0.72138957898
\]

Therefore:

\[
P(X=2)=45 \cdot 0.0016 \cdot 0.72138957898
\]

\[
P(X=2)\approx 0.05194
\]

So the probability that exactly 2 parts are defective is:

\[
\boxed{P(X=2)\approx 0.05194}
\]

---

## 2. Probability that at least one part is defective

The event “at least one defective part” means:

\[
X \geq 1
\]

It is easier to use the complement:

\[
P(X \geq 1)=1-P(X=0)
\]

Now calculate \(P(X=0)\):

\[
P(X=0)=\binom{10}{0}(0.04)^0(0.96)^{10}
\]

Since:

\[
\binom{10}{0}=1
\quad \text{and} \quad
(0.04)^0=1
\]

we get:

\[
P(X=0)=(0.96)^{10}
\]

\[
(0.96)^{10}\approx 0.66483263599
\]

Thus:

\[
P(X\geq1)=1-0.66483263599
\]

\[
P(X\geq1)\approx 0.33517
\]

So the probability that at least one part is defective is:

\[
\boxed{P(X\geq1)\approx 0.33517}
\]

---

## Final answers

\[
\boxed{P(X=2)\approx 0.05194}
\]

\[
\boxed{P(X\geq1)\approx 0.33517}
\]

---

## Final conclusion

This task uses the **binomial distribution**, because:

- there is a fixed number of trials (\(10\)),
- each trial has two outcomes: defective or not defective,
- the trials are independent,
- the probability of a defective part is constant and equals \(0.04\).