## Task 3 — Geometric Model (Waiting for the First Event)

In a printing house, each printed page may contain a printing error with probability `p`.

We assume that:
- pages are independent,
- the probability of an error is the same for every page.

We observe consecutive pages until the **first error** appears.

This is a **geometric model**, because:
- each trial has two possible outcomes,
- the trials are independent,
- the probability of success is constant,
- we are interested in the trial on which the **first success** occurs.

---

### 1) Description of the random experiment

The experiment consists of checking printed pages one by one.

For each page, there are two possibilities:
- the page contains an error,
- the page does not contain an error.

We continue this process until the **first page with an error** is observed.

So the outcome of the experiment is not just whether an error appears, but **when the first error appears**.

---

### 2) Sample space Omega

Let:
- E = "page contains an error"
- N = "page does not contain an error"

Since we stop at the first error, every elementary outcome has the form:

- E
- N E
- N N E
- N N N E
- ...

So the sample space is:

Omega = {E, NE, NNE, NNNE, NNNNE, ...}

In general, the outcome means:

- the first `k - 1` pages have no error,
- the `k`-th page contains the first error.

---

### 3) Probability distribution

Define the random variable:

X = the number of the page on which the first error appears

Then X can take the values:

X = 1, 2, 3, 4, ...

To have `X = k`, the following must happen:
- the first `k - 1` pages must have no error,
- the `k`-th page must contain an error.

The probability of:
- no error on one page is `1 - p`,
- error on one page is `p`.

Because the pages are independent, we multiply these probabilities:

P(X = k) = (1 - p)^(k - 1) * p,   for k = 1, 2, 3, ...

This is the probability mass function of the **geometric distribution**.

---

### 4) What is considered a success?

In this model, a **success** means:

"a page contains a printing error"

So:
- success = page with an error
- failure = page without an error

The geometric model counts how many trials are needed until the **first success**, that is, until the **first error** appears.

---

### Final conclusion

This is a geometric distribution with:
- success probability: `p`
- random variable: `X` = trial number of the first success

Its distribution is:

P(X = k) = (1 - p)^(k - 1) * p,   for k = 1, 2, 3, ...