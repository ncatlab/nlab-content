
> This entry is about the notion of "limit" in [[category theory]]. For the notion of the same name in [[analysis]] and [[topology]] see _[[limit of a sequence]]_ and _[[limit of a function]]_.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In [[category theory]] a limit of a [[diagram]] $F : D \to C$ in a [[category]] $C$ is an [[object]] $lim F$ of $C$ equipped with morphisms to the objects $F(d)$ for all $d \in D$, such that everything in sight commutes. Moreover, the limit $lim F$ is the _universal_ object with this property, i.e. the "most optimized solution" to the problem of finding such an object.

The limit construction has a wealth of applications throughout category theory and mathematics in general.  In practice, it is possibly best thought of in the context of [[representable functor|representable functors]] as a [[classifying space]] for maps into a diagram. So in some sense the limit object $lim F$ "subsumes" the entire diagram $F(D)$ into a single object, as far as morphisms _into_ it are concerned.
The corresponding universal object for morphisms _out_ of the diagram is the [[colimit]]. 

An intuitive general idea is that a limit of a diagram is the locus or solution set of a bunch of equations, where each of the coordinates is parametrized by one of the objects of the diagram, and where the equations are prescribed by the morphisms of the diagram. This idea is explained more formally [here](http://ncatlab.org/nlab/show/limits+and+colimits+by+example#limitsintermsofotherops). 

Often, the general theory of limits (but not colimits!) works better if the source of $F$ is taken to be the [[opposite category]] $D^op$ (or equivalently, if $F$ is taken to be a [[contravariant functor]]).  This is what we do below.  In any given situation, of course, you use whatever categories and functors you\'re interested in.

In some cases the category-theoretic notion of limit does reproduce notions of limit as known from analysis. See the examples below.

### Global versus local 

In correspondence to the _local_ definition of [[adjoint functor|adjoint functors]] (as discussed there), there is a _local_ definition of limits (in terms of cones), that defines a limit (if it exists) for each individual diagram, and there is a _global_ definition, which defines the limit for _all_ diagrams (in terms of an [[adjoint functor|adjoint]]).

If all limits over the given shape of diagrams exist in a category, then both definitions are equivalent.

See also the analogous discussion at [[homotopy limit]].


## Terminology and notation 

A limit is taken over a [[functor]] $F : D^{op} \to C$ and since the functor comes equipped with the information about what its domain is, one can just write $\lim F$ for its limit. But often it is helpful to indicate how the functor is evaluated on objects, in which case the limit is written $\lim_{d \in D} F(d)$; this is used particularly when $F$ is given by a formula (as with other notation with bound variables.)

In some schools of mathematics, limits are called _projective limits_, while colimits are called _inductive limits_.  Also seen are (respectively) _inverse limits_ and _direct limits_.  Both these systems of terminology are alternatives to using 'co-' when distinguishing limits and colimits.  The first system also appears in [[pro-object]] and [[ind-object]].

Correspondingly, the symbols $\underset{\leftarrow}lim$ and $\underset{\rightarrow}\lim$ are used instead of $\lim$ and $\colim$.

Confusingly, many authors restrict the meanings of these alternative terms to (co)limits whose sources are [[direction|directed sets]]; see [[directed limit]].  In fact, this is the original meaning; projective and inductive limits in this sense were studied in algebra before the general category-theoretic notion of (co)limit.

## Definition

### Local definition in terms of representable functors 

There is a general abstract definition of limits
in terms of representable functors, which we 
describe now. This reproduces the more concrete
and maybe more familiar description in terms of
universal cones, which is described further below.

Let in the following $D$ be a [[small category]] and [[Set]] the category of sets (possibly realized as the category $U Set$ of $U$-small sets with respect to a given [[Grothendieck universe]].) 

#### Limit of a Set-valued functor

The **limit of a Set-valued functor** $F : D^{op} \to Set$ is the [[hom-set]] 
$$
  lim F \coloneqq Hom_{[D^{op}, Set]}(pt, F)
  \in Set
$$
in the [[functor category]] $[D^{op}, Set]$ (the [[presheaf]] category), where

$$
  pt : D^{op} \to Set
$$
$$
  pt : d \mapsto \{*\}
$$
is the functor constant on the [[point]], i.e. the [[terminal object|terminal]] diagram.

The set $lim F$ is equivalently called 

* the set of [[global section|global sections]] of $F$;

* the set of [[global element|global elements]] of $F$.

The set $lim F$ can be equivalently expressed as an [[equalizer]] of a [[product]], explicitly:

$$
  lim F \simeq
  \left\lbrace
    (x_d)_{d \in D}
    \in
    \prod_{d \in D}
    F(d)
    |
    \forall (d_i \stackrel{\alpha}{\to} d_j) \in D :
    F(\alpha)(x_{d_j}) = x_{d_i}
  \right\rbrace
$$

In particular, the limit of a set-valued functor always exists. 

Notice the important triviality that the covariant [[hom-functor]] commutes with set-valued limits: for every set $S$ we have a bijection of sets

$$
  Hom_{Set}(S, lim F)
  \simeq
  \lim Hom_{Set}(S, F(-))
  \,,
$$

where $Hom(S, F(-)) : D^{op} \to Set$.


#### Limit of a functor with values in an arbitrary category 

The above formula generalizes straightforwardly to
a notion of limit for 
functors $F : D^{op} \to C$ for $C$
an arbitrary category if we construct a certain [[presheaf]] on $C$ which we will call $\hat \lim F$. The actual limit $lim F$ is then, if it exists, the object of $C$ [[representable functor|representing]] this presheaf.

More precisely, using the [[Yoneda embedding]] $y: C \to [C^{op}, Set]$ define for $F : D^{op} \to C$ the [[presheaf]] $\hat \lim F \in [C^{op}, Set]$ by

$$
  (\hat \lim F)(c)\coloneqq Hom_{Set^{D^{op}}}(pt,Hom_C(c,F(-)))
$$

for all $c \in C$, or suppressing the subscripts for readability:

$$
  (\hat lim F)(c) = 
  Hom(pt , Hom(c,F(-)))
  \,.
$$

The [[presheaf]]-valued limit always exists; iff this presheaf is [[representable functor|representable]] by an object $\lim F$ of $C$, then this is the **limit** of $F$:

$$
  Hom(c, \lim F)
  \simeq
  Hom(pt, Hom(c,F(-)))
  \,.
$$

#### Generalization to weighted limits 

In the above formulation, there is an evident
generalization to [[weighted limit|weighted limits]]:

replace in the above the constant terminal functor
$pt : D^{op} \to Set$ with _any_ functor
$W : D^{op} \to Set$ -- then called the _weight_ --,
then the $W$-weighted limit of $F$ 

$$
  \lim_W F
$$

often written

$$
  \{W,F\}
$$

is, if it exists, the
object representing the presheaf
$$
 c \mapsto
    Hom_{[D^{op}, Set]}(W , Hom_C(c,F(-)))
  \,,
$$

i.e. such that

$$
  Hom(c, \lim_W F)
  \simeq
  Hom(W, Hom(c,F(-)))
  \,
$$

naturally in $c \in C$.

#### Relation to continuous functors 

The very definition of limit as above asserts
that the covariant [[hom-functor]] 
$Hom(c,-) : C \to Set$
commutes with
forming limits. Indeed, the definition is equivalent
to saying that the [[hom-functor]] is a 
[[continuous functor]].


### Definition in terms of universal cones 

Unwrapping the above abstract definition of limits
yields the following more hands-on description  in terms
of universal cones.

#### Unwrapping 

Let $F : D^{op} \to C$ be a functor.

Notice that for every object $c \in C$ an element
$$
  * \to Hom(pt, Hom(c, F(-)))
$$ 
is to be identified with a collection of morphisms
$$
  c \to F(d)
$$
for all $d \in D$, such that all triangles
$$
  \array{
     && c
     \\
     & \swarrow && \searrow
     \\
     F(d_i)
     && \stackrel{F(f)}{\to}
     &&
     F(d_j)
  }
$$
commute. Such a collection of morphisms is called a **cone** over $F$, for the obvious reason. 

If the limit 
$\lim F \in C$ of $F$ exist, then it
singles out a special cone given by
the composite morphism
$$
  *
  \stackrel{* \mapsto Id_{\lim F}}{\to}
  Hom_C(\lim F, \lim F)
  \stackrel{\simeq}{\to}  
  Hom(pt, Hom(\lim F, F(-)))
  \,,
$$
where the first morphism picks the [[identity morphism]]
on $\lim F$ and the second one is the defining
bijection of a limit as above.

The cone
$$
  \array{
     && \lim F
     \\
     & \swarrow && \searrow
     \\
     F(d_i)
     && \stackrel{F(f)}{\to}
     &&
     F(d_j)
  }
$$
is called the **universal cone** over $F$, because,
again by the defining property of limit as above,
every cone $\{c \to F(d)\}_{d \in D}$ as 
above is bijectively related to a morphism
$c \to  \lim F$ 

$$
  *
  \stackrel{\{c \to F(d)\}_{d \in D}}{\to}
  Hom(pt, Hom(c, F(-)))
  \stackrel{\simeq}{\to}  
  Hom(c, \lim F)
  \,.
$$

By inspection one finds that, indeed, the morphism
$c \to \lim F$ is the morphism which exhibits the
factorization of the cone $\{c \to F(d)\}_{d \in D}$
through the universal limit cone

$$
  \array{
     && c
     \\
     & \swarrow && \searrow
     \\
     F(d_i)
     && \stackrel{F(f)}{\to}
     &&
     F(d_j)
  }
  =
  \array{
     && c
     \\
     && \downarrow
     \\
     && \lim F
     \\
     & \swarrow && \searrow
     \\
     F(d_i)
     && \stackrel{F(f)}{\to}
     &&
     F(d_j)
  }
  \,.
$$
An illustrative example is the following: a limit of the [[identity functor]] $Id_c:C\to C$ is, if it exists, an [[initial object]] of $C$.


### Global definition in terms of adjoint of the constant diagram functor 

Given categories $D$ and $C$, limits over functors $D^{op} \to C$ may exist for some functors, but not for all. If it does exist for all functors, then the above _local definition_ of limits is equivalent to the following _global definition_.

For $D$ a [[small category]] and $C$ any category, the [[functor category]] $[D^{op},C]$ is the category of $D$-[[diagram|diagrams]] in $C$.  Pullback along the functor $D^{op} \to pt$ to the [[terminal object|terminal]] category $pt = \{\bullet\}$ induces a functor
$$
  const :  C \to [D^{op},C]
$$
which sends every object of $C$ to the diagram functor constant on this object.

The [[adjoint functor|left adjoint]]
$$
  colim_D : [D^{op},C] \to C
$$
of this functor is, if it exists, the functor
which sends every diagram to its [[colimit]] and the [[adjoint functor|right adjoint]] is, if it exists, the functor
$$
  lim_D : [D^{op},C] \to C
$$
which sends every diagram to its [[limit]]. The Hom-isomorphisms of these [[adjunction|adjunctions]] state precisely the universal property of [[limit]] and [[colimit]] given above.

Concretely this means that for all $c \in C$ we have a bijection
$$
  Hom_C(c, \lim F)
  \simeq
  Hom_{[D^{op},C]}(const_c, F)
  \,.
$$


From this perspective, a limit is a special case of a [[Kan extension]], as described there, namely a Kan extension to the [[point]].

### Generalizations 

The notion of limit, being fundamental to 
[[category theory]], generalizes to many other situations.  Examples include the following.

* In [[enriched category theory]] one has the notion of [[weighted limit]].  This makes sense in ordinary category theory as well, but it turns out that in that case all weighted limits reduce to ordinary "conical" ones.
* Weighted limits generalize further to the notion of limit in a [[2-category equipped with proarrows]], or to a [[Yoneda structure]].
* In [[2-category theory]] one has the notion of a [[2-limit]].
* Similarly, in [[(infinity,1)-category]] theory there is a notion of a limit.  Using quasicategories as a model for $(\infty,1)$-categories, the definition is a straightforward extension of the one as a terminal cone: it is simply a [[terminal object in a quasi-category|quasi-categorical terminal object]] in the quasicategory of cones.  See [[limit in quasi-categories]].
* One expects that similarly, all sorts of [[higher categories]] have their own appropriate notions of limit and colimit.  


## Examples

The central point about examples of limits is:

_Categorical limits are ubiquitous_. 

To a fair extent, [[category theory]] is all about limits and the other [[universal construction|universal constructions]]: [[Kan extension|Kan extensions]], [[adjoint functor|adjoint functors]], [[representable functor|representable functors]], which are all special cases of limits -- and limits are special cases of these.

Listing examples of limits in [[category theory]] is much like listing examples of [[integral|integrals]] in [[analysis]]: one can and does fill books with these. (In fact, that analogy has more to it than meets the casual eye: see [[coend]] for more).


Keeping that in mind, we do list some special cases and special classes of examples that are useful to know. But any list is necessarily wildly incomplete.

### General

* For a pedagogical list of examples see [[limits and colimits by example]].

Here are some important examples of limits, classified by the shape of the [[diagram]]:

* A limit of the [[empty set|empty diagram]] is a [[terminal object]].
* A limit of a diagram consisting of two (or more) objects and no nontrivial morphisms is their [[product]].
* A limit of a [[cospan]] is a [[pullback]].
* A limit of a pair (or more) of [[parallel morphisms]] is an [[equalizer]].
* A limit over a [[finite category]] is a [[finite limit]].
* Another important "shape" of limits are those that give rise to [[end|ends]].
* A limit of a diagram $F : D \to C$ for which $D$  admits an [[initial object]] $I$, is simply $F(I)$.

### Limits in analysis

The concept of [[limit of a sequence]] in [[topological spaces]] is a special case of category theoretic limits, see [there](limit+of+a+sequence#RelationToLimitsInCategoryTheory).

## Properties

### Existence: construction from products and equalizers
 {#ConstructionFromProductsAndEqualizers}

Frequently some limits can be computed in terms of other limits.  This makes things easier since we only have to assume that categories have, or functors preserve, some easier-to-verify class of limits in order to obtain results about a larger one.

The most common example of this is the computation of limits in terms of products and equalizers.  Specifically, if the limit of $F : D^{op} \to C$ and the [[products]] $\prod_{d\in Obj(D)} F(d)$ and $\prod_{f\in Mor{d}} F(s(f))$ all exist, then $lim F$ is a [[subobject]] of $\prod_{d\in Obj(D)} F(d)$, namely the [[equalizer]] of

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\prod_{f \in Mor(d)} (F(f) \circ p_{s(f)}) }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))
$$

