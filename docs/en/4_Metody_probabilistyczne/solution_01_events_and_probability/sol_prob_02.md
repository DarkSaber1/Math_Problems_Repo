## Task 2

## Solution

Let $A_i$ denote the event: "element $a_i$ is functional at time $t$".

### Step 1: Describe the condition for the parallel block to work

In a parallel connection, current can flow through the block if **at least one of the elements works**.

So the event that the parallel block works is:

$A_2 \cup A_3$

### Step 2: Combine with the series element

In a series connection, current flows only if **all series parts are functional**.

So we need:
- $a_1$ works (event $A_1$)
- the parallel block works (event $A_2 \cup A_3$)

Therefore, the event $A$ ("current flow will not be interrupted in time interval $t$") is:

$A = A_1 \cap (A_2 \cup A_3)$
