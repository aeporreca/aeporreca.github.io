---
layout: post
title: Time is unpredictable
redirect_from: /2011/02/19/time-is-unpredictable/
---

*This post is inspired by the question <a href="http://cstheory.stackexchange.com/q/5004/182">Are runtime bounds in P decidable?</a> asked by <a href="http://www.mrfm.org/">John Sidles</a> on the CSTheory website, and the <a href="http://cstheory.stackexchange.com/questions/5004/are-runtime-bounds-in-p-decidable-answer-no/5006#5006">answer</a> given by <a href="http://www.ccs.neu.edu/home/viola/">Emanuele Viola</a>.</em>

Is there an automatic procedure to determine whether a given Turing machine, *known</em> to be halting, operates within time bound *O</em>(*f</em>) (assuming *f</em> is a computable function)?

Predictably, the answer turns out to be negative.

Let’s start by formalising the problem. Assume *M</em> is the Turing machine whose runtime we’re interested in, and *F</em> is another TM computing the time bound *f</em>; then

<blockquote style="border:none;font-style:normal;">
*L</em> = {(*M</em>, *F</em>) : *M</em> halts within *O</em>(*F</em>) steps}.
</blockquote>

Also let *H</em> be the halting problem:

<blockquote style="border:none;font-style:normal;">
*H</em> = {(*M’</em>, *x</em>) : *M</em> halts on input *x</em>}.
</blockquote>

We can now define the function *R</em>(*M’</em>, *x</em>) = (*M</em>, *F</em>), where *F</em> computes *n</em><sup>2</sup> and *M</em>, on input *y</em>, behaves as follows:
<ul>
<li>Simulate *M’</em> on *x</em> for *n</em> = |*y</em>| steps.</li>
<li>If *M’</em> has already halted, then loop for *n</em><sup>2</sup> steps.
<li>Otherwise, loop for *n</em><sup>3</sup> steps.
</ul>

We’re finally ready to prove our undecidability result.

<strong>Theorem.</strong> *R</em> is a many-one reduction from *H</em> to *L</em>.

*Proof.</em> Clearly *R</em> is a computable function, so we just need to show that
<blockquote style="border:none;font-style:normal;">
(*M’</em>, *x</em>) &isin; *H</em> &hArr; (*M</em>, *F</em>) &isin; *L</em>.
</blockquote>

If  (*M’</em>, *x</em>) &isin; *H</em>, that is, if *M’</em> halts on input *x</em>, then it does so in *k</em> steps (for some *k</em> &isin; ℕ). Hence *M</em> runs in *O</em>(*n</em><sup>2</sup>) time (notice that it runs in *n</em><sup>3</sup> time for |*y</em>| &lt; *k</em>, but it’s only the asymptotic behaviour that matters for us). Thus (*M</em>, *F</em>) &isin; *L</em>.

On the other hand, if *M’</em> does not halt on *x</em>, then *M</em> never completes its simulation, and the runtime for *M</em> is *O</em>(*n</em><sup>3</sup>). Thus (*M</em>, *F</em>) &notin; *L</em>. □

<strong>Remark.</strong> We’ve actually proved a stronger statement, i.e., that the set of Turing machines running in *O</em>(*n</em><sup>2</sup>) time is undecidable, even if we restrict the domain to machines halting in polynomial time. Similar undecidability results hold for an infinite class of time bounds.
