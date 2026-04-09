# Task 4 — Poisson Model (Arrival of Events)

## 1. Description of the random experiment

A web service receives error reports over time.  
It is given that, on average, the service receives **3 error reports per hour**.

We observe one fixed time interval of length **1 hour** and count how many error reports arrive during that time.

This situation is described by the **Poisson model**, which is used for counting the number of events occurring in a fixed time interval.

---

## 2. Sample space \( \Omega \)

Let \(X\) denote the number of error reports received in one hour.

Since the number of reports can be any non-negative integer, the sample space is:

\[
\Omega = \{0,1,2,3,\dots\}
\]

This means that during one hour the service may receive:

- no reports,
- one report,
- two reports,
- three reports,
- and so on.

---

## 3. Formula of the probability distribution

If the random variable \(X\) has a Poisson distribution with parameter \(\lambda\), then its probability distribution is:

\[
P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}, \quad k=0,1,2,3,\dots
\]

where:

- \(e\) is the base of the natural logarithm,
- \(\lambda\) is the average number of events in the considered interval,
- \(k\) is the exact number of events we want to calculate the probability for.

In this task, since the average number of error reports per hour is 3, we have:

\[
\lambda = 3
\]

So for this situation the distribution is:

\[
P(X=k)=\frac{e^{-3}3^k}{k!}, \quad k=0,1,2,3,\dots
\]

---

## 4. Interpretation of the parameter \( \lambda \)

The parameter \(\lambda\) in the Poisson distribution represents:

> **the average number of events in a fixed interval**

In this task, the interval is **one hour**, and the web service receives on average **3 error reports per hour**.

Therefore:

\[
\lambda = 3
\]

This means that in every one-hour interval, the expected number of received error reports is 3.

---

## Final conclusion

Task 4 is an example of a **Poisson model**, because:

- we count the number of events occurring in a fixed time interval,
- the possible values are \(0,1,2,\dots\),
- the distribution is determined by the parameter \(\lambda\),
- here \(\lambda = 3\), because the average number of reports per hour equals 3.