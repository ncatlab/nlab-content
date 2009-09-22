<div class="rightHandSide toc">

***
[[!include category theory - contents]]
</div>


#Contents#
* tic
{:toc}

#Idea#

In [[category theory]] a limit of a [[diagram]] $F : D \to C$ in a [[category]] $C$ is an [[object]] $lim F$ of $C$ equipped with morphisms to the objects $F(d)$ for all $d \in D$, such that everything in sight commutes. Moreover, the limit $lim F$ is the _universal_ object with this property, i.e. the "most optimized solution" to the problem of finding such an object.

The limit construction has a wealth of applications throughout category theory and mathematics in general.  In practice, it is possibly best thought of in the context of [[representable functor]]s as a **classifying space** for maps into a diagram. So in some sense the limit object $lim F$ "subsumes" the entire diagram $F(D)$ into a single object, as far as morphisms _into_ it are concerned.
The corresponding universal object for morphisms _out_ of the diagram is the [[colimit]].

Often, the general theory of limits (but not colimits!) works better if the source of $F$ is taken to be the [[opposite category]] $D^op$ (or equivalently, if $F$ is taken to be a [[contravariant functor]]).  This is what we do below.  In any given situation, of course, you use whatever categories and functors you\'re interested in.

In some cases the category-theoretic notion of limit does reproduce notions of limit as known from analysis. See the examples below.

## Global versus local ##

In correspondence to the _local_ defintion of [[adjoint functor]]s (as discussed there), there is a _local_ definition of limits (in terms of cones), that defines a limit (if it exists) for each individual diagram, and there is a _global_ definition, which defines the limit for _all_ diagrams (in terms of an [[adjoint functor|adjoint]]).

If all limits over the given shape of diagrams exist in a category, then both definitions are equivalent.

See also the analogous discussion at [[homotopy limit]].


# Terminology and notation #

A limit is taken over a [[functor]] $F : D^{op} \to C$ and since the functor comes equipped with the information about what its domain is, one can just write $\lim F$ for its limit. But often it is helpful to indicate how the functor is evaluated on objects, in which case the limit is written $\lim_{d \in D} F(d)$; this is used particularly when $F$ is given by a formula (as with other notation with bound variables.)

In some schools of mathematics, limits are called _projective limits_, while colimits are called _inductive limits_.  Also seen are (repsectively) _inverse limits_ and _direct limits_.  Both these systems of terminology are alternatives to using 'co-' when distinguishing limits and colimits.  The first system also appears in [[pro-object]] and [[ind-object]].

Correspondingly, the symbols $lim_{\leftarrow}$ and $lim_{\rightarrow}$ are used instead of $lim$ and $colim$.  (Actually, the arrows should be directly underneath the '$lim$'s, something like ${\lim \atop \longleftarrow}$ and ${\lim \atop \longrightarrow}$.  But the text should also be at normal size.)

Confusingly, many authors restrict the meanings of these alternative terms to (co)limits whose sources are [[direction|directed set]]s; see [[directed limit]].  In fact, this is the original meaning; projective and inductive limits in this sense were studied in algebra before the general category-theoretic notion of (co)limit.

# Local definition in terms of representable functors #

There is a general abstract definition of limits
in terms of representable functors, which we 
describe now. This reproduces the more concrete
and maybe more familiar description in terms of
universal cones, which is described further below.

Let in the following $D$ be a [[small category]] and [[Set]] the category of sets (possibly realized as the category $U Set$ of $U$-small sets with respect to a given [[Grothendieck universe]].) 

## Limit of a Set-valued functors ##

The **limit of a Set-valued functor** $F : D^{op} \to Set$ is the [[hom-set]] 
$$
  lim F := Hom_{[D^{op}, Set]}(pt, F)
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

* the set of _global sections_ of $F$;

* the set of [[generalized element]]s of $F$.

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

Notice the important triviality that the covariant [[hom-functor]] comutes with set-valued limits: for every set $S$ we have a bijection of sets

$$
  Hom_{Set}(S, lim F)
  \simeq
  \lim Hom_{Set}(S, F(-))
  \,,
$$

where $Hom(S, F(-)) : D^{op} \to Set$.


## Limit of a functor with values in an arbitrary category ##

