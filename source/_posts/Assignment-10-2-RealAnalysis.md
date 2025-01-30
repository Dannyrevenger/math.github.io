---
title: 'Assignment 10.2: Real Analysis'
date: 2024-10-28 20:14:45
tags:
katex: true
mathjax: true
---
## Q1. Let {% mathjax %}\{r ∈ \mathbb{Q} | r > 0 ∧ r^2 > 3\}{% endmathjax %} Show that A has a lower bound in {% mathjax %}\mathbb{Q}{% endmathjax %} but no greatest lower bound in {% mathjax %}\mathbb{Q}{% endmathjax %}. Give all details of the proof along the lines of the proof given in the lecture that the rationals are not complete.
**Proof:** Let {% mathjax %} A = \{ r \in \mathbb{Q} \mid r > 0 \text{ and } r^2 > 3 \} {% endmathjax %}. We aim to show that {% mathjax %} A {% endmathjax %} has a lower bound in {% mathjax %} \mathbb{Q} {% endmathjax %} but no greatest lower bound in {% mathjax %} \mathbb{Q} {% endmathjax %}. 

**Step 1:** Existence of a Lower Bound in {% mathjax %} \mathbb{Q} {% endmathjax %}

Since all elements of {% mathjax %} A {% endmathjax %} are positive and satisfy {% mathjax %} r^2 > 3 {% endmathjax %}, we observe that {% mathjax %} b = 0 {% endmathjax %} is a lower bound. For all {% mathjax %} r \in A {% endmathjax %}, {% mathjax %} r > 0 {% endmathjax %}, so {% mathjax %} 0 \leq r {% endmathjax %}. Therefore, {% mathjax %} b = 0 {% endmathjax %} is a lower bound of {% mathjax %} A {% endmathjax %} in {% mathjax %} \mathbb{Q} {% endmathjax %}.

**Step 2:** Assume the Existence of a Greatest Lower Bound {% mathjax %} b = \frac{p}{q} \in \mathbb{Q} {% endmathjax %}

To reach a contradiction, assume that there exists a rational number {% mathjax %} b = \frac{p}{q} {% endmathjax %} (where {% mathjax %} p, q \in \mathbb{Z}, q > 0 {% endmathjax %}) that is the greatest lower bound (infimum) of {% mathjax %} A {% endmathjax %}. We will examine two cases based on whether {% mathjax %} b^2 < 3 {% endmathjax %} or {% mathjax %} b^2 \geq 3 {% endmathjax %}.

**Step 3:** Case 1: {% mathjax %} b^2 < 3 {% endmathjax %}

Suppose {% mathjax %} b^2 < 3 {% endmathjax %}. We will show this leads to a contradiction by finding a rational number larger than {% mathjax %} b {% endmathjax %} that is still a lower bound of {% mathjax %} A {% endmathjax %}.

Since {% mathjax %} b^2 < 3 {% endmathjax %}, there exists a positive integer {% mathjax %} n {% endmathjax %} such that:

{% mathjax %}
n^2(3q^2 - p^2) > (2n + 1)p^2.
{% endmathjax %}

Dividing both sides by {% mathjax %} n^2 q^2 {% endmathjax %}, we obtain:

{% mathjax %}
\frac{(n+1)^2 p^2}{n^2 q^2} < 3.
{% endmathjax %}

This implies that the rational number {% mathjax %} \frac{(n+1)p}{nq} {% endmathjax %} (which is larger than {% mathjax %} b = \frac{p}{q} {% endmathjax %}) satisfies {% mathjax %} \left( \frac{(n+1)p}{nq} \right)^2 < 3 {% endmathjax %}, making it a valid lower bound of {% mathjax %} A {% endmathjax %}.

Therefore, {% mathjax %} \frac{(n+1)p}{nq} {% endmathjax %} is larger than {% mathjax %} b {% endmathjax %} but still a lower bound of {% mathjax %} A {% endmathjax %}, which contradicts the assumption that {% mathjax %} b {% endmathjax %} is the greatest lower bound.

**Step 4:** Case 2: {% mathjax %} b^2 \geq 3 {% endmathjax %}

