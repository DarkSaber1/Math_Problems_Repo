# Problem 5 — From recorded frequencies to probability

A student rolled a six-sided die **1000 times** and recorded the numbers of occurrences of the elementary outcomes as follows:

\[
n(\{1\})=168,\qquad n(\{2\})=154,\qquad n(\{3\})=181,
\]

\[
n(\{4\})=167,\qquad n(\{5\})=160,\qquad n(\{6\})=170.
\]

The sample space is:

\[
\Omega=\{1,2,3,4,5,6\}.
\]

For every event \(A \subseteq \Omega\), the observed frequency is defined by

\[
f(A)=\frac{n(A)}{1000}.
\]

The goal of this problem is not only to compute some frequencies, but also to understand how frequencies behave when events are combined, and how this leads naturally to the abstract concept of probability. :contentReference[oaicite:0]{index=0}

---

## Part A — From elementary outcomes to events

We compute, step by step, the number of occurrences and then the observed frequency for each event.

### 1. \(A=\{2,4,6\}\)

This event means that the die result is even.

So:

\[
n(A)=n(\{2\})+n(\{4\})+n(\{6\})
\]

\[
n(A)=154+167+170=491
\]

Therefore:

\[
f(A)=\frac{491}{1000}=0.491
\]

---

### 2. \(B=\{1,2,3\}\)

This event means that the outcome is at most 3.

So:

\[
n(B)=n(\{1\})+n(\{2\})+n(\{3\})
\]

\[
n(B)=168+154+181=503
\]

Thus:

\[
f(B)=\frac{503}{1000}=0.503
\]

---

### 3. \(C=\{5,6\}\)

This event means that the die shows either 5 or 6.

So:

\[
n(C)=n(\{5\})+n(\{6\})
\]

\[
n(C)=160+170=330
\]

Hence:

\[
f(C)=\frac{330}{1000}=0.330
\]

---

### 4. \(D=\{1,3,5\}\)

This event means that the outcome is odd.

So:

\[
n(D)=n(\{1\})+n(\{3\})+n(\{5\})
\]

\[
n(D)=168+181+160=509
\]

Therefore:

\[
f(D)=\frac{509}{1000}=0.509
\]

---

### 5. \(E=\{1,2,3,4\}\)

This event means that the result is at most 4.

So:

\[
n(E)=n(\{1\})+n(\{2\})+n(\{3\})+n(\{4\})
\]

\[
n(E)=168+154+181+167=670
\]

Thus:

\[
f(E)=\frac{670}{1000}=0.670
\]

---

## Summary of Part A

\[
n(\{2,4,6\})=491,\qquad f(\{2,4,6\})=0.491
\]

\[
n(\{1,2,3\})=503,\qquad f(\{1,2,3\})=0.503
\]

\[
n(\{5,6\})=330,\qquad f(\{5,6\})=0.330
\]

\[
n(\{1,3,5\})=509,\qquad f(\{1,3,5\})=0.509
\]

\[
n(\{1,2,3,4\})=670,\qquad f(\{1,2,3,4\})=0.670
\]

---

## Part B — How frequencies combine

In this part we verify several identities and explain why they hold. The key idea is that if events are built from **disjoint elementary outcomes**, then their frequencies add in the obvious way. :contentReference[oaicite:1]{index=1}

### 1. Verify:

\[
f(\{2,4,6\}) = f(\{2\}) + f(\{4\}) + f(\{6\})
\]

We compute:

\[
f(\{2\})=\frac{154}{1000}=0.154
\]

\[
f(\{4\})=\frac{167}{1000}=0.167
\]

\[
f(\{6\})=\frac{170}{1000}=0.170
\]

So:

\[
f(\{2\})+f(\{4\})+f(\{6\})=0.154+0.167+0.170=0.491
\]

And from Part A:

\[
f(\{2,4,6\})=0.491
\]

Therefore:

\[
f(\{2,4,6\}) = f(\{2\}) + f(\{4\}) + f(\{6\})
\]

This equality holds because the events \(\{2\}, \{4\}, \{6\}\) are **disjoint**: a single die throw cannot be 2 and 4 at the same time.

---

### 2. Verify:

\[
f(\{1,2,3,4\}) = f(\{1,2\}) + f(\{3,4\})
\]

First compute:

\[
n(\{1,2\})=168+154=322
\]

\[
f(\{1,2\})=\frac{322}{1000}=0.322
\]

Next:

\[
n(\{3,4\})=181+167=348
\]

\[
f(\{3,4\})=\frac{348}{1000}=0.348
\]

So:

\[
f(\{1,2\})+f(\{3,4\})=0.322+0.348=0.670
\]

And from Part A:

\[
f(\{1,2,3,4\})=0.670
\]

Hence:

\[
f(\{1,2,3,4\}) = f(\{1,2\}) + f(\{3,4\})
\]

This works because \(\{1,2\}\) and \(\{3,4\}\) are disjoint, and together they form \(\{1,2,3,4\}\).

