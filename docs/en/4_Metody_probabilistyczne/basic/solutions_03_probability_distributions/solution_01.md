# Task 1 — Binomial Model (Quality Control)

## 1. Description of the random experiment

We inspect **3 consecutive screws** produced in the factory.  
Each inspected screw can have one of two possible outcomes:

- **G** — the screw is good,
- **D** — the screw is defective.

We assume that:

- the inspections are **independent**,
- the probability that a screw is defective is the same in each inspection and equals **p**,
- therefore, the probability that a screw is good equals **1 - p**.

So this experiment is a sequence of **3 independent Bernoulli trials**.

---

## 2. Sample space \( \Omega \)

Since each of the 3 screws can be either good or defective, the sample space consists of all possible sequences of length 3:

\[
\Omega = \{GGG, GGD, GDG, DGG, GDD, DGD, DDG, DDD\}
\]

Each element of \( \Omega \) describes the results of the three consecutive inspections.

---

## 3. Probabilities of the elements of the sample space

Because the inspections are independent, the probability of each elementary outcome is the product of the probabilities of its components.

- \[
P(GGG) = (1-p)^3
\]

- \[
P(GGD) = (1-p)^2 p
\]

- \[
P(GDG) = (1-p)^2 p
\]

- \[
P(DGG) = p(1-p)^2
\]

- \[
P(GDD) = (1-p)p^2
\]

- \[
P(DGD) = p(1-p)p = p^2(1-p)
\]

- \[
P(DDG) = p^2(1-p)
\]

- \[
P(DDD) = p^3
\]

These probabilities follow directly from the multiplication rule for independent events.

---

## 4. Definition of success

In this model, a **success** is defined as:

> **the event that an inspected screw is defective**

Therefore, if we define the random variable \(X\) as the **number of defective screws among the 3 inspected screws**, then:

\[
X \sim \mathrm{Bin}(3, p)
\]

That means \(X\) has a **binomial distribution** with parameters:

- \(n = 3\) — number of trials,
- \(p\) — probability of success in each trial.

---

## Final conclusion

Task 1 is an example of a **binomial model**, because:

- there is a fixed number of trials (**3 inspections**),
- each trial has only two outcomes (**good / defective**),
- the trials are independent,
- the probability of success (**defective screw**) is constant and equal to \(p\).