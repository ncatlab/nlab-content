
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of $\infty$-groupoid is the generalization of that of [[group]] and [[groupoid]]s to [[higher category theory]]:

an $\infty$-groupoid -- equivalently an [[(∞,0)-category]] -- is an [[∞-category]] in which all [[k-morphism]]s for all $k$ are [[equivalences]]. 

The collection of all $\infty$-groupoids forms the [[(∞,1)-category]] [[∞Grpd]].

Special cases of $\infty$-groupoids include [[groupoid]]s, [[2-groupoid]]s, [[3-groupoid]]s, [[n-groupoid]]s, [[delooping]]s of [[group]]s, [[2-group]]s, [[∞-group]]s.


## Properties

### Presentations

There are many ways to [[presentable (∞,1)-category|present]] the [[(∞,1)-category]] [[∞Grpd]] of all $\infty$-groupoids, or at least obtain its [[homotopy category]].

A simple and very useful incarnation of $\infty$-groupoids is available using a [[geometric definition of higher categories]] in the form of [[simplicial sets]] that are [[Kan complex]]es: the $k$-cells of the underlying simplicial set are the [[k-morphism]]s of the $\infty$-groupoid, and the Kan [[horn]]-[[filler]] conditions encode the fact that adjacent $k$-morphisms have a (non-unique) composite $k$-morphism and that every $k$-morphism is invertible with respect to this composition.
See [[Kan complex]] for a detailed discussion of how these incarnate $\infty$-groupoids. 

The [[(∞,1)-category]] of all $\infty$-groupoids is [[presentable (∞,1)-category|presented]] along these lines by the Quillen [[model structure on simplicial sets]], whose fibrant-cofibrant objects are precisely the Kan complexes:

$$
  \infty Grpd \simeq (sSet_{Quillen})^\circ
  \,.
$$

One may turn this geometric definition into an [[algebraic definition of higher category|algebraic definition of ∞-groupoids]] by _choosing [[horn]]-fillers_ . The resulting notion is that of an [[algebraic Kan complex]] that has been shown by [[Thomas Nikolaus]] to yield an equivalent [[(∞,1)-category]] of $\infty$-groupoids.

There are various model categories which are [[Quillen equivalence|Quillen equivalent]] to $sSet_{Quillen}$. For instance the standard [[model structure on topological spaces]], a [[model structure on marked simplicial sets]] and many more. All these therefore present [[∞Grpd]].

Moreover, the corresponding  [[homotopy category of an (∞,1)-category]] $Ho(\infty Grpd)$, hence a category whose objects are [[homotopy types]] of $\infty$-groupoids, is given by the [[homotopy category]] of the [[category of presheaves]] over any _[[test category]]_. See there for more details.

Every other algebraic definition of [[omega-categories]] is supposed to yield an equivalent notion of $\infty$-groupoid when restricted to $\omega$-categories all whose [[k-morphism]]s are invertible. This is the statement of the [[homotopy hypothesis]], which is for Kan complexes and algebraic Kan complexes a theorem and for other definitions regarded as a consistency condition.

 
Notably in [[Pursuing Stacks]] and the earlier letter to [[Larry Breen]], [[Alexander Grothendieck]] initiated the study of $\infty$-groupoids and the homotopy hypothesis with his original definition of [[Grothendieck weak infinity-groupoid]]s, that has recently attracted renewed attention.

### Strict $\infty$-groupoids

One may also consider entirely strict $\infty$-groupoids, usually called $\omega$-groupoids or [[strict ∞-groupoids]]. These are equivalent to [[crossed complexes]] of [[groups]] and [[groupoids]]. 

### Relation to $\infty$-groups

[[pointed object|Pointed]], [[0-connected]] $\infty$-groupoids  are the [[delooping]] $\mathbf{B}G$ of [[∞-group]]s (see _[[looping and delooping]]_). 

These are presented by [[simplicial group]]s. Notably, abelian simplicial groups are therefore a model for abelian $\infty$-groupoids (more precisely, [[HA|H$\mathbb{Z}$]]-[[(∞,1)-module|modules]]). Under the [[Dold-Kan correspondence]] these are equivalent to non-negatively graded [[chain complex]]es, which therefore also are a model for abelian $\infty$-groupoids. This way much of [[homological algebra]] is secretly the study of special (structured) $\infty$-groupoids.

## Related concepts

* [[discrete ∞-groupoid]], [[∞-stack]], [[cohesive ∞-groupoid]]

* [[homotopy theory]], [[(∞,1)-category]]

* [[model structure for ∞-groupoids]]

* [[∞Grpd]]

* [[homotopy hypothesis]], [[test category]], [[modelizer]]



[[!include homotopy n-types - table]]

## Terminology

The term ∞-groupoid is sometimes considered to be too unwieldy,
and some alternatives have been suggested or used, but none has gained wide acceptance.

Historically, the word “space” is often (ab)used to mean ∞-groupoid, due to the traditional presentation of $\infty Gpd$ by the [[model structure on topological spaces]].  Some have [condemned](https://nforum.ncatlab.org/discussion/4781/against-spaces-in-homotopy-theory/) this usage, but others argue that a "homotopy space" is a valid notion of "space".

The term “homotopy type” is also quite close in meaning to “∞-groupoid”.  Historically, it differed in that morphisms of homotopy types were mere homotopy classes of maps of ∞-groupoids, but more recently (especially with the advent of [[homotopy type theory]] some have used "homotopy type" synonymously with "$\infty$-groupoid".

More radically, [[Dustin Clausen]] and [[Peter Scholze]] use the term “anima” (plural: anima) as a synonym for $\infty$-groupoid, in particular in relation to [[condensed mathematics]].  Reference: [nCafe](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057623).  In
_Purity for flat cohomology_ by
Kęstutis Česnavičius and Peter Scholze they write
“If the objects of $C$ are called widgets, then we call those of $Ani(C)$ animated widgets, except that we abbreviate $Ani(Set)$ to $Ani$ and the term ‘animated set’ to anima (plural: anima).”


## References

* [[Jacob Lurie]], Section 1.1.2 in: *[[Higher Topos Theory]]*, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))


Formulations in [[homotopy type theory]] include

* [[Thorsten Altenkirch]], Ondrej Ryp&#225;cek, _A Syntactical Approach to Weak $\omega$-Groupoids_ ([pdf](http://www.cs.nott.ac.uk/~txa/publ/weakomega2.pdf))

See also at _[[category object in an (infinity,1)-category]]_ for more along these lines.


[[!redirects ∞-groupoid]]
[[!redirects ∞-groupoids]]
[[!redirects infinity-groupoid]]
[[!redirects infinity-groupoids]]
[[!redirects infinity groupoid]]
[[!redirects $\infty$-groupoid]]

[[!redirects weak omega-groupoid]]
[[!redirects weak ∞-groupoid]]
[[!redirects weak omega-groupoids]]
[[!redirects weak ∞-groupoids]]

[[!redirects weak ∞-groupoid]]
[[!redirects weak ∞-groupoids]]
[[!redirects weak infinity-groupoid]]
[[!redirects weak infinity-groupoids]]


category:∞-groupoid