---

### 3. Verify:

\[
f(\{1,3,5\}) + f(\{2,4,6\}) = 1
\]

From Part A:

\[
f(\{1,3,5\})=0.509
\]

\[
f(\{2,4,6\})=0.491
\]

Therefore:

\[
0.509+0.491=1.000
\]

So:

\[
f(\{1,3,5\}) + f(\{2,4,6\}) = 1
\]

This is true because \(\{1,3,5\}\) and \(\{2,4,6\}\) are complementary events: every die result is either odd or even, and no result is both.

---

### 4. Verify:

\[
f(\{5,6\}) = 1 - f(\{1,2,3,4\})
\]

From Part A:

\[
f(\{5,6\})=0.330
\]

\[
f(\{1,2,3,4\})=0.670
\]

So:

\[
1-f(\{1,2,3,4\})=1-0.670=0.330
\]

Thus:

\[
f(\{5,6\}) = 1 - f(\{1,2,3,4\})
\]

This holds because \(\{5,6\}\) is the complement of \(\{1,2,3,4\}\) in \(\Omega\).

---

## Part C — When simple addition works and when it fails

This part is very important conceptually. It shows that simple addition works for disjoint events, but fails if the events overlap. :contentReference[oaicite:2]{index=2}

### 1. Check that

\[
f(\{1,2\}\cup\{5,6\}) = f(\{1,2\}) + f(\{5,6\})
\]

We already know:

\[
f(\{1,2\})=0.322
\]

\[
f(\{5,6\})=0.330
\]

Now:

\[
\{1,2\}\cup\{5,6\}=\{1,2,5,6\}
\]

So:

\[
n(\{1,2,5,6\})=168+154+160+170=652
\]

\[
f(\{1,2,5,6\})=\frac{652}{1000}=0.652
\]

And:

\[
f(\{1,2\})+f(\{5,6\})=0.322+0.330=0.652
\]

Therefore:

\[
f(\{1,2\}\cup\{5,6\}) = f(\{1,2\}) + f(\{5,6\})
\]

This works because the two events are disjoint.

---

### 2. Consider

\[
M=\{1,2,3\},\qquad N=\{3,4,5\}
\]

Compute all required values.

#### Frequency of \(M\)

\[
n(M)=168+154+181=503
\]

\[
f(M)=\frac{503}{1000}=0.503
\]

#### Frequency of \(N\)

\[
n(N)=181+167+160=508
\]

\[
f(N)=\frac{508}{1000}=0.508
\]

#### Frequency of \(M\cup N\)

We have:

\[
M\cup N=\{1,2,3,4,5\}
\]

So:

\[
n(M\cup N)=168+154+181+167+160=830
\]

\[
f(M\cup N)=\frac{830}{1000}=0.830
\]

#### Sum \(f(M)+f(N)\)

\[
f(M)+f(N)=0.503+0.508=1.011
\]

So we obtain:

\[
f(M)=0.503,\qquad f(N)=0.508,\qquad f(M\cup N)=0.830,\qquad f(M)+f(N)=1.011
\]

---

### 3. Explain why

\[
f(M\cup N)\neq f(M)+f(N)
\]

The reason is that the events \(M\) and \(N\) are **not disjoint**.

Indeed:

\[
M\cap N=\{3\}
\]

This means that the outcome 3 belongs to both events. Therefore, when we compute \(f(M)+f(N)\), the outcome 3 is counted **twice**.

That is why the sum \(f(M)+f(N)\) is larger than \(f(M\cup N)\).

---

### 4. Which elementary outcomes are counted twice?

The only common outcome is:

\[
3
\]

So the event counted twice is:

\[
M\cap N=\{3\}
\]

Its frequency is:

\[
f(\{3\})=\frac{181}{1000}=0.181
\]

Indeed, if we subtract this double counting from \(f(M)+f(N)\), we get:

\[
1.011-0.181=0.830
\]

which is exactly \(f(M\cup N)\).

---

## Part D — Covering the whole sample space

This part explains why frequencies over a full partition of the sample space must add up to 1. :contentReference[oaicite:3]{index=3}

### 1. Add the observed frequencies of all one-element events

\[
f(\{1\})=\frac{168}{1000}=0.168
\]

\[
f(\{2\})=\frac{154}{1000}=0.154
\]

\[
f(\{3\})=\frac{181}{1000}=0.181
\]

\[
f(\{4\})=\frac{167}{1000}=0.167
\]

\[
f(\{5\})=\frac{160}{1000}=0.160
\]

\[
f(\{6\})=\frac{170}{1000}=0.170
\]

Now add them:

\[
0.168+0.154+0.181+0.167+0.160+0.170=1.000
\]

So the sum is:

\[
1
\]

---

### 2. Why must the result be equal to 1?

Because these six one-element events are:

- pairwise disjoint,
- and together they cover the whole sample space \(\Omega\).

