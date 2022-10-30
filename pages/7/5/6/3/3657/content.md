
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

An [[inverse sequence]] ([[sequential diagram]]) $G_\bullet$ of [[groups]] is said to satisfy the _Mittag-Leffler condition_ if the [[images]] of groups from far down the sequence do not get smaller.

This is a condition used to assure the vanishing of the first [[derived functor]] of the [[limit]]-functor, $\underset{\longleftarrow}{lim}^1 G_\bullet$. See at _[[lim^1 and Milnor sequences]]_.

This is relevant for the preservation of exactness when applying limiting processes to exact sequences.  _



## Definition




An inverse sequence of groups consists of some groups $G_n$ indexed by the [[natural numbers]]  and between them group [[homomorphisms]]: if $m \gt n$, there is a homomorphism $p^m_n : G_m \to G_n$ and if $l\gt m  \gt n$, $p^m_n p^l_m= p^l_n$, so that we really just need the $p^{n+1}_n$s to define everything.

An inverse system $G = \{G_n,p^m_n\}$ is said to _satisfy the Mittag-Leffler property_ (or _condition_) if

for any $n$, there is an $n^\prime \gt n$ such that for any $n^{\prime\prime} \gt n^\prime$, 


$$p^{n^{\prime\prime}}_n(G_{n^{\prime\prime}}) = p^{n^\prime}_n(G_{n^\prime}).$$

## Discussion

This is the 'classical' form of the condition. It can also be applied in any category where images make sense. 

An inverse sequence is a special type of [[pro-object]].

Any Mittag-Leffler pro-object is known to be [[essentially epimorphic pro-object|essentially epimorphic]] in the sense that it is isomorphic to a pro-object whose connecting morphisms are epis, that is to a [[strict pro-object]]. 


## Literature

Related $n$Lab entries include [[movable pro-object]].

Mittag-Leffler property of pro-objects in the category of pointed sets and in the category of (nonabelian) groups is studied in Ch.II, Sec. 6.2 of

* [[S. Mardešić]], J. Segal, _Shape theory_, North Holland 1982

[[!redirects Mittag-Leffler conditions]]
[[!redirects Mittag-Leffler property]]
