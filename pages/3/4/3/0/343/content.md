
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Definition

A __cartesian monoidal category__ (usually just called a **[[cartesian category]]**), is a [[monoidal category]] whose monoidal structure is given by the category-theoretic [[product]] (and so whose unit is a [[terminal object]]).  

A cartesian monoidal category which is also [[closed monoidal category|closed]] is called a [[cartesian closed category]]. 

A [[strong monoidal functor]] between cartesian categories is called a [[cartesian functor]].

Any category with finite products can be considered as a cartesian monoidal category (as long as we have either (1) a specified product for each pair of objects, (2) a global [[axiom of choice]], or (3) we allow the monoidal product to be an [[anafunctor]]).

The term __cartesian category__ usually means a category with finite products but can also mean a [[finitely complete category]], so we avoid that term.


## Properties

Cartesian monoidal categories have a number of special and important properties, such as the existence of diagonal maps $\Delta_x : x \to x\otimes x$ and augmentations $e_x: x \to I$ for any object $x$.  In applications to computer science we can think of $\Delta$ as 'duplicating data' and $e$ as 'deleting' data.  These maps make any object into a [[comonoid]].  In fact, any object in a cartesian monoidal category becomes a comonoid in a unique way.  

Moreover, one can show (e.g. [Fox 1976](#Fox76) or [Heunen-Vicary 2012, p. 79 (p. 85 of the pdf)](#HeunenVicary12)) that any [[symmetric monoidal category]] equipped with suitably well-behaved diagonals and augmentations _must_ in fact be cartesian monoidal.   More precisely: suppose $C$ is a symmetric monoidal category equipped with monoidal natural transformations
$$           \Delta_x : x \to x \otimes x $$
and
$$             e_x : x \to I   $$
such that the following composites are identity morphisms:
$$       x \stackrel{\Delta_x}{\longrightarrow} x \otimes x 
\stackrel{e_x \otimes 1}{\longrightarrow} I \otimes x 
\stackrel{\ell_x}{\longrightarrow} x $$
$$       x \stackrel{\Delta_x}{\longrightarrow} x \otimes x 
\stackrel{1 \otimes e_x}{\longrightarrow} x \otimes I 
\stackrel{r_x}{\longrightarrow} x $$
where $r$, $\ell$ are the right and left unitors.   Then $C$ is cartesian.  

Heuristically: a symmetric monoidal category is cartesian if we can duplicate and delete data, and 'duplicating a piece of data and then deleting one copy is the same as not doing anything'.

A related theorem describes cartesian monoidal categories as monoidal categories satisfying two properties involving the unit object.  First, we say a monoidal category $C$ is [[semicartesian monoidal category|semicartesian]] if the unit for the tensor product is [[terminal object|terminal]].   If this is true, any tensor product of objects $x \otimes y$ comes equipped with morphisms 
$$ p_x : x \otimes y  \to x $$
$$ p_y : x \otimes y \to y$$
given by
$$ x \otimes y \stackrel{1 \otimes e_y}{\longrightarrow} x \otimes I \stackrel{r_x}{\longrightarrow} x $$
and
$$ x \otimes y \stackrel{e_x \otimes 1}{\longrightarrow} I \otimes y \stackrel{\ell_y}{\longrightarrow} y $$
respectively, where $e$ stands for the unique morphism to the terminal object and $r$, $\ell$ are the right and left unitors.  We can thus ask whether $p_x$ and $p_y$ make $x \otimes y$ into the [[product]] of $x$ and $y$.  If so, it is a theorem that $C$ is a cartesian monoidal category.  (This theorem is probably in Eilenberg and Kelly's paper on closed categories, but they may not have been the first to note it.)

Cartesian categories may be [[freely generated]] from sets, categories, signatures, etc., as explained at [[free cartesian category]].

## Related concepts

* [[monoidal category]]

* [[symmetric monoidal category]]

* [[semicartesian monoidal category]]

* [[cocartesian monoidal category]]

* [[monoidal category with diagonals]]

* [[relevance monoidal category]]

* [[cartesian monoidal (∞,1)-category]]


## References

The characterization of cartesian monoidal categories as [[symmetric monoidal categories]] with [[extra structure]]:

* {#Fox76} [[Thomas Fox]], *Coalgebras and cartesian categories*, Communications in Algebra **4** 7 (1976) 665-667 ([doi:10.1080/00927877608822127](https://doi.org/10.1080/00927877608822127), [pdf](https://www.tandfonline.com/doi/pdf/10.1080/00927877608822127))


Discussion with an eye towards [[finite quantum mechanics in terms of dagger-compact categories]] is in

* {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], _Lectures on categorical quantum mechanics_, 2012 ([pdf](https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf))


[[!redirects cartesian monoidal category]]
[[!redirects cartesian monoidal categories]]

[[!redirects Cartesian monoidal category]]
[[!redirects Cartesian monoidal categories]]
