
#Contents#
* table of contents
{:toc}


## Idea

The _abc conjecture_ (or _ABC conjecture_) is a [[number theory|number theoretic]] conjecture due to ([Oesterl&#233;-Masser 1985](#Oesterl&#233;Masser)), which says that there are only [[finite set|finitely many]] solutions to the simple [[equation]] 

$$
  a + b = c   \;\;\; for a,b,c \geq 1 \in \mathbb{N}
$$

if one requires the [[natural numbers]] $a,b,c$ to have no common factor as well as having "joint power" greater than a given bound.

Here the _power_ of $a,b,c$ is

$$
  P(a,b,c) \coloneqq \frac{log|c|}{log(rad(a\cdot b\cdot c))}
  \,,
$$

where the [[radical]] $rad(n)$ of an [[integer]] $n$ is the product of all its distinct [[prime factors]]. 

The precise form of the conjecture is:

+-- {: .un_theorem}
###### Conjecture
**(abc conjecture)**

For any number $\epsilon\gt 0$ there are only finitely many positive [[coprime integers|coprime]] [[integer]] solutions $(a,b,c)$ to the [[equation]] $a + b = c$   with power $P(a,b,c)\geq 1+\epsilon$.

=--



According to ([Mazur](#Matzur)):

> The beauty of such a Conjecture is that it captures the intuitive sense that triples of numbers which satisfy a linear relation, and which are divisible by high perfect powers, are rare; the precision of the Conjecture goads one to investigate this rarity quantitatively. Its very statement makes an attractive appeal to perform a range of numerical experiments that would test the empirical waters. On a theoretical level, it is enlightening to understand its relationship to the constellation of standard arithmetic theorems, conjectures, questions, etc., and we shall give some indications of this below.

## Relation to other statements

The abc conjecture implies the [[Mordell conjecture]] ([Elkies](#Elkies)).

It is equivalent to the general form of [[Szpiro's conjecture]].


## References

The abc conjecture was stated in 

* Joseph Oesterl&#233;, David Masser (1985)
 {#Oesterl&#233;Masser}

[[Shinichi Mochizuki]] recently anounced the proof which the mathematical community perceives as a serious but unchecked claim. See the references at _[[inter-universal Teichmüller theory]]_.

At 

* MathOverflow, _[Philosophy behind Mochizuki's work on the ABC conjecture](http://mathoverflow.net/questions/106560/philosophy-behind-mochizukis-work-on-the-abc-conjecture/106658#106658)_

are some technical summaries.

See also

* [[Barry Mazur]], _Questions about number_, [pdf](http://www.math.harvard.edu/~mazur/papers/scanQuest.pdf) scan
 {#Mazur}

* PolyMath, _[ABC conjecture](http://michaelnielsen.org/polymath1/index.php?title=ABC_conjecture)_

*  Abderrahmane Nitaj, _[The ABC Conjecture Homepage](http://www.math.unicaen.fr/~nitaj/abc.html)_

* Wikipedia, _[abc conjecture](http://en.wikipedia.org/wiki/Abc_conjecture)_


The relation to the [[Mordell conjecture]] is discussed in

* [[Noam Elkies]], _ABC conjecture implies Mordell_, Int. Math. Research Notices 7 (1991) 99-109
 {#Elkies}

The relation to [[Szpiro's conjecture]] is discussed in 

* Matt Baker (notes taken by William Stein), _Elliptic curves, the ABC conjecture, and points of small canonical height_ ([pdf](http://modular.math.washington.edu/mcs/archive/Fall2001/notes/12-10-01/12-10-01.pdf))
