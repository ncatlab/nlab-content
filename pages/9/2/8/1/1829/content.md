<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* tic
{:toc}


# Idea #

An [[(∞,1)-sheaf]] -- often called a [[∞-stack]] -- is the 
[[(infinity,1)-category|(∞,1)-categorical]] analog of a [[sheaf]].
Just like a [[category of sheaves]] is a [[topos]], 
an [[(∞,1)-category of (∞,1)-sheaves]] is an 
[[(∞,1)-topos]].

There is good [[motivation for sheaves, cohomology and higher stacks]].

Here we recall basic definitions and then concentrate on 
[[model category|1-categorical models]] that 
[[presentable (infinity,1)-category|present]] $(\infty,1)$-categories
of $\infty$-stacks.

What we describe is effectively the old theory of the 
[[model structure on simplicial presheaves]] seen in the new light of
[[Higher Topos Theory]].


# Plan #

We proceed as follow.

* As a preparation, 

  * we recall 1-categorical [[presheaf|presheaves]]
  
  * and how a [[category of sheaves]] may equivalently be thought of as
    
    * a category [[geometric embedding|geometrically embedded]] into that of presheaves
 
    * or equivalently as the [[localization]] of presheaves at [[local isomorphisms]].

* Then in the main part, after recalling

  * the definition of [[(∞,1)-category]]
  
    * and the [[presentable (infinity,1)-category|presentation]] of
      $(\infty,1)$-categories by [[model category|1-categorical models]]

  we give

  * the general definition of [[(∞,1)-presheaves]];
  
    * and their [[presentable (infinity,1)-category|presentation]] by the [[global model structure on simplicial presheaves]]
      
  and finally
  
  * the definition of the [[(∞,1)-category of (∞,1)-sheaves]] by [[reflective (infinity,1)-subcategory|(∞,1)-geometric embedding]];    
  * and the [[model category|1-categorical model]] of this by [[Bousfield localization]] to the [[local model structure on simplicial presheaves]].
  


# Sheaf toposes #

It is helpful to briefly recall the story that we want to tell in the [[category theory]] context, because in the full [[higher category theory]] context it will be **literally the same** with all notions such as [[adjoint functor]], [[exact functor]] etc suitably regarded in the context of [[(∞,1)-functors]].

## Presheaves ##

Consider a [[category]] $C$ that we want to think as a category
of "test spaces". Classical choices would be $C = $ [[Top]], the
category of [[topological spaces]], $C = $ [[Diff]], the category
of smooth manifolds or $C = Op(X)$, the [[category of open subsets]]
of some [[topological space]] $X$.

Let [[Set]] be the category of sets. We write

$$
  PSh(C) := [C^{op}, Set] := Func(C^{op}, Set)
$$

for the category of [[presheaf|presheaves]] on $C$.
This is like a category of [[space and quantity|very general spaces]] modeled on $C$
as described at [[motivation for sheaves, cohomology and higher stacks]].


## Sheaves ##

In fact, this is a bit too general for most purposes: 
the objects of $PSh(C)$ may be very non-local in that they don't 
respect the way test objects in $C$ are supposed to glue together.
The full subcategory on those presheaves that do respect some
kind of gluing of test objects is the [[category of sheaves]].

+-- {: .un_defn}
###### Definition

A [[category of sheaves]] on $C$ is a category $Sh(C)$
equipped with a [[geometric embedding]] into $PSh(C)$

$$
  Sh(C) \stackrel{\leftarrow}{\to} PSh(C)
  \,.
$$


=--


Recall that this means that

* $Sh(C) \hookrightarrow PSh(C)$ is a [[full and faithful functor]];

* $\bar {(\cdot)} : PSh(C) \to Sh(C)$ is a [[exact functor|left exact]] [[left adjoint]].

in other words that

* $Sh(C) \hookrightarrow PSh(C)$ is the inclusion of a [[reflective subcategory]];

* with the special property that the [[left adjoint]] to the inclusion is [[exact functor|left exact]] (i.e. preserves finite [[limits]]).


In view of our models for $\infty$-sheaves it is of importance that
this implies an equivalence characterization


+-- {: .un_prop }
###### Proposition

The category $Sh(C)$ is equivalent to the full [[subcategory]] of 
$S$-[[local object|local]] presheaves, where $S$ is the set of [[local isomorphisms]].


=--



Another useful kind of [[geometric embeddings]] is that of the point: 

let
${*}$ be the category with a single morphism (the identity on a single object).
Then $PSh({*}) \simeq Sh({*}) \simeq Set $. Geometric embeddings

$$
  x : Sh({*}) \stackrel{\leftarrow}{\to} Sh(C)
$$

are called [[point of a topos|points]] of $Sh(C)$. We say that
$Sh(C)$ has _enough points_ if isomorphisms of sheaves can be tested on
points

