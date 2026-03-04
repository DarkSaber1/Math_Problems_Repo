## Task 4

## Solution

Two elements $a_1$ and $a_2$ are connected **in parallel**.  
Let $A_i$ denote the event that element $a_i$ remains functional for at least time $t$.

### Step 1: Express the event of continuous current flow

In a parallel connection, the system will conduct current as long as **at least one** element works.

So the event of continuous current flow for at least time $t$ is:

$A = A_1 \cup A_2$

### Step 2: Compute its probability

We use the union formula:

$P(A_1 \cup A_2) = P(A_1) + P(A_2) - P(A_1 \cap A_2)$

Given:
- $P(A_1) = p$
- $P(A_2) = p$
- $P(A_1 \cap A_2) = p^2$

Substitute:

$P(A) = p + p - p^2 = 2p - p^2$

### Final answer

$P(\text{continuous current flow for at least time } t) = 2p - p^2$