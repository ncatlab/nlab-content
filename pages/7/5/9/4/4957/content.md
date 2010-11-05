

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

## Definition

A **local geometric morphism** $f : E \to S$ between [[topos]]es $E,S$ is 

*  a [[geometric morphism]]

   $$
    (f^* \dashv f_*) \colon E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  S
   $$

*  such that a further [[right adjoint]] $f^! : S \to E$ exists 

   $$
    (f^* \dashv f_* \dashv f^!) : 
    E
    \stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
   $$

*  and such that one, hence all, of the following equivalent conditions hold:

   1. The right adjoint $f^!$ is an $S$-[[indexed functor]].
   1. $f$ is [[connected geometric morphism|connected]], i.e. $f^*$ is [[full and faithful functor|fully faithful]].
   1. The right adjoint $f^!$ is fully faithful.
   1. The right adjoint $f^!$ is [[cartesian closed functor|cartesian closed]].

When we regard $E$ as a topos over $S$, so that $f$ is regarded as its [[global section]] geometric morphism in the category of toposes over $S$, then we say that $E$ is a **local $S$-topos**.  In this case we may label the functors involved as

$$
  (Disc \dashv \Gamma \dashv Codisc) : 
    E
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    S
$$

to indicate that if we think of $\Gamma$ as sending a [[space]] to its underlying $S$-object of points by forgetting [[cohesive topos|cohesion]], then $Disc$ creates the [[discrete space]] and $Codisc$ the [[codiscrete space]] on an object in $S$.

This is especially common when $S=$ [[Set]], in which case the final condition is automatic since all functors are $Set$-indexed.


## Properties

### Concrete sheaves

Every local topos $\Gamma : E \to S$ comes with a notion of [[concrete sheaves]], a [[reflective subcategory]] $Conc_\Gamma(E) \hookrightarrow E$ which factors the topos inclusion of $S$:

$$
  S 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(E) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  E
$$

and is a [[quasitopos]]. See [[concrete sheaf]] for details.

## Examples

### Easy examples

* If $X$ is a [[topological space]], or more generally a [[locale]], then $Sh(X)$ is local (over Set) iff $X$ has a [[focal point]], i.e. a point whose only [[neighborhood]] is the whole space.

* If $C$ is a small category with a [[terminal object]], then the [[presheaf topos]] $[C^{op},Set]$ is local.  The converse is true if $C$ is [[Cauchy complete category|Cauchy complete]].

### Sheaves on $CartSp$

Let $E = Sh(CartSp)$ be the [[gros topos]] of [[sheaves]] on the [[site]] [[CartSp]] of [[Cartesian space]]s with the [[good open cover]] [[coverage]]. This is a local topos.

The further right adjoint
is 

$$
  Codisc : Set \to Sh(CartSp)
$$

the functor that sends a set to the [[diffeological space]] on that set with _codiscrete_ smooth structure (every map of sets is smooth). 

(Thanks to [[David Carchedi]].)

### Localization

Let $LocTopos$ denote the 2-category of local [[Grothendieck toposes]] (over Set) with all geometric morphisms between them.  Let $PTopos$ denote the 2-category whose objects are [[pointed topos|pointed toposes]] (i.e. (Grothendieck) toposes $E$ equipped with a geometric morphism $s\colon Set\to E$), and whose morphisms are pairs $(f,\alpha)$ such that $f\colon E\to E'$ is a geometric morphism and $\alpha\colon s'\to f s$ is a (not necessarily invertible) geometric transformation.

Note that if $E$ is a local topos with global sections geometric morphism $e^*\dashv e_*$, then the adjunction $e_*\dashv e^!$ is also a geometric morphism $Set\to E$.  In this way we have a functor $LocTopos \to PTopos$, which is a full embedding, and turns out to have a [[right adjoint]]: this right adjoint is called the **localization** of a pointed topos at its specified point.  For example:

* If $C$ is a small category and $U$ is an object of $C$, then the localization of $[C^{op},Set]$ at the point induced by $U\colon 1\to C$ can be identified with $[(C/U)^{op},Set]$.

* If $X=Spec(A)$ is the [[Zariski spectrum]] of a [[commutative ring]] $A$, and $P\subset A$ is a prime ideal of $A$ (i.e. a point of $X$), then the localization of $Sh(X)$ at $P\colon 1\to X$ can be identified with $Sh(Spec(A_P))$, where $A_P$ denotes the [[localization]] of $A$ at $P$.  Of course, this is the origin of the terminology.

A similar construction is possible for [[bounded geometric morphism|bounded]] toposes over any base (not just Set).


## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* **local topos** / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]


## References

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_  Proc. London Math. Soc.  (1989)   s3-58  (2):  281-305.  ([pdf](http://plms.oxfordjournals.org/content/s3-58/2/281.full.pdf+html))


* [[Peter Johnstone]], _[[Elephant]]_ Chapter C3.6

* [[Steven Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_ Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz))

This is based on part 2 of

* [[Lars Birkedal]], _Developing Theories of Types and
Computability via Realizability_ PhD Thesis ([pdf](http://itu.dk/people/birkedal/papers/devttc.pdf))

[[!redirects local geometric morphisms]]
[[!redirects local topos]]
[[!redirects local topoi]]
[[!redirects local toposes]]
