#Contents#
* table of contents
{:toc}

## Idea

Let $(X, O_X)$ be a [[ringed space]].  In analogy with [[modules]] over a [[commutative ring]], one may study $(X, O_X)$ by studying the category $Mod(O_X)$ of [[sheaf of modules|sheaves of modules]] over $O_X$.  There is a [[symmetric monoidal model category|symmetric monoidal]] [[cofibrantly generated model category|cofibrantly generated]] [[model structure]] on $Mod(O_X)$.  The [[homotopy category]] with respect to this model structure, i.e. the [[derived category]] of $Mod(O_X)$, is a [[triangulated category]] $D(Mod(O_X))$ associated to $X$.  Here we discuss various interesting subcategories of $D(Mod(O_X))$.  In particular, the bounded derived category of coherent sheaves is an important invariant studied by the school of [[Bondal]], [[Orlov]] and others.  The triangulated category of perfect complexes is a very significant construction in [[noncommutative algebraic geometry]].

## Derived category of quasi-coherent sheaves

Recall that one has the full abelian subcategory $QCoh(O_X) \subset Mod(O_X)$ of [[quasi-coherent sheaves]], which are the ones corresponding locally to [[modules]] over a [[ring]].  One gets a triangulated subcategory $D(QCoh(O_X)) \subset D(Mod(O_X))$.

## Derived category of coherent sheaves

When $X$ is a [[noetherian scheme]], one has the full abelian subcategory $Coh(O_X) \subset QCoh(O_X)$ of [[coherent sheaves]]; these are the ones corresponding locally to [[finitely generated modules]].  Hence one gets the triangulated subcategory $D(Coh(O_X)) \subset D(QCoh(O_X))$.

## Bounded derived category of coherent sheaves

Let $X$ be a [[noetherian scheme]] and let $D^b(Coh(O_X))$ denote the [[bounded derived category]] of $Coh(O_X)$.

+-- {: .num_prop}
###### Proposition
The canonical [[fully faithful]] [[functor]]
  $$ D^b(Coh(O_X)) \hookrightarrow D(Mod(O_X)) $$
identifies $D^b(Coh(O_X))$ with the full subcategory of $D(Mod(O_X))$ of [[bounded complexes]] whose [[cohomology]] objects are [[coherent sheaves]].
=--

See [(SGA 6, Exp. II, Corollaire 2.2.2.1)](#SGA6).

## Triangulated category of perfect complexes

Let $X$ be a [[ringed space]] and let $Pf(X) \subset D(Mod(O_X))$ denote the full subcategory of [[perfect complexes]] of $O_X$-modules.  This is a [[triangulated subcategory]] that is contained in $D_{coh}(Mod(O_X)) \subset D(Mod(O_X))$, the full subcategory of complexes with [[coherent sheaf|coherent]] [[cohomology]].  It is stable under [[derived tensor product]], [[derived inverse image]], and [[derived direct image]] of [[proper morphisms]].

+-- {: .num_prop}
###### Proposition
If $X$ is a [[smooth scheme]], there is a canonical [[equivalence]]
  $$ Pf(X) \stackrel{\sim}{\to} D^b(Coh(O_X)) $$
of [[triangulated categories]].
=--

See [(SGA 6, Exp. I)](#SGA6).

## Facts

The bounded derived category of coherent sheaves $D^b(Coh(O_X))$ is an important invariant of $X$.  

+-- {: .num_theorem}
###### Theorem
Let $X$ and $Y$ be [[smooth scheme|smooth]] [[projective scheme|projective]] [[varieties]] over a [[field]] $K$.  Suppose that the [[canonical sheaf]] of $X$ is [[ample]] or anti-ample.  Then if there is a triangulated equivalence $D^b(Coh(O_X)) \simeq D^b(Coh(O_Y))$, then $X$ is isomorphic to $Y$.
=--

See [[Bondal-Orlov reconstruction theorem]].

## References

* [[SGA 6]]
{#SGA6}

For the [[model structure]] on $Mod(O_X)$, see [[model structure on chain complexes]] and in particular

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([url](http://www.intlpress.com/HHA/v11/n1/a11/))
{#CisinskiDeglise}

### Triangulated category of perfect complexes

* [[Luc Illusie]]. _Le complexe cotangent I et II_, Lecture Notes in Math. 239, 283, Springer-Verlag, Berlin (1971,1972).

* [[R. Thomason]], T. Trobaugh. _Higher algebraic K-theory of schemes and of derived categories_. The Grothendieck Festschrift, Vol. III Birkh&#168;auser, Boston (1990), 247-436.

* [[Andre Hirschowitz]], [[Carlos Simpson]].  _Descente pour les n-champs_, [arXiv:math/9807049](http://arxiv.org/abs/math/9807049)

* [[Stacks Project]], [tag 08CL](http://stacks.math.columbia.edu/tag/08CL)

[[!redirects triangulated category of sheaves]]
[[!redirects triangulated category of perfect complexes]]