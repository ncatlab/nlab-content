#Idea#


_Sieves_ are an equivalent way to encode [[subobject]]s of [[representable functor]]s in a [[presheaf]] category in terms of the total sets of _elements_ of such a subfunctor.

The notion of _sieve_ is usually used when certain such subobjects are singled out as [[cover]]s of a [[Grothendieck topology]]: the singled out subobjects then correspond to _covering sieves_.

+-- {: .query}
Urs, I changed 'coverage' back to 'Grothendieck topology' above, since it\'s specifically Grothendieck topologies that deal with covering sieves; coverages deal with arbitrary covering families (generally not sieves and generally not all of them), which is part of why coverages both can be more useful and are less canonical.

[[Urs Schreiber|Urs]]: hm, okay. My impression was that the point of coverages is that we don't impose the four axioms of Grothendieck topology on the covering things, while we do keep the notion of sieves itself. Because "sieve" is really just another way to say "subfunctor of a representable" so the question really is: which collections of subfunctors of representables do we want to use as coverages.  For me the 1-line definition of "coverage" would be: choice of subcollection of all monois in a given 1-topos. That then makes sense also in non-presheaf topoi. For presheaf topoi it happens to have a reformulation in terms of sieves.

So, in conclusion, I am thinking that the point of using more general coverages over Grothendieck topologies is not primarily to relax the closure under composition that makes a sieve a sieve. That's kind of a trivial thing. The point is that we don't need to impose the four axioms of a Grothendieck topology on the collection of all such.

But maybe not. This is just so you know what I am thinking. :-)

=--

A choice of collections of morphism $d \to c$ into an object $c \in C$  for each $d \in C$ reminds one of the [[representable functor]] [[presheaf]]
$Y(c) := \hom_C(-, c): C^{op} \to Set$ which assigns to each $d \in C$ the set of _all_ morphisms from $d$ to $c$. Every choice of covers of $c$ is therefore for each $d \in C$ a subset of the value of this functor evaluated at $d$. This begins to look like an [[monomorphism|monic]] [[natural transformation]] into this functor. Indeed, it turns out that one can assume without restriction of generality that the assignment of covers of $c$ can always be extended to such a monic natural transformation, and hence one formalizes the notion of "collection of covers" of $c$ as a [[subobject]] $i: F \hookrightarrow \hom(-, c)$ of the functor represented by $c$: a _sieve_ at $c$. 


#Definition#

Let $C$ be a [[small category]].

+-- {: .un_defn}
###### Definition

A _sieve_ $S$ (Fr. _crible_) on an object $c \in C$ is a subset $S \subset Ob(C/c)$ of the set of objects of the [[over category]] over $c$ which is _closed under precomposition_:  it has the property that with $(d \to c) \in S$ for every morphism $(e \to d) \in Mor(C)$ also the composite $(e \to d \to c)$ is in $S$.
=--


Sometimes the condition of a sieve being closed under the operation of precomposing with an arbitrary morphism $g: e \to d$ is called a "saturation condition". Given any collection of morphisms targeted at $c$, one can always close it up or saturate it, to obtain a sieve on $c$. 


# Relation to subfunctors #

There is a canonical way to create subfunctors from sieves and sieves from subfunctors.

+-- {: .query}
_Bruce_: What is a subfunctor? Can you link that word to a page?
=--

A subfunctor is a [[subobject]] in a [[functor category]]. Here, specifically, one is interested in [[subobject]]s in a [[presheaf]] category of [[representable functor]]s. It's these subfunctors of representable functors that are in bijection with sieves.

+-- {: .un_defn}
###### Definition

Given a sieve $S$ on $c$, the **subfunctor** $F_S \hookrightarrow Y(c)$ **defined by the sieve**  is the [[presheaf]] 

* that assigs to each object $d \in C$ the set $F_S(d) = \{(d \to c) \in S\}$;

* that assigns to each morphism $(d \to d') \in C$ the function $F_S(d') \to F_S(d)$ induced on elements by precomposition with $d \to d'$.
=--

+-- {: .un_defn}
###### Definition

Given a subfunctor $F \hookrightarrow Y(c)$, the **sieve defined by the subfunctor** is given by

* $S_F := \{g: d \to c \in Mor(C) | Y(d) \stackrel{Y(g)}\to Y(c) = Y(d)  \to F \to Y(c) \}$

