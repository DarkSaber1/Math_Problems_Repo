## Task 06 – Conditional Probability: Definition and Direct Computation

In each problem we follow the same plan:

1. define the events A and B,
2. compute P(A), P(B), and P(A ∩ B),
3. use the definition of conditional probability:

P(A | B) = P(A ∩ B) / P(B),   provided that P(B) > 0

---

### 1) Two numbers are drawn successively from {1, 2, 3, 4, 5} without replacement

Define:
- A = "the product of the drawn numbers is greater than 10"
- B = "the first number drawn is odd"

Since two numbers are drawn successively without replacement, order matters.

So the sample space consists of all ordered pairs (x, y) with x ≠ y.

Number of all possible outcomes:

5 * 4 = 20

So all 20 ordered outcomes are equally likely.

---

#### Step 1: Compute P(B)

The first number must be odd.

Odd numbers in the set are:

1, 3, 5

So there are 3 possible choices for the first number.

After choosing the first number, the second number can be any of the remaining 4 numbers.

Thus the number of outcomes in B is:

3 * 4 = 12

Therefore:

P(B) = 12 / 20 = 3 / 5

---

#### Step 2: Compute P(A)

We need the product of the two drawn numbers to be greater than 10.

List all ordered pairs (x, y) with x ≠ y and x * y > 10.

Possible unordered pairs with product greater than 10 are:

{3,4}, {3,5}, {4,5}

Each unordered pair gives 2 ordered outcomes.

So the favorable ordered pairs are:

(3,4), (4,3), (3,5), (5,3), (4,5), (5,4)

There are 6 such outcomes.

Therefore:

P(A) = 6 / 20 = 3 / 10

---

#### Step 3: Compute P(A ∩ B)

Now we need both conditions:

- the product is greater than 10,
- the first number is odd.

From the 6 outcomes in A:

(3,4), (4,3), (3,5), (5,3), (4,5), (5,4)

we keep only those whose first number is odd.

These are:

(3,4), (3,5), (5,3), (5,4)

So there are 4 favorable outcomes.

Therefore:

P(A ∩ B) = 4 / 20 = 1 / 5

---

#### Step 4: Compute P(A | B)

Using conditional probability:

P(A | B) = P(A ∩ B) / P(B)

Substitute:

P(A | B) = (1/5) / (3/5) = 1/3

**Answer:** P(A | B) = 1/3

---

### 2) One card is drawn from a standard deck

Define:
- A = "the card is a face card"
- B = "the card is a spade"

A standard deck has 52 cards.

Face cards are Jack, Queen, and King.

So there are:

3 face cards in each suit * 4 suits = 12 face cards

There are 13 spades.

---

#### Step 1: Compute P(A)

P(A) = 12 / 52 = 3 / 13

---

#### Step 2: Compute P(B)

P(B) = 13 / 52 = 1 / 4

---

#### Step 3: Compute P(A ∩ B)

This means: the card is both a face card and a spade.

The spade face cards are:
- Jack of spades
- Queen of spades
- King of spades

So there are 3 such cards.

Therefore:

P(A ∩ B) = 3 / 52

---

#### Step 4: Compute P(A | B)

P(A | B) = P(A ∩ B) / P(B)

Substitute:

P(A | B) = (3/52) / (13/52) = 3/13

**Answer:** P(A | B) = 3/13

---

### 3) Two cards are drawn from a standard deck

Define:
- A = "at least one card is greater than 9"
- B = "neither card is a diamond"

We interpret "greater than 9" as cards:
10, J, Q, K, A

So in each suit there are 5 such cards.

Hence in the whole deck there are:

5 * 4 = 20 cards greater than 9

The number of diamonds is 13, so the number of non-diamonds is:

52 - 13 = 39

Two cards are drawn from the deck without replacement.

Since the question is about events such as "at least one" and "neither", it is most natural to count unordered 2-card hands.

Total number of 2-card hands:

C(52,2) = 1326

---

#### Step 1: Compute P(B)

Event B means both cards are non-diamonds.

So we choose 2 cards from the 39 non-diamonds:

Number of favorable hands = C(39,2) = 741

Therefore:

P(B) = C(39,2) / C(52,2) = 741 / 1326 = 19 / 34

---

#### Step 2: Compute P(A)

Event A means at least one of the two cards is greater than 9.

It is easier to use the complement.

Complement of A:
- neither card is greater than 9

There are:

52 - 20 = 32 cards that are not greater than 9

So:

P(A^c) = C(32,2) / C(52,2) = 496 / 1326

Therefore:

P(A) = 1 - 496/1326 = 830/1326 = 415/663

---

#### Step 3: Compute P(A ∩ B)

Now both conditions must hold:
- neither card is a diamond,
- at least one card is greater than 9

Restrict first to the 39 non-diamond cards.

Among these 39 cards, the cards greater than 9 are in the three non-diamond suits:
- hearts, clubs, spades
- 5 in each suit

So there are:

3 * 5 = 15

non-diamond cards greater than 9.

Thus the non-diamond cards that are not greater than 9 are:

39 - 15 = 24

Now count 2-card hands from the 39 non-diamond cards that contain at least one card greater than 9.

Again use complement inside B:

- total non-diamond 2-card hands: C(39,2) = 741
- non-diamond hands with no card greater than 9: C(24,2) = 276

So:

number of favorable hands = 741 - 276 = 465

Therefore:

P(A ∩ B) = 465 / 1326 = 155 / 442

---

#### Step 4: Compute P(A | B)

P(A | B) = P(A ∩ B) / P(B)

Substitute:

P(A | B) = (465/1326) / (741/1326) = 465/741

Simplify:

P(A | B) = 155/247

**Answer:** P(A | B) = 155/247

---

### Final answers

1. Two numbers drawn from {1,2,3,4,5}:
   - P(A) = 3/10
   - P(B) = 3/5
   - P(A ∩ B) = 1/5
   - P(A | B) = 1/3

2. One card from a standard deck:
   - P(A) = 3/13
   - P(B) = 1/4
   - P(A ∩ B) = 3/52
   - P(A | B) = 3/13

3. Two cards from a standard deck:
   - P(A) = 415/663
   - P(B) = 19/34
   - P(A ∩ B) = 155/442
   - P(A | B) = 155/247