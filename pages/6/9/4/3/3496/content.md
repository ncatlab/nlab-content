
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[geometric morphism]] $f : E \to F$ between [[topos]]es is a [[functor]] of the underlying categories that is consistent with the interpretation of $E$ and $F$ as generalized [[topological space]]s. 

If $F = Set = Sh(*)$ is the terminal [[sheaf topos]], then $E \to Set$ is essential if $E$ is a **[[locally connected topos]]**. In general, $f$ being essential is a necessary (but not sufficient) condition to ensure that $f$ behaves like a map of topological spaces whose [[fiber]]s are locally connected: that it is a [[locally connected geometric morphism]].


## Definition


+-- {: .num_defn}
###### Definition

Given a [[geometric morphism]] $(f^* \dashv f_*) : E \to F$, it is an **essential geometric morphism** if the [[inverse image]] functor $f^*$ has not only the [[right adjoint]] $f_*$, but also a [[left adjoint]] $f_!$:

$$
  (f_! \dashv f^* \dashv f_*) 
  \;\;\; : \;\;\;
  E
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^*}{\longleftarrow}}{\underset{f_*}{\longrightarrow}}}
  F
  \,.
$$

=--

A [[point of a topos]] $x : Set \to E$ which is given by an essential geometric morphism is called an **essential point** of $E$. 


+-- {: .num_remark}
###### Remark


There are various further conditions that can be imposed on a geometric morphism:

* If $f_!$ can be made into an $E$-[[indexed functor]] and $f^*$ satisfies some extra conditions, the geometric morphism $f$ is a [[locally connected geometric morphism]] (see there for details).

* If $f_!$ preserves finite [[products]] then $f$ is called **connected surjective**.

* If in addition to the above $f$ is a [[local geometric morphism]] in that there is a further functor $f^! : F \to E$ which is  [[right adjoint]] $(f_* \dashv f^!)$ and [[full and faithful functor|full and faithful]] then the geometric morphism $f$ is called **[[cohesive topos|cohesive]]**.

=--

+-- {: .num_remark}
###### Remark


