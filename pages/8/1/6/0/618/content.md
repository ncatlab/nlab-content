
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea 

A **coverage** on a [[category]] $C$ consists of, for each object $U\in C$, a collection of families $\{f_i \colon U_i\to U\}_{i\in I}$ of [[morphisms]] with [[target]] $U$ to be thought of as [[cover|covering families]].  The essential characteristic of these covering families is that they be "stable under [[base change|pullback]]."  A number of other "saturation" conditions are frequently also imposed for convenience.  A category equipped with a coverage is called a [[site]].

One of the main purposes of a coverage is that it provides the minimum structure necessary to define a notion of [[sheaf]] (or more generally [[stack]]) on $C$.  A [[Grothendieck topos]] is defined to be the category of sheaves (of sets) on a small site.  From this perspective, the example to keep in mind is the [[partial order|poset]] $O(X)$ of open sets in some [[topological space]] (or [[locale]]) $X$, where a morphism is an inclusion, and a family of inclusions $\{U_i \hookrightarrow U\}$ is a covering family iff $U = \bigcup_i U_i$.

Another perspective on a coverage is that the covering families are "postulated well-behaved quotients."  That is, saying that $\{f_i:U_i\to U\}_{i\in I}$ is a covering family means that we want to think of $U$ as a well-behaved quotient (i.e. colimit) of the $U_i$.  Here "well-behaved" means primarily "stable under pullback."  In general, $U$ may or may not _actually_ be a colimit of the $U_i$; if it always is we call the site _[[subcanonical coverage|subcanonical]]_.  From this perspective, the embedding of $C$ into its category of sheaves is "the free cocompletion of $C$ that takes covering families to well-behaved quotients"; compare how the [[Yoneda embedding]] of an arbitrary category $C$ into its category of [[presheaf|presheaves]] is its [[free cocompletion]], period.

The traditional name for a coverage, with the extra saturation conditions imposed, is a [[Grothendieck topology]], and this is still widely used in mathematics.  Following the [[Elephant]], on this page we use _coverage_ for a pullback-stable system of covering families and _Grothendieck coverage_ if the extra saturation conditions are imposed.  See [[Grothendieck topology]] for a discussion of the objections to that term. 

A related notion is that of [[basis for a Grothendieck topology]], which is similar to the notion of coverage, and similarly induces a Grothendieck topology, but assumes existence of [[pullback]]s and closure of covering families under these pullbacks.


