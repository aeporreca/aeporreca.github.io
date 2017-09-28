---
layout: post
title: On the length of proofs
redirect_from: /2010/07/04/length-of-proofs/
---

One of the most amazing facts about (un)computability is the existence of functions <em>f</em> : ℕ → ℕ that <em>grow faster than any recursive function</em>, that is, for all computable <em>g</em> : ℕ → ℕ we have

$$\displaystyle \lim_{n \to \infty} \frac{g(n)}{f(n)} = 0.$$

The most common function of this kind is the <a href="http://en.wikipedia.org/wiki/Busy_beaver">busy beaver function</a>, described by Tibor Radó in his paper <a href="http://www.ftonti.net/wiki/_media/rado-on_non-computable_functions.pdf">On non-computable functions</a>; for an introduction to this topic, you can read the excellent paper <a href="http://www.scottaaronson.com/writings/bignumbers.pdf">Who can name the bigger number?</a> by Scott Aaronson (that's where I first read about it).

Radó's paper was published in the Bell System Technical Journal in 1962 but, as often happens, related work was done before by Kurt Gödel; see, for instance, the paper bearing the same title as this post, whose translation can be found in the classic collection <a href="http://books.google.com/books?id=qW8x7sQ4JXgC&lpg=PA82&ots=TMvQ5gJ-hI&dq=godel%20%22on%20the%20length%20of%20proofs%22&pg=PA82#v=snippet&q=%22kurt%20godel%20on%20the%20length%20of%20proofs%22&f=false"><em>The Undecidable</em></a> (edited by Martin Davis).

A cool result that can be proved is that the length of the proofs of arithmetical statements also grows faster than any recursive function. Quoting Juliette Kennedy's <a href="http://plato.stanford.edu/entries/goedel/#SpeUpThe">article</a> about Gödel on the <em>Stanford Encyclopedia of Philosophy</em>:

> <strong>Theorem 5.</strong> Given any recursive function $f$ there are provable sentences $\varphi$ of arithmetic such that the shortest proof is greater than $f(\ulcorner\varphi\urcorner)$ in length.

In other words, <em>some theorems just have really freaking long proofs</em>. See the <abbr title="Stanford Encyclopedia of Philosophy">SEP</abbr> article for the details.
