---
title: 'Test Flight Problem Set'
date: 2025-01-26 15:14:45
tags: "notes"
katex: true
mathjax: true
---
**1. Say whether the following is true or false and support your answer by a proof {% mathjax%}(∃m ∈ \mathbb{N})(∃n ∈ \mathbb{N})(3m + 5n = 12){% endmathjax %}**
**Answer**: The statement is **false**. There do not exist natural numbers {% mathjax %} m {% endmathjax %} and {% mathjax %} n {% endmathjax %} such that {% mathjax %} 3m + 5n = 12 {% endmathjax %}.  

**Proof**:  
Assume for contradiction that {% mathjax %} \exists m, n \in \mathbb{N} {% endmathjax %} (where {% mathjax %} \mathbb{N} = \{1, 2, 3, \ldots\} {% endmathjax %}) satisfying {% mathjax %} 3m + 5n = 12 {% endmathjax %}. Rewrite the equation as:  
{% mathjax %}  
3(m + n) + 2n = 12.  
{% endmathjax %}  
Let {% mathjax %} x = 3(m + n) {% endmathjax %} and {% mathjax %} y = 2n {% endmathjax %}. Then {% mathjax %} x + y = 12 {% endmathjax %}. Since {% mathjax %} m, n \geq 1 {% endmathjax %}, we derive:  
{% mathjax %}  
x \geq 6 \quad \text{and} \quad y \geq 2.  
{% endmathjax %}  
Suppose {% mathjax %} x = 6 + k {% endmathjax %} and {% mathjax %} y = 6 - k {% endmathjax %} for some integer {% mathjax %} k \geq 0 {% endmathjax %}. Substituting back:  
1. {% mathjax %} 3(m + n) = 6 + k \implies m + n = 2 + \frac{k}{3} {% endmathjax %}.  
2. {% mathjax %} 2n = 6 - k \implies n = 3 - \frac{k}{2} {% endmathjax %}.  

For {% mathjax %} n \in \mathbb{N} {% endmathjax %}, {% mathjax %} k {% endmathjax %} must be even **and** a multiple of {% mathjax %} 3 {% endmathjax %}, so {% mathjax %} k {% endmathjax %} is a multiple of {% mathjax %} 6 {% endmathjax %}. 
Testing {% mathjax %} k = 0 {% endmathjax %}:  
- {% mathjax %} n = 3, m = -1 {% endmathjax %} (invalid).  

For {% mathjax %} k = 6 {% endmathjax %}:  
- {% mathjax %} n = 0 {% endmathjax %} (invalid).  

No valid {% mathjax %} k {% endmathjax %} exists. **Conclusion**: The equation has no solutions in {% mathjax %} \mathbb{N} {% endmathjax %}.  

**2. Say whether the following is true or false and support your answer by a proof: The sum of any five consecutive integers is divisible by 5 (without remainder).**
**Answer**: The statement is **true**.  

**Proof by Induction**:  

**Base Case ({% mathjax %} n=0 {% endmathjax %}):** Consider the five consecutive integers starting at {% mathjax %} 0 {% endmathjax %}:  {% mathjax %} 0 + 1 + 2 + 3 + 4 = 10.{% endmathjax %} Since {% mathjax %} 10 {% endmathjax %} is divisible by {% mathjax %} 5 {% endmathjax %} ({% mathjax %} 10 = 5 \times 2 {% endmathjax %}), the base case holds.  

**Inductive Hypothesis:**  Assume that for some integer {% mathjax %} k {% endmathjax %}, the sum of five consecutive integers starting at {% mathjax %} k {% endmathjax %} is divisible by {% mathjax %} 5 {% endmathjax %}. That is: {% mathjax %} k + (k+1) + (k+2) + (k+3) + (k+4) = 5m {% endmathjax %}, where {% mathjax %} m {% endmathjax %} is an integer.  

