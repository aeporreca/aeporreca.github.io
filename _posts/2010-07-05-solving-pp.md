---
layout: post
title: Solving PP-complete problems using P systems
redirect_from: /2010/07/05/solving-pp/
---

Today we submitted the final version of our paper <a href="https://doi.org/10.1007/978-3-642-18123-8_26">P systems with elementary active membranes: Beyond NP and coNP</a>, which has been accepted for the <a href="http://cmc11.uni-jena.de">Eleventh International Conference on Membrane Computing</a>, taking place on 24–27 August.

The venue of <abbr title="Eleventh International Conference on Membrane Computing">CMC11</abbr> is <a href="http://www.uni-jena.de">Friedrich-Schiller-Universität</a> in Jena, Germany. This university has some slightly notable alumni, such as Rudolf Carnap, Gottlob Frege, Gottfried "Calculemus" Leibniz, Karl Marx, and Arthur Schopenhauer among <a href="http://en.wikipedia.org/wiki/University_of_Jena#Notable_alumni">others</a>; the teaching staff was marginally interesting too, including modest names such as Gottlieb Fichte, Georg Wilhelm Friedrich Hegel, Friedrich Schelling, and Friedrich Schiller himself. In short, rest assured that I certainly won't be going around hunting for busts or statues of these guys, and that I won't get someone to take pictures of me beside them to post on this blog.

Anyway, in our paper we solve a <strong>PP</strong>-complete problem via <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.43.6198">P systems with active membranes</a>, using only division for elementary membranes (that is, membranes that don't contain other membranes). The problem is a variant of <a href="http://books.google.com/books?id=yJIMx9nXB6kC&pg=PA1090&dq=%22majority+sat%22&hl=en&ei=-EQyTKW4OdfgsAaC2uzNBA&sa=X&oi=book_result&ct=result&resnum=4&ved=0CDQQ6AEwAw#v=onepage&q=%22majority%20sat%22&f=false">Majority-SAT</a>.

P systems with elementary active membranes are known for their ability to generate exponentially many membranes in linear time by using membrane division. These membranes can then explore, in a parallel way, the whole space of candidate solutions of an <strong>NP</strong>-complete problem, thus solving it in polynomial time.

In the paper we extend this algorithm (which is pretty <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.29.1987">standard</a> in our literature) by checking whether the number of membranes finding a satisfying assignment exceeds a certain threshold, instead of just checking whether there is at least one. Lo and behold, not only we can solve <strong>NP</strong>-complete problems in polynomial time, but also <strong>PP</strong>-complete ones.