Every single throw gives exactly one result from \(\{1,2,3,4,5,6\}\), so all 1000 throws are counted exactly once when we add the frequencies of these elementary events.

That is why the total must be 1.

---

### 3. Split \(\Omega\) into three disjoint events

\[
\{1,2\},\qquad \{3,4\},\qquad \{5,6\}
\]

Compute their frequencies.

First:

\[
n(\{1,2\})=168+154=322,\qquad f(\{1,2\})=0.322
\]

Second:

\[
n(\{3,4\})=181+167=348,\qquad f(\{3,4\})=0.348
\]

Third:

\[
n(\{5,6\})=160+170=330,\qquad f(\{5,6\})=0.330
\]

Now sum them:

\[
0.322+0.348+0.330=1.000
\]

So again, the sum is:

\[
1
\]

---

### 4. Why is this sum also equal to 1?

Because the three events are:

- disjoint,
- and their union is the whole sample space:

\[
\{1,2\}\cup\{3,4\}\cup\{5,6\}=\Omega
\]

Thus every trial belongs to exactly one of these three groups, so all trials are counted once and only once.

---

### 5. General statement

Whenever the sample space \(\Omega\) is decomposed into disjoint events whose union is \(\Omega\), the sum of their observed frequencies is equal to 1.

In other words:

> If \(A_1,\dots,A_n\) are pairwise disjoint and
> \[
> A_1\cup\cdots\cup A_n=\Omega,
> \]
> then
> \[
> f(A_1)+\cdots+f(A_n)=1.
> \]

This is one of the key patterns that later becomes an axiom of probability.

---

## Part E — From observed frequency to probability

Now we move from the concrete data of 1000 throws to a more abstract idea. We no longer want to talk only about this one recorded experiment, but about a mathematical rule that assigns a number to every event \(A\subseteq\Omega\), expressing how likely that event is expected to be. :contentReference[oaicite:4]{index=4}

Based on the previous parts, such an assignment should satisfy the following properties.

### 1. It assigns numbers between 0 and 1

A frequency is always a fraction of the total number of trials, so it cannot be negative and cannot exceed 1.

Therefore probability should satisfy:

\[
0\leq P(A)\leq 1
\]

for every event \(A\).

---

### 2. It assigns 0 to the impossible event

The impossible event is the empty set:

\[
\varnothing
\]

If an event never occurs, its observed frequency is 0. So probability should also satisfy:

\[
P(\varnothing)=0
\]

---

### 3. It assigns 1 to the whole sample space

The event \(\Omega\) always occurs, because every trial produces some outcome in the sample space.

So probability should satisfy:

\[
P(\Omega)=1
\]

---

### 4. For disjoint events, the value on the union is the sum of the values

If two events cannot occur simultaneously, then counting the union is the same as counting the two parts separately and adding them.

So for disjoint events \(A\) and \(B\) with \(A\cap B=\varnothing\), we should have:

\[
P(A\cup B)=P(A)+P(B)
\]

More generally, this should hold for any finite family of pairwise disjoint events.

---

### 5. For complementary events, the two values add up to 1

If \(A^c\) is the complement of \(A\), then the events \(A\) and \(A^c\):

- are disjoint,
- together cover the whole sample space.

Therefore:

\[
P(A)+P(A^c)=1
\]

This matches exactly the patterns we observed for frequencies.

---

## Part F — Conclusion

We can now clearly describe the connection between the three levels mentioned in the problem.

### 1. Elementary outcomes and events

At the most concrete level, we start with elementary outcomes such as:

\[
1,2,3,4,5,6
\]

Events are simply subsets of the sample space. For example:

- \(\{2,4,6\}\) means “the result is even,”
- \(\{5,6\}\) means “the result is at least 5.”

So events are built from elementary outcomes.

---

### 2. Observed frequencies from a real experiment

Next, we perform real experiments and count how often each event occurs.

This gives observed frequencies such as:

\[
f(\{2,4,6\})=0.491,\qquad f(\{1,3,5\})=0.509
\]

These frequencies are empirical: they come from actual data.

By studying how they behave, we discover patterns such as:

- values lie between 0 and 1,
- complements sum to 1,
- disjoint unions correspond to sums.

---

### 3. Probability as mathematical abstraction

Finally, probability is introduced as an abstract mathematical function \(P\) that preserves these structural properties, even when we are not looking at one concrete experiment.

So probability is not just a list of measured frequencies. It is a mathematical model inspired by the regularities observed in frequencies.

In this way, we move from:

- concrete outcomes,
- to recorded experimental data,
- to an abstract theory that describes uncertainty in a precise and general way.

---

## Final conclusion

Problem 5 shows the full conceptual path:

1. start with elementary outcomes and events as subsets of the sample space,
2. record frequencies in a real experiment,
3. observe the algebraic rules satisfied by those frequencies,
4. abstract those rules into the mathematical notion of probability.

This is exactly the transition from empirical observation to formal mathematical structure.