**Inductive Step ({% mathjax %} k \to k+1 {% endmathjax %}):**  We need to show that the sum of the next five consecutive integers, starting at {% mathjax %} k+1 {% endmathjax %}, is also divisible by {% mathjax %} 5 {% endmathjax %}. Consider: {% mathjax %} (k+1) + (k+2) + (k+3) + (k+4) + (k+5). {% endmathjax %} Simplify the sum: {% mathjax %} (k+1) + (k+2) + (k+3) + (k+4) + (k+5) = (k + k+1 + k+2 + k+3 + k+4) + 5.{% endmathjax %} From the inductive hypothesis, we know:  {% mathjax %} k + (k+1) + (k+2) + (k+3) + (k+4) = 5m.{% endmathjax %} Thus, the sum becomes:  {% mathjax %} 5m + 5 = 5(m + 1).{% endmathjax %} Since {% mathjax %} m + 1 {% endmathjax %} is an integer, {% mathjax %} 5(m + 1) {% endmathjax %} is divisible by {% mathjax %} 5 {% endmathjax %}.  

**Conclusion:** By induction, the sum of any five consecutive integers is divisible by {% mathjax %} 5 {% endmathjax %}.  


**3. For any integer n, consider the expression {% mathjax %} n^2 + n + 1.{% endmathjax %}**
**Answer**: The statement is **true**.  
**Proof by Induction** (for non-negative integers {% mathjax %} n {% endmathjax %}):  
1. **Base Case**: {% mathjax %} n = 0 {% endmathjax %}:  
   {% mathjax %} 0^2 + 0 + 1 = 1 \quad (\text{odd}). {% endmathjax %}  
2. **Inductive Step**: Assume {% mathjax %} n^2 + n + 1 {% endmathjax %} is odd for some integer {% mathjax %} n \geq 0 {% endmathjax %}. For {% mathjax %} n + 1 {% endmathjax %}:  
   {% mathjax %} (n+1)^2+(n+1)+1=n^2+3n+3=(n^2+n+1)+2(n+1) \quad (\text{odd}). {% endmathjax %}  
   By hypothesis, {% mathjax %} n^2 + n + 1 {% endmathjax %} is odd, and {% mathjax %} 2(n + 1) {% endmathjax %} is even.  
   **Odd + Even = Odd**, so {% mathjax %} (n + 1)^2 + (n + 1) + 1 {% endmathjax %} is odd.  
By induction, the statement holds for all {% mathjax %} n \geq 0 {% endmathjax %}. For negative integers, parity (even/odd) is preserved, so the case analysis above suffices.  

**Conclusion**: The statement is **true** for all integers {% mathjax %} n {% endmathjax %}.  

**4. Prove that every odd natural number is of one of the forms 4n + 1 or 4n + 3, where n is an integer.**
**Proof:** We aim to show that every odd natural number is of one of the forms {% mathjax %} 4n+1 {% endmathjax %} or {% mathjax %} 4n+3 {% endmathjax %}, where n is an integer.

By the **Division Algorithm** (or Remainder Theorem), for any integer a and a positive integer b = 4, there exist unique integers q and r such that:  {% mathjax %} a = 4q + r, \quad \text{where } 0 \leq r < 4. {% endmathjax %}  

Here, r is the remainder when a is divided by 4, and r can take one of the values 0, 1, 2, or 3.

Now, consider the possible cases for r:

1. **Case r = 0:**  {% mathjax %} a = 4q + 0 = 4q. {% endmathjax %}  
This is an even number because it is divisible by 2.

2. **Case r = 1:**  {% mathjax %} a = 4q + 1. {% endmathjax %}  
This is an odd number because it is not divisible by 2.

3. **Case r = 2:**  {% mathjax %} a = 4q + 2 = 2(2q + 1). {% endmathjax %}  
This is an even number because it is divisible by 2.

4. **Case r = 3:**  {% mathjax %} a = 4q + 3. {% endmathjax %}  
This is an odd number because it is not divisible by 2.

Since a is an odd natural number, it cannot be of the form {% mathjax %} 4q {% endmathjax %} or {% mathjax %} 4q+2 {% endmathjax %} (as these are even). Therefore, a must be of one of the forms: {% mathjax %} a = 4q+1 \quad \text{or} \quad a = 4q+3. {% endmathjax %}  

Letting n = q, we conclude that every odd natural number is of one of the forms {% mathjax %} 4n+1 {% endmathjax %} or {% mathjax %} 4n+3 {% endmathjax %}, where n is an integer.

**QED**



**5. Prove that for any integer n, at least one of the integers n, n + 2, n + 4 is divisible by 3.**
**Proof:** We aim to prove that for any integer n, at least one of the integers n, n+2, or n+4 is divisible by 3.