Suppose {% mathjax %} b^2 \geq 3 {% endmathjax %}, which implies {% mathjax %} b^2 > 3 {% endmathjax %} (since {% mathjax %} b \in \mathbb{Q} {% endmathjax %} and {% mathjax %} \sqrt{3} \notin \mathbb{Q} {% endmathjax %}).

Since {% mathjax %} b^2 > 3 {% endmathjax %}, there exists an integer {% mathjax %} n {% endmathjax %} large enough such that:

{% mathjax %}
\frac{n^2 p^2}{(n+1)^2 q^2} > 3.
{% endmathjax %}

This implies that {% mathjax %} \frac{np}{(n+1)q} {% endmathjax %}, a rational number smaller than {% mathjax %} b {% endmathjax %}, is still in {% mathjax %} A {% endmathjax %}, as {% mathjax %} \left( \frac{np}{(n+1)q} \right)^2 > 3 {% endmathjax %}. This contradicts the assumption that {% mathjax %} b {% endmathjax %} is the greatest lower bound, as there is a smaller element in {% mathjax %} A {% endmathjax %}.

**Step 5:** Conclusion

Since both cases lead to contradictions, we conclude that there cannot be a greatest lower bound for {% mathjax %} A {% endmathjax %} in {% mathjax %} \mathbb{Q} {% endmathjax %}. Thus, {% mathjax %} A {% endmathjax %} has a lower bound in {% mathjax %} \mathbb{Q} {% endmathjax %}, but no greatest lower bound.

This completes the proof.


Let {% mathjax %} r, s \in \mathbb{R} {% endmathjax %} with {% mathjax %} r < s {% endmathjax %}. We need to show that there exists a rational number {% mathjax %} q \in \mathbb{Q} {% endmathjax %} such that {% mathjax %} r < q < s {% endmathjax %}.

## Q2. In addition to the completeness property, the Archimedean property is an important fundamentalproperty of R. It says is that if x, y ∈ {% mathjax %}\mathbb{R}{% endmathjax %} and x, y > 0, there is an n ∈ {% mathjax %}\mathbb{N}{% endmathjax %} such that nx > y.Use the Archimedean property to show that if r, s ∈ {% mathjax %}\mathbb{R}{% endmathjax %} and r < s, there is a q ∈ {% mathjax %} \mathbb{Q} {% endmathjax %} such that r < q < s.(Hint: pick n ∈ N , {% mathjax %} n > \frac{1}{s − r} {% endmathjax %}, and find an m ∈ N such that  {% mathjax %} r < \frac{m}{n} < s {% endmathjax %}.) 
**Proof:** **Step 1:** Choose {% mathjax %} n \in \mathbb{N} {% endmathjax %} such that {% mathjax %} n > \frac{1}{s - r} {% endmathjax %}.

Since {% mathjax %} s - r > 0 {% endmathjax %}, by the Archimedean property, there exists an integer {% mathjax %} n {% endmathjax %} such that:

{% mathjax %}
n > \frac{1}{s - r}.
{% endmathjax %}
**Step 2:** Conclude that {% mathjax %} \frac{1}{n} < s - r {% endmathjax %}.

Since {% mathjax %} n > \frac{1}{s - r} {% endmathjax %}, we have {% mathjax %} \frac{1}{n} < s - r {% endmathjax %}. Adding {% mathjax %} r {% endmathjax %} to both sides gives:

{% mathjax %}
r < \frac{1}{n} + r < s.
{% endmathjax %}

Therefore, it suffices to find a rational number between {% mathjax %} r {% endmathjax %} and {% mathjax %} \frac{1}{n} + r {% endmathjax %}.

**Step 3:** Find an Integer {% mathjax %} m {% endmathjax %} such that {% mathjax %} n \cdot r < m < n \cdot (r + 1) {% endmathjax %}.

Let {% mathjax %} m {% endmathjax %} be the greatest integer less than {% mathjax %} 1 + n \cdot r {% endmathjax %}. Then we have:

{% mathjax %}
n \cdot r < m < 1 + n \cdot r.
{% endmathjax %}

Dividing by {% mathjax %} n {% endmathjax %} gives:

{% mathjax %}
r < \frac{m}{n} < r + \frac{1}{n}.
{% endmathjax %}

