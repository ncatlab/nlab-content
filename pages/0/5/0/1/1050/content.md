
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* tic
{: toc}


## Idea 

A [[functor]] is called _left exact_ or [[flat functor|flat]] if it preserves [[finite limits]], and _right exact_ if it preserves [[finite colimits]].
A functor is called _exact_ if it is both left and right exact.

Specifically [[Ab]]-[[enriched functor]]s between [[abelian categories]] are exact if they preserve [[exact sequence]]s.


## Definition#

* A [[functor]] $F : C \to D$ is **right exact** if for all [[objects]] $d \in D$ the [[comma category]] $F/d$ is [[filtered category|filtered]].

* A [[functor]] $F : C \to D$ is **left exact** if for all [[objects]] $d \in D$ the [[opposite category|opposite]] [[comma category]] $(d/F)^{op}$ is [[filtered category|filtered]].

* A [[functor]] is **exact** if it is both left and right exact.


+-- {: .un_prop}
###### Proposition

A left exact functor preserves every [[finite limit]] that exists in $C$.

If $C$ admits all [[finite limits]] then a functor is left exact if and only if it preserves these limits.  

=--

+-- {: .un_prop}
###### Proposition

A functor between categories with finite limits preserves [[finite limit]]s if and only if:

* it preserves [[terminal objects]], binary [[product]]s, and [[equalizer]]s; or

* it preserves [[terminal object]]s and binary [[pullback]]s.

=--


Since these conditions frequently come up individually, it may be worthwhile listing them separately: 

* $F: C \to D$ **preserves terminal objects** if $F(t_C)$ is terminal in $D$ whenever $t_C$ is terminal in $C$; 

* $F: C \to D$ **preserves binary products** if the pair of maps 
$$F(c) \stackrel{F(\pi_1)}{\leftarrow} F(c \times d) \stackrel{F(\pi_2)}{\to} F(d)$$ 
exhibits $F(c \times d)$ as a product of $F(c)$ and $F(d)$, where $\pi_1: c \times d \to c$ and $\pi_2: c \times d \to d$ are the product projections in $C$; 

* $F: C \to D$ **preserves equalizers** if the map 
$$F(i): F(e) \to F(c)$$ 
is the equalizer of $F(f), F(g): F(c) \stackrel{\to}{\to} F(d)$, whenever $i: e \to c$ is the equalizer of $f, g: c \stackrel{\to}{\to} d$ in $C$. 
 


## Terminology

Frequently the term "left exact" is restricted to the case that $C$ has all [[finite limits]]. If so,  then the general case is called a [[flat functor]]. 

+-- {: .query}
Conceivably, it might be used also in the more general case, but to refer to a weaker notion: a functor that preserves those finite limits that exist.  Certainly that\'s how I would interpret 'finitely continuous functor'.  ---Toby
=--

'Left exact' is sometimes abbreviated **lex**.  In particular, [[Lex]] is the 2-category of categories with [[finite limits]] and lex functors.  See also [[continuous functor]].   Similarly, but more rarely, 'right exact' is sometimes abbreviated as **rex**.

## Between abelian categories



+-- {: .un_prop}
###### Proposition

A functor $F : C \to D$ between [[abelian categories]] is left exact if and only if it preserves [[direct sums]] and [[kernels]]. 

A functor $F : C \to D$ between [[abelian categories]] is right exact if and only if it preserves [[direct sums]] and [[cokernels]].  

=--

In particular for $0 \to A \to B \to C \to 0$ is an [[exact sequence]] in the abelian category $C$, we have that 

* if $F$ is left exact then 

  $$
    0 \to F(A) \to F(B) \to F(C)
  $$

  is an exact sequence in $D$;

* if $F$ is right exact then 

  $$
    F(A) \to F(B) \to F(C) \to 0
  $$

  is an exact sequence in $D$;

* if $F$ is exact then 

  $$
    0 \to F(A) \to F(B) \to F(C) \to 0
  $$

  is an exact sequence in $D$.

Also: if $F$ is exact then it preserves [[chain homology]].

## In higher category theory

The notion of exact functor has straightforward analogs in [[higher category theory]].

For [[(∞,1)-category]] theory see [[exact (∞,1)-functor]].


## References

A general discussion is for instance section 3.3 of

* Kashiwara, Schapira, _[[Categories and Sheaves]]_

A detailed discussion of how the property of a functor being exact is related to the property of it preserving homology in generalized situations is in 

* [[Michael Barr]], _Preserving homology_ , Theory and Applications of Categories,  Vol. 16, 2006, No. 7, pp 132-143. ([TAC](http://www.tac.mta.ca/tac/volumes/16/7/16-07abs.html))


[[!redirects left exact]]
[[!redirects left exact functor]]
[[!redirects lex functor]]
[[!redirects right exact functor]]
[[!redirects right exact functor]]
[[!redirects rex functor]]