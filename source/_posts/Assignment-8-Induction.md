---
title: 'Assignment 8: Induction'
date: 2024-07-18 15:14:45
tags:
katex: true
mathjax: true
---
**1. Prove or disprove the claim that there are integers m, n such that {% mathjax %} m^2 + mn + n^2 {% endmathjax %} is a perfect square.**
Proof: Let n = 0. Then {% mathjax %} m^2 + mn + n^2 = m^2 {% endmathjax %}. And {% mathjax %} m^2 {% endmathjax %} is a perfect square. Q.E.D

**2. Prove or disprove the claim that for any positive integer m there is a positive integer n such that {% mathjax %} mn + 1 {% endmathjax %}is a perfect square.**
Proof: For any positive integer m, let n=m+2, then {% mathjax %} mn +1= m(m+2)+1=m^2+2m+1=(m+1)^2 {% endmathjax %}. And {% mathjax %} (m+1)^2 {% endmathjax %} is a perfect square. Q.E.D

**3. Prove that there is a quadratic {% mathjax %} f(n) = n^2 + bn + c {% endmathjax %}, with positive integers coefficients b, c, such that f(n) is composite (i.e, not prime) for all positive integers n, or else prove that the statement is false.**
Proof: Let b=2 and c=1. Then {% mathjax %} f(n) = n^2 + bn + c = n^2 + 2n + 1 = (n+1)^2 {% endmathjax %}. And {% mathjax %} (n+1)^2 \geq 4 {% endmathjax %} and {% mathjax %} (n+1)^2 {% endmathjax %}is composite for all positive integers n. Q.E.D

**4. Prove that if every even natural number greater than 2 is a sum of two primes (the Goldbach Conjecture), then every odd natural number greater than 5 is a sum of three primes.**
Proof: {% mathjax %} \forall k_1 \in \mathbb{N} \land k_1>1 \exists p,q \in \mathbb{P}, 2k_1=p+q => 2(k_1+1)+1=2k_1+3=p+q+3. {% endmathjax %} And since {% mathjax %} k_1>1 {% endmathjax %}, so {% mathjax %} 2(k_1+1)+1>5 {% endmathjax %}. And {% mathjax %} 2(k_1+1)+1 {% endmathjax %}is odd for all natural numbers . Let {% mathjax %} k_2 = k_1 +1 {% endmathjax %}. Then we can get {% mathjax %} \forall k_2 \in \mathbb{N} \land k_2>2 \exists p,q \in \mathbb{P}, 2k_2+1=p+q {% endmathjax %}. So now we have proven "if every even natural number greater than 2 is a su m of two primes, then every odd natural number greater than 5 is a sum of three primes."


**5. Use the method of induction to prove that the sum of the first n odd numbers is equal to {% mathjax %} n^2 {% endmathjax %}.**
Proof: We need to prove {% mathjax %} \forall k \in \mathbb Z_{> 0}, \sum_{1}^{k}(2k+1)=(k+1)^2 {% endmathjax %} by induction.
For k=0, the left-hand side is 1 and the right-hand side is {% mathjax %} (1+0)^2=1 {% endmathjax %}, so the identity is valid for k=0.
Assume the identity holds for k. So {% mathjax %} \sum_{1}^{k}(2k+1)=(k+1)^2 {% endmathjax %}. Now we need to show show that {% mathjax %} \sum_{1}^{k+1}(2k+1)=(k+2)^2 {% endmathjax %}. We split the {% mathjax %} \sum_{1}^{k+1}(2k+1) {% endmathjax %} into two sections i.e. {% mathjax %} \sum_{1}^{k+1}(2k+1)= \sum_{1}^{k}(2k+1) + [2(k+1)+1] {% endmathjax %}. And by our assumption, we can get {% mathjax %} \sum_{1}^{k}(2k+1) + [2(k+1)+1] = (k+1)^2 + [2(k+1)+1] {% endmathjax %}. It's trivial to get {% mathjax %} (k+1)^2 + [2(k+1)+1] = (k+2)^2 {% endmathjax %}. This is the identity for k+1. Hence, by induction, the theorem is proved.

