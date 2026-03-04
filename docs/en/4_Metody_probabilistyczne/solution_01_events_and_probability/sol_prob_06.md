## Task 6

Two machines produce identical products. The production ratio of machine 1 to machine 2 is $3:2$.

Let:
- $M_1$ = event "product was produced by machine 1"
- $M_2$ = event "product was produced by machine 2"
- $F$ = event "product is first-grade"

### Step 1: Convert the production ratio into probabilities

If the ratio is $3:2$, then out of $3+2=5$ parts:
\[
P(M_1)=\frac{3}{5}, \quad P(M_2)=\frac{2}{5}
\]

Given quality rates:
\[
P(F\mid M_1)=0.65, \quad P(F\mid M_2)=0.85
\]

---

### 1) Probability a randomly selected product is first-grade (Total Probability)

We apply the total probability formula:
\[
P(F)=P(M_1)P(F\mid M_1)+P(M_2)P(F\mid M_2)
\]

Substitute values:
\[
P(F)=\frac{3}{5}\cdot 0.65 + \frac{2}{5}\cdot 0.85
\]

Compute:
- $\frac{3}{5}\cdot 0.65 = 0.39$
- $\frac{2}{5}\cdot 0.85 = 0.34$

So:
\[
P(F)=0.39+0.34=0.73
\]

**Answer:** $P(F)=0.73$

---

### 2) Given the product is first-grade, probability it came from machine 1 (Bayes)

We use Bayes' theorem:
\[
P(M_1\mid F)=\frac{P(M_1)P(F\mid M_1)}{P(F)}
\]

Substitute:
\[
P(M_1\mid F)=\frac{\frac{3}{5}\cdot 0.65}{0.73}=\frac{0.39}{0.73}\approx 0.534
\]

**Answer:** $P(M_1\mid F)\approx 0.534$ (about $53.4\%$)