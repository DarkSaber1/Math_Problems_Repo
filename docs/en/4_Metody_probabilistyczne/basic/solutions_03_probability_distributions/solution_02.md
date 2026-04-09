# Task 2 — Hypergeometric Model (Sampling from a Batch)

## 1. Description of the random experiment

A warehouse contains **20 components** in total:

- **5 defective** components,
- **15 functional** components.

We randomly select **4 components without replacement** for inspection.

Because the selection is made **without replacement**, the probabilities change from draw to draw.  
This is why the experiment is described by the **hypergeometric model**.

---

## 2. Definition of the random variable

Let \(X\) denote the **number of defective components** in the selected sample of 4 elements.

So:

\[
X = \text{number of defective components in the sample}
\]

---

## 3. Possible values of \(X\)

Since we select 4 components, the smallest possible number of defective elements is **0**, and the largest possible number is **4**.

Also, since there are 5 defective elements in the warehouse, selecting 4 defective elements is possible.

Therefore:

\[
X \in \{0,1,2,3,4\}
\]

---

## 4. Probability distribution

The hypergeometric distribution has the following formula:

\[
P(X=k)=\frac{\binom{5}{k}\binom{15}{4-k}}{\binom{20}{4}}, \quad k=0,1,2,3,4
\]

### Explanation of the formula

- \(\binom{5}{k}\) — number of ways to choose \(k\) defective components from 5 defective ones,
- \(\binom{15}{4-k}\) — number of ways to choose the remaining \(4-k\) functional components from 15 functional ones,
- \(\binom{20}{4}\) — total number of ways to choose any 4 components from 20.

Thus, the full distribution is:

\[
P(X=0)=\frac{\binom{5}{0}\binom{15}{4}}{\binom{20}{4}}
\]

\[
P(X=1)=\frac{\binom{5}{1}\binom{15}{3}}{\binom{20}{4}}
\]

\[
P(X=2)=\frac{\binom{5}{2}\binom{15}{2}}{\binom{20}{4}}
\]

\[
P(X=3)=\frac{\binom{5}{3}\binom{15}{1}}{\binom{20}{4}}
\]

\[
P(X=4)=\frac{\binom{5}{4}\binom{15}{0}}{\binom{20}{4}}
\]

---

## 5. Meaning of success in this model

In this model, a **success** means:

> **drawing a defective component**

So each time a defective element is selected, we count it as a success.

---

## Final conclusion

Task 2 is an example of a **hypergeometric model**, because:

- we select elements from a **finite population**,
- the population contains two types of elements (**defective** and **functional**),
- the selection is made **without replacement**,
- the random variable \(X\) counts the number of successes, where a success means selecting a defective component.