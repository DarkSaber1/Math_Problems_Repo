# Task 4 — Circular Permutations

In this task we work with **circular arrangements**.

For linear arrangements of \(n\) distinct people, we use \(n!\).  
But for seating around a **round table**, many arrangements that look different in a line are actually the same after rotation.

For example, if everyone shifts one seat clockwise, the relative positions do not change, so this is considered the **same circular arrangement**.

Because of this, the number of circular permutations of \(n\) distinct objects is

$$
(n-1)!
$$

We now solve each problem carefully.

---

## 1. In how many ways can 7 people sit around a round table?

We have 7 distinct people seated around a round table.

In circular seating, only the **relative order** matters, not the absolute position.

A standard method is to fix one person in place to remove the rotational symmetry.  
Then we arrange the remaining 6 people around that fixed person.

So the number of circular arrangements is

$$
(7-1)! = 6!
$$

Now compute:

$$
6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720
$$

### Answer:
$$
720
$$

---

## 2. In how many ways can they sit if two particular people must sit next to each other?

Let the two particular people be \(A\) and \(B\).

Since \(A\) and \(B\) must sit next to each other, we treat them as a **single block**.

### Step 1: Form a block

If \(A\) and \(B\) are together, then we have:

- one block \((AB)\),
- plus the remaining 5 people.

So in total we now have **6 objects** to arrange around the circle.

### Step 2: Count the circular arrangements of the 6 objects

The number of circular arrangements of 6 distinct objects is

$$
(6-1)! = 5!
$$

### Step 3: Count the internal arrangements of the block

Inside the block, the two people can be ordered in 2 ways:

- \(AB\)
- \(BA\)

So we multiply by

$$
2!
$$

### Step 4: Multiply

Thus the total number of seatings is

$$
5! \cdot 2!
$$

Now compute:

$$
5! = 120, \qquad 2! = 2
$$

So:

$$
5! \cdot 2! = 120 \cdot 2 = 240
$$

### Answer:
$$
240
$$

---

## 3. In how many ways can they sit if those two people must sit opposite each other?

Again let the two particular people be \(A\) and \(B\).

For two people to sit **opposite each other**, the table must have an even number of seats in a symmetric circle.  
Since there are 7 people, there are 7 seats around the table.

But with 7 seats, there is **no seat directly opposite** any given seat.  
In an odd-numbered circle, opposite positions do not exist.

Therefore, it is impossible for two people to sit opposite each other when 7 people are seated around a round table.

### Answer:
$$
0
$$

---

# Final Answers

1. Number of circular seatings of 7 people:

$$
(7-1)! = 6! = 720
$$

2. Number of seatings where two particular people sit next to each other:

$$
5! \cdot 2! = 240
$$

3. Number of seatings where two particular people sit opposite each other:

$$
0
$$