or equivalently

* $S_F = \coprod_{d \in Obj(C)}F(d)$.
=--

+-- {: .un_lemma}
###### Lemma

These two definitions establish a bijection between sieves on $c$ and subobjects of $Y(c)$.

For every sieve $S$ we have

$$
  S_{F_S} = S
$$

and for every subfunctor we have

$$
  F_{S_F} = F
  \,.
$$
=--


+-- {: .un_remark}
###### Remarks

* The construction of $S_F$ makes sense for every morphism of presheaves $F \to Y(c)$. The sieve is sensitive precisely to the [[image]] of this map, 
$$
  S_{F} = S_{im (F \to Y(c))}
  \,.
$$

* In the presence of a [[Grothendieck topology]] a morphism $F \to Y(c)$ is sometimes called a [[local epimorphism]] if the sieve $S_F$ is a covering sieve. If $F \to Y(c)$ is actually a subfunctor, then it is called a [[dense monomorphism]].


* The [[pullback]] of a subfunctor $i: F_S \hookrightarrow Y(c) = \hom(-, c)$ along any morphism $\hom(-, g): \hom(-, d) \to \hom(-, c)$ is again a subfunctor $g^* F$ of $d$, hence sieves are closed under pulling back. Concretely, 
$$g^* S = \bigcup_{e \in Ob(C)} \{f: e \to d: g f \in S\}
\,.$$

* A sieve $S_F$ on $c$, for $i: F \hookrightarrow \hom(-, c)$ a subfunctor, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 
=--

+-- {: .un_lemma}
###### Lemma

The subfunctor $F_S \hookrightarrow X$ corresponding to a sieve $S$ is the [[coimage]] of the morphism out of the disjoint union of all objects (regarded as representable presheaves) in the sieve:

$$
 (U = \coprod_{(U_\alpha \to X) \in S} U_\alpha)  \to X
$$

in that