By the **Division Algorithm**, any integer n can be expressed as:  
{% mathjax %} n \equiv 0 \pmod{3}, \quad n \equiv 1 \pmod{3}, \quad \text{or} \quad n \equiv 2 \pmod{3}. {% endmathjax %}  

- If {% mathjax %} n \equiv 0 \pmod{3} {% endmathjax %}, then n is divisible by 3.  
- If {% mathjax %} n \equiv 1 \pmod{3} {% endmathjax %}, then:  
  {% mathjax %} n+2 \equiv 1+2 \equiv 3 \equiv 0 \pmod{3}, {% endmathjax %}  
  so n+2 is divisible by 3.  
- If {% mathjax %} n \equiv 2 \pmod{3} {% endmathjax %}, then:  
  {% mathjax %} n+4 \equiv 2+4 \equiv 6 \equiv 0 \pmod{3}, {% endmathjax %}  
  so n+4 is divisible by 3.

In each case, at least one of the integers n, n+2, or n+4 is divisible by 3.

**Conclusion:** For any integer n, at least one of the integers n, n+2, or n+4 is divisible by 3.

**QED**

**6. A classic unsolved problem in number theory asks if there are infinitely many pairs of ‘twin primes’, pairs of primes separated by 2, such as 3 and 5, 11 and 13, or 71 and 73. Prove that the only prime triple (i.e. three primes, each 2 from the next) is 3, 5, 7.**
**Proof**: Assume, for contradiction, that there exists an integer n>3 such that n, n + 2, and n+4 are all prime.

For any integer n, it must satisfy one of the following modulo 3:
- {% mathjax %}n\equiv0\pmod{3}{% endmathjax %}
- {% mathjax %}n\equiv1\pmod{3}{% endmathjax %}
- {% mathjax %}n\equiv2\pmod{3}{% endmathjax %}

Analyzing each case:
1. If {% mathjax %}n\equiv0\pmod{3}{% endmathjax %}, then n is divisible by 3.
2. If {% mathjax %}n\equiv1\pmod{3}{% endmathjax %}, then {% mathjax %} n + 2\equiv1 + 2 = 3\equiv0\pmod{3} {% endmathjax %}, so n + 2 is divisible by 3.
3. If {% mathjax %}n\equiv2\pmod{3}{% endmathjax %}, then {% mathjax %} n+4\equiv2 + 4 = 6\equiv0\pmod{3} {% endmathjax %}, so n + 4 is divisible by 3.

Thus, one of n, n + 2, or n+4 must be divisible by 3. Since n>3, this number would be greater than 3 and therefore composite (as primes divisible by 3 must equal 3). This contradicts the assumption that all three numbers are prime.

Hence, no such n>3 exists. The only valid prime triple is \(3, 5, 7\).

QED

**7. Prove that for any natural number, {% mathjax %}2 + 2^{2}+2^{3}+\cdots+2^{n}=2^{n + 1}-2{% endmathjax %}**
**Proof by Mathematical Induction:**
We aim to prove that for any natural number n:{% mathjax %}2 + 2^{2}+2^{3}+\cdots + 2^{n}=2^{n + 1}-2{% endmathjax %}

For n = 1:{% mathjax %}2 = 2^{1 + 1}-2 = 2^{2}-2 = 4 - 2 = 2{% endmathjax %}

Thus, the formula holds for n = 1.

Assume that the formula holds for some arbitrary k:{% mathjax %}2 + 2^{2}+2^{3}+\cdots + 2^{k}=2^{k + 1}-2{% endmathjax %}

We need to show that the formula holds for k + 1, i.e.,{% mathjax %}2 + 2^{2}+2^{3}+\cdots + 2^{k}+2^{k + 1}=2^{(k + 1)+1}-2{% endmathjax %}

Using the inductive hypothesis:{% mathjax %}(2 + 2^{2}+2^{3}+\cdots + 2^{k})+2^{k + 1}=(2^{k + 1}-2)+2^{k + 1}{% endmathjax %}

Simplifying:{% mathjax %}2^{k + 1}-2 + 2^{k + 1}=2^{k + 1}+2^{k + 1}-2 = 2\cdot2^{k + 1}-2 = 2^{k + 2}-2{% endmathjax %} which is exactly the desired formula for k + 1.

