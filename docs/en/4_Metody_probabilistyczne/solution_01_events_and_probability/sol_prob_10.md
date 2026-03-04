## Task 10

Possible transmitted 4-letter signals are only:
- $S=AAAA$ with $P(S=AAAA)=0.4$
- $S=BBBB$ with $P(S=BBBB)=0.3$
- $S=CCCC$ with $P(S=CCCC)=0.3$

For each single letter, transmission errors are independent and the channel probabilities are:

- If $A$ is sent: receive $A$ with 0.8, $B$ with 0.1, $C$ with 0.1
- If $B$ is sent: receive $B$ with 0.8, $A$ with 0.1, $C$ with 0.1
- If $C$ is sent: receive $C$ with 0.8, $A$ with 0.1, $B$ with 0.1

Because letters are affected independently, for a 4-letter word we multiply the corresponding single-letter probabilities.

We use total probability:
$P(R=r) = \sum_s P(S=s)\,P(R=r \mid S=s)$

---

### 1) Probability of receiving $AAAA$

Compute conditional probabilities:

- If $S=AAAA$ was sent:
  $P(R=AAAA\mid S=AAAA) = 0.8^4 = 0.4096$

- If $S=BBBB$ was sent:
  $P(R=AAAA\mid S=BBBB) = 0.1^4 = 0.0001$ (each $B$ must be received as $A$)

- If $S=CCCC$ was sent:
  $P(R=AAAA\mid S=CCCC) = 0.1^4 = 0.0001$ (each $C$ must be received as $A$)

Now total probability:

$P(R=AAAA) = 0.4\cdot 0.4096 + 0.3\cdot 0.0001 + 0.3\cdot 0.0001$

$P(R=AAAA) = 0.16384 + 0.00003 + 0.00003 = 0.16390$

**Answer:** $P(R=AAAA)=0.16390$

---

### 2) Probability of receiving $ACAA$

Compute conditional probabilities letter-by-letter.

- If $S=AAAA$ was sent, to receive $A C A A$:
  - $A\to A$: 0.8
  - $A\to C$: 0.1
  - $A\to A$: 0.8
  - $A\to A$: 0.8  
  So $P(R=ACAA\mid S=AAAA)=0.8\cdot 0.1\cdot 0.8\cdot 0.8 = 0.0512$

- If $S=BBBB$ was sent:
  - $B\to A$: 0.1
  - $B\to C$: 0.1
  - $B\to A$: 0.1
  - $B\to A$: 0.1  
  So $P(R=ACAA\mid S=BBBB)=0.1^4 = 0.0001$

- If $S=CCCC$ was sent:
  - $C\to A$: 0.1
  - $C\to C$: 0.8
  - $C\to A$: 0.1
  - $C\to A$: 0.1  
  So $P(R=ACAA\mid S=CCCC)=0.1\cdot 0.8\cdot 0.1\cdot 0.1 = 0.0008$

Now total probability:

$P(R=ACAA)=0.4\cdot 0.0512 + 0.3\cdot 0.0001 + 0.3\cdot 0.0008$

$P(R=ACAA)=0.02048 + 0.00003 + 0.00024 = 0.02075$

**Answer:** $P(R=ACAA)=0.02075$