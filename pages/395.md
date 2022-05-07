
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#

* table of contents
{: toc}

## Idea

A _category of fibrant objects_ is a [[category with weak equivalences]] equipped with extra structure somewhat weaker than that of a [[model category]]. 

The extra structure of fibrations _and_ cofibrations in a [[model category]] is, while convenient if it exists, not carried by many [[categories with weak equivalences]] which nevertheless admit many constructions in [[homotopy theory]]. Even if they do, sometimes the cofibrations are intractable in practice.

A _category of fibrant objects_ is essentially like a [[model category]] but with all axioms concerning the cofibrations dropped, the concept of fibrations retained ("[[fibration category]]") and assuming that all objects are fibrant (whence the name). It turns out that this is sufficient for many useful constructions. In particular, it is sufficient for giving a convenient construction of the [[homotopy category]] in terms of [[span]]s of length one. This makes categories of fibrant objects useful in [[homotopical cohomology theory]].

## Definition

+-- {: .num_defn}
###### Definition

A **category of fibrant objects** $\mathbf{C}$ is 

* a [[category with weak equivalences]], i.e equipped with a subcategory
  $$
    Core(\mathbf{C}) \hookrightarrow W \hookrightarrow C
  $$
  where $f \in Mor(W)$ is called a **weak equivalence**;

* equipped with a further subcategory 
  $$
    Core(\mathbf{C}) \hookrightarrow F \hookrightarrow C
    \,,
  $$
  where $f \in Mor(F)$ is called a **fibration**

  Those morphisms which are both weak equivalences and fibrations are called **acyclic fibrations** .

This data has to satisfy the following properties:

* $C$ has [[finite products]], and in particular a [[terminal object]] ${*}$;

* the [[pullback]] of a fibration along an arbitrary morphism exists, and is again a fibration;

* acyclic fibrations are preserved under [[pullback]];

* weak equivalences satisfy [[category with weak equivalences|2-out-of-3]]

* for every object there exists a [[path object]]

  * this means: for every object $B$ there exists at least one object denoted $B^I$ (not necessarily but possibly the [[internal hom]] with an [[interval object]]) that fits into a diagram
  $$
    (B \stackrel{Id \times Id}{\to} B \times B)
    =
    (B \stackrel{\sigma}{\to} B^I \stackrel{d_0 \times d_1}{\to} B \times B)
  $$
  where $\sigma$ is a weak equivalence and $d_0 \times d_1$ is a fibration;

* all objects are _fibrant_, i.e. all morphisms $B \to {*}$ to the terminal object are fibrations.

=--



## Examples

