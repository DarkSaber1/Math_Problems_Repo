# Task 8 — Geometric Model

The probability of an error in program compilation is:

\[
p = 0.1
\]

Therefore, the probability that a compilation is successful (no error) is:

\[
1-p = 0.9
\]

The programmer performs consecutive compilations until the **first error** occurs.

Let \(X\) denote the number of the compilation on which the first error appears.

Then \(X\) has a **geometric distribution**:

\[
X \sim \mathrm{Geom}(0.1)
\]

---

## 1. Probability that the first error appears on the 4th compilation

For a geometric distribution, the probability that the first success occurs on the \(k\)-th trial is:

\[
P(X=k)=(1-p)^{k-1}p
\]

Here:

- \(p=0.1\),
- \(k=4\).

So:

\[
P(X=4)=(0.9)^3 \cdot 0.1
\]

Now calculate:

\[
(0.9)^3 = 0.729
\]

Thus:

\[
P(X=4)=0.729 \cdot 0.1 = 0.0729
\]

So the probability that the first error appears on the 4th compilation is:

\[
\boxed{P(X=4)=0.0729}
\]

---

## 2. Probability that the first error appears no later than the 3rd compilation

The phrase **“no later than the 3rd compilation”** means:

\[
P(X \leq 3)
\]

This includes the following cases:

- the first error appears on the 1st compilation,
- the first error appears on the 2nd compilation,
- the first error appears on the 3rd compilation.

It is easiest to use the complement:

\[
P(X \leq 3)=1-P(X>3)
\]

The event \(X>3\) means that **there is no error in the first 3 compilations**.

The probability of no error in one compilation is \(0.9\), so:

\[
P(X>3)=(0.9)^3
\]

\[
P(X>3)=0.729
\]

Therefore:

\[
P(X\leq3)=1-0.729
\]

\[
P(X\leq3)=0.271
\]

So the probability that the first error appears no later than the 3rd compilation is:

\[
\boxed{P(X\leq3)=0.271}
\]

---

## Final answers

\[
\boxed{P(X=4)=0.0729}
\]

\[
\boxed{P(X\leq3)=0.271}
\]

---

## Final conclusion

This task uses the **geometric distribution**, because:

- each compilation has two possible outcomes: error or no error,
- the compilations are independent,
- the probability of error is constant and equals \(0.1\),
- we are interested in the trial on which the **first error** occurs.