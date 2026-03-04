## Task 8

## Solution

There are 7 pulses in total:
- 4 pulses of type $A$
- 2 pulses of type $B$
- 1 pulse of type $C$

All arrangements are assumed random, so the probability that a given position contains a certain type is proportional to how many of that type remain.

---

### 1) Probability that the first received pulse is $A$

At the first position there are 4 favorable pulses out of 7 total:
\[
P(\text{first is }A)=\frac{4}{7}
\]

---

### 2) Probability that the first received pulse is $A$ or $C$

Favorable pulses: 4 of type $A$ and 1 of type $C$, so 5 favorable out of 7:
\[
P(\text{first is }A \text{ or } C)=\frac{4+1}{7}=\frac{5}{7}
\]

---

### 3) Probability that the first two pulses are $A$ and $C$ in that order

We use sequential probability (without replacement):

- First pulse is $A$: $\frac{4}{7}$
- After one $A$ is used, 6 pulses remain and still 1 pulse of type $C$ remains, so:
  \[
  P(\text{second is }C \mid \text{first is }A)=\frac{1}{6}
  \]

Multiply:
\[
P(A\text{ then }C)=\frac{4}{7}\cdot \frac{1}{6}=\frac{4}{42}=\frac{2}{21}
\]

**Answer:** $P(\text{first two are }A \text{ then } C)=\frac{2}{21}$