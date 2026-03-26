## Task 07 – Conditional Probability in Dice, Cards, and Selection Problems

In this task we use the definition of conditional probability:

P(A | B) = P(A ∩ B) / P(B)

In each problem:
- A = the event we are interested in,
- B = the given condition.

---

### 1) Two fair dice are rolled

We want the probability that the sum is 6, given that at least one die shows a prime number.

Define:
- A = "the sum is 6"
- B = "at least one die shows a prime number"

The prime numbers on a die are:
2, 3, 5

Since two dice are rolled, the sample space has:

6 * 6 = 36

ordered outcomes.

---

#### Step 1: Compute P(A)

The sum is 6 for the following outcomes:

(1,5), (2,4), (3,3), (4,2), (5,1)

So there are 5 favorable outcomes.

Therefore:

P(A) = 5 / 36

---

#### Step 2: Compute P(B)

We want at least one die to show a prime number.

It is easier to count the complement:

B^c = "neither die shows a prime number"

The non-prime numbers on a die are:
1, 4, 6

So each die has 3 non-prime possibilities.

Thus:

number of outcomes in B^c = 3 * 3 = 9

Therefore:

number of outcomes in B = 36 - 9 = 27

So:

P(B) = 27 / 36

---

#### Step 3: Compute P(A ∩ B)

Now we check the 5 outcomes whose sum is 6:

(1,5), (2,4), (3,3), (4,2), (5,1)

In each of these outcomes, at least one die shows a prime number.

So all 5 outcomes belong to B.

That means:

A ∩ B = A

Hence:

P(A ∩ B) = 5 / 36

---

#### Step 4: Compute P(A | B)

P(A | B) = P(A ∩ B) / P(B)

Substitute:

P(A | B) = (5/36) / (27/36) = 5/27

**Answer:** P(A | B) = 5/27

---

### 2) From a group of 4 men and 3 women, 2 people are chosen at random

We want the probability that both chosen people are women.

This problem does not explicitly contain a condition, so we compute an ordinary probability.

Total number of ways to choose 2 people from 7:

C(7,2) = 21

Number of ways to choose 2 women from 3:

C(3,2) = 3

Therefore:

P(both women) = C(3,2) / C(7,2) = 3/21 = 1/7

**Answer:** P(both women) = 1/7

---

### 3) A card is drawn from a standard deck

We want the probability that it is a face card, given that it is black.

Define:
- A = "the card is a face card"
- B = "the card is black"

A standard deck has 52 cards.

Black suits are:
- spades
- clubs

So there are:

26 black cards

Face cards are:
- Jack
- Queen
- King

Each suit has 3 face cards, so among the 2 black suits there are:

2 * 3 = 6 black face cards

Thus:

P(A ∩ B) = 6 / 52
P(B) = 26 / 52

Now compute:

P(A | B) = P(A ∩ B) / P(B)
         = (6/52) / (26/52)
         = 6/26
         = 3/13

**Answer:** P(A | B) = 3/13

---

### 4) Two cards are drawn without replacement

We want the probability that both are aces, given that at least one is an ace.

Define:
- A = "both cards are aces"
- B = "at least one card is an ace"

Since the condition speaks about the two-card hand, it is most natural to count unordered 2-card selections.

Total number of 2-card hands from a 52-card deck:

C(52,2) = 1326

---

#### Step 1: Compute P(A)

There are 4 aces in the deck.

To have both cards be aces, we choose 2 out of the 4 aces:

number of favorable hands = C(4,2) = 6

So:

P(A) = 6 / 1326

---

#### Step 2: Compute P(B)

We want at least one ace.

It is easier to count the complement:

B^c = "no ace is drawn"

There are:

52 - 4 = 48

non-ace cards.

So the number of 2-card hands with no ace is:

C(48,2) = 1128

Thus the number of hands with at least one ace is:

1326 - 1128 = 198

So:

P(B) = 198 / 1326

---

#### Step 3: Compute P(A ∩ B)

If both cards are aces, then automatically at least one card is an ace.

So:

A ∩ B = A

Therefore:

P(A ∩ B) = 6 / 1326

---

#### Step 4: Compute P(A | B)

P(A | B) = P(A ∩ B) / P(B)

Substitute:

P(A | B) = (6/1326) / (198/1326) = 6/198 = 1/33

**Answer:** P(A | B) = 1/33

---

### Final answers

1. Two fair dice:
   - P(sum = 6 | at least one prime) = 5/27

2. Group of 4 men and 3 women:
   - P(both chosen are women) = 1/7

3. One card from a standard deck:
   - P(face card | black) = 3/13

4. Two cards without replacement:
   - P(both are aces | at least one ace) = 1/33