---
layout: post
title: "Developments in Language Theory 2010: Where tetration has lease"
redirect_from: /2010/08/15/dlt-2010-where-tetration-has-lease/
---

Tomorrow I'm leaving for Canada, to attend the <a href="http://www.csd.uwo.ca/DLT2010/">14th International Conference on Developments in Language Theory</a>, held at <a href="http://uwo.ca/">University of Western Ontario</a>, London. You can find the programme <a href="http://www.csd.uwo.ca/DLT2010/program.html">here</a>.

Our <abbr>DLT</abbr> 2010 paper, authored by yours truly, Alberto Leporati and Claudio Zandron, is titled <a href="https://doi.org/10.1007/978-3-642-14455-4_33">On a powerful class of non-universal P systems with active membranes</a>. In it, we describe a restricted variant of <a href="http://researchspace.auckland.ac.nz/handle/2292/3611">P systems with active membranes</a> (computing devices inspired by biological cells) that is not Turing-equivalent, but nonetheless decide a surprisingly large class of languages. This class also seems to be somewhat "new" (we haven't been able to find any reference to it in the literature).

Consider the operation of <a href="http://en.wikipedia.org/wiki/Tetration"><em>tetration</em></a> (iterated exponentiation), defined as

$${}^n b = \underbrace{\,b^{b^{b^{\cdot^{\cdot^{\cdot^b}}}}}}_{n \text{ times}}$$

and call <strong>PTETRA</strong> the class of languages decided by Turing machines working in time ${}^{p(n)}2$ for some polynomial <em>p</em> (the <strong>P</strong> in <strong>PTETRA</strong> signifies the fact that exponentiation is iterated only polynomially many times instead of, say, exponentially many). This class is trivially closed under union, intersection, complement, and polytime reductions. Furthermore, it's easy to see that it can also be defined in terms of <em>space</em> ${}^{p(n)}2$ (you can also throw in nondeterminism, if you really want to).

Well, the main result of our paper is the following funny theorem.

<strong>Theorem.</strong> <em>The class of languages decided by our variant of P system with active membranes is exactly</em> <strong>PTETRA</strong>.

The proof works like this:
<ul>
<li>The upper bound is proved by a few calculations that show how our P systems can never use more that tetrational space, because the process of membrane division (which generates lots of new membranes) must stop after a finite number of steps.</li>
<li>To prove the lower bound, we show that we can simulate with our P systems all tetrational-space <a href="http://en.wikipedia.org/wiki/Counter_machine">counter machines</a>, hence tetrational-space Turing machines.</li>
</ul>

The result is somewhat unexpected, as I was under the impression that all we could do with these P systems was <strong>EXPSPACE</strong>, and indeed I wasted a few days trying to prove that. Fortunately, reality turned out to be much more interesting.
