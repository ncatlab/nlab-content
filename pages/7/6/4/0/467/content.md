#Idea#

If regarded from the right perspective, [[sheaf|sheaves]], [[stack|stacks]], [[infinity-stack|infinity-stacks]] on a given site $S$ with their [[descent and codescent|descent conditions]] are nothing but a way of talking about the [[infinity-category]] of [[infinity-category|infinity-categories]] modeled on $S$, in  the sense of [[space and quantity]]: the $\infty$-category of $\infty$-category-valued [[presheaf|presheaves]]/[[sheaf|sheaves]] on $S$.

In particular, the all-important [[descent and codescent|descent condition]] is from this perspective nothing but the condition that the [[Yoneda lemma]] extends to respect higher categorical [[equivalence|equivalences]]: 

for $X \in S$ a representable $\infty$-category valued presheaf, $Y \stackrel{\simeq}{\to} X$ a weakly equivalent replacement of $X$, descent says that the usual statement of the [[Yoneda lemma]] for an $\infty$-category valued presheaf $\mathbf{A}$ -- that $[X,\mathbf{A}] \simeq \mathbf{A}(X)$ -- extends along the weak equivalence to yield also $\cdots \simeq [Y,\mathbf{A}]$.

The $\infty$-category valued presheaves satisfying this condition represent the objects in the proper $\infty$-category of $\infty$-category valued presheaves, which is usefully conceived as a suitable [[enriched homotopy theory|enriched homotopy category]]: these are the _$\infty$-stacks._

Switching back perspective from presheaves to spaces, and reading the Yoneda lemma as the consistency condition on this interpretation (as indicated at [[Yoneda lemma]]), this  says that $\infty$-stacks on a site $S$ are nothing but $\infty$-categories consistently modeled on $S$. For instance a 0-stack=[[sheaf]] modeled on $S = $[[Diff]] may be a [[generalized smooth space]], while a 1-stack=[[stack]] modeled on [[Diff]] may be a [[differentiable stack]] representing a [[Lie groupoid|smooth groupoid]].

***

###Discussion

_A previous version of the above paragraphs led to the following objection:_

+--{.query}

_[[Mike Shulman|Mike]]_: I object to those claims.  For one thing, I think you should make clear at the outset that descent conditions only arise when you consider not ordinary $\infty$-categories, but what are essentially sheaves/stacks of $\infty$-categories over some site.  I don't think choosing to call such stacks "$\infty$-categories for which the notion of space is modeled on the objects of some locally small category" justifies saying that descent is just a way of talking about morphisms between $\infty$-categories.  If nothing else, it's confusing to someone who doesn't realize that by "$\infty$-category" you mean what many people would call an "$\infty$-stack."  But it also puts the emphasis in the wrong place, since there is no problem talking about morphisms between $\infty$-categories that are not stacks without descent; descent only arises when we pass to stacks.

Likewise, while certainly the Yoneda lemma for $\infty$-stacks depends on descent, but since there is a perfectly good $\infty$-Yoneda lemma, for $\infty$-categories that are not stacks which has nothing to do with descent, I think it is only confusing and not helpful to try to draw a connection between descent and the Yoneda lemma.  Really the (basically tautological) connection is between descent and stacks, since the Yoneda lemma can exist without either.

_[[Urs Schreiber|Urs]]_: I agree, I didn't phrase that well. I still think it is important for a good general understanding to emphasize that the descent condition is just the extension of the Yoneda statement along weak equivalences, though. The above is my attempt to keep that point while taking into account your sensible objections. Let me know if this is better now.

=--

***

Instead of committing the following discussion to a fixed model for [[infinity-category|infinity-categories]] or [[omega-category|omega-categories]] I describe the situation in a setup which aims to come close to making the minimum number of necessary assumptions on the ambient context. After discussing the general idea I give concrete examples in concrete realizations of $\infty$-categorical contexts.


#Setup in enriched homotopy theory#

In the context of [[enriched homotopy theory]] we assume that our model for [[infinity-category|infinity-categories]] can be thought of as 

1. [[space and quantity|generalized spaces modeled on]] the objects in a  [[locally small]] [[category]], and

2.  such that there is a good notion of [[homotopy]] between maps into these spaces;


By the yoga of [[space and quantity]] the first point means that our infinity-categories are [[presheaf|presheaves]] on a [[locally small]] category $S$. By the yoga of [[enriched homotopy theory]] the second point means that these presheaves take values in a [[closed monoidal homotopical category]].

So let

* $S$ be a [[site]];

* $V$ be a [[closed monoidal homotopical category]];