$$
  (F_S \to X) = ((colim(U \times_X U \stackrel{\to}{\to} U)   \to X)
  \,.
$$
=--

If the sieve is generated by (is the saturation of) a collection of morphisms $\{U_\alpha \to U\}$ then the same statement remains true with $U$ being the coproduct over just these $U_\alpha$.

+-- {: .proof}
###### Proof

As described at [[limits and colimits by example]], the colimit of presheaves may be computed objectwise in $Set$. Doing so and using the [[Yoneda lemma]] tells us that for each object $V$ we have

$$
  \begin{aligned}
    colim(U \times_X U \stackrel{\to}{\to} U)(V)
    & \simeq
    colim(Hom(V,U \times_X U) \stackrel{\to}{\to} Hom(V,U))
    \\
    & \simeq
    colim( Hom(V,U) \times_{Hom(U,X)} Hom(V,U)  \stackrel{\to}{\to} Hom(V,U))
  \end{aligned}
$$

where all objects appearing (at least in the first lines) are implicitly regarded as presheaves under the [[Yoneda embedding]].

But this colimit now manifestly computes the set

$$
  \{ maps from V to X that factor through U\}_\sim
$$

where the equivalence relation is

$$
  ((f \to U \to X) \sim (g \to U \to X))
  \Leftrightarrow
  (f and g coincide as maps to X)
  \,.
$$

So the set is just the set of maps from $V$ to $X$ that factor through one of the $U_\alpha$, which is precisely the set $F_S(V)$ assigned by the subfunctor corresponding to the sieve.
=--




#Examples#

* For $X$ a [[topological space]] let $Op(X)$ be the [[category of open subsets]] of $X$ and consider presheaves $PSh(X) := [Op(X)^{op}, Set]$ on $X$. For any open subset $c = V \in Op(X)$ let $\{d_i\} = \{U_i\}$ be a cover of $V$ by open subsets $U_i$ in the ordinary sense (i.e. each $U_i$ is an open subset of $V$ and their joint union is $V$, $\bigcup_i U_i = V$), then  $\pi : (\coprod_i Y(U_i)) \stackrel{\coprod_i U_i \hookrightarrow_i X}{\to} Y(V)$ (with $Y$ the [[Yoneda embedding]]) is a [[local epimorphism]] of presheaves on $V$ and its [[image]] -- or equivalently its [[coimage]] -- is the subfunctor $(F := \bigcup_i Y(U_i)) \hookrightarrow Y(V)$ that sends each $W \in Op(X)$ to the set of maps $W \to V$ that factor through one of the $U_i$. The collection of all such maps for all choice of $W$ is the corresponding _covering sieve_ $\{ f : W \to V  \in Mor(S) \;|\; f = W \to U_i \to V  \}$.

* The situation for more general [[site]]s $S$ other than $Op(X)$ is literally the same as above, with $U_i, W, V$ etc. objects of $S$.



# Recovering the sheaf condition from morphisms out of the sieve#

We now show that $F$ is the _right_ sieve incarnation of the cover by demonstrating that using it the usual [[sheaf|sheaf condition]] on a presheaf with respect to the cover $\coprod_i U_i$ is reproduced:

First notice that $F$ is precisely the [[coequalizer]] of the obvious pair of morphisms

$$
  \coprod_{i, j} \hom(-, U_i \cap U_j)
    \stackrel{\to}{\to}
  \coprod_i hom(-, U_i)
$$

where the domain of this parallel pair is the [[pullback]] of the evident map
$\coprod_i hom(-, U_i) \to hom(-,X)$  
along itself, and the two parallel arrows are the projection maps out of this pullback:

$$
  \array{
     \coprod_{i,j} hom(-,U_i \cap U_j)
     &\to&
     \coprod_i hom(-, U_j)
     \\
     \downarrow && \downarrow
     \\
     \coprod_i hom(-, U_i)
     &\to&
     hom(-,X)
  }
$$
 
Thus for $G$ any [[presheaf]],
maps $F \to G$ are precisely the same as maps
$\coprod_i \hom(-, U_i) \to G$
which coequalize the parallel pair. Applying $Hom_{Set^{C^{op}}}(-,G)$ to the colimit diagram

$$
  \coprod_{i, j} \hom(-, U_i \cap U_j)
    \stackrel{\to}{\to}
  \coprod_i hom(-, U_i)
  \to
  F
$$
                     
yields the limit diagram

$$
  Hom(F, G)
  \to 
  Hom(\coprod_i hom(-, U_i), G)
  \stackrel{\to}{\to}
  Hom(\coprod_{i, j} \hom(-, U_i \cap U_j), G)
$$

which using [[Yoneda lemma|Yoneda]] is the equalizer diagram

$$
  Hom(F,G)
  \to
 \prod_i G(U_i) \stackrel{\to}{\to} \prod_{i, j} G(U_i \cap U_j)
$$

and hence identifies $Hom(F,G)$ indeed as the set of [[descent]] data for the [[sheaf]] condition on $G$. 

# Interpretation in terms of higher descent and codescent #


This description contains in it the seed of its generalization from the context of [[sheaf|sheaves]] to that of [[descent]] for [[infinity-stack]]s: 

for $Y := \coprod_i U_i$ a cover, there is a [[simplicial presheaf]] $ Y_\bullet $ that in degree $n$ is the $(n+1)$-fold [[fiber product]] $Y_n = Y^{[n+1]} = Y \times_X Y \times_X \cdots \times_X Y$.

This may be regarded as an [[infinity-groupoid]] valued presheaf.

More algebraically, with $\Pi(\Delta^n)$ the free [[strict omega-groupoid]] on the standard filtered $n$-[[simplex]], $Y_\bullet$ is the [[nerve]] of the groupoid

$$
  Codesc(Y) := \int^{[n] \in \Delta} O([n])\cdot Y^{[n+1]}
$$

The sieve associated with the cover is the presheaf obtained by starting with the $\infty$-prestack represented by $Codesc(Y)$ and decategorifying, i.e. passing to equivalence classes.

$$
  \bigcup_i hom(-,U_i)
  \simeq
  hom(-, Codesc(Y))/_\sim
  \,.
$$


Equivalently, for $A$ a [[presheaf]] regarded as a constant [[simplicial presheaf]] using the inclusion $const : $ [[Set]] $\hookrightarrow$ [[SSet]] we have

$$
  Hom_{SPSh}(Codesc(Y), A) \simeq Hom_{PSh}(Codesc(Y)/_\sim, A)
  \,,
$$

simply because all the higher morphism of $Codesc(Y)$ have to map to identity morphisms in $A$.