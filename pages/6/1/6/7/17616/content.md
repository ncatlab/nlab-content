
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _pro-manifold_ is a [[pro-object]] in a [[category]] of [[manifolds]], i.e. a formal [[projective limit]] of [[manifolds]].

Details depend on what exactly is understood by "[[manifold]]", i.e. whether [[topological manifolds]] or [[smooth manifold]], etc. 

Typically one wants to mean [[pro-objects]] in manifolds of [[finite number|finite]] [[dimensions]], the point being then that a pro-manifold is like an [[infinite-dimensional manifold]] but with "mild" infinite dimensionality, expressed by the very fact that it may be presented as a formal projective limit of finite dimensional manifolds.

To amplify this specification, one should properly speak of "pro-(finite dimensional smooth manifolds)", but beware that people often abbreviate to "pro-manifold" regardless. Also "pro-finite manifold" is in use, which however, strictly speaking, is a misnomer since a "finite manifold" is one with a [[finite number]] of points.

An important example of pro-objects in finite-dimensional smooth manifolds are infinite [[jet bundles]]. These are the formal projective limits of the underlying finite-order jet bundles.


## Pro-Cartesian spaces


### Embedding into smooth loci

+-- {: .num_defn #proCartSp}
###### Definition

Write [[CartSp]] for the [[full subcategory]] of that of [[smooth manifolds]] on the [[Cartesian spaces]], i.e. on those of the form $\mathbb{R}^n$, for $n \in \mathbb{N}$. Write 

$$
  ProCartSp \coloneqq Pro(CartSp)
$$ 

for its category of [[pro-objects]], the **pro-Cartesian spaces**.

=--

+-- {: .num_prop #ProCartSpFullyFaithfulInSmoothLoc}
###### Proposition

The functor which sends a formal cofiltered limit of Cartesian spaces to its actual [[cofiltered limit]] of [[smooth loci]] is a [[fully faithful functor]], hence constitutes a [[full subcategory]] inclusion of [[pro-Cartesian spaces]] (def. \ref{proCartSp}) into [[smooth loci]]:

$$
  Pro(CartSp) \hookrightarrow SmthLoc
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $Pro(\mathcal{C}) \simeq (Ind(\mathcal{C}^{op}))^{op}$ ([remark](pro-object#ProObjectAsFormalDualOfIndObject)) it is sufficient to show that the functor in question is on opposite categories a fully faithful functor of the form

$$
  Ind(CartSp^{op})
    \hookrightarrow
  SmthLoc^{op} = SmthAlg_{\mathbb{R}}
  \,,
$$

where $SmthAlg_{\mathbb{R}}$ is the category of [[smooth algebras]].

Now, there is the [[fully faithful functor]] 

$$
  i \;\colon\; CartSp \hookrightarrow SmthLoc 
$$ 

([prop.](smooth+locus#SmoothManifoldsFullSubcategoryOfSmoothLoci)) hence a fully faithful functor

$$
  i^{op} \colon CartSp^{op} \hookrightarrow SmthAlg_{\mathbb{R}}
  \,.
$$ 

Moreover, the image of the latter is in [[compact objects]] $i^{op} \colon CartSp^{op} \hookrightarrow (SmthAlg_{\mathbb{R}})_{cpt} \hookrightarrow SmthAlg$, because

$$
  C^\infty(\mathbb{R}^n) \simeq y(\mathbb{R}^n)
  \in 
  SmthAlg_{\mathbb{R}} \simeq Func_\times(CartSp,Set)
$$

is [[representable functor|co-representable]], hence [[compact object|compact]] (by the [[Yoneda lemma]] and since colimits are computed objectwise [prop.](limits+and+colimits+by+example#LimitsOfPresheaves)).

This implies that the composite

$$
  Ind(CartSp^{op})
   \overset{Ind(i^{op})}{\hookrightarrow}
  Ind(SmthAlg_{\mathbb{R}})
    \overset{L}{\longrightarrow}
  SmthAlg_{\mathbb{R}}
$$

is also fully faithful ([prop.](ind-object#JFIsFullyFaithful)).

Here $Ind(i^{op})$ takes formal filtered colimits in $CartSp^{op}$ to the corresponding formal colimits in $SmthAlg_{\mathbb{R}}$ ([prop.](ind-object#FunctorialityOfInd)), while $L$ takes formal filtered colimits to actual [[filtered colimits]] ([prop.](ind-object#ReflectionToYonedaEmbedding)). Hence this is indeed the functor in question.

=--

### The site of towers of Cartesian spaces and pro-morphisms
 {#SiteOfTowersOfCartesianSpaces}

> under construction


+-- {: .num_defn #TowersOfCartesianSpaces}
###### Definition

Write

$$
  TowCartSp \hookrightarrow ProCartSp
$$

for the [[full subcategory]] of the category of [[pro-Cartesian spaces]] (def. \ref{proCartSp}) on those [[pro-objects]] in [[CartSp]] which are presented as formal [[sequential limits]] of [[tower]] diagrams, i.e. where the indexing category $\mathcal{K} = \mathbb{N}_{\geq}$.

=--


+-- {: .num_defn #ProGoodOpenCoverOnACartesianSpace}
###### Definition

For $U \in TowCartSp$ a [[tower of Cartesian spaces]]  (def. \ref{TowersOfCartesianSpaces}), say that a **tower of [[good open covers]]** of $U$ is a sequence of morphisms $\{U_i \overset{\phi_i}{\to} U\}$ in $TowCartSp$ such that these are the formal [[sequential limit]] of a cofiltered diagram of [[good open covers]] $\{U_i^k \overset{\phi_i^k}{\to} U^k\}$.

$$
  \array{
    U_i^{k} &\overset{\underset{\longleftarrow}{\lim}^f}{\mapsto}& U_i
    \\
    {}^{\mathllap{\phi_i^k}}\downarrow && \downarrow^{\mathrlap{\phi_i}}
    \\
    U^k &\overset{\underset{\longleftarrow}{\lim}^f}{\mapsto}& U
  } 
$$


=--

+-- {: .num_defn }
###### Definition

The collection of towers of [[good open covers]] on $TowCartSp$, according to def. \ref{ProGoodOpenCoverOnACartesianSpace}, constitutes a [[coverage]].

=--

+-- {: .proof}
###### Proof

By the definition of [[coverage]] ([def.](coverage#ConditionsOnACoverage)) we need to check that for every tower of [[good open covers]] $\{U_i \overset{\phi_i}{\to} U\}$ and for every morphism $V \overset{g}{\longrightarrow} U$ in $TowCartSp$, there exists a tower of [[good open covers]] $\{V_j \overset{\psi_j}{\longrightarrow} V\}$ of $V$ such that for each index $j$ we may find an index $i$ and a morphism $V_j \overset{}{\to} U_i$ such as to make a [[commuting diagram]] of the form

$$
  \array{
    V_j &\overset{}{\longrightarrow}& U_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi_i}}
    \\
    V &\underset{g}{\longrightarrow}& U
  }
  \,.
$$

Now by [this prop.](tower#ProMorphismsBetweenTowerDiagrams) the bottom morphism is represented by a sequence of component morphisms

$$
  V^{n(k)} \overset{}{\longrightarrow} U^k
  \,.
$$

Since ordinary [[good open covers]] do form a [[coverage]] on [[CartSp]] ([prop.](good+open+cover#GoodOpenCoversFormACoverageOnParacompactSmooothManifolds)) each of these component diagrams may be completed

$$
  \array{
    \tilde V^{n(k)}_j &\overset{}{\longrightarrow}& U^k_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi^k_i}}
    \\
    V^{n(k)} &\underset{g^k}{\longrightarrow}& U^k
  }
$$

by first forming the [[pullback]] [[open cover]] $(g^k)^\ast U^k_i \to V^{n(k)}$ and then refining this to a [[good open cover]] $\tilde V^{n(k)}_j \to V^{n(k)}$. By the [[universal property]] of the [[pullback]], there are morphisms

$$
  \tilde V^{n(k+1)} \longrightarrow (g^k)^\ast U^k_i
$$

that make the evident cube commute 

$$
  \array{
    \tilde V^{n(k+1)}_j &\overset{}{\longrightarrow}& U^{k+1}_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi^{k+1}_i}}
    \\
    V^{n(k+1)} &\underset{g^{k+1}}{\longrightarrow}& U^{k+1}
  }  
  \;\;\;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    (g^{k})^\ast U_i^k &\overset{}{\longrightarrow}& U^k_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi^k_i}}
    \\
    V^{n(k)} &\underset{g^k}{\longrightarrow}& U^k
  }  
$$


Take 

$$
  V^{n(0)}_j \coloneqq \tilde V^{n(0)}_j
$$ 

and then inductively define 

$$
  V^{n(k+1)}_j
$$ 

to be a refinement by a good open cover of the joint refinement of $\{\tilde V^{n(k+1)}_j\}$ with the pullback of $\{V^{n(k)}_j\}$ to $V^{n(k+1)}$.

This refines the above commuting cubes to

$$
  \array{
    V_j^{n(k+1)} &\overset{}{\longrightarrow}& U^{k+1}_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi^{k+1}_i}}
    \\
    V^{n(k+1)} &\underset{g^{k+1}}{\longrightarrow}& U^{k+1}
  }  
  \;\;\;\;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    V_j^{n(k)} &\overset{}{\longrightarrow}& U^k_i
    \\
    \downarrow 
      &&
    \downarrow^{\mathrlap{\phi^k_i}}
    \\
    V^{n(k)} &\underset{g^k}{\longrightarrow}& U^k
  }  
$$

and hence provides components for the required diagram in $TowCartSp$.


=--



[[!redirects pro-manifolds]]

[[!redirects promanifold]]
[[!redirects promanifolds]]

[[!redirects pro-Cartesian space]]
[[!redirects pro-Cartesian spaces]]

[[!redirects tower of Cartesian spaces]]
[[!redirects towers of Cartesian spaces]]
[[!redirects tower of cartesian spaces]]
[[!redirects towers of cartesian spaces]]
