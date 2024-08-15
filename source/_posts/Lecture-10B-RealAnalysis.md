---
title: 'Lecture 10B: Real Analysis 2'
date: 2024-07-18 15:14:45
tags: notes
katex: true
mathjax: true
---
## Theorem: The rational line is not complete.
**Proof**: By contradiction. Assume the rational line is complete. 
            Then there exists a counterexample. Let A={x{% mathjax %} \in \mathbb{Q} {% endmathjax %}| {% mathjax %} x\leq 0 {% endmathjax %} and {% mathjax %} x^2 {% endmathjax %} <2}. {% mathjax %} \forall a \in A {% endmathjax %} a<2. So 2 is a upper bound of A. Now we need to show that A doesn't have a least upper bound. 
            Let x be any upper bound of A. Assume b is the least upper bound so that for any x, x < b. 
            <img src="../img/ratisincmplt.jpg">

            Assume {% mathjax %} b^2 \leq 2. {% endmathjax %}. Hence {% mathjax %} b^2 > 2. {% endmathjax %}. Let b^~= {% mathjax %} \frac{4+3b}{3+2b}{% endmathjax %}. Then {% mathjax %} b^~{% endmathjax %}