
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

__Foliated categories__ (French: *catégories feuilletées*), or simply __foliations__ (not to be confused with the notion of [[foliations]] in [[differential geometry]]), were introduced by [[Jean Bénabou]] in unpublished work dating back to 1984.

They are a weaker [[structure]] than [[fibered categories]], but still allow one to test for various standard properties of [[functors]] [[fibre]]-wise.


## Definition

A [[functor]] $P\colon \mathbf{X} \to \mathbf{B}$ makes its [[domain]] [[category]] $\mathbf{X}$ a *foliated category* (over $\mathbf{B}$) if the following conditions hold:

1. Every [[morphism]] $f$ in $\mathbf{X}$ factors as a $P$-vertical morphism $v$ (i.e. $P(v)$ is an identity morphism in $\mathbf{B}$), followed by a [weak](Cartesian+morphism+WeakCartesianMorphisms) $P$-[[cartesian morphism]] $k$, i.e. $f = k\circ v$, 

1. The [[class]] of [weak](Cartesian+morphism+WeakCartesianMorphisms) $P$-[[cartesian morphisms]] is closed under [[composition]]. 


If closure under composition is not required, we obtain the notion of **prefoliated category**.

A morphism between foliated categories $\mathbf{X}'\to \mathbf{X}$ (over $\mathbf{B}$) is a functor over $\mathbf{B}$ that sends cartesian morphisms to cartesian morphisms, and such that for every object $X'$ of $\mathbf{X}'$, and morphism $f\colon Y\to F(X')$ in $\mathbf{X}$, there is a factorisation $f = F(k)\circ v$, where $v$ is vertical in $\mathbf{X}$ and $k$ is cartesian in $\mathbf{X}'$. Bénabou calls such functors _cartesian_.

## In indexed form
While every functor $P: X \to B$ corresponds to a normal lax functor $dP : B^{\mathrm{op}} \to \mathbf{Prof}$, foliated categories can be characterized as those that factor through the inclusion $\mathbf{ParCat} \to \mathbf{Prof}$, where $\mathbf{ParCat}$ is the 2-category of [[partial functor|partial functors]].

Indeed, the only obstruction to full representability of the profunctors $dP(h)$, with $h:b \to b'$ in the base $B$, is the existence of all weak cartesian lifts: the domain of definition of the partial functor corresponding to $dP(h)$ will be spanned by those objects $p \in dP(b')$ that admit a weak cartesian lift (this corresponds to Axiom 1 above). Axiom 2 then assures the laxator is well-defined.

## References

* [[Jean Bénabou]], _Cartesian functors and foliated categories_, talk at Oxford (1 May 2012) &lbrack;[YouTube](https://www.youtube.com/watch?v=Y1CeHmjNcuk)&rbrack;

* [[Jean Bénabou]], _Foncteurs cartésiens et catégories feuilletées_, talk at *Journée Guitart*, Paris (9 November 2012) &lbrack;[YouTube](https://www.youtube.com/watch?v=p3vcZDyZ4Yo), [slides](https://docs.google.com/presentation/d/17E0epsZWcDTYlwAMZ4PFCLIf4dyigS-WUA0siUtU-wY/edit?hl=fr#slide=id.gce595186_059), [[Benabou-FoliatedCategories.pdf:file]]&rbrack;

* [[Jean Bénabou]], _Du vieux et du neuf sur la construction de Grothendieck_, talk at Paris-Diderot (March 2019) &lbrack;[YouTube](https://youtu.be/NC0I18B45kE)&rbrack; 

  > (the material on foliated categories -- called simply foliations --- starts at 1:01:00).

A short summary is in [this message](https://github.com/punkdit/categories/blob/master/gmane/science/mathematics/categories/8243) on the Category Theory Mailing List.

[[!redirects foliated categories]]
[[!redirects prefoliated category]]
[[!redirects prefoliated categories]]