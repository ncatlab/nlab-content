
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


> See also [[derived hom space]]

#Simplicial localisation#
* table of contents
{:toc}


## Idea 

A [[category with weak equivalences]] or  [[homotopical category]] is a [[category]] $C$ equipped with the information that some of its [[morphisms]], specifically, a subcategory $W \supset Core(C)$, are to be regarded as "weakly invertible".  One way to make this notion precise is through the concept of __simplicial localization__:

The _simplicial localization_ $L C$ of a category $C$ is an [[(∞,1)-category]] realized concretely as a [[simplicially enriched category]] which is such that the original category injects into it,  $C \hookrightarrow L C$, such that every morphism in $C$ that is labeled as a weak equivalence becomes an actual equivalence in the sense of morphisms in [[(∞,1)-categories]] in $L C$. And $L C$ is in some sense universal with this property.

Passing to the [[homotopy category of an (∞,1)-category]] of $L C$ then reproduces the [[homotopy category]] that can also directly be obtained from $C$:

$$
  Ho_C(a,b) \simeq \Pi_0 (L C(a,b))
$$

(where $\Pi_0$ gives the  [[simplicial homotopy group|0th simplicial homotopy groupoid]]).

If the homotopical structure on $C$ extends to that of a (combinatorial) [[model category]], then there is another procedure to obtain a simplicially enriched category from $C$, the [[presentable (infinity,1)-category|(∞,1)-category presented by a combinatorial model category]]. This $(\infty,1)$-category is equivalent to the one obtained by simplicial localization but typically more explicit and more tractable. 

See also [[localization of a simplicial model category]].


## Construction

See [[simplicial localization of a homotopical category]].


## Definition

### "Standard" simplicial localization



Let $U : \mathbf{Cat} \to \mathbf{Grph}$ be the [[forgetful functor]] that sends a (small) category to its underlying _[[reflexive graph|reflexive]]_ [[graph]], and let $F : \mathbf{Grph} \to \mathbf{Cat}$ be its [[left adjoint]]. We then get a [[comonad]] $\mathbb{G} = (G, \epsilon, \delta)$ on $\mathbf{Cat}$, and as usual this defines a functor $G_\bullet : \mathbf{Cat} \to [\mathbf{\Delta}^{op}, \mathbf{Cat}]$ from [[Cat]] to [[simplicial objects in Cat]] equipped with a canonical augmentation, where $G_n C = G^{n+1} C$.

+-- {: .num_defn}
###### Definition
The **standard resolution** of a small category $C$ is defined to be the simplicial category $G_\bullet C$.
=--

Note that this is also a [[simplicial category]] in the strong sense, i.e. $ob G_\bullet C$ is discrete! Thus we may also regard $G_\bullet C$ as an [[sSet]]-[[simplicially enriched category|category]]. This is a [[resolution]] in the sense that the augmentation $\epsilon : G_\bullet C \to C$ is a [[Dwyer-Kan equivalence]]. (In fact, for objects $X$ and $Y$ in $C$, the morphism $G_\bullet C (X, Y) \to C (X, Y)$ admits an extra degeneracy and hence a contracting homotopy.)

+-- {: .num_defn}
###### Definition

The **standard simplicial localization** of a [[relative category]] $(C, W)$ is the simplicial category $L_\bullet (C, W)$ where $L_n (C, W) = G_n C [{G_n W}^{-1}]$.

=--

