
> This entry is about the concept of "exact functors" in plain [[category theory]]. For the different concept of that name in [[triangulated category]] theory see at _[[triangulated functor]]_.

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
* table of contents
{: toc}


## Idea 

A left/right _exact functor_ is a [[functor]] that [[preserved limit|preserves]] [[finite limits]]/finite [[colimits]]. 

The term originates in [[homological algebra]], see remark \ref{OriginOfTerminology} below, where a central role is played by [[exact sequences]] (originally of [[modules]], more generally in any [[abelian category]]) and the fact that various [[functors]] preserve or destroy exactness of sequences to some extent gave vital information on those functors.

In this context, one says that an **exact functor** is one that preserves exact sequences.  However, many functors are only "exact on one side or the other".  For instance, for all modules $M$ and [[short exact sequences]] $0 \to A \to B \to C \to 0$  of modules (over some ring $R$), the sequence

$$0 \to Mod_R(M, A) \to Mod_R(M,B) \to Mod_R(M,C)$$ 

is exact -- but note that there is no 0 on the right hand.  Thus $F(-) = Mod_R(M,-)$ converts an exact sequence into a _left_ exact sequence; such a functor is called a **left exact functor**.  Dually, one has **right exact functors**.

It is easy to see that an [[additive functor]] between [[additive categories]] is left exact in this sense if and only if it preserves [[finite limits]].  