**Step 4:** Conclude that {% mathjax %} r < \frac{m}{n} < s {% endmathjax %}.

Since {% mathjax %} \frac{1}{n} < s - r {% endmathjax %}, it follows that:

{% mathjax %}
r < \frac{m}{n} < s.
{% endmathjax %}

Thus, {% mathjax %} q = \frac{m}{n} {% endmathjax %} is a rational number such that {% mathjax %} r < q < s {% endmathjax %}.

**Conclusion:** We have shown that for any {% mathjax %} r, s \in \mathbb{R} {% endmathjax %} with {% mathjax %} r < s {% endmathjax %}, there exists a rational number {% mathjax %} q {% endmathjax %} such that {% mathjax %} r < q < s {% endmathjax %}. This completes the proof. Q.E.D.


## Q3. Formulate both in symbols and in words what it means to say that {% mathjax %} a_n {% endmathjax %} doesn't approach {% mathjax %} a {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}.

### In Symbols
{% mathjax %}
\exists \epsilon > 0 \text{s.t.} \forall m \in \mathbb{N}, \, \exists n > m |a_n - a| \geq \epsilon.
{% endmathjax %}

### In Words

This expression states that:

> There exists a positive number \( \epsilon \) such that no matter how large we choose \( m \), there will always be some \( n > m \) for which \( a_n \) is at least \( \epsilon \) away from \( a \).

In other words, the sequence \( a_n \) does not settle close to \( a \) as \( n \) grows, and there are always terms in the sequence that remain a fixed distance from \( a \), regardless of how far out in the sequence we go.

## Q4. Prove that {% mathjax %} \left( \frac{n}{n + 1} \right)^2 \to 1 {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}.
**Proof:** To prove that {% mathjax %} \left( \frac{n}{n + 1} \right)^2 \to 1 {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}, let {% mathjax %} \epsilon > 0 {% endmathjax %} be given. We need to find an {% mathjax %} n {% endmathjax %} such that for all {% mathjax %} m \geq n {% endmathjax %}, {% mathjax %} \left| \left( \frac{m}{m + 1} \right)^2 - 1 \right| < \epsilon {% endmathjax %}.

Pick an {% mathjax %} n {% endmathjax %} so large that {% mathjax %} n > \frac{2}{\epsilon} {% endmathjax %}, by the Archimedean property. Then we have:{% mathjax %}\frac{2}{n} < \epsilon.{% endmathjax %}
Now observe that:{% mathjax %}\left| \left( \frac{m}{m+1} \right)^2 - 1 \right| < \left| \left( \frac{n}{n+1} \right)^2 - 1 \right| = \frac{2n+1}{(n+1)^2}.{% endmathjax %}

Since {% mathjax %} \frac{2n+1}{(n+1)^2} < \frac{2n}{n^2} = \frac{2}{n} {% endmathjax %}, we have:{% mathjax %}\frac{2}{n} < \epsilon.{% endmathjax %}

Therefore, for all {% mathjax %} m \geq n {% endmathjax %}, {% mathjax %} \left| \left( \frac{m}{m + 1} \right)^2 - 1 \right| < \epsilon {% endmathjax %}. This completes the proof.

## Q5. Prove that {% mathjax %} \frac{1}{n^2} \to 0 {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}.
**Proof:** To prove that {% mathjax %} \frac{1}{m^2} \to 0 {% endmathjax %} as {% mathjax %} m \to \infty {% endmathjax %}, let {% mathjax %} \epsilon > 0 {% endmathjax %} be given. We need to find an {% mathjax %} n {% endmathjax %} such that for all {% mathjax %} m \geq n {% endmathjax %}, {% mathjax %} \left| \frac{1}{m^2} - 0 \right| < \epsilon {% endmathjax %}.

Choose {% mathjax %} n {% endmathjax %} so large that {% mathjax %} n > \frac{1}{\epsilon} {% endmathjax %}, by the Archimedean property. Then we have:{% mathjax %}\frac{1}{n} < \epsilon.{% endmathjax %}
Now, for any {% mathjax %} m \geq n {% endmathjax %}, we observe that:{% mathjax %}\left|\frac{1}{m^2} - 0 \right| < \left| \frac{1}{n^2} - 0 \right| = \frac{1}{n^2} < \frac{1}{n}< \epsilon.{% endmathjax %}