**6. The notation {% mathjax %} \sum_{i=1}^{n}(a_1) {% endmathjax %} is a common abbreviation for the sum {% mathjax %} a_1+a_2+a_3+...+a_n	{% endmathjax %}. For instance, {% mathjax %} \sum_{r=1}^{n}(r^2) {% endmathjax %}, denotes the sum {% mathjax %} 1^2+2^2+3^2+...+n^2 {% endmathjax %}. Prove by induction that: {% mathjax %} \forall n \in \mathbb{N}: \sum_{r=1}^{n}(r^2)=\frac{1}{6}n(n+1)(2n+1) {% endmathjax %}**
Proof: By induction.
For n=1, the left-hand side is 1 and the right-hand side is {% mathjax %} \frac{1}{6}1(1+1)(2+1)=1 {% endmathjax %}, so the identity is valid for n=1.
Assume the identity holds for n. So {% mathjax %} \sum_{r=1}^{n}(r^2)=\frac{1}{6}n(n+1)(2n+1) {% endmathjax %}. Now we need to show show that {% mathjax %} \sum_{r=1}^{n+1}(r^2)=\frac{1}{6}(n+1)[(n+1)+1][2(n+1)+1] {% endmathjax %}. We split the {% mathjax %} \sum_{r=1}^{n+1}(r^2) {% endmathjax %} into two sections i.e. {% mathjax %} \sum_{r=1}^{n+1}(r^2)= \sum_{r=1}^{n}(r^2) + (n+1)^2 {% endmathjax %}. And by our assumption, we can get {% mathjax %} \sum_{r=1}^{n}(r^2) + (n+1)^2 = \frac{1}{6}n(n+1)(2n+1) + (n+1)^2 {% endmathjax %}. It's trivial to get {% mathjax %} \frac{1}{6}n(n+1)(2n+1) + (n+1)^2 =  \frac{n(n+1)(2n+1)}{6} + \frac{6(n+1)^2}{6} {% endmathjax %}. By addition of fractions, we can get {% mathjax %} \frac{(n+1)[n(2n+1)+6(n+1)]}{6} {% endmathjax %}. By combining like terms, we can get {% mathjax %} \frac{(n+1)(2n^2+7n+6)}{6} {% endmathjax %}. Finally by factorization, we can get {% mathjax %} \frac{(n+1)(2n+3)(n+2)}{6} {% endmathjax %}. This is the identity for n+1. Hence, by induction, the theorem is proved.

## OPTIONAL PROBLEMS
**1. In the lecture we used induction to prove the general theorem**
      <div align="center"> 
        {% katex %}
          1 + 2 + . . . + n = \frac{1}{2}n(n + 1)
        {% endkatex %}
      </div>
      **There is an alternative proof that does not use induction, famous because Gauss used the key idea to solve a “busywork” arithmetic problem his teacher gave to the class when he was a small child at school. The teacher asked the class to calculate the sum of the first hundred natural numbers. Gauss noted that if**
      <div align="center"> 
        {% katex %}
          1 + 2 + . . . + 100 = N
        {% endkatex %} 
      </div>
      **then you can reverse the order of the addition and the answer will be the same:**
      <div align="center"> 
        {% katex %}
          100 + 99 + . . . + 1 = N.
        {% endkatex %}
      </div>
      **So by adding those two equations, you get**
      <div align="center"> 
        {% katex %}
          101 + 101 + . . . + 101 = 2N
        {% endkatex %}
      </div>
      **and since there are 100 terms in the sum, this can be written as**
      <div align="center"> 
        {% katex %}
          100 · 101 = 2N
        {% endkatex %}
      </div>
      **and hence**
      <div align="center"> 
        {% katex %}
          N = \frac{1}{2} (100 · 101) = 5, 050.
        {% endkatex %}
      </div>
      **Generalize Gauss’s idea to prove the theorem without recourse to the method of induction.**
Proof: Assume that {% mathjax %} S = 1 + 2 + . . . + n {% endmathjax %}. Then we can get {% mathjax %} n + (n-1) + . . . + 1 = S {% endmathjax %}. So by adding those two equations, we can get {% mathjax %}(n+1)+(n+1)+ . . . + (n+1) = 2S {% endmathjax %}. and since there are n terms in the sum, this can be written as {% mathjax %} n(n+1) = 2S {% endmathjax %} and hence {% mathjax %} S = = \frac{1}{2}n(n+1) {% endmathjax %}

**2. Prove that for any finite collection of points in the plane, not all collinear, there is a triangle having three of the points as its vertices, which contains none of the other points in its interior.**
Proof: By contradiction.
Assume that for any finite collection of points in the plane, not all collinear, every triangle having three of the points as its vertices contain at least one point in its interior. Now we can easily construct a counterexample to our assumption. We construct a triangle having three vertices labeled A, B, and C, and a point D in its interior. ![](/img/A8O2.jpg) Now we connect the point D and the point A, and at the same time, we connect the point D and the point C. After that, we get a new triangle with three vertices A, D, and C. But there is no points inside the new triangle which contradicts to our assumption. And hence our assumption is false. Therefore the original statement is true.


