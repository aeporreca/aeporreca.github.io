---
layout: post
title: How I learned to stop worrying about Turing completeness and love primitive recursion
redirect_from: /2010/07/11/primitive-recursion/
---

The primitive recursive functions are a class of computable arithmetic functions with a reasonably natural <a href="http://en.wikipedia.org/wiki/Primitive_recursive_function#Definition">definition</a>. They do not exhaust all computable functions (e.g., <a href="http://en.wikipedia.org/wiki/Ackermann_function">Ackermann's function</a> grows faster than any <abbr title="primitive recursive">PR</abbr> function). Here is a list of reasons to like them anyway.

<ul>
<li>The <abbr title="primitive recursive">PR</abbr> functions are exactly the functions that can be computed by using only <em>for</em> loops (i.e., without unbounded kinds of loop such as <em>while</em> and <em>repeat-until</em>).</li>
<li>Each time you apply the primitive recursion schema, you get new functions. Meaning: with <em>n</em> + 1 nested <em>for</em> loops you can compute functions that you can't compute using only <em>n</em> nested <em>for</em> loops.</li>
<li>Any computable function can be obtained by using <abbr title="primitive recursive">PR</abbr> functions plus a single application of the <a href="http://en.wikipedia.org/wiki/Mu_operator"><em>μ</em> operator</a>. In other words, you just need to use one <em>while</em> loop (together with the <em>for</em> loops) to obtain a Turing machine. This is called <a href="http://en.wikipedia.org/wiki/Kleene's_T_predicate#Normal_form_theorem">Kleene's normal form theorem</a>.</li>
<li>Every recursively enumerable set is also primitively recursively enumerable. See this <a href="http://mathoverflow.net/questions/21087">question</a> on MathOverflow, where I recently discovered this fact.</li>
<li>The <abbr title="primitive recursive">PR</abbr> functions are exactly the functions that can be computed by Turing machines operating within a <abbr title="primitive recursive">PR</abbr> time bound. Isn't this amazing? See, e.g., this <a href="http://doi.acm.org/10.1145/800196.806014">paper</a> by A.R. Meyer and D.M. Ritchie (yes, <a href="http://cm.bell-labs.com/cm/cs/cbook/">that</a> D.M. Ritchie).
</li><li>Any function of practical use is primitive recursive. This is a consequence of the previous point: polynomials, but also exponentials (and <a href="http://en.wikipedia.org/wiki/Tetration">much</a>, <a href="http://en.wikipedia.org/wiki/Knuth's_up-arrow_notation">much</a> worse functions) are all <abbr title="primitive recursive">PR</abbr>. If a function is not <abbr title="primitive recursive">PR</abbr>, then you don't have enough time to compute it.</li>
</ul>

I strongly urge you to like the primitive recursive functions too.
