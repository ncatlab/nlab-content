+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

A __$\sigma$-complete lattice__ is a [[lattice]] $(L, \leq, \bot, \vee, \top, \wedge)$ with a function

$$\Vee_{i:\mathbb{N}} (-)(i): (\mathbb{N} \to L) \to L$$

such that 

* for all natural numbers $n \in \mathbb{N}$ and sequences $s: \mathbb{N} \to L$
$$ s(n) \leq \Vee_{i \in \mathbb{N}} s(i)$$

* for all elements $x \in L$ and sequences $s:\mathbb{N} \to L$, if $s(n) \leq x$ for all natural numbers $n \in \mathbb{N}$, then 
$$\Vee_{i \in \mathbb{N}} s(i) \leq x$$

## Properties

Given an element $a \in L$, let $t \mapsto a$ denote the [[constant function|constant]] [[sequence]] to $a$, and given an element $a \in L$ and a sequence $s:\mathbb{N} \to L$, let $T(a, s):\mathbb{N} \to L$ denote the sequence inductively defined by $T(a, s, 0) = a$ and $T(a, s, n + 1) = s(n)$. For simplicity, we denote the infinitary operation as

$$V(s) \coloneqq \Vee_{i \in \mathbb{N}} s(i):(\mathbb{N} \to L) \to L$$

The infinitary operation on a $\sigma$-complete lattice $L$ is 

* [[commutative]] in that given a sequence $s:\mathbb{N} \to L$ and a [[bijection]] $b:\mathbb{N} \cong \mathbb{N}$, 

$$V(s) = V(s \circ b)$$

* [[idempotent]] in that given an element $a \in L$, 

$$V(t \mapsto a) = a$$

* [[associative]] in that given an element $a \in L$ and sequences $r:\mathbb{N} \to L$ and $s:\mathbb{N} \to L$, 

$$V(T(V(T(a, r)), s)) = V(T(V(T(a, s)), r))$$

i.e. using concatenation to denote the infinitary operation

$$(\ldots r_3 r_2 r_1 r_0 a) s_0 s_1 s_2 s_3 \ldots = \ldots r_3 r_2 r_1 r_0 (a s_0 s_1 s_2 s_3 \ldots)$$

The commutative property being satisfied ensures that all other possible associativity equations are satisfied as well. 

* The bottom element $\bot \in L$ is a [[neutral element]] of the infinitary operation in the sense that for all elements $a \in L$

$$V(T(a, t \to \bot)) = a$$

The commutative property being satisfied ensures that all other possible neutral element equations are satisfied as well. 

## See also 

* [[lattice]]

* [[sigma-frame]]

* [[sigma-complete Heyting algebra]]

* [[sigma-complete Boolean algebra]]

* [[sigma-continuous valuation]]

* [[sigma-continuous probability valuation]]

* [[countably prime filter]]

## References ##

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))

[[!redirects sigma-complete lattice]]
[[!redirects sigma-complete lattices]]
[[!redirects σ-complete lattice]]
[[!redirects σ-complete lattices]]