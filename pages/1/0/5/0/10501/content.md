
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $(X, O_X)$ be a [[ringed space]].  In analogy with [[modules]] over a [[commutative ring]], one may study $(X, O_X)$ by studying the category $Mod(O_X)$ of [[sheaf of modules|sheaves of modules]] over $O_X$.  There is a [[symmetric monoidal model category|symmetric monoidal]] [[cofibrantly generated model category|cofibrantly generated]] [[model structure]] on $Mod(O_X)$.  The [[homotopy category]] with respect to this model structure, i.e. the [[derived category]] of $Mod(O_X)$, is a [[triangulated category]] $D(Mod(O_X))$ associated to $X$.  Here we discuss various interesting subcategories of $D(Mod(O_X))$.  In particular, the bounded derived category of coherent sheaves is an important invariant studied by the school of [[Bondal]], [[Orlov]] and others.  The triangulated category of perfect complexes is a very significant construction in [[noncommutative algebraic geometry]].

## Definitions

### Derived category of quasi-coherent sheaves

Recall that one has the [[full subcategory|full]] [[abelian category|abelian]] [[subcategory]] $QCoh(O_X) \subset Mod(O_X)$ of [[quasi-coherent sheaves]], which are the ones corresponding locally to [[modules]] over a [[ring]].  One gets a triangulated subcategory $D(QCoh(O_X)) \subset D(Mod(O_X))$.

### Derived category of coherent sheaves

When $X$ is a [[noetherian scheme]], one has the full abelian subcategory $Coh(O_X) \subset QCoh(O_X)$ of [[coherent sheaves]]; these are the ones corresponding locally to [[finitely generated modules]].  Hence one gets the triangulated subcategory $D(Coh(O_X)) \subset D(QCoh(O_X))$.

### Bounded derived category of coherent sheaves

Let $X$ be a [[noetherian scheme]] and let $D^b(Coh(O_X))$ denote the [[bounded derived category]] of $Coh(O_X)$.

+-- {: .num_prop}
###### Proposition
The canonical [[fully faithful]] [[functor]]
  $$ D^b(Coh(O_X)) \hookrightarrow D(Mod(O_X)) $$
identifies $D^b(Coh(O_X))$ with the [[full subcategory]] of $D(Mod(O_X))$ of [[bounded complexes]] whose [[cohomology]] objects are [[coherent sheaves]].
=--

