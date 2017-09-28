---
layout: post
title: On the length of proofs (episode II)
redirect_from: /2010/07/12/length-of-proofs-2/
---

Last week I wrote a <a href="/2010/07/04/length-of-proofs/">post</a> about arithmetical theorems having very long proofs, and linked to an <a href="http://plato.stanford.edu/entries/goedel/#SpeUpThe">article</a> on the <abbr title="Stanford Encyclopedia of Philosophy">SEP</abbr> for the details. Today, me and my colleague Luca Manzoni realised that there is a much simpler proof; it is essentially the same <a href="http://www.scottaaronson.com/writings/bignumbers.pdf">proof</a> described by Scott Aaronson for the uncomputability of the busy beaver function, and it holds for any undecidable, recursively axiomatisable theory $T$ (that is, if there exists a recursive set of axioms generating the sentences of the theory, but no decision procedure for checking whether a sentence is a theorem).

Let $L(\varphi)$ be the length in symbols of the shortest proof of the sentence $\varphi$, using a standard set of inference rules together with any recursive set of axioms for $T$; set $L(\varphi) = 0$ if $\varphi$ is not a theorem. Also, let $L(n)$ be the maximum $L(\varphi)$ among all sentences $\varphi$ of length at most $n$. 

**Theorem.** $L$ grows faster than any computable function.

*Proof.* Otherwise, given a sentence $\varphi$, we can first compute an integer $f(\lvert\varphi\rvert) \ge L(\lvert\varphi\rvert)$, then enumerate all proofs of length at most $f(\lvert\varphi\rvert)$ and check them. If at least one of these is a proof of $\varphi$, we answer "yes", otherwise "no". But this is a decision procedure for $T$, since we know that if $\varphi$ is a theorem, then it has a proof of length at most$f(\lvert\varphi\rvert)$; contradiction. □

In particular, the theorem holds for Peano arithmetic and friends.
