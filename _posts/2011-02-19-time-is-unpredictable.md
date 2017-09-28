---
layout: post
title: Time is unpredictable
redirect_from: /2011/02/19/time-is-unpredictable/
---

<em>This post is inspired by the question <a href="http://cstheory.stackexchange.com/q/5004/182">Are runtime bounds in P decidable?</a> asked by <a href="http://www.mrfm.org/">John Sidles</a> on the CSTheory website, and the <a href="http://cstheory.stackexchange.com/questions/5004/are-runtime-bounds-in-p-decidable-answer-no/5006#5006">answer</a> given by <a href="http://www.ccs.neu.edu/home/viola/">Emanuele Viola</a>.</em>

Is there an automatic procedure to determine whether a given Turing machine, <em>known</em> to be halting, operates within time bound $O(f)$ (assuming <em>f</em> is a computable function)?

Predictably, the answer turns out to be negative.

Let’s start by formalising the problem. Assume <em>M</em> is the Turing machine whose runtime we’re interested in, and <em>F</em> is another TM computing the time bound <em>f</em>; then

<blockquote style="border:none;font-style:normal;">
<em>L</em> = {(<em>M</em>, <em>F</em>) : <em>M</em> halts within <em>O</em>(<em>F</em>) steps}.
</blockquote>

Also let <em>H</em> be the halting problem:

<blockquote style="border:none;font-style:normal;">
<em>H</em> = {(<em>M’</em>, <em>x</em>) : <em>M</em> halts on input <em>x</em>}.
</blockquote>

We can now define the function <em>R</em>(<em>M’</em>, <em>x</em>) = (<em>M</em>, <em>F</em>), where <em>F</em> computes <em>n</em><sup>2</sup> and <em>M</em>, on input <em>y</em>, behaves as follows:
<ul>
<li>Simulate <em>M’</em> on <em>x</em> for <em>n</em> = |<em>y</em>| steps.</li>
<li>If <em>M’</em> has already halted, then loop for <em>n</em><sup>2</sup> steps.
<li>Otherwise, loop for <em>n</em><sup>3</sup> steps.
</ul>

We’re finally ready to prove our undecidability result.

<strong>Theorem.</strong> <em>R</em> is a many-one reduction from <em>H</em> to <em>L</em>.

<em>Proof.</em> Clearly <em>R</em> is a computable function, so we just need to show that
<blockquote style="border:none;font-style:normal;">
(<em>M’</em>, <em>x</em>) &isin; <em>H</em> &hArr; (<em>M</em>, <em>F</em>) &isin; <em>L</em>.
</blockquote>

If  (<em>M’</em>, <em>x</em>) &isin; <em>H</em>, that is, if <em>M’</em> halts on input <em>x</em>, then it does so in <em>k</em> steps (for some <em>k</em> &isin; ℕ). Hence <em>M</em> runs in <em>O</em>(<em>n</em><sup>2</sup>) time (notice that it runs in <em>n</em><sup>3</sup> time for |<em>y</em>| &lt; <em>k</em>, but it’s only the asymptotic behaviour that matters for us). Thus (<em>M</em>, <em>F</em>) &isin; <em>L</em>.

On the other hand, if <em>M’</em> does not halt on <em>x</em>, then <em>M</em> never completes its simulation, and the runtime for <em>M</em> is <em>O</em>(<em>n</em><sup>3</sup>). Thus (<em>M</em>, <em>F</em>) &notin; <em>L</em>. □

<strong>Remark.</strong> We’ve actually proved a stronger statement, i.e., that the set of Turing machines running in <em>O</em>(<em>n</em><sup>2</sup>) time is undecidable, even if we restrict the domain to machines halting in polynomial time. Similar undecidability results hold for an infinite class of time bounds.