$$
  (f : A \stackrel{\simeq}{\to} B)\in Sh(C) 
  \;\;
  \Leftrightarrow
  \;\;
  \forall x : (x^* f : x^* A \stackrel{\simeq}{\to} x^* B)
  \,.
$$ 

This is the situation we shall concentrate on here. 

* The topos $Sh(Diff)$ has enough points, one for every $n \in \mathbb{N}$.

* The topos $Sh(Op(X))$ has enough points: one for every ordinary point of $X$.

If $Sh(C)$ has enough points, we may characterize sheaves in yet another way, which is the one that directly suggests the  [[local model structure on simplicial presheaves]] discussed below:


+-- {: .un_prop }
###### Proposition

Let $S \subset Mor(PSh(C))$ be the set of _[[stalk]]wise isomorphisms_, i.e. those morphisms $f : A \to B$ of presheaves such that for all [[point of a topos|points]]
$x$ the morphism $x^* f : x^* A \to x^* B$ is
an [[isomorphism]] (of [[sets]]).

If $Sh(C)$ has [[point of a topos|enough points]], then $Sh(C)$ is equivalent to the full [[subcategory]] of $S$-local presheaves.

=--

The [[local model structure on simplicial presheaves]] that we are going to describe is obtained from this description of sheaves by 

* replacing [[sets]] by [[simplicial set]]

* replacing [[stalk]]wise [[isomorphism]] of sets by [[stalk]]wise [[model structure on simplicial sets|weak homotopy equivalences]] of simplicial sets.

So the model structures we shall encounter are plausible guesses. What is less trivial is that this plausible structure indeed [[presentable (infinity,1)-category|presents]] the fully general notion of [[(∞,1)-sheaf]]/[[∞-stack]].

This fully general notion we introduce now.



# $(\infty,1)$-categories and their presentation #

An ordinary [[locally small category]] is a 
[[enriched category|category enriched]] over the category [[Set]]
of [[sets]]. 

An [[(∞,0)-category]] is an [[∞-groupoid]]
which we think of as modeled by a [[simplicial set]] that 
is a [[Kan complex]].

Recall that there is a notion of 
[[nerve and realization]] 

$$
  N : SSet\text{-}Cat \stackrel{\leftarrow}{\to} SSet : |-|
$$

for [[SSet]]-[[enriched category|enriched categories]] 
induced by a [[simplicial object|cosimplicial]] [[simplicially enriched category]]

$$
 \Delta_{SSet-Cat} : \Delta \to SSet-Cat
$$

where the [[nerve]] operation $N$ is called the [[homotopy coherent nerve]]
of [[simplicially enriched category|simplicially enriched categories]].

+-- {: .un_defn}
###### Definition ($(\infty,1)$-category)

An [[(∞,1)-category]] is a 
[[enriched category|category enriched]] over $\infty$-groupoids,
i.e. an [[SSet]]-[[enriched category]] all whose [[hom-objects]] happen
to be [[Kan complexes]].


Given two $(\infty,1)$-categories $\mathbf{C}$ and $\mathbf{D}$
the [[(∞,1)-functor]] $(\infty,1)$-category is

$$
  Func(\mathbf{C}, \mathbf{D}) :=
  |SSet(N(\mathbf{C}), N(\mathbf{D}))|
  \,.
$$

This is indeed itself an $(\infty,1)$-category ([[Higher Topos Theory|HTT, prop 1.2.7.3]]).

The [[(∞,1)-category of (∞,1)-categories]] 
$(\infty,1)Cat$ is that whose 

* objects are $(\infty,1)$-categories;

* for $\mathbf{C}$ and $\mathbf{D}$ two $(\infty,1)$-categories the $\infty$-groupoid $(\infty,1)Cat(\mathbf{C}, \mathbf{D})$  is the maximal [[Kan complex]] inside the [[simplicial set]] of maps between the [[homotopy coherent nerves]]

  $$
    (\infty,1)Cat(\mathbf{C}, \mathbf{D})
    :=
    Core( SSet(N(\mathbf{C}), N(\mathbf{D})) )
    \,.
  $$ 

=--


**Examples**

* Using the [[monoidal category|monoidal]] embedding $const : Set \hookrightarrow \infty Grpdf \subset SSet$
  every ordinary category is an $(\infty,1)$-category.
  