Since for a [[Grothendieck topos]] $E$ the [[inverse image]] $x^*$ of an essential point is of the form $Hom_E(P,-)$ where $P\ncong\emptyset$ is [[projective object|projective]] and [[connected]], objects satisfying these three conditions are sometimes called _essential objects_ (cf. [Johnstone 1977, p.255](#JTT77)).

=--

## Properties 
 {#Properties}

### A criterion for Grothendieck toposes

The inverse image $f^\ast$ of an essential geometric morphism preserves small limits since it is a right adjoint. Hence, this provides a minimal requirement to satisfy for a general geometric morphism $f^\ast\dashv f_\ast$ in order to qualify for being essential. In case, the toposes involved are [[Grothendieck toposes]] this condition is not only necessary but sufficient.

+-- {: .num_prop}
###### Proposition
Let $f^\ast\dashv f_\ast:\mathcal{E}\to\mathcal{F}$ a geometric morphism between Grothendieck toposes. Then $f$ is essential iff $f^\ast$ preserves small limits iff $f^\ast$ preserves small products.
=--

+-- {: .proof}
###### Proof
Grothendieck toposes are [[locally presentable category|locally presentable]] and $f^\ast$ has rank i.e. it preserves $\alpha$-filtered colimits for some [[regular cardinal]] $\alpha$ since it is a left adjoint. But by ([[Handbook of Categorical Algebra|Borceux vol. 2]]  Thm.5.5.7, p.275) a functor between two locally presentable categories has a left adjoint precisely if it has rank and preserves small limits.

Since limits can be constructed from products and equalizers and $f^\ast$ preserves the latter, it preserves small limits precisely when it preserves small products.
=--

### Relation to morphisms of (co)sites
 {#RelationToSiteMorphisms}


For $C$ and $D$ [[small categories]] write $[C,Set]$ and $[D,Set]$ for the corresponding [[copresheaf]] [[presheaf topos|toposes]]. (If we think of the [[opposite categories]] $C^{op}$ and $D^{op}$ as [[sites]] equipped with the trivial [[coverage]], then these are the corresponding [[sheaf toposes]].)

+-- {: .num_prop}
###### Proposition

This construction extends to a [[2-functor]]

$$
  [-,Set] : Cat_{small}^{co} \to Topos_{ess}
$$

from the [[2-category]] [[Cat]]${}_{small}$ with [[2-morphism]]s reversed) to the sub-2-category of [[Topos]] on essential geometric morphisms, where a [[functor]] $f : C \to D$ is sent to the essential geometric morphism

$$
  (f_! \dashv f^* \dashv f_*) : 
  [C,Set]
    \stackrel{\overset{f_! := Lan_f}{\to}}{\stackrel{\overset{f^* := (-) \circ f}{\leftarrow}}{\underset{f_* := Ran_f}{\to}}}
  [D,Set]
  \,,
$$

where $Lan_f$ and $Ran_f$ denote the left and right [[Kan extension]] along $f$, respectively.

=--

+-- {: .num_prop}
###### Proposition

This 2-functor is a [[full and faithful 2-functor]] when restricted to [[Cauchy complete categories]]:

$$
  [-, Set] : Cat^co_{CauchyComp} \hookrightarrow Topos_{ess}
  \,.
$$

For all small categories $C,D$ we have an [[equivalence of categories]]

$$
  Func(\overline{C},\overline{D})^{op}
  \simeq
  Topos_{ess}([C,Set], [D,Set])
$$

between the [[opposite category]] of the [[functor category]] between the [[Cauchy completion]]s of $C$ and $D$ and the the category of essential geometric morphisms between the copresheaf toposes and [[geometric transformation]]s between them.

=--

In particular, since every [[poset]] -- when regarded as a [[category]] -- is Cauchy complete, we have

+-- {: .num_cor}
###### Corollary

The [[2-functor]]

$$
  [-,Set] : Poset \to Topos_{ess}
$$

is a [[full and faithful 2-functor]].

=--

+-- {: .num_remark}
###### Remark

Sometimes it is useful to decompose this statement as follows.

There is a functor 

$$
  Alex : Poset \to Locale
$$

which assigns to each [[poset]] a [[locale]] called its [[Alexandroff locale]]. By a theorem discussed there, a morphisms of locales $f : X \to Y$ is in the image of this functor precisely if its inverse image morphism $f^* Op(Y) \to Op(X)$ of [[frame]]s has a [[left adjoint]] in the [[2-category]] [[Locale]]. 

Moreover, for any poset $P$ the [[sheaf topos]] over $Alex P$ is naturally equivalent to $[P,Set]$

$$
  [-,Set] \simeq Sh \circ Alex
  \,.
$$

With this, the fact that $[-,Set] : Poset \to Topos$ hits precisely the essential geometric morphisms follows with the basic fact about [[localic reflection]], which says that $Sh : Locale \to Topos$ is a [[full and faithful 2-functor]].

=--


### Some morphism calculus



+-- {: .num_prop}
###### Proposition

Let $f : E \to F$ be an essential geometric morphism.

For every $\phi : X \to f^* f_* A$ in $E$ the diagram

$$
  \array{
    X &\stackrel{\phi}{\to}& f^* f_* A
    \\
    \downarrow && \downarrow
    \\
    f^* f_! X &\stackrel{}{\to}& A
  }
$$

commutes, where the vertical morphisms are unit and counit, respectively, and where the bottom horizontal morphism is the [[adjunct]] of $\phi$ under the composite adjunction $(f^* f_! \dashv f^* f_*)$.

=--

+-- {: .proof}
###### Proof

The morphism $\phi : X \to f^* f_* A$ is the component of a [[natural transformation]]

$$
  \array{
    *&&\overset{X}{\to}&& E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow 
    \\
    E &\underset{f_*}{\to}&F
  }
  \,.
$$

The composite $X \stackrel{\phi}{\to}  f^* f_* A \to A$ is the component of this composed with the counit $f^* f_* \Rightarrow Id$.

We may insert the 2-identity given by the zig-zag law

$$
  \cdots \;\;\; = \;\;\;
  \array{
    *&&\overset{X}{\to}&& E && = && E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow &\Downarrow& \searrow^{f_!} 
    &\Downarrow& \nearrow_{\mathrlap{f^*}}
    \\
    E &\underset{f_*}{\to}&F &&=&& F   
  }
  \,.
$$

Composing this with the counit $f^* f_* \Rightarrow Id$ produces the transformation whose component is manifestly the morphism $X \to f^* f_! X \to A$.

=--


## Examples

### Logical functors and etale geometric morphisms

A [[logical functor]] $E\to F$ with a [[left adjoint]] has automatically also a [[right adjoint]] whence is the [[inverse image]] part of an essential geometric morphism $F\to E$.

A particularly important instance of this situation is the following:

For any morphism $f\colon A\to B$ in a topos $E$, the induced geometric morphism $f\colon E/A \to E/B$ of [[overcategory]] [[topos]]es is essential. Here, the logical functor is given by the pullback functor $f^*:E/B\to E/A$ of course.

In the special case $B = *$ the [[terminal object]], the essential geometric morphism

$$
  \pi : E/A \to E
$$

is also called an [[etale geometric morphism]].

Conversely, (almost) any essential geometric morphism $\pi$ whose [[inverse image]] $\pi^*$ is a [[logical functor]] has the form of an [[etale geometric morphism]]:

+-- {: .num_prop}
###### Proposition

If the [[left adjoint]] $\pi_!$ of a logical functor $\pi^*:E\to F$ furthermore preserves equalizers, then the corresponding essential geometric morphism is up to equivalence an [[etale geometric morphism]] $\pi : F\simeq E/A \to E$ for an object $A$ in $E$ that is determined up to isomorphism. 

=--

For a proof see e.g. Johnstone [(1977, p.37)](#JTT77).

### Locally connected toposes

A [[locally connected topos]] $E$ is one where the [[global section]] [[geometric morphism]] $\Gamma : E \to Set$ is essential. 

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{\Pi_0}{\longrightarrow}}{\stackrel{\overset{LConst}{\longleftarrow}}{\underset{\Gamma}{\longrightarrow}}}
  Set
  \,.
$$

In this case, the functor $\Gamma_! = \Pi_0 : E \to Set$ sends each object to its set of connected components.  More on this situation is at [[homotopy groups in an (∞,1)-topos]].  

Note, though that if $p\colon E\to S$ is an arbitrary geometric morphism through which we regard $E$ as an $S$-topos, i.e. a topos "in the world of $S$," the condition for $E$ to be locally connected as an $S$-topos is not just that $p$ is essential, but that the left adjoint $p_!$ can be made into an $S$-[[indexed functor]] (which is automatically true for $p^*$ and $p_*$).  This is automatically the case for $Set$-toposes (at least, when our [[foundation]] is [[material set theory]]---and if our foundation is [[structural set theory]], then our large categories and functors all need to be assumed to be $Set$-indexed anyway). For more see [[locally connected geometric morphism]].

### Tiny objects

The [[tiny object]]s of a [[presheaf topos]] $[C,Set]$ are precisely the essential points $Set \to [C,Set]$. See [[tiny object]] for details.



## Related concepts

* [[essential subtopos]] / [[level of a topos]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]


## References

Like many other things, it all started as an exercise in

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (expos&#233; IV, ex.7.6, pp.414-417)

Speaking of exercises, consider the results of [[Jan Erik Roos|Roos]] on essential points reported in exercise 7.3 of

* {#JTT77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014, pp.254f)

The case of sheaves valued in [[FinSet]] is considered in

* J. Haigh, _Essential geometric morphisms between toposes of finite sets_ , Math. Proc. Phil. Soc. **87** (1980) pp.21-24.

The standard reference for _essential localizations_ [^further], aka [[level of a topos|levels]], is

* {#KL89}[[G. M. Kelly]], [[F. W. Lawvere]], _On the Complete Lattice of Essential Localizations_ , Bull. Soc. Math. de Belgique **XLI** (1989) 289-319 &lbrack;[[Kelly-Lawvere_EssentialLocalizations.pdf:file]]&rbrack;

[^further]: See at [[Aufhebung]] for further references on essential localizations.

For more on this see also

* {#Lima15} [[Guilherme Frederico Lima]], _From Essential Inclusions to Local Geometric Morphisms_, talk at [Topos &#224; l'IHES](https://indico.math.cnrs.fr/event/747/), November 2015, Paris ([video](https://www.youtube.com/watch?v=YsoGN91Rh_s))

The definition of essential geometric morphisms appears before Lemma A.4.1.5 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_ , Oxford UP 2002.

Connected surjective and local geometric morphisms are discussed in 

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_ , Proceedings London Mathematical Society **58** (1989), pp.281-305.

Further refinements are in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))


[[!redirects essential geometric morphisms]]