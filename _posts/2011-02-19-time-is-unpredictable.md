---
layout: post
title: Time is unpredictable
redirect_from: /2011/02/19/time-is-unpredictable/
---

<em>This post is inspired by the question <a href="http://cstheory.stackexchange.com/q/5004/182">Are runtime bounds in P decidable?</a> asked by <a href="http://www.mrfm.org/">John Sidles</a> on the CSTheory website, and the <a href="http://cstheory.stackexchange.com/questions/5004/are-runtime-bounds-in-p-decidable-answer-no/5006#5006">answer</a> given by <a href="http://www.ccs.neu.edu/home/viola/">Emanuele Viola</a>.</em>

Is there an automatic procedure to determine whether a given Turing machine, <em>known</em> to be halting, operates within time bound $O(f)$ (assuming $f$ is a computable function)?

Predictably, the answer turns out to be negative.

Let’s start by formalising the problem. Assume $M$ is the Turing machine whose runtime we’re interested in, and $F$ is another TM computing the time bound $f$; then

<blockquote style="border:none;font-style:normal;">
$L = \{(M, F) : M$ halts within $O(F)$ steps$\}$.
</blockquote>

Also let <em>H</em> be the halting problem:

<blockquote style="border:none;font-style:normal;">
$H = \{(M’, x) : M$ halts on input $x\}$.
</blockquote>

We can now define the function $R(M’, x) = (M, F)$, where $F$ computes $n^2$ and $M$, on input $y$, behaves as follows:
- Simulate $M'$ on $x$ for $n = |y|$ steps.</li>
- If $M'$ has already halted, then loop for $n^2$ steps.
- Otherwise, loop for $n^3$ steps.

We’re finally ready to prove our undecidability result.

<strong>Theorem.</strong> $R$ is a many-one reduction from $H$ to $L$.

<em>Proof.</em> Clearly $R$ is a computable function, so we just need to show that
<blockquote style="border:none;font-style:normal;">
$(M', x) \in H \iff (M, F) \in L$.
</blockquote>

If  (<em>M’</em>, <em>x</em>) &isin; <em>H</em>, that is, if <em>M’</em> halts on input <em>x</em>, then it does so in <em>k</em> steps (for some <em>k</em> &isin; ℕ). Hence <em>M</em> runs in <em>O</em>(<em>n</em><sup>2</sup>) time (notice that it runs in <em>n</em><sup>3</sup> time for |<em>y</em>| &lt; <em>k</em>, but it’s only the asymptotic behaviour that matters for us). Thus (<em>M</em>, <em>F</em>) &isin; <em>L</em>.

On the other hand, if <em>M’</em> does not halt on <em>x</em>, then <em>M</em> never completes its simulation, and the runtime for <em>M</em> is <em>O</em>(<em>n</em><sup>3</sup>). Thus (<em>M</em>, <em>F</em>) &notin; <em>L</em>. □

<strong>Remark.</strong> We’ve actually proved a stronger statement, i.e., that the set of Turing machines running in <em>O</em>(<em>n</em><sup>2</sup>) time is undecidable, even if we restrict the domain to machines halting in polynomial time. Similar undecidability results hold for an infinite class of time bounds.
