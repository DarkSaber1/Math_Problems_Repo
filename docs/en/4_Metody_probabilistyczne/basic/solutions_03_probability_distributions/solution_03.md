## Task 03 – Event Algebra for Two Coin Tosses

We consider the experiment of tossing a fair coin twice.

Let:

- A = "at least one head occurs"
- B = "both tosses give the same result"

---

### Step 1: Write the sample space explicitly

Each toss can give one of two results:
- H = Head
- T = Tail

Since we toss the coin twice, the possible ordered outcomes are:

Omega = {HH, HT, TH, TT}

where:
- HH = first toss head, second toss head
- HT = first toss head, second toss tail
- TH = first toss tail, second toss head
- TT = first toss tail, second toss tail

---

### Step 2: Describe events A and B as subsets of the sample space

#### Event A: "at least one head occurs"

This means that in the two tosses, we get one or two heads.

The only outcome that does **not** belong to this event is TT, because it has no heads.

So:

A = {HH, HT, TH}

---

#### Event B: "both tosses give the same result"

This means:
- both tosses are heads, or
- both tosses are tails

So:

B = {HH, TT}

---

### Step 3: Determine the required event operations

#### 1) A ∪ B

The union contains all outcomes that belong to A or B or both.

A = {HH, HT, TH}  
B = {HH, TT}

Combining all elements:

A ∪ B = {HH, HT, TH, TT}

Therefore:

A ∪ B = Omega

---

#### 2) A ∩ B

The intersection contains only outcomes that belong to both A and B.

A = {HH, HT, TH}  
B = {HH, TT}

The only common outcome is HH.

So:

A ∩ B = {HH}

---

#### 3) A^c

The complement of A contains all outcomes from Omega that are not in A.

Omega = {HH, HT, TH, TT}  
A = {HH, HT, TH}

The only missing outcome is TT.

So:

A^c = {TT}

---

#### 4) B^c

The complement of B contains all outcomes from Omega that are not in B.

Omega = {HH, HT, TH, TT}  
B = {HH, TT}

The outcomes not in B are HT and TH.

So:

B^c = {HT, TH}

---

#### 5) A \ B

This means outcomes that belong to A but do not belong to B.

A = {HH, HT, TH}  
B = {HH, TT}

We remove HH from A, because it also belongs to B.

So:

A \ B = {HT, TH}

---

#### 6) B \ A

This means outcomes that belong to B but do not belong to A.

B = {HH, TT}  
A = {HH, HT, TH}

We remove HH from B, because it also belongs to A.

So:

B \ A = {TT}

---

### Step 4: Decide whether A and B are mutually exclusive

Two events are mutually exclusive if they cannot happen at the same time.

That means their intersection must be empty:

A ∩ B = empty set

But here:

A ∩ B = {HH}

This is not empty.

Therefore, A and B are **not mutually exclusive**.

---

### Step 5: Decide whether A and B are independent

Two events are independent if:

P(A ∩ B) = P(A) * P(B)

Since the coin is fair and tossed twice, all 4 outcomes are equally likely.

So:

P(A) = 3/4  
because A = {HH, HT, TH}

P(B) = 2/4 = 1/2  
because B = {HH, TT}

P(A ∩ B) = 1/4  
because A ∩ B = {HH}

Now check independence:

P(A) * P(B) = (3/4) * (1/2) = 3/8

But:

P(A ∩ B) = 1/4

Since:

1/4 != 3/8

the events are **not independent**.

---

### Final answers

- A = {HH, HT, TH}
- B = {HH, TT}
- A ∪ B = {HH, HT, TH, TT} = Omega
- A ∩ B = {HH}
- A^c = {TT}
- B^c = {HT, TH}
- A \ B = {HT, TH}
- B \ A = {TT}
- A and B are **not mutually exclusive**
- A and B are **not independent**