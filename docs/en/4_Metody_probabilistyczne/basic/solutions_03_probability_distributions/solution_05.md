# Task 5 — Multinomial Model (Categories of Outcomes)

## 1. Description of the random experiment

A player rolls a die **5 times**.

Each result is classified into one of the following three categories:

- **small numbers**: \(1,2\)
- **medium numbers**: \(3,4\)
- **large numbers**: \(5,6\)

Since a fair die is used, each face has probability \(1/6\).  
Therefore, each category contains 2 outcomes, so the probability of each category is:

\[
P(\text{small}) = \frac{2}{6} = \frac{1}{3}
\]

\[
P(\text{medium}) = \frac{2}{6} = \frac{1}{3}
\]

\[
P(\text{large}) = \frac{2}{6} = \frac{1}{3}
\]

Thus, the experiment consists of **5 independent trials**, where each trial may result in one of **3 possible categories**.

This is a **multinomial model**, because it generalizes the binomial model to more than two possible outcomes.

---

## 2. Sample space \( \Omega \)

For each of the 5 die rolls, the result belongs to one of the three categories:

- \(S\) — small,
- \(M\) — medium,
- \(L\) — large.

So the sample space consists of all sequences of length 5 built from the symbols \(S\), \(M\), and \(L\):

\[
\Omega = \{S,M,L\}^5
\]

Examples of elements of the sample space are:

\[
SSMLL,\quad MMMMM,\quad LSMSL,\quad SSSSS
\]

Since each of the 5 trials has 3 possible outcomes, the number of elements in the sample space is:

\[
|\Omega| = 3^5 = 243
\]

---

## 3. Multinomial distribution

Let:

- \(X_1\) = number of small outcomes,
- \(X_2\) = number of medium outcomes,
- \(X_3\) = number of large outcomes.

Then:

\[
X_1 + X_2 + X_3 = 5
\]

The random vector \((X_1, X_2, X_3)\) has a **multinomial distribution** with parameters:

- \(n=5\),
- \(p_1=\frac{1}{3}\),
- \(p_2=\frac{1}{3}\),
- \(p_3=\frac{1}{3}\).

Its probability distribution is:

\[
P(X_1=x_1, X_2=x_2, X_3=x_3)
=
\frac{5!}{x_1!x_2!x_3!}
\left(\frac{1}{3}\right)^{x_1}
\left(\frac{1}{3}\right)^{x_2}
\left(\frac{1}{3}\right)^{x_3}
\]

where:

\[
x_1+x_2+x_3=5
\]

and each \(x_i \geq 0\).

Because all three probabilities are equal to \(1/3\), the formula may also be written as:

\[
P(X_1=x_1, X_2=x_2, X_3=x_3)
=
\frac{5!}{x_1!x_2!x_3!}
\left(\frac{1}{3}\right)^5
\]

provided that \(x_1+x_2+x_3=5\).

---

## 4. Interpretation of the parameters

The parameters of the multinomial distribution are interpreted as follows:

- \(n=5\) — the number of trials, because the die is rolled 5 times,
- \(p_1=\frac{1}{3}\) — probability of obtaining a small number,
- \(p_2=\frac{1}{3}\) — probability of obtaining a medium number,
- \(p_3=\frac{1}{3}\) — probability of obtaining a large number.

The variables \(X_1\), \(X_2\), and \(X_3\) tell us how many times each category appears in the 5 rolls.

---

## Final conclusion

Task 5 is an example of a **multinomial model**, because:

- there is a fixed number of trials (\(5\)),
- each trial has more than two possible outcome categories,
- the trials are independent,
- the category probabilities remain constant in each trial.