and

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\prod_{f \in Mor(d)} (p_{t(f)}) }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))  
  \,.
$$

Conversely, if both of these products exist and so does the equalizer of this pair of maps, then that equalizer is a limit of $F$.  In particular, therefore, a category has all limits as soon as it has all products and equalizers, and a functor defined on such a category [[preserved limit|preserves]] all limits as soon as it preserves products and equalizers.

(More precisely, it suffices only to consider equalizers of [[reflexive pairs]].)

Another example is that all [[finite limits]] can be computed in terms of [[pullbacks]] and a [[terminal object]].

### Interaction with $Hom$-functor

+-- {: .num_prop}
###### Proposition
**([[hom-functor preserves limits]])**

For $C$ a [[locally small]] category,
for $F : D^{op} \to C$ a functor and writing $C(c, F(-)) : D^{op} \to Set$, we have
$$
  C(c, lim F) \simeq lim C(c, F(-))
  \,.
$$
=--

Depending on how one introduces limits this holds by definition or is an easy consequence.




### In $Set$

+-- {: .num_prop}
###### Limits in Set are hom-sets

For $F : D^{op} \to Set$ any functor and $const_{*} : D^{op} \to Set$ the functor constant on the [[point]], the limit of $F$ is the [[hom-set]]
$$
  lim F \simeq [D^{op}, Set](const_{*}, F)