* The $(\infty,1)$-category $\infty Grpd$ ([[∞Grpd]]) is the full [[SSet]-subcategory of [[SSet]]
  on [[Kan complexes]].
  

+-- {: .un_defn}
###### Definition (homotopy category)
 

The [[simplicial homotopy groups|simplicial connected components]] functor 

$$
  \pi_0 : SSet \to Set
$$

is strong monoidal and hence induces a functor

$$
  H : (\infty,1)Cat \to Cat
  \,.
$$

The image $H(\mathbf{C})$ of an $(\infty,1)$-category $\mathbf{C}$
with $H(\mathbf{C})(x,y) = \pi_0(\mathbf{C}(x,y))$
is the [[homotopy category of an (∞,1)-category]].

Two $(\infty,1)$-categories $\mathbf{C}$ and $\mathbf{D}$ are
**equivalent** if they are isomorphic in $H((\infty,1)Cat)$

$$
  (f : \mathbf{C} \to \mathbf{D} \;is equivalence)
  \;\;
  \Leftrightarrow
  \;\;
  (H_{(\infty,1)Cat}(f) : \mathbf{C} \to \mathbf{D}
  \;
  is isomorphism)
  \,.
$$

=--


## Presentations ##

It is often convenient to [[presentable (infinity,1)-category|present]]
$(\infty,1)$-categories by 1-categorical [[model category|models]].


+-- {: .un_defn}
###### Definition ($(\infty,1)$-category presented by a model category)

For $\mathbf{A}$ a [[combinatorial simplicial model category]],
the $(\infty,1)$-category [[presentable (infinity,1)-category|presented]]
by it is the full 
subcategory $\mathbf{A}^\circ \subset \mathbf{A}$ on objects that
are both cofibrant and fibrant.

=--


**Remark** The axioms of a simplicial model category
ensure that the [[hom-object|hom-simplicial sets]] of 
$\mathbf{A}^\circ$ are indeed [[Kan complexes]].
(for instance [[Higher Topos Theory|HTT, remark 3.1.8]]).


+-- {: .un_prop }
###### Proposition ([[Higher Topos Theory|HTT, remark A.3.7.7]])


Let $\mathbf{A}$ and $\mathbf{B}$ be 
[[combinatorial simplicial model category|combinatorial simplicial model categories]].
Then the corresponding $(\infty,1)$-categories $\mathbf{A}^\circ$ and 
$\mathbf{B}^\circ$ are equivalent precisely if there is a sequence of
[[SSet]]-[[enriched functor|enriched]] [[Quillen equivalences]] 
$$
  \mathbf{A}
  \stackrel{\leftarrow}{\to}
  \stackrel{\to}{\leftarrow}
  \stackrel{\leftarrow}{\to}
  \cdots
  \mathbf{B}
  \,.
$$

=--


# $(\infty,1)$-Sheaf $(\infty,1)$-toposes #

There is now an obvious definition of $(\infty,1)$-categories of $(\infty,1)$-presheaves and 
of $(\infty,1)$-sheaves by interpreting the 1-categorical story in the $(\infty,1)$-categorical context.


## $(\infty,1)$-Presheaves ##

Now we generalize the above from sheaves to 
[[(∞,1)-sheaves]] also known as 
[[∞-stacks]].



+-- {: .un_defn}
###### Definition ($(\infty,1)$-presheaves)


The $(\infty,1)$-category of [[(∞,1)-presheaves]]
on $C$ is

$$
  PSh_\infty(C) := [C^{op}, \infty Grpd] = 
  Func( C^{op}, \infty Grpd )
  \,.
$$

=--


+-- {: .un_prop}
###### Proposition (models for $(\infty,1)$-presheaves) ([[Higher Topos Theory|HTT, prop. 4.2.4.4]],
see also
[[Higher Topos Theory|HTT, prop. 5.1.1.1]])

The $(\infty,1)$-category 
presented by the
[[global model structure on simplicial presheaves]]
$SPSh(C)_{proj}$
on $C$ 
(either the projective or the injective one)
is equivalent to that of $(\infty,1)$-presheaves on $C$:
$$
 (SPSh(C)_{proj})^{\circ}
 \simeq
 (SPSh(C)_{inj})^{\circ}
 \simeq
 PSh_\infty(C)
 \,.
$$

=--


## $(\infty,1)$-sheaves ##

There are $(\infty,1)$-category analogs of all the familiar
notions from [[category theory]], in particular

* [[adjoint functor]]

* [[exact functor]] (preserving finite [[limits]]).

Using this we obtain a definition of [[geometric embedding]]
of $(\infty,1)$-toposes , i.e. left exaxt 
[[reflective (∞,1)-subcategories]]
by literally copying the 1-categorical definition.

+-- {: .un_defn}
###### Definition ($(\infty,1)$-sheaves) ([[Higher Topos Theory|HTT, def. 6.1.0.4]])

An [[(∞,1)-category of (∞,1)-sheaves]] is a [[geometric embedding]]
into an [[(∞,1)-category of (∞,1)-presheaves]]

$$
  Sh_\infty(C) \stackrel{\leftarrow}{\to} PSh_\infty(C)
  \,.
$$

=--

+-- {: .num_lemma }
###### Proposition (models for reflective $(\infty,1)$-subcategories)



