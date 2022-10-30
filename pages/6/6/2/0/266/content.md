+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


##Idea

The _Kan extension_ of a [[functor]]
$F : C \to D$ with respect to a functor
$$
 \array{
  C
  \\
  \downarrow^p
  \\
  C'
 }
$$

is, if it exists, a kind of _best approximation_ to 
the problem of finding a functor $C' \to D$ such that 
$$
  \array{
     C &\stackrel{F}{\to}& D
     \\
     \downarrow^p & \nearrow
     \\
     C'
  }
  \,,
$$

hence to extending the [[domain]] of $F$ through $p$ from $C$ to $C'$.

More generally, this makes sense not only in [[Cat]] but in any [[2-category]].

Similarly, a [[Kan lift]] is the best approximation to lifting a morphism $F : C \to D$ through a morphism

$$
  \array{
    D'
    \\
    \downarrow
    \\
    D
  }
$$

to a morphism $\hat F$

$$
  \array{
    && D'
    \\
    & {}^{\hat F}\nearrow & \downarrow
    \\
    C &\stackrel{F}{\to}& D
  }
  \,.
$$

Kan extensions are ubiquitous. See the discussion at _[Examples](#Examples)_ below.


## Definitions
 {#Definitions}

There are various slight variants of the definition of _Kan extension_ . In good cases they all exist and all coincide, but in some cases only some of these will actually exist.

We (have to) distinguish the following cases:

1. ["ordinary" or "weak" Kan extensions](#OrdinaryKanExtensions) 

   These define the extension of an entire functor, by an [[adjunct|adjointness]] relation. 

   Here we (have to) distinguish further between

   1. [global Kan extensions](#GlobalKanExtensions),

      which define extensions of _all_ possible functors of given domain and codomain (if all of them indeed exist);

   1. [local Kan extensions](#LocalKanExtensions),

      which define extensions of single functors only, which may exist even if not every functor has an extension.

1. ["pointwise" or "strong" Kan extensions](#Pointwise)

   These define the _value_ of an extended functor on each object (each "point") by a [[weighted limit|weighted (co)limit]]. 

   Furthermore, a pointwise Kan extension can be ["absolute"](#AbsoluteKanExtension).

If the pointwise version exists, then it coincides with the "ordinary" or "weak" version, but the former may exist without the pointwise version existing. See [below](#pointwiseVsWeak) for more.

Some authors (such as [Kelly](Kelly)) assert that only pointwise Kan extensions deserve the name "Kan extension," and use the term as 
"weak Kan extension" for a functor equipped with a universal natural transformation.  It is certainly true that most Kan extensions which arise in practice are pointwise.  This distinction is even more important in [[enriched category]] theory.


### Ordinary or weak Kan extensions 
 {#OrdinaryKanExtensions}


#### Global Kan extensions
 {#GlobalKanExtensions}


Let 

$$
  p : C \to C'
$$ 

be a [[functor]]. For $D$ any other category, write

$$
  p^* : [C',D] \to [C,D]
$$

for the induced functor on the [[functor categories]]: this sends a functor $h : C' \to D$ to the composite functor $p^* h : C \stackrel{p}{\to} C' \stackrel{h}{\to} D$.


+-- {: .num_defn}
###### Definition

If $p^*$ has a [[left adjoint]], typically denoted

$$
  p_! : [C,D] \to [C',D]
$$

or 

$$
  Lan_p : [C,D] \to [C',D]
$$

then this left adjoint is called the ( _ordinary_ or _weak_ ) **left Kan extension** operation along $p$. For $h \in [C,D]$ we call $p_! h$ the **left Kan extension of $h$** along $p$.

Similarly, if $p^*$ has a [[right adjoint]], this right adjoint is called the **right Kan extension** operation along $p$. It is typically denoted

$$
  p_* : [C,D] \to [C',D]
$$

or 

$$
  Ran = Ran_p: [C,D] \to [C',D]
  \,.
$$

=--

The analogous definition clearly makes sense as stated in other contexts, such as in [[enriched category theory]].  

+-- {: .num_prop}
###### Observation

If $C' = *$ is the [[terminal category]], then

* the left Kan extension operation forms the [[colimit]] of a functor;

* the right Kan extension operation forms the [[limit]] of a functor.

=--

+-- {: .proof}
###### Proof

The functor $p^*$ in this case sends objects $d$ of $D$ to the [[constant functor]] $\Delta_d$ on $d$. Notice that for $F \in [C,D]$ any functor, 

* a [[natural transformation]] $\Delta_d \to F$ is the same as a [[cone]] over $F$;

* a [[natural transformation]] $F \to \Delta_d$ is the same as a [[cocone]] under $F$.

Therefore the natural hom-isomorphisms of the [[adjoint functor]]s 
$(p_! \dashv p^*)$ and $(p^* \dashv p_*)$ 

$$
  D(d, p_* F) \simeq Func(\Delta_d, F)
$$

and

$$
  D(p_! F, d) \simeq Func(F, \Delta_d)
$$

assert that

* $p_* F$ corepresents the [[cone]]s over $F$: this means by definition that $p_* F = \lim_\leftarrow F$ is the [[limit]] over $F$;

* $p_! F$ represents the [[cocone]]s under $F$: this means by definition that $p_! F = \lim_\to F$ is the [[colimit]] of $F$.

=--


#### Local Kan extension
 {#LocalKanExtensions}

There is also a *local* definition of "the Kan extension of a given functor $F$ along $p$" which can exist even if the entire functor defined above does not.  This is a generalization of the fact that a *particular* diagram of shape $C$ can have a limit even if not every such diagram does.  It is also a special case of the fact discussed at [[adjoint functor]] that an adjoint functor can fail to exist completely, but may still be partially defined.  If the local Kan extension of every single functor exists for some given $p\colon C\to C'$ and $D$, then these local Kan extensions fit together to define a functor which is the global Kan extension.


Thus, by the general notion of "partial adjoints"; we say

+-- {: .num_defn #LocalKanExtension}
###### Definition

The local **left Kan extension** of  a functor $F\in [C,D]$ along $p : C \to C'$ is, if it exists, a functor

$$
  Lan_p\,F : C'\to D
$$ 

equipped with a [[natural isomorphism]]

$$
  Hom_{[C,D]}(F,p^*(-))\cong Hom_{[C',D]}(Lan_p\,F,-)
  \,,
$$

hence a [[representable functor|(co)representation]] of the functor $Hom_{[C,D]}(F,p^*(-))$.  

The local definition of right Kan extensions along $p$ is dual.

=--


As for adjoints and limits, by the usual logic of representable functors this can equivalently be rephrased in terms of 
<a href="http://ncatlab.org/nlab/show/adjoint%20functor#UniversalArrows">universal morphisms</a>:

+-- {: .num_defn}
###### Definition

The **left Kan extension $Lan F = Lan_p F$ of $F : C \to D$ along 
$p :C\to C'$ is a functor $Lan F : C' \to D$ equipped with a [[natural transformation]] $\eta_F : F \Rightarrow p^* Lan F$. 

<center markdown="1">[[kan-0.png:pic]]</center>

with the property that every other natural transformation
$F \Rightarrow p^* G$ factors uniquely through $\eta_F$ as

<center markdown="1">[[kan-1.png:pic]]</center>

Similarly for the right Kan extension, with the direction of the natural transformations reversed:

<center markdown="1">[[kan-2.png:pic]]</center>

=--

By the usual reasoning (see e.g. [[Categories Work]], chapter IV, theorem 2), if these representations exist for every $F$ then they can be organised into a left (right) adjoint $Lan_p$ ($Ran_p$) to $p^*$.

+-- {: .num_remark #InHigherCats}
###### Remark

The definition in this form makes sense not just in [[Cat]] but in every [[2-category]]. In slightly different terminology, the left Kan extension of a 1-cell $F:C\to D$ along a 1-cell $p\in K(C,C')$ in a 2-category $K$ is a pair $(Lan_p F,\alpha)$ where $\alpha : F\to Lan_p F\circ p$ is a 2-cell which [[reflections|reflects]] the object $F\in K(C,D)$ along the functor $p^* = K(p,D):K(C',D)\to K(C,D)$.  Equivalently, it is such a pair such that for every $G\colon C' \to D$, the function
$$ K(C',D)(Lan_p F, G) \xrightarrow{- \cdot \alpha} K(C,D)(F, G \circ p) $$
is a [[bijection]].

In this form, the definition generalizes easily to any [[n-category]] for any $n\ge 2$.  If $K$ is an $n$-category, we say that the left Kan extension of a 1-morphism $F:C\to D$ along a 1-morphism $p\in K(C,C')$ is a pair $(Lan_p F,\alpha)$, where $Lan_p F \colon C' \to D$ is a 1-morphism and $\alpha : F\to Lan_p F\circ p$ is a 2-morphism, with the property that for any 1-morphism $G\colon C'\to D$, the induced functor
$$ K(C',D)(Lan_p F, G) \xrightarrow{- \cdot \alpha} K(C,D)(F, G \circ p) $$
is an [[equivalence]] of $(n-2)$-categories.

=--

### Preservation of Kan extensions
{#Preservation}

We say that a Kan extension $Lan_p F$ is *preserved* by a functor $G$ if the composite $G \circ Lan_p F$ is a Kan extension of $G F$ along $p$, and moreover the universal natural transformation $G F \to G(Lan_p F)p$ is the composite of $G$ with the universal transformation $F\to (Lan_p F)p$.

### Pointwise or strong Kan extensions 
 {#Pointwise}

If the [[codomain]] category $D$ admits certain [[limit|(co)limits]], then left and right Kan extensions can be constructed, over each object ("point") of the domain category $C'$ out of these: Kan extensions that admit this form are called _pointwise_. (Reviews include ([Riehl, I 1.3](#Riehl))).

The notion of pointwise Kan extensions deserves to be discussed in the general context of [[enriched category theory]], which we do below. The reader may want to skip ahead to the section

* [pointwise Kan extensions by conical (co)limits](#PointwiseByConicalLimits)

which discusses the situation in ordinary ([[Set]]-[[enriched category|enriched]]) [[category theory]] in terms of ordinary limits ("conical" limits, defined in terms of [[cone]]s, to be distinguished from the more general [[weighted limit]]s). While the formulas in that case are classical and fundamentally useful in practice, they do rely heavily on special properties of the enriching category [[Set]].

The general formulation of pointwise Kan extensions in general enriched contexts is

* [in terms of weighted (co)limits](#PointwiseByWeightedColimits).

In the case that the codomain category is [[tensoring|(co)tensored]] these may be expressed equivalently

* [in terms of (co)ends](#PointwiseByCoEnds).

First, here is a characterization that doesn't rely on any computational framework:

+-- {: .num_defn}
###### Definition

A Kan extension, def. \ref{LocalKanExtension}, is called __pointwise__ if and only if it is [preserved](#Preservation) by all [[representable functor]]s.

=--

([[Categories Work]], theorem X.5.3)


#### in terms of weighted (co)limits 
 {#PointwiseByWeightedColimits}

Suppose given $F : C \to D$ and $p : C \to C'$ such that for every $c' \in C'$, the [[weighted limit]]

$$
  (Ran_p F)(c') \coloneqq lim^{C'(c',p(-))} F
  \,.
$$

exists.  Then these objects fit together into a functor $Ran_p F$ which is a right Kan extension of $F$ along $p$.  Dually, if the [[weighted limit|weighted colimit]]
$$
  (Lan_p F)(c') \coloneqq colim^{C'(p(-),c')} F
  \,.
$$
exists for all $c'$, then they fit together into a left Kan extension $Lan_p F$.  These definitions evidently make sense in the generality of $V$-[[enriched category theory]] for $V$ a [[closed monoidal category|closed]] [[symmetric monoidal category]].  (In fact, they can be modified slightly to make sense in the full generality of a [[2-category equipped with proarrows]].)

In particular, this means that if $C$ is [[small category|small]] and $D$ is [[complete category|complete]] (resp. cocomplete), then all right (resp. left) Kan extensions of functors $F\colon C\to D$ exist along any functor $p\colon C\to C'$.

One can prove that any Kan extension constructed in this way must be pointwise, in the sense of being preserved by all representables as above.  Moreover, conversely, if a Kan extension $Lan_p F$ is pointwise, then one can prove that $(Lan_p F)(c')$ must be in fact a $C'(p(-),c')$-weighted colimit of $F$, and dually; thus the two notions are equivalent.


#### in terms of (co)ends 
 {#PointwiseByCoEnds}

If the $V$-[[enriched category]] $D$ is [[power]]ed over $V$, then the above weighted limit may be re-expressed in terms of an [[end]] as

$$
  (Ran_p F)(c') \simeq \int_{c \in C} C'(c',p(c))\pitchfork F(c)
  \,.
$$

So in particular when $D = V$ this is

\[
  \label{RightKanExtensionViaEndFormula}
  (Ran_p F)(c') \simeq \int_{c \in C} [C'(c',p(c)),F(c)]
  \,.
\]

([Kelly (4.24)](#Kelly))


Similarly, if $D$ is [[copower|tensored]] over $V$, then the left Kan extension is given by a [[coend]].

\[
  \label{LeftKanExtensionViaCoendFormula}
  (Lan_p F)(c') \simeq \int^{c \in C} C'(p(c),c')\otimes F(c)
  \,.
\]

([Kelly (4.25)](#Kelly))


+-- {: .num_example #CoendFormulaForPresheavesOfSets}
###### Example
**(coend formula for left Kan extension of presheaves)**

The coend formula for the  left Kan extension is nicely understood when thinking of $C$ and $D$ above as [[opposite categories]] and for $\mathcal{V} = Set$, so that it takes [[presheaves]] $F$ on $C$ along $p \colon C \to C'$ to presheaves $Lan_p F$ on $C'$, by the formula

$$
  (Lan_p F)(c') \simeq \int^{c \in C} C'(c', p(c)) \times F(c)
  \,.
$$

Using the [[Yoneda lemma]] to rewrite $F(c) \simeq Hom_{PSh(C)}(c,F)$, this is

$$
  (Lan_p F)(c') \simeq \int^{c \in C} Hom_{C'}(c', p(c)) \times Hom_{PSh(C)}(c,F)
  \,.
$$

In this form one sees that the coend produces the set whose elements are [[equivalence classes]] of pairs of morphisms

$$
   (c' \to p(c), c \to F)
$$

where two such are regarded as equivalent whenever there is $f \colon c_1 \to c_2$ such that 

$$
  \array{
    && c'
    \\
    & \swarrow && \searrow
    \\
    p(c_1) && \stackrel{p(f)}{\longrightarrow} && p(c_2)
    \\
    c_1 && \stackrel{f}{\longrightarrow} && c_2
    \\
    & \searrow && \swarrow
    \\
    && F
  }
  \,.
$$

This is particularly suggestive in cases when we may think of the objects of $C$ and $C'$ on the same footing, notably when $p$ is a [[full subcategory]] inclusion. For in that case we may imagine that a representative pair $(c' \to p(c), c \to F)$ is a stand-in for the actual pullback of elements of $F$ via forming the composite "$c'\to c \to F$", only that this composite is not defined. But the above equivalence relation is precisely that under which this composite would be invariant.


=--



#### in terms of conical (co)limits
 {#PointwiseByConicalLimits}

In the case of functors between ordinary [[locally small categories]], hence in the special case of $V$-[[enriched category theory]] for $V = $ [[Set]], there is an expression of a weighted (co)limit and hence a pointwise Kan extension as an ordinary ("conical", meaning: in terms of [[cone]]s) (co)limit over a [[comma category]]:

+-- {: .num_prop}
###### Proposition

Let 

* $C$ be a [[small category]];

* $D$ have all small [[limit]]s.

Then the right Kan extension of a functor $F : C \to D$ of locally small categories along a functor $p : C \to C'$ exists 
and its value on an object $c' \in C'$ is given by the [[limit]]

$$
    (Ran_p F)(c')
      \simeq 
    \lim_\leftarrow \left((\Delta_{c'}/p) \to C \stackrel{F}{\to} D\right)
  \,,
$$

where 

* $\Delta_{c'}/p$ is the [[comma category]];

* $\Delta_{c'}/p \to C$ is the canonical [[forgetful functor]].

Likewise, if $D$ admits small [[colimit]]s, 
the left Kan extension of a functor exists and is pointwise given by the [[colimit]]

$$
    (Lan_p F)(c')
      \simeq 
     \lim_\to \left((p/\Delta_{c'}) \to C \stackrel{F}{\to} D\right)
  \,.
$$

=--

This appears for instance as ([Borceux, I, thm 3.7.2](#Borceux)).
Discussion in the context of [[enriched category theory]] is in ([Kelly, section 3.4](#Kelly)).

A cartoon picture of the forgetful functor out of the [[comma category]] $p/\Delta_{c'} \to C$, useful to keep in mind, is

$$
  \left(
    \array{
      p(c_1) &&\stackrel{p(\phi)}{\to}&& p(c_2)
      \\
      & \searrow && \swarrow
      \\
      &&  c'
    }
  \right)
   \;\;
   \mapsto
   \;\;
  \left(
    c_1 \stackrel{\phi}{\to} c_2
  \right)
  \,.
$$

The [[comma category]] here is equivalently the [[category of elements]] of the functor $C'(p(-), c') : C^{op} \to Set$

$$
  (p/\Delta_{c'}) \simeq el( C'(p(-), c') )
  \,.
$$

+-- {: .proof}
###### Proof

Consider the case of the left Kan extension, the other case works analogously, but dually.

First notice that the above pointwise definition of values of a functor canonically extends to an actual functor:

for $\phi : c'_1 \to c'_2$ any morphism in $C'$ we get a functor

$$
  \phi_* : p/\Delta_{c'_1} \to p/\Delta_{c'_2}
$$

of comma categories, by postcomposition. This morphism of [[diagram]]s induces canonically a corresponding morphism of [[colimit]]s

$$
  (Lan_p F)(c'_1) \to (Lan_p F)(c'_2)
  \,.
$$

Now for the universal property of the functor $Lan_p F$ defined  this way. For $c' \in C'$ denote the components of the colimiting [[cocone]] $(Lan_p F)(c') := \lim_{\to}( p/\Delta_{c'} \to C \stackrel{F}{\to} D) $ by $s_{(-)}$, as in

$$
  \array{
   (p(c_1)\stackrel{\phi}{\to} c') 
      &&\stackrel{p(h)}{\to}&& 
   (p(c_2)\stackrel{\lambda}{\to} c')
    \\
    \\
    \\
    F(c_1) &&\stackrel{F(h)}{\to}&& F(c_2)
    \\
    & {}_{\mathllap{s_\phi}}\searrow && \swarrow_{\mathrlap{s_{\lambda}}}
    \\
    && (Lan_p F)(c')
  }
  \,.
$$

We now construct in components a natural transformation

$$
  \eta_F : F \to p^* Lan_p F
$$

for $Lan_p F$ defined as above, and show that it satisfies the required universal property.
The components of $\eta_F$ over $c \in C$ are morphisms

$$
  \eta_F(c) : F(c) \to (Lan_p F)(p (c))
  \,.
$$

Take these to be given by 

$$

  \eta_F(c) := s_{Id_{p(c)}}
$$

(this is similar to what happens in the proof of the [[Yoneda lemma]], all of these arguments are variants of the argument for the Yoneda lemma, and vice versa). It is straightforward, if somewhat tedious, to check that these are natural, and that the natural transformation defined this way has the required universal property.

=--

#### Comparing the definitions   {#pointwiseVsWeak}

We have seen that if $D$ has enough limits or colimits, then a pointwise Kan extension can be defined in terms of these limits, and will necessarily satisfy the universal property described first.  However, not all Kan extensions are pointwise: that is, having a universal transformation $F \to (Lan_p F)p$ does not necessarily imply that the individual values of $Lan_p F$ are limits or colimits in its codomain.  Non-pointwise Kan extensions can exist even when $D$ does not admit very many limits.

It should be noted, though, that pointwise Kan extensions can still exist, and hence the particular requisite limits/colimits exist, even if $D$ is not (co)complete.  For instance, the Kan extensions that arise in the study of [[derived functor]]s are pointwise, and in fact [[absolute colimit|absolute]] (preserved by *all* functors), even though their codomains are [[homotopy categories]] which generally do not admit all limits and colimits.

Non-pointwise Kan extensions seem to be very rare in practice.  However, the abstract notion of Kan extension (sometimes called simply "extension") in a 2-category, and its dual notion of lifting, can be useful in [[2-category theory]].  For instance, [[bicategories]] such as [[Prof]] admit all right extensions and right liftings; a bicategory with this property may be considered a [[horizontal categorification]] of a [[closed monoidal category]].


### Absolute Kan extensions
  {#AbsoluteKanExtension}

An _absolute_ Kan extension $Lan_p F$ is one which is [preserved](#Preservation) by all functors $G$ out of the codomain of $F$:
\[
G (Lan_p F) \simeq Lan_p(G F)
\]
(same for right Kan extensions).

The most prominent example of absolute Kan extensions is given by [[adjoint functor|adjoint functors]]; in fact they can be defined as certain absolute Kan extensions. See there for the precise statement.

#### absolute vs pointwise

Absolute Kan extensions are always pointwise, as the latter can be defined as those preserved by representables; there are (lots of) examples of pointwise Kan extensions which are not absolute.

Note that in a general 2-category, absolute Kan extensions make perfect sense, while for defining pointwise ones more structure is needed: [[comma object|comma objects]] and/or some structure which would let us work with (co)limits _inside_ that 2-category (such as a [[Yoneda structure|(co)Yoneda structure]] or a [[2-category equipped with proarrows|proarrow equipment]]).


### Of $(\infty,1)$-functors

The global definition of Kan extensions for
functors in terms of left/right adjoints to pullbacks may be interpreted essentially verbatim in the context of [[(∞,1)-categories]] 

See at _[[(∞,1)-Kan extension]]_.

### In a general 2-category
  {#In2cat}

The Kan extension of a functor may be regarded more abstractly as an extension-problem in the [[2-category]] [[Cat]] of categories. The same extension problem can be stated verbatim in any [[2-category]] and hence there is a corresponding more general notion of Kan extensions of [[1-morphisms]] in [[2-categories]].  This is discussed in ([Lack 09, section 2.2](#Lack09)).

The question of defining a *pointwise* Kan extension in a general 2-category is more subtle, and there are at least two distinct approaches.  If the 2-category has [[comma objects]], then we can define a Kan extension to be pointwise if it remains a Kan extension upon pasting with any comma object; this is an "internalization" of the above definition in terms of *conical* colimits.  On the other hand, in a [[2-category equipped with proarrows]] we can define pointwise Kan extensions as particular weighted (co)limits using a representable weight; this generalizes the above definition as a weighted (co)limit.

In some 2-categories such as $Cat$, both definitions agree; but in others they do not, and in general in this case it is the equipment-theoretic version that is "correct".  For instance, in $V Cat$ the equipment-theoretic version gives the right notion of pointwise Kan extension, whereas the comma-object one is too strong.

As a concrete example, let $V=Cat$, so that $V Cat = 2 Cat$; then comma objects are not informative enough because they "don't see the 2-cells".  In even more specificity, let $B$ be the [[walking]] 2-cell and $M$ the walking pair of parallel 1-morphisms, with $f:1\to B$ and $g:1\to M$ the inclusions of the common domain of the parallel 1-morphisms; then the equipment-theoretic-pointwise $Lan_f g$ is constant at the domain object, whereas the comma-object-pointwise $Lan_f g$ does not exist.  See [(Roald, Example 2.24)](#Roald13) for details.


## Existence

The following reproduces a [MathOverflow answer](https://mathoverflow.net/questions/365947/when-size-matters-in-category-theory-for-the-working-mathematician/365951#365951) by [[Ivan Di Liberti]]:

\begin{lemma}
(Kan).
Let $\mathsf{B} \stackrel{f}{\leftarrow} \mathsf{A} \stackrel{g}{\to} \mathsf{C}$ be a [[span]] where $\mathsf{A}$ is [[small category|small]] and $\mathsf{C}$ is (small) [[cocomplete category|cocomplete]]. Then the [[left Kan extension]] $\mathsf{lan}_f g$ exists.
\end{lemma}

Kan extensions are a useful tool in everyday practice, with applications in many different topics of [[category theory]]. In this lemma (which is one of the most used in this topic) the set-theoretic issue is far from being hidden: **$\mathsf{A}$ needs to be small (with respect to $Ob(\mathsf{C})$!** There is no chance that the lemma is true when $\mathsf{A}$ is a [[large category]]. Indeed since [[colimits]] can be computed via Kan extensions, the lemma would imply that every (small) [[cocomplete category]] is large cocomplete, which is not allowed because [cocomplete small categories are posets](complete+small+category#CompleteSmallCategoriesArePosets). Also, there is no chance to solve the problem by saying: *well, let's just consider $\mathsf{C}$ to be large-cocomplete*, again because [cocomplete small categories are posets](complete+small+category#CompleteSmallCategoriesArePosets).

This problem is hard to avoid because the size of the categories of our interest is *as a fact* always larger than the size of their inhabitants (this just means that most of the time **Ob**$\mathsf{C}$ is a [[proper class]], as big as the size of the [[enriched category|enrichment]]).

Notice that the Kan extension problem **recovers the [[adjoint functor theorem]] one,** because adjoints are computed via Kan extensions of identities of large categories. Indeed, in that case, the [[solution set condition]] is precisely what is needed in order to cut down the size of some colimits that otherwise would be too large to compute, as can be synthesized by the sharp version of the Kan lemma.

\begin{lemma}
**Sharp Kan lemma.**
Let $\mathsf{B} \stackrel{f}{\leftarrow} \mathsf{A} \stackrel{g}{\to} \mathsf{C}$ be a span where $\mathsf{B}(f-,b)$ is a small presheaf for every $b \in \mathsf{B}$ and $\mathsf{C}$ is (small) cocomplete. Then the left Kan extension $\mathsf{lan}_f g$ exists.
\end{lemma}

Indeed this lemma allows $\mathsf{A}$ to be large, but we must pay a tribute to its presheaf category: $f$ needs to be somehow *locally small* (with respect to **Ob**$\mathsf{C}$).

\begin{lemma}
**Kan lemma Fortissimo.**
Let $ \mathsf{A} \stackrel{f}{\to} \mathsf{B} $ be a functor. The following are equivalent:

* for every $g :\mathsf{A} \to \mathsf{C}$ where $\mathsf{C}$ is a small-cocomplete category, $\mathsf{lan}_f g$ exists.
* $\mathsf{lan}_f y$ exists, where $y$ is the Yoneda embedding in the category of small presheaves $y: \mathsf{A} \to \mathcal{P}(\mathsf{A})$.
* $\mathsf{B}(f-,b)$ is a is small presheaf for every $b \in \mathsf{B}$.

\end{lemma}

Even unconsciously, the previous discussion is one of the reasons of the popularity of [[locally presentable categories]]. Indeed, having a dense generator is a good compromise between *generality and tameness*. As an evidence of this, in the context of [[accessible categories]] the sharp Kan lemma can be simplified.

\begin{lemma}
**Tame Kan lemma.**
Let $\mathsf{B} \stackrel{f}{\leftarrow} \mathsf{A} \stackrel{g}{\to} \mathsf{C}$ be a span of accessible categories, where $f$ is an accessible functor and $\mathsf{C}$ is (small) cocomplete. Then the left Kan extension $\mathsf{lan}_f g$ exists.
\end{lemma}

*References for Sharp.* I am not aware of a reference for this result. It can follow from a careful analysis of **Prop. A.7** in my paper **Codensity: Isbell duality, pro-objects, compactness and accessibility**. The structure of the proof remains the same, presheaves must be replaced by small presheaves.

*References for Tame.* This is an exercise, it can follow directly from the sharp Kan lemma, but it's enough to properly combine the usual Kan lemma, **Prop A.1&2** of the above-mentioned paper, and the fact that [[accessible functors]] have arity.


## Properties
  {#Properties}

### Left Kan extension on representables / fully faithfulness
 {#LeftKanOnRepresentables}

Let $\mathcal{V}$ be a suitable enriching category (a [[cosmos]]). Notably $\mathcal{V}$ may be [[Set]].

+-- {: .num_prop #LeftKanExtensionBasicProp}
###### Proposition

For $F : C \to D$ a $\mathcal{V}$-[[enriched functor]] between [[small category|small]] $\mathcal{V}$-[[enriched categories]] we have

1. the left Kan extension along $F$ takes [[representable functor|representable]] [[presheaves]] $C(c,-) : C \to \mathcal{V}$ to their image under $F$:

   $$
     Lan_F C(c, -) \simeq D(F(c), -)
   $$

   for all $c \in C$.

1. if $F$ is a [[full and faithful functor]] then 
   $F^* (Lan_F H) \simeq H$ and in fact the $(Lan_F \dashv F^*)$-[[unit of an adjunction]] is a [[natural isomorphism]]

   $$
      Id \stackrel{\simeq}{\to} F^* \circ Lan_{F}
   $$ 

   whence it follows (by [this property](adjoint+functor#FullyFaithfulAndInvertibleAdjoints) of [[adjoint functor]]s) that $Lan_F : [C,\mathcal{V}] \to [D,\mathcal{V}]$ is itself a [[full and faithful functor]].

=-- 

The second statement appears for instance as ([Kelly, prop. 4.23](#Kelly)).

+-- {: .proof}
###### Proof

For the first statement, using the [[coend]] formula for the left Kan extension [above](#PointwiseByCoEnds) we have naturally in $d' \in D$ the expression

$$
  \begin{aligned}
    Lan_F C(c,-) : 
    d' \mapsto 
     & 
    \int^{c' \in C} D(F(c'), d') \cdot C(c,-)(c')
    \\
    & \simeq
    \int^{c' \in C} D(F(c'), d') \cdot C(c,c')
    \\
    & \simeq 
    D(F(c), d')
  \end{aligned} 
  \,.
$$

Here the last step is called sometimes the [[co-Yoneda lemma]]. It follows for instance by observing that $\int^{c' \in C} D(F(c'), d') \cdot C(c,c')$ is equivalently dually the expression for the left Kan extension of the non-representable $D(F(-),d') : C^{op} \to \mathcal{V}$ along the _identity_ functor.

Similarly for the second, if $H : D \to E$ is any $\mathcal{V}$-[[enriched functor]] with $E$ [[tensoring|tensored]] over $\mathcal{V}$, then its left Kan extension evaluated on the image of $F$ is

$$
  \begin{aligned}
    Lan_F H : F(d) \mapsto
     & \int^{c \in C} D(F(c), F(d)) \cdot H(c) 
     \\
     & \simeq 
     \int^{c \in C} C(c, d) \cdot H(c)
     \\
     & \simeq H(d)
  \end{aligned}
  \,.
$$

=--

### Left Kan extensions preserving certain limits
 {#LeftKanExtensionPreservingCertainLimits}

The following statement says that [[left exact functors]] into [[toposes]] have left exact left Kan extension along the [[Yoneda embedding]] ([[Yoneda extension]]) and that this is the [[inverse image]] of a [[geometric morphism]] of [[sheaf toposes]] if the original functor preserves [[covers]].

(We state this in [[(∞,1)-category theory]], the same statement holds true in plain [[category theory]] by just disregarding all occurences of "$\infty$".)

+-- {: .num_prop #YonedaExtensionOfLeftExact}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and let $\mathcal{C}$ be an [[(∞,1)-site]] with [[(∞,1)-sheaf (∞,1)-category]] $Sh(\mathcal{C})$. Then the [[(∞,1)-functor]]

$$
  Top(\mathcal{X}, Sh(\mathcal{C}))
  \simeq
  Func^{lex, leftadj}(Sh(\mathcal{C}), \mathcal{X})
  \stackrel{(-)\circ L }{\longrightarrow}
  Func(PSh(\mathcal{C}), \mathcal{X})
  \stackrel{(-)\circ Y }{\longrightarrow}
  Func(\mathcal{C}, \mathcal{X})
$$

given by precomposition with [[∞-stackification]]/[[sheafification]] $L$ and with the [[(∞,1)-Yoneda embedding]] $Y$ is a [[full and faithful (∞,1)-functor]]. Moreover, its [[essential image]] consisist of those [[(∞,1)-functors]] $f \colon \mathcal{C} \longrightarrow \mathcal{X}$ which are [[left exact (∞,1)-functor|left exact]] and which preserve covers in that for $\{U_i \to X\}_i$ a [[covering]] in $\mathcal{C}$, then $\coprod_i f(U_i) \to f(X)$ is an [[effective epimorphism]] in $\mathcal{X}$.

=--

This appears as [[Higher Topos Theory|Lurie, HTT, prop. 6.2.3.20]].

+-- {: .num_remark }
###### Remark

Prop. \ref{YonedaExtensionOfLeftExact} is a central statement in the theory of [[classifying toposes]]. See there for more.

=--

For more discussion of left exactness properties preserved by left Kan extension see also ([Borceux-Day](#BorceuxDay), [Karazeris-Protsonis](#KarazerisProtsonis)).

### Kan extension along (op)fibration
 {#AlongFibrations}

+-- {: .num_prop}
###### Proposition

Let $f : C \to D$ be a small [[opfibration]] of categories, and let $\mathcal{C}$ be a category with all small [[colimits]]. Then for each $d \in D$ the inclusion

$$
  f^{-1}(d) \to f/d
$$

of the [[fiber]] over $d$ into the [[comma category]] given by

$$
  c \mapsto (c, Id_{d} = Id_{f(c)})
$$

has a [[left adjoint]]. given by

$$
  (c, f(c) \to d) \mapsto c'
  \,,
$$

where $c \to c'$ is a coCartesian lift of $f(c) \to d$.
 
Therefore (by the discussion _[here](final+functor#Examples)_) it is a [[cofinal functor]]. Accordingly, the local formula for the left Kan extension 

$$
  f_! : [C, \mathcal{D}] \to [D, \mathcal{D}]
$$

is equivalently given by taking the colimit over the [[fiber]]:

$$
  f_! X : d \mapsto \lim_{\underset{f^{-1}(d)}{\to}} X
  \,.
$$

=--

A similar result holds for $(\infty,1)$-categories.
See [[Higher Topos Theory|Lurie, HTT, prop. 4.3.3.10]], set $S=Y$ and $q = \id_Y$.

## Examples
 {#Examples}

The central point about examples of Kan extensions is:

_Kan extensions are ubiquitous_ . 

To a fair extent, [[category theory]] is all about Kan extensions and the other [[universal construction]]s: [[limit]]s, [[adjoint functor]]s, [[representable functor]]s, which are all special cases of Kan extensions -- and Kan extensions are special cases of these.

Listing examples of Kan extensions in [[category theory]] is much like listing examples of [[integral]]s in [[analysis]]: one can and does fill books with these. (In fact, that analogy has more to it than meets the casual eye: see [[coend]] for more).


Keeping that in mind, we do list some special cases and special classes of examples that are useful to know. But any list is necessarily wildly incomplete.

### General

* For $C' = $ the [[point]], the right Kan extension of $F$ is the [[limit]] of $F$, $Ran F \simeq \lim F$ and the left Kan extension is the [[colimit]] $Lan F \simeq colim F$.

* For $f : X \to Y$ a [[site|morphism of sites]] coming from a functor $f^t : S_Y \to S_X$ of the underlying categories, the left Kan extension of functors along $f^t$ is the [[inverse image]] operation $f^{-1} : PSh(Y) \to PSh(X)$.

* see also [[examples of Kan extensions]]

### Non-pointwise Kan extensions

Examples of Kan extensions that are not point-wise are discussed in [Borceux, exercise 3.9.7](#Borceux).

### Restriction and extension of sheaves 

For more on the following see also 

* [[restriction and extension of sheaves]]

The basic example for left Kan extensions using the above pointwise formula, is in the construction of the pullback of sheaves along a morphism of topological spaces. Let $f:X\to Y$ be a continuous map and $F$ a presheaf over $X$. Then the formula $(f_* F)(U) = F(f^{-1}(U))$ clearly defines a presheaf $f_* F$ on $Y$, which is in fact a sheaf if $F$ is.
On the other hand, given a presheaf $G$ over $Y$ we can not
define pullback presheaf $(f^{-1} G)(V)=G(f(V))$ because $f(V)$ might not be open in general (unless $f$ is an open map). For Grothendieck sites such $f(V)$ would not make even sense. But one can consider approximating from above by $G(W)$ for all $W\supset f(V)$ which are open and take a colimit of this diagram of inclusions (all $W$ are bigger, so getting down to the lower bound means going reverse to the direction of inclusions). But inclusion $f(V)\subset W$ implies $V\subset f^{-1}(f(V))\subset f^{-1}(W)$. The latter identity $V\subset f^{-1}(W)$ involves _only open sets_. Thus we take a colimit over the comma category $(V\downarrow f^{-1})$ of $G$. If $G$ is a sheaf, the colimit $G(V)$ understood as a rule $V\mapsto G(V)$ is still not a sheaf, we need to [[sheafification|sheafify]]. The result is sheaf-theoretic pullback 
$$
f^{-1}G = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{V\hookrightarrow f^{-1}W} G(W)) = \mathrm{sheafify}(V\mapsto\mathrm{colim}_{(V\downarrow f^{-1})} G)
$$ 
which is a sheaf, and one can analyze this construction to show that $f^{-1}$ is a left adjoint to $f_*$. This usage of left Kan extension persists in the more general case of Grothendieck topologies. 


### Kan extension in physics
 {#ExamplesKanExtensionsInPhysics}

We list here some occurrences of Kan extensions in [[physics]].

Notice that since, by the above discussion, Kan extensions are ubiquitous in [[category theory]] and are essentially equivalent to other standard [[universal constructions]] such as notably [[colimit|co]]/[[limits]], to the extent that there is a relation between [[higher category theory and physics|category theory and physics]] at all, it necessarily also involves Kan extensions, in some guise. But here is a list of some example where they appear rather explicitly.

* In [[extended quantum field theory]] on open and closed manifolds, usually the theory "in the bulk" (on closed manifolds) is induced by "extending" that "[[boundary field theory|on the boundary]]", and in good cases this extension is explicitly a ([[homotopy Kan extension|homotopy]])-Kan extension. This is the case notably for [[2d TQFT]] in the form of [[TCFT]] ([Costello 04](TCFT#Costello04)), see at _[TCFT -- Classification](TCFT#Classification)_ for details.

* When [[path integral]] [[quantization]] is formalized in terms of [[fiber integration in generalized cohomology]] (as surveyed at _[[motivic quantization]]_) then the push-forward step, hence the path integral itself, is given by left [[homotopy Kan extension]] of [[parameterized spectrum|parameterized spectra]]. For explicit details see ([[schreiber:master thesis Nuiten|Nuiten 13, section 4.1]]), also ([[schreiber:Homotopy-type semantics for quantization|Schreiber 14, section 6.2]]). By example 6.3, a special case of this is the integration formulas via Kan extension in ([[Ambidexterity in K(n)-Local Stable Homotopy Theory|Hopkins-Lurie 14, section 4]]).


## Remark on terminology: pushforward vs. pullback

Generally, for $p : C \to C'$ a [[functor]], the induced "precomposition" functor on [[functor category|functor categories]]
$$
  [C', D] \stackrel{- \circ p}{\to}
  [C,D]
$$
is spoken of as _pulling back_ a functor on $C'$ to a functor on $C$, as this operation goes in the direction opposite to that of $p$ itself.  For this reason, we have above denoted this functor by $p^*$.  Likewise, one might call the (left or right) Kan extensions along $p$ a _push forward_ of functors from $C$ to functors on $C'$.


This notation also coincides with that for [[geometric morphisms]] in one case: any functor $p\colon C\to C'$ between small categories induces a geometric morphism $[C,Set] \to [C',Set]$ of [[presheaf topos|presheaf toposes]], whose [[inverse image]] is the above $p^*$ and whose [[direct image]] $p_*$ is the right Kan extension functor.  Note that $p^*$ preserves (finite) limits, as required of an inverse image functor, since it has a left adjoint, namely *left* Kan extension.

On the other hand, if $p$ is additionally a [[flat functor]], then the above precomposition functor is also the *direct* image of a geometric morphism, whose inverse image is given by *left* Kan extension (which preserves finite limits when $p$ is flat).  More generally, if $C^{op}$ and $(C')^{op}$ are [[sites]] and $p^{op}\colon C^{op}\to (C')^{op}$ is flat and preserves covering families (i.e. it is a [[morphism of sites]]), then precomposition is the direct image of a geometric morphism $Sh(C^{op})\to Sh((C')^{op})$ between sheaf toposes.

For example, $C^{op}$ and $(C')^{op}$ might be the [[posets]] $Open(X)$ and $Open(X')$ of open subsets of [[topological spaces]] (or [[locales]]) $X$ and $X'$ and inclusions, in which case
$$
  Open(X)^{op} \to Open(X')^{op}
$$ 
come from continuous maps of topological spaces going the other way
$$
  X \leftarrow X' : f
  \,,
$$
via the usual inverse image $f^{-1} : O(X)^{op} \to O(X')^{op}$ of open subsets.


Thus, in such cases, the functor $p^*$, which looks like a pullback of functors along $p = f^{-1}$, corresponds geometrically to a _push-forward_ of (pre)sheaves along $f$.  Therefore, in [[presheaf]] literature (such as [[Categories and Sheaves]]) the precomposition functor induced by $p$ is usually denoted $p_*$ and not $p^*$.

It is however noteworthy that also the opposite perspective does occur in geometrically motivated examples. For instance 

* if $C$ is the [[discrete category]] on smooth space and $D = U(1)$ is the discrete category on the smooth space $X$ underlying the Lie group $U(1)$, then smooth functors (i.e. functors [[internal category|internal to]] [[generalized smooth space|smooth spaces]]) $F : C \to D$ can be identified with smooth $U(1)$-valued functions on $X$, and the functor on these functor categories induced by a smooth functor $p : C \to C'$ does correspond to the familiar notion of _pullback_ of functions;

* and similar in higher degrees: if $C = P_1(X)$ is the smooth path groupoid of a smooth space and $D = \mathbf{B} U(1)$ the smooth [[group]] $U(1)$ regarded as a one-object [[Lie groupoid]], then smooth functors $C \to D$ correspond to smooth 1-forms $\in \Omega^1(X)$ on $X$, and precomposition with a smooth functor $p : P_1(X) \to P_1(X')$ corresponds to the familiar notion of _pullback_ of 1-forms.

This means that whether or not Kan extensions correspond geometrically to pushforward or to pullback depends on the way (covariant or contravariant) in which the domain categories $C$, $C'$ are identified with geometric entities.

## Related concepts

* **Kan extension**, [[(∞,1)-Kan extension]]

* [[base change]]

  * [[dependent sum]], [[dependent product]]

  * [[dependent sum type]], [[dependent product type]]

* [[internal (co-)limit]]

* [[codensity monad]]

* [[shape theory]]

## References

Textbook sources include 

* {#Borceux} [[Francis Borceux]], section 3.7 of _[[Handbook of Categorical Algebra]] I_
 

* Kashiwara and Shapira, section 2.3 in _[[Categories and Sheaves]]_

The book

* [[Saunders MacLane]], _[[Categories Work|Categories for the working mathematician]]_

has a famous treatment of Kan extensions with a statement: "The notion of Kan extensions subsumes all the other fundamental concepts in category theory".  Of course, many other fundamental concepts of category theory can also be regarded as subsuming all the others.

Lecture notes with an eye towards applications in [[homotopy theory]] include

* {#Riehl} [[Emily Riehl]], _Categorical homotopy theory_ ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf)).

For Kan extensions in the context of [[enriched category theory]] see

* [[Eduardo Dubuc]], _Kan extensions in enriched category theory_,  Lecture Notes in Mathematics, Vol. 145 Springer-Verlag, Berlin-New York 1970 xvi+173 pp.

and chapter 4 of

* {#Kelly} [[Max Kelly]], _Basic Concepts of Enriched Category Theory_, 
 Cambridge University Press, Lecture Notes in Mathematics 64, 1982,  Republished in: Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))
 


The [[(∞,1)-category theory]] notion is discussed in section 4.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

For uses of Kan extension in the study of [[algebra over a Lawvere theory|algebras over an algebraic theory]] see

* [[Paul-André Melliès]] and [[Nicholas Tabareau]], _Free models of T-algebraic theories computed as Kan extensions_ ([web](http://hal.archives-ouvertes.fr/hal-00339331/fr/))

Preservation of certain limits by left Kan extended functors is discussed in 

* {#BorceuxDay} [[Francis Borceux]], and [[Brian Day]], _On product-preserving Kan extension_, Bulletin of the Australian Mathematical Society, Vol 17 (1977), 247-255 ([pdf](http://journals.cambridge.org/download.php?file=%2FBAZ%2FBAZ17_02%2FS0004972700010455a.pdf&code=e8c9ebb215a55a0891f4e05f6aebbcf2))
  
* {#KarazerisProtsonis} Panagis Karazeris, Grigoris Protsonis, _Left Kan extensions preserving finite products_, ([pdf](http://www.math.upatras.gr/~pkarazer/publications/topsift.pdf))
 
The general notion of extensions of [[1-morphisms]] in [[2-categories]] is discussed in 

* {#Lack09} [[Steve Lack]], _A 2-categories companion_, in [[John Baez]], [[Peter May]], _[[Towards Higher Categories]]_, Springer, (2009) ([arXiv:math/0702535](http://arxiv.org/abs/math/0702535))
* [[Ross Street]], _Pointwise extensions and sketches in bicategories_, [arXiv:1409.6427](https://arxiv.org/abs/1409.6427)
* {#Roald13} Seerp Roald Koudenburg, *Algebraic weighted colimits*, [arXiv](http://arxiv.org/abs/1304.4079)
 
For the notion of (2-dimensional) (pointwise) bi-Kan extensions of pseudofunctors, see

* Fernando Lucatelli Nunes, *On biadjoint triangles*, TAC [31-9](http://tac.mta.ca/tac/volumes/31/9/31-09abs.html)

* Fernando Lucatelli Nunes, *Pseudo-Kan extensions and descent theory*, TAC [33-15](http://www.tac.mta.ca/tac/volumes/33/15/33-15abs.html)

and its applications to the theory of (2-dimensional) [[flat functors]] can be seen in

* M.E. Descotte, E.J. Dubuc, M. Szyld, *On the notion of flat 2-functors*, [Adv. Math](https://www.sciencedirect.com/science/article/abs/pii/S0001870818301968), arXiv:[1610.09429](https://arxiv.org/abs/1610.09429)

[[!redirects Kan extension]]
[[!redirects Kan extensions]]
[[!redirects kan extension]]
[[!redirects kan extensions]]
[[!redirects left Kan extension]]
[[!redirects left Kan extensions]]
[[!redirects left kan extension]]
[[!redirects left kan extensions]]
[[!redirects right Kan extension]]
[[!redirects right Kan extensions]]
[[!redirects right kan extension]]
[[!redirects right kan extensions]]
[[!redirects pointwise Kan extension]]
[[!redirects pointwise Kan extensions]]