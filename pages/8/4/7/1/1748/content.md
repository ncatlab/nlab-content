

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

* This page is about homotopy as a transformation.  For homotopy sets in [[homotopy categories]], see [[homotopy (as an operation)]].

***

#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

In many [[category|categories]] $C$ in which one does [[homotopy theory]], there is a notion of _homotopy_ between morphisms, which is closely related to the higher morphisms in [[higher category theory]].  If we regard such a category as a presentation of an $(\infty,1)$-[[(infinity,1)-category|category]], then homotopies $f\sim g$ present the 2-cells $f\Rightarrow g$ in the resulting $(\infty,1)$-category.


# Definition in enriched categories #

If $C$ is [[enriched category|enriched]] over [[Top]], then a **homotopy** in $C$ between maps $f,g:X\,\rightrightarrows \,Y$ is a map $H:[0,1] \to C(X,Y)$ in $Top$ such that $H(0)=f$ and $H(1)=g$.  In $Top$ itself this is the classical notion.

If $C$ has [[copower|copowers]], then an equivalent definition is a map $[0,1]\odot X\to Y$, while if it has [[power|powers]], an equivalent definition is a map $X\to \pitchfork([0,1],Y)$.

There is a similar definition in a [[simplicially enriched category]], replacing $[0,1]$ with the 1-simplex $\Delta^1$, with the caveat that in this case not all _simplicial homotopies_ can be composed.  Likewise in a [[dg-category]] we can use the "chain complex interval" to get a notion of _chain homotopy_.


# Definition in model categories #

If $C$ is instead a [[model category]], it has an intrinsic notion of homotopy determined by its factorizations.

* A **[[path object]]** $Path(X)$ for an object $X$ is a factorization of the diagonal $X \to X \times X$ as
$$
  X \to Path(X) \to X \times X
  \,.
$$
where $X\to Path(X)$ is a weak equivalence.

* A **[[cylinder object]]** $Cyl(X)$ is a factorization of the codiagonal (or "fold") $X \sqcup X \to X$ as
$$
  X \sqcup X \to Cyl(X) \to X
  \,.
$$
where $Cyl(X) \to X$ is a weak equivalence.

Frequently one asks as well that $Path(X)\to X\times X$ be a fibration and $X\sqcup X\to Cyl(X)$ be a cofibration; we call such paths and cylinders _good_.  Clearly any object has a good path object and a good cylinder object.  However, in the usual [[model structure on topological spaces]], the obvious object $X\times I$ is a cylinder, but not a good cylinder unless $X$ itself is cofibrant.

We think of $Path(X)$ as an analogue of $\pitchfork(I,X)$ and $Cyl(X)$ as an analogue of $I\odot X$.  In fact, if $C$ is a $Top$-enriched model category and $X$ is cofibrant, then these powers and copowers  are in fact examples of path and cylinder objects.  (This works more  generally if $C$ is a $V$-model category and $e\sqcup e \to I \to e$ is a good cylinder object for the cofibrant unit object $e$ of $V$.)

+--{.query}
Are there any interesting consequences or conditions for the existence of an actual object $I$ that produces path objects and cylinder objects in that way?

One consequence of a well-behaved such object $I$ is the existence of model structures on categories of operads (Berger-Moerdijk 2003).

[[Urs Schreiber|Urs]]: I need to look at Berger-Moerdijk. Just yesterday I wrote down a definition of "category with interval object" myself in an attempt to capture precisely this idea. I said: 

**Definition**: a category $V$ with interval object is a [[closed monoidal homotopical category]] whose homotopical structure extends to a [[category of fibrant objects]] and eqipped with with $\sigma, \tau : pt \to I$ in $V$ an internal _co-category_ such that for every object $B$ the object $[I,B]$ is a path object of $B$.

Examples are essentially all categories $V$ of higher fibrant structures, I think, Kan complexes, higher categories, etc. The interval object is always the obvious one in these cases. There is an obvious generalization to the non-fibrant case, too, I think.

And in a category with interval object one can do a bunch of things that one would want to do with higher structures -- notably one can do nonabelian principal $\infty$-bundles, I think, as I try to describe [[schreiber:Nonabelian homotopical cohomology and fiber bundles|here]].


[[Tim Porter|Tim]] The question asked at the start of this query relates to a large part of the modelizer story which occupies quite a large part of Grothendieck's _Pursuit of Stacks_. For a discussion and quite a detailed treatment of cylinder bjects and the way in which their properties influence what homotopical theorem hold in that context you might look at my book with Heiner Kamps.

[[Urs Schreiber|Urs]]: may I ask that we move this discussion to [[interval object]] where it may have more room to develop in its own right, not just being an afterthought to this entry here. Tim: is maybe the answer to the question which I am asking at [[interval object]] in that book of yours which you mention? I will have a look.

=--

Then:

* A **left homotopy** between two morphisms $f,g : X \to Y$ in $C$ is a morphism $\eta : Cyl(X) \to Y$ such that
$$
  \array{
    X &\rightarrow& Cyl(X) &\leftarrow& X
    \\
    & {}_f\searrow &\downarrow^\eta& \swarrow_g
    \\
    && 
    Y
  }
  \,.
$$

* A **right homotopy** between two morphisms $f,g : X \to Y$ in $C$ is a morphism $\eta : X \to Path(Y)$ such that
$$
  \array{
    && X
    \\
    & {}^f\swarrow & \downarrow^\eta & \searrow^{g} 
    \\
    Y &\leftarrow& Path(Y) &\rightarrow& Y
  }
  \,.
$$

By the above remarks about powers and copowers, it follows that in a $Top$-model category, any enriched homotopy between maps $X\to Y$ is a left homotopy if $X$ is cofibrant and a right homotopy if $Y$ is fibrant.  Similar remarks hold for other enrichments.

# Remarks #

Path objects and right homotopies also exist in various other situations, for instance, if there is not the full structure of a [[model category]] but just of a [[category of fibrant objects]] is given.  Likewise for cylinder objects and left homotopies in a category of cofibrant objects.

Likewise if there is a [[cylinder functor]], one gets functorially defined [[cylinder object]]s. 

# References #



* W. G. Dwyer and J. Spalinski.  "Homotopy Theories and Model Categories," 1995.

* Clemens Berger and Ieke Moerdijk.  "Axiomatic homotopy theory for operads," 2003.

* K. H. Kamps and T. Porter, _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

[[!redirects left homotopy]]
[[!redirects right homotopy]]

[[!redirects left homotopies]]
[[!redirects right homotopies]]


[[!redirects homotopy (as a transformation)]]

[[!redirects homotopies]]