Let 
the [[combinatorial simplicial model category]] $\mathbf{B}$ 
be a left [[Bousfield localization]] of 
the
[[combinatorial simplicial model category]]
$\mathbf{A}$
then 

$$
  \mathbf{B}^\circ \stackrel{\leftarrow}{\to}
  \mathbf{A}^\circ
$$

is the inclusion of a [[reflective (∞,1)-subcategory]].

=--

+-- {: .proof}
###### Proof


By [[Higher Topos Theory|HTT, prop A.3.7.4]] every
combinatorial simplicial left  [[Bousfield localization]]
is given by a set $S$ of cofibrations such that 

* the fibrant objects of $\mathbf{B}$ are
  precisely the fibrant objects in $\mathbf{A}$
  that are $S$-[[local object]];

* the weak equivalences of $\mathbf{B}$ 
  are the $S$-local morphisms in $\mathbf{A}$.


Accordingly $\mathbf{B}^\circ$ is the full $\infty Grpd$-enriched 
subcategory of $\mathbf{A}^\circ$ on $S$-[[local objects]].
(see also [[Higher Topos Theory|HTT, prop 6.5.2.14]]).

By [[Higher Topos Theory|HTT, prop. 5.5.4.15]] this means that
$\mathbf{B}$ is a [[reflective (∞,1)-subcategory]] of $\mathbf{A}$.

=--


**Remark**
Notice that this does not yet say that the localization is 
_left exact_ .

But this makes at least plausible that 
the [[local model structure on simplicial presheaves]] is a 
[[presentable (infinity,1)-category|presentation]] for an
[[(∞,1)-category of (∞,1)-sheaves]]. 

That this is indeed the case is 

+-- {: .num_lemma #SizeOfLeftCoset}
###### Proposition (model for hypercomplete $(\infty,1)$-sheaves) ([[Higher Topos Theory|HTT, prop. 6.5.2.14]])


The [[local model structure on simplicial presheaves]]
$SSh(C)^{l loc}_{proj}$ presents the [[hypercompletion|hypercompleted version]]
of the [[(∞,1)-category of (∞,1)-sheaves]] 
$Sh^{hc}(C)$ on $C$.

$$
  (SPSh(C)_{proj}^{loc})^\circ
  \simeq
  Sh^{hc}(C)
  \,.
$$

=--


**Remark** See the discussion at [[Cech cohomology]] for 
the  role of [[hypercompletion]].


# Applications #

## Abelian sheaf cohomology as special case of $\infty$-stackification ## 

The [[nerve]] operation of the [[Dold-Kan correspondence]]

$$
  N : Ch_+ \to SimpAb \subset \infty Grpd
$$

embeds [[sheaf|sheaves]] with values in non-negatively graded [[chain complex]]es
of abelian groups
into simplicial sheaves as those simplicial sheaves with values in
[[Kan complex]]es that carry a struict abelian group structure.
This way [[homological algebra]] and [[abelian sheaf cohomology]]
are realized as special cases of models for $\infty$-stacks:
a complex of abelian sheaves presents a stably abelian $\infty$-stack.

+-- {: .un_prop}
###### Proposition

Under the [[Dold-Kan correspondence]] [[abelian sheaf cohomology]]
identifies with the [[hom-set]] of the 
[[homotopy category of an (infinity,1)-category|homotopy category]] corresponding 
[[infinity-stack]] [[(infinity,1)-topos]].

More precisely, let 

* the underlying [[site]] be the [[category of open subsets]]  $C = Op(X)$
  of a [[topological space]] $X$,
 
* let $A \in Sh(X)$ be a sheaf with values in abelian groups on $X$;

* let $\mathbf{B}^n A \in Sh(X,SSet)$ be the image of the 
  complex of sheaves $A[-n]$ concentrated in degree $n$ under the
  [[Dold-Kan correspondence|Dold-Kan]] [[nerve]];
  
* write $X \in Sh(X)$ for the [[terminal object]] sheaf in $Sh(X)$ (the sheaf constant
  on the singleton set).
  
Then degree $n$ [[abelian sheaf cohomology]] of $X$ with coefficients in $A$ is 
homotopy classes of maps from $X$ to $\mathbf{B}^n A$:

$$
  H^n(X,A) \simeq Ho_{SSh(X)}(X, \mathbf{B}^n A)
  \,.
$$
=--

+-- {: .proof}
###### Proof

The original proof was given in [[BrownAHT]] in terms of the [[category of fibrant objects]] structure on locally Kan simplicial sheaves. 

The analogous arguments in terms of the full injective model structure were  given by Jardine. See section 6 of his [lecture notes](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf).
=--


[[!redirects models for infinity-stack (infinity,1)-topoi]]
[[!redirects models for ∞-stack (∞,1)-toposes]]
[[!redirects models for ∞-stack (∞,1)-topoi]]