# Solution
# Task 1 — Recognizing Counting Models

For each situation, we identify the correct combinatorial model by answering the key questions:

1. Are we using **all objects** or only **some** of them?
2. Does **order matter**?
3. Is **repetition allowed**?
4. Are some objects **identical**?
5. Is the arrangement **linear** or **circular**?

---

## 1. Arranging 7 students in a line

We are arranging **all 7 students**, so this is not a selection of only some objects.

Also, the students are placed **in a line**, so order matters.  
For example, if Alice is first and Bob is second, this is different from Bob being first and Alice being second.

The students are all different people, so they are **distinguishable**, and no student can appear more than once.

Therefore:

- all objects are used,
- order matters,
- no repetition,
- linear arrangement.

### Conclusion:
This is a **permutation**.

---

## 2. Choosing 4 members of a committee from 12 people

Here we are **not arranging all 12 people**, but only selecting **4 of them**.

In a committee, the order of the chosen people does **not** matter.  
For example, choosing Anna, John, Mike, and Sara is the same committee as choosing Sara, Mike, Anna, and John.

Also, one person cannot be chosen twice.

Therefore:

- only some objects are used,
- order does **not** matter,
- no repetition.

### Conclusion:
This is a **combination**.

---

## 3. Assigning gold, silver, and bronze medals among 15 athletes

We are choosing **3 athletes** from 15, so only some of the objects are used.

However, **order matters**, because getting gold is different from getting silver, and silver is different from bronze.

For example:

- Alice = gold, Bob = silver, Carol = bronze

is different from

- Bob = gold, Alice = silver, Carol = bronze.

Also, one athlete cannot receive more than one medal.

Therefore:

- only some objects are used,
- order matters,
- no repetition.

### Conclusion:
This is a **k-permutation** (ordered selection without repetition).

---

## 4. Forming a 6-digit PIN code

A PIN code consists of **6 positions**, and each position can contain a digit.

Order clearly matters.  
For example, the code `123456` is different from `654321`.

Also, in a PIN code, digits **may repeat** unless stated otherwise.  
For example, `111111` is allowed.

So this is an ordered sequence where repetition is allowed.

Therefore:

- order matters,
- repetition is allowed,
- each position is chosen independently.

### Conclusion:
This is a **sequence with repetition**.

---

## 5. Arranging the letters of the word BANANA

The word **BANANA** has 6 letters:

- B appears 1 time,
- A appears 3 times,
- N appears 2 times.

We are arranging **all letters**, so this is an arrangement of all objects.

Order matters, because different letter orders create different words.

However, some letters are **repeated**, and identical letters are not distinguished from one another.  
For example, swapping one `A` with another `A` does not create a new arrangement.

Therefore:

- all objects are used,
- order matters,
- some objects are identical.

### Conclusion:
This is a **permutation with repeated elements**.

---

## 6. Seating 6 people around a round table

We are arranging **all 6 people**, so all objects are used.

But this is not a line; it is a **circle**.  
In circular arrangements, rotating the whole seating does not produce a new arrangement.

For example, if everyone shifts one seat to the left, the relative positions stay the same, so it is considered the same circular arrangement.

Therefore:

- all objects are used,
- arrangement is circular,
- only relative position matters.

### Conclusion:
This is a **circular permutation**.

---

# Final Answers

1. Arranging 7 students in a line → **Permutation**  
2. Choosing 4 members of a committee from 12 people → **Combination**  
3. Assigning gold, silver, and bronze medals among 15 athletes → **k-permutation**  
4. Forming a 6-digit PIN code → **Sequence with repetition**  
5. Arranging the letters of **BANANA** → **Permutation with repeated elements**  
6. Seating 6 people around a round table → **Circular permutation**