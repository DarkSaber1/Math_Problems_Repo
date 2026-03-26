## Task 04 – Basic Probability Properties

In this task we use only standard probability rules:
- complement rule,
- union formula,
- the property of mutually exclusive events,
- and the definition of independence.

---

### 1) If P(A) = 0.35, find P(A^c)

The complement of event A means that event A does not occur.

For every event A, the following rule holds:

P(A) + P(A^c) = 1

So:

P(A^c) = 1 - P(A)

Substitute the given value:

P(A^c) = 1 - 0.35 = 0.65

**Answer:** P(A^c) = 0.65

---

### 2) If P(A) = 0.4, P(B) = 0.5, P(A ∩ B) = 0.2, compute P(A ∪ B)

To find the probability that at least one of the events A or B occurs, we use the union formula:

P(A ∪ B) = P(A) + P(B) - P(A ∩ B)

We subtract P(A ∩ B) because it is counted twice when we add P(A) and P(B).

Now substitute the values:

P(A ∪ B) = 0.4 + 0.5 - 0.2

P(A ∪ B) = 0.7

**Answer:** P(A ∪ B) = 0.7

---

### 3) If A and B are mutually exclusive and P(A) = 0.18, P(B) = 0.27, compute P(A ∪ B)

If two events are mutually exclusive, they cannot occur at the same time. Therefore:

A ∩ B = empty set

and so:

P(A ∩ B) = 0

The union formula becomes:

P(A ∪ B) = P(A) + P(B)

Substitute:

P(A ∪ B) = 0.18 + 0.27 = 0.45

**Answer:** P(A ∪ B) = 0.45

---

### 4) If P(A ∪ B) = 0.9, P(A) = 0.6, P(B) = 0.5, compute P(A ∩ B)

Again we use the union formula:

P(A ∪ B) = P(A) + P(B) - P(A ∩ B)

Now solve for the intersection:

P(A ∩ B) = P(A) + P(B) - P(A ∪ B)

Substitute the values:

P(A ∩ B) = 0.6 + 0.5 - 0.9

P(A ∩ B) = 0.2

**Answer:** P(A ∩ B) = 0.2

---

### 5) Can two events be simultaneously:
- mutually exclusive,
- independent,
- and both have positive probability?

We analyze the two conditions separately.

#### Mutually exclusive

If A and B are mutually exclusive, then they cannot occur together. So:

P(A ∩ B) = 0

#### Independent

If A and B are independent, then:

P(A ∩ B) = P(A) · P(B)

Now suppose both events have positive probability. That means:

P(A) > 0 and P(B) > 0

Then their product is also positive:

P(A) · P(B) > 0

But for mutually exclusive events we already have:

P(A ∩ B) = 0

So we would need:

0 = P(A) · P(B)

This is impossible if both P(A) and P(B) are positive.

Therefore, two events cannot be at the same time:
- mutually exclusive,
- independent,
- and both have positive probability.

This can happen only in the trivial case when at least one of the events has probability 0.

**Answer:** No, this is impossible if both events have positive probability.