**3. Prove the following by induction:**
  **(a) {% mathjax %} 4^n − 1 {% endmathjax %}is divisible by 3.**
    Proof: We need to prove that {% mathjax %}  \forall n \in \mathbb{N}, 3|(4^n-1) {% endmathjax %} by induction.
    For n=1, {% mathjax %} 4^1-1=3 {% endmathjax %} which is divisible by 3, so the identity is valid for n=1.
    Assume the identity holds for n. So {% mathjax %} 3|(4^n − 1) {% endmathjax %}. Now we need to show show that {% mathjax %} 3|(4^(n+1)-1) {% endmathjax %}. We split the {% mathjax %} (4^(n+1)-1) {% endmathjax %} into two sections i.e. {% mathjax %} (4^(n+1)-1)= 4\times(4^(n)-1)+3 {% endmathjax %}. And by our assumption, we can get {% mathjax %} 3|(4^n − 1) {% endmathjax %}. It's trivial to get {% mathjax %} 3|[4\times(4^(n)-1)+3] {% endmathjax %}. For n+1, {% mathjax %} 3|(4^(n+1)-1) {% endmathjax %}. Hence, by induction, the theorem is proved.

  **(b) {% mathjax %} (n + 1)! > 2^{n+3} {% endmathjax %}for all n ≥ 5.**
    Proof: By induction.
    For n=5, the left-hand side is 720 and the right-hand side is 256, so the inequality is valid for n=5.
    Assume the identity holds for n. So {% mathjax %} (n + 1)! > 2^{n+3} {% endmathjax %}. Now we need to show show that {% mathjax %} [(n + 1)+1]! > 2^{[(n+1)+3]} {% endmathjax %}. We split the {% mathjax %} [(n + 1)+1]! {% endmathjax %} into two sections i.e. {% mathjax %} [(n + 1)+1]! = (n + 1)!\times(n+2) {% endmathjax %}. And by our assumption, we can get {% mathjax %} (n + 1)!\times(n+2) > 2^{n+3}\times(n+2) {% endmathjax %}. And since {% mathjax %} (n+2) \geq 7 {% endmathjax %}, so {% mathjax %} (n+2) > 2 {% endmathjax %}. So we can get {% mathjax %} (n + 1)!\times(n+2) > 2^{n+3}\times 2 {% endmathjax %}. For n+1, {% mathjax %} [(n + 1)+1]! > 2^{(n+1)+3} {% endmathjax %}. Hence, by induction, the theorem is proved.
  
  **(c) ∀n ∈ N : {% mathjax %} \sum_{r=1}^{n}(r\times r!) = (n + 1)! − 1 {% endmathjax %}**
    Proof: By induction.
    For n=1, the left-hand side is {% mathjax %} (1\times 1!) = 1 {% endmathjax %} and the right-hand side is {% mathjax %} 2! - 1 = 1 {% endmathjax %}, so the inequality is valid for n=1.
    Assume the identity holds for n. So {% mathjax %} \sum_{r=1}^{n}(r\times r!) = (n + 1)! − 1 {% endmathjax %}. Now we need to show show that {% mathjax %} \sum_{r=1}^{n+1}(r\times r!) = [(n + 1) + 1]! − 1 {% endmathjax %}. We split the {% mathjax %} \sum_{r=1}^{n+1}(r\times r!) {% endmathjax %} into two sections i.e. {% mathjax %} \sum_{r=1}^{n+1}(r\times r!)=\sum_{r=1}^{n}(r\times r!) + (n+1)\times (n+1)!{% endmathjax %}. And by our assumption, we can get {% mathjax %} \sum_{r=1}^{n}(r\times r!) + (n+1)\times (n+1)! = (n + 1)! − 1 +  (n+1)\times (n+1)! {% endmathjax %}. By combining like items, we can get {% mathjax %} (n + 1)! − 1 +  (n+1)\times (n+1)! = (n+2)(n+1)! - 1 {% endmathjax %}. It's trivial to get {% mathjax %} (n+2)(n+1)! - 1 = (n+2)!-1 {% endmathjax %}.This is the identity for n+1. Hence, by induction, the theorem is proved.
  