## Definition  
 {#Definition}



+-- {: .num_defn #ConditionsOnACoverage}
###### Definition

A **coverage** on a [[category]] $C$ consists of a [[function]] assigning to each [[object]] $U\in C$ a collection of families of [[morphisms]] $\{f_i:U_i\to U\}_{i\in I}$, called _[[covering]] families_, such that

* If $\{f_i:U_i\to U\}_{i\in I}$ is a covering family and $g:V\to U$ is a morphism, then there exists a covering family $\{h_j:V_j\to V\}$ such that each composite $g h_j$ factors through some $f_i$.

$$
  \array{
    V_j &\overset{k}{\longrightarrow}& U_i
    \\
    \mathllap{{}^{h_j}}\big\downarrow & & \big\downarrow\mathrlap{^{f_i}}
    \\
    V &\underset{g}{\longrightarrow}& U
  }
  \;\;.
$$

(NB. The logic here is: $\forall f, \forall g, \exists h, \forall j, \exists i, \exists k \colon$ such that the above [[commuting diagram|diagram commutes]].)

=--

+-- {: .num_defn}
###### Definition


A [[site]] is a category equipped with a coverage.  

=--

Often [[site]]s are required to be [[small category|small]]; see [[large site]] for complications that may otherwise arise.


### Sheaves on a site 

See [[sheaf]], of course, but it seems appropriate to briefly recall the concept here.  If $\{f_i:U_i\to U\}_{i\in I}$ is a family of morphisms with codomain $U$, a [[presheaf]] $X:C^{op}\to Set$ is called a **sheaf** for this family if

* For any collection of elements $x_i \in X(U_i)$ such that, whenever $g:V\to U_i$ and $h:V\to U_j$ are such that $f_i g = f_j h$, we have $X(g)(x_i) = X(h)(x_j)$, then there exists a unique $x\in X(U)$ such that $X(f_i)(x)=x_i$ for all $i$.

If $C$ is a site, a presheaf $X:C^{op}\to Set$ is called a **sheaf** on $C$ if it is a sheaf for every covering family in $C$.  We call a site $C$ **[[subcanonical coverage|subcanonical]]** if every representable functor $C(-,c):C^{op}\to Set$ is a sheaf.

The [[category of sheaves]] $Sh(C)$ is a full [[subcategory]] of the category $[C^{op},Set]$ of presheaves.  If $C$ is [[subcanonical coverage|subcanonical]], then its [[Yoneda embedding]] $C\to [C^{op},Set]$ factors through $Sh(C)$.  If $C$ is small, then $Sh(C)$ is [[reflective subcategory|reflective]] in $[C^{op},Set]$ and a [[Grothendieck topos]].


### Sites with pullbacks
{#cartesian}

If, as is frequently the case, $C$ has [[pullback|pullbacks]], then it is natural to impose the following stronger condition:

* If $\{f_i:U_i\to U\}_{i\in I}$ is a covering family and $g:V\to U$ is a morphism, then the family of pullbacks $\{g^*(f_i):g^*U_i\to V\}$ is a covering family of $V$.

One can also impose the weaker condition that the pullbacks of covering families exist and are covering families, even if not all pullbacks exist in $C$.  The saturation conditions below imply that on a category with pullbacks, every coverage is equivalent to one satisfying this stronger condition, which perhaps we may call a __cartesian coverage__.

Likewise, when $C$ has pullbacks (of covering families), the condition for a presheaf $X$ to be a sheaf for a covering family $\{f_i:U_i\to U\}_{i\in I}$ can be stated more simply (and probably more familiarly, to some readers), as the assertion that the following diagram is an [[equalizer]]:
\[
X(U) \to \prod_{i\in I} X(U_i) \rightrightarrows \prod_{j,k\in I} X(U_j\times_U U_k).
\]
The generalization to [[stack|stacks]] using [[cosimplicial object|cosimplicial objects]] is then straightforward.


### Saturation conditions 

The collection of covering families can be "closed up" under a number of convenient operations without changing the notion of sheaf.

1. Any presheaf is a sheaf for the singleton family $\{1_U:U\to U\}$.

1. Any presheaf which is a sheaf for a family $\{f_i:U_i\to U\}_{i\in I}$ and also for some family $\{h_{i j}:U_{i j} \to U_i\}_{j\in J_i}$ for each $i$ is also a sheaf for the family of all composites $\{f_i h_{i j}:U_{i j}\to U\}_{i\in I, j\in J_i}$.

1. Let $C$ be a site and $\{f_i:U_i\to U\}_{i\in I}$ a covering family, and suppose $\{g_j:V_j\to U\}_{j\in J}$ is a family of morphisms such that each $f_i$ factors through some $g_j$.  Then any sheaf $X$ on $C$ is also a sheaf for the family $\{g_j:V_j\to U\}_{j\in J}$.  _(NB: for this condition, it is essential that $\{f_i\}$ be part of a coverage and that $X$ be a sheaf for the entire coverage, not just for $\{f_i\}$.)_

1. For any family $\{f_i:U_i\to U\}_{i\in I}$, the [[sieve]] it generates is the family of all morphisms $g:V\to U$ which factor through some $f_i$.  A presheaf $X$ is a sheaf for $\{f_i\}$ iff it is a sheaf for the sieve it generates.


### Grothendieck coverages 


Grothendieck originally considered only coverages that are closed under some or all of the above saturation conditions.  

Because of the final condition, we may choose to consider only covering _sieves_.  Incorporating the other saturation conditions as well, we define a **Grothendieck coverage** (commonly called a [[Grothendieck topology]]) to be a collection of sieves called _covering sieves_, satisfying the following pullback-stability and saturation conditions.  (If $R$ is a sieve on $U$ and $g:V\to U$ is a morphism, we define $g^*(R)$ to be the sieve on $V$ consisting of all morphisms $h$ into $V$ such that $g h$ factors through some morphism in $R$.)

* If $R$ is a covering sieve on $U$ and $g:V\to U$ is any morphism, then $g^*(R)$ is a covering sieve on $V$.

* For each $U$ the sieve $M_U$ consisting of _all_ morphisms into $U$ (the sieve generated by the singleton family $\{1_U\}$) is a covering sieve.

* If $R$ is a covering sieve on $U$ and $S$ is an arbitrary sieve on $U$ such that for each $f:V\to U$ in $R$, $f^*(S)$  is a covering sieve on $V$, then $S$ is also a covering sieve on $U$.

One can then show that for every coverage, there is a _unique_ Grothendieck coverage having the same sheaves.  When $C$ is small, then Grothendieck coverages on $C$ are also in bijective correspondence with [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] on its presheaf topos $[C^{op},Set]$, and thus in bijection with [[subtopos|subtoposes]] of $[C^{op},Set]$. For more on this see [[category of sheaves]].

On the other hand, it is often useful to consider only pullback-stable covering families, without needing to close them up into sieves satisfying the saturation conditions.  For instance, in many cases the generating covering families will be finite and easy to describe.  As we saw above, the notion of sheaf can also be defined more explicitly in terms of covering families, especially when $C$ has pullbacks.

Frequently, though, these covering families will satisfy at least some of the saturation conditions.  The name [[Grothendieck pretopology]] or _basis for a Grothendieck topology_ is commonly used for a coverage (often of the stronger sort requiring pullbacks) that also satisfies

* Every isomorphism is a covering family.

* If $\{f_i:U_i\to U\}_{i\in I}$ is a covering family and for each $i$, so is $\{h_{i j}:U_{i j} \to U_i\}_{j\in J_i}$, then $\{f_i h_{i j}:U_{i j}\to U\}_{i\in I, j\in U_i}$ is also a covering family.


## Examples {#Examples}

* For $X$ a [[topological space]] and $Op(X)$ its [[category of open subsets]], the collection of [[open cover]]s is a [[subcanonical coverage|subcanonical]] coverage on $Op(X)$. I.e. a covering family on an open subset $U \subset X$ is a collection of further open subsets $\{U_i \subset X\}$ such that their union (in $X$) is $U$: $\cup_i U_i = U$. 

  This is the standard choice of coverage on $Op(X)$. Sheaves for this coverage are the usual notion of sheaf on a topological space.  

  A **[[basis for the topology]]** on $X$ is also a coverage on $X$, generating the same Grothendieck topology but in general not being closed under pullbacks (which in $Op(X)$ is intersection of open subsets). Notice that thence a basis for a topology on $X$ is not what is called a [[basis for a Grothendieck topology]] on $Op(X)$.

* Similarly on (any [[small category|small]] version of) the category [[Top]] or [[Diff]] or similar categories of topological spaces possibly with extra [[stuff, structure, property|structure]], [[open cover]]s form a coverage.

  Another choice of coverage is given by taking covering families to 
  consist of [[étale map]]s, i.e. of local [[homeomorphism]]s. Notice that
  every open cover $\{U_i \to X\}$ consist of local homeomorphisms and
  in addition gives the local homeomorphism 
  out of the [[coproduct]] $\coprod_i U_i \to X$.

* On [[Diff]] also 
  [[good open cover]]s form an equivalent coverage.   
  While good open covers are not stable under pullback in [[Diff]],
  every pullback of a good open cover gives an open cover that may be
  refined by a good open cover. This is all we need in the definition of
  coverage.

* There are many interesting coverages on the category of [[scheme|schemes]]; it was these examples which originally motivated Grothendieck to consider the notion. See [[fpqc topology]], etc.

* On any [[category]] there is the _[[trivial coverage]]_ which has no covering families at all.  Every presheaf is a sheaf for this coverage (and in particular, it is subcanonical).  The corresponding Grothendieck coverage consists of all sieves that contain a [[split epimorphism]].  (Note that every presheaf is a sheaf for any family containing a split epic.)

* On any [[regular category]] there is a coverage, called the _regular coverage_, whose covering families are the singletons $\{f:V\to U\}$ where $f$ is a [[regular epimorphism]].  It is subcanonical.

* On any [[coherent category]] there is a a coverage, called the _coherent coverage_, whose covering families are the finite families $\{f_i:U_i \to U\}_{1\le i\le n}$ the union of whose images is all of $U$.  It is subcanonical.  Likewise there is a _geometric coverage_ on any infinitary-coherent category.

* On any [[extensive category]] there is a coverage, called the _extensive coverage_, whose covering families are the inclusions into a (finite) coproduct.  It is subcanonical.  The coherent coverage on an extensive coherent category is generated by the union of the regular coverage and the extensive one.

* Any category has a _[[canonical coverage]]_, defined to be the largest subcanonical one.  (Hence the name "subcanonical" = "contained in the canonical coverage.")  The covering sieves for the canonical coverage are precisely those which are **universally effective-epimorphic**, meaning that their target is their colimit and this colimit is preserved by pullback.

* The canonical coverage on a [[Grothendieck topos]] coincides with its geometric coverage, and moreover every sheaf for this coverage is representable.  That is, a Grothendieck topos is a ([[large site|large]]) site which is equivalent to its own category of sheaves.


## Applications 

In addition to the construction of [[sheaf|sheaves]] and [[stack|stacks]], other (not unrelated) applications of coverages include:

* The definition of internal [[anafunctor|anafunctors]].

* The construction of [[folk model structure|model structures for internal categories]].


## In higher category theory

The notion of [[site]] and hence that of [[Grothendieck topology]], [[Grothendieck pretopology]] and coverage typically has its straightforward analogs in [[higher category theory]].

in [[(∞,1)-category theory]] the corresponding notion is that of [[(∞,1)-site]]. Such an $(\infty,1)$-site has correspondingly its [[(∞,1)-category of (∞,1)-sheaves]]. A discussion of a [[model category]] [[presentable (∞,1)-category|presentation]] of this in terms of localization at a coverage is at [[model structure on simplicial presheaves]] in the section <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage">Localization at a coverage</a>.

## Related concepts

* [[open cover]], [[good open cover]]

* [[closed cover]]

* [[quasi-net]]

## References 

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_ , especially section C2.1.

* [[Anders Kock]], _[Postulated colimits and left exactness of Kan-extensions](http://home.imf.au.dk/kock/postulated.pdf)_

[[!redirects coverages]]