**Conclusion**

By the principle of mathematical induction, the formula{% mathjax %}2 + 2^{2}+2^{3}+\cdots + 2^{n}=2^{n + 1}-2{% endmathjax %} holds for all natural numbers n.

**QED**

**8. Prove (from the definition of a limit of a sequence) that if the sequence {% mathjax %} \{a_n\}_{n = 1}^{\infty}{% endmathjax %} tends to limit L as {% mathjax %}n\to \infty{% endmathjax %}, then for any fixed number M>0, the sequence {% mathjax %}\{Ma_n\}_{n = 1}^{\infty}{% endmathjax %} tends to the limit .**
**Proof:**  

*Using the definition of a limit, we will show that if {% mathjax %}\lim_{n \to \infty} a_n = L{% endmathjax %}, then {% mathjax %}\lim_{n \to \infty} (M a_n) = M L{% endmathjax %} for any fixed constant {% mathjax %}M{% endmathjax %}.*  

By the definition of convergence, for every {% mathjax %}\varepsilon > 0{% endmathjax %}, there exists a natural number {% mathjax %}N{% endmathjax %} such that for all {% mathjax %}n \geq N{% endmathjax %}:  

{% mathjax %}  
|a_n - L| < \varepsilon.  
{% endmathjax %}  

To prove {% mathjax %}\lim_{n \to \infty} (M a_n) = M L{% endmathjax %}, we need to show that for every {% mathjax %}\varepsilon' > 0{% endmathjax %}, there exists {% mathjax %}N'{% endmathjax %} such that for all {% mathjax %}n \geq N'{% endmathjax %}:  

{% mathjax %}  
|M a_n - M L| < \varepsilon'.  
{% endmathjax %}  

Factor out {% mathjax %}M{% endmathjax %}:  

{% mathjax %}  
|M a_n - M L| = |M| \cdot |a_n - L|.  
{% endmathjax %}  

