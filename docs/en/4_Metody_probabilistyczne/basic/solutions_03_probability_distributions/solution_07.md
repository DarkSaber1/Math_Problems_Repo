# Task 7 — Hypergeometric Model

A box contains:

- **12 working light bulbs**,
- **3 defective light bulbs**.

So the total number of bulbs is:

\[
15
\]

We draw:

\[
5
\]

bulbs **without replacement**.

Let \(X\) denote the number of defective bulbs in the sample.

We want to calculate the probability that the sample contains **exactly 2 defective bulbs**.

---

## 1. Distribution used

Because the bulbs are drawn **without replacement** from a finite population containing two types of elements (working and defective), this is a **hypergeometric distribution**.

The formula is:

\[
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
\]

where:

- \(N=15\) — total number of bulbs,
- \(K=3\) — number of defective bulbs,
- \(n=5\) — number of drawn bulbs,
- \(k=2\) — number of defective bulbs in the sample.

---

## 2. Apply the formula

Substitute the values into the formula:

\[
P(X=2)=\frac{\binom{3}{2}\binom{12}{3}}{\binom{15}{5}}
\]

---

## 3. Calculate each binomial coefficient

First:

\[
\binom{3}{2}=3
\]

Next:

\[
\binom{12}{3}=\frac{12\cdot 11\cdot 10}{3\cdot 2\cdot 1}=220
\]

And:

\[
\binom{15}{5}=3003
\]

So:

\[
P(X=2)=\frac{3\cdot 220}{3003}
\]

\[
P(X=2)=\frac{660}{3003}
\]

\[
P(X=2)\approx 0.21978
\]

---

## Final answer

\[
\boxed{P(X=2)=\frac{660}{3003}\approx 0.21978}
\]

---

## Final conclusion

This task uses the **hypergeometric distribution**, because:

- we draw elements from a finite set,
- the sample is taken **without replacement**,
- there are two categories of bulbs: working and defective,
- we count how many defective bulbs appear in the sample.