## Task 5

## Solutions

We are given:
- $P(A)=0.6$ where $A$ = "water volume is in $\langle 125,250\rangle$"
- $P(B)=0.7$ where $B$ = "water volume is in $(200,300\rangle$"
- $P(A \cup B)=0.8$

We compute the requested probabilities using basic rules.

---

### 1) $P(A')$ (complement of $A$)

The complement rule says that an event and its complement cover the whole sample space:
\[
P(A) + P(A') = 1
\]

So:
\[
P(A') = 1 - P(A) = 1 - 0.6 = 0.4
\]

---

### 2) $P(A \cap B)$ (intersection)

We use the inclusion–exclusion formula:
\[
P(A \cup B) = P(A) + P(B) - P(A \cap B)
\]

Solve for $P(A \cap B)$:
\[
P(A \cap B) = P(A) + P(B) - P(A \cup B)
\]
\[
P(A \cap B) = 0.6 + 0.7 - 0.8 = 0.5
\]

---

### 3) $P(A' \cap B')$ (neither interval)

“Not in $A$ and not in $B$” means the complement of “in $A$ or in $B$”.
By De Morgan's law:
\[
A' \cap B' = (A \cup B)'
\]

Therefore:
\[
P(A' \cap B') = 1 - P(A \cup B) = 1 - 0.8 = 0.2
\]

---

### Final answers

- $P(A') = 0.4$
- $P(A \cap B) = 0.5$
- $P(A' \cap B') = 0.2$