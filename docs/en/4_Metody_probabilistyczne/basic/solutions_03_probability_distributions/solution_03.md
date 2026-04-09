# Task 3 — Geometric Model (Waiting for the First Event)

## 1. Description of the random experiment

In a printing house, each printed page may contain a **printing error** with probability \(p\).

We assume that:

- each page is checked independently,
- the probability of an error is the same for every page,
- we continue observing consecutive pages until the **first error** appears.

So the experiment consists of counting how many pages are observed before the first page with a printing error is obtained.

This is a typical **geometric model**, because we repeat independent trials until the first success occurs.

---

## 2. Sample space \( \Omega \)

Let the result of the experiment be the number of the page on which the **first printing error** appears.

Then the sample space is:

\[
\Omega = \{1,2,3,4,\dots\}
\]

### Interpretation
- \(1\) means that the first page already contains an error,
- \(2\) means that the first page has no error, but the second page has an error,
- \(3\) means that the first two pages have no error, and the third page has an error,
- and so on.

Thus, the sample space is infinite.

---

## 3. Probability distribution

Let \(X\) be the random variable denoting the number of the page on which the first error appears.

Then \(X\) has a **geometric distribution** with parameter \(p\), and its probability distribution is:

\[
P(X=k) = (1-p)^{k-1}p, \quad k=1,2,3,\dots
\]

### Explanation of the formula

To obtain the first error on the \(k\)-th page:

- the first \(k-1\) pages must contain **no error**,
- the \(k\)-th page must contain **an error**.

The probability of no error on one page is:

\[
1-p
\]

So the probability of no error on the first \(k-1\) pages is:

\[
(1-p)^{k-1}
\]

Then we multiply by the probability that the \(k\)-th page contains an error, which is \(p\).

Therefore:

\[
P(X=k) = (1-p)^{k-1}p
\]

---

## 4. Definition of success

In this model, a **success** is defined as:

> **the appearance of a printing error on a page**

So we repeat the observations until the first success occurs, where success means detecting the first printing error.

---

## Final conclusion

Task 3 is an example of a **geometric model**, because:

- each trial has two possible outcomes: **error** or **no error**,
- the trials are independent,
- the probability of success is constant and equal to \(p\),
- we are interested in the trial on which the **first success** occurs.