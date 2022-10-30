
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


# Pointed objects
* table of contents
{: toc}

## Idea

In a [[category]] $C$ with a [[terminal object]] $1$, a **pointed object** is an [[object]] $X$ equipped with a [[global element]] $1\to X$, often called its __basepoint__.

A pointed object is distinguished from an [[inhabited set|inhabited]] one in that the chosen point is _structure_ rather than a property.  In particular, a morphism of pointed objects is a morphism in the original category which preserves the points.  In other words, the category of pointed objects in $C$ is the [[under category|co-slice category]] $1/C$ under the terminal object.

There is an obvious [[forgetful functor]] from $1/C$ to $C$.  If $C$ has [[finite colimit|finite]] [[coproducts]], this functor has a [[left adjoint|left]] [[adjoint functor]] which takes an object $X$ to the coproduct $1\sqcup X$, equipped with its obvious point (this functor underlies the "[[maybe monad]]").  This is often written $X_+$ and called "$X$ with a disjoint basepoint adjoined." A pointed object is equivalently a [[module over a monad]] of this monad.

## Definition

+-- {: .num_defn #SliceCategory}
###### Definition

Let $\mathcal{C}$ be a [[category]] and let $X \in \mathcal{C}$ be an [[object]]. 

The _[[slice category]]_ $\mathcal{C}_{/X}$ is the category whose 

* objects are morphisms $\array{A \\ \downarrow \\ X}$ in $\mathcal{C}$;

* morphisms are [[commuting diagram|commuting triangles]] $\array{ A && \longrightarrow && B \\ & {}_{}\searrow && \swarrow \\ && X}$ in $\mathcal{C}$.

Dually, the _[[coslice category]]_ $\mathcal{C}^{X/}$ is the category whose

* objects are morphisms $\array{X \\ \downarrow \\ A}$ in $\mathcal{C}$;

* morphisms are [[commuting diagram|commuting triangles]] $\array{ && X \\ & \swarrow && \searrow \\ A && \longrightarrow && B }$ in $\mathcal{C}$.

There is the canonical [[forgetful functor]]

$$
  U \;\colon \; \mathcal{C}_{/X}, \mathcal{C}^{X/} \longrightarrow \mathcal{C}
$$

given by forgetting the morphisms to/from $X$.

=--

We here focus on this class of examples:

+-- {: .num_defn #CategoryOfPointedObjects}
###### Definition

For $\mathcal{C}$ a [[category]] with [[terminal object]] $\ast$, the [[coslice category]] (def. \ref{SliceCategory}) $\mathcal{C}^{\ast/}$ is the corresponding _[[category of pointed objects]]_: its

* objects are morphisms in $\mathcal{C}$ of the form $\ast \overset{x}{\to} X$ (hence an object $X$ equipped with a choice of point; i.e. a _[[pointed object]]_);

* morphisms are [[commuting diagram|commuting triangles]] of the form

  $$
    \array{
       && \ast
       \\
       & {}^{\mathllap{x}}\swarrow && \searrow^{\mathrlap{y}}
       \\
       X && \overset{f}{\longrightarrow} && Y
    }
  $$

  (hence morphisms in $\mathcal{C}$ which preserve the chosen points).

=--

## Examples

* The basic example are [[pointed sets]].

* [[natural numbers object]]s, [[monoid object]]s, and [[group object]]s in a category are pointed objects. 

* [[pointed topological spaces]] and [[pointed simplicial sets]] are important in [[homotopy theory]] (where they are often called **based**) for instance for the discussion of [[homotopy fibers]], [[loop space objects]] etc. See also at _[[classical model structure on pointed topological spaces]]_, which makes them be models for [[pointed homotopy types]].

* Pointed $n$-[[n-categories]] figure prominently in the [[delooping hypothesis]]; see also [[k-tuply monoidal n-category]].  In particular, a fancy name for a pointed set is a _0-tuply monoidal 0-category_.

## Properties


### Forgetting and adjoining basepoints

+-- {: .num_defn #BasePointAdjoined}
###### Definition

Let $\mathcal{C}$ be a [[category]] with [[terminal object]] and [[finite colimits]]. Then the [[forgetful functor]] $\mathcal{C}^{\ast/} \to \mathcal{C}$ from its [[category of pointed objects]], def. \ref{CategoryOfPointedObjects}, has a [[left adjoint]] given by forming the [[disjoint union]] ([[coproduct]]) with a base point ("adjoining a base point"), this is denoted by

$$
  (-)_+ \coloneqq (-) \sqcup \ast \;\colon \; \mathcal{C} \longrightarrow \mathcal{C}^{\ast/}
  \,.
$$

=--

### Zero object and pointed category structure

+-- {: .num_remark #PointedObjectsHaveZeroObject}
###### Remark

In a [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, the [[terminal object]] coincides with the [[initial object]], both are given by $\ast \in \mathcal{C}$ itself, pointed in the unique way. 

In this situation one says that $\ast$ is a _[[zero object]]_ and that $\mathcal{C}^{\ast/}$ is a _[[pointed category]]_. 

It follows that also all [[hom-sets]] $\mathcal{C}^{\ast/}(X,Y)$ of $\mathcal{C}^{\ast/}$ are canonically [[pointed sets]], pointed by the _[[zero morphism]]_

$$
  0 
    \;\colon\;
  X \overset{\exists!}{\longrightarrow} 0 \overset{\exists}{\longrightarrow} Y
  \,.
$$

=--

Conversely, if $\mathcal{C}$ has a [[zero object]], then every object is automatically pointed in a unique way, so that $\mathcal{C}$ is equivalent to its category of pointed objects.



### Limits and colimits

+-- {: .num_prop #LimitsAndColimitsOfPointedObjects}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with all [[limits]] and [[colimits]]. Then also the [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, has all limits and colimits.

Moreover:

1. the limits are the limits of the underlying diagrams in $\mathcal{C}$, with the base point of the limit induced by its universal property in $\mathcal{C}$;

1. the colimits are the limits in $\mathcal{C}$ of the diagrams _with the basepoint adjoined_.

=--

+-- {: .proof}
###### Proof

It is immediate to check the relevant [[universal property]]. For details see at _[slice category -- limits and colimits](overcategory#LimitsAndColimits)_.

=--


### Wedge sum and Smash product
 {#WedgeSumAndSmashProduct}

+-- {: .num_example #WedgeSumAsCoproduct}
###### Example

Given two pointed objects $(X,x)$ and $(Y,y)$, then:

1. their [[product]] in $\mathcal{C}^{\ast/}$ is simply $(X\times Y, (x,y))$;

1. their [[coproduct]] in $\mathcal{C}^{\ast/}$ has to be computed using the second clause in prop. \ref{LimitsAndColimitsOfPointedObjects}: since the point $\ast$ has to be adjoined to the diagram, it is given not by the coproduct in $\mathcal{C}$, but by the [[pushout]] in $\mathcal{C}$ of the form:

   $$
     \array{
       \ast &\overset{x}{\longrightarrow}& X
       \\
       {}^{\mathllap{y}}\downarrow &(po)& \downarrow
       \\
       Y &\longrightarrow& X \vee Y
     }
     \,.
   $$

   This is called the _[[wedge sum]]_ operation on pointed objects.

Generally for a set $\{X_i\}_{i \in I}$ in $\mathcal{C}^{\ast/}$

1. their [[product]] is formed in $Top$, with the new basepoint canonically induced;

1. their [[coproduct]] is formed by the [[colimit]] in $Top$ over the diagram with a basepoint adjoined, and is called the [[wedge sum]] $\vee_{i \in I} X_i$.

=--


+-- {: .num_example}
###### Example

For $X$ a [[CW-complex]],  then for every $n \in \mathbb{N}$ the [[quotient]] of its $n$-skeleton by its $(n-1)$-skeleton is the [[wedge sum]], def. \ref{WedgeSumAsCoproduct}, of $n$-spheres, one for each $n$-cell of $X$:

$$
  X^n / X^{n-1} \simeq \underset{i \in I_n}{\vee} S^n
  \,.
$$

=--


+-- {: .num_defn #SmashProductOfPointedObjects}
###### Definition

For $\mathcal{C}^{\ast/}$ a [[category of pointed objects]] with [[finite limits]] and [[finite colimits]], the _[[smash product]]_ is the [[functor]]

$$
  (-)\wedge(-)
  \;\colon\;
  \mathcal{C}^{\ast/}
  \times 
  \mathcal{C}^{\ast/}
  \longrightarrow
  \mathcal{C}^{\ast/}
$$

given by

$$
  X \wedge Y
  \;\coloneqq\;
  \ast
  \underset{X\sqcup Y}{\sqcup} (X \times Y)
  \,,
$$

hence by the [[pushout]] in $\mathcal{C}$

$$
  \array{
    X \sqcup Y &\overset{(id_X,y),(x,id_Y) }{\longrightarrow}& X \times Y
    \\
    \downarrow && \downarrow
    \\
    \ast &\longrightarrow& X \wedge Y
  }
  \,.
$$

In terms of the [[wedge sum]] from def. \ref{WedgeSumAsCoproduct}, this may be written concisely as

$$
  X \wedge Y = \frac{X\times Y}{X \vee Y}
  \,.
$$
 
=--

These two operations are ubiquituous in [[stable homotopy theory]]:

| symbol | name | category theory |
|--------|------|-----------------|
| $X \vee Y$ | [[wedge sum]] | [[coproduct]] in $\mathcal{C}^{\ast/}$ |
| $X \wedge Y$ | [[smash product]] | [[tensor product]] in $\mathcal{C}^{\ast/}$|

+-- {: .num_example #WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces}
###### Example

For $X, Y \in Top$, with $X_+,Y_+ \in Top^{\ast/}$, def. \ref{BasePointAdjoined}, then

* $X_+ \vee Y_+ \simeq (X \sqcup Y)_+$;

* $X_+ \wedge Y_+ \simeq (X \times Y)_+$. 

=--

+-- {: .proof}
###### Proof

By example \ref{WedgeSumAsCoproduct}, $X_+ \vee Y_+$ is given by the colimit in $Top$ over the diagram

$$
  \array{
    && && \ast
    \\
    && & \swarrow && \searrow
    \\
    X &\,\,& \ast && && \ast &\,\,& Y
  }  
  \,.
$$

This is clearly $A \sqcup \ast \sqcup B$. Then, by definition \ref{SmashProductOfPointedObjects}

$$
  \begin{aligned}
    X_+ \wedge Y_+
    & \simeq
    \frac{(X \sqcup \ast) \times (X \sqcup \ast)}{(X\sqcup \ast) \vee (Y \sqcup \ast)}
    \\
    & \simeq 
    \frac{X \times Y \sqcup X \sqcup Y \sqcup \ast}{X \sqcup Y \sqcup \ast}
    \\
    & \simeq
    X \times Y \sqcup \ast
    \,.
  \end{aligned} 
$$

=--

+-- {: .num_example #StandardReducedCyclinderInTop}
###### Example

Let $\mathcal{C}^{\ast/} = Top^{\ast/}$ be [[pointed topological spaces]]. Then 

$$
  I_+ \in Top^{\ast/}
$$

denotes the standard interval object $I = [0,1]$, with a disjoint basepoint adjoined, def. \ref{BasePointAdjoined}. Now for $X$ any [[pointed topological space]], then 

$$
  X \wedge (I_+) = (X \times I)/(\{x_0\} \times I)
$$

is the **[[reduced cylinder]]** over $X$: the result of forming the ordinary cyclinder over $X$, and then identifying the interval over the basepoint of $X$ with the point.

(Generally, any construction in $\mathcal{C}$ properly adapted to pointed objects $\mathcal{C}^{\ast/}$ is called the "reduced" version of the unpointed construction. Notably so for "[[reduced suspension]]" which we come to [below](#MappingCones).)


Just like the ordinary cylinder $X\times I$ receives a canonical injection from the [[coproduct]] $X \sqcup X$ formed in $Top$, so the reduced cyclinder receives a canonical injection from the coproduct $X \sqcup X$ formed in $Top^{\ast/}$, which is the [[wedge sum]] from example \ref{WedgeSumAsCoproduct}:

$$
  X \vee X \longrightarrow X \wedge (I_+)
  \,.
$$

=--

### Fibers and cofibers -- kernels and cokernels


+-- {: .num_defn #FiberAndCofiberInPointedObjects}
###### Definition

Given a morphism $f \colon X \longrightarrow Y$ in a [[category of pointed objects]] $\mathcal{C}^{\ast/}$, def. \ref{CategoryOfPointedObjects}, with finite limits and colimits,

1. its **[[fiber]]** or **[[kernel]]** is the [[pullback]] of the point inclusion

   $$
     \array{
       fib(f) &\longrightarrow& X
       \\
       \downarrow &(pb)& \downarrow^{\mathrlap{f}}
       \\
       \ast &\longrightarrow& Y
     }
   $$

1. its **[[cofiber]]** or **[[cokernel]]** is the [[pushout]] of the point projection

   $$
     \array{
       X &\overset{f}{\longrightarrow}& Y
       \\
       \downarrow &(po)& \downarrow
       \\
       \ast &\longrightarrow& cofib(f)
     }
     \,.
   $$

=--

+-- {: .num_remark }
###### Remark

In the situation of def. \ref{FiberAndCofiberInPointedObjects}, both the pullback as well as the pushout are equivalently computed in $\mathcal{C}$. For the pullback this is the first clause of prop. \ref{LimitsAndColimitsOfPointedObjects}. The second clause says that for computing the pushout in $\mathcal{C}$, first the point is to be adjoined to the diagram, and then the colimit over the larger diagram

$$
  \array{
    \ast
    \\
    & \searrow
    \\
    & & X &\overset{f}{\longrightarrow}& Y
    \\
    & & \downarrow && 
    \\
    & & \ast && 
   }
$$

be computed. But one readily checks that in this special case this does not affect the result. (The technical jargon is that the inclusion of the smaller diagram into the larger one in this case happens to be a [[final functor]].)

=--




### Closed and monoidal structure
 {#ClosedMonoidalStructure}

+-- {: .num_defn #PointedMappingSpace}
###### Definition

Let $\mathcal{C}$ be a [[closed monoidal category]] with [[finite limits]].

For $X, Y \in \mathcal{C}^{\ast}$ two pointed objects in $\mathcal{C}$, their **[[pointed mapping space]]** 

$$
  [X,Y]_*
  \in
  \mathcal{C}^{\ast/}
$$

(the "object of basepoint-preserving maps"), is the [[pullback]]

$$
  \array{ 
    [X,Y]_* & \overset{}{\longrightarrow} & \ast
    \\
    \downarrow &(pb)& \downarrow
    \\
    [X,Y] & \underset{}{\longrightarrow} & [1,Y]
   }
$$

where the morphism $[X,Y]\to [1,Y]$ is induced from the point $\ast\to X$, and the morphism $\ast\to [\ast,Y]$ is the [[adjunct]] to $\ast \otimes \ast \to \ast \to Y$.  

Regard $[X,Y]_*$ as a pointed object with basepoint induced by the map $\ast\to [X,Y]$ whose [[adjunct]] is $\ast \otimes X \to \ast \to Y$.  

=--

+-- {: .num_prop #SmashProductLeftAdjointToPointedMappingSpace}
###### Proposition

Let $\mathcal{C}$ be a [[closed monoidal category]] with [[finite limits]] and with [[finite colimits]].

For every pointed object $X \in \mathcal{C}^{\ast}$ the operation of forming the pointed [[mapping space]] out of $X$, def. \ref{PointedMappingSpace}, and the operation of forming the [[smash product]] with $X$, def. \ref{SmashProductOfPointedObjects} form a pair of [[adjoint functors]]

$$
  (
  X \wedge (-)
  \;\dashv\;
  [X,-]_\ast
  )
  \;\colon\;
  \mathcal{C}^{\ast/}
  \leftrightarrow
  \mathcal{C}^{\ast/}
  \,.
$$

This makes $\mathcal{C}^{\ast/}$ itself a [[closed monoidal category]], which is [[symmetric monoidal category|symmetric]] if $\mathcal{C}$ is.  The [[tensor unit]] is $I_+$ (def. \ref{BasePointAdjoined}) for $I$ the unit for the monoidal structure on $\mathcal{C}$.  

=--

([Elmendorf-Mandell 07, lemma 4.20](#ElmendorfMandell07))

+-- {: .num_remark}
###### Remark

The case when $\mathcal{C}$ is [[cartesian monoidal category|cartesian]], or at least [[semicartesian monoidal category|semicartesian]], is most common in the literature.

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is [[monoidal category|monoidal]] but not [[closed monoidal category|closed]], the same definition \ref{SmashProductOfPointedObjects} of the [[smash product]] makes $\mathcal{C}^{\ast/}$ [[monoidal category|monoidal]] as long as the tensor product of $\mathcal{C}$ preserves finite colimits in each variable separately.  

If not, the smash product can fail to be associative. For instance, the smash product on the ordinary category [[Top]] (without any [[nice category of spaces|niceness conditions]] imposed) is not associative.

=--


For [[base change]] functoriality of these structures see at _[Wirthm&#252;ller context -- Examples -- On pointed objects](Wirthm&#252;ller+context#PointedObjects)_.

### Monadicity
 {#Monadicity}

Pointed objects are the [[algebras over a monad]] of the [[monad]] $X \mapsto X \coprod \ast$ (the "[[maybe monad]]"). (Already the unit axiom of the monad makes its algebras be pointed objects, the action axiom does not add any further condition in this case.)

Notice that if sufficient [[colimits]] exist in the first place, then this functor is trivially an [[accessible functor]], hence an [[accessible monad]]. This makes categories of pointed objects inherit good properties from the ambient category, see at _[accessible monad -- Categories of algebras](accessible+monad#CategoryOfAlgebras)_.

### Classifying topos

The [[classifying topos]] for pointed object is the [[presheaf topos]] $PSh((FinSet_\ast)^{op})$ on the [[opposite category]] of pointed [[finite sets]]. See at _[[classifying topos for the theory of objects]]_ for more on this.

### Model category structure
 {#ModelCategoryStructure}

+-- {: .num_prop #ModelStructureOnSliceCategory}
###### Proposition
**([[model structure on pointed objects]])**

Let $\mathcal{C}$ be a [[model category]] and let $X \in \mathcal{C}$ be an [[object]]. Then both the [[slice category]] $\mathcal{C}_{/X}$ as well as the [[coslice category]] $\mathcal{C}^{X/}$, def. \ref{SliceCategory}, carry model structures themselves -- the **[[model structure on a slice category|model structure on a (co-)slice category]]**,  where a morphism is a weak equivalence, fibration or cofibration iff its image under the [[forgetful functor]] $U$ is so in $\mathcal{C}$.

In particular the category $\mathcal{C}^{\ast/}$ of [[pointed objects]], def. \ref{CategoryOfPointedObjects}, in a model category $\mathcal{C}$ becomes itself a model category this way.

=--

+-- {: .proof}
###### Proof

The model strcuture as claimed is immediate by inspection.

=--


+-- {: .num_example #ClassicalPointedHomotopyCategory}
###### Example

For $\mathcal{C} = Top_{Quillen}$, the [[classical model structure on topological spaces]], then the model structure on [[pointed topological spaces]] induced via prop. \ref{ModelStructureOnSliceCategory} we call the _[[classical model structure on pointed topological spaces]]_ $Top_{Quillen}^{\ast/}$. Its [[homotopy category of a model category]] is the _classical pointed homotopy theory_ $Ho(Top^{\ast/})$.

=--

+-- {: .num_example #NonDegenerateBasepointAsCofibrantObjects}
###### Example

The fibrant objects in the pointed model structure $\mathcal{C}^{\ast/}$, prop. \ref{ModelStructureOnSliceCategory}, are those that are fibrant as objects of $\mathcal{C}$.

But the cofibrant objects in $\mathcal{C}^{\ast}$ are now those for which the basepoint inclusion is a cofibration in $X$.

For $\mathcal{C}^{\ast/} = Top^{\ast/}$, then the corresponding cofibrant pointed topological spaces are tyically referred to as spaces _with non-degenerate basepoints_. Notice that the point itself is cofibrant in $Top_{Quillen}$, so that cofibrant pointed topological spaces are in particular cofibrant topological spaces.

=--


+-- {: .num_example #HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets}
###### Example

For $\mathcal{C}$ any [[model category]], with $\mathcal{C}^{\ast/}$ its [[slice model structure|pointed model structure]] according to prop. \ref{ModelStructureOnSliceCategory}, then the corresponding [[homotopy category of a model category|homotopy category]] is, by remark \ref{PointedObjectsHaveZeroObject}, canonically [[enriched category|enriched]] in [[pointed sets]], in that its [[hom-functor]] is of the form

$$
  [-,-]_\ast
  \;\colon\;
  Ho(\mathcal{C}^{\ast/})^\op
  \times
  Ho(\mathcal{C}^{\ast/})
  \longrightarrow
  Set^{\ast/}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is a [[monoidal model category]] with cofibrant [[tensor unit]], then the pointed model structure on  $\mathcal{C}^{\ast/}$ (prop. \ref{ModelStructureOnSliceCategory}) is also a [[monoidal model category]], and the [[smash product]]$\dashv$[[mapping space]] adjunction of prop. \ref{SmashProductLeftAdjointToPointedMappingSpace} is a [[Quillen adjunction]]

$$
  (
  X \wedge (-)
  \;\dashv\;
  (-)^X
  )
  \;\colon\;
  \mathcal{C}^{\ast/}
  \leftrightarrow
  \mathcal{C}^{\ast/}
  \,.
$$

=--


## Related concepts

* [[bi-pointed object]]

* [[pointed type]]

* [[smash product]]

* [[topos of pointed objects]]

* [[fibration of points]]

* [[model structure on pointed objects]]

## References

* [[Francis Borceux]], [[Dominique Bourn]], _Mal'cev, Protomodular, Homological and Semi-Abelian Categories_ , Kluwer Dordrecht 2004.

* [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories, multicategories, and algebraic K-theory_, Algebraic & Geometric Topology **9** (2009) 2391-2441. ([arXiv:0710.0082](http://arxiv.org/abs/0710.0082))
 {#ElmendorfMandell07}

[[!redirects pointed object]]
[[!redirects pointed objects]]

[[!redirects base point]]
[[!redirects base points]]
[[!redirects basepoint]]
[[!redirects basepoints]]

[[!redirects category of pointed objects]]
[[!redirects categories of pointed objects]]