Let {% mathjax %}\varepsilon = \frac{\varepsilon'}{|M|}{% endmathjax %} (if {% mathjax %}M \neq 0{% endmathjax %}).  
From the assumption, there exists {% mathjax %}N{% endmathjax %} such that for all {% mathjax %}n \geq N{% endmathjax %}:  

{% mathjax %}  
|a_n - L| < \varepsilon = \frac{\varepsilon'}{|M|}.  
{% endmathjax %}  

Multiply both sides by {% mathjax %}|M|{% endmathjax %}:  

{% mathjax %}  
|M| \cdot |a_n - L| < |M| \cdot \frac{\varepsilon'}{|M|} \implies |M a_n - M L| < \varepsilon'.  
{% endmathjax %}  

Thus, for {% mathjax %}n \geq N{% endmathjax %}, {% mathjax %}|M a_n - M L| < \varepsilon'{% endmathjax %}.  

For any fixed {% mathjax %}M{% endmathjax %}, the sequence {% mathjax %}\{M a_n\}{% endmathjax %} converges to {% mathjax %}M L{% endmathjax %}. Therefore:  

{% mathjax %}  
\lim_{n \to \infty} (M a_n) = M \cdot \lim_{n \to \infty} a_n = M L.  
{% endmathjax %}  

**QED**

**9. Given an infinite collection {% mathjax %}A_n{% endmathjax %}, {% mathjax %}n = 1, 2, \ldots{% endmathjax %} of intervals of the real line, their intersection is defined to be {% mathjax %}\bigcap_{n = 1}^{\infty}A_n=\{x|(\forall n)(x\in A_n)\}{% endmathjax %} Give an example of a family of intervals {% mathjax %}A_n{% endmathjax %}, \(n = 1, 2, {% mathjax %}\ldots{% endmathjax %}\), such that {% mathjax %}A_{n + 1}\subset A_n{% endmathjax %} for all n and {% mathjax %}\bigcap_{n = 1}^{\infty}A_n=\varnothing {% endmathjax %} Prove that your example has the stated property.**
**Proof:** We consider the sequence of nested open intervals:  
{% mathjax %} A_n = \left( 0, \frac{1}{n} \right) {% endmathjax %} for {% mathjax %} n = 1, 2, 3, \dots {% endmathjax %}.  

We need to show that {% mathjax %} A_{n+1} \subset A_n {% endmathjax %} for all {% mathjax %} n {% endmathjax %}.  

Since {% mathjax %} A_n = \left( 0, \frac{1}{n} \right) {% endmathjax %}, we have:  
{% mathjax %} A_{n+1} = \left( 0, \frac{1}{n+1} \right). {% endmathjax %}  

Since {% mathjax %} 0 < \frac{1}{n+1} < \frac{1}{n} {% endmathjax %} for all {% mathjax %} n {% endmathjax %}, every element in {% mathjax %} A_{n+1} {% endmathjax %} is also in {% mathjax %} A_n {% endmathjax %}. Thus, {% mathjax %} A_{n+1} \subset A_n {% endmathjax %}.  

By definition,  
{% mathjax %} \bigcap_{n=1}^{\infty} A_n = \{ x \mid (\forall n)(x \in A_n) \}. {% endmathjax %}  

For any {% mathjax %} x \in \bigcap_{n=1}^{\infty} A_n {% endmathjax %}, we must have {% mathjax %} x \in A_n {% endmathjax %} for all {% mathjax %} n {% endmathjax %}. This means:  
{% mathjax %} 0 < x < \frac{1}{n}, {% endmathjax %} for all {% mathjax %} n {% endmathjax %}.  

Taking the limit as {% mathjax %} n \to \infty {% endmathjax %}, we see that {% mathjax %} \frac{1}{n} \to 0 {% endmathjax %}, so any {% mathjax %} x {% endmathjax %} in the intersection must satisfy {% mathjax %} 0 < x < 0 {% endmathjax %}, which is impossible.

Thus,  
{% mathjax %} \bigcap_{n=1}^{\infty} A_n = \emptyset. {% endmathjax %}  

The given sequence of intervals satisfies the required conditions, proving that their intersection is empty.

**10. Give an example of a family of intervals {% mathjax %}{% endmathjax %}, {% mathjax %}n = 1, 2, \cdots{% endmathjax %}, such that {% mathjax %}A_{n + 1}\subset A_n{% endmathjax %} for all {% mathjax %}n{% endmathjax %} and {% mathjax %}\bigcap_{n = 1}^{\infty}A_n {% endmathjax %} consists of a single real number. Prove that your example has the stated property.**
**Proof:** Consider the sequence of closed intervals:  
{% mathjax %} A_n = \left[ 0, \frac{1}{n} \right] {% endmathjax %} for {% mathjax %} n = 1, 2, 3, \dots {% endmathjax %}.  

We first verify that {% mathjax %} A_{n+1} \subset A_n {% endmathjax %}. Since  
{% mathjax %} A_n = \left[ 0, \frac{1}{n} \right] {% endmathjax %} and {% mathjax %} A_{n+1} = \left[ 0, \frac{1}{n+1} \right] {% endmathjax %}, we have  
{% mathjax %} 0 \leq x \leq \frac{1}{n+1} {% endmathjax %} implies {% mathjax %} 0 \leq x \leq \frac{1}{n} {% endmathjax %},  
so every element in {% mathjax %} A_{n+1} {% endmathjax %} is also in {% mathjax %} A_n {% endmathjax %}, proving {% mathjax %} A_{n+1} \subset A_n {% endmathjax %}.  

Now, we compute the intersection:  
{% mathjax %} \bigcap_{n=1}^{\infty} A_n = \{ x \mid (\forall n)(x \in A_n) \}. {% endmathjax %}  

For any {% mathjax %} x \in \bigcap_{n=1}^{\infty} A_n {% endmathjax %}, we must have  
{% mathjax %} 0 \leq x \leq \frac{1}{n} {% endmathjax %} for all {% mathjax %} n {% endmathjax %}.  

Taking the limit as {% mathjax %} n \to \infty {% endmathjax %}, we see that {% mathjax %} \frac{1}{n} \to 0 {% endmathjax %}, meaning that the only possible value for {% mathjax %} x {% endmathjax %} is 0.  

Thus,  
{% mathjax %} \bigcap_{n=1}^{\infty} A_n = \{ 0 \}. {% endmathjax %}  

This proves that the intersection consists of the single real number 0.