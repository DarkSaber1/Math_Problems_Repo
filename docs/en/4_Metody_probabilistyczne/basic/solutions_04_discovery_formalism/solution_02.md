# Problem 2 — Die × Die

We consider an experiment consisting of **two dice rolls**.

Each outcome is a pair \((i,j)\), where:
- \(i\) is the result of the first die (row),
- \(j\) is the result of the second die (column).

Representation:

      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .


---

## Part A — marking events

### 1. the sum is equal to 8

We mark all pairs \((i,j)\) such that:
\[
i + j = 8
\]

Possible outcomes:
\[
(2,6), (3,5), (4,4), (5,3), (6,2)
\]

1 | . | . | . | . | . | . |
2 | . | . | . | . | . | X |
3 | . | . | . | . | X | . |
4 | . | . | . | X | . | . |
5 | . | . | X | . | . | . |
6 | . | X | . | . | . | . |

---

### 2. the first die is greater than the second

We mark all pairs \((i,j)\) such that:
\[
i > j
\]

1 | . | . | . | . | . | . |
2 | X | . | . | . | . | . |
3 | X | X | . | . | . | . |
4 | X | X | X | . | . | . |
5 | X | X | X | X | . | . |
6 | X | X | X | X | X | . |

---

### 3. both dice show even numbers

Even numbers are: \(2,4,6\)

We mark all pairs where both values are even.

1 | . | . | . | . | . | . |
2 | . | X | . | X | . | X |
3 | . | . | . | . | . | . |
4 | . | X | . | X | . | X |
5 | . | . | . | . | . | . |
6 | . | X | . | X | . | X |

---

### 4. at least one die shows 6

We mark all outcomes where:
- first die = 6 OR
- second die = 6

1 | . | . | . | . | . | X |
2 | . | . | . | . | . | X |
3 | . | . | . | . | . | X |
4 | . | . | . | . | . | X |
5 | . | . | . | . | . | X |
6 | X | X | X | X | X | X |

---

### 5. exactly one die shows 1

We mark all outcomes where:
- one die = 1,
- the other is NOT 1

1 | . | X | X | X | X | X |
2 | X | . | . | . | . | . |
3 | X | . | . | . | . | . |
4 | X | . | . | . | . | . |
5 | X | . | . | . | . | . |
6 | X | . | . | . | . | . |

---

## Part B — interpretation

### Case 1

      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . X X X X
4     . . X X X X
5     . . X X X X
6     . . X X X X

In this case, all outcomes where both dice are at least 3 are marked.

So the event is:

\[
\text{both dice show numbers greater than or equal to 3}
\]

---

### Case 2

      1 2 3 4 5 6
1     X . . . . .
2     . X . . . .
3     . . X . . .
4     . . . X . .
5     . . . . X .
6     . . . . . X

Here, only diagonal elements are marked.

This means:
\[
i = j
\]

So the event is:

\[
\text{both dice show the same number}
\]

---

## Final conclusion

This problem illustrates how:

- outcomes of a two-dimensional experiment can be represented in a grid,
- conditions on outcomes translate into marked subsets,
- logical statements correspond to geometric patterns in the table,
- graphical representation helps to understand relations between events.