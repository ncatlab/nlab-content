
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

We discuss a refinement of the traditional notion of _[[Atiyah Lie groupoids]]_ (the [[Lie groupoids]] which are the [[Lie integration]] of [[Atiyah Lie algebroids]] of $G$-[[principal bundles]]) from [[differential geometry]] to [[higher differential geometry]] and generally to [[higher geometry]].

Briefly, for $G$ an [[∞-group]] in an [[(∞,1)-topos]] and $P \to X$ a $G$-[[principal ∞-bundle]], its _higher Atiyah groupoid_ is the [[groupoid object in an (∞,1)-category|groupoid object]] $At(P)$ such that the

* object of [[objects]] is $X$;

* object of [[morphisms]] is the collection of all $G$-equivariant maps between all pairs of [[fibers]] of $P$.

In these vague words this is precisely the same description as for the traditional Atiyah groupoid. Definition \ref{HigherAtiyahGroupoid} below makes precise what this means in [[higher geometry]].

Besides generalizing the traditional definition to [[homotopy theory]], the notion of higher Atiyah groupoids also generalizes from [[concrete objects]] such as [[Lie groups]] to general objects in an [[(∞,1)-topos]] (general [[∞-stacks]], not necessarily "supported on points"), notably to _[[moduli ∞-stacks]]_ for [[cocycles]] in [[differential cohomology]]. For instance if we assume that the ambient [[(∞,1)-topos]] $\mathbf{H}$ is [[cohesive (∞,1)-topos|cohesive]] and consider $\mathbb{G} \in \mathrm{Grp}(\mathbf{H})$  a _[[sylleptic ∞-group]]_, then there is the [[moduli ∞-stack]] $\mathbf{B}\mathbb{G}_{\mathrm{conn}}$ of _$\mathbb{G}$-[[principal ∞-connections]]_ and this is itself again a [[group object in an (∞,1)-category|group object]]. 
A $(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$-[[principal ∞-bundle]] is equivalently a $(\mathbf{B}^2\mathbb{G})$-[[principal ∞-connection]] "without [[curving]]". For instance if $\mathbb{G} = U(1)$ is the [[circle group]] in [[smooth ∞-groupoids]], then 
$\mathbf{B}(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$ classifies [[circle 2-bundle with connection]] without 2-form part: in parts of the literature this is known as "[[bundle gerbes]] with connective structure but without [[curving]]".

So the general definition considered here assigns a higher Atiyah groupoid to a "bundle gerbe with connective structure but no [[curving]]". It turns out that this is the _[[Courant 2-groupoid]]_ which [[Lie integration|Lie integrates]] the [[standard Courant Lie 2-algebroid]] traditionally induced by this data.

The  notion of higher Atiyah groupoids is more general still: the definition does not really require that the object fed into the construction is a plain [[principal ∞-bundle]]. It may notably also be a genuine [[principal ∞-connection]] (hence " _with_ [[curving]]"). We show below that the corresponding higher Atiyah groupoid is that groupoid object whose [[∞-group of bisections]] is the [[quantomorphism n-group]] of the principal $\infty$-connection regarded as a [[prequantum n-bundle]].

In summary, the [[higher geometry|higher geometric]] generalization of the notion of Atiyah groupoids unifies all three of the traditional notions of [[Atiyah groupoid]], of [[Courant 2-groupoid]] and of [[quantomorphism group]] and refines each of these to [[higher geometry]]:

[[!include higher Atiyah groupoid - table]]

At the same time the definition of higher Atiyah groupoids in [[(∞,1)-topos theory]], def. \ref[HigherAtiyahGroupoid} below, is very simple, almost tautological, identifying it as a very fundamental notion in [[(∞,1)-topos theory]]/[[homotopy type theory]].

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Let $G \in Grp(\mathbf{H})$ be a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, an [[∞-group]].

We define now for every $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ a _[[groupoid object in an (∞,1)-category|groupoid object]]_ $At(P) \in Grpd(\mathbf{H})$ in $\mathbf{H}$. In order to do so we invoke two basic facts.

+-- {: .num_prop #EffectiveEpisAreEquivalentlyGroupoids}
###### Proposition

The construction of forming the [[Cech nerve]] of a [[morphism]] consitutes an [[equivalence of (∞,1)-categories]] from that of [[1-epimorphisms]] to that of [[groupoid objects in an (∞,1)-category|groupoid objects]] in $\mathbf{H}$:

$$
  (\mathbf{H}^{\Delta^1})_{1epi}
  \stackrel{\simeq}{\to}
  Grpd(\mathbf{H})
 \,.
$$

=--

This is a refined version of one of the [[Giraud-Rezk-Lurie axioms]] characterizing [[(∞,1)-topos]], discussed at _[[groupoid object in an (∞,1)-category]]_.

+-- {: .num_remark }
###### Remark

In terms of traditional terminology in the literature on [[topological stacks]]/[[differentiable stacks]] etc, this says that a groupoid object in $\mathbf{H}$ is equivalently an object $X \in \mathbf{H}$ which is equipped with an [[atlas]] $X_0 \to X$.

=--

Write $\mathbf{B}G \in \mathbf{H}$ for the [[delooping]] of $G$ in $\mathbf{H}$ (the [[moduli ∞-stack]] of $G$-[[principal ∞-bundles]], as the following proposition asserts:

+-- {: .num_prop #ClassificationOfGPrincipalBundles}
###### Proposition

The operation of forming [[(∞,1)-fibers]] ([[homotopy fibers]]) constitutes an [[equivalence of ∞-groupoids]]

$$
  fib 
  \;\colon\;
  \mathbf{H}(X, \mathbf{B}G)
  \to 
  G Bund(X)
  \,.
$$

=--

This is discussed at _[[principal ∞-bundle]]_.

Using these two facts we now set:

+-- {: .num_defn #HigherAtiyahGroupoid}
###### Definition

For $P \to X$ a $G$-[[principal ∞-bundle]] in $\mathbf{H}$, its **Atiyah groupoid** is the [[groupoid object in an (∞,1)-category|groupoid object]] $At \in \mathrm{Grpd}(\mathbf{H}) \simeq (\mathbf{H}^{\Delta^1})_{1epi}$ which is the [[1-image]] projection of the classifying map $g \colon X \to \mathbf{B}G$:

$$
  g 
  \;\colon\;
  X
   \stackrel{}{\to}
  At(P) \coloneqq im_1(g)
  \hookrightarrow
  \mathbf{B}G
  \,.
$$  

=--

+-- {: .num_remark #AtiyahGroupoidIsCechNerve}
###### Remark

By the discussion at _[[1-image]]_, the 1-image projection of any morphism $f \colon X \to Y$ in an [[(∞,1)-topos]] is equivalently given as the canonical map given by the [[(∞,1)-colimit]] over the [[Cech nerve]]

$$
  X \to im_1(f) \simeq \underset{\rightarrow}{\lim} (X^{\times^{\bullet+1}_Y})
  \,.
$$

This means that regarded as an object of $Grpd(\mathbf{H})$, the Atiyah groupoid $At(P)$ _is_ simply the [[Cech nerve]] of the classifying map. This means that the definition of Atiyah groupoids in [[higher geometry]] is much more fundamental than in traditional [[geometry]]. 

=--

## Properties

### Equivalence of Atiyah-groupoid bisections to slice automorphisms

We discuss how the [[∞-group of bisections]] of a higher Atiyah groupoid is canonically equivalent to the $\mathbf{H}$-valued [[automorphism ∞-group]] of the modulating map that gave rise to it, regarded as an object in the [[slice (∞,1)-topos]] over its [[codomain]]. 

To this end we need the following two definitions

+-- {: .num_defn #HValuedAutomorphismGroup}
###### Definition

For $f \colon X \to Y$ a [[morphism]] in an [[(∞,1)-topos]] $\mathbf{H}$, its **$\mathbf{H}$-valued [[automorphism ∞-group]]** $\mathbf{Aut}_{\mathbf{H}}(f)$ is the [[dependent product]] over $Y$ over the [[automorphism ∞-group]] of $f$ regarded as an object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/Y}$:

$$
  \mathbf{Aut}_{\mathbf{H}}(f)
  \coloneqq
  \underset{Y}{\prod} \mathbf{Aut}_{/Y}(f)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For [[concrete object|non-concrete]] codomains $Y$ one is usually interested in the [[concretification]] of this group. To be discussed... For an example see at _[The quantomorphism $n$-group](#TheQuantomorphismNGroups)_ below.

=--



+-- {: .num_defn}
###### Definition

For $\mathcal{G} \in Grpd(\mathbf{H})$ a [[groupoid object in an (∞,1)-category|groupoid object]] in an [[(∞,1)-topos]] $\mathbf{H}$, its **[[∞-group of bisections]]** $\mathbf{BiSect}(\mathcal{G}) \in Grpd(\mathbf{H})$ is the $\mathbf{H}$-valued automorphism $\infty$-group, def. \ref{HValuedAutomorphismGroup}, of the [[atlas]] $\phi_{\mathcal{G}} \colon \mathcal{G}_0 \to \mathcal{G}$ of $\mathcal{G}$ under prop. \ref{EffectiveEpisAreEquivalentlyGroupoids}:

$$
  \mathbf{BiSect}(\mathcal{G})
  \coloneqq
  \mathbf{Aut}_{\mathbf{H}}(\phi_{\mathcal{G}})
  \,.
$$

=--

With this the following proposition is immediate, but important for the interpretation of higher Atiyah groupoids:

+-- {: .num_prop}
###### Propostition

For $c \;\colon\; X \to \mathbf{F}$ a [[morphism]] in an [[(∞,1)-topos]] $\mathbf{H}$, modulating an [[fiber ∞-bundle]] $P \to X$, there is an canonical [[equivalence in an (infinity,1)-category|equivalence]] of [[∞-groups]] 

$$
  \mathbf{BiSect}(At(P))
  \simeq
  \mathbf{Aut}_{\mathbf{H}}(c)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We may read this as saying that the higher Atiyah groupoid of an [[fiber ∞-bundle]] is the [[universal property|universal]] solution to the problem of finding a [[groupoid object in an (∞,1)-category|groupoid object]] whose [[∞-group of bisections]] reproduces a given slice [[automorphism ∞-group]]. In many applications, this is indeed the crucial property that drives the interest in higher Atiyah groupoids, see the _[Examples](#Examples)_ below.

=--


### Sequences of inclusions of Atiyah-bisection $\infty$-groups
 {#SequencesOfInclusionsOfGroupsOfBisections}

Let $\mathbf{H}$ be an [[(∞,1)-topos]] which is [[cohesive (∞,1)-topos|cohesive]]. As discussed there, this implies that there is an internal notion of [[differential cohomology]] and in particular of [[principal ∞-connections]] in $\mathbf{H}$. We note here how the canonical forgetful maps between [[moduli ∞-stacks]] of [[principal ∞-bundles]] equipped with differing degree of differential refinement induce canonical inclusions of the corresponding higher Atiyah groupoids. 

Let $\mathbb{G} \in Grp(\mathbf{H}) be a $[[braided ∞-group]]. Then there exists, by [[cohesion]], a canonical notion of $\mathbb{G}$-[[principal ∞-connections]], whose [[moduli ∞-stack]] we denote $\mathbf{B}\mathbb{G}_{\mathrm{conn}}$. This is equipped with a canonical map

$$
  \mathbf{B}\mathbb{G}_{conn} \to \mathbf{B}\mathbb{G}
$$

which "forgets the connection". Then for $\nabla \colon X \to \mathbf{B}\mathbb{G}_{conn}$ a $\mathbb{G}$-[[principal ∞-connection]] we write

$$
  \nabla_0 \;\colon\; X \stackrel{\nabla}{\to} 
   \mathbf{B}\mathbb{G}_{conn} \to \mathbf{B}\mathbb{G}
$$

for the corresponding underlying map.

+-- {: .num_prop #InclusionOfNableBisectionsIntoNable0Bisections}
###### Proposition

The [[dependent sum]] along this map induces a canonical map of [[∞-groups]] 

$$
  \mathbf{BiSect}(At(\nabla))
  \to   
  \mathbf{BiSetc}(At(\nabla_0))
  \,.
$$

=--

If we regard $\nabla$ as a [[prequantum n-bundle]] then this is a canonical inclusion of the [[quantomorphism n-group]] into the $\infty$-group of "$\nabla_0$-twisted diffeomorphisms".


If $\mathbb{G}$ is even a [[sylleptic ∞-group]], then the above moduli $\infty$-stacks have a further [[delooping]] and we obtain a 2-step sequence of forgetful maps

$$
  \mathbf{B}^2 \mathbb{G}_{conn}
  \to 
  \mathbf{B}(\mathbf{B}\mathbb{G}_{conn})
  \to 
   \mathbf{B}^2 \mathbb{G}
  \,.
$$

Accordingly:

+-- {: .num_prop #InclusionOfNableBisectionsIntoNable1AndNabla0Bisections}
###### Proposition

The [[dependent sum]] along these maps induces inclusions of $\infty$-groups

$$
  \mathbf{BiSect}(At(\nabla))
  \to 
  \mathbf{BiSect}(At(\nabla_1))
  \to
  \mathbf{BiSect}(At(\nabla_0))  
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This now interprets as the inclusion 

1. of the [[quantomorphism n-group]] into the $\infty$-group of bisections of the [[higher Courant groupoid]];

1. $\infty$-group of bisections of the [[higher Courant groupoid]] into that of "$\nabla_0$-twisted diffeomorphisms".

See below at _[Examples-- The traditional Courant Lie 2-algebroid](#TheTraditionalCourantLie2Algebroid)_ for more on this.


=--




## Examples
 {#Examples}

We first show how the general notion of _higher Atiyah groupoid_ reproduces various traditonal structures.

* _[The traditonal Atiyal Lie groupoid](#TheTraditionalAtiyagLieGroupoid)_

* _[The traditional Courant Lie 2-algebroid](#TheTraditionalCourantLie2Algebroid)_

* _[The traditional quantomorphism group](#TheTraditionalQuantomorphismGroup)_

* _[The quantomorphism n-groups](#TheQuantomorphismNGroups)_


### The traditional Atiyah Lie groupoid
 {#TheTraditionalAtiyagLieGroupoid}

We discuss how the traditional notion of [[Atiyah Lie groupoids]] in traditional [[differential geometry]] is a special case of higher Atiyah groupoids of def. \ref{HigherAtiyahGroupoid}.

To set this up we take the ambient [[(∞,1)-topos]] to be 

$\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] and make use of the canonical embeddings

[[SmthMfd]] $\hookrightarrow$ [[diffeological space|DiffeologicalSpace]] $\hookrightarrow$ [[smooth spaces|SmoothSpace]] $\hookrightarrow$ [[Smooth∞Grpd]],

and 

[[Lie groupoid|LieGrpd]] $\simeq$ [[differentiable stack]] $\hookrightarrow$ [[Smooth∞Grpd]]

which are understood in the following.

+-- {: .num_prop }
###### Proposition

For $G$ a [[Lie group]], $X$ a [[smooth manifold]] and $P \to X$ a $G$-[[principal bundle]], the traditional [[Atiyah Lie groupoid]] of $P$ is equivalent to that of def. \ref{HigherAtiyahGroupoid}.

=--

+-- {: .proof}
###### Proof

Write $g \colon X \to \mathbf{B}G$ for the classifying map of $P \to X$, by prop. \ref{ClassificationOfGPrincipalBundles}. 

By remark \ref{AtiyahGroupoidIsCechNerve} the higher Atiyah groupoid $At(P)$ is simply the [[Cech nerve]] of this map. Since $G$ and $X$ and hence $P$ are all [[truncated object in an (infinity,1)-category|0-truncated objects]], hence $\mathbf{B}G$ a [[1-truncated]] object, this Cech nerve is [[coskeleton|2-coskeletal]] and hence is sufficient to consider the first three degrees. By definition these are

$$
  At(P)
  \simeq
  \left(
    X \underset{\mathbf{B}G}{\times}X \underset{\mathbf{B}G}{\times}X 
      \stackrel{\to}{\stackrel{\to}{\to}} 
    X \underset{\mathbf{B}G}{\times}X
      \stackrel{\to}{\to}
    X 
  \right)
  \,,
$$ 

where $X \underset{\mathbf{B}G}{\times}X $ denotes the [[homotopy fiber product]] of $g$ with itself, and so forth. To see what this object is, pick any $U \in $ [[CartSp]], and observe that 

$$
  \mathbf{H}(U, X\underset{\mathbf{B}G}{\times}X )
  \simeq
  \mathbf{H}(U,X) \underset{\mathbf{H}(U,\mathbf{B}G)}{\times} \mathbf{H}(U,X)
$$

(using that the [[(∞,1)-categorical hom]]-[[(∞,1)-functor]] $\mathbf{H}(U,-)$ preserves [[(∞,1)-limits]]) is equivalently the [[set]] of [[triples]] consisting of two [[smooth functions]] $\phi_1, \phi_2 \colon X$ and a [[gauge transformation]] between the [[pullback|pulled-back bundles]] $\eta \colon \phi_1^* P \to \phi_2^* P$ on $U$.

Since $U$ is topologically [[contractible topological space|contractible]], and hence every $G$-[[principal bundle]] over $U$ admits a [[section]], every such triple induces a [[function]], in fact a [[bijection]], from the set of lifts $\hat \phi_1 \colon U \to P$ of $\phi_1$ to the set of lifts $\hat \phi_2 \colon U \to P$ which are $C^\infty(U,G)$-equivariant. By $G$-equivariant every pair consisting of a single lift $\hat \phi_1$ and its image $\eta(\hat \phi_1)$ already uniquely determes $\eta$. Therefore the above set of triples is [[natural isomorphism|naturally isomorphic]] to the set of [[smooth functions]] $U \to P \times_G P \coloneqq (P \times P)/_{diag} G$. This is precisely the [[smooth manifold]] of [[morphisms]] of the traditional [[Atiyah Lie groupoid]]. Since this is true for all $U \in $ [[CartSp]] and [[natural transformation|naturally]] so, and since [[CartSp]] is a [[site]] of definition of [[Smooth∞Grpd]] it follows by the [[(∞,1)-Yoneda lemma]] (which in the present cases reduces to the ordinary [[Yoneda lemma]]), we have a [[natural equivalence]]

$$
  X \underset{\mathbf{B}G}{\times} X 
  \simeq 
  P \times_G P
  \,.
$$

In this manner it is immediate to check that this identification respects all the structure maps, and hence the above Cech nerve is indeed identified as the [[simplicial manifold]] which is the [[nerve]] of the traditional [[Atiyah Lie groupoid]] $(P \times_G P \stackrel{\to}{\to} X)$.

=--

### The traditional Courant Lie 2-algebroid 
 {#TheTraditionalCourantLie2Algebroid}

There is a traditional construction which assigns to a [[bundle gerbe]] "with connective structure but without [[curving]]" a [[Courant Lie 2-algebroid]]. We discuss here how this is the [[Lie differentiation]] of the corresponding higher Atiyah groupoid.

In order to do so, we pick again, as [above](#TheTraditionalAtiyagLieGroupoid), as ambient context $\mathbf{H} = $ [[Smooth∞Grpd]].

+-- {: .num_prop }
###### Proposition

For $\mathbb{G} \coloneqq U(1) \in LieGrp \hookrightarrow Grp(\mathbf{H})$ the [[circle Lie group]] (which is in particular a [[sylleptic ∞-group]]), the sequence of maps of [[moduli ∞-stacks]]

$$
  \mathbf{B}^2 U(1)_{conn}
  \to 
  \mathbf{B}(\mathbf{B}U(1)_{conn})
  \to
  \mathbf{B}^2 U(1)
$$

of prop. \ref{InclusionOfNableBisectionsIntoNable1AndNabla0Bisections} is presented under the canonical equivalence [[Smooth∞Grpd]] $\simeq _{L_{lwhe}} Func(CartSp^{op}_{smooth}, sSet)$ by the image under the [[Dold-Kan correspondence]] of the evident sequence of [[chain maps]]

$$
  \array{
    U(1) &\stackrel{id}{\to}& U(1) &\stackrel{id}{\to}& U(1)
    \\
    \downarrow^{\mathrlap{d log}} && \downarrow^{\mathrlap{d log}} && \downarrow^{\mathrlap{0}}
    \\
    \Omega^1 &\stackrel{id}{\to}& \Omega^1 &\stackrel{\mathrlap{0}}{\to}& 0
    \\
    \downarrow^{\mathrlap{d}} && \downarrow^{\mathrlap{0}} && \downarrow^{\mathrlap{0}}    
    \\
    \Omega^2 &\to& 0 &\to& 0
  }
  \,,
$$

where on the left we have the [[Deligne complex]] for degree-3-[[ordinary differential cohomology]].

=--

+-- {: .proof}
###### Proof

This is a direct consequence of the discussion at _[[circle n-bundle with connection]]_.

=--

+-- {: .num_remark }
###### Remark

This makes precise how

* $\mathbf{B}^2 U(1)_{conn}$ is the [[moduli infinity-stack|moduli 2-stack]] of [[circle 2-bundles with connection]];

* $\mathbf{B}(\mathbf{B}U(1)_{conn})$ is the moduli 2-stack of circle 2-bundle "with connection but without [[curving]]";

* $\mathbf{B}^2 U(1)$ is the moduli 2-stack of [[circle 2-group]]-[[principal 2-bundles]].

=--

Let

$$
  \nabla_1 \colon X \to \mathbf{B}(\mathbf{B}U(1)_{conn})
$$

be the map modulating [[circle 2-bundle with connection]] but "without [[curving]]". Then then higher Atiyah groupoid of th $(\mathbf{B}U(1)_{conn})$-[[principal 2-bundle]] classified by this map has as higher Atiyah groupoid the corresponding _[[Courant Lie 2-groupoid]]_: the object which is the [[Lie integration]] of the traditional [[Courant Lie 2-algebroid]] associated with $\nabla_1$.

To see we observe that the corresponding [[∞-group of bisections|2-group of bisections]] is

$$
  \mathbf{Aut}_{\mathbf{H}}(\nabla_1)
  \coloneqq
  \underset{\mathbf{B}(\mathbf{B}U(1)_{conn})}{\prod}
  \mathbf{Aut}_{/\mathbf{B}(\mathbf{B}U(1)_{conn})}(\nabla_1)
  \,.
$$

This has as objects [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
     X &&\underoverset{\simeq}{\phi}{\to}&& X
     \\
     & {}_{\mathllap{\nabla_1}}\searrow &\swArrow_\eta& \swarrow_{\mathrlap{\nabla_1}}
     \\
     && \mathbf{B}(\mathbf{B}U(1)_{conn})
  }
  \,,
$$

hece equivalently pairs consisting of a [[diffeomorphism]] $\phi \colon X \to X$ and a [[gauge transformation]] (of 2-connections without [[curving]])

$$
  \eta 
    \;\colon \;
  \phi^* \nabla_1 \to \nabla_1
  \,.
$$

The morphisms are accordingly the suitable [[natural transformations]] of these diagrams.

This is precisely the 2-group of "bundle gerbe symmetries" of $\nabla_1$ which is studient in ([Collier](#Collier)). With this identification the main result there is the above claim.

Moreover, the canonical inclusions of smooth 2-groups of prop. \ref{InclusionOfNableBisectionsIntoNable1AndNabla0Bisections} reproduces, under [[Lie differentiation]], the inclusion of the [[Poisson Lie 2-algebra]] into that [[Lie 2-algebra]] of sections of the corresponding [[Courant Lie 2-algebroid]] observed in ([Rogers](#Rogers)).


### The traditional quantomorphism group
 {#TheTraditionalQuantomorphismGroup}

For $\nabla \colon X \to \mathbf{B}U(1)_{conn}$
the [[group of bisections]] of the corresponding Atiyah groupoid is the [[quantomorphism group]] of $\nabla$ regarded as a [[prequantum bundle]].

(...)


### The quantomorphism $n$-groups
 {#TheQuantomorphismNGroups}

For $\nabla \colon X \to \mathbf{B}^nU(1)_{conn}$
the [[∞-group of bisections]] of the corresponding Atiyah groupoid is the [[quantomorphism n-group]] of $\nabla$ regarded as a [[prequantum n-bundle]]. Under [[Lie differentiation]] this is the corresponding [[Poisson Lie n-algebra]]. ([Fiorenza-Rogers-Schreiber](#FiorenzaRogersSchreiber)).

## Related concepts

[[!include higher Atiyah groupoid - table]]

## References

The [above](#TheTraditionalCourantLie2Algebroid) identification of higher Atiyah groupoids of "bundle gerbes with connective structure but without [[curving]]" with those [[Lie integration|Lie integrating]] the corresponding [[standard Courant Lie 2-algebroid]] is directly implied (under the above translations) by the main result in 

* [[Braxton Collier]], _Infinitesimal Symmetries of Dixmier-Douady Gerbes_ ([arXiv:1108.1525](http://arxiv.org/abs/1108.1525))
 {#Collier}

The corresponding inclusion of the [[Poisson Lie 2-algebra]] into the [[Lie 2-algebra]] of bisections of the [[Courant Lie 2-algebroid]] was first observed in

* [[Chris Rogers]], _2-plectic geometry, Courant algebroids, and categorified prequantization_ ,  [arXiv:1009.2975](http://arxiv.org/abs/1009.2975).

in the context of _[[2-plectic geometry]]_ over [[smooth manifolds]].

Most further statements here will appear in 

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Chris Rogers]], ...
 {#FiorenzaRogersSchreiber}


[[!redirects higher Atiyah groupoids]]