### Full subcategories of model categories 
 {#FullSubcategoriesOfModelCategories}


The tautological example is the [[full subcategory]] of any [[model category]] on all objects which are fibrant. 

### Right proper model categories
 {#RightProperModelCategories}

Let $M$ be a [[right proper model category]], let $W$ be the class of weak equivalences, and let $F_+$ be the class of morphisms $f$ in $M$ such that any [[pullback]] of $f$ in $M$ is also a [[homotopy pullback]]. Then $M$ together with $W$ and $F_+$ satisfy all the conditions to be a category of fibrant objects _except_ possibly the condition that every morphism $X \to {*}$ in $M$ is in $F_+$; so if we restrict to the [[full subcategory]] of those objects $X$ in $M$ such that $X \to {*}$ is in $F_+$, then we do get a category of fibrant objects.

For example, [[sSet]] via its [[model structure on simplicial sets|standard model structure]] is a category of fibrant objects in this way. The fibrations in this case are not the [[Kan fibrations]] (these also yields a category-of-fibrant-objects structure, via [the above](#FullSubcategoriesOfModelCategories), but a different one) but are the [[sharp maps]].


### $\infty$-Groupoids ##

This includes notably all models for categories of [[infinity-groupoid]]s:

  * the category of [[Kan complex]]es (a full [[subcategory]] of [[SSet]])

  * the category of [[strict omega-groupoid]]s using the [[model structure on strict omega-groupoids]]

+-- {: .num_prop}
###### Proposition

[[nLab:Kan complex|Kan complexes]] form a [[nLab:category of fibrant objects|Brown category of fibrant objects]].

=--

+-- {: .proof}
###### Proof

The [[path object]] of any $X$ can be chosen to be the [[nLab:internal hom|internal hom]]

$$
  X^I = [\Delta^1, X]
$$

in with respect to the [[closed monoidal structure on presheaves|closed monoidal structure on]] [[SSet]] with the simplicial 1-[[simplex]] $\Delta^1$.

The morphism $X \to X^I$ is given by the [[simplex category|degeneracy map]] $\sigma_0 : \Delta^0 \to \Delta^1$ as
$$
  X \stackrel{\simeq}{\to}
  [\Delta^0, X]
  \stackrel{[\sigma_0, X]}{\to}
  [\Delta^1, X]
  \,.
$$
This is indeed a weak equivalence, since by the [[simplicial identities]] it is a [[section]] (a [[inverse|right inverse]]) for the morphism
$$
  [\Delta^1, X] \stackrel{[\delta_0,X]}{\to}
  [\Delta^0, X]
  \,.
$$
This map, one checks, has the 
[[weak factorization system|right lifting property]] 
with respect to all [[boundary of a simplex]]-inclusions
$\partial \Delta^n \to \Delta^n$. By a lemma discussed
at [[Kan fibration]] this means that $[\delta_0,X]$
is an acyclic fibration. Hence $[\sigma_0, X]$, being
its right [[inverse]], is a weak equivalence.

The remaining morphism of the [[path object|path space object]] $X^I \to X \times X$ is
$$
  [\Delta^1, X]
  \stackrel{[\delta_0 \sqcup \delta_1, X]}{\to}
  [\Delta^0 \sqcup \Delta^0, X]
  \stackrel{\simeq}{\to}
  X \times X
  \,.
$$
One checks that this is indeed a [[Kan fibration]].

The stability of fibrations and acyclic fibrations
follows from the above fact that both are characterized
by a [[nLab:weak factorization system|right lifting property]] (as described a [[model structure on simplicial sets]]).

See for instance [section 1](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi) of 

* Goerss, Jardine, _Simplicial homotopy theory_ .

=--

  Concerning the example of [[Kan complex]]es, notice that [[SSet]] is also a _category of co-fibrant objects_ (i.e. $SSet^{op}$ is a category of fibrant objects) so that [[Kan complex]]es are in fact cofibrant and fibrant. That makes much of the technology discussed below superfluous, since it means that the right notion of $\infty$-morphism between Kan complexes is already the ordinary notion. 

  But then, often it is useful to model Kan complexes using the [[Dold-Kan correspondence]], and then the second example becomes relevant, where no longer ever object is cofibrant.

### Simplicial sheaves 

The point of the axioms of a category of fibrant objects is that when passing from [[infinity-groupoid]]s to [[infinity-stack]]s, i.e. to [[sheaf|sheaves]] with values in [[infinity-groupoid]]s, the obvious na&#239;ve way to lift the model structure from $\infty$-groupoids to sheaves of $\infty$-groupoids fails, as the required lifting axioms will be satisfied only locally (e.g. [[stalk]]wise).

 One can get around this by employing a more sophisticated [[model category]] structure as described at [[model structure on simplicial presheaves]], but often it is useful to use a more lightweight solution and consider sheaves with values in $\infty$-groupoids just as a category of fibrant objects, thereby effectively dispensing with the troublesome lifting property (as all mention of cofibrations is dropped):


+-- {: .num_defn}
###### Definition 

**($\infty$-groupoid valued sheaves)**

For $C$ be a [[site]] such that the [[sheaf]] [[topos]]
$Sh(C)$ has [[point of a topos|enough points]],
i.e. so that a morphism $f : A \to B$ in $Sh(X)$
is an isomorphism precisely if its image

$$
  x^* f : x^* A \to x^* B
$$

is a bijection of sets for all [[point of a topos|points]]
([[geometric morphism]]s from $Sh({*}) \simeq Set$)

$$
  x : Set \simeq Sh({*}) 
   \stackrel{\stackrel{x^*}{\leftarrow}}
     {\stackrel{x_*}{\to}}
  Sh(C)
  \,.
$$

Then let

$$
  \mathbf{C} = SSh(C)
$$ 

be the full [[subcategory]] of 

* [[sheaf|sheaves]] on $C$ with values in the category [[SSet]] of [[simplicial set]]s 

* equivalently: [[simplicial object]]s in the [[category of sheaves]] on $C$

on those sheaves $A$ 
for which each [[stalk]] $x^* A \in SSet$ is a [[Kan complex]].

Define a morphism $f : A \to B$ to be a fibration or a weak equivalence, if on each [[stalk]] $x^* f : x^* A \to x^* B$ is a fibration or weak equivalence, respectively, of Kan complexes (in terms of the standard [[model structure on simplicial sets]]).

=--

**Remarks**

* For instance for $X$ any [[topological space]]
we may take $C = Op(X)$ to be the 
[[category of open subsets]] of $X$. 
The points of this topos precisely correspond to the
ordinary points of $X$.

  Equipped with its structure as a category of fibrant
objects, simplicial sheaves on $X$ are a model
for [[infinity-stack]]s living **over $X$**
(the way an object $A \in Sh(X)$ is a sheaf "over $X$").

* Or let $C = $ [[Diff]] be a (small model of)
the [[site]] of smooth [[manifold]]s. 
The corresponding [[sheaf]] [[topos]], 
that of [[smooth space]]s has, up to
isomorphism, one point per natural number, corresponding
to the $n$-dimensional ball $D^n$.

  Equipped with its structure as a category of fibrant
objects, simplicial sheaves on $Diff$ are a model
for [[smooth infinity-stack]]s.



+-- {: .num_lemma }
###### Lemma

$SSh(X)$ with this structure is a category of fibrant objects.

=--

+-- {: .proof}
###### Proof

The terminal object ${*} = X$ is the sheaf constant on the 0-[[simplex]] $\Delta^0$, which represents the space $X$ itself as a sheaf. 

For every simplicial sheaf $A$ and every point $x \in X$ the [[stalk]] of the unique morphism $A \to {*}$ is $x^* A \to x^* {X}$, which is the unique morphism from the [[Kan complex]] $x^* A$ to $\Delta^0$. Since [[Kan complex]]es are fibrant, this is a [[Kan fibration]] for every $x \in X$. So every $A$ is a fibrant object by the above definition.

The fact that fibrations and acyclic fibrations
are preserved under pullback follows from the fact that
the [[stalk]] operation 

$$
  x^* : SSh(X) \to SSh(pt) \simeq SSet
$$

is the [[inverse image]] of a [[geometric morphism]]
and hence preserves finite [[limit]]s and in particular [[pullback]]s. So if $f : A \to B$ is a fibration or acyclic fibration in $SSh(X)$ and 

$$
  \array{
    A \times_B C &\to& B
    \\
    \downarrow^{\mathrlap{h^* f}} && \downarrow^\mathrlap{f}
    \\
    C &\stackrel{h}{\to}& B
  }
$$

is a [[pullback]] diagram in $SSh(X)$, then for $x \in X$ any point of $X$ also

$$
  \array{
    x^*(A \times_{B} C) &\to& x^*B
    \\
    \downarrow^{\mathrlap{x^* (h^* f)}} && \downarrow^{\mathrlap{x^* f}}
    \\
    x^*C &\stackrel{x^*}{\to}& B
  }
$$

is a [[pullback]] diagram, now of [[Kan complex]]es. Since Kan complexes form a category of fibrant objects, 
by the above, it follows that $x^* (h^* f)$ is a fibration or acyclic fibration of Kan complexes, respectively. Since this holds for every $x$, it follows that $h^* f$ is a fibration or acyclic fibration, respectively, in $SSh(X)$.

Recall that a functorial choice of [[path object]] for a [[Kan complex]]e $K$ is the [[internal hom]] $[\Delta^1, K]$ with respect to the [[closed monoidal structure on presheaves|closed monoidal structure on]] [[simplicial set]]s:

$$
  K \stackrel{=}{\to} [\Delta^0, K]
  \stackrel{s_0}{\to}
  [\Delta^1, K]
  \stackrel{d_0 \times d_1}{\to}
  [\Delta^0, K] \times [\Delta^0, K]
  \stackrel{=}{\to}
  K \times K
  \,,
$$

where $s_i$ and $d_i$ denote the [[simplicial set|degeneracy and face maps]], respectively.

For $A \in SSh(X)$ let $[\Delta^1,A]$ denote the sheaf
$$
  [\Delta^1,A] : U \mapsto [\Delta^1,A(U)]
  \,,
$$
where on the left we have new notation and on the right we have the [[internal hom]] in [[SSet]]. 

(The notation on the left defines the way in which $SSh(X)$ is [[copower]]ered  over [[SSet]]).

We want to claim that $[\Delta^1,A]$ is a [[path object]] for $A$.

To check that $[\Delta^1,A]$ is fibrant, let $x \in X$ be any point and consider the [[stalk]] $x^* [\Delta^1,A] \in SSet$. We compute laboriously

$$
  \begin{aligned}
    x^* [\Delta^1,A] &\simeq colim_{U \ni x} [\Delta^1,A(U)]
    \\
    &\simeq colim_{U \ni x} 
     SSet(\Delta^1 \times \Delta^\bullet, A(U))
    \\
    &\simeq 
      ([n] \mapsto colim_{U \ni x} 
     SSet(\Delta^1 \times \Delta^\n, A(U))
    \\
    & 
    \simeq  ([n] \mapsto colim_{U \ni x} 
     \int_{[k] \in \Delta}
      Set(\Delta([k],[1])\times\Delta([k],[n]), A(U)_k)
    \\
    & \simeq
      ([n] \mapsto      
      \int_{[k \leq n+1] \in \Delta}(   
        colim_{U \ni x} 
        Set(\Delta([k],[1])\times\Delta([k],[n]), A(U)_k
      )
    \\
    &\simeq
      ([n] \mapsto      
      \int_{[k] \in \Delta|_{n+1}}(   
       Set(\Delta([k],[1])\times\Delta([k],[n]), 
       colim_{U \ni x} A(U)_k
      )  
    \\
    &\simeq
      ([n] \mapsto      
      \int_{[k] \in \Delta|_{n+1}}(   
       Set(\Delta([k],[1])\times\Delta([k],[n]), 
       (colim_{U \ni x} A(U))_k
      )  
    \\
    &\simeq
     [\Delta^1, colim_{U \ni x} A(U)]
    \\
    & \simeq
     [\Delta^1, x^* A]
)  
  \end{aligned}
$$

Where the

* first step is the general formula for the [[stalk]];

* second step is the formula for the [[internal hom]] in the [[closed monoidal structure on presheaves|closed monoidal structure on simplicial sets]];

* third step is the fact that colimits of presheaves are computed objectwise (see examples at [[colimit]]);

* the fourth step is the definition of the 
  [[SSet]]-[[enriched functor category]] by an [[end]]

* the fifth step uses that 

  * the end truncates to a finite limit with $k \leq n+1$ since $\Delta^1 \times \Delta^n$ is $(n+1)$-[[simplicial skeleton|skeletal]]

  * and that the colimit is over a [[filtered category]] 

  * and that [[limits and colimits by example|filtered colimits commute with finite limits]];

* the sixth step uses that the set $\Delta([k],[1])\times \Delta([k],[n])$ is finite, hence a [[compact object]] so that the colimit can be taken into the hom;

* the seventh step uses again that colimits of presheaves are computed objectwise

* the remaining steps then just rewind the first ones, only that now $A(U)$ has been replaced by $colim_{U \ni x} A(U)$.

That the morphism $A \to [\Delta^1,A]$ is a weak equivalence and that $[\Delta^1,A] \stackrel{d_0 \times d_1}{\to} A \times A$ is a fibration follows similarly by taking the [[stalk]] colimit inside to reduce to the statement that
$x^* A \to [\Delta^1,x^* A]$ is a weak equivalence and 
$[\Delta^1,x^* A] \stackrel{d_0 \times d_1}{\to} x^*A \times x^* A$ is a fibration, using that $[\Delta^1,x^*A]$ is a [[path object]] for the [[Kan complex]] $x^* A$.



=--

The category of fibrant objects $SSh(X)$ 
is in fact the motivating example in [[BrownAHT]]. Notice that the [[homotopy category]] in question coincides with that using the [[model structure on simplicial presheaves]], so that the category of fibrant objects of stalk-wise Kan sheaves is a model for the homotopy category of [[infinity-stack]]s.


#### Example 

Let $G$ be a topogical [[group]] and recall that
$\mathbf{B} G$ denotes the corresponding one-object
[[groupoid]].

For $X$ a [[topological space]] and
$U$ an open subset, let $C(U, G) \in Set$
be the set of continuous maps from $U$ into
$G$. This set naturally is itself a group, so
that to each $U \subset X$ we may associuate the
one-object groupoid 
$$
  U \mapsto \mathbf{B} C(U,G)
  \,.
$$
By postcomposition this with the [[nerve]] operation
we obtain an assignment of [[Kan complex]]es to
open subsets:

$$
  U \mapsto N \mathbf{B} C(U,G) 
  \,.
$$

In degree 0 this is the constant [[sheaf]]

$$
  (N \mathbf{B}(-,G))_0 : U \mapsto {*}  
$$

while in degree 1 this is the [[sheaf]] of $G$-valued functions

$$
  (N \mathbf{B}(-,G))_1 : U \mapsto C(U,G)  
  \,.
$$

When the context is understood, we will just
write $\mathbf{B}G$ again for this $\infty$-groupoid
valued sheaf

$$
  \mathbf{B}G := N \mathbf{B} C(-,G)
  \,.
$$



### Slice categories

Let $\mathbf{C}$ be a category of fibrant objects, with fibrations $F \subset Mor(\mathbf{C})$ and weak equivalences $W \subset Mor(\mathbf{C})$.

For any object $B$ in $\mathbf{C}$, let $\mathbf{C}_B^F$ be the category of fibrations over $B$ (a full subcategory of the [[slice category]] $\mathbf{C}/B$):

* objects are fibrations $A \to B$ in $\mathbf{C}$,

* morphisms are commuting triangles 
  $$
    \array{  
      A &&\to&& A'
      \\
      & {}_{\in F}\searrow && \swarrow_{\in F}
      \\
      && B
    }  
  $$
  in $\mathbf{C}$.

There is an obvious [[forgetful functor]] $\mathbf{C}_B^F \to \mathbf{C}$, which induces notions of weak equivalence and fibration in $\mathbf{C}_B^F$.

+-- {: .num_lemma}
###### Lemma
With this structure, $\mathbf{C}_B^F$ becomes a category of fibrant objects.
=--
+-- {: .proof}
###### Proof

Below is proven the _[[factorization lemma]]_
that holds in any category of fibrant objects.
This implies in particular that every morphism

$$
  \array{
    A &&\stackrel{Id \times Id}{\to}&& A \times_B A
    \\
    & {}_{\in F}\searrow && \swarrow_{\in F}
    \\
    &&
    B 
  }
$$

may be factored as

$$
  \array{
    A &\stackrel{\in W}{\to}& A^I &\stackrel{\in F}{\to}& 
    A \times_B A
    \\
    & {}_{\in F}\searrow && \swarrow_{\in F}
    \\
    &&
    B 
  }
  \,.
$$

This provides the [[path object|path space objects]]
in $\mathbf{C}^F_B$.

=--


## Properties

### Simple consequences of the definition 
 {#SimpleConsequences}

Before looking at more sophisticated constructions, we record the following direct consequences of the definition
of a category of fibrant objects.

+-- {: .num_lemma }
###### Lemma

For every two objects $A_1, A_2 \in \mathbf{C}$,
the two projection maps 
$$
  p_i : A_1 \times A_2 \stackrel{\in F}{\to} A_i
$$
out of their [[product]] are fibrations.

=--

+-- {: .proof}
###### Proof

Because by assumption 
both morphisms $A_i \to {*}$ are fibrations
and fibrations are preserved under pullback

$$
  \array{
    A_1 \times A_2 &\to& A_2
    \\
    \;{}^{p_1}\downarrow^{\mathrlap{\Rightarrow \in F}} && \downarrow^{\mathrlap{\in F}}
    \\
    A_1 &\to&  {*}
  }
  \,.
$$

=--

+-- {: .num_lemma }
###### Lemma

For every object $B \in \mathbf{C}$ and
everey [[path object]] $B^I$ of $B$,
the two morphisms
$$
  d_i : B^I \stackrel{\in W \cap F}{\to} B
$$ 
(whose product $d_0 \times d_1$, recall, is required to be
a fibration) are each separately acyclic fibrations.

=--

+-- {: .proof}
###### Proof

By the above lemma 
$d_i : B^I \stackrel{d_0 \times d_1}{\to} B \times B
  \stackrel{p_i}{\to} B$ is the composite of two fibrations
 and hence itself a fibration.

Moreover, from the diagram

$$
  \array{
    B 
    &\stackrel{\simeq}{\to}& 
    B^I 
    &\stackrel{d_0 \times d_1}{\to}&
    B \times B
    \\
    &&&\searrow^{d_i}& \downarrow^{\mathrlap{p_i}}
    \\
    & \searrow^{Id}&&& B
  }
$$

one reads off that the 2-out-of-3 
property for weak equivalences implies that $d_i$
is also a weak equivalence.


=--


### Generalized universal bundles and the factorization lemma

A central lemma in the theory of categories of fibrant objects is the following [[factorization lemma]].

+-- {: .num_lemma #FactorizationLemma}
###### Lemma (factorization lemma)

For every morphism $f : C \to D$ in a category
$\mathbf{C}$ of fibrant objects, there is an object 
$\mathbf{E}_f B$ such that $f$ factors as

$$
  \array{
    && \mathbf{E}_f B
    \\
    & {}^{\sigma_f \in W}\nearrow && \searrow^{p_f \in F}
    \\
    C &&\stackrel{f}{\to}&& B
  }
$$

with

* $p_f$ a fibration

* $\sigma_f$ a weak equivalence that is a 
  [[section]] ( a [[inverse|right inverse]]) of an acyclic fibration:
  $$
    Id_{\mathbf{E}_f B}
    =
    (
     C
      \stackrel{\sigma_f}{\to}
      \mathbf{E}_f B \stackrel{\simeq}{\to}
      C 
    )
    \,.
  $$

=--

+-- {: .num_remark}
###### Remarks

This is the analog of one of the _factorization axioms_ in a [[model category]] which says that every map factors as an acyclic cofibration followed by a fibration.

Notice that by 
[[category with weak equivalences|2-out-of-3]] 
this in particular implies that every weak equivalence 
$f : C \stackrel{\in W}{\to} B$
is given by a span of acyclic fibrations. 

$$
  \array{
    && \mathbf{E}_f B
    \\
    & {}^{\sigma_f \in W}\nearrow && 
    \searrow^{p_f \in F\cap W}
    \\
    C &&\stackrel{f \in W}{\to}&& B
  }
  \,.
$$

In the context of [[Lie groupoid]] theory these are known as the [[Morita equivalence]]s between groupoids. 
There here arise as a special case. 
Compare also the notion of [[anafunctor]].

=--

The way the proof of this lemma works, one sees that
this really arises in the wider context of computing
[[homotopy pullback]]s in $C$. Therefore we split the
proof in two steps that are useful in their own right
and will be taken up in the next section on homotopy limits.

+-- {: .num_defn}
###### Definition 

For $f : C \to B$ a morphism in $\mathbf{C}$, we say that 
the morphism $p_f : \mathbf{E}_f B \to B$
defined as the composite vertical morphism in the
[[pullback]] diagram

$$
  \array{
   \mathbf{E}_f B &\stackrel{\simeq}{\to}& C
   \\
   \downarrow && \downarrow^{\mathrlap{f}}
   \\
   B^I &\stackrel{d_0}{\to}& B
   \\
   \downarrow^{\mathrlap{d_1}}
   \\
   B
  }
$$

for some [[path object|path space object]] $B^I$
is the [[generalized universal bundle]] over $B$
relative to $f$.

=--

The universal bundle terminology is best
understood from the following example

+-- {: .num_example}
###### Example

Consider the category of fibrant objects given by
[[Kan complex]]es or just [[strict omega-groupoid]]s.

For $G$ an ordinary [[group]] write $\mathbf{B} G$
for the corresponding [[groupoid]].
When regarding $G$ as a constant [[simplicial group]]
the corresponding [[Kan complex]] is often denoted
$\bar W G$ (see [[simplicial group]]) but we shall
just write $\mathbf{B} G$ also for this Kan complex,
for simplicity.

The corresponding [[path object]] is given by the [[groupoid]] 
(or its corresponding Kan complex) 
$$
  (\mathbf{B} G)^I
  =
  [\Delta^1, \mathbf{B} G ]
  =
  G \backslash \backslash G//G
$$
where the right denotes the [[action groupoid]]
of $G \times G$ acting on $G$ by left and right multiplication.

Let ${*} : {*} \to \mathbf{B} G$ be the unique
morphism from the [[point]] into $\mathbf{B} G$.
The corresponding generalized universal bundle is

$$
  \mathbf{E}_{*} G = G//G
$$

the [[action groupoid]] of $G$ acting on  itself
from just the right. (The corresponding [[Kan complex]]
is traditionally denoted $W G$ when thought of as a 
[[simplicial group]]).

That $G//G \to \mathbf{B}G$ is indeed the 
universal $G$-[[principal bundle]] 
(under the [[homotopy hypothesis|Quillen equivalence of]]
[[Kan complex]]es and [[topological space]]s) is an
old result of Segal
(as described at [[generalized universal bundle]]).


=--


+-- {: .num_lemma }
###### Lemma

The morphism $p_f : \mathbf{E}_f B \to B$ is
a fibration.

=--

+-- {: .proof}
###### Proof

The defining [[pullback]] diagram for $\mathbf{E}_f B$
can be refined to a double pullback diagram as follows

$$
  \array{
    \mathbf{E}_f B 
     &\stackrel{\in F}{\to}& 
     C \times B 
     &\stackrel{p_1}{\to}& 
     C
     \\
     \downarrow && \downarrow^{\mathrlap{f \times Id}} && \downarrow^{\mathrlap{f}}
     \\
     B^I &\stackrel{d_0 \times d_1 \in F}{\to}&
     B \times B &\stackrel{p_1}{\to}&
     B
     \\
     \downarrow^{\mathrlap{d_1}} & \swarrow_{p_2 \in F}
     \\
     B
  }
  \,.
$$

Both squares are pullback squares. Since
pullbacks of fibrations are fibrations, the morphism
$\mathbf{E}_f B  \to C \times B$ is a fibration.

By one of the lemmas above, also the projection map
$p_i : B \times B \to B$ is a fibration. 

The above diagram exibits $p_f$ as the the composite

$$
  \begin{aligned}
    p_f &: \mathbf{E}_f B \to C \times B
    \stackrel{f \times Id}{\to}
    B \times B
    \stackrel{p_2}{\to}
    B
    \\
    & =
    \mathbf{E}_f B \to C \times B
    \stackrel{p_2}{\to}
    B 
  \end{aligned}
$$

of two fibrations. Therefore it is itself a fibration.

=--

+-- {: .num_lemma }
###### Lemma

The morphism $\mathbf{E}_f B \stackrel{\simeq}{\to} C$ 
has a [[section]] (a [[inverse|right inverse]])
$\sigma_f : C \stackrel{\simeq}{\to}
   \mathbf{E}_f B$ and its composite with
   $p_f$ is $f$:

  $$
    \array{
      \mathbf{E}_f B &\stackrel{\sigma_f}{\leftarrow}&&
      C
      \\
      \downarrow^{\mathrlap{p_f}} && \swarrow_{f}
      \\
      B
    }
  $$

=--

+-- {: .proof}
###### Proof

The [[section]] 
$$
  \sigma_f = Id \times \sigma \circ f
$$
is the morphism induced via the
universal property of the [[pullback]] by the
[[section]] $\sigma : B  \to B^I$ of
$d_0 : B^I \to B$:

$$
  \array{
    C 
    &\stackrel{\sigma_f \in W}{\to}&
    \mathbf{E}_f B 
    &\stackrel{\in W \cap F}{\to}&
    C
    \\
    \downarrow^{\mathrlap{f}} 
    &&
    \downarrow
    &&
    \downarrow^{\mathrlap{f}} 
    \\
    B &\stackrel{\sigma}{\to}&
    B^I
    &\stackrel{d_1 \in W \cap F}{\to}&
    B
    \\
    & {}_{Id}\searrow & \downarrow^{\mathrlap{d_0}}
    \\
    && B
  }
  \;\;\;\;
  =
  \;\;\;\;
  \array{
    C 
    &\stackrel{Id}{\to}&
    C
    \\
    \downarrow^{\mathrlap{f}} 
    &&
    \downarrow^{\mathrlap{f}} 
    \\
    B &\stackrel{Id}{\to}&
    B
  }
  \,.
$$

=--

### More sophisticated consequences of the definition

Using the [[factorization lemma]], one obtaines the following
further useful statements about categories of fibrant
objects:

Recall that plain weak equivalences,
if they are not at the same time fibrations,
are not required by the axioms to be preserved by 
[[pullback]]. But it follows from the axioms that
weak equivalences are preserved under pullback along fibrations.

This we establish in two lemmas.

+-- {: .num_lemma #BaseChangePreservesFibrationsAndWeakEquivalences}
###### Lemma

Let 

$$
 \array{
  A_1 &&\stackrel{f}{\to}&& A_2
  \\
  & {}_{\in F}\searrow && \swarrow_{\in F}
  \\
  && B
 }
$$

be a morphism of fibrations over 
some object $B$ in $\mathbf{C}$
and let $u : B' \to B$ be any morphism in 
$\mathbf{C}$. Let 

$$
 \array{
  u^*A_1 &&\stackrel{u^* f}{\to}&& u^* A_2
  \\
  & {}_{\in F}\searrow && \swarrow_{\in F}
  \\
  && B'
 }
$$

be the corresponding morphism pulled back along $u$.

Then

* if $f \in F$ then also $u^* f \in F$;

* if $f \in W$ then also $u^* f \in W$.



=--

+-- {: .num_proof}
###### Proof

For $f \in F$ the statement follows from 
the fact that in the diagram

$$
  \array{
    B' \times_B A_1 &\to& A_1
    \\
    \;\;\downarrow^{\mathrlap{u^* f \in F}} 
    && \;\;\downarrow^{\mathrlap{f \in F}}
    \\
    B' \times_B A_2 &\to& A_2
    \\
    \;\downarrow^{\mathrlap{\in F}} && \;\downarrow^{\mathrlap{\in F}}
    \\
    B' &\stackrel{u}{\to}& B
  }
$$

all squares (the two inner ones as well as the
outer one) are [[pullback]] squares,
since pullback squares compose under pasting.

The same reasoning applies for $f \in W \cap F$.

To apply this reasoning 
to the case where $f \in W$, we first
make use of the factorization lemma 
to decompose $f$ as a right inverse to an
acyclic fibration followed by an
acyclic fibration. 

$$
  f : A_1 \stackrel{\in W}{\to} \mathbf{E}_f A_2 
  \stackrel{\in W \cap F}{\to} A_2
  \,.
$$

(Compare the definition of the category
of fibrant objects
$\mathbf{C}_B^F$ of fibrations over $B$,
discussed in the example section above.)


Using the above this reduces the proof to showing that 
the pullback of the top horizontal morphism of

$$
 \array{
  A_1 &&\stackrel{}{\to}&& \mathbf{E}_f A_2
  \\
  & {}_{\in F}\searrow && \swarrow_{\in F}
  \\
  && B
 }
$$

(here the fibration on the right is the composite 
of the fibration $\mathbf{E}_f A_2 \to A_2$ with $A_2 \to B$)

along $u$ is a weak equivalence. For that 
consider the diagram

$$
  \array{
    B' \times_B A_1  &\to& A_1
    \\
    \downarrow && \downarrow
    \\
    B' \times_B \mathbf{E}_f A_2 
    &\to& 
    \mathbf{E}_f A_2
    \\
    \;\;\downarrow^{\mathrlap{\in W \cap F}} 
    && 
      \;\;\downarrow^{\mathrlap{\in W \cap F}}
    \\
    B' \times_B A_1 &\to& A_1
    \\
    \;\downarrow^{\mathrlap{\in F}} && \;\downarrow^{\mathrlap{\in F}}
    \\     
    B' &\to& B
  }
$$

where again all squares are pullback squares.
The top two vertical composite morphisms are
identities. Hence by 2-out-of-3 
the morphism
$B' \times_B E_1 \to B' \times_B \mathbf{E}$
is a weak equivalence.

=--


+-- {: .num_lemma }
###### Lemma

The pullback of a weak equivalence along a fibration
is again a weak equivalence.

=--
\begin{proof}
Let be a fibration $p:E\to B$ and let $e:A\to B$ be a weak equivalence. Without
loss of generality we can assume that $e$ is a section of a acyclic fibration
$q:B\to A$ -- otherwise we first decompose with the factorization lemma and then
pull back along the factors individually.

Consider the following diagram where the four tiled squares are pullbacks,
$f=\langle{p,\mathrm{id}}\rangle$, and the bent back rectangle is also a
pullback.
\begin{tikzcd}[sep = 15]
        Y       \ar[rr,"h"']
                \ar[rd,"g"]
                \ar[rddddd, bend right]
&&      E       \ar[rd,"f" description]
                \ar[rrrd,"\mathrm{id}"]
                \ar[rddddd, bend right,"p"]
\\&     E       \ar[dd,"p"]
                \ar[rr, crossing over,"k"' near end]
&&      X       \ar[rr,"l"']
                \ar[dd]
&&      E       \ar[dd,"p"]
\\\\&   B       \ar[rr, crossing over]
                \ar[dd,"q"]
&&      \bullet \ar[rr]
                \ar[dd]
&&      B       \ar[dd,"q"]
\\\\&   A       \ar[rr,"e"]
&&      B       \ar[rr,"q"]
&&      A
\end{tikzcd}
$l$ is a weak equivalence since $q$ is a acyclic fibration, and by 2-out-of-3 we can
conclude that $f$ is a weak equivalence as well. By the preceding lemma \ref{BaseChangePreservesFibrationsAndWeakEquivalences}, so is
$g$. The goal is to show that $h$ is a weak equivalence, and by 2-out-of-3 it's enough
to check that for $k$. This follows again from 2-out-of-3 since $k$ is a section of
$l$ (because the bottom row of the diagram is an identity).
\end{proof}

+-- {: .num_remark}
###### Remarks

[[model category|Model categories]]
that satisfy this property are called 
[[right proper model category|right proper model categories]].

Right properness is a crucial assumption
in the closely related work

* Jardine, 
  _Cocycle categories_ ([arXiv](http://arxiv.org/abs/math.AT/0605198))
=--



### Homotopy fiber product 
 

Using the existence of [[path object|path space objects]] one can construct specific [[homotopy pullback]]s
called  _homotopy fiber products_ .


+-- {: .num_defn #HomotopyFiberProducts}
###### Definition

A **homotopy fiber product** 
or **homotopy pullback** of two morphisms

$$
  A \stackrel{u}{\to} C \stackrel{v}{\leftarrow} B
$$

in a category of fibrant objects
is the object $A \times_C C^I \times_C B$  defined as the 
(ordinary) [[nLab:limit|limit]]

$$
  \array{
    A \times_C C^I \times_C B &&&\to & B
    \\
    &&&& \downarrow^v
    \\
    & &C^I & \stackrel{d_0}{\to}& C
    \\
    \downarrow &&
    \downarrow^{\mathrlap{d_1}}
    \\
    A &\stackrel{u}{\to} & C    
  }
  \,.
$$

=--



+-- {: .num_remark}
###### Remark

This essentially says that $A \times_C C^I \times_C B$ is the universal object that makes the diagram
$$
  \array{
     A \times_C C^I \times_C B &\to& B
     \\
     \downarrow && \downarrow^{\mathrlap{v}}
     \\
     A &\stackrel{u}{\to}& C
  }
$$
commute up to [[homotopy]] 
(see the section on homotopies for more on that).

=--

+-- {: .num_remark}
###### Remark

These homotopy pullbacks present indeed the correct 
[[(infinity,1)-limits]], this is the content of 
prop. \ref{PullbacksAlongFibrationsAreCorrectHomotopyPullbacks}
below.

=--

+-- {: .num_lemma }
###### Lemma


The projection

$$
 A \times_C C^I \times_C B \to A
$$
out of a homotopy fiber product is a fibration. If $v : B \to C$ is 
a weak equivalence, then this is an acyclic fibration.

=--

The same is of course true for the map to $B$ and the
morphism $u : A \to C$, by symmetry of the diagram.

+-- {: .proof}
###### Proof

One may compute this [[nLab:limit|limit]] in terms of two consecutive 
[[nLab:pullback|pullback]]s in two different ways.

On the one hand we have

$$
  \array{
    A \times_C C^I \times_C B &\to& \mathbf{E}_v C &\to 
    & B
    \\
    && \downarrow && \downarrow^{\mathrlap{v}}
    \\
    & &C^I & \stackrel{d_0}{\to}& C
    \\
    \downarrow &&
    \downarrow^{\mathrlap{d_1}}
    \\
    A &\stackrel{u}{\to}& C    
  }
$$

where both squares are [[pullback]] squares. 

By the above lemma on generalized universal bundles,
the map $\mathbf{E}_v C \to C$ is a fibration. The first
claim follows then since fibrations are stable under pullback.

On the other hand we can rewrite the limit diagram also as
$$
  \array{
    A \times_C C^I \times_C B &\to& && B
    \\
    \downarrow && && \downarrow^{\mathrlap{v}}
    \\
    \mathbf{E}_u C & \stackrel{\in W \cap F}{\to} &C^I & 
    \stackrel{d_0 \in W \cap F}{\to}& C
    \\
    \downarrow^{\mathrlap{\in W \cap F}} 
    &&
    \;\;\downarrow^{\mathrlap{d_1\in W \cap F}}
    \\
    A &\stackrel{u}{\to} & C    
  }
$$

where again both inner squares are [[pullback]] squares.

Again by the above statement on generalized universal
bundles, we have that the morphism 
$\mathbf{E}_u C \to C$ is a fibration.
By one of the above propositions, weak equivalences
are stable under pullback along fibrations, hence the pullback 
$A \times_C C^I \times_C B \to \mathbf{E}_u C$
of $v$ is a weak equivalence. Since also 
$\mathbf{E}_u C \to A$ is a weak equivalence 
(being the pullback of an acyclic fibration)
the entire morphism 
$A \times_C C^I \times_C B  \to A$ is.

=--


### Homotopies  
 {#Homotopies}


+-- {: .num_defn}
###### Definition

Two morphism $f,g : A \to B$ in $C(A,B)$
are 

* **right [[homotopy|homotopic]]**, denoted $f \simeq g$, precisely if they fit into a diagram
  $$
    \array{
      && B
      \\
      & {}^f\nearrow & \uparrow^{d_0}
      \\
      A &\stackrel{\eta}{\to}&
      B^I
      \\
      & {}_g\searrow & \downarrow^{\mathrlap{d_1}}
      \\
      && B
    }
  $$ 
  for some [[path object|path space object]] $B^I$;

* **[[homotopy|homotopic]]**, denoted $f \sim g$,
  if they become right homotopic after pulled back
  to a weakly equivalent domain, 
  i.e. precisely if they fit into a diagram

$$
  \array{
    &&
    A 
    &\stackrel{f}{\to}& B
    \\
    &{}^{w \in W}\nearrow&&& \uparrow^{d_0}
    \\
    \hat A 
    &&
    \stackrel{\eta}{\to}
    &&
    B^I
    \\
    &{}_{w\in W}\searrow & &&
    \downarrow^{d_1}
    \\
    &&
    A
    &\stackrel{g}{\to}& 
    B
  }
$$

for some object $\hat A$ and
for some [[path object|path space object]] $B^I$ of $I$

=--

+-- {: .num_remark}
###### Remark

So this says that there is a
right [[homotopy]] between the two morphisms after
both are pulled back to a sufficiently good resolution of 
their domain.
=--

+-- {: .num_lemma }
###### Lemma

For $A,B \in \mathbf{C}$, right homotopy
is an equivalence relation on the 
[[hom-set]] $\mathbf{C}(A,B)$.

=--

+-- {: .proof}
###### Proof

This follows by "piecing path spaces together":

Let $B^{I_1}$ and $B^{I_2}$ be two path space
objects of $B$. Then the pullback

$$
  \array{
    B^{I_1 \vee I_2} &\to&  B^{I_2}
    \\
    \downarrow && \downarrow^{d_0}
    \\
    B^{I_1} &\stackrel{d_1}{\to}& B
  }
$$

defines a new path object, with structure maps

$$
  B
  \stackrel{\sigma_1 \times \sigma_2}{\to}
  B^{I_1 \vee I_2}
  \stackrel{(d_0 \circ p_1) \times (d_1\circ p_2)}{\to}
  B \times B
  \,.
$$

So given two right homotopies 
with respect to $B^{I_1}$ and $B^{i_2}$ we can paste them
next to each other and deduce a homotopy through 
$B^{I_1 \vee I_2}$

$$
  \array{
    && B
    \\
    & {}^f\nearrow &  \uparrow^{d_0^1}
    \\
    A &\stackrel{\eta_1}{\to}&
    B^{I_1}
    \\
    & {}_{g}\searrow& \downarrow^{\mathrlap{d_1^1}}
    & \nwarrow
    \\
    && B && B^{I_1 \vee I_2}
    \\
    & {}^{g}\nearrow & \downarrow^{\mathrlap{d_0^2}}
    & \swarrow
    \\
    A &\stackrel{\eta_2}{\to}& B^{I_2}
    \\
    & {}_h\searrow & \downarrow^{\mathrlap{d_1^2}}
    \\
    &&B
  }
$$

=--


We next similarly want to deduce that not only right homotopy
$f \simeq g$ but also true homtopy $f \sim g$
defines an equivalence relation on [[hom-set]]s 
$\mathbf{C}(A,B)$. For that we need the following to lemmas.


+-- {: .num_lemma }
###### Lemma

Every diagram

$$
  \array{
    A &\to& E
    \\
    \;\;\downarrow^{\mathrlap{i \in W}}
    &&
    \;\;\downarrow^{\mathrlap{p \in F}}
    \\
    X
    &\to&
    B
  }
$$

may be refined to a diagram

$$
  \array{
    A &\to & X' &\to& E
    \\
    & {}_{i}\searrow & 
    \;\;\downarrow^{\mathrlap{t \in W \cap F}}
    &&
    \;\;\downarrow^{\mathrlap{p \in F}}
    \\
    && X
    &\to&
    B
  }
$$


=--


+-- {: .proof}
###### Proof

Consider the pullback square

$$
  \array{
    A &\to&
    X \times_B E &\to& E 
    \\
    &{}_{i \in W}\searrow& \;\; \downarrow^{\mathrlap{\in F}}
    &&
    \;\; \downarrow^{\mathrlap{\in F}}
    \\
    && X &\to& B
  }
$$

and apply the [[factorization lemma]], lemma \ref{FactorizationLemma}, to factor 
the universal morphism $A \to X \times_B E \to E$
into the pullback as

$$
  A \stackrel{\in W}{\to} \mathbf{E} E \stackrel{\in F}{\to}
  E
$$ 

to obtain the diagram

$$
  \array{
    A &\stackrel{\simeq}{\to}&
    \mathbf{E} E &\to& E 
    \\
    &{}_{i \in W}\searrow& 
    \;\; \downarrow^{\mathrlap{\in F}}
    &&
    \;\; \downarrow^{\mathrlap{\in F}}
    \\
    && X &\to& B
  }
  \,,
$$

where the middle vertical morphism is still a
fibration, being the composite of two fibrations.
By [[category with weak equivalences|2-out-of-3]]
it follows that it is also a weak equivalence.

=--


+-- {: .num_lemma}
###### Lemma


For $ u : B \to C$ a morphism and $B^I$, $C^I$ choices of path objects,
there is always another path object $B^{I'}$
with an acyclic fibration 
$B^I \stackrel{\in W \cap F}{\leftarrow} B^{I'}$ 
and a span of morphisms of path space objects


$$
  \array{
    B &\stackrel{=}{\leftarrow}& B &\stackrel{u}{\to}& C
    \\
    \downarrow^{\mathrlap{\sigma}} && \downarrow^{\sigma'} && \downarrow^{\mathrlap{\sigma_C}}
    \\
    B^I &\stackrel{\in W \cap F}{\leftarrow}& B^{I'} &\stackrel{\bar u}{\to}& C^I
    \\
    \;\;\downarrow^{d_0 \times d_1} 
    && \;\;\downarrow^{\mathrlap{d'_0 \times d'_1}} 
    && \;\;\downarrow^{\mathrlap{d_0^C \times d_1^C}}
    \\
    B \times B
    &\stackrel{=}{\leftarrow}&
    B \times B 
    &\stackrel{u \times u}{\to}&    
    C \times C
  }
$$

=--


+-- {: .proof}
###### Proof

Apply the lemma above to the square

$$
  \array{
    B &\stackrel{u}{\to}& C 
     &\stackrel{\sigma_C}{\to}& 
     C^I
    \\
    \downarrow^{\mathrlap{\sigma}} &&&& \downarrow^{\mathrlap{d_0 \times d_1}}
    \\
    B^I &\stackrel{d_0 \times d_1}{\to}& B \times B
    &\stackrel{u \times u}{\to}& C \times C
  }
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

Right homotopy $f \simeq g$ between morphisms 
is preserved under pre- and postcomposition with a given morphism.

More precisely,
let $f, g : B \to C$ be two homotopic morphisms. Then 

* for all morphisms $A \to B$ and $C \to D$ the composites
$A \to B \stackrel{f}{\to} C \to D$ and $A \to B \stackrel{g}{\to} C \to D$
are still right homotopic.

* moreover, the right homotopy may be realized 
  with every given choice of   
  [[nLab:path object|path space object]] $D^I$ for $D$.

=--

+-- {: .proof}
###### Proof

We decompose this into two statements:

1. for any $A \to B$ the morphisms $A \to B \stackrel{f,g}{\to} B$ are right homotopic.

1. for any $u : C \to D$ and choice $D^I$ of path object there is an acyclic fibration
   $
     B' \to B
   $
   such that 
   $B' \to B \stackrel{f}{\to} C \to D$ 
   is right homotopic to
   $B' \to B \stackrel{g}{\to} C \to D$
   by a right homotopy $\eta : B' \to D^I$.
   
The first of these follows trivially.

The second one follows by using the weak functoriality property of path objects
from above: let $B' := B \times_{C^I} C^{I'}$ 
be the [[pullback]]
in the following diagram

$$
  \array{
    B' 
    &\to&
    C^{I'}
    &\stackrel{\bar u}{\to}&
    D^I
    \\
    \;\;\;\downarrow^{\mathrlap{\in W \cap F}}
    &&
    \;\;\;\downarrow^{\mathrlap{\in W \cap F}}     
    &&
    \downarrow
    \\
    B 
    &\stackrel{\eta}{\to}&
    C^I 
    \\
    &{}_{f \times g}\searrow
    & \downarrow
    && 
    \downarrow
    \\
    &&
    C \times C
    &\stackrel{u \times u}{\to}&
    D \times D
  }
$$

=--


We need one more intermediate result 
for seeing that homotopy is an equivalence relation


+-- {: .num_lemma}
###### Lemma

* Every diagram

  $$
  \array{
    && B
    \\
    && \downarrow^{\mathrlap{w \in W}}
    \\
    A &\to& C  
  }
  $$

  in $\mathbf{C}$ extends to a 
  (right) homtopy-commutative diagram
  $$
  \array{
    A' &\to & B
    \\
    \downarrow^{\mathrlap{w' \in W}} && \downarrow^{\mathrlap{w \in W}}
    \\
    A &\to& C  
  }
  \,.
  $$

* For every pair of morphisms
  $$
    f, g, A \stackrel{\to}{\to} B
  $$
  and weak equivalence
  $t : B \stackrel{\in W}{\to} C$
  such that there is a right homotopy
  $t \circ f \simeq t \circ g$, there exists
  a weak equivalence $t' : A' \to A$
  such that $f \circ t' \simeq g \circ t'$.


=--

+-- {: .proof}
###### Proof


* The first point we accomplish this by letting $A' := A \times_C C^I \times_C B$ be the homotopy fiber product
in $C$ of a representative of the pullback diagram. 
The lemma 
about morphisms out of the
homotopy fiber product says 
that $A' \to A$ is a weak equivalence.

* The second point is more work. 
  Let $\eta : A \to C^I$ the right homotopy in question. 
  We start by considering
  the homotopy fiber product
  $$
    \array{
      D := B \times_C C^I \times_C B
      &\to&&\stackrel{\in W}{\to}& B
      \\
      \downarrow^{\mathrlap{\in W}} &&&&
      \downarrow^{\mathrlap{t \in W}}
      \\
      && C^I &\stackrel{d_0}{\to}&
      C
      \\
      \downarrow && \downarrow^{d_1}
      \\
      B &\stackrel{t \in W}{\to}& C
    }
    \,,
  $$
  where the long morphisms are weak equivalences
  by the lemma on morphisms out of homotopy fiber products.

 Then consider the two universal morphisms
  $$
   (f,\eta,g) : A \to B \times_C C^I \times_C B
  $$
  and
  $$
    (Id, \sigma \circ t, Id) : 
    B \stackrel{\in W}{\to} B \times_C C^I \times_C B
  $$
  into that. It follows by 2-out-of-3 that the latter
  is a weak equivalence. Factoring this 
  using the factorization lemma produces hence
  $$
    B \stackrel{\in W}{\to} D' \stackrel{\in W \cap F}{\to}
    D
    \,.
  $$

  We know moreover that the product map 
  $D \stackrel{\in F}{\to} B \times B$
  is a fibration, as we can rewrite the homotopy
  limit as the pullback
  $$
    \array{  
       D &\to& C^I
       \\
       \downarrow && \downarrow^{\mathrlap{\in F}}
       \\
       B \times B &\stackrel{f \times g}{\to}&
       C \times C
    }
    \,.
  $$

  It follows that the composite $D' \to D \to B \times B$
  is a fibration and hence $D'$ a path space object for
  $B$.

  Finally, by setting $A' = A \times_D D'$
  we obtaine the desired right homotopy
  $f \circ t' \simeq g \circ t'$.
  $$
    \array{
      A' &\to& D'
      \\
      \downarrow^{\mathrlap{t'}} && \downarrow
      \\
      A &\to & D &\to & C^I
      \\
      & {}_{f \times g}\searrow & \downarrow 
      && \downarrow 
      \\
      && B \times B
      &\stackrel{t \times t}{\to}&
      C \times C
    }
    \,.
  $$

=--
 

+-- {: .num_lemma }
###### Lemma

The relation "$f, g \in C(A,B)$ are homotopic",
$f \sim g$,
is an [[equivalence relation]] on $C(A,B)$.

=--

+-- {: .proof}
###### Proof

The nontrivial part is to show transitivity.
This now follows with the above lemma
about homtopy commutative composition of 
pullback diagrams and then using the
"piecing together of path objects"
used above to show that right homotopy
is an equivalence relation.


=--












+-- {: .num_defn}
###### Definition

For $C$ a category of fibrant objects the category
$\pi C$ is defined to be the category

* with the same objects as $C$;

* with [[hom-set]]s the set of equivalence classes
  $$
   \pi C(A,B) := C(A,B)/_\sim
  $$
  under the above equivalence relation.

* Composition in $\pi C$ is given by composition of
  representatives in $C$.

=--

+-- {: .num_defn}
###### Definition

The obvious functor

$$
  C \to \pi C
$$

is the identity on objects and the projection to
[[equivalence relation|equivalence classes]] on
[[hom-set]].

Let $\pi W \subset Mor(\pi C)$ be the image of the 
weak equivalences of $C$ in $\pi C$ under this functor,
and $\pi F$ the image of the fibrations.

=--


+-- {: .num_theorem }
###### Theorem

The weak equivalences in $\pi C$ form  a left multiplicative system.

=--

+-- {: .proof}
###### Proof

This is now a direct consequence of the above
lemma on homotopy-commutative completions of diagrams.

=--



### The homotopy category  
 {#HomotopyCategory}

We discuss now 
that the structure of a category of fibrant objects on a 
[[homotopical category]] $C$ induces 

* a related category $\pi C$ 

* with a morphism $C \to \pi C$

  * that is the identity on objects, 
  
  * and induces on $\pi C$ a notion of weak equivalences
    $$
      \pi W \subset Mor(\pi C)
    $$
    and fibrations
    $$
      \pi F \subset Mor(\pi C)
    $$

* such that

  * the weak equivalences in $\pi C$ form a [[calculus of fractions|left multiplicative system]] .

This implies the following convenient construction
of the [[homotopy category]] of $C$:

+-- {: .num_theorem}
###### Theorem

For $C$ a category of fibrant objects, 
its [[homotopy category]] is 
([[equivalence of categories|equivalent]] to) the category
$Ho_C$ with

* the same objects as $C$;

* the [[hom-set]] $Ho_C(A,B)$ for all $A, B \in Obj(C)$
  given naturally by
  $$
    \begin{aligned}
      Ho_C(A,B) 
      & \simeq 
      colim_{\hat A \stackrel{w\in \pi W}{\to} A}
      \pi C (\hat A,B)
      \\
      & =
      colim_{\hat A \stackrel{f\in \pi W\cap F}{\to} A}
      \pi C (\hat A,B)      
    \end{aligned}
    \,.
  $$

=--

Here the colimit is, as described at [[calculus of fractions|multiplicative system]], over the [[opposite category]] of the category $\pi W_A$ or $(\pi F\cap \pi W)_A$ 
whose objects are weak equivalences $\hat A \stackrel{w \in \pi W}{\to} A$ or acyclic fibrations
$\hat A \stackrel{f \in \pi W\cap F}{\to} A$ in $\pi C$, and whose morphisms are commuting triangles

$$
  \array{
    \hat A &&\stackrel{h}{\to}&& \hat A'
    \\
    & \searrow && \swarrow
    \\
    &&
    A
  }
$$
in $\pi C$ (i.e. for arbitrary $h$).

So more in detail the above colimit is over the functor

$$
  \pi C(-, B)_A : 
  (\pi W_A)^{op} \to (\pi C)^{op} 
  \stackrel{\pi C(-, B)}{\to}
  Set
  \,,
$$

where the first functor is the obvious forgetful functor.

+-- {: .num_remark}
###### Remark

It is again the factorization lemma above (and using 2-out-of-3 that implies that inverting just the acyclic fibrations in $C$ is already equivalent to inverting all weak equivalences. This means that the above theorem remains valid if the weak equivalences $t : A' \to A$ are replaced by _acyclic fibrations_:

every cocycle 
$\array{
   Y &\stackrel{g}{\to}& A
   \\
   {}^\simeq \downarrow^{\mathrlap{f}} 
   \\
   X
 }$

out of a weak equivalence is refines by a cocycle out of an acyclic fibrantion, namely

$$
\array{
   \mathbf{E}_f X &\stackrel{\simeq}{\to}& 
      Y &\stackrel{g}{\to}& A
   \\
   &{}_{\in F \cap W}\searrow& {}^\simeq \downarrow^{\mathrlap{f}} 
   \\
   && X
 }
  \,.
$$


Using acyclic fibrations has the advantage that these are preserved under [[pullback]]. This allows to consistently compose spans whose left leg is an acyclic fibration by [[pullback]]. See also the discussion at [[anafunctor]].

A discussion of this point of using weak equivalences versus acyclic fibrations in the construction of the homotopy category is also in Jardine: [Cocycle categories](http://www.math.uiuc.edu/K-theory/0782/).
=--


We now provide the missing definitions and then the proof
of this theorem.


+-- {: .num_lemma }
###### Lemma

The homotopy categories of $C$ and $\pi C$ coincide:

$$
  Ho_C \simeq Ho_{\pi C}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By one of the lemmas above, the morphisms
$d_i : B^I \to B$ are weak equivalences
and become [[isomorphism]]s in $Ho_C$.
The [[section]] $\sigma : B \to B^I$
then becomes an [[inverse]] for both 
of them, hence the images of $d_0$ and
$d_1$ in $Ho_C$ coincide. Therefore
the above diagram says that homotopic morphisms
in $C$ become equal in $Ho_C$.

But this means that the localization morphism
$$
  Q_C : C \to Ho_C
$$
factors through $\pi C$ as

$$
  Q_C : C \to \pi C \stackrel{Q_{\pi C}}{\to} Ho_C
$$

where $Q_{\pi C}$ sends weak equivalences in $\pi C$
to isomorphisms in $Ho_C$.

The universal property of $Q$ then implies the universal
property for $Q_{\pi C}$

$$
  \array{
    C &\to& \pi C &\to & A
    \\
    \downarrow^{\mathrlap{Q_C}} & \swarrow^{Q_{\pi C}} && \swarrow
    \\
    Ho_C
  }
  \,.
$$

=--



The above theorem on the description of $Ho_C$
now follows from the general formula for
[[localization]] at a 
[[calculus of fractions|left multiplicative system]]
of weak equivalences.

### Pointed category of fibrant objects 

If the category $C$ of fibrant objects has an initial object which _coincides_ with the terminal object $e$, i.e. a [[zero object]], then $C$ is a [[pointed category]]. In this case we have the following additional concepts and structures.

### Fibers

 For $p : Y \to X$ a fibration, the pullback $F$ in

$$
  \array{
     F &\stackrel{i}{\to}& Y
     \\
     \downarrow && \downarrow
     \\
     e &\to& X
  }
$$

is the **fibre** of $p$ and $i$ is the _fibre inclusion_.
(This is the _kernel_ of the morphism $f$ of [[pointed object]]s)


### Fibration Sequences 

(See also [[fibration sequence]])

For $B$ any object and $B^I$ any of its [[path object]]s, the fiber of $B^I \stackrel{d_0 \times d_1}{\to} B \times B$ is the **[[loop space object|loop object]]** $\Omega^{(I)} B$ of $B$ with respect to the chosen path object. This construction becomes independent up to canonical isomorphism of the chosen path space after mapping to the [[homotopy category]] and hence there is a functor

$$
  \Omega : Ho_C \to Ho_C
$$

which sends any object $B$ of $C$ to its canonical loop object $\Omega B$.

Any loop object $\Omega B$ becomes a group object in $Ho_C$, i.e. a group [[internalization|internal to]] $Ho_C$ in a natural way.

### Derived hom-spaces
 {#DerivedHomSpaces}

There is an explicit simplicial construction of the [[derived hom spaces]] for a homotopical category that is equipped with the structure of a category of fibrant objects.
This is described in ([Cisinksi 10](#Cisinski10)) and ([Nikolaus-Schreiber-Stevenson 12, section 3.6.2](#NSS12)).

+-- {: .num_defn #CocycleCategories}
###### Definition 

For $\mathcal{C}$ a category of fibrant objects, write for any $X, A \in Obj(\mathcal{C})$

$$
  Cocycle(X,A) , wCocycle(X,A) \in Cat
$$

for the [[categories]] ("categories of [[cocycles]] on $X$ with [[coefficients]] in $A$") whose [[objects]] are [[correspondences]]

$$
  X \stackrel{\simeq}{\longleftarrow}
  \hat X
  \stackrel{}{\longrightarrow}
  A
$$

with the left leg an acyclic fibration (for $Cocycle(X,A)$) or just a weak equivalence (for $wCocycle(X,A)$); and whose morphisms are morphisms of spans

$$
  \array{
    && \hat X
    \\
    & \swarrow && \searrow
    \\
    X && \downarrow && A
    \\
    & \nwarrow && \nearrow
    \\
    && \hat X'
  }
$$

=--

+-- {: .num_prop #CocycleCategoriesPresentDerivedHomSpaces}
###### Proposition

Write $L^H_{we} \mathcal{C}$ for the [[simplicial localization]] of the category of fibrant objects $\mathcal{C}$ at its weak equivalences (hence essentially the [[(infinity,1)-category]] that it presents). Then for all objects $X,A \in Obj(\mathcal{C})$ the canonical maps

$$
  N Cocycle(X,A)
  \to
  N wCocycle(X,A)
  \to 
  L^H_{we} \mathcal{C}(X,A)
$$

of [[simplicial sets]] (on the left the [[nerves]] of the cocycle categories of def. \ref{CocycleCategories}, on the right the [[derived hom space]] given by the [[simplicial localization]]) are [[weak homotopy equivalences]].

=--

In other words, $N Cocycle(X,A) \simeq_{whe} N wCocycle(X,A)$ is a model for the correct [[derived hom space]].

From this it follows for instance that 

+-- {: .num_prop #PullbacksAlongFibrationsAreCorrectHomotopyPullbacks}
###### Proposition

The [[homotopy fiber products]] in $\mathcal{C}$ as defined in def. \ref{HomotopyFiberProducts} present indeed the correct [[(infinity,1)-limits]]. 

=--

+-- {: .proof}
###### Proof

Observe that for each object $X$ the 2-functor $N Cocycle(X,-) \colon \mathcal{C} \to sSet$ of def. \ref{CocycleCategories} sends fibrations
to [[Kan fibrations]] of simplicial sets (the [[horn]]-filling condition comes down to factoring maps through the given fibration, which is possible by pullback along the fibration). Moreover, it is evident that $N Cocycle(X,-)$ preserves ordinary [[pullbacks]]. This means that $N Cocycle(X,-)$ takes pullbacks along a fibration in $\mathcal{C}$ to pullbacks in [[sSet]] one of whose maps is a [[Kan fibration]]. Since the standard [[model structure on simplicial sets]] $sSet_{Quillen}$ is a [[right proper model category]], this means that these are [[homotopy pullbacks]] (as discussed there) in $sSet_{Quillen}$. Finally by prop. \ref{CocycleCategoriesPresentDerivedHomSpaces} this means that the [[derived hom-space]] functor $\mathbb{R}Hom(X,-)$ sends pullbacks along fibrations to [[homotopy pullbacks]] of the correct derived hom-spaces. This means (as discussed for instance at _[[homotopy Kan extension]]_) that the original pullbacks in $\mathcal{C}$ are the correct homotopy pullbacks.

=--

## Application in cohomology theory 

When the catgegory of fibrant objects is that of locally Kan simplicial sheaves, the [[hom-set]]s of its 
[[homotopy category]] compute generalized notions of [[cohomology]].

At [[abelian sheaf cohomology]] is a detailed discussion of how the ordinary notion of sheaf cohomology arises as a special case of that.

## Related concept

* [[category of cofibrant objects]]

* [[Waldhausen category]]

* [[model category]]


## References

The notion of _category of fibrant objects_ was introduced and the above results obtained in

* [[Kenneth Brown]], _[[BrownAbstractHomotopyTheory.pdf:file]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458 ([[BrownAHT]]).

for application to [[homotopical cohomology theory]].

A review is in [section I.9](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi) of 

* [[Paul Goerss]] and [[Rick Jardine]], 1999, _[[Simplicial homotopy theory]]_, number 174 in Progress in Mathematics, Birkhauser. ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

There is a description and discussion of this theory and its dual (using cofibrant objects) in

* [[K. H. Kamps]] and [[Tim Porter]], _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

Discussion of embeddings of categories of fibrant objects into model categories is in 

* {#Cisinski10} [[Denis-Charles Cisinski]], _Invariance de la K-Th&#233;orie
par &#233;quivalences d&#233;riv&#233;es_ ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/eqderkth.pdf))
 

Also discussion of the [[derived hom spaces]] in categories of fibrant objects is in that article, as well as in section 6.3.2 of


* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_ ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249))

and also in

* [[Geoffroy Horel]], *Brown categories and bicategories*, [arxiv](https://arxiv.org/abs/1506.02851)


Usage of categories of fibrant objects for the [[homotopical structure on C*-algebras]] is in :

* [[Otgonbayar Uuye]], _Homotopy theory for $C^\ast$-algebras_,  Journal of Noncommutative Geometry, ([arxiv:1011.2926](http://arxiv.org/abs/1011.2926))

Categories of fibrant objects form a convenient setting for the study of [[homotopy type theory]]:

* Jeremy Avigad, Chris Kapulkin, Peter LeFanu Lumsdaine, _Homotopy limits in type theory_ [1304.0680](http://arxiv.org/abs/1304.0680)

It is shown in the following paper that categories of fibrant objects are themselves fibrant in the [[model structure on categories with weak equivalences]]:

* Lennart Meier, *Fibration Categories are Fibrant Relative Categories*, [arxiv](https://arxiv.org/abs/1503.02036)
 {#Meier}


[[!redirects categories of fibrant objects]]