Therefore, for all {% mathjax %} m \geq n {% endmathjax %}, {% mathjax %} \left| \frac{1}{m^2} - 0 \right| < \epsilon {% endmathjax %}. This completes the proof.


## Q6. Prove that {% mathjax %} \frac{1}{2^n} \to 0 {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}.
**Proof:** To prove that {% mathjax %} \frac{1}{2^n} \to 0 {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}, let {% mathjax %} \epsilon > 0 {% endmathjax %} be given. We need to find an {% mathjax %} N {% endmathjax %} such that for all {% mathjax %} n \geq N {% endmathjax %}, {% mathjax %} \left| \frac{1}{2^n} - 0 \right| < \epsilon {% endmathjax %}.

Choose {% mathjax %} N {% endmathjax %} so large that {% mathjax %} N > \log_2\left(\frac{1}{\epsilon}\right) {% endmathjax %}. This can be rearranged as:{% mathjax %}2^N < \frac{1}{\epsilon}.{% endmathjax %}

Now, for any {% mathjax %} n \geq N {% endmathjax %}, we have:{% mathjax %}\frac{1}{2^n} < \frac{1}{2^N} < \epsilon.{% endmathjax %}

Thus, we conclude that for all {% mathjax %} n \geq N {% endmathjax %}, {% mathjax %} \left| \frac{1}{2^n} - 0 \right| < \epsilon {% endmathjax %}. 

This completes the proof.

## Q7. Let {% mathjax %} \{a_n\}_{n=1}^\infty {% endmathjax %} be an increasing sequence (i.e., {% mathjax %} a_n < a_{n+1} {% endmathjax %} for each {% mathjax %} n {% endmathjax %}). Suppose that {% mathjax %} a_n \to a {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}. Prove that {% mathjax %} a = \text{lub}\{a_n \mid n \in \mathbb{N}\} {% endmathjax %}.
**Proof**:Part 1: Prove That {% mathjax %} a {% endmathjax %} Is an Upper Bound of the Sequence {% mathjax %} \{a_n\} {% endmathjax %}
**Goal**: We need to prove that {% mathjax %} a_n < a {% endmathjax %} for all {% mathjax %} n \in \mathbb{N} {% endmathjax %}. This shows that {% mathjax %} a {% endmathjax %} is an upper bound of the sequence.
**Proof by Contradiction**: Assume there exists some {% mathjax %} n \in \mathbb{N} {% endmathjax %} such that:{% mathjax %} a_n \geq a {% endmathjax %}
Define:{% mathjax %} \epsilon = a_n - a \geq 0 {% endmathjax %}
**Mathematical Induction**: We need to prove that for any {% mathjax %} m \in \mathbb{N} {% endmathjax %}:{% mathjax %} a_{n+m} - a > \epsilon {% endmathjax %}
**Base Case ({% mathjax %} m = 1 {% endmathjax %})**: Since the sequence is increasing: {% mathjax %} a_{n+1} > a_n {% endmathjax %}
Subtracting {% mathjax %} a {% endmathjax %} from both sides: {% mathjax %} a_{n+1} - a > a_n - a = \epsilon {% endmathjax %}
**Inductive Step**: Assume that for some {% mathjax %} k \in \mathbb{N} {% endmathjax %}: {% mathjax %} a_{n+k} - a > \epsilon {% endmathjax %}Since the sequence is increasing:{% mathjax %} a_{n+k+1} > a_{n+k} {% endmathjax %}
Thus:{% mathjax %} a_{n+k+1} - a > a_{n+k} - a > \epsilon {% endmathjax %}
By induction, for all {% mathjax %} m \in \mathbb{N} {% endmathjax %}:{% mathjax %} a_{n+m} - a > \epsilon {% endmathjax %}
This implies that {% mathjax %} a_n {% endmathjax %} never stabilizes below or equal to {% mathjax %} a {% endmathjax %} if {% mathjax %} a_n \geq a {% endmathjax %}, which contradicts the convergence of the sequence to {% mathjax %} a {% endmathjax %}. Therefore:{% mathjax %} a_n < a \quad \text{for all } n \in \mathbb{N} {% endmathjax %}
Thus, {% mathjax %} a {% endmathjax %} is an upper bound of the sequence {% mathjax %} \{a_n\} {% endmathjax %}.
### Part 2: Prove That {% mathjax %} a {% endmathjax %} Is the Least Upper Bound (Lub) by Contradiction
**Goal**: Prove that {% mathjax %} a = \text{lub}\{a_n\} {% endmathjax %}, where lub represents the least upper bound of the sequence.
**Proof by Contradiction**:Suppose there exists some {% mathjax %} b < a {% endmathjax %} that is an upper bound for the sequence {% mathjax %} \{a_n\} {% endmathjax %}.
Since {% mathjax %} b < a {% endmathjax %}, we can define:{% mathjax %} \epsilon = a - b > 0 {% endmathjax %}
Since {% mathjax %} a_n \to a {% endmathjax %} as {% mathjax %} n \to \infty {% endmathjax %}, for sufficiently large {% mathjax %} n {% endmathjax %}, we have:{% mathjax %} |a_n - a| < \epsilon {% endmathjax %}
This implies:{% mathjax %} a - \epsilon < a_n < a {% endmathjax %}
But since {% mathjax %} \epsilon = a - b {% endmathjax %}:{% mathjax %} b < a_n < a {% endmathjax %}
This implies that, for sufficiently large {% mathjax %} n {% endmathjax %}, {% mathjax %} a_n > b {% endmathjax %}. This contradicts the assumption that {% mathjax %} b {% endmathjax %} is an upper bound for the sequence {% mathjax %} \{a_n\} {% endmathjax %}.
No number {% mathjax %} b < a {% endmathjax %} can be an upper bound of the sequence {% mathjax %} \{a_n\} {% endmathjax %}.
Thus, {% mathjax %} a {% endmathjax %} is the least upper bound (lub) of the sequence.

