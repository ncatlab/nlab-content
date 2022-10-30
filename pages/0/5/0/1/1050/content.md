
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

In homological algebra, a central place is played by [[exact sequence]]s, (originally of modules), and the fact that various functors preserve or destroy exactness to some extent gave vital information on those functors.

In this context, one says that an **exact functor** is one that preserves exact sequences.  However, many functors are only "exact on one side or the other".  For instance, for all modules $M$ and short [[exact sequence]]s $0 \to A \to B \to C \to 0$  of modules (over some ring $R$), the sequence

$$0 \to Mod_R(M, A) \to Mod_R(M,B) \to Mod_R(M,C)$$ 

is exact, (but note no right hand 0).  Thus $F(-) = Mod_R(M,-)$ converts an exact sequence into a left exact sequence; such a functor is called a **left exact functor**.  Dually, one has **right exact functors**.

It is easy to see that an [[additive functor]] between [[additive categories]] is left exact if and only if it preserves finite limits.  Since merely preserving left exact sequences does not require a functor to be additive, in a non-additive context one defines a **left exact functor** to be one which preserves finite limits, and dually.


## Definition#

A [[functor]] between [[finitely complete categories]] is called __left exact__ (or [[flat functor|flat]]) if it preserves [[finite limits]].  Dually, a functor between finitely cocomplete categories is called __right exact__ if it preserves [[finite colimits]].  A functor is called __exact__ if it is both left and right exact.

Specifically, [[Ab]]-[[enriched functor]]s between [[abelian categories]] are exact if they preserve [[exact sequence]]s.


##Characterisations

+-- {: .un_prop}
###### Proposition
* A [[functor]] $F : C \to D$ between finitely cocomplete categories is right exact if and only if for all [[objects]] $d \in D$ the [[comma category]] $F/d$ is [[filtered category|filtered]].

* A [[functor]] $F : C \to D$ between finitely complete categories is left exact if and only if for all [[objects]] $d \in D$ the [[opposite category|opposite]] [[comma category]] $(d/F)^{op}$ is [[filtered category|filtered]].
=--

In other language, this says that a functor between finitely complete categories is left exact if and only if it is (representably) [[flat functor|flat]].  Conversely, one can show that a representably flat functor preserves all finite limits that exist in its domain.

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
 


+-- {: .un_remark}
###### Terminology

Some author use the term "left exact" when $C$ does not have all [[finite limits]], defining it to mean a [[flat functor]]. 

'Left exact' is sometimes abbreviated **lex**.  In particular, [[Lex]] is the 2-category of categories with [[finite limits]] and lex functors.  See also [[continuous functor]].   Similarly, but more rarely, 'right exact' is sometimes abbreviated as **rex**.

Left exact functors correspond to [[pro-representable functors]], provided some smallness conditions are satisfied. 

=--

## Properties

### On abelian categories


+-- {: .un_prop}
###### Proposition

A functor $F : C \to D$ between [[abelian categories]] is left exact if and only if it preserves [[direct sums]] and [[kernels]]. 

A functor $F : C \to D$ between [[abelian categories]] is right exact if and only if it preserves [[direct sums]] and [[cokernels]].  

=--

+-- {: .un_corollary}
###### Corollary

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

=--





## Related concepts

* **exact functor**

*  [[exact (∞,1)-functor]]


## References


An early use of _left exact_ and _exact_ is in:

*  [[A. Grothendieck]], 1959, _Technique de descente et th&#233;or&#232;mes d'existence 
en g&#233;om&#233;trie alg&#232;brique. II. Le th&#233;or&#232;me d'existence en th&#233;orie formelle
des modules_, in S&#233;minaire Bourbaki, Vol. 5 , Exp. No. 195, 369 &#8211; 390, 
Soc. Math. France [Numdam](http://www.numdam.org/numdam-bin/item?id=SB_1958-1960__5__369_0), Paris. 




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
