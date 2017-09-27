---
title: Nash beats Gödel: On the history of complexity and cryptography
layout: post
date: 2013-11-29 00:00:00 -0500
---

Nash beats Gödel: On the history of complexity and cryptography
===============================================================

We know that Kurt Gödel, unhappy with having only completeness and incompleteness theorems named after him, also essentially invented the <strong>P</strong> vs <strong>NP</strong> question in a <a href="http://rjlipton.wordpress.com/the-gdel-letter/">1956 letter to John Von Neumann</a>. Unfortunately, there were no blogs back then, so we had to wait until the 1980s to read it, and Cook, Karp & co. had to reinvent the question from scratch.

What we <em>didn't</em> know until a few days ago (I personally discovered it today via <a href="http://aaronsadventures.blogspot.com/2012/02/amazing-new-declassified-document.html">Aaron Roth</a>) is that in 1955, one year before Gödel's letter, <em>John Nash</em> also had something to say on the topic, in a few letters to NSA. Gödel and Nash independently made <em>strikingly</em> similar remarks, starting from completely different points of view. While Gödel's perspective was that of a logician (his letter was about the length of proofs in first-order logic), Nash was interested in cryptography, and wrote about the security of cryptographic systems.

<a href="http://www.nsa.gov/public_info/press_room/2012/nash_exhibit.shtml">NSA's press release</a> about the declassification of Nash's letters was apparently made on 27 January 2012; <a href="http://www.nsa.gov/public_info/_files/nash_letters/nash_letters1.pdf">here</a> is a PDF containing Nash's letters and the replies he got from NSA. I'll only focus on the second letter here, leaving a cryptoanalysis of the system he proposed in the third one to someone more knowledgeable than me on the topic.

I assume Nash was familiar with Shannon's work <em>Communication theory of secrecy systems</em> (1949), so he already knew that the only mathematically unbreakable cipher is one-time pad. Hence, in order to discuss practical encryption systems, he invented the principles of modern cryptography about 20 years in advance:

<blockquote style="border:none;">If <span style="font-style:normal;">[</span>the computation required in order to recover the key from the ciphertext<span style="font-style:normal;">]</span>, although possible in principle, were sufficiently long at best then the process could still be secure in a practical sense.</blockquote>

Here is some computational complexity, 8 years before Hartmanis and Stearns:

<blockquote style="border:none;">The most direct computation procedure would be for the enemy to try all <span style="font-style:normal;">2</span><sup><em>r</em></sup> possible keys, one by one. Obviously this is <span style="font-style:normal;">easily</span> made impractical for the enemy by simply choosing <em>r</em> large enough.</blockquote>

Apparently Nash already knew quite well ("obviously", "easily") that exponential time is too much.

And here is how one can classify cryptosystems (but also general computation problems) according to him. I think you can read essentially the same paragraph in all modern complexity theory and cryptography books.

<blockquote style="border:none;">So a logical way to classify enciphering processes is by the way in which the computation length for the computation of the key increases with increasing length of the key. This is at best exponential and at worst probably a relatively small power of <em>r</em>, <em>ar</em><sup><span style="font-style:normal;">2</span></sup> or <em>ar</em><sup><span style="font-style:normal;">3</span></sup>, as in substitution ciphers.</blockquote>

Nash also conjectures that many problems cannot be solved in polynomial time. In hindsight, there is some naivety here about the design of good ciphers, but this is still very interesting:

<blockquote style="border:none;">Now my general conjecture is as follows: For almost all sufficiently complex types of enciphering, especially where the instructions given by different portions of the key interact complexly with each other in the determination of their ultimate effects on the enciphering, the mean key computation length increases exponentially with the length of the key, or in other words, with the information content of the key.

The significance of this general conjecture, assuming its truth, is easy to see. It means that it is quite feasible to design ciphers that are effectively unbreakable. As ciphers became more sophisticated the game of cipher breaking by skilled teams, etc., should become a thing of the past.</blockquote>

All in all, this seems to me a truly magnificent historical document, possibly on par with the aforementioned letter by Gödel. I'd really like to know what people working in cryptography think about this.

These "Lost Letter" discoveries also make me wonder what further treasures may be hidden in NSA's cardboard boxes, or in private correspondence collections. What if there exists a “Fermat's Lost (Last?) Letter” along the lines of "Here's the proof that didn't fit in the margin", or a “Russell's Lost Letter” that he sent to Whitehead to tell him “I found a proposition that can't be proved nor refuted in <em>Principia Mathematica</em>”?
