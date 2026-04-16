# Problem 4 — Building complex statements from simple ones

We consider an experiment consisting of **two dice rolls**.

Each outcome is a pair \((i,j)\), where:
- \(i\) — result of the first die (row),
- \(j\) — result of the second die (column).

Representation:
      1 2 3 4 5 6
1     . . . . . .
2     . . . . . .
3     . . . . . .
4     . . . . . .
5     . . . . . .
6     . . . . . .

---

## Part A — basic statements

### Event A — sum equals 7

Condition:
\[
i + j = 7
\]
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 X . . . . .

---

### Event B — first die greater than second

Condition:
\[
i > j
\]
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X X . . .
5 X X X X . .
6 X X X X X .

---

### Event C — at least one die shows 6

Condition:
\[
i = 6 \quad \text{or} \quad j = 6
\]
1  . . . . . X
2  . . . . . X
3  . . . . . X
4  . . . . . X
5  . . . . . X
6  X X X X X X

---

## Part B — compound statements

### 1. A ∪ C (sum = 7 OR at least one 6)
1 . . . . . X
2 . . . . X X
3 . . . X . X
4 . . X . . X
5 . X . . . X
6 X X X X X X

---

### 2. A ∩ C (sum = 7 AND at least one 6)

Only outcomes satisfying both:
- sum = 7
- at least one 6
1 . . . . . X
2 . . . . . .
3 . . . . . .
4 . . . . . .
5 . . . . . .
6 X . . . . .

---

### 3. B ∩ C (first > second AND at least one 6)
1 . . . . . .
2 . . . . . .
3 . . . . . .
4 . . . . . .
5 . . . . . .
6 X X X X X .

---

### 4. A ∩ Bᶜ (sum = 7 AND first ≤ second)
1 . . . . . X
2 . . . . X .
3 . . . X . .
4 . . . . . .
5 . . . . . .
6 . . . . . .

---

### 5. A ∩ (no 6)

(sum = 7 AND neither die is 6)
1 . . . . . .
2 . . . . X .
3 . . . X . .
4 . . X . . .
5 . X . . . .
6 . . . . . .

---

### 6. C ∩ Aᶜ (at least one 6 BUT sum ≠ 7)
1 . . . . . .
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 X X X X X X

(remove (1,6) and (6,1))

---

### 7. Aᶜ ∩ B (sum ≠ 7 AND first > second)
1 . . . . . .
2 X . . . . .
3 X X . . . .
4 X X . . . .
5 X . . . . .
6 X X X X X .

(remove pairs where sum = 7)

---

### 8. Bᶜ ∩ C (first ≤ second AND at least one 6)
1 . . . . . X
2 . . . . . X
3 . . . . . X
4 . . . . . X
5 . . . . . X
6 . . . . . X

---

### 9. (A ∪ C)ᶜ

(not sum = 7 AND no die shows 6)
1 X X X X X .
2 X X X X . .
3 X X X . X .
4 X X . X X .
5 X . X X X .
6 . . . . . .

---

### 10. (A ∩ C)ᶜ

(all except intersection)
1 X X X X X .
2 X X X X X X
3 X X X X X X
4 X X X X X X
5 X X X X X X
6 . X X X X X

---

## Final conclusion

This problem demonstrates:

- how logical operations correspond to set operations:
  - OR → union
  - AND → intersection
  - NOT → complement
- how events can be constructed from simpler ones,
- how graphical representation helps visualize complex logical relations.