The above formula generalizes straightforwardly to
a notion of limit for 
functors $F : D^{op} \to C$ for $C$
an arbitrary category if we take the object "$lim F$"
to be a [[presheaf]] on $C$. The true $lim F$ is then,
if it exists, the object of $C$ 
[[representable functor|representing]] this presheaf.


More precisely, using the
the [[Yoneda embedding]]
$Y : C \to [C^{op}, Set]$ define for $F : D^{op} \to C$
the [[presheaf]] $\hat \lim F \in [C^{op}, Set]$ by
the analog of the above formula

$$
  (\hat \lim F)(d)
  \simeq
  Hom_{[C^{op}, Set]}(Y(d), lim F)
  :=
  \lim Hom_{[C^{op}, Set]}(Y(d), F(-))
$$

for all $d \in D$.

Here the $\lim$ on the right is again that of
[[Set]]-valued functors defined before.


By the above this can also be written as

$$
  (\hat lim F)(c) = 
  Hom_{[D^{op}, Set]}(pt , Hom_{[C^{op}, Set]}(c,F(-))
$$
or, suppressing the subscripts for readability:
$$
  (\hat lim F)(c) = 
  Hom(pt , Hom(c,F(-))
  \,.
$$

So also the [[presheaf]]-valued limit always exist. If this presheaf is [[representable functor|representble]] by an object $lim F$ of $F$, then this is the **limit** of $F$:

$$
  Hom(c, \lim F)
  \simeq
  Hom(pt, Hom(c,F(-)))
  \,.
$$

## Generalization to weighted limits ##

In the above formulation, there is an evident
generalization to [[weighted limit]]s:

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
 d \mapsto
    Hom_{[D^{op}, Set]}(W , Hom([C^{op}, Set]))(c,F(-))
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

## Relation to continuous functors ##

The very definition of limit as above asserts
that the covariant [[hom-functor]] 
$Hom(c,-) : C \to Set$
commutes with
forming limits. Indeed, the definition is equivalent
to saying that the [[hom-functor]] is a 
[[continuous functor]].


# Definition in terms of universal cones #

Unwrapping the above abstract definition of limits
yields the following more hands-on description  in terms
of universal cones.

## Unwrapping ##

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

This cone
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
again by the defining proprty of limit as above,
everey other cone $\{c \to F(d)\}_{d \in D}$ as 
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


# Global Definition in terms of adjoint of the constant diagram functor #

Given categories $D$ and $C$, limits over functors $D^{op} \to C$ may exist for some functors, but not for all. If it does exist for all functors, then the above _local definition_ of limits is equivalent to the following _global definition_.

For $D$ a [[small category]] and $C$ any category, the [[functor category]] $[D^{op},C]$ is the category of $D$-[[diagram]]s in $C$.  Pullback along the functor $D^{op} \to pt$ to the [[terminal object|terminal]] category $pt = \{\bullet\}$ induces a functor
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
which sends every diagram to its [[limit]]. The Hom-isomorphisms of these [[adjunction]]s state precisely the universal property of [[limit]] and [[colimit]] given above.

Concretely this means that for all $c \in C$ we have a bijection
$$
  Hom_C(c, \lim F)
  \simeq
  Hom_{[D^{op},C]}(const_X, F)
  \,.
$$

Compare this with the discussion at [[Kan extension]].


## Relation to Kan extension ##

From this perspective, a limit is a special case of a [[Kan extension]], as described there, namely a Kan extension to the [[point]].

# Definition for $(\infty,1)$-categories #

The definition of a limit as a terminal cone
has a straightforward generalization to the 
context of 
[[(infinity,1)-category|(infinity,1)-categories]].


+-- {: .un_defn}
###### Definition

For $K$ and $C$ two [[quasi-category|quasi-categories]] and $F : K \to C$ a morphism of [[quasi-category|quasi-categories]], the **limit** over $F$ is, if it exists, the [[terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category|over quasi-categories]] $C_{/F}$:

$$
  lim F := TerminalObj(C_{/F})
  \,.
$$

=--

For more details see [[limit in quasi-categories]].





#Examples#

* For a pedagogical list of examples see [[limits and colimits by example]].

## Types of shapes of limit cones ##

Here are some important examples of limits, classified by the shape of the diagram:

* A limit of the [[empty set|empty diagram]] is a [[terminal object]].
* A limit of a diagram consisting of two (or more) objects and no nontrivial morphisms is their [[product]].
* A limit of a [[cospan]] is a [[pullback]].
* A limit of a pair (or more) of [[parallel morphisms]] is an [[equalizer]].
* Another important "shape" of limits are those that give rise to [[end]]s.

##Properties#

+-- {: .un_prop}
###### Limits in Set are hom-sets

For $F : D^{op} \to Set$ any functor and $const_{*} : D^{op} \to Set$ the functor constant on the [[point]], the limit of $F$ is the [[hom-set]]
$$
  lim F \simeq [D^{op}, Set](const_{*}, F)
$$
in the [[functor category]], i.e. the set of [[natural transformation]]s from the constant functor into $F$.
=--

+-- {: .un_prop}
###### Covariant Hom commutes with limits

For $C$ a [[locally small]] category,
for $F : D^{op} \to C$ a functor and writing $C(c, F(-)) : CD^{op} \to Set$, we have
$$
  C(c, lim F) \simeq lim C(c, F(-))
  \,.
$$
=--

Depending on how one introduces limits this holds by definition or is an easy consequence.


+-- {: .un_prop}
###### Proposition -- limits in functor categories are computed pointwise

Let $D$ be a small category and let $D'$ be any category. Let $C$ be a category which admits limits of shape $D$. Write $[D',C]$ for the [[functor category]]. Then
* $[D',C]$ admits $D$-shaped limits;
* these limits are computed objectwise ("pointwise") in $C$:  for $F : D^{op} \to [D',C]$ a functor we have for all $d' \in D'$ that $(lim F)(d') \simeq lim (F(-)(d'))$. Here the limit on the right is in $C$.
=--

+-- {: .un_prop}
###### Proposition -- small limits commute with small limits

Let $D$ and $D'$ be small catgeories and let $C$ be
a category which admits limits of shape $D$ as well as
limits of shape $D'$. Then these limits commute with each other, in that 

for $F : D^{op} \times {D'}^{op} \to C$ a functor , with corresponding induced functors $F_D : {D'}^{op} \to [D^{op},C]$ and $F_{D'} : {D}^{op} \to [{D'}^{op},C]$, then
$$
  lim F \simeq lim_{D}  (lim_{D'} F_D )
  \simeq
   lim_{D'}  (lim_{D} F_{D'} )
  \,.
$$
=--

+-- {: .un_prop}
###### Proposition -- right adjoints commute with limits

Let $R : C \to C'$ be a functor that is [[right adjoint]] to some functor $L : C' \to C$. Let $D$ be a small category such that $C$ admits limits of shape $D$. Then $R$ commutes with $D$-shaped limits in $C$ in that

for $F : D^{op} \to C$ some diagram, we have
$$
  R(lim F) \simeq lim (R \circ F)
  \,.
$$
=--

+-- {: .proof}
######Proof

Using the adjunction isomorphism and the above fact that Hom commutes with limits, one obtains for every $c' \in C'$
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

Since this holds naturally for every $c'$, the [[Yoneda lemma|Yoneda lemma, corollary II]] on uniquenes of representing objects implies that $R (lim F) \simeq lim (G \circ F)$.
=--


+-- {: .un_prop}
###### Proposition -- limits are equalizers of products

The limit of $F : D^{op} \to C$ is, if it exists, a [[nLab:subobject|subobject]] of the [[nLab:product|product]] of the $F(d)$, namely the [[nLab:equalizer|equalizer]] of

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\prod_{f \in Mor(d)} (F(f) \circ p_{t(f)}) }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))
$$

and

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\prod_{f \in Mor(d)} (p_{s(f)}) }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))  
  \,.
$$

In particular therefore, a category has all limits already if it has all products and equalizers.

=--

See [[limits and colimits by example]] for what this formula says for instance for the special case $C =$ [[Set]].

## Commutativity of limits with colimits ##

In general limits do not commute with colimits. But under a number of special conditions of interest they do. More on that at [[commutativity of limits and colimits]].


[[!redirects limits]]