## Q8. Prove that if {% mathjax %} \{a_n\}_{n=1}^\infty {% endmathjax %} is increasing and bounded above, then it tends to a limit.
**Proof:** Bounded Above Implies Existence of Least Upper Bound

Let {% mathjax %} \{a_n\} {% endmathjax %} be an increasing sequence that is bounded above.  
By the **completeness property of real numbers**, the set {% mathjax %} \{a_n : n \in \mathbb{N}\} {% endmathjax %} has a least upper bound {% mathjax %} a {% endmathjax %}, such that:  {% mathjax %} a_n \leq a \quad \text{for all} \quad n \in \mathbb{N}. {% endmathjax %}  
For every {% mathjax %} \epsilon > 0 {% endmathjax %}, there exists an index {% mathjax %} m \in \mathbb{N} {% endmathjax %} such that:  {% mathjax %} a_m > a - \epsilon.{% endmathjax %}

Convergence of {% mathjax %} \{a_n\} {% endmathjax %} to {% mathjax %} a {% endmathjax %}:Since {% mathjax %} \{a_n\} {% endmathjax %} is an increasing sequence, for any {% mathjax %} n \geq m {% endmathjax %}, we have:  {% mathjax %} a_m \leq a_n \leq a. {% endmathjax %}  
Therefore,  {% mathjax %} a - a_n \leq a - a_m. {% endmathjax %}  
Given that {% mathjax %} a_m > a - \epsilon {% endmathjax %}, it follows that:  {% mathjax %} a - a_m < \epsilon.{% endmathjax %}  
Thus, for {% mathjax %} n \geq m {% endmathjax %}:  {% mathjax %} |a_n - a| = a - a_n < a - a_m < \epsilon.{% endmathjax %}
Conclusion:For any {% mathjax %} \epsilon > 0 {% endmathjax %}, there exists {% mathjax %} m \in \mathbb{N} {% endmathjax %} such that for all {% mathjax %} n \geq m {% endmathjax %}: {% mathjax %} |a_n - a| < \epsilon.{% endmathjax %}  
Hence, {% mathjax %} \{a_n\} {% endmathjax %} converges to {% mathjax %} a {% endmathjax %}.



