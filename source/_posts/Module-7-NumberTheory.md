---
title: 'Lecture 9A: Number Theory'
date: 2024-07-18 15:14:45
tags: "notes"
katex: true
mathjax: true
---
**1. The Euclid's Lemma: For any integer a, b, if there exists a prime p such p divides ab, then p divides at least one of a or b.**
Proof: By stong induction. We need to prove that {% mathjax %} \forall a, b \in \mathbb{Z} \exists prime\space p [p|ab \implies (p|a \lor p|b)] {% endmathjax %}
Suppose that p|ab and gcd(p,a) = 1 which means p can't divide a. Now we have to show that p|b. Since p|ab, there is an integer q such that pq=ab.
Without lose of generality, we can suppose p, q, a, and b are positive, since the divisibility relation is independent from the signs of the involved integers. For proving this by strong induction, we assume {% mathjax %} (p|ab \implies p|b) {% endmathjax %} is valid for all positive lower values of ab.
For p=a, since gcd(p,a)=1, we can get p=1, and p divides b trivially.
For p < a, one has p(q-b)=(a-p)b. Since gcd(p,a)=1, then gcd(p,(a-p))=1. Now we have to show that p|b. Since {% mathjax %} (a-p)b < ab {% endmathjax %}, then by induction hypothesis we can get p|b.
For p > a, one has (p-a)q=a(b-q). Since gcd(p,a)=1, then gcd((p-a),a)=1. Now we have to show that (p-a)|(b-q). We know that a(b-q) < ab. So by induction hypothesis, we can get (p-a)|(b-q). So there exists an integer k such that (p-a)k = (b-q). So, (p-a)q=a(p-a)k, and by dividing by (p-a), one has q=ak. Therefore, pq=pak=ab, and by dividing by a, one has pk=b, the desired result.

Refernce: https://www.youtube.com/watch?v=LZRESW_4OZU