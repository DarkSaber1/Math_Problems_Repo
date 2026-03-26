## Task 05 – Event Algebra in Card and Urn Problems

In this task we first describe the events using set notation, and then compute the required probabilities.

---

### 1) One card is drawn from a standard deck

Define:
- A = "the card is a heart"
- B = "the card is a king"

A standard deck has 52 cards.
There are:
- 13 hearts,
- 4 kings.

So:

A = {all 13 hearts}  
B = {King of hearts, King of diamonds, King of clubs, King of spades}

#### a) A ∪ B

This means: the drawn card is a heart or a king.

So this event contains:
- all 13 hearts,
- plus the 3 kings that are not hearts.

Therefore:

A ∪ B = {all hearts} ∪ {all kings}

and its size is:

|A ∪ B| = 13 + 4 - 1 = 16

We subtract 1 because the King of hearts belongs to both A and B.

---

#### b) A ∩ B

This means: the card is both a heart and a king.

The only such card is:

A ∩ B = {King of hearts}

---

#### c) A^c

This means: the card is not a heart.

So A^c is the set of all non-heart cards.

There are:

52 - 13 = 39

such cards.

Thus:

A^c = {all cards except hearts}

---

#### d) B \ A

This means: the card is a king, but not a heart.

So we take all kings and remove the King of hearts.

Therefore:

B \ A = {King of diamonds, King of clubs, King of spades}

---

### 2) One ball is drawn from an urn

The urn contains:
- 5 red balls,
- 3 blue balls,
- 2 green balls.

So the total number of balls is:

5 + 3 + 2 = 10

Define:
- A = "the ball is red"
- B = "the ball is not green"

---

#### a) Probability of A

There are 5 red balls out of 10 total.

So:

P(A) = 5/10 = 1/2

---

#### b) Probability of B

"Not green" means the ball is either red or blue.

So the number of favorable balls is:

5 + 3 = 8

Therefore:

P(B) = 8/10 = 4/5

---

#### c) Probability of A ∩ B

Event A means red.
Event B means not green.

Every red ball is automatically not green.

So:

A ∩ B = A

Therefore:

P(A ∩ B) = P(A) = 5/10 = 1/2

---

#### d) Probability of A ∪ B

Since every red ball is already included in "not green", event A is a subset of B.

So:

A ∪ B = B

Therefore:

P(A ∪ B) = P(B) = 8/10 = 4/5

---

### 3) A class contains 12 girls and 15 boys

A 3-person delegation is selected uniformly at random.

Define:
- A = "at least one girl is selected"

We are asked to express A using a complement event and compute its probability.

---

#### Step 1: Define the complement event

The complement of "at least one girl is selected" is:

A^c = "no girls are selected"

If no girls are selected, then all 3 selected students must be boys.

---

#### Step 2: Count all possible delegations

There are:

12 + 15 = 27

students in total.

The total number of possible 3-person delegations is:

C(27,3)

---

#### Step 3: Count the delegations with no girls

There are 15 boys, and we choose all 3 members from the boys.

So the number of such delegations is:

C(15,3)

---

#### Step 4: Compute the probability

Using the complement rule:

P(A) = 1 - P(A^c)

So:

P(A) = 1 - C(15,3) / C(27,3)

Now compute:

C(15,3) = 455  
C(27,3) = 2925

Thus:

P(A) = 1 - 455/2925

P(A) = (2925 - 455) / 2925 = 2470 / 2925

This fraction can be simplified:

P(A) = 494 / 585

Approximate value:

P(A) ≈ 0.8444

---

### Final answers

#### Part 1
- A ∪ B = hearts or kings
- A ∩ B = {King of hearts}
- A^c = all non-heart cards
- B \ A = {King of diamonds, King of clubs, King of spades}

#### Part 2
- P(A) = 1/2
- P(B) = 4/5
- P(A ∩ B) = 1/2
- P(A ∪ B) = 4/5

#### Part 3
- A^c = "all 3 selected students are boys"
- P(A) = 1 - C(15,3) / C(27,3) = 494/585 ≈ 0.8444