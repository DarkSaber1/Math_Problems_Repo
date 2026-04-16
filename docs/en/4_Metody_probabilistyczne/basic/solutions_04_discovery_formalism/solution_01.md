# Problem 1 — Coin × Coin

We consider an experiment consisting of **two coin tosses**.

Each outcome is a pair:
- the first toss (row),
- the second toss (column).

The sample space is:

\[
\Omega = \{HH, HT, TH, TT\}
\]

Representation:
      H   T
H     .   .
T     .   .

  
## Part A — marking events

### 1. exactly one head

Exactly one head means that one toss is H and the other is T.

Possible outcomes:
\[
HT,\ TH
\]
  H   T

  
### 2. both tosses are the same

Both tosses are the same means:
\[
HH,\ TT
\]
  H   T

  
### 3. at least one head

At least one head means all outcomes except TT:

\[
HH,\ HT,\ TH
\]
 H   T

 
### 4. the first toss is tails

The first toss corresponds to the row.

So we select all outcomes where the first toss is T:
\[
TH,\ TT
\]
 H   T


### 5. the second toss is heads

The second toss corresponds to the column.

So we select all outcomes where the second toss is H:
\[
HH,\ TH
\]
  H   T

  
## Part B — interpretation

### Case 1

In this case, all outcomes in the first row are marked.

This means that the **first toss is heads**, regardless of the second toss.

So the event is:

\[
\text{the first toss is heads}
\]

### Case 2

In this case, the marked outcomes are:

\[
HT,\ TH
\]

This corresponds to the situation where the two tosses are different.

So the event is:

\[
\text{exactly one head}
\]

## Final conclusion

This problem shows how:

- elementary outcomes are represented as cells in a table,
- events correspond to subsets of the sample space,
- logical statements are translated into sets,
- graphical representation helps understand the structure of events.