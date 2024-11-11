---
title: 'Assignment 10.1: Real Analysis'
date: 2024-07-25 15:14:45
tags:
katex: true
mathjax: true
---
**1.Prove that the intersection of two intervals is again an interval. Is the same true for unions?**
Proof: **Firstly, we need to prove that {% mathjax %}\emptyset \implies an\space interval{% endmathjax %}**. It's vacuously true. Assume, on the contrary, {% mathjax %}\emptyset \nRightarrow an\space interval{% endmathjax %}. 
In other words, there must exist two elements x,y {% mathjax %}\in \emptyset {% endmathjax %} such that there exist at least one element z(where x<z<y) that is not in the set. 
Here rasies a contradction, since there are no elements in the {% mathjax %}\emptyset {% endmathjax %}. Hence, our assumption is invalid, so {% mathjax %}\emptyset \implies an\space interval{% endmathjax %}.

**Secondly, we come to prove that the intersection of two intervals is again an interval.** Let A=(a,b)={x|a<x<b}, Let B=(c,d)={x|c<x<d}.
Case 1: {% mathjax %}A\cap B = \emptyset{% endmathjax %}. We've already proven that it's a vacuous truth. 
Case 2: {% mathjax %}A\cap B {% endmathjax %} = (min(a,c), min(b,d)). Define min(a,c) as the smallest number between a and c. {% mathjax %}\forall x,y \in A\cap B, \forall z (where\space x<z<y) \in A\cap B.{% endmathjax %}
        Hence, {% mathjax %} A\cap B {% endmathjax %}= (min(a,c), min(b,d)) is an interval.

**Last but not least, we need to show that the unions of two intervals aren't intervals.** Since it's easy to find two elements x,y {% mathjax %}\in {% endmathjax %} any unions of two intervals such that there exist at least one element z(where x<z<y) that is not in the set. 


Relavant: {x| x {% mathjax %} \in {% endmathjax %}image} {% mathjax %} \subset {% endmathjax %} {x| x is the answer in the question} 
Spurious: {x| x is the answer in the answer column}  {% mathjax %} \subset {% endmathjax %} {x| x {% mathjax %} \in {% endmathjax %}image}
Y: {x| x is the answer in the answer column}  {% mathjax %} \not\subset {% endmathjax %} {x| x {% mathjax %} \in {% endmathjax %}image}
**Consider a scenario where a question specifies a property, such as stating 'it is a painting.' If an image, denoted as {x | x ∈ image}, lacks this property and is considered spurious by the definition, should it be labeled as 'S'?**