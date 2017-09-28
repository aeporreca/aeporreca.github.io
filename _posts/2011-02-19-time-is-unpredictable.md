---
layout: post
title: Time is unpredictable
redirect_from: /2011/02/19/time-is-unpredictable/
---

<em>This post is inspired by the question <a href="http://cstheory.stackexchange.com/q/5004/182">Are runtime bounds in P decidable?</a> asked by <a href="http://www.mrfm.org/">John Sidles</a> on the CSTheory website, and the <a href="http://cstheory.stackexchange.com/questions/5004/are-runtime-bounds-in-p-decidable-answer-no/5006#5006">answer</a> given by <a href="http://www.ccs.neu.edu/home/viola/">Emanuele Viola</a>.</em>

Is there an automatic procedure to determine whether a given Turing machine, <em>known</em> to be halting, operates within time bound $O(f)$ (assuming $f$ is a computable function)?

Predictably, the answer turns out to be negative.

Let’s start by formalising the problem. Assume $M$ is the Turing machine whose runtime we’re interested in, and $F$ is another TM computing the time bound $f$; then

$ L = \\{ (M, F) : M \\text{ halts within } O(F) \\text{ steps} \\}. $

Also let $H$ be the halting problem:

$ H = \\{ (M’, x) : M \\text{ halts on input } x \\}. $

We can now define the function $R(M’, x) = (M, F)$, where $F$ computes $n^2$ and $M$, on input $y$, behaves as follows:

* Simulate $M'$ on $x$ for $n = |y|$ steps.
* If $M'$ has already halted, then loop for $n^2$ steps.
* Otherwise, loop for $n^3$ steps.

We’re finally ready to prove our undecidability result.

<strong>Theorem.</strong> $R$ is a many-one reduction from $H$ to $L$.

<em>Proof.</em> Clearly $R$ is a computable function, so we just need to show that

$ (M', x) \\in H \\iff (M, F) \\in L. $

If  $(M', x) \\in H$, that is, if $M'$ halts on input $x$, then it does so in $k$ steps (for some $k \\in \\mathbb{N}$). Hence $M$ runs in $O(n^2)$ time (notice that it runs in $n^3$ time for $|y| < k$, but it's only the asymptotic behaviour that matters for us). Thus $(M, F) \\in L$.

On the other hand, if <em>M’</em> does not halt on <em>x</em>, then <em>M</em> never completes its simulation, and the runtime for <em>M</em> is <em>O</em>(<em>n</em><sup>3</sup>). Thus (<em>M</em>, <em>F</em>) &notin; <em>L</em>. □

<strong>Remark.</strong> We’ve actually proved a stronger statement, i.e., that the set of Turing machines running in <em>O</em>(<em>n</em><sup>2</sup>) time is undecidable, even if we restrict the domain to machines halting in polynomial time. Similar undecidability results hold for an infinite class of time bounds.
