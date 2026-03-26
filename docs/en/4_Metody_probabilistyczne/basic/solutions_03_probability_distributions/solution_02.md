## Task 2

Let $\Omega$ be a finite sample space with equally likely elementary outcomes.

Let $A$ and $B$ be two events.

We use basic properties of probability and set algebra.

---

### 1) Probability of the complement of an event

The complement of event $A$, denoted $A^c$, contains all outcomes not in $A$.

Since $A$ and $A^c$ together form the entire sample space:

P(A) + P(A^c) = 1

Therefore:

P(A^c) = 1 - P(A)

---

### 2) Probability of the union of two events

To find the probability that at least one of the events $A$ or $B$ occurs, we use:

P(A ∪ B) = P(A) + P(B) - P(A ∩ B)

We subtract $P(A ∩ B)$ because it is counted twice when adding $P(A)$ and $P(B)$.

---

### 3) If A and B are disjoint events

If $A ∩ B = ∅$, then the events cannot occur simultaneously.

In this case:

P(A ∪ B) = P(A) + P(B)

---

### 4) Probability of difference of events

The event $A \ B$ means that event $A$ occurs but $B$ does not.

This can be written as:

A \ B = A ∩ B^c

So:

P(A \ B) = P(A ∩ B^c)

---

### 5) Probability of intersection using conditional probability

If we know conditional probability, we can write:

P(A ∩ B) = P(A) · P(B | A)

or equivalently:

P(A ∩ B) = P(B) · P(A | B)