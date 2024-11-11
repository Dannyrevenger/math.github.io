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



同学们大家好，欢迎来到今天的数学课堂。我是来自静安区教育学院附属学校的厉老师。前几节课，我们已经学习了因式分解的意义，以及**提取公因式法、公式法和十字相乘法**这三种因式分解的方法。我们知道公式法和十字相乘法主要适用于二项式和三项式。而今天，我们将重点研究**如何对四项式进行因式分解**。

请同学们首先思考这个问题：如何将 {% mathjax %} AX + AY + BX + BY {% endmathjax %} 进行因式分解？我们一起观察分析一下这个四项式的特征。可以发现，这个四项式有四项，且没有公因式。显然，之前学过的**提取公因式法、公式法和十字相乘法**都不适用，因而我们遇到了一些困难。

在解决这个问题之前，我们先来看一个类似的表达式：
{% mathjax %}
A \cdot (X + Y) + B \cdot (X + Y)
{% endmathjax %}
这个表达式存在公因式 {% mathjax %} (X + Y) {% endmathjax %}，我们可以使用**提取公因式法**来进行因式分解。同学们一定能够轻松解决这个问题。

那么请大家再观察一下这两个表达式之间的关系。你会发现，如果将第二个表达式乘展开，就得到了第一个四项式。它们本质上是相同的表达式。现在，同学们是否能够因式分解 {% mathjax %} AX + AY + BX + BY {% endmathjax %} 了呢？我们可以发现，这个整式的**前两项**都有字母 {% mathjax %} A {% endmathjax %}，而**后两项**都有字母 {% mathjax %} B {% endmathjax %}。我们可以把前两项分为一组，后两项分为一组，利用加法结合律，从第一组中提取公因式 {% mathjax %} A {% endmathjax %}，得到 {% mathjax %} A(X + Y) {% endmathjax %}；从第二组中提取公因式 {% mathjax %} B {% endmathjax %}，得到 {% mathjax %} B(X + Y) {% endmathjax %}。这样一来，我们形成了新的公因式 {% mathjax %} (X + Y) {% endmathjax %}。将它提取出来，最后就得到了：
{% mathjax %}
A(X + Y) + B(X + Y) = (A + B)(X + Y)
{% endmathjax %}
这样，因式分解就完成了。

回顾一下这个问题的解决过程：一开始，这个四项式没有公因式，但通过**分组**，我们成功地找到了新的公因式 {% mathjax %} (X + Y) {% endmathjax %}，进而完成了因式分解。这让我们体会到，**分组法**结合**提取公因式法**是解决类似问题的有效手段。

既然分组的方法非常有效，我们继续深入学习。接下来我们思考一个新的问题：**该如何进行合理的分组**？

例如，我们有一个式子：{% mathjax %} -2X + 6Y - 4X + 12Y {% endmathjax %}。我们可以将第一项和第三项进行分组，同时将第二项和第四项进行分组，分别提取公因式：从第一组中提取公因式 {% mathjax %} -2 {% endmathjax %}，得到 {% mathjax %} -2(X + 3Y) {% endmathjax %}；第二组中提取 {% mathjax %} -4 {% endmathjax %}，也得到了 {% mathjax %} -4(X + 3Y) {% endmathjax %}。于是，我们又有了新的公因式 {% mathjax %} (X + 3Y) {% endmathjax %}，最终因式分解为：
{% mathjax %}
(X + 3Y)(-2 - 4)
{% endmathjax %}

接下来，请同学们思考另一个四项式：{% mathjax %} A^2 + 2AB + B^2 - 1 {% endmathjax %}。我们首先观察它的特征。这又是一个四项式，且没有公因式。提取公因式法、公式法和十字相乘法似乎都不适用。是不是有同学已经开始尝试**两项两项分组**了呢？有什么发现吗？对，通过两项两项分组，无法形成新的公因式，因此我们需要换一种思路。

我们可以观察到，前三项 {% mathjax %} A^2 + 2AB + B^2 {% endmathjax %} 正好符合**完全平方公式**的特征，可以将它们归为一组，形成 {% mathjax %} (A + B)^2 {% endmathjax %}；而最后的一项是 {% mathjax %} -1 {% endmathjax %}，这个表达式整体上又符合**平方差公式**的特征：
{% mathjax %}
(A + B)^2 - 1 = (A + B - 1)(A + B + 1)
{% endmathjax %}

因此，我们通过分组和公式法相结合，成功将这个四项式因式分解。

回顾这个问题的解决过程，一开始这个四项式没有公因式，也不符合任何公式的特征，但**分组**起到了非常关键的作用。不过这里的分组不是简单的两项两项分组，而是将前三项分为一组，最后的一项单独一组。这三项恰好满足完全平方公式的特征，而剩下的一项组合在一起则满足平方差公式的特征。通过分组法和公式法结合，我们成功解决了问题。

对于项数较多的多项式进行因式分解，**分组**是一个很好的策略。但分组必须合理，必须基于整式的特征。通过今天的学习，我们知道四项式可以**两项两项分组**，也可以**三项和一项分组**。我们需要从整式的特征出发，合理选择分组方法。

那么，同学们思考一下，本题还有其他的分组方法吗？你可以尝试将前三项与最后一项单独分组，或者寻找其他合理的分组方式。希望大家通过练习，不断提升因式分解的技能！

