---
layout: post
title: Time is unpredictable
redirect_from: /2011/02/19/time-is-unpredictable/
---

*This post is inspired by the question <a href="http://cstheory.stackexchange.com/q/5004/182">Are runtime bounds in P decidable?</a> asked by <a href="http://www.mrfm.org/">John Sidles</a> on the CSTheory website, and the <a href="http://cstheory.stackexchange.com/questions/5004/are-runtime-bounds-in-p-decidable-answer-no/5006#5006">answer</a> given by <a href="http://www.ccs.neu.edu/home/viola/">Emanuele Viola</a>.*

Is there an automatic procedure to determine whether a given Turing machine, *known* to be halting, operates within time bound *O*(*f*) (assuming *f* is a computable function)?

Predictably, the answer turns out to be negative.

Let’s start by formalising the problem. Assume *M* is the Turing machine whose runtime we’re interested in, and *F* is another TM computing the time bound *f*; then

<blockquote style="border:none;font-style:normal;">
*L* = {(*M*, *F*) : *M* halts within *O*(*F*) steps}.
</blockquote>

Also let *H* be the halting problem:

<blockquote style="border:none;font-style:normal;">
*H* = {(*M’*, *x*) : *M* halts on input *x*}.
</blockquote>

We can now define the function *R*(*M’*, *x*) = (*M*, *F*), where *F* computes *n*<sup>2</sup> and *M*, on input *y*, behaves as follows:
<ul>
<li>Simulate *M’* on *x* for *n* = |*y*| steps.</li>
<li>If *M’* has already halted, then loop for *n*<sup>2</sup> steps.
<li>Otherwise, loop for *n*<sup>3</sup> steps.
</ul>

We’re finally ready to prove our undecidability result.

<strong>Theorem.</strong> *R* is a many-one reduction from *H* to *L*.

*Proof.* Clearly *R* is a computable function, so we just need to show that
<blockquote style="border:none;font-style:normal;">
(*M’*, *x*) &isin; *H* &hArr; (*M*, *F*) &isin; *L*.
</blockquote>

If  (*M’*, *x*) &isin; *H*, that is, if *M’* halts on input *x*, then it does so in *k* steps (for some *k* &isin; ℕ). Hence *M* runs in *O*(*n*<sup>2</sup>) time (notice that it runs in *n*<sup>3</sup> time for |*y*| &lt; *k*, but it’s only the asymptotic behaviour that matters for us). Thus (*M*, *F*) &isin; *L*.

On the other hand, if *M’* does not halt on *x*, then *M* never completes its simulation, and the runtime for *M* is *O*(*n*<sup>3</sup>). Thus (*M*, *F*) &notin; *L*. □

<strong>Remark.</strong> We’ve actually proved a stronger statement, i.e., that the set of Turing machines running in *O*(*n*<sup>2</sup>) time is undecidable, even if we restrict the domain to machines halting in polynomial time. Similar undecidability results hold for an infinite class of time bounds.
