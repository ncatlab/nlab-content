
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A crucial ingredient in a [[topos]] is a [[subobject classifier]]. That this has to do with [[subobjects]] turns out to the a coincidence of low dimensions. As discussed at [[stuff, structure, property]], the classifying objects in [[higher topos theory]] classify more general morphisms.

When one passes all the way to $\infty$-toposes, there should be objects that classify _all_ morphisms. This is made precise in the context of [[(∞,1)-topos]] [[higher topos theory|theory]].

One way to characterize an [[(∞,1)-topos]] is as 

* a [[presentable (∞,1)-category]]

* with [[universal colimits]]

* such that for all sufficiently large [[regular cardinal]]s $\kappa$ there is a **classifying object** for the class of all $\kappa$-compact morphisms in $X$.

This statement is originally due to [[Charles Rezk]]. It is reproduced as theorem 6.1.6.8 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

## Details

### Subobject classifier {#DetailsSubObjClassf}

+-- {: .un_defn}
###### Definition

Let $C$ be an [[(∞,1)-category]] and $S \in C_1$ a class of [[morphism]]s that is stable under [[pullback]] in $C$.

Let $Cod_C$ be the [[codomain fibration]] of $X$, i.e. the [[(∞,1)-category of (∞,1)-functors]]

$$
  Cod_C := Func(\Delta[1], C)
$$

equipped with the [[Cartesian fibration]] $Cod_C \to C$ induced from the endpoint inclusion $Delta[0] \to \Delta[1]$.

Write

* $Cod_C^S$ for the full [[subcategory]] of $Cod_C$ on the object in $S$;

* $Cod_C^{(S)}$ the non-full subcategory whose objects are the elements of $S$, and whose morphisms are squares that are pullback diagrams.

Then evaluation at $\Delta[0] \to \Delta[1]$ yields

* a [[Cartesian fibration]] $Cod_C^S \to C$;

* a [[right fibration]] $Cod_C^{(S)} \to C$.

We say a morphism $f :x \to y$ in $C$ _classifies_ $S$ -- or simply that $y$ classifies $S$ -- if it is the [[terminal object]] in $Cod_C^{(S)}$.

=--

This is [[Higher Topos Theory|HTT, notation 6.1.3.4]] and [[Higher Topos Theory|HTT, def. 6.1.6.1 ]].

+-- {: .un_defn}
###### Definition

A **subobject classifier** for $C$ is an object that classifies the class $S$ of [[monomorphism in an (∞,1)-category|monomorphisms in the (∞,1)-category]] $C$.

=--

[[Higher Topos Theory|HTT, def. 6.1.6.1 ]]


**Example** The $(\infty,1)$-category [[∞Grpd]] has a a subobject classifier: the set $\{0,1\}$ with two elements, regarded as a [[discrete groupoid]].


+-- {: .un_prop}
###### Proposition

Every [[(∞,1)-topos]] has a subobject classifier.

=--


+-- {: .proof}
###### Proof

[[Higher Topos Theory|HTT, prop. 6.1.6.3]] and the remark below that

=--

### Object classifier {#DetailsObjClassf}


**Remark/Warning.** However, the point of having [[subobject]]s and hence [[monomorphism]]s classified by an object in an ordinary [[topos]] may be thought of as being solely due to the fact that in a 1-[[topos]], any object necessarily classifies a _set_  (or rather a [[poset]] i.e. a [[0-category]] or rather a [[(0,1)-category]]) of morphisms, and the point of subobjects/monomorphisms of a given object is that they don't have [[automorphism]]s and hence indeed form a set (or rather: [[poset]]).

In an $(\infty,1)$-topos we might thus expect an object that classifies _all_ morphisms, in that the assignment

$$
  c \mapsto Core(C_{/c})
$$

of an object $c\in C$ to the [[core]] of its [[over quasi-category|over (∞,1)-category]] yields a [[(∞,1)-functor]] $C^{op} \to \infty Grpd$ that is [[representable functor|representable]].

Indeed, this is _essentially_ the case -- up to size issues, that the following definitions take care of.

+-- {: .un_defn}
###### Definition

For $\kappa$ some [[cardinal]], say a morphism $f : x \to y$ in $C$ is **relatively $\kappa$-compact** if for all [[pullback]]s along $h : y' \to y$ to $\kappa$-[[compact object]]s, $y'$, the pulled back object $h^* x'$ is itself a $\kappa$-compact object.

=--


+-- {: .un_theorem}
###### Theorem

A [[presentable (∞,1)-category]] $C$  is an [[(∞,1)-topos]] precisely if

1. it has [[universal colimits]];

1. for sufficiently large regular [[cardinal]]s $\kappa$, $C$ has a classifying object for relatively $\kappa$-compact morphisms.

=--

+-- {: .proof}
###### Proof

This is due to [[Charles Rezk]]. The statement appears as [[Higher Topos Theory|HTT, theorem 6.1.6.8]].

=--


## Examples

+-- {: .query}
David Corfield: What are the object classifiers for [[Top]]?

[[Mike Shulman]]: I presume you mean Top as a model for $\infty Gpd$?  I expect that you get them by looking at the $\infty$-groupoid [[core]] of the $(\infty,1)$-category of all $\kappa$-compact $\infty$-groupoids.

[[David Corfield]]: Thanks. Do we have this $\kappa$-compact business explained somewhere? Should I also be thinking about the [[universal fibration of (infinity,1)-categories|universal fibration of (infinity,1)-groupoids]]?

[[Urs Schreiber]]: see [[compact object]]

[[Mike Shulman]]: Yes, and I think the universal fibration is relevant.

[[Urs Schreiber]]: now more details on "relative $\kappa$-compact" morphisms above in the "Details"-section.

[[Urs Schreiber]]: so the [[universal fibration of (infinity,1)-categories|universal fibration of (infinity,1)-groupoids]] $(Z_{grpd_{\leq \kappa}}^op) \to \infty Grpd_{\leq \kappa}$ would seem to classify just [[left fibration]]s over objects, but in fact every $\infty$-functor between $\infty$-groupoids should be a left fibration, up to equivalence:

this follows explicitly from HTT, prop 3.3.1.8, recalled at [[Cartesian fibration]].



=--

[[!redirects object classifier]]
[[!redirects object classifiers]]
[[!redirects (sub)object classifier in an (∞,1)-topos]]
[[!redirects (sub)object classifiers in an (∞,1)-topos]]
[[!redirects (sub)object classifiers in an (infinity,1)-topos]]