$$
in the [[functor category]], i.e. the set of [[natural transformation|natural transformations]] from the constant functor into $F$.
=--

### In functor categories

+-- {: .un_prop}
###### Proposition
**(limits in functor categories are computed pointwise)

Let $D$ be a small category and let $D'$ be any category. Let $C$ be a category which admits limits of shape $D$. Write $[D',C]$ for the [[functor category]]. Then

* $[D',C]$ admits $D$-shaped limits;
* these limits are computed objectwise ("pointwise") in $C$: for $F : D^{op} \to [D',C]$ a functor we have for all $d' \in D'$ that $(lim F)(d') \simeq lim (F(-)(d'))$. Here the limit on the right is in $C$.
=--

### Compatibility with universal constructions
 {#CompatibilityAmongUniversalConstructions}

+-- {: .num_prop #RightAdjointsPreserveLimits}
###### Proposition
**([[right adjoints preserve limits]])

Let $R \;\colon\; C \to C'$ be a [[functor]] that is [[right adjoint]] to some functor $L : C' \to C$. Let $D$ be a [[small category]] such that $C$ admits [[limits]] of shape $D$. Then $R$ [[preserved limit|commutes with]] $D$-shaped limits in $C$ in that

for $F : D^{op} \to C$ some diagram, we have

$$
  R(lim F) \simeq lim (R \circ F)
  \,.
$$
=--

+-- {: .proof}
######Proof

Using the adjunction isomorphism and the above fact that [[hom-functor preserves limits]], one obtains for every $c' \in C'$

$$
\begin{aligned}
  C'(c', R (lim F)) & \simeq C(L(c'), lim F)
  \\
  & \simeq lim C(L(c'), F) 
  \\
  & \simeq lim C'(c', R\circ F)
  \\
  & \simeq C'(c', lim (R \circ F)) 
  \,.
\end{aligned}
  \,.
$$

Since this holds naturally for every $c'$, the [[Yoneda lemma|Yoneda lemma, corollary II]] on uniqueness of representing objects implies that $R (lim F) \simeq lim (R \circ F)$.

=--



+-- {: .num_prop #LimitsCommuteWithLimits}
###### Proposition
**([[limits commute with limits]])**

Let $D$ and $D'$ be [[small categories]] and let $C$ be
a category which admits [[limits]] of shape $D$ as well as
[[limits]] of shape $D'$. Then these limits commute with each other, in that 
for $F : D^{op} \times {D'}^{op} \to C$ a [[functor]] , with corresponding induced functors $F_D : {D'}^{op} \to [D^{op},C]$ and $F_{D'} : {D}^{op} \to [{D'}^{op},C]$, then the canonical comparison morphism 

\[
  \label{ComparisonMorphismForCommutingLimits}
  lim F \simeq lim_{D}  (lim_{D'} F_D )
  \simeq
   lim_{D'}  (lim_{D} F_{D'} )
\]

is an [[isomorphism]].

=--

+-- {: .proof}
######Proof

Since the [[limit]]-construction is the [[right adjoint]] functor to the [[constant functor|constant]] [[diagram]]-functor, this is a special case of _[[right adjoints preserve limits]]_ (Prop. \ref{RightAdjointsPreserveLimits}).

=--

See [[limits and colimits by example]] for what formula (eq:ComparisonMorphismForCommutingLimits) says for instance for the special case $C =$ [[Set]].

+-- {: .num_remark}
###### Remark
**(general non-commutativity of limits with colimits)**

In general limits do _not_ commute with [[colimits]]. But under a number of special conditions of interest they do. Special cases and concrete examples are discussed at _[[commutativity of limits and colimits]]_.

=--


## Related concepts

* **limit**

  * [[internal limit]]

  * [[colimit]], [[universal construction]], [[Kan extension]], [[end]], [[coend]]

* [[2-limit]]

* [[(∞,1)-limit]]

  * [[homotopy limit]]

  * [[lim^1 and Milnor sequences]]


## References

Limits and [[colimits]] were defined in [[Daniel M. Kan]] in Chapter II of the paper that also defined [[adjoint functors]] and [[Kan extensions]]:

* [[Daniel M. Kan]], _Adjoint functors_, Transactions of the American Mathematical Society 87:2 (1958), 294–294 ([doi:10.1090/s0002-9947-1958-0131451-0](https://doi.org/10.1090/s0002-9947-1958-0131451-0))

This paper refers to limits as _inverse limits_.

The observation that limits can be constructed from [[products]] and [[equalisers]] is due to:

* [[J.-M. Maranda]], *Some remarks on limits in categories*. Canadian Mathematical Bulletin **5** 2 (1962) 133-146 &lbrack;[doi:10.4153/CMB-1962-015-0](https://doi.org/10.4153/CMB-1962-015-0)&rbrack;

That, more generally, it suffices to consider only equalisers of [[reflexive pairs]] is due to:

* [[Ernest Manes]], *A triple miscellany: Some aspects of the theory of algebra over a triple*, PhD thesis, Wesleyan University, 1967. &lbrack;[pdf](https://github.com/CategoryTheoryArchive/archive/blob/main/resources/1967_manes_triple-miscellany.pdf)&rbrack;

* S. A. Huq and R. Cornu. _A remark on the existence of limits in categories_. Mathematische Nachrichten 55.1‐6 (1973): 223-224. &lbrack; [doi:10.1002/mana.19730550111](https://doi.org/10.1002/mana.19730550111)&rbrack;

Textbook accounts:

* [[Saunders MacLane]], §III.4 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


[[!redirects limits]]
[[!redirects limit functor]]
[[!redirects limit functors]]

[[!redirects limit of a functor]]
[[!redirects limits of a functor]]
[[!redirects limits of functors]]

[[!redirects limit of a cofunctor]]
[[!redirects limits of a cofunctor]]
[[!redirects limits of cofunctors]]

[[!redirects limit of a diagram]]
[[!redirects limits of a diagram]]
[[!redirects limits of diagrams]]