Since merely preserving left exact sequences does not require a functor to be additive, in a non-additive context one defines a **left exact functor** to be one which preserves finite limits, and dually. Below we give the [general definition](#Definition) and then discuss the relation to the concept in homological algebra in the section [Properties - On abelian categories](#OnAbelianCategories).


## Definition
 {#Definition}

A [[functor]] between [[finitely complete categories]] is called __left exact__ (or [[flat functor|flat]]) if it preserves [[finite limits]].  Dually, a functor between finitely cocomplete categories is called __right exact__ if it preserves [[finite colimits]].  A functor is called __exact__ if it is both left and right exact.

Specifically, [[Ab]]-[[enriched functor]]s between [[abelian categories]] are exact if they preserve [[exact sequence]]s.

## Properties


### Characterisations

#### General

+-- {: .num_prop}
###### Proposition
* A [[functor]] $F : C \to D$ between finitely cocomplete categories is right exact if and only if for all [[objects]] $d \in D$ the [[comma category]] $F/d$ is [[filtered category|filtered]].

* A [[functor]] $F : C \to D$ between finitely complete categories is left exact if and only if for all [[objects]] $d \in D$ the [[opposite category|opposite]] [[comma category]] $(d/F)^{op}$ is [[filtered category|filtered]].
=--

In other language, this says that a functor between finitely complete categories is left exact if and only if it is (representably) [[flat functor|flat]].  Conversely, one can show that a representably flat functor preserves all finite limits that exist in its domain.

+-- {: .num_prop}
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
 


+-- {: .num_remark}
###### Terminology

Some author use the term "left exact" when $C$ does not have all [[finite limits]], defining it to mean a [[flat functor]]. 

'Left exact' is sometimes abbreviated **lex**.  In particular, [[Lex]] is the 2-category of categories with [[finite limits]] and lex functors.  See also [[continuous functor]].   Similarly, but more rarely, 'right exact' is sometimes abbreviated as **rex**.

Left exact functors correspond to [[pro-representable functors]], provided some smallness conditions are satisfied. 

=--

#### Between categories of modules

Right exact functors between [[categories of modules]] are characterized by the _[[Eilenberg-Watts theorem]]_. See there for more details.

### On abelian categories / in homological algebra
 {#OnAbelianCategories}

In the context of [[homological algebra]], the notion of left/right exact functors is considered specifically in [[abelian categories]]. In this context the above formulation is equivalently formulated in terms of the behaviour of the functor on [[short exact sequences]]. We now discuss this case.

+-- {: .num_prop}
###### Proposition

A functor $F : C \to D$ between [[abelian categories]] is left exact if and only if it preserves [[direct sums]] and [[kernels]]. 

A functor $F : C \to D$ between [[abelian categories]] is right exact if and only if it preserves [[direct sums]] and [[cokernels]].  

=--

+-- {: .num_cor #ExactFunctorPreservesExactSequences}
###### Corollary

In particular for $0 \to A \to B \to C \to 0$ an [[exact sequence]] in the abelian category $C$, we have that 

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

+-- {: .proof}
###### Proof

We discuss the first case. The second is formally dual. The third combines the two cases.

For the first case notice that $0 \to A \stackrel{i}{\to} B \stackrel{p}{\to} C \to 0$ being an [[exact sequence]] is equivalent to $i$ being a [[monomorphism]] and $p$ being an [[epimorphism]], hence to $0 \to A$ being the [[kernel]] of $i$, $i$ being the kernel of $p$ and $C \to 0$ being the [[cokernel]] of $p$. Since the functor $F$ is assumed to preserve this kernel-property, but not the cokernel property, it follows that $F(0) \to F(A)$ is the kernel of $F(A) \stackrel{F(i)}{\to} F(B)$, but not more than that. This means that

$$
  0 \to F(A) \to F(B) \to F(C)
$$

is an exact sequence, as claimed.

=--


+-- {: .num_remark #OriginOfTerminology}
###### Remark

The properties of corollary \ref{ExactFunctorPreservesExactSequences} explain the "left"/"right"-terminology: a _left_ exact functor preserves exactness of sequences to the left of a morphism (only), while a _right_ exact functor preserves exactness to the right.

=--




## Related concepts

* [[LexCat]]

* [[derived functor]]

* [[exact (∞,1)-functor]]

* [[satellite]]

* [[exact category]]


## References

Early use of _left exact_ and _exact_:

* {#CartanEilenberg56} [[Henri Cartan]], [[Samuel Eilenberg]], *[[Homological Algebra]]*, Princeton Univ. Press (1956), Princeton Mathematical Series **19** (1999) &lbrack;[ISBN:9780691049915](https://press.princeton.edu/books/paperback/9780691049915/homological-algebra-pms-19-volume-19), [doi:10.1515/9781400883844](https://doi.org/10.1515/9781400883844), [pdf](http://www.math.stonybrook.edu/~mmovshev/BOOKS/homologicalalgeb033541mbp.pdf)&rbrack;
 

*  [[A. Grothendieck]], 1959, _Technique de descente et th&#233;or&#232;mes d'existence en g&#233;om&#233;trie alg&#232;brique. II. Le th&#233;or&#232;me d'existence en th&#233;orie formelle des modules_, in S&#233;minaire Bourbaki, Vol. 5 , Exp. No. 195, 369 &#8211; 390, 
Soc. Math. France [Numdam](http://www.numdam.org/numdam-bin/item?id=SB_1958-1960__5__369_0), Paris. 

General discussion

* [[Francis Borceux]], Section 6.1 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

* [[Masaki Kashiwara]], [[Pierre Schapira]], Section 3.3 in: _[[Categories and Sheaves]]_

See also:

* [[Michael Barr]], *Right exact functors*, J. Pure Appl. Algebra **4** (1974) 1–8 &lbrack;<a href="https://doi.org/10.1016/0022-4049(74)90025-5">doi:10.1016/0022-4049(74)90025-5</a>, [pdf](https://www.math.mcgill.ca/barr/papers/right.exact.pdf), [[Barr-ExactFunctors.pdf:file]]&rbrack;

A detailed discussion of how the property of a functor being exact is related to the property of it preserving homology in generalized situations:

* [[Michael Barr]], _Preserving homology_ , Theory and Applications of Categories,  Vol. 16, 2006, No. 7, pp 132-143. ([TAC](http://www.tac.mta.ca/tac/volumes/16/7/16-07abs.html))

Discussion of left exactness (or [[flat functor]]) in the context of [[(∞,1)-category theory]] is in 

* [[Jacob Lurie]], def. 5.3.2.1 in _[[Higher Topos Theory]]_


[[!redirects exact functors]]

[[!redirects left exact]]
[[!redirects left exact functor]]
[[!redirects left exact functors]]

[[!redirects lex functor]]
[[!redirects lex functors]]
[[!redirects lex]]

[[!redirects right exact functor]]
[[!redirects right exact functors]]

[[!redirects rex functor]]
[[!redirects rex functors]]
[[!redirects rex]]

[[!redirects finitely continuous]]
[[!redirects finitely continuous functor]]
[[!redirects finitely continuous functors]]
[[!redirects finitely cocontinuous]]
[[!redirects finitely cocontinuous functor]]
[[!redirects finitely cocontinuous functors]]