See [(SGA 6, Exp. II, Corollaire 2.2.2.1)](#SGA6).

### Triangulated category of perfect complexes

Let $X$ be a [[ringed space]] and let $Pf(X) \subset D(Mod(O_X))$ denote the [[full subcategory]] of [[perfect complexes]] of $O_X$-[[modules]].  This is a [[triangulated subcategory]] that is contained in $D_{coh}(Mod(O_X)) \subset D(Mod(O_X))$, the full subcategory of complexes with [[coherent cohomology]].  It is stable under [[derived tensor product]], [[derived inverse image]], and [[derived direct image]] of [[proper morphisms]].

+-- {: .num_prop}
###### Proposition
If $X$ is a [[smooth scheme]], there is a canonical [[equivalence]]
  $$ Pf(X) \stackrel{\sim}{\to} D^b(Coh(O_X)) $$
of [[triangulated categories]].
=--

See [(SGA 6, Exp. I)](#SGA6).

## Derived equivalence

The bounded derived category of coherent sheaves $D^b(Coh(O_X))$ is usually called simply the **derived category of $X$** and denoted $D(X)$.  It is an important invariant of $X$, which has been studied extensively by [[Mukai]], [[Bondal]]-[[Orlov]], and others.

There are several geometrically interesting examples of non-isomorphic [[varieties]] $X$ and $Y$ with $D(X) \simeq D(Y)$; for example, the derived category of an [[abelian variety]] $X$ is equivalent to the derived category of its dual $\hat{X}$.  In such cases one often says that $X$ and $Y$ are **derived equivalent**.  However, the derived category is not a weak invariant of $X$, indeed in some cases it is as strong as isomorphism; see [[Bondal-Orlov reconstruction theorem]].  In fact, the construction $X \mapsto D(X)$ seems to lose just enough information so that derived equivalence becomes a geometrically interesting invariant.

### Fourier-Mukai functors

+-- {: .num_thm}
###### Theorem ([[Orlov]])
Let $X$ and $Y$ be smooth projective [[varieties]] over a [[field]] $K$.  Let $F : D(X) \to D(Y)$ be a [[triangulated functor|triangulated]] [[fully faithful functor]].  There exists an object $E \in D(X \times Y)$ which is unique up to isomorphism and is such that $F$ is isomorphic to the [[Fourier-Mukai transform]] of $E$, that is the functor
  $$ F \mapsto Rq_*(Lp^*(F) \otimes^L E)) $$
where $p : X \times Y \to X$ and $q : X \times Y \to Y$ are the [[projections]].
=--

See [[Fourier-Mukai functor]] for details.

### Derived invariants

Let us say that a functor on the category of smooth projective [[varieties]] is a **derived invariant** if it maps derived equivalent varieties to isomorphic objects.

* The [[canonical ring]] is a derived invariant [(Orlov 2003)](#OrlovSurvey).

* [[Orlov]] has proved that for [[abelian varieties]], the functor $X \mapsto X \times \hat{X}$ is a derived invariant [(Orlov 2003)](#OrlovSurvey).

* [[Rouquier]] has proved that the functor $X \mapsto Pic^0(X) \rtimes Aut^0(X)$ valued in [[algebraic groups]] is a derived invariant [(Rouquier 2010)](#Rouquier2010).  (Note that this a generalization of Orlov's result on abelian varieties above.)

* [[Orlov]] has proved that the derived category $D(X)$ determines the rational [[Chow motive]] $M(X)$ up to [[Tate twists]].  Under a certain condition on the [[Fourier-Mukai functor|corresponding]] object $E \in D(X \times Y)$, this may be refined to derived invariance of the integral [[Chow motive]].  In particular the corresponding statements are true for any [[Weil cohomology theory]] (e.g. [[etale cohomology]], [[Betti cohomology]], [[de Rham cohomology]], etc.).  See [(Orlov, 2005)](#Orlov2005).

* The derived category $D(X)$ determines the [[noncommutative Chow motive]] $NM(X)$ up to isomorphism.  In particular, it follows that all [[additive invariants]], like [[K-theory]] or [[Hochschild homology]], are derived invariants.  See [(Yusufzai)](#Yusufzai).


## Related concepts

* [[abelian sheaf cohomology]]

* [[derived category of coherent sheaves]]

* [[perfect complex]]

* [[deformation theory of sheaves]]

## References

* [[SGA 6]]
{#SGA6}

For the [[model structure]] on $Mod(O_X)$, see [[model structure on chain complexes]] and in particular

* [[Denis-Charles Cisinski]], F. D&#233;glise, _Local and stable homologial algebra in Grothendieck abelian categories_, Homology, Homotopy and Applications, vol. 11 (1) (2009)  ([url](http://www.intlpress.com/HHA/v11/n1/a11/))
{#CisinskiDeglise}

### Derived categories of quasi-coherent sheaves

* [[R. Thomason]], T. Trobaugh. _Higher algebraic K-theory of schemes and of derived categories_. The Grothendieck Festschrift, Vol. III Birkh&#168;auser, Boston (1990), 247-436.

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc., vol. 9, no. 1, 1996, pp. 205-236, [doi](http://dx.doi.org/10.1090/S0894-0347-96-00174-9).

### Bounded derived category of coherent sheaves

For a summary of the results of [[Bondal]]-[[Orlov]], see

* [[Aleksei Bondal]], [[Dmitri Orlov]], _Derived categories of coherent sheaves_, [arXiv](http://arxiv.org/abs/math/0206295).

For a detailed survey, see

* [[Dmitri Orlov]], _Derived categories of coherent sheaves and equivalences between them_, Russian Math. Surveys, 58 (2003), 3, 89-172, [translation](http://www.mi.ras.ru/~orlov/papers/Uspekhi2003.pdf).
 {#OrlovSurvey}

On the relationship between derived categories and Chow motives, see

* [[Dmitri Orlov]], _Derived categories of coherent sheaves and motives_.
[math.AG/0512620](http://arxiv.org/abs/math/0512620)

For some discussion of the above result and the relationship between derived categories and [[additive invariants]] see

* [[Adeel Khan Yusufzai]], _Perfect correspondences and Chow motives_, master's thesis, 2013.  [arXiv](http://arxiv.org/abs/1310.0249).

For the derived invariance of $Pic^0 \rtimes Aut^0$, see

* [[Rouquier]], _Automorphismes, graduations et categories triangulees_, [arXiv](http://arxiv.org/abs/1008.1971).

### Triangulated category of perfect complexes

* [[Luc Illusie]]. _Le complexe cotangent I et II_, Lecture Notes in Math. 239, 283, Springer-Verlag, Berlin (1971,1972).

* [[Andre Hirschowitz]], [[Carlos Simpson]].  _Descente pour les n-champs_, [arXiv:math/9807049](http://arxiv.org/abs/math/9807049)

* [[Stacks Project]], [tag 08CL](http://stacks.math.columbia.edu/tag/08CL)

[[!redirects triangulated category of sheaves]]
[[!redirects triangulated category of perfect complexes]]
[[!redirects bounded derived category of coherent sheaves]]