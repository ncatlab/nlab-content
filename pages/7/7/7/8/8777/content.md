
> This is a sub-entry of _[[geometry of physics]]_.

***

#Contents#
* table of contents
{:toc}

## **Principal connections**
 {#PrincipalConnections}



### Model Layer

#### Motivation

* [[Dirac charge quantization]] implies that the [[electromagnetic field]] is not just given by a closed [[differential 2-form]] but by a refinement of that to a [[circle group]] [[principal connection]]

* analogous arguments show that more generally a configuration of the _[[Yang-Mills field]]_ for some [[gauge group]] $G$ is a $G$-[[principal connection]];

* analogous arguments say that the [[B-field]] and the [[C-field]] are given by [[circle n-bundles with connection]] for $n = 2$ and $n = 3$, respectively.

In this way all of [[gauge theory]] is much the study of [[principal connections]] and all of [[higher gauge theory]] is much the study of [[principal infinity-connections]].

More is true: also a configuration of the [[field (physics)|field]] of [[gravity]] is represented by a connection, in this case a _[[Cartan connection]]_, which is a [[Poincare group]]-[[principal connection]] satisfying an extra condition (that "[[vielbein|solders]]" it to the underlying manifold).



#### Deligne cohomology
 {#DeligneCohomology}

It turns out that one of the many equivalent incarnations of [[circle n-bundles with connection]] are [[cocycles]] in [[Deligne cohomology]]. That this is so we discuss below in the [Semantics layer](#SemanticsLayer). Here instead we discuss [[Deligne cohomology]] taken at face value.

##### Preliminaries on sheaf cohomology
 {#PreliminariesOnSheafCohomology}

In order to be somewhat self-contained, this section reviews some elements of [[abelian sheaf cohomology]] specified to the context that we need. It also sets up some notation. The definition of the Deligne complex itself is [below](#TheDeligneComplex) in def. \ref{TheSmoothDeligneComplex}.

Recall the following definition, which is discussed in much detail in the chapter _[[geometry of physics -- smooth sets]]_.

+-- {: .num_defn #Smooth0Types}
###### Definition

Write [[CartSp]] for the [[site]] whose 

* [[objects]] are [[Cartesian space]]  $\mathbb{R}^n$ for $n \in \mathbb{N}$, 

* [[morphisms]] are [[smooth functions]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ between these;

*  whose [[coverage]] is given by "differentially [[good open covers]]", those [[open covers]] of $\mathbb{R}^n$s all whose finite non-empty intersections are [[diffeomorphism|diffeomorphic]] to an [[open ball]], hence again to $\mathbb{R}^n$.

Write $PSh(CartSp) = Func(CartSp^{op},Set)$ for the [[category of presheaves]] over this site. Write

$$
  Smooth0Type \coloneqq Sh(CartSp)
$$

for its [[category of sheaves]], also called the [[cohesive topos]] of [[smooth spaces]].

=--

+-- {: .num_remark}
###### Remark

Instead of the site [[CartSp]] of def. \ref{Smooth0Types} one could use the site [[SmoothMfd]] of all smooth manifolds. All of the statements and constructions in the following go through in that case just as well. In fact [[CartSp]] is a [[dense subsite]] of [[SmoothMfd]]. On the one hand this implies that the [[abelian sheaf cohomology]] is the same for both sites, but on the other hand means that it is convenient to restrict to the much "smaller" site of Cartesian spaces. In fact since the [[stalks]] of sheaves over smooth manifolds are evaluations on small [[open balls]] and since every open ball is [[diffeomorphism|diffeomorphic]] to a Cartesian space, many statements that are true (only) stalkwise over [[SmoothMfd]] are actually true globally over $CartSp$. It is the "[[descent]]" or "[[infinity-stackification]]" which is implicit in abelian sheaf cohomology that takes care of these global statements over [[CartSp]] to translate into the same local statements as one gets over [[SmoothMfd]].

=--

+-- {: .num_example #RepresentableSheavesAndTheirConstantVersion}
###### Example

The assignment $C^\infty(-,\mathbb{R}) \colon \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n,\mathbb{R})$ of [[smooth functions]] with values in the [[real numbers]] is a [[sheaf]]. Since this is [[representable functor|representable]] we are entitled to identify this with the [[smooth manifold]] $\mathbb{R}$ (the [[real line]]) itself, and just write $\mathbb{R} \in Sooth0Type$. 

Similarly for $X$ any other [[smooth manifold]], it represents a sheaf on [[CartSp]] and we just write $X \in Smooth0Type$ for this.

Of particular interest below is the case where $X = S^1 = \mathbb{R}/\mathbb{Z} = U(1)$ is the [[circle]], to be regarded as the [[circle group]].

Notice that traditionally the sheaf represented by $\mathbb{R}$ or $U(1)$ is indicated by an underline as in $\underline{\mathbb{R}}$ and $\underline{U}(1)$, but we do not follow this tradition here. 

Instead, if we consider the other sheaf that might deserve to be denoted by $\mathbb{R}$, namely the [[constant sheaf]] on $\mathbb{R}$, which sends each $U \in CartSp$ to the set underlying $\mathbb{R}$, then we write $\flat \mathbb{R}$ for that. Similarly 

$$
  \flat U(1) \in Smooth0Type
$$ 

is the sheaf sending each test manifold to the set of points in the circle, and each smooth function between Cartesian spaces to the identity function on that set.


=--

+-- {: .num_example #SheavesOfFormsAndDeRhamDifferential}
###### Example

For $k \in \mathbb{N}$ write 

$$
  \mathbf{\Omega}^k \in Sh(CartSp)
$$ 

for the [[sheaf]] $\mathbf{\Omega}^k \colon U \mapsto \Omega^k(U)$ of smooth [[differential n-forms|differential k-forms]] on $X$.
The [[de Rham differential]] extends to a morphism of sheaves

$$
  \mathbf{d} \colon \mathbf{\Omega}^k \to \mathbf{\Omega}^{k+1}
  \,.
$$

For positive $k$ its [[kernel]] is the [[subfunctor|sub-sheaf]]

$$
  0 \to 
  \mathbf{\Omega}^k_{cl} \hookrightarrow \mathbf{\Omega}^k
  \stackrel{\mathbf{d}}{\longrightarrow}
  \mathbf{\Omega}^{k+1}
$$

of closed differential forms; and for $k = 0$ its kernel is the
[[subfunctor|sub-sheaf]] of constant functions

$$
  0 \to
  \flat \mathbb{R} \hookrightarrow \mathbb{R} 
  \stackrel{\mathbf{d}}{\longrightarrow}
  \mathbf{\Omega}^1
  \,.
$$


=--


In the background, what plays a role for the following is the full [[cohesive (∞,1)-topos|cohesive]] [[homotopy theory]] of [[smooth ∞-groupoids]]. This receives a map from the following coarse [[homotopy theory]] of [[chain complexes]] of [[abelian sheaves]], which is all that is necessary for the present purpose.



+-- {: .num_defn #FibrantOnjectStructureOnChSmooth}
###### Definition

Write

$$
  Ch_+(Smooth0Type)
  =
  Ch_+(Sh(CartSp))
  =
  Sh(CartSp,Ch_+)
$$

for the [[category of chain complexes]] in the smooth sheaves of def. \ref{Smooth0Types}, hence for the [[1-category]] whose objects are [[chain complexes]] of [[abelian sheaves]] on $CartSp$.

Regard this as equipped with the structure of a [[category of fibrant objects]] induced by the [[projective model structure on chain complexes]], hence with classes of [[morphisms]] labeled as follows: a [[chain map]] $f_\bullet \colon A_\bullet \to B_\bullet$ is called

*  a _[[weak equivalence]]_ if it is a [[quasi-isomorphism]], hence if it induces [[isomorphisms]] on ([[sheaves]] of) [[chain homology]] groups;

* a _[[fibration]]_ if it is an [[epimorphism]] (of [[abelian sheaves]]) in positive degree.

=--

+-- {: .num_remark #HomotopyFibersViaFactorizationLemma}
###### Remark

For our purpose the main use of this structure is to compute [[homotopy fibers]] via the [[factorization lemma]]. Namely 

1. every chain map may be replaced, up to weak equivalence of its domain, by a fibration;

1. the [[homotopy fiber]] of a chain map is the ordinary fiber of any of its fibration replacements.

=--

+-- {: .num_remark}
###### Remark

That the properties in def. \ref{FibrantOnjectStructureOnChSmooth} 
are interpreted in sheaves simply means that they apply [[stalk]]-wise.
For instance a morphism of chain complexes of presheaves
$f_\bullet \colon A_\bullet \to B_\bullet$ is a weak equivalence
precisely if the underlying presheaf of chain complexes becomes
a [[quasi-isomorphism]] for each point $x$ in each Cartesian space
$\mathbb{R}^n$ after restricting 
(via the presheaf structure maps) to a small enough [[open neighbourhood]]
of that point. Similarly for epimorphisms.

=--


+-- {: .num_remark #HomotopyPullbacksPreservedbyInclusionIntoAllSmoothHomotopyTypes}
###### Remark

There is a canonical map of [[homotopy theories]] from $Ch_+(Smooth0Type)$ to the full [[(∞,1)-topos]] [[Smooth∞Grpd]] which is given by applying the [[Dold-Kan correspondence]] followed by [[∞-stackification]]. The key point is that this map preserves [[homotopy fiber products]], which is the [[universal construction]] that already captures most of the relevant properties of the Deligne complex. In this way it is sufficient to concentrate on $Ch_+(Smooth0Type)$ for much of the theory.



=--


When writing out the components of chain complexes we will use square brackets always denote the group in degree-0 to the far right, and the group in degree $k$ being $k$ steps to the left from that.

+-- {: .num_example #DeloopingsOfAbelianSheaf}
###### Example

For $A \in Ab(Smooth0Type) = Sh(CartSp,Ab)$ any [[abelian sheaf]] and for $n \in \mathbb{N}$ we write

$$
  (\mathbf{B}^n A)_{\bullet}
  \coloneqq
  A[-n]
  =
  \left[
     A

     \to 0 \to \cdots \to 0
  \right]
$$

for the [[chain complex]] of sheaves concentrated on $A$ in degree $n$.


=--

+-- {: .num_example #LogDiffInSmoothContext}

###### Example

There is a weak equivalence, def. \ref{FibrantOnjectStructureOnChSmooth},


$$
  \left[\mathbb{Z}\to \mathbb{R} \right]
  \stackrel{\simeq}{\longrightarrow}
  U(1)
$$

given by the [[chain map]]

$$
  \array{
     \mathbb{Z} &\hookrightarrow& \mathbb{R}
     \\
     \downarrow && \downarrow^{\mathrlap{mod\,\mathbb{Z}}}
     \\
     0 &\to& U(1)
  }
$$

(which is just the [[exponential sequence]] regarded as a chain map).

The de Rham differential [[extension|extends]] through this equivalence
to produce a morphism denoted $\mathbf{d} log$:

$$
  \array{
    (\mathbb{Z} \to \mathbb{R}) &\stackrel{\mathbf{d}}{\longrightarrow}&
    \mathbf{\Omega}^1
    \\
    \downarrow^{\mathrlap{\simeq}} & \nearrow_{\mathrlap{\mathbf{d} log}}
    \\
    U(1) 
    \,.
  }
$$

On a given $U(1)$-valued function this is given by
representing the function by a smooth $\mathbb{R}$-valued function
under mod-$\mathbb{Z}$-reduction
(which is always possible over a [[Cartesian space]]) and applying the 
de Rham differential to that.

The [[kernel]] of that is the constant sheaf $\flat U(1)$ 
of example \ref{RepresentableSheavesAndTheirConstantVersion}

$$
  0 \to
  \flat U(1) \hookrightarrow U(1)
  \stackrel{\mathbf{d} log}{\longrightarrow}
  \mathbf{\Omega}^1
  \,.
$$


=--


Under addition of differential forms, the sheaves $\mathbf{\Omega}^k$ of example \ref{SheavesOfFormsAndDeRhamDifferential} becomes [[abelian sheaves]], and we will implicitly understand them this way now.


+-- {: .num_defn #DeRhamResolutionOfConstantFunctions}
###### Definition

Write $\widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet \in Ch(Smooth0Type)$ for the complex of sheaves given by the truncated [[de Rham complex]]:

$$
  \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
  \coloneqq
  \left[
    \mathbb{R}
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^1
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^2
    \stackrel{\mathbf{d}}{\to}
    \cdots    
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^{n+1}_{cl}
  \right]
  \,.
$$

=--

+-- {: .num_prop #TheDeRhamResolutionOfConstantFunctions}
###### Proposition

The morphism

$$
  (\flat \mathbf{B}^{n+1}\mathbb{R})_\bullet
  \longrightarrow
  \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
$$

given by the canonical [[chain map]]

$$
  \array{
    \flat \mathbb{R}
    &\stackrel{}{\to}&
    0
    &\stackrel{}{\to}&
    0
    &\stackrel{}{\to}&
    \cdots    
    &\stackrel{}{\to}&
    0
    \\
    \downarrow && \downarrow && \downarrow && \cdots
    && \downarrow
    \\
    \mathbb{R}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^2
    &\stackrel{\mathbf{d}}{\to}&
    \cdots    
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n+1}_{cl}
  }
$$

is a weak equivalence in the sense of def. \ref{FibrantOnjectStructureOnChSmooth}.

=--

+-- {: .proof}
###### Proof

By the [[Poincaré lemma]]. This _is_ the Poincar&#233; Lemma.

=--

Every $A_\bullet \in Ch_+(Smooth0Type)$ serves as the [[coefficients]] for an [[abelian sheaf cohomology]] theory on smooth manifolds. Abelian sheaf cohomology has a general abstract characterization (see at _[[cohomology]]_) in terms of [[derived hom-spaces]]. For definiteness, we recall the model for this construction given by [[Cech cohomology]]
.
+-- {: .num_defn #CechComplex}
###### Definition
**(&#268;ech complex)**

Let $X$ be a [[smooth manifold]] and let $A_\bullet \in Ch_+(Smooth0Type)$ be a sheaf of chain complexes. Let $\{U_i \to X\}$ be a [[good open cover]] of $X$, i.e. an open cover such that each finite non-empty intersection $U_{i_0, \cdots, i_k}$ is [[diffeomorphism|diffeomorphic]] to an [[open ball]]/[[Cartesian space]].

The **&#268;ech cochain complex** $C^\bullet((X,\{U_i\}),A_\bullet)$ 
of $X$ with respect to the cover $\{U_i \to X\}$ and with [[coefficients]] in $A_\bullet$ is in degree $k \in \mathbb{N}$ given by the [[abelian group]]

$$
  C_k((X,\{U_i\}),A_\bullet)
  \coloneqq
  \oplus_{{l,n} \atop {k = l-n}}
  \oplus_{i_0, i_1, \cdots, i_n}
  A_l(U_{i_0, \cdots, i_n})
$$


which is the [[direct sum]] of the values of $A_\bullet$ on the given intersections as indicated; and whose [[differential]] 

$$
  d
  \colon
  C^{k}((X,\{U_i\}),A_\bullet)
  \longrightarrow
  C^{k+1}((X,\{U_i\}),A_\bullet)
$$

is defined componentwise (see at [[matrix calculus]] for conventions on maps between [[direct sums]]) by

$$
  \begin{aligned}
    (d a)_{i_0, \cdots, i_{k+1}} 
    & \coloneqq 
    (\partial_A + (-1)^k \delta a)_{i_0, \cdots, i_{k+1}} 
    \\
    & \coloneqq
    \partial_A a_{i_0, \cdots, i_{k+1}}
    +
    (-1)^k
    \sum_{0 \leq j \leq k+1} (-1)^{j}
    a_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_{k+1}} 
    |_{U_{i_0, \cdots, i_{k+1}}}
  \end{aligned}
$$

where on the right the sum is over all components of $a$ obtained via the canonical restrictions obtained by discarding one of the original $(k+1)$ subscripts.

The **Cech cohomology** groups of $X$ with coefficients in $A_\bullet$ __relative to the given cover__ are the [[chain homology]] groups of the Cech complex

$$
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \coloneqq
  H^k(C^\bullet((X,\{U_i\}),A_\bullet))
  \,.
$$

The **Cech cohomology** groups as such as the [[colimit]] of these groups over refinements of covers

$$
  H^k_{Cech}(X, A_\bullet)
  \coloneqq
  \underset{\longrightarrow}{\lim}_{\{U_i \to X\}}
  H_{Cech}^k((X,\{U_i\}), A_\bullet)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Often Cech cohomology is considered for the case that $A_\bullet$ is concentrated in a single degree, in which case the first term in the sum defining the differential in def. \ref{CechComplex} disappears. 
When $A_\bullet$ is not concentrated in a single degree, then for emphasis one sometimes speaks of _[[hypercohomology]]_. This is the case of relevance for Deligne cohomology.

=--


+-- {: .num_remark}
###### Remark

The Cech chain complex in def. \ref{CechComplex} is the [[total complex]] of the [[double complex]] whose vertical differential is that of $A_\bullet$ and whose horizontal differential is the _Cech differential_ $\delta$ given by alternating sums over restrictions along patch inclusions

$$
  \array{
     \vdots && \vdots
     \\
     \downarrow^{\mathrlap{\partial_A}}
     &&
     \downarrow^{\mathrlap{\partial_A}}
     \\
     \oplus_i A_1(U_i)
     &\stackrel{\delta}{\longrightarrow}&
     \oplus_{i_1, i_2} A_1(U_{i_1, i_2})
     &\stackrel{\delta}{\longrightarrow}&
     \cdots
     \\
     \downarrow^{\mathrlap{\partial_A}}
     &&
     \downarrow^{\mathrlap{\partial_A}}
     \\
     \oplus_i A_0(U_i)
     &\stackrel{\delta}{\longrightarrow}&
     \oplus_{i_1, i_2} A_0(U_{i_1, i_2})
     &\stackrel{\delta}{\longrightarrow}&
     \cdots
  }
$$

=--


+-- {: .num_remark #GoodCoverCechCohomologyIsHomotopicallyGood}
###### Remark

For analyzing the properties of Deligne cohomology [below](#Properties), all one needs is the following fact about [[Cech cohomology]], which is discussed for instance at  _[[infinity-cohesive site]]_:

For $X$ a [[smooth manifold]] (in particular [[paracompact topological space|paracompact]]), 

1. $X$ admits a [[good open cover]] $\{U_i \to X\}$ (by [[charts]] $U_i$ all whose finite non-empty intersections are [[diffeomorphism|diffeomorphic]] to an [[open ball]]/[[Cartesian space]] $\mathbb{R}^n$);

1. for any such good open cover the [Cech complex](&#268;ech+cohomology#CechComplex) $C^\bullet((X,\{U_i\}),A_\bullet)$ already computes Cech cohomology (i.e. there is no further need to form the [[colimit]] of Cech complexes over refinements of covers);

1. the functor $C^\bullet((X,\{U_i\}),-) \colon Ch_+(Smooth0Type) \to Ch_+$ preserves weak equivalences and fibrations. 

This means in particular that if $X_\bullet \to Y_\bullet \to Z_\bullet$ is a [[homotopy fiber sequence]] in $Ch_+(Smooth0Type)$, then also 

$$
  C^\bullet((X,\{U_i\}), X_\bullet) 
    \to 
  C^\bullet((X,\{U_i\}), Y_\bullet)
    \to 
  C^\bullet((X,\{U_i\}), Z_\bullet)
$$

is a homotopy fiber sequence of chain complexes, and therefore the [[cohomology groups]] sit in the [[long exact sequence in homology]] of this sequence of chain complexes.


=--




+-- {: .num_example #DeRhamTheorem}
###### Example

Passing to [[abelian sheaf cohomology]] (e.g. via def. \ref{CechComplex}),
then prop. \ref{TheDeRhamResolutionOfConstantFunctions}
is the [[de Rham theorem]].

=--

We will have need to give names to truncations of the de Rham complex. One is this:

+-- {: .num_defn #TruncatedDeRham}
###### Definition

For $n \in \mathbb{N}$ write

$$
  \mathbf{\Omega}^{\bullet \leq n} \in Ch_+(Smooth0Type)
$$

for the [[chain complex]] of the form

$$
  \mathbf{\Omega}^{\bullet \leq n}
  \coloneqq
  \left[
     \mathbb{R}
     \stackrel{\mathbf{d}}{\to}
     \mathbf{\Omega}^1 
     \stackrel{\mathbf{d}}{\to}
     \cdots
     \stackrel{\mathbf{d}}{\to}
     \mathbf{\Omega}^{n-1}
     \stackrel{\mathbf{d}}{\to}
     \mathbf{\Omega}^{n}
  \right]
$$

with all $n$-forms, not just the closed ones, in degree 0.


=--

+-- {: .num_example #CohomologyWithCoefficientsInTruncatedDeRham}
###### Example

The [[abelian sheaf cohomology]] of the truncated
de Rham complex in def. \ref{TruncatedDeRham}
is $\Omega^n(X)/im(\mathbf{d})$.

=--






##### The Deligne complex
 {#TheDeligneComplex}

+-- {: .num_defn #TheSmoothDeligneComplex}
###### Definition


For $n \in \mathbb{N}$ the **smooth Deligne complex** of degree $n$

$$
  (\mathbf{B}^n U(1)_{conn})_\bullet
  \in 
  Ch_+(Smooth0Type)
$$

is the [[chain complex]] of [[abelian sheaves]] given by

$$
  (\mathbf{B}^n U(1)_{conn})_\bullet
  \;
   \coloneqq
  \;
  \left[
    U(1) \stackrel{\mathbf{d} log}{\to}
    \mathbf{\Omega}^1
    \stackrel{\mathbf{d}}{\to} 
     \cdots 
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^n
  \right]
$$

with $U(1)$ in degree $n$ and with the differentials as
in def. \ref{SheavesOfFormsAndDeRhamDifferential} and example \ref{LogDiffInSmoothContext}.

=--

+-- {: .num_remark #RModZResolutionOfU1DeligneComplex}
###### Remark

By example \ref{LogDiffInSmoothContext}
the obvious [[chain map]]

$$
  \array{
    \mathbb{Z}    
    &\hookrightarrow&
    \mathbb{R}
      &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^1
     &\stackrel{\mathbf{d}}{\to}& 
       \cdots 
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^n
    \\
    \downarrow
    &&
    \downarrow^{\mathrlap{(-)/\mathbb{Z}}}
    &&
    \downarrow^{id}
    &&
    &&
    \downarrow^{id}
    \\
    0 
    &\to&
    U(1)
      &\stackrel{\mathbf{d} log}{\to}&
     \mathbf{\Omega}^1
     &\stackrel{\mathbf{d}}{\to}& 
       \cdots 
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^n
  }
$$

is a weak equivalence, def. \ref{FibrantOnjectStructureOnChSmooth},
and one could define the top chain complex here as "the" Deligne complex,
just as well. In the context of [[homotopy theory]]/[[homological algebra]],
all that matters is the complex up to [[zig-zags]] of
weak equivalences.

=--



+-- {: .num_remark}
###### Remark


In def. \ref{TheSmoothDeligneComplex} the de Rham complex is truncated to the right by discarding what would be the next differentials, without passing to their [[kernel]], i.e. in degree 0 the Deligne complex has all differential $n$-forms, not just the closed $n$-fomrs. This simple point is the key aspect of the Deligne complex. If one instead truncates while preserving the chain homology in the lowest degree, then one obtains the following complex with the sheaf $\mathbf{\Omega}^{n}_{cl}$ of _closed_ forms in lowest degree, which gives [[ordinary cohomology]].

=--

+-- {: .num_defn #FlatSmoothDeligneComplex}
###### Definition

For $n \in \mathbb{N}$ the **flat smooth Deligne complex** of degree $n$

$$
  (\mathbf{B}^n U(1)_{flat})_\bullet
  \in 
  Ch_+(Smooth0Type)
$$

is the [[chain complex]] of [[abelian sheaves]] given by

$$
  (\mathbf{B}^n U(1)_{flat})_\bullet
  \;
   \coloneqq
  \;
  \left[
    U(1) \stackrel{\mathbf{d} log}{\to}
    \mathbf{\Omega}^1
    \stackrel{\mathbf{d}}{\to} 
     \cdots 
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^n_{cl}
  \right]
$$

with $U(1)$ in degree $n$ and with the differentials as
in def. \ref{SheavesOfFormsAndDeRhamDifferential} and example \ref{LogDiffInSmoothContext}, and with the _closed_ $n$-forms
on the right.

=--

+-- {: .num_defn #FlatBnU1}
###### Definition

Write 

$$
  (\flat\mathbf{B}^n U(1))_\bullet
  =
  (\mathbf{B}^n \flat U(1))_\bullet
  \in 
  Ch_+(Smooth0Type)
$$

for the [[chain complex]] of [[abelian sheaves]] given by

$$
  (\flat \mathbf{B}^n U(1))_\bullet
  \;
   \coloneqq
  \;
  \left[
    \flat U(1) \stackrel{}{\to}
    0
    \stackrel{}{\to} 
     \cdots 
    \stackrel{}{\to}
    0
  \right]
$$

with the constant sheaf $\flat U(1)$ of example \ref{RepresentableSheavesAndTheirConstantVersion} 
in degree $n$.

=--

+-- {: .num_prop #TwoEquivalentModelsForFlatBnU1}
###### Proposition

For $(\flat \mathbf{B}^n U(1))_\bullet$ as in def. \ref{FlatBnU1},
then the morphism 

$$
  (\flat \mathbf{B}^n U(1))_\bullet
  \stackrel{\simeq}{\longrightarrow}
  (\mathbf{B}^n U(1)_{flat})_\bullet
$$

given by the [[chain map]]

$$
  \array{
    \flat U(1) &\to& 0 &\to& \cdots &\to& 0
    \\
    \downarrow && \downarrow  && \cdots && \downarrow 
    \\
    U(1) 
     &\stackrel{\mathbf{d}log}{\to}& 
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^n_{cl}
  }
$$

(with the vertical morphism on the left being the 
inclusion of example \ref{LogDiffInSmoothContext}) 
is a weak equivalence, def. \ref{FibrantOnjectStructureOnChSmooth}.

=--

+-- {: .proof}
###### Proof

By the [[Poincaré lemma]], this is just an immediate variant of 
prop. \ref{TheDeRhamResolutionOfConstantFunctions}.

=--


##### Curvature and characteristic classes
 {#CharacteristicMaps}

We discuss the construction of two canonical morphisms out of Deligne cohomology,
and two canonical morphisms into it. Below these are shown to form two interlocking [[exact sequences]] and in fact an exact [[differential cohomology hexagon]] which accurately characterizes Deligne cohomology as the [[differential cohomology]] extension of integral [[ordinary cohomology]] by [[differential forms]].

Throughout, for ease of notation, we assume $n \in \mathbb{N}$ to be positive, 

$$
  n \geq 1
  \,.
$$

The remaining case $n = 0$ describes "circle 0-bundles with connection", which are just $U(1)$-valued functions, and is hence essentially trivial in itself.

In the following $X$ is any [[smooth manifold]].

+-- {: .num_defn #UnderlyingBundleMap}
###### Definition

Let $(\mathbf{B}^{n+1}\mathbb{Z})_\bullet \in Ch_+(Smooth0Type)$
be as in example \ref{DeloopingsOfAbelianSheaf}. Write 

$$
  (\mathbf{B}^n U(1)_{conn})_{\bullet}
  \stackrel{\simeq}{\longleftarrow}
  \stackrel{DD_\bullet}{\longrightarrow}
  (\mathbf{B}^{n+1} \mathbb{Z})_{\bullet}
$$

for the [[zig-zag]] of chain complexes where the left 
weak equivalence is that  of remark \ref{RModZResolutionOfU1DeligneComplex}, i.e. for the [[chain maps]] given by

$$
  \array{
     \mathbb{Z} 
     &\to&
     0
     &\to&
     0
     &\to&
     \cdots  
     &\to&
     0
     \\
     \uparrow^{\mathrlap{id}}
     &&
     \uparrow^{\mathrlap{}}
     &&
     \uparrow^{\mathrlap{}}
     &&
     \cdots
     &&
     \uparrow^{\mathrlap{}}   
     \\
     \mathbb{Z}
     &\hookrightarrow&
     \mathbb{R}
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^1
     &\stackrel{\mathbf{d}}{\to}&
     \cdots
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^n
     \\
     \downarrow^{\mathrlap{0}}
     &&
     \downarrow^{\mathrlap{mod\,\mathbb{Z}}}
     &&
     \downarrow^{\mathrlap{id}}
     &&
     \cdots
     &&
     \downarrow^{\mathrlap{id}}
     \\
     0 &\to&
     U(1)
     &\stackrel{\mathbf{d} log}{\to}&
     \mathbf{\Omega}^1
     &\stackrel{\mathbf{d}}{\to}&
     \cdots
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^n
  }
$$

Passing to [[abelian sheaf cohomology]] this gives a morphism

$$
  \array{
     H^{n+1}_{conn}(X,\mathbb{Z})
     \\
     & \searrow^{\mathrlap{DD}}
     \\
     && H^{n+1}(X,\mathbb{Z})
  }
$$

from Deligne cohomology to [[ordinary cohomology]] with [[integer]] [[coefficients]] in degree $n+1$.

For $[\nabla] \in H^{n+1}_{conn}(X,\mathbb{Z})$ 
we call $DD(\nabla) \in H^{n+1}(X,\mathbb{Z})$  
the [[Dixmier-Douady class]] of the _underlying [[circle n-bundle]]_.

=--

+-- {: .num_defn #CurvatureMap}
###### Definition

Write

$$
  (F_{(-)})_\bullet
  \colon
  (\mathbf{B}^n U(1)_{conn})_\bullet
  \stackrel{}{\longrightarrow}
  \mathbf{\Omega}^{n+1}_{cl}
$$

for the morphism given by the chain map which is just the
de Rham differential in degree 0

$$
  \array{
     0 &\to&
     U(1)
     &\stackrel{\mathbf{d} log}{\to}&
     \mathbf{\Omega}^1
     &\stackrel{\mathbf{d}}{\to}&
     \cdots
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^{n-1}
     &\stackrel{\mathbf{d}}{\to}&
     \mathbf{\Omega}^n
     \\
     \downarrow
     &&
     \downarrow
     &&
     \downarrow
     &&
     \cdots
     &&
     \downarrow^{\mathrlap{}}
     &&
     \downarrow^{\mathrlap{\mathbf{d}}}
     \\
     0 
     &\to&
     0
     &\to&
     0
     &\to&
     \cdots
     &\stackrel{}{\to}&
     0
     &\to&
     \mathbf{\Omega}^{n+1}_{cl}     
  }
$$

Passing to [[abelian sheaf cohomology]] this gives a morphism of the form

$$
  \array{
     && \Omega^{n+1}_{cl}(X)
     \\
     & {}^{\mathllap{F_{(-)}}}\nearrow 
     \\
     H^{n+1}_{conn}(X,\mathbb{Z})
  }
$$

We call this the _[[curvature]] map_, i.e. for 
$[\nabla] \in H^{n+1}_{conn}(X,\mathbb{Z})$ 
the class of a Deligne cocycle, we call

$$
  F_\nabla \in \Omega^{n+1}_{cl}(X)
$$

its _[[curvature form]]_.

=--

+-- {: .num_defn #InclusionOfGloballyDefinedConnectionForms}
###### Definition

Consider the [[zig-zag]] 

$$
  \mathbf{\Omega}^{\bullet\leq n}  
  \stackrel{}{\longrightarrow}
  (\mathbf{B}^n U(1)_{conn})_\bullet
$$

out of the complex of def. \ref{TruncatedDeRham},
given by the [[chain maps]]

$$
  \array{
    0 &\to& \mathbb{R} &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^1 &\stackrel{\mathbf{d}}{\to}& \cdots &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^{n-1}
   &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^n
    \\
    \downarrow && \downarrow && \downarrow^{\mathrm{id}}  
    && \cdots && \downarrow^{\mathrm{id}} && \downarrow^{\mathrm{id}}
    \\
    \mathbb{Z}
    &\hookrightarrow&
    \mathbb{R}
     &\stackrel{\mathbf{d}}{\to}& 
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n-1}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^n
    \\
    \downarrow && \downarrow && \downarrow^{\mathrm{id}}  
    && \cdots && \downarrow^{\mathrm{id}} && \downarrow^{\mathrm{id}}
    \\
    0
    &\to&
    U(1)
     &\stackrel{\mathbf{d}log}{\to}& 
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n-1}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^n
  }
$$

where the bottom [[quasi-isomorphism]] is from remark  \ref{RModZResolutionOfU1DeligneComplex}.

On passing to [[abelian sheaf cohomology]] this gives, 
by example \ref{CohomologyWithCoefficientsInTruncatedDeRham}, a morphism 

$$
  \array{
    \Omega^n(X)/im(\mathbf{d})
    \\
    & \searrow
    \\
    && H^{n+1}_{conn}(X,\mathbb{Z})
  }
$$

=--

+-- {: .num_defn #InclusionOfFlatConnections}
###### Definition

Consider the canonical morphism

$$
  (\flat \mathbf{B}^n U(1))_\bullet
  \stackrel{\simeq}{\longrightarrow}
  (\mathbf{B}^n U(1)_{flat})_\bullet
  \longrightarrow
  (\mathbf{B}^n U(1)_{conn})_\bullet
$$

via def. \ref{FlatSmoothDeligneComplex}, 
prop. \ref{TwoEquivalentModelsForFlatBnU1}.

Passing to [[abelian sheaf cohomology]] this induces
a morphism

$$
  \array{
    && H^{n+1}_{conn}(X,\mathbb{Z})
    \\
    & \nearrow
    \\
    H^n(X,U(1))
  }
$$

We call this map the _inclusion of the [[flat infinity-connections]]_
into all [[circle n-connections]].

=--

Combining what we have so far:

+-- {: .num_prop #BocksteinHomomorphism}
###### Proposition

The [[composition|composite]] of the morphisms
of def. \ref{InclusionOfGloballyDefinedConnectionForms} and of the curvature morphism of def. \ref{CurvatureMap}

$$
  \array{
    \Omega^n(X)/im(\mathbf{d}) && \stackrel{\mathbf{d}}{\longrightarrow} &&
    \Omega^{n+1}_{cl}(X)
    \\
    & \searrow && \nearrow_{\mathrlap{F_{(-)}}}
    \\
    && H^{n+1}_{conn}(X,\mathbb{Z})
  }
$$

is given by the de Rham differential $\mathbf{d}$ on differential forms.

The composite of the morphisms of def. \ref{InclusionOfFlatConnections}
and def. \ref{UnderlyingBundleMap} is
the [[Bockstein homomorphism]]:

$$
  \array{
    && H^{n+1}_{conn}(X,\mathbb{Z})
    \\
    & \nearrow && \searrow^{\mathrlap{DD}}
    \\
    H^n(X,U(1))
    &&
     \underset{\beta}{\longrightarrow}
    &&
    H^{n+1}(X,\mathbb{Z})
  }
$$

=--

+-- {: .proof}
###### Proof

By composing the defining zig-zags of [[chain maps]]
the statement is immediate. 

=--

##### The Chern character 
 {#TheChernCharacter}

While the explicit definition of the Deligne complex 
in def. \ref{TheSmoothDeligneComplex} is easy enough, all its 
good abstract properties are best understood by realizing that it is the [[homotopy fiber product]] of a kind of higher abelian [[Chern character]] map with the closed differential forms $\mathbf{\Omega}^{n+1}_{cl}$. This is the content of prop. \ref{HomotopyFiberProductCharacterization} below.

+-- {: .num_defn #ChernCharacterMap}
###### Definition

Write

$$
  ch_\bullet
   \colon
  (\mathbf{B}^{n+1}\mathbb{Z})_\bullet
  \longrightarrow
  (\flat \mathbf{B}^{n+1}\mathbb{R})_\bullet
$$

for the morphism given as the composite

$$
  (\mathbf{B}^{n+1}\mathbb{Z})_\bullet
  =
  (\flat \mathbf{B}^{n+1}\mathbb{Z})_\bullet
  \longrightarrow
  (\flat \mathbf{B}^{n+1}\mathbb{R})_\bullet
$$

where the second morphism is induced by the canonical inclusion $\mathbb{Z} \hookrightarrow \mathbb{R}$.

Passing to [[abelian sheaf cohomology]] this induces a morphism

$$
  \array{
    && H^{n+1}(X,\mathbb{R})
    \\
    & \nearrow_{\mathrlap{ch}}
    \\
    H^{n+1}(X,\mathbb{Z})
  }
$$

=--

+-- {: .num_remark}
###### Remark

The morphism in def. \ref{ChernCharacterMap} 
is just the traditional map from [[ordinary cohomology]] with [[integer]] coefficients to that with [[real numbers]] coefficients given for instance via [[singular cohomology]] simply by forming the [[tensor product of abelian groups]] with $\mathbb{R}$. In the broader context of [[differential cohomology]] however it is useful to think of this map as the _[[Chern character]]_, whence the notation.

While this is easy enough to construct in itself, 
the underlying [[chain map]] here is not a fibration in the 
sense of def. \ref{FibrantOnjectStructureOnChSmooth} (having as non-trivial component the inclusion $\mathbb{Z} \hookrightarrow \mathbb{R}$, which is evidently not an epimorphism). But the [[homotopy fiber]] of this map plays a crucial role in the theory, and so in view of remark \ref{HomotopyFibersViaFactorizationLemma} we consider now a fibration [[resolution]] of this map

=--


+-- {: .num_defn #DifferentialResolutionOfIntegralCoefficients}
###### Definition

Consider the chain complex

$$
  \widehat {(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
  \coloneqq
  \left[
  \array{
    \mathbb{Z} &\stackrel{}{\hookrightarrow}& \mathbb{R}
    &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^1  &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^{n-1}
    &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^n
    \\
    \oplus 
    &\nearrow_{-\mathrlap{id}}& 
    \oplus 
    &\nearrow_{+\mathrlap{id}}& 
    \oplus
    &\nearrow_{-\mathrlap{id}}&
    \cdots
    &\nearrow_{\pm\mathrlap{id}}&
    \oplus
    &\nearrow_{\mp\mathrlap{id}}&
    \\
    \mathbb{R} &\underset{\mathbf{d}}{\to}& \mathbf{\Omega}^1
    &\underset{\mathbf{d}}{\to}&
    \mathbf{\Omega}^2 &\underset{\mathbf{d}}{\to}& \cdots
    &\underset{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n}
    &&
  }
  \right]
$$

where we use [[matrix calculus]]-notation as for [[mapping cones]] 
(see at _[mapping cone -- Examples -- In chain complexes](mapping+cone#InChainComplexes)_).

Write

$$
  \widehat {(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
  \stackrel{\widehat{ch}_\bullet}{\longrightarrow}
  \widehat {(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
$$

for the morphism to the chain complex of  def. \ref{DeRhamResolutionOfConstantFunctions} which is given by the chain map that 
in positive degree projects onto the lower row in the above [[direct sum]] expression and in degree 0 is given by the de Rham differential:

$$
  \array{
    \mathbb{Z} &\stackrel{}{\hookrightarrow}& \mathbb{R}
    &\stackrel{\mathbf{d}}{\to}& \mathbf{\Omega}^1  
    &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}& 
    \mathbf{\Omega}^{n-1}
    &\stackrel{\mathbf{d}}{\to}& 
    \mathbf{\Omega}^n
    \\
    \oplus 
    &\nearrow_{-\mathrlap{id}}& 
    \oplus 
    &\nearrow_{+\mathrlap{id}}& 
    \oplus
    &\nearrow_{-\mathrlap{id}}&
    \cdots
    &\nearrow_{\pm\mathrlap{id}}&
    \oplus
    &\nearrow_{\mp\mathrlap{id}}&
    \\
    \mathbb{R} &\underset{\mathbf{d}}{\to}& \mathbf{\Omega}^1
    &\underset{\mathbf{d}}{\to}&
    \mathbf{\Omega}^2 &\underset{\mathbf{d}}{\to}& \cdots
    &\underset{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n}
    &&
    \\
    \downarrow && \downarrow && \downarrow && \cdots 
    && \downarrow && \downarrow^{\mathrlap{\mathbf{d}}}
    \\
    \mathbb{R}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^2
    &\stackrel{\mathbf{d}}{\to}&  
    \cdots
    &\stackrel{\mathbf{d}}{\to}& 
    \mathbf{\Omega}^{n}
    &\stackrel{\mathbf{d}}{\to}& 
    \mathbf{\Omega}^{n+1}
  }
$$ 

Finally write

$$
  (\mathbf{B}^{n+1}\mathbb{Z})_\bullet
  \longrightarrow
  \widehat {(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
$$

for the morphism given by the chain map which in degree $n+1$ is given by 

$$
  \mathbb{Z} \to \mathbb{Z} \oplus \mathbb{R}
$$

$$  
  n \mapsto (n,n)
  \,.
$$

=--

+-- {: .num_lemma #ChernCharacterResolution}
###### Lemma

The construction in def. \ref{DifferentialResolutionOfIntegralCoefficients}
gives a fibration resolution of the 
Chern character morphism of def. \ref{ChernCharacterMap}
in that it gives a [[commuting diagram]] of [[chain maps]]

$$
  \array{
    (\mathbf{B}^{n+1}\mathbb{Z})_\bullet
    &\stackrel{ch_\bullet}{\longrightarrow}&
    (\flat\mathbf{B}^{n+1} \mathbb{R})_\bullet
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    \widehat {(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
    &\stackrel{\widehat {ch}_\bullet}{\longrightarrow}&
    \widehat {(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
  }
$$

with, on the right, the weak equivalence of prop. \ref{TheDeRhamResolutionOfConstantFunctions}, where

1. the left vertical morphism is a weak equivalence;

1. the bottom horizontal morphism $\widehat{ch}_\bullet$ is a fibration.

=--

+-- {: .proof}
###### Proof

That the diagram commutes is a straightforward inspection, unwinding the definitions. That $\widehat{ch}_\bullet$ is a fibration according to def. \ref{FibrantOnjectStructureOnChSmooth} is by its very construction, being a [[projection]] in positive degree. That the left morphism is a weak equivalence comes down to the [[Poincaré lemma]], in a slight variant of the simple argument that proves prop. \ref{TheDeRhamResolutionOfConstantFunctions}.

=--

+-- {: .num_defn #MapFromClosedFormsToHyperDeRhamCoefficients}
###### Definition

Write

$$
  \mathbf{\Omega}^{n+1}_{cl}
  \stackrel{\iota_\bullet}{\longrightarrow}
  \widehat{\flat \mathbf{B}^{n+1}\mathbb{R}}_\bullet
  \stackrel{\simeq}{\longleftarrow}
  (\flat \mathbf{B}^{n+1}\mathbb{R})_\bullet
$$

for the [[zig-zag]] whose right morphism
is the weak equivalence of prop. \ref{TheDeRhamResolutionOfConstantFunctions}
and whose left morphism is given by the [[chain map]]

$$
  \array{
    0 &\to& 0 &\to& \cdots &\to& 0 &\to& \mathbf{\Omega}^{n+1}_{cl}
    \\
    \downarrow && \downarrow && \vdots && \downarrow && \downarrow^{\mathrlap{id}}
    \\
    \mathbb{R}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^1
    &\stackrel{\mathbf{d}}{\to}&
    \cdots
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n}
    &\stackrel{\mathbf{d}}{\to}&
    \mathbf{\Omega}^{n+1}_{cl}
  }
  \,.
$$

=--

+-- {: .num_prop #HomotopyFiberProductCharacterization}
###### Proposition

The chain maps  

* $(F_{(-)})_\bullet$, def. \ref{CurvatureMap};

* $DD_\bullet$, def. \ref{UnderlyingBundleMap};

* $\iota_\bullet$, def. \ref{MapFromClosedFormsToHyperDeRhamCoefficients}

* $\widehat{ch}_\bullet$, def. \ref{DifferentialResolutionOfIntegralCoefficients}

fit into a [[commuting diagram]]

$$
  \array{
     && \mathbf{\Omega}^{n+1}_{cl}
     \\
     & {}^{\mathllap{(F_{(-)})_\bullet }}\nearrow && \searrow^{\mathrlap{\iota_\bullet}}
     \\
     (\mathbf{B}^n U(1)_{conn})_\bullet
     && && \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
     \\
     & {}_{\mathllap{DD_\bullet}}\searrow && 
     \nearrow_{\mathrlap{\widehat{ch}_\bullet}}
     \\
     && \widehat{(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
  }
$$

which is a [[pullback diagram]] in $Ch_+(Smooth0Type)$.
This exhibits the  Deligne complex $(\mathbf{B}^n U(1)_{conn})_\bullet$
as the [[homotopy pullback]]
of the inclusion of $\mathbf{\Omega}^{n+1}_{cl}$
along the Chern character map $ch_\bullet$.

=--

+-- {: .proof}
###### Proof

The first statement follows straightforwardly by inspection,
using that pullbacks of chain complexes are computed componentwise.
From this the second statement follows then since by 
\ref{ChernCharacterResolution} $\widehat{ch}_\bullet$ is 
a fibration resolution of $ch_\bullet$.

=--


##### The exact sequences for curvature and characteristic classes
 {#ExactSequenceForCurvatureAndCharacteristicClass}


+-- {: .num_defn #IntegralDifferentialForms}
###### Definition

Write

$$
  \Omega^{n+1}_{int}(X)
  \hookrightarrow
  \Omega^{n+1}_{cl}(X)
$$

for the inclusion of those closed [[differential forms]] whose [[periods]] ([[integration of differential forms|integration]] over $(n+1)$-cycles) takes values in the [[integers]].

=--

+-- {: .num_prop #ImageOfCurvatureInIntegralDifferentialForms}
###### Proposition

The [[image]] of the curvature map 
$F_{(-)} \colon H^{n+1}_{conn}(X,\mathbb{Z}) \longrightarrow \Omega^{n+1}_{cl}(X)$
of def. \ref{CurvatureMap} are the integral forms of 
def. \ref{IntegralDifferentialForms}.

=--

+-- {: .proof}
###### Proof

The [[homotopy pullback]] characterization of
of prop. \ref{HomotopyFiberProductCharacterization} 
implies that the image consists of precisely those closed differential forms
which under the [[de Rham theorem]], remark \ref{DeRhamTheorem}, represent
real cohomology classes that are in the image of integral
cohomology classes. These are the differential forms
with integral periods.

=--


+-- {: .num_prop #CurvatureExactSequence}
###### Proposition
**(curvature exact sequence)**

The Deligne cohomology group fits into a [[short exact sequence]] 
(of [[abelian groups]]) of the form

$$  
  0
  \to
  H^n(X,U(1))
  \longrightarrow
  H^{n+1}_{conn}(X,\mathbb{Z})
  \stackrel{F_{(-)}}{\longrightarrow}
  \Omega^{n+1}_{int}(X)
  \to 0
$$

where $F_{(-)}$ is the [[curvature]] map of def. \ref{CurvatureMap}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{ImageOfCurvatureInIntegralDifferentialForms} the
morphism on the right is indeed an epimorphism. 
It remains to determine its [[kernel]]. 

To that end, consider the [[pasting diagram]] of [[homotopy pullbacks]]
obtained form the homotopy pullback in 
prop. \ref{HomotopyFiberProductCharacterization}.
Using the [[pasting law]] and the fact that 
the [[loop space object]] of a 
[[0-truncated]] object such as $\mathbf{\Omega}^{n+1}_{cl}$ is trivial,
this is of the form

$$
  \array{
     0 &\longrightarrow& \widehat{(\flat \mathbf{B}^{n}(\mathbb{R}/\mathbb{Z}))}_\bullet &\longrightarrow& 0
     \\
     \downarrow && \downarrow && \downarrow^{}
     \\
     0 &\longrightarrow& (\mathbf{B}^n U(1)_{conn})_\bullet
     &\stackrel{(F_{(-)}_\bullet)}{\longrightarrow}&
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     && \downarrow^{\mathrlap{DD_\bullet}} && \downarrow^{\mathrlap{\iota_\bullet}}
     \\     
     && \widehat{(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
     &\stackrel{\widehat{ch}_\bullet}{\longrightarrow}&
     \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
  }
  \,.
$$

Passing to [[abelian sheaf cohomology]]
and applying the induced [[long exact sequence in homology]], in view of remark \ref{GoodCoverCechCohomologyIsHomotopicallyGood}, implies the claim.

=--


+-- {: .num_prop #CharacteristicClassExactSequence}
###### Proposition
**(characteristic class exact sequence)**

The Deligne cohomology group fits into a [[short exact sequence]] 
(of [[abelian groups]]) of the form


$$
  0
  \to
  \Omega^{n}(X)/\Omega^n_{int}(X)
  \stackrel{}{\longrightarrow}
  H^{n+1}_{conn}(X,\mathbb{Z})
  \stackrel{DD}{\longrightarrow}
  H^{n+1}(X,\mathbb{Z})
  \to 0
$$

where $DD$ is the characteristic class map of
def. \ref{UnderlyingBundleMap}.

=--

+-- {: .proof}
###### Proof

The [[chain map]] that represents the [[Dixmier-Douady class]]
by def. \ref{UnderlyingBundleMap} is manifestly 
a fibration in the sense of def. \ref{FibrantOnjectStructureOnChSmooth}.
Therefore its ordinary [[fiber]] is already its [[homotopy fiber]].
That ordinary fiber is evidently the domain of the morphism
constructed in def. \ref{InclusionOfGloballyDefinedConnectionForms},
in its second weakly equivalent incarnation as displayed there.

Therefore the [[long exact sequence in homology]], induced by 
the [[chain map]] $DD_\bullet$ under passage to [[abelian sheaf cohomology]]
(in view of remark \ref{GoodCoverCechCohomologyIsHomotopicallyGood}) goes as

$$
  \cdots
  \longrightarrow
  H^n(X,\mathbb{Z})
  \longrightarrow
  \Omega^n(X)/im(\mathbf{d})
  \stackrel{}{\longrightarrow}
  H^{n+1}_{conn}(X,\mathbb{Z})
  \stackrel{DD}{\longrightarrow}
  H^{n+1}(X,\mathbb{Z})
$$

As in the proof of prop. \ref{ImageOfCurvatureInIntegralDifferentialForms}
it follows that the rightmost morphism is an [[epimorphism]]. Hence we get a [[short exact sequence]] by dividing out the image of $H^n(X,\mathbb{Z})$ in $\Omega^n/im(\mathbf{d})$. That image is $\Omega^n_{int}(X)$. Since this image contains $im(\mathbf{d})$ (as the closed differential forms all whose periods are $0 \in \mathbb{N}$ ) the resulting quotient is $\Omega^n(X)/Omega^n_{int}(X)$ and the claim follows.

=--

+-- {: .num_remark}
###### Remark

In words the statement of prop. \ref{CurvatureExactSequence}
and prop. \ref{CharacteristicClassExactSequence}
is that Deligne [[cohomology groups]]
$H^{n+1}_{conn}(X,\mathbb{Z})$
constitute a [[group extension]] 

1. of integral [[ordinary cohomology]] by differential $n$-forms modulo integral forms;

1. of closed $(n+1)$-forms by $U(1)$-valued ordinary cohomology.

The first statement is what gives the name to "[[differential cohomology]]" as it makes precise how $H^{n+1}_{conn}(X)$ is a combination of ordinary integral cohomology with _[[differential form]]_-data.

The second statement is secretly of the same flavor, if maybe not as manifestly so: the $U(1)$-valued ordinary cohomology is really what classifies _[[flat infinity-connections|flat]]_ [[circle n-connections]] on [[circle n-group]] [[principal infinity-bundles]] (either, depending on perspective, by def. \ref{FlatSmoothDeligneComplex} or else, more intrinsically, by the very statement of prop. \ref{CurvatureExactSequence}) and hence again describes a combination of underlying bundles with differential form data.

=--





##### The exact differential cohomology hexagon
 {#TheExactDifferentialCohomologyHexagon}


Summing up,
the homotopy  pullback square of prop. \ref{HomotopyFiberProductCharacterization}
together with the maps of 
prop. \ref{BocksteinHomomorphism} form a [[commuting diagram]]
in $Ch_+(Smooth0Type)$ of the form.

$$
  \array{
     \mathbf{\Omega}^{\bullet \leq n} && 
     \stackrel{\mathbf{d}}{\longrightarrow} && \mathbf{\Omega}^{n+1}_{cl}
     \\
     &\searrow& & {}^{\mathllap{(F_{(-)})_\bullet }}\nearrow && \searrow^{\mathrlap{\iota_\bullet}}
     \\
     && (\mathbf{B}^n U(1)_{conn})_\bullet
     && && \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
     \\
     &\nearrow& & {}_{\mathllap{DD_\bullet}}\searrow && 
     \nearrow_{\mathrlap{\widehat{ch}_\bullet}}
     \\
     \widehat{(\flat \mathbf{B}^n U(1))}_\bullet
     && \underset{\beta}{\longrightarrow} && \widehat{(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
  }
$$

+-- {: .num_prop #TheDifferentialHexagonForDeligne}
###### Proposition

This extends to a diagram in $Ch_+(Smooth0Type)$ of the form

$$
  \array{
     && \mathbf{\Omega}^{\bullet \leq n} && 
     \stackrel{\mathbf{d}}{\longrightarrow} && \mathbf{\Omega}^{n+1}_{cl}
     \\
     & \nearrow& &\searrow& & {}^{\mathllap{(F_{(-)})_\bullet }}\nearrow && \searrow^{\mathrlap{\iota_\bullet}}
     \\
     \widehat{(\flat \mathbf{B}^n \mathbb{R})}_{\bullet}
     && && (\mathbf{B}^n U(1)_{conn})_\bullet
     && && \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
     \\
     &\searrow & &\nearrow& & {}_{\mathllap{DD_\bullet}}\searrow && 
     \nearrow_{\mathrlap{\widehat{ch}_\bullet}}
     \\
     && \widehat{(\flat \mathbf{B}^n U(1))}_\bullet
     && \underset{\beta}{\longrightarrow} && \widehat{(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
  }
$$

such that

1. both square are [[homotopy pullback]] squares;

1. both diagonals are [[homotopy fiber sequences]];

1. the two outer sequences are [[long homotopy fiber sequences]].

=--

+-- {: .proof}
###### Proof

For the first statement consider the pasting of homotopy pullback diagrams as in the proof of prop. \ref{CurvatureExactSequence}, now extended to the left,
via the [[pasting law]], as

$$
  \array{
     \widehat{(\flat \mathbf{B}^n \mathbb{R})}_\bullet &\longrightarrow& \widehat{(\flat \mathbf{B}^{n}(\mathbb{R}/\mathbb{Z}))}_\bullet &\longrightarrow& 0
     \\
     \downarrow && \downarrow && \downarrow^{}
     \\
     \mathbf{\Omega}^{\bullet \leq n}
     &\longrightarrow& (\mathbf{B}^n U(1)_{conn})_\bullet
     &\stackrel{(F_{(-)}_\bullet)}{\longrightarrow}&
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     && \downarrow^{\mathrlap{DD_\bullet}} && \downarrow^{\mathrlap{\iota_\bullet}}
     \\     
     && \widehat{(\mathbf{B}^{n+1}\mathbb{Z})}_\bullet
     &\stackrel{\widehat{ch}_\bullet}{\longrightarrow}&
     \widehat{(\flat \mathbf{B}^{n+1}\mathbb{R})}_\bullet
  }
  \,.
$$

That the NE-diagonal is a homotopy fiber sequence is the statement in the proof
of prop. \ref{CurvatureExactSequence}. That the SE-diagonal is a homotopy fiber sequence follows by inspection as remarked in the proof of prop. \ref{CharacteristicClassExactSequence}.

From this the last statement now is implied by using the [[pasting law]] 
yet once more, as show in the proof [here](differential+cohomology+diagram#TheDifferentialDiagram).

=--

+-- {: .num_remark}
###### Remark

The form of the exact hexagon characterizing the Deligne 
complex via prop. \ref{TheDifferentialHexagonForDeligne}
is in fact a general abstract consequence of the
fact that all universal constructions in $Ch_+(Smooth0Type)$
considered here indeed may be understood as
taking place in the
[[cohesive (∞,1)-topos|cohesive]] [[homotopy theory]] of [[smooth ∞-groupoids]],
via remark \ref{HomotopyPullbacksPreservedbyInclusionIntoAllSmoothHomotopyTypes}.
This is discussed in detail at _[[differential cohomology hexagon]]_.

=--



### Semantic Layer
 {#SemanticsLayer}

#### Differential cohomology
 {#SmoothDifferentialCohomology}

We discuss now a general abstract construction of differential coefficient objects using the axioms of [[cohesion]]. When applied in the model of [[smooth infinity-groupoids]] we find that the [[Deligne complex]] considered [above](#DeligneCohomology) is a realization of this axiomatics


Let $G \in Grp(\mathbf{H})$ be a [[braided ∞-group]]. Equivalently, let its [[delooping]] $\mathbf{B}G \in \mathbf{H}$ be itself equipped with the structure of an [[∞-group]]. Write

$$
  \mathbf{B}^2 G \in \mathbf{H}
$$

for the corresponding double [[delooping]].

+-- {: .num_defn #UniversalCurvatureCharacteristic}
###### Definition

Write 

$$
  curv_{G} 
   \coloneqq 
  \theta_{\mathbf{B}\mathbb{G}}
  \colon
  \mathbf{B}G
  \to
  \flat_{dR} \mathbf{B}^2 G
$$

for the [[Maurer-Cartan form]] on the [[∞-group]] $\mathbf{B}G$, def. \ref{GeneralAbstractMaurerCartanForm}. We call this the **universal curvature characteristic** of $G$.

=--

+-- {: .num_defn #GeneralConcreteDifferentialCohomology}
###### Definition

The **[[differential cohomology]]** with [[coefficients]] in $\mathbf{B}G$ is [[cohomology]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\flat_{dR} \mathbf{B}^2 G}$ with [[coefficients]] in $curv_G$

$$
  \mathbf{H}_{/\flat_{dR}\mathbf{B}^2 G}(-, curv_G)
  \,.
$$

=--

#### Differential-form curvatures


$$
  \array{
     \mathbf{B} \mathbb{G}_{conn} &\to& \Omega^{n+1}_{cl}(-)
     \\
     \downarrow &pb& \downarrow^{\mathrlap{}}
     \\
     \mathbf{B}\mathbb{G} 
       &\stackrel{curv}{\to}&
     \flat_{dR} \mathbf{B}^2 \mathbb{G}
  }
$$

presented by [[ordinary differential cohomology]]


#### Higher holonomy
 {#Holonomy}

* [[higher holonomy]]

$$
  \exp(2 \pi i \int_{\Sigma}(-))
  \colon
  [\Sigma,\mathbf{B}^n U(1)_{conn}]
  \stackrel{conc \circ \tau_0}{\to}
  U(1)
$$

### Syntactic Layer

#### The dependent curvature type


The universal curvature characteristic, def. \ref{UniversalCurvatureCharacteristic}, has the [[syntax]]

$$
  \vdash curv_{G} \colon \mathbf{B}G \to \flat_{dR} \mathbf{B}^2 G
  \,.
$$

Regarded as a [[dependent type]] in the de Rham coefficient [[context]] this is

$$
    \omega \colon \flat_{dR}\mathbf{B}^2 G
    \;
    \vdash 
    \;
    \underset{\mathbf{c} \colon \mathbf{B}G}{\sum} 
    \left(
      curv_G\left(\mathbf{c}\right)
      \simeq \omega
    \right)
  \colon
  Type
$$

Therefore the [[syntax]] for a domain object $F \colon X \to \flat_{dR} \mathbf{B}^2 G$ in this [[context]] is

$$
  \omega \colon \flat_{dR} \mathbf{B}^2 G
  \;\vdash\;
  \underset{x \colon X}{\sum} 
  \left(
    F_x \simeq \omega
  \right)
  \colon Type
$$

and the [[syntax]] for a [[cocycle]] 

$$
  \array{
    X &&\stackrel{\bar P}{\to}&& \mathbf{B}G
    \\
    & {}_{\mathllap{F}}\searrow &\swArrow_{\nabla}& \swarrow_{\mathrlap{curv_G}}
    \\
    && \flat_{dR} \mathbf{B}^2 G
  }
$$

in [[differential cohomology]], def. \ref{GeneralConcreteDifferentialCohomology}, on $(X,F)$ is hence

$$
  \vdash \;
  (\bar P,\nabla)
  \colon
  \underset{\omega \colon \flat_{dR} \mathbf{B}^2 G}{\prod}
  \left(
    \left(
    \underset{x \colon X}{\sum}
    \left(
      F_x \simeq \omega
    \right)
    \right)
    \to 
    \left(
    \underset{\mathbf{c} \colon \mathbf{B}G}{\sum}
    \left(
      curv_G(\mathbf{c}) \simeq \omega
    \right)
    \right)
  \right)
$$

#### Fixed curvature twists

$$
  \begin{aligned}
    (\mathbf{B}^n \mathbb{G} \colon Type)_{conn} \colon & Type
    \\
     \coloneqq &  
     \sum_{\mathbf{c} \colon \mathbf{B}\mathbb{G}}
     \sum_{\omega \colon \Omega^{n+1}_{cl}}
     \left(
       curv(\mathbf{c}) = \omega
     \right)
  \end{aligned}
$$