* $C := Sh(S,V)$ be the category of $V$-valued [[sheaf|sheaves]] on $S$ such that it becomes a $V$-[[enriched homotopical category]] with weak equivalences the _stalkwise_ weak equivalences of $V$.

+--{.query}

_Mike_: What is the meaning of "stalkwise" for an arbitrary site?  The only notion of "stalk" I can think of for sheaves on an arbitrary site is a preimage under some geometric morphism ("point") $Set = Sh(1) \to Sh(S)$ (or maybe some enriched version thereof).  But there are very nontrivial sites $S$ such that $Sh(S)$ has no points, so this doesn't work in full generality.

[[Urs Schreiber|Urs]]: Right, this is a point I was glossing over. I am thinking that we shouldn't actually be talking about stalks here but

1. assume that our site is such that infinite unions of covers are still covers;

2. define a _local weak equivalence_ (or a _local fibration_) of sheaves $f : \mathbf{A} \to \mathbf{B}$ to be one such that for all objects $U \in S$ in the site there is a cover $Y$ such that $\mathbf{A}(Y) \to \mathbf{B}(Y)$ is a weak eqivalence (or a fibration) in $V$.

=--

The $V$-[[enriched homotopical category]] $C$ is our generic model for an $\infty$-category of [[infinity-category|infinity-categories]].

## Examples ##

* Let $S = pt$ be the terminal category so that $C = V$ and take $V$ to be any of the examples listed at [[monoidal model category]], such as [[Cat]], [[strict 2-category|2Cat]], probably [[strict omega-category|omegaCat]] (but here the [[pushout-product axiom]] still needs to be checked), or [[simplicial set|SimpSet]]. Even though for such simple $S$ there is no nontrivial "topology" in the game, the notion of $\infty$-stack resulting from this setup is still interesting: it encodes for instance [[nonabelian cohomology]] of finite (really: discrete) groups, $\infty$-groups, $\infty$-[[groupoids]].

* Let $S =$ [[Top]] with its standard [[Grothendieck topology]] and let $V = $ [[simplicial set|SimpSet]]. Then I think that the $Ho_V$-enriched category $Ho_C$ is the $SimpSet$-eriched homotopy category of simplicial presheaves  that is discussed in [ToenSNAC]() and [ToenHDS](). As described in [ToenHDS](), one can think of this $C$ as modelling the collection of [[(infinity,1)-category|(infinity,1)-categories]].

* Let $S = $ [[Diff]] and with its standard [[Grothendieck topology]] and $V = $ [[strict omega-category|omegaCat]]. The $C$ is the model for smooth $\infty$-categories used in [[schreiber:Differential Nonabelian Cohomology]].

* Restrict $V$ either from [[simplicial set]]s to [[Kan complex]]es or from [[strict omega-category|strict omega-categories]] to [[omega-groupoid]]s hence equivalently to [[crossed complex]]es and then further to complexes of abelian groups to make contact, below, with ordinary notions of sheaf cohomology. 

#The enriched homotopy category#

The $Ho_V$-[[enriched category]] $Ho_C$ is now our model for the $\infty$-category if $\infty$-categories. The claim is:

* $\infty$-stacks on $S$ are nothing but the morphisms in $Ho_C$;

* the [[descent and codescent|descent condition]] condition on these morphisms in just the $\infty$-version of the [[Yoneda lemma]] which says that for $X \in S \subset C$ a space and $Y \in C$ a [[cover]] $Y \stackrel{\simeq}{\to} X$ in $C$ the ordinary [[Yoneda lemma]] which says that 
$$
  Ho_C(X,\mathbf{A}) \simeq \mathbf{A}(X)
$$ 
extends to a statement which respects the weak equivalence $Y \stackrel{\simeq}{\to} X$ in that also 
$$\mathbf{A}(X) \stackrel{\simeq}{\to} Desc(Y,\mathbf{A}) := Ho_C(Y,\mathbf{A})$$

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

* for $S = pt$, $V = $ [[crossed complex|CrossedComplexes]]: this is the context of results about cohomology in [[Nonabelian algebraic topology]];

* for $S = $ [[Top]] and $V = $ [[simplicial set|SimpSet]] this are pretty much the statements in [ToenHDS](http://arxiv.org/abs/math.AG/0604504):

  * $C$ is the category of simplicial sheaves (middle of p. 11);

  * the right derived $(V =SimpSet)$-eriched Hom is denoted there $Map(F,G) := R Hom(F,G)$ (for instance middle of p. 14)

  * sheaf cohomology is reproduced as indicated, for instance p. 7 of [ToenSNAC].

...

# References #

* **ToenSNAC** -- B. To&#235;n, [[ToenStacksNAC.pdf:file]]

* **ToenHDS** -- B. To&#235;n, _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504))