This appears as ([DwyerKanLocalizations, def. 4.1](#DwyerKanLocalizations)). 
Again, $L_\bullet C$ is a simplicial category in the strong sense, because $G_\bullet C$ is. 

### Hammock localization

+-- {: .num_defn}
###### Definition

Let $(C,W)$ be a [[category with weak equivalences]]. 
For $X,Y \in C$ any two objects, write 

$$
  L^H C(X,Y) \in sSet
$$

for the simplicial set which is the [[nerve]] of the category defined as follows:

* objects are [[equivalence class]]es of zig-zags of morphisms in $C$

  $$
    X \stackrel{\simeq}{\leftarrow}
    K_1 \to K_2 \stackrel{\simeq}{\leftarrow} K_3 \to
    \cdots \to Y
    \,,
  $$

  where the left-pointing morphisms are to be in $W$;

* [[morphisms]] are equivalence classes of "natural transformations" between such objects, fixing the endpoints:

  $$
    \array{
       && K_1 &\to& K_2 &\stackrel{\simeq}{\leftarrow}&
       \cdots 
       \\
       & {}^{\mathllap{\simeq}}\swarrow
       &&&&& && \searrow^{}
       \\
      X 
      && \downarrow^{\simeq}&& \downarrow^{\simeq}& \cdots&&  && Y
      \\
       & {}_{\mathllap{\simeq}}\nwarrow
       &&&&& && \nearrow^{}
      \\
       && L_1 &\to& L_2 &\stackrel{\simeq}{\leftarrow}&
       \cdots 
    }
    \;
  $$

* the equivalence relation identifies two such zig-zags if one is obtained by removing morphisms in one slot and/or by composing morphism that become composable this way.

For $X,Y,Z$ three objects, there is an evident compositing morphism

$$
  L^H C(X,Y) \times L^H C(Y,Z) \to L^H C(X,Z)
$$

given by horizontally concatenating hammock diagrams as above. 

The [[simplicially enriched category]] $L^H C$ obtained this way is the **hammock localization** of $(C,W)$.

=--

This appears as ([DwyerKanCalculating, def. 2.1](#DwyerKanCalculating)).


## Properties

### Basic properties

+-- {: .num_prop}
###### Proposition

For $(C,W)$ a [[category with weak equivalences]], write $L^H C \in sSet Cat$ for its hammock localization and $C[W^{-1}] \in Cat$ for its ordinary [[localization]]. 
Write $Ho(L^H C) \in Cat$ for the category with the same objects as $C$ and morphisms between $X$ and $Y$ being $\pi_0 L^H C(X,Y)$.

There is an [[equivalence of categories]]

$$
  Ho L^H C(X,Y)
   \simeq
  C[W^{-1}]
  \,.
$$

=--

This appears as ([DwyerKanCalculating, prop. 3.1](#DwyerKanCalculating)).

+-- {: .num_prop #PrePostCompositionWithWeakEquivalences}
###### Proposition

Let $(C,W)$ be a [[category with weak equivalences]], and let

$$
  (f : X \to Y) \in W \subset Mor(C)
$$

be a weak equivalence. Then for all objects $U \in C$ we have that the to concatenation operations on hammocks induce [[weak homotopy equivalence]]s

$$
  f_* : L^H C(U,X) \stackrel{\simeq}{\to}
     L^H C(U,Y)
$$

and

$$
  f^* : L^H C(Y,U) \stackrel{\simeq}{\to} L^H C(X, U)
  \,.
$$

=--

This appears as ([DwyerKanCalculating, prop. 3.3](#DwyerKanCalculating)).


### Simplical localization gives all $(\infty,1)$-categories

+-- {: .num_prop}
###### Proposition

Up to Dwyer-Kan equivalence --the [[weak equivalences]] in the [[model structure on sSet-categories]] -- every [[simplicial category]] is the simplicial localization of a [[category with weak equivalences]].


This is ([DwyerKan 87, 2.5](#DwyerKanEquivalences)).

=--

If the [[category with weak equivalences]] in question happens to carry even the structure of a [[model category]] there exist more refined tools for computing the [[SSet]]-[[hom object]] of the simplicial localization. These are described at [[(∞,1)-categorical hom-space]]. 

### Equivalences between simplicial localizations

+-- {: .num_prop #SimplicialLocalizationOfNaturalTransformation}
###### Proposition

Let $(C,W)$ and $(C', W')$ be [[categories with weak equivalences]]. Write $L^H C, L^H C' \in sSet Cat$ for the corresponding [[hammock localizations]].

Then for $F_1, F_2 :  C \to C'$ two [[homotopical functors]] (functors respecting the weak equivalences, i.e. $F_i(W) \subset W'$) with

$$
  \eta : F_1 \Rightarrow F_2
$$

a [[natural transformation]] with components in the $W'$,
we have that for all objects $X,Y \in C$, there is induced a [[natural transformation|natural]] [[homotopy]] between morphisms of [[simplicial sets]]

$$
  \array{
    && L^H C'(F_1(X), F_1(Y) )     
    \\
    & 
    {}^{\mathllap{L^H F_1}}\nearrow 
    && 
    \searrow^{\mathrlap{\eta(Y)_*}}
    \\
    L^H C(X,Y) 
     && \Downarrow && 
    L^H C'(F_1(X), F_2(Y))
    \\
    & 
     {}_{\mathllap{L^H F_2}}\searrow 
    &&  
     \nearrow_{\mathrlap{\eta(X)^*}}
    \\
    && L^H C' (F_2(X), F_2(Y))
  }
  \,.
$$

=--

This is ([DwyerKanComputations, prop. 3.5](#DwyerKanComputations)).


+-- {: .num_cor}
###### Corollary

Let $i : (C_1, W_1) \hookrightarrow (C_2, W_2)$
be a [[full subcategory]] such that 

1. $i$ is homotopy-essentially surjective: for every object $c_2 \in C_2$ there is an object $c_1 \in C_1$ and a weak equivalence $c_2 \stackrel{\simeq}{\to} i(c_1)$;

1. there is a [[functor]] $Q : (C_2,W_2) \to (C_1, W_1)$ and a [[natural transformation]]

   $$
     i \circ Q  \Rightarrow Id_{C_2}
     \,.
   $$

Then we have an [[equivalence of (∞,1)-categories]]

$$
  L^H C_1 \simeq L^H C_2
  \,.
$$

=--

+-- {: .proof}
###### Proof

We have to check that $i$ is an [[essentially surjective (∞,1)-functor]] and a [[full and faithful (∞,1)-functor]].

The first condition is immediate from the first assumption. The second follows with prop. \ref{SimplicialLocalizationOfNaturalTransformation} (using prop. \ref{PrePostCompositionWithWeakEquivalences}) from the second assumption.

=--

### Simplicial localization of model categories

+-- {: .num_prop}
###### Proposition

Let $C$ be a [[simplicial model category]]. Write $C^\circ$ for the full $Set$-subcategory on the fibrant and cofibrant objects. 

Then $C^\circ$ and $L^H C$ are connected by an [[equivalence of (∞,1)-categories]].

=--

This is one of the central statements in ([DwyerKanFunctionComplexes](#DwyerKanFunctionComplexes)). The weak homotopy equivalence between $C^\circ(X,Y)$ and $L^H C(X,Y)$ is in corollary 4.7. The equivalence of $\infty$-categories stated above follows with this and the diagram of morphisms of simplicial categories in prop. 4.8.


## References 

The original articles are

* [[William Dwyer]], [[Dan Kan]], 

  _Simplicial localizations of categories_ , J. Pure Appl. Algebra 17 (1980), 267&#8211;284. ([pdf](http://www.nd.edu/~wgd/Dvi/SimplicialLocalizations.pdf))
  {#DwyerKanLocalizations}

  _Calculating simplicial localizations_ , J. Pure Appl. Algebra 18 (1980), 17&#8211;35. ([pdf](http://www.nd.edu/~wgd/Dvi/CalculatingSimplicialLocalizations.pdf))
  {#DwyerKanCalculating}

  _Function complexes in homotopical algebra_ , Topology 19 (1980), 427&#8211;440.
  {#DwyerKanFunctionComplexes}
  _Equivalences between homotopy theories of diagrams_ , Algebraic topologx and algebraic K-theory, (Princeton, N.J. 1983) , Ann. of Math. Stud. 113, Princeton University Press, Princeton, N.J. 1987 .
  {#DwyerKanEquivalences}


* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]],  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories
and Homotopical Categories]]_ , volume 113 of Mathematical Surveys and Monographs


A survey of the general topic involved here can be found in the following paper:

* [[Tim Porter]], _$S$-Categories, $S$-groupoids, Segal categories and quasicategories_ ([arXiv](http://arxiv.org/abs/math/0401274))

Hammock localization is described in Section 4.1 there.

A useful quick collection of facts can be found at the beginning of Section 2 in the following paper:

* [[Clark Barwick]], _On (enriched) Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

[[!redirects simplicial localizations]]


[[!redirects Dwyer-Kan localization]]
[[!redirects Dwyer-Kan localisation]]
[[!redirects Dwyer?Kan localization]]
[[!redirects Dwyer?Kan localisation]]
[[!redirects Dwyer--Kan localization]]
[[!redirects Dwyer--Kan localisation]]
[[!redirects Hammock-Localization]]
[[!redirects Hammock localization]]
[[!redirects Hammock localisation]]

[[!redirects hammock localization]]
[[!redirects hammock localizations]]

