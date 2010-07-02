
<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
</div>

#Contents#
* tic
{: toc}


## Idea 

A functor is left _exact_ or [[flat functor|flat]] if it preserves [[finite limit]]s


##Definition#

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
 




+-- {: .un_prop}
###### Proposition

A functor between [[abelian categories]] is left exact if and only if it preserves [[direct sums]] and [[kernels]]. 

A functor between [[abelian categories]] is right exact if and only if it preserves [[direct sums]] and [[cokernels]].  

=--


##Terminology

Frequently the term "left exact" is restricted to the case that $C$ has all [[finite limits]]. If so,  then the general case is called a [[flat functor]]. 

+-- {: .query}
Conceivably, it might be used also in the more general case, but to refer to a weaker notion: a functor that preserves those finite limits that exist.  Certainly that\'s how I would interpret 'finitely continuous functor'.  ---Toby
=--

Left exactness is sometimes abbreviated **lex**.  In particular, [[Lex]] is the 2-category of categories with finite limits and lex functors.  See also [[continuous functor]].

## In higher category theory

The notion of exact functor has straightforward analogs in [[higher category theory]].

For [[(∞,1)-category]] theory see [[exact (∞,1)-functor]].


##References

for instance section 3.3 of

* Kashiwara, Schapira, [[Categories and Sheaves]]


[[!redirects left exact functor]]
[[!redirects lex functor]]
[[!redirects right exact functor]]
[[!redirects rex functor]]