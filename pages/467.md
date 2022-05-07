[[!redirects ∞-stack homotopically]]

This entry is about models/presentations for an [[(infinity,1)-category of (infinity,1)-sheaves]] in terms of [[model category|model categories]] of $\infty$-presheaves, in particular in terms of the Brown-Joyal-Jardine [[model structure on simplicial presheaves]]. 

For other notions see [[infinity-stack]] and in general see [[Higher Topos Theory]].

#Idea#

From one perspective, [[sheaf|sheaves]], [[stack|stacks]], [[infinity-stack|infinity-stacks]] on a given site $S$ with their [[descent]] conditions are nothing but a way of talking about the [[infinity-category]] of [[infinity-category|infinity-categories]] modeled on $S$, in  the sense of [[space and quantity]]: the $\infty$-category of $\infty$-category-valued [[presheaf|presheaves]]/[[sheaf|sheaves]] on $S$.

In particular, the all-important [[descent]] condition is from this perspective nothing but the condition that the [[Yoneda lemma]] extends to respect higher categorical [[equivalence|equivalences]]: 

for $X \in S$ a representable $\infty$-category valued presheaf, $Y \stackrel{\simeq}{\to} X$ a weakly equivalent replacement of $X$, descent says that the usual statement of the [[Yoneda lemma]] for an $\infty$-category valued presheaf $\mathbf{A}$ -- that $[X,\mathbf{A}] \simeq \mathbf{A}(X)$ -- extends along the weak equivalence to yield also $\cdots \simeq [Y,\mathbf{A}]$.

The $\infty$-category valued presheaves satisfying this condition represent the objects in the proper $\infty$-category of $\infty$-category valued presheaves/sheaves, which is usefully conceived as a suitable [[enriched homotopy theory|enriched homotopy category]]: these are the _$\infty$-stacks._

Switching back perspective from presheaves to spaces, and reading the Yoneda lemma as the consistency condition on this interpretation (as indicated at [[Yoneda lemma]]), this  says that $\infty$-stacks on a site $S$ are nothing but $\infty$-categories consistently modeled on $S$. For instance a 0-stack=[[sheaf]] modeled on $S = $[[Diff]] may be a [[generalized smooth space]], while a 1-stack=[[stack]] modeled on [[Diff]] may be a [[differentiable stack]] representing a [[Lie groupoid|smooth groupoid]].

Instead of committing the following discussion to a fixed model for [[infinity-category|infinity-categories]] or [[omega-category|omega-categories]] I describe the situation in a setup which aims to come close to making the minimum number of necessary assumptions on the ambient context. After discussing the general idea I give concrete examples in concrete realizations of $\infty$-categorical contexts.


#Setup in enriched homotopy theory#

In the context of [[enriched homotopy theory]] we assume that our model for [[infinity-category|infinity-categories]] can be thought of as 

1. [[space and quantity|generalized spaces modeled on]] the objects in a  [[locally small category]], and

2.  such that there is a good notion of [[homotopy]] between maps into these spaces;


By the yoga of [[space and quantity]] the first point means that our infinity-categories are [[presheaf|presheaves]] on a [[locally small category]] $S$. By the yoga of [[enriched homotopy theory]] the second point means that these presheaves take values in a [[closed monoidal homotopical category]].

So let

* $S$ be a [[site]];

* $V$ be a [[closed monoidal homotopical category]];

* $C := Sh(S,V)$ be the category of $V$-valued [[sheaf|sheaves]] on $S$ such that it becomes a $V$-[[enriched homotopical category]] with some induced (usually local) notion of weak equivalences.


##Remark##

From this $V$-enriched perspective it is natural to generalize to the case where the site $S$ is not just locally small, i.e. enriched over $Sets$, but is enriched over $V$ itself. If one does this one speaks of [[derived stack|derived]] $\infty$-stacks.

***

The $V$-[[enriched homotopical category]] $C$ is our generic model for an $\infty$-category of [[infinity-category|infinity-categories]] modeled on $S$.

## Examples ##


* Let $S = pt$ be the terminal category so that $C = V$ and take $V$ to be any of the examples listed at [[monoidal model category]], such as [[Cat]], [[strict 2-category|2Cat]], probably [[strict omega-category|omegaCat]] (but here the [[pushout-product axiom]] still needs to be checked), or [[simplicial set|SimpSet]]. Even though for such simple $S$ there is no nontrivial "topology" in the game, the notion of descent resulting from this setup is still interesting: it encodes for instance [[nonabelian cohomology]] of finite (really: discrete) groups, $\infty$-groups, $\infty$-[[infinity-groupoid|groupoids]].

