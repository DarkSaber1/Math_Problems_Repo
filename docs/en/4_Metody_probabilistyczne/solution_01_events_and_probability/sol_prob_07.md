## Task 7

## Solution

Two possible transmitted signals:
- $S=111$ with prior probability $P(S=111)=0.65$
- $S=000$ with prior probability $P(S=000)=0.35$

Interference acts independently on each symbol:
- $1$ is received as $0$ with probability $0.2$  ⇒ $P(1\to 1)=0.8$
- $0$ is received as $1$ with probability $0.2$  ⇒ $P(0\to 0)=0.8$

Let $R$ be the received 3-bit signal. We use the law of total probability:
\[
P(R=r)=P(S=111)P(R=r\mid S=111)+P(S=000)P(R=r\mid S=000)
\]

---

### 1) Probability of receiving $111$

If $111$ was sent, to receive $111$ all three 1s must stay 1:
\[
P(R=111\mid S=111)=0.8^3
\]

If $000$ was sent, to receive $111$ all three 0s must flip to 1:
\[
P(R=111\mid S=000)=0.2^3
\]

Therefore:
\[
P(R=111)=0.65\cdot 0.8^3 + 0.35\cdot 0.2^3
\]
\[
P(R=111)=0.65\cdot 0.512 + 0.35\cdot 0.008
=0.3328+0.0028=0.3356
\]

**Answer:** $P(R=111)=0.3356$

---

### 2) Probability of receiving $000$

If $111$ was sent, to receive $000$ all three 1s must flip to 0:
\[
P(R=000\mid S=111)=0.2^3
\]

If $000$ was sent, to receive $000$ all three 0s must stay 0:
\[
P(R=000\mid S=000)=0.8^3
\]

Therefore:
\[
P(R=000)=0.65\cdot 0.2^3 + 0.35\cdot 0.8^3
\]
\[
P(R=000)=0.65\cdot 0.008 + 0.35\cdot 0.512
=0.0052+0.1792=0.1844
\]

**Answer:** $P(R=000)=0.1844$

---

### 3) Probability of receiving $010$

Compute conditional probabilities using independence.

If $111$ was sent, to receive $010$:
- first bit: $1\to 0$ with prob $0.2$
- second bit: $1\to 1$ with prob $0.8$
- third bit: $1\to 0$ with prob $0.2$

So:
\[
P(R=010\mid S=111)=0.2\cdot 0.8\cdot 0.2=0.032
\]

If $000$ was sent, to receive $010$:
- first bit: $0\to 0$ with prob $0.8$
- second bit: $0\to 1$ with prob $0.2$
- third bit: $0\to 0$ with prob $0.8$

So:
\[
P(R=010\mid S=000)=0.8\cdot 0.2\cdot 0.8=0.128
\]

Now apply total probability:
\[
P(R=010)=0.65\cdot 0.032 + 0.35\cdot 0.128
\]
\[
P(R=010)=0.0208+0.0448=0.0656
\]

**Answer:** $P(R=010)=0.0656$