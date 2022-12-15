
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An **absolute colimit** is a [[colimit]] which is [[preserved limit|preserved]] by any [[functor]] whatsoever.  In general this happens because the colimit is a colimit for purely "diagrammatic" reasons.  The notion is most important in [[enriched category theory]].

Of course, there is a dual notion of **absolute limit**, but it is used less frequently.

## Definitions

The term "absolute colimit" is actually used for two closely related, but distinct, notions.

### Particular absolute colimits

+-- {: .num_defn #DefParticular}
###### Definition
A particular [[colimit]] diagram in a particular [[category]] $C$ is an **absolute colimit** if it is [[preserved limit|preserved]] by every [[functor]] with domain $C$.
=--

This definition makes sense also in [[enriched category theory]]: for any $V$, a [[weighted colimit]] in a particular $V$-[[enriched category]] $C$ is an **absolute colimit** if it is preserved by every $V$-functor with domain $C$.

Note, however, that a [[conical colimit]] in a $V$-category $C$ may be preserved by all $V$-functors without being preserved by all unenriched functors on the underlying ordinary category $C_o$.

Generalizing in a different direction, absolute colimits in $Set$-enriched categories can be regarded as the particular case of [[postulated colimit]]s in [[sites]] where the site has the [[trivial topology]].


### Weights for absolute colimits

+-- {: .num_defn #DefWeight}
###### Definition
For a given $V$, a [[weighted colimit|weight]] $\Phi\colon D^{op} \to V$ for colimits is an **absolute weight**, or a **weight for absolute colimits**, if $\Phi$-weighted colimits in *all* $V$-categories are preserved by all $V$-functors.
=--

Absolute colimits of this sort are also called **Cauchy colimits**.  A $V$-[[category]] which admits all absolute colimits --- that is, all $V$-weighted colimits whose weights are absolute -- is called [[Cauchy complete category|Cauchy complete]].  By the characterization below, it is equivalent to admit *limits* weighted by all weights for absolute limits.


## Characterizations

Both types of absolute colimits admit pleasant characterizations.

### Particular absolute colimits

For a particular [[cocone]] $\mu \colon F \to \Delta A$ under a functor $F\colon I\to C$ (all in the Set-enriched world), the following are equivalent:

* $\mu$ is an absolute colimiting cocone.

* $\mu$ is a colimiting cocone which is is preserved by the [[Yoneda embedding]] $C \hookrightarrow [C^{op},Set]$.

* $\mu$ is a colimiting cocone which is preserved by the representable functors $C(F(i),-)\colon C\to Set$ (for all $i\in I$) and $C(A,-)\colon C\to Set$.

* There exists $i_0\in I$ and $d_0\colon A\to F(i_0)$ such that
  1. For every $i\in I$, $d_0 \circ \mu_i$ and $1_{F(i)}$ are in the same connected component of the [[comma category]] $(F(i) / F)$.
  1. $\mu_{i_0} \circ d_0 = 1_{A}$.

The equivalence of the first two is basically because the Yoneda embedding is the [[free cocompletion]] of $C$.  The third clearly follows from the second.  The fourth follows from the third by inspecting exactly what preservation by those representables means in terms of colimits in [[Set]] (as is explained in more detail in the special case of [[absolute coequalizers]]).  Finally, it is straightforward to check that the fourth implies that $\mu$ is colimiting, and it is clearly a property preserved by any functor.

Note that in particular, the fourth condition implies that $A$ is a [[retract]] of $F(i_0)$.  Also, the first half of the fourth condition by itself characterizes absolute [[weak colimits]].

It is also possible to prove directly that the third condition implies the first two, without extracting the fourth condition along the way.  Namely, Let $B$ be the full subcategory of $C$ consisting of the objects $F(i)$ and $A$.  Then $F$ defines a functor $I\to B$; call it $F'$.  Note that $A$ is also the colimit of $F'$ in $B$.  Moreover, by the equivalence of the first two conditions, $A$ is an *absolute* colimit of $F'$, since by hypothesis it is preserved by all representable functors out of $B$.  Therefore, this colimit is in particular preserved by the inclusion $B\hookrightarrow C$, along with its composite with any functor out of $C$; so $A$ is an absolute colimit of $F$.


### Weights for absolute colimits
 {#CharacterizationsWeightsForAbsoluteColimits}

Let $V$ be a B&#233;nabou [[cosmos]] and $J\colon K &#x21F8; A$ a $V$-[[profunctor]].  Then the following are equivalent:

* $J$ is a weight for absolute colimits (i.e. $J$-weighted colimits in any $V$-category are preserved by all $V$-functors)

* $J$ has a [[right adjoint]] $J^*$ in the [[bicategory]] $V$-[[Prof]].

* There is a weight $J^*\colon A &#x21F8; K$ such that $J$-weighted colimits coincide naturally with $J^*$-weighted limits.


## Examples
 {#Examples}

### Particular absolute colimits

Of course, every colimit weighted by a weight for absolute colimits is itself a particular absolute colimit.  But it may also happen that a particuclar colimit may be absolute without all colimits of that shape being absolute.  For example (in ordinary category theory, with $V=Set$):

* [[split coequalizers]] are absolute, and figure in Beck's [[monadicity theorem]].
* More generally (of course), [[absolute coequalizers]] are absolute.
* [[absolute pushouts]] appear in [[elegant Reedy categories]].

We can also say something about non-examples.

* Initial objects (in $Set$-enriched categories) are *never* absolute.  If $0$ is an initial object, then it is never preserved by the representable functor $C(0,-)\colon C \to Set$.

* Similarly, coproducts in $Set$-enriched categories are never absolute.

### Weights for absolute colimits
 {#WExampleseightsForAbsoluteColimits}


In ordinary $Set$-enriched category theory there are not very many weights for absolute colimits, but we have

* [[split idempotents]].

In fact, this example is "universal," in that an ordinary category is Cauchy complete iff it has split idempotents, although not every absolute colimit "is" the splitting of an idempotent.  More precisely, the class of absolute $Set$-limits is the [[saturated class of limits|saturation]] of idempotent-splittings.

In [[enriched category theory]] there can be more types of absolute colimits.  For instance:

* in categories with [[zero morphisms]] (that is, enriched over [[pointed sets]]), [[initial objects]] are absolute.

* in [[Ab-enriched categories]] (or, more generally, categories enriched over commutative [[monoids]]), finite [[biproducts]] are absolute.  Finite biproducts and splitting of idempotents together are "universal" absolute colimits for Ab-enrichment.

* in [[SupLat]]-enriched categories, arbitrary small biproducts are absolute, and together with splitting of idempotents these generate all absolute colimits.

* in [[dg-categories]] (or more generally, categories enriched over [[graded set|graded sets]]), *shifts/suspensions* and [[mapping cones]] are absolute.

* in Lawvere [[metric spaces]], limits of Cauchy sequences are absolute.  This is the origin of the name "Cauchy colimit."

* in [[posets]], suprema of subsets with a greatest element are absolute.

* in categories [[bicategory-enriched category|enriched]] over the [[bicategory]] (or [[double category]]) of relations in a [[site]], *gluings* are absolute.  In this case the enriched categories can roughly be identified with [[separated presheaves]] and the Cauchy-complete ones with [[sheaves]].

* in categories enriched over [[rational number|rational]] [[vector spaces]], quotients by finite [[group actions]] are absolute.

New kinds of absolute (co)limits also arise in [[higher category theory]].

* for [[(∞,1)-categories]] (enriched over $\infty$-groupoids), splitting of idempotents is a universal absolute colimit.

* in [[stable (∞,1)-categories]] (which are enriched, in the $(\infty,1)$-categorical sense, over the $(\infty,1)$-category of [[spectra]]), initial objects and [[pushouts]] are absolute, and therefore so are all finite colimits.

## References


* [[Ross Street]], *Absolute colimits in enriched categories*, [Cahiers 1983](http://www.numdam.org/item/CTGDC_1983__24_4_377_0/)
* [[Robert Pare]], *On absolute colimits*, J. Alg. 19 (1971), 80-95.
* [[Mike Shulman]]'s answer to [*What are _all_ of the exactness properties enjoyed by stable ∞-categories?*](https://mathoverflow.net/a/267324)

[[!redirects absolute colimits]]
[[!redirects absolute limit]]
[[!redirects absolute limits]]
[[!redirects Cauchy colimit]]
[[!redirects Cauchy colimits]]