In all of the following examples notice that if one wants to take the site $S$ to be something like [[Top]] or [[Diff]], as one often does, then one needs to beware of the size issues of sheaves on [[large site|large sites]].



* [[simplicial presheaf|Simplicial presheaves]], using the [[model structure on simplicial presheaves]] or the [[model structure on simplicial sheaves]]:  If $S$ is any site and $V = $ [[simplicial set|SimpSet]], then the natural notion of local weak equivalences in $Sh(S,V)$ are those morphisms $f : \mathbf{A} \to \mathbf{B}$ which induce isomorphisms of sheaves of simplicial homotopy groups under all functors $\pi_n : SimpSet \to Groups$.  If $S$ has enough points (such as the site of open sets of a topological space), then this is equivalent to $f$ being a stalkwise weak equivalence of simplicial sets, using the [[model structure on simplicial sets]] (see for instance section 1 of [JardStackSSh](http://intlpress.com/HHA/v3/n2/a5/v3n2a5.pdf)).  Then I think that the $Ho_V$-enriched category $Ho_C$ is the $SimpSet$-enriched homotopy category of simplicial presheaves that is discussed in [ToenSNAC](#ToenSNAC) and [ToenHDS](#ToenHDS).

* Let $S = $ [[Diff]] and with its standard [[Grothendieck topology]] and $V = $ [[strict omega-category|omegaCat]]. The $C$ is the model for smooth $\infty$-categories used in [[schreiber:Differential Nonabelian Cohomology]].

* Restrict $V$ either from [[simplicial set]]s to [[Kan complex]]es or from [[strict omega-category|strict omega-categories]] to [[omega-groupoid]]s hence equivalently to [[crossed complex]]es and then further to complexes of abelian groups to make contact, below, with ordinary notions of sheaf cohomology. 

#The enriched homotopy category#

The $Ho_V$-[[enriched category]] $Ho_C$ is now our model for the $\infty$-category if $\infty$-categories modeled on $S$. The claim is:

* $\infty$-stacks on $S$ are nothing but the objects in $Ho_C$;

* the [[descent]] condition on these morphisms is an extension of the statement of the [[Yoneda lemma]] -- which says that for $X \in S \subset C$ a space and $Y \in C$ a [[cover]] $Y \stackrel{\simeq}{\to} X$ we have
$
  [X,\mathbf{A}] \simeq \mathbf{A}(X)
$ -- 
extends to a statement which respects the weak equivalence $Y \stackrel{\simeq}{\to} X$ in that also 
$$\mathbf{A}(X) \stackrel{\simeq}{\to} Desc(Y,\mathbf{A}) := [Y,\mathbf{A}]$$;

* the morphisms of $Ho_C$ are (of course) computed by the [[derived functor|right-derived Hom-functor]] in $C$
$$
  R Hom : C^op \times C \to V
$$
and

  * for fixed $X \in S$ the functor 
    $$
      R Hom(X, -) : Sh(S,V) \to V
    $$
    is the functor which computes sheaf cohomology in the form of being the right-derived functor of the global section functor;

  * for fixed $\mathbf{A} \in Sh(S,V)$ the functor
    $$
      R Hom(-, \mathbf{A})
    $$
    is the functor which computes sheaf cohomology of the sheaf $\mathbf{A}$ in the form of &#268;ech cohomology (by mapping out of $\infty$-categorical resolutions aka _hypercovers_ of a space $X$).


## Examples ##

* for $S = pt$, $V = $ [[crossed complex|CrossedComplexes]]: this is the context of results about cohomology in [[nonabelian algebraic topology]];

* for $V = $ [[simplicial set|SimpSet]] these are pretty much the statements in [ToenHDS](#ToenHDS):

  * $C$ is the category of simplicial sheaves on $S$ (middle of p. 11);

  * the right derived $(V =SimpSet)$-enriched Hom is denoted there $Map(F,G) := R Hom(F,G)$ (for instance middle of p. 14)

  * sheaf cohomology is reproduced as indicated, for instance p. 7 of [ToenSNAC](#ToenSNAC).

...

# References #

* **JardStackSSh** -- J. Jardine, _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3(2), 2001 p. 361-284 ([pdf](http://intlpress.com/HHA/v3/n2/a5/v3n2a5.pdf))

* **JardSimpSh** -- J. Jardine, _Fields Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

{: #ToenSNAC}
* **ToenSNAC** -- [[Bertrand Toën]], [[ToenStacksNAC.pdf:file]]

{: #ToenHDS}
* **ToenHDS** -- [[Bertrand Toën]], _Higher and derived stacks: a global overview_ ([arXiv:math/0604504](https://arxiv.org/abs/math/0604504))