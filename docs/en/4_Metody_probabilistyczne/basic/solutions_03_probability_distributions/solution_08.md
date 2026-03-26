## Task 08 – Multiplication Rule and Multi-Stage Experiments

In this task we use the multiplication rule.

If an experiment happens in stages, then the probability of a specific sequence of events is found by multiplying the probability of each stage, taking previous stages into account when necessary.

In symbols:

P(A ∩ B) = P(B) * P(A | B)

or more generally for several stages:

P(A1 ∩ A2 ∩ A3) = P(A1) * P(A2 | A1) * P(A3 | A1 ∩ A2)

---

### 1) An urn contains 6 white and 4 black balls. Two balls are drawn without replacement.

We want the probability that:
- the first ball is white,
- the second ball is black.

#### Step 1: Probability that the first ball is white

There are 6 white balls out of 10 total balls.

So:

P(first is white) = 6/10 = 3/5

#### Step 2: Probability that the second ball is black, given that the first was white

After drawing one white ball, there are:
- 9 balls left in total,
- still 4 black balls.

So:

P(second is black | first is white) = 4/9

#### Step 3: Multiply the stage probabilities

P(first white and second black) = P(first white) * P(second black | first white)

P(first white and second black) = (6/10) * (4/9)

P(first white and second black) = 24/90 = 4/15

**Answer:** P(first white and second black) = 4/15

---

### 2) A box contains 5 defective and 15 non-defective components. Three components are drawn without replacement.

We want the probability that:
- the first two are defective,
- the third is non-defective.

Let:
- D = defective,
- N = non-defective.

So we want the sequence:

D, D, N

#### Step 1: Probability that the first component is defective

There are 5 defective components out of 20 total.

So:

P(first is defective) = 5/20 = 1/4

#### Step 2: Probability that the second component is defective, given that the first was defective

Now there are:
- 19 components left,
- 4 defective left.

So:

P(second is defective | first defective) = 4/19

#### Step 3: Probability that the third component is non-defective, given that the first two were defective

After drawing two defective components, there are:
- 18 components left,
- still 15 non-defective.

So:

P(third is non-defective | first two defective) = 15/18 = 5/6

#### Step 4: Multiply all three probabilities

P(D, D, N) = (5/20) * (4/19) * (15/18)

Simplify step by step:

(5/20) = 1/4  
(15/18) = 5/6

So:

P(D, D, N) = (1/4) * (4/19) * (5/6)

The 4 cancels:

P(D, D, N) = 1/19 * 5/6 = 5/114

**Answer:** P(exactly first two defective and third non-defective) = 5/114

---

### 3) A family has two children.

Assume that each child is equally likely to be a boy or a girl, independently of the other.

We want the probability that both are girls, given that the older child is a girl.

#### Step 1: Write the sample space

We describe children in order: (older, younger)

Possible outcomes:

{BB, BG, GB, GG}

where:
- B = boy
- G = girl

Each outcome has probability 1/4.

#### Step 2: Apply the condition

We are given that the older child is a girl.

So we keep only outcomes where the first child is G:

{GB, GG}

These are the only possible outcomes under the condition.

#### Step 3: Find the favorable outcomes

We want both children to be girls.

Among {GB, GG}, only GG satisfies this.

So there is 1 favorable outcome out of 2 possible conditional outcomes.

Therefore:

P(both girls | older child is a girl) = 1/2

**Answer:** P(both girls | older child is a girl) = 1/2

---

### 4) A machine produces parts, each defective with probability 0.03, independently of others.

We want the probability that among the next three parts:
- the first two are good,
- the third is defective.

#### Step 1: Determine the probability that a part is good

If a part is defective with probability 0.03, then it is good with probability:

P(good) = 1 - 0.03 = 0.97

So:
- P(good) = 0.97
- P(defective) = 0.03

#### Step 2: Multiply the probabilities

The required sequence is:

good, good, defective

Since the productions are independent, we multiply directly:

P(G, G, D) = 0.97 * 0.97 * 0.03

First compute:

0.97 * 0.97 = 0.9409

Then:

0.9409 * 0.03 = 0.028227

So:

P(G, G, D) = 0.028227

**Answer:** P(first two good and third defective) = 0.028227

---

### Final answers

1. Urn problem:
   - P(first white and second black) = 4/15

2. Components problem:
   - P(first two defective and third non-defective) = 5/114

3. Two children problem:
   - P(both girls | older child is a girl) = 1/2

4. Machine problem:
   - P(first two good and third defective) = 0.028227