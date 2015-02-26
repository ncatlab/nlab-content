
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 


## Idea
 {#Idea}

_Deligne cohomology_ -- or _[[Pierre Deligne|Deligne]]-[[Alexander Beilinson|Beilinson]] cohomology_ -- is an [[abelian sheaf cohomology]] that models [[ordinary differential cohomology]].

The _Deligne complex_ is like a truncated [[de Rham complex]] but, crucially, with the sheaf of 0-forms -- the [[structure sheaf]] $\mathcal{O}$ - replaced by the [[multiplicative group]] $\mathcal{O}^\times$ under the [[exponential map]]

$$
  \left[
     \mathcal{O}^\times
     \stackrel{d log}{\longrightarrow}
     \Omega^1
     \stackrel{d}{\longrightarrow}
     \Omega^2
     \stackrel{d}{\longrightarrow}
     \cdots
     \stackrel{d}{\longrightarrow}
     \Omega^n
  \right]
  \,.
$$

Deligne cohomology $H^{n+1}_{conn}(X, \mathbb{Z})$ in degree $(n+1)$ is the [[abelian sheaf cohomology]] with [[coefficients]] in this [[chain complex]] of [[sheaves of abelian groups]] ("[[hypercohomology]]"). 

This was introduced in ([Deligne 71](#Deligne71)) in the context of [[analytic geometry]] (hence using [[holomorphic differential forms]]) as a [[Hodge filtration|Hodge-filtered]] version of [[singular cohomology]], designed to be a target for the [[Beilinson regulator]] from [[motivic cohomology]]. But the form of the definition applies more generally, in particular also in smooth [[differential geometry]], a fact amplified and popularized in ([Brylinski 93](#Brylinski93)).

In smooth [[differential geometry]] the typical minor variant has the sheaf $\underline{U}(1) = C^\infty(-,U(1))$ of [[circle group]]-valued [[smooth functions]] in degree $n$:

$$
  \left[
     C^\infty(-,U(1))
     \stackrel{d log}{\longrightarrow}
     \Omega^1
     \stackrel{d}{\longrightarrow}
     \Omega^2
     \stackrel{d}{\longrightarrow}
     \cdots
     \stackrel{d}{\longrightarrow}
     \Omega^n
  \right]
  \,.
$$

Given any [[manifold]] $X$, then the resulting complex of abelian groups is, under the [[Dold-Kan correspondence]], the [[n-groupoid]] of [[circle n-bundles with connection]] whose underlying [[circle n-group|circle (n-1)-group]]-[[principal infinity-bundle]] is trivialized. Passing to the [[abelian sheaf cohomology]] implicitly corresponds to considering the [[infinity-stackification]] of this $n$-groupoid valued presheaf, and in this way Deligne cohomology computes equivalence classes of [[circle n-bundles with connection]]. Another way to say this is that under the [[Dold-Kan correspondence]] and [[infinity-stackification]], the above Deligne complex defines a [[smooth infinity-stack]] $\mathbf{B}^n U(1)_{conn}$ which is the [[moduli infinity-stack]] for [[circle n-bundles with connection]], and Deligne cohomology computes the [[homotopy classes]] of maps (of [[infinity-stacks]]) into this ([FSS 10](#FSS10))

$$
  H^{n+1}_{conn}(X,\mathbb{Z})
  \simeq
  \pi_0(X \to \mathbf{B}^n U(1)_{conn})
  \,.
$$

In this way Deligne cohomology, or rather the collection of Deligne [[cocycles]] with [[coefficients]] in the Deligne complex that defines it, is considerably richer than other models for [[ordinary differential cohomology]] such as [[Cheeger-Simons differential characters]], which see only the [[cohomology group]], but not the full [[moduli infinity-stack|moduli n-stack]].

Explicitly, computing the [[abelian sheaf cohomology]] with coefficients in the [[Deligne complex]] via [[Cech cohomology]] gives that a [[cocycle]] $\overline{A}$ on some [[space]] $X$ is represented with respect to a suitable [[covering]] $\{U_i \to X\}$ by a collection of [[differential forms]] and functions

$$
  \overline{A}
  = 
  \left\{
     A_{i_0, \cdots, i_k}
     \in \Omega^{n-k}(U_{i_0, \cdots i_k})
  \right\}_{k = 0}^{n}
  \cup
  \{
     g_{i_0, \cdots, i_n} \in \mathcal{O}^\times(U_{i_0, \cdots, i_{n+1}})
  \}
$$

such that the failure of the $(n-k+1)$-forms to glue on $(k+1)$-fold intersections of charts is given by the de Rham differential of the $(n-k)$-forms

$$
  \sum_{j = 0}^k
  (-1)^j
  A_{i_0, \cdots, i_{j-1}, i_{j+1}, \cdots, i_{k+1}}
  =
  d_{dR} A_{i_0, \cdots, i_{k+1}}
  \,.
$$


This evidently generalizes the familiar Cech cocycle data for traditional [[line bundles with connection]].

As the notation indicates, Deligne cohomology is a [[differential cohomology]] refinement of [[ordinary cohomology]] with [[integer]] [[coefficients]], exhibited by a canonical forgetful map

$$
  \array{
    H^{n+1}_{conn}(X,\mathbb{Z})
    \\
    & \searrow
    \\
    && H^{n+1}(X,\mathbb{Z})   
  }
$$

which is induced by the evident morphism of [[chain complexes]]. This is one map in an exact [[differential hexagon]] which exhibits Deligne cohomology as the differential refinement of ordinary integral cohomology by closed [[curvature]] [[differential form]] data.

$$
  \array{
    0 & && && && & 0
    \\
    & \searrow && && &&  \nearrow 
    \\
    && \Omega^{n}(X)/\Omega^n(X)_{\mathbb{Z}} && \stackrel{\mathbf{d}}{\longrightarrow} &&  \Omega^{n+1}_{cl}(X)
    \\
    & \nearrow && \searrow^{\mathrlap{a}} && {}^{\mathllap{F_{(-)}}}\nearrow && \searrow
    \\
    H^{n}(X, \mathbb{R})
    && &&
    H^{n+1}_{conn}(X,\mathbb{Z})
    && &&
    H^{n+1}(X,\mathbb{R})
    \\
    & \searrow && \nearrow && \searrow^{\mathrlap{DD}} && \nearrow
    \\
    && H^{n}(X,U(1)) && \underset{\beta}{\longrightarrow} && H^{n+1}(X,\mathbb{Z})
    \\
    & \nearrow && && &&  \searrow 
    \\
    0 & && && && & 0
    \\
    \\
    &&  connection\;forms\;on\;trivial\;bundles && \stackrel{de\;Rham\;differential}{\longrightarrow} && curvature\;forms
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{curvature}} && \searrow^{\mathrlap{de\;Rham\;theorem}}
    \\
    flat\;differential\;forms  && && geometric\;bundles\;with \;connection && && rationalized\;bundle
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{topol.\;class}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && geometric\;bundles\;with\;flat\;connection && \underset{Bockstein\,homomorphism}{\longrightarrow} && shape\;of\;bundle
  }
$$




## Definition

### General

In any context where these symbols make the evident sense, the Deligne complex of degree $(n+1)$ is the [[chain complex]] $\mathcal{O}^\times \stackrel{d log}{\to}\Omega^1 \stackrel{d}{\to} \Omega^2 \to \cdots \to \Omega^n$, and Deligne cohomology in degree $(n+1)$ is the [[abelian sheaf cohomology]] with [[coefficients]] in this complex. 

More generally one considers any [[discrete group]] $A$ and inclusion $A \hookrightarrow \mathcal{O}$ into the [[structure sheaf]], then the corresponding Deligne complex is $A \hookrightarrow \mathcal{O} \stackrel{d}{\to} \Omega^1 \to \cdots \to \Omega^n$.

### In smooth differential geometry
 {#DefinitionInSmooth}

For definiteness we consider here the Deligne complex in the smooth differential geometric context. Most variants work directly analogously, but it may be useful to have a specific case in hand.

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

+-- {: .num_example #RepresentableSheavesAndTheirConstantVersion}
###### Example

The assignment $C^\infty(-,\mathbb{R}) \colon \mathbb{R}^n \mapsto C^\infty(\mathbb{R}^n,\mathbb{R})$ of [[smooth functions]] with values in the [[real numbers]] is a [[sheaf]]. Since this is [[representable functor|representable]] we are entitled to identify this with the [[smooth manifold]] $\mathbb{R}$ (the [[real line]]) itself, and just write $\mathbb{R} \in Sooth0Type$. 

Similarly for $X$ any other [[smooth manifold]], it represents a sheaf on [[CartSp]] and we just write $X \in Smooth0Type$ for this.

Of particular interest below is the case where $X = S^1 = U(1)$ is the [[circle]], to be regarded as the [[circle group]].

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


+-- {: .num_remark}
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

Under addition of differential forms, the sheaves $\mathbf{\Omega}^k$ of example \ref{SheavesOfFormsAndDeRhamDifferential} becomes [[abelian sheaves]], and we will implicitly understand them this way now.

+-- {: .num_example}
###### Example

Write $(\flat_{dR}\mathbf{B}^n \mathbb{R})_\bullet \in Ch(Smooth0Type)$ for the complex of sheaves given by the [[de Rham complex]] truncated as follows:

$$
  (\flat_{dR}\mathbf{B}^n \mathbb{R})_\bullet
  \coloneqq
  \left[
    \mathbf{\Omega}^1
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^2
    \stackrel{\mathbf{d}}{\to}
    \cdots
    \stackrel{\mathbf{d}}{\to}
    \mathbf{\Omega}^n_{cl}
  \right]
  \,.
$$

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

Observe that in the above constructions the de Rham complex is truncated to the right by discarding what would be the next differentials, without passing to their [[kernel]]. This simple point is the key aspect of the Deligne complex. If one instead truncates while preserving the chain homology in in the lowest degree, then one obtains the following complex with the sheaf $\mathbf{\Omega}^{n}_{cl}$ of _closed_ forms in lowest degree, which gives [[ordinary cohomology]]:

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
  (\mathbf{B}^n U(1)_{conn})_\bullet
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

By the [[Poincaré lemma]]. This _is_ the Poincar&#233; Lemma.

=--




## Properties

### Characteristic maps out of and into Deligne cohomology
 {#CharacteristicMaps}

We discuss the construction of two canonical morphisms out of Deligne cohomology,
and two canonical morphisms into it. Below in ... these are shown to form two interlocking [[exact sequences]] and in fact an exact [[differential cohomology hexagon]] which accurately characterizes Deligne cohomology as the [[differential cohomology]] extension of integral [[ordinary cohomology]] by [[differential forms]].

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
  \mathbf{\Omega}^n/im(\mathbf{d})
  \stackrel{\simeq}{\longleftarrow}
  \stackrel{}{\longrightarrow}
  (\mathbf{B}^n U(1)_{conn})_\bullet
$$

given by the [[chain maps]]

$$
  \array{
    0 &\to& 0 &\stackrel{}{\to}& 0 &\stackrel{}{\to}& \cdots &\stackrel{}{\to}& 0
   &\stackrel{}{\to}& \mathbf{\Omega}^n/im(\mathbf{d})
    \\
    \uparrow && \uparrow && \uparrow^{\mathrm{id}}  
    && \cdots && \uparrow^{\mathrm{id}} && \uparrow^{\mathrm{id}}
    \\
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

where the bottom [[quasi-isomorphism]] is from remark  \ref{RModZResolutionOfU1DeligneComplex} and the top one is a quasi-iso by 
the [[Poincaré lemma]], as in prop. \ref{TwoEquivalentModelsForFlatBnU1}.

On passing to [[abelian sheaf cohomology]] this gives a morphism 

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

+-- {: .num_prop}
###### Proposition

The [[composition|composite]] of the morphisms
of def. \ref{InclusionOfGloballyDefinedConnectionForms} and of the curvature morphism of def. \ref{CurvatureMap}

$$
  \array{
    \Omega^n(X)/im(\mathbf{d}) && \stackrel{\mathbf{d}}{\longrightarrow} &&
    \Omega^{n+1}_{cl}
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

### The exact sequences for curvature and DD-class

We discuss how the Deligne [[cohomology groups]]
$H^{n+1}_{conn}(X,\mathbb{Z})$
constitute a [[group extension]] 

1. of integral [[ordinary cohomology]] by differential $n$-forms modula integral forms;

1. of closed $(n+1)$-forms by $U(1)$-valued ordinary cohomology.

+-- {: .num_pro}
###### Proposition

There are [[short exact sequences]]: the 

**curvature exact sequence**

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

and the **characteristic class exact sequence**

$$
  0
  \to
  \Omega^{n}(X)/Omega^n_{int}(X)
  \stackrel{}{\longrightarrow}
  H^{n+1}_{conn}(X,\mathbb{Z})
  \stackrel{DD}{\longrightarrow}
  H^{n+1}(X,\mathbb{Z})
  \to 0
$$

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
the [[chain map]] $DD_\bullet$ goes as

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

Form the above it follows that the rightmost morphism is an [[epimorphism]]. Hence we get a short exact sequence by dividing out the image of $H^n(X,\mathbb{Z})$ in $\Omega^n/im(\mathbf{d})$. That image is $\Omega^n_{int}(X)$. Since this includes $im(\mathbf{d})$ the resulting quotient is $\Omega^n(X)/Omega^n_{in}(X)$ and the claim follows.

=--

### The exact differential cohomology hexagon


These two morphisms exhibit Deligne cohomology as a refinement in [[differential cohomology]] of ordinary (i.e. integral [[Eilenberg-MacLane spectrum|Eilenberg-MacLane]]) [[cohomology]], in that the diagram

$$
  \array{
    H(X,\bar \mathbf{B}^\bullet U(1))
    &\stackrel{[F]}{\to}&
    H^{\bullet+1}_{dR}(X)
    \\
    \downarrow^{cl} && \downarrow
    \\
    H^{\bullet+1}(X,\mathbb{Z})
    &\to&
    H^{\bullet + 1}(X,\mathbb{R})
  }
$$

is the cohomology of a homotopy pullback diagram, i.e. satisfies the axioms described at [[differential cohomology]].



### Interpretation in terms of higher parallel transport

There is a natural way to understand the Deligne complex of sheaves as a sheaf which assigns to each patch the Lie $n$-groupoid of smooth [[higher parallel transport]] [[n-functor]]s. This perspective is helpful for understanding how Deligne cohomology relates to the bigger picture of [[differential cohomology]].

We start by discussing this in low degree.

There is [[path groupoid]] $P_1(X)$ whose smooth 
space of objects is $X$ and whose smooth space of morphisms is
a space of classes of smooth paths in $X$. 
Every smooth 1-form $A \in \Omega^1(X)$ induces 
a smooth [[functor]] $tra_A : P_1(X) \to \mathbf{B}U(1)$
from $P_1(X)$ to to the smooth [[groupoid]] $\mathbf{B} U(1)$
with one object and $U(1)$ as its smooth space of morphisms
by sending each path $\gamma : [0,1] \to X$
to $\exp (2 \pi i\int_0^1 \gamma^* A)$. This map 
from 1-forms to smooth functors turns out to be bijective:
every smooth functor of this form uniquely arises this way.
Similarly, one finds that smooth [[natural transformation]]
$\eta_f : tra_A \to tra_{A'}$ between two such functors
is in components precisely a 
smooth function $f : X \to U(1)$ such that $A' = A + d log f$.

Since the analogous statements are true for every open subset 
$U \subset X$ this defines a [[sheaf]] of [[Lie groupoid]]s 
$$
  Funct^\infty(P_1(-), \mathbf{B}U(1)) : Op(X)^{op} \to LieGrpd
  \,.
$$
By the [[Dold-Kan correspondence]] this sheaf of groupoids
corresponds to a sheaf of complexes of groups. This complex
of sheaves is nothing but the degree 2 Deligne complex

$$
  Funct^\infty(\Pi_1(-), \mathbf{B}U(1)) \simeq \mathbb{Z}(2)^\infty_D
  \,.
$$
 
This way Deligne cohomology is realized as computing the
[[(infinity,1)-sheafification|stackification]] of the pre-stack
$Funct^\infty(P_1(-), \mathbf{B}(1))$ of smooth $U(1)$-valued 
parallel transport functors.

The identification generalizes: for all $n$ there is a [[path n-groupoid]] $P_n(X)$ whose $k$-morphisms are 
$k$-dimensional smooth paths in $X$. Smooth $n$-functors
$tra_C : _n(X) \to \mathbf{B}^n U(1)$ are canonically identified
with smooth $n$-forms $C \in \Omega^n(X)$ and 
under the [[Dold-Kan correspondence]] the Deligne-complex in degree
$n+1$ is identified with the sheaf of $n$-groupoids of such smooth 
$n$-functors
$$
  n Funct^\infty(P_n(-), \mathbf{B}^n)
  \simeq
  \mathbb{Z}(n+1)^\infty_D
  \,.
$$

See

* John Baez, Urs Schreiber, _Higher Gauge Theory_ ([arXiv](http://arxiv.org/abs/math/0511710))

The full proof for $n=1$ this is in

* Urs Schreiber, Konrad Waldorf, _Parallel transport and functors_ ([arXiv](http://arxiv.org/abs/0705.0452));

for $n=2$ in 

* Urs Schreiber, Konrad Waldorf, _Smooth functors versus differential forms_ ([arXiv](http://arxiv.org/abs/0802.0663))

For more on this see [[infinity-Chern-Weil theory introduction]].

For higher $n$ there is as yet no detailed proof in the literature, but the
low dimensional proofs have obvious generalizations.


### Cup product

See [[Beilinson-Deligne cup-product]].

### Moduli and deformation theory

[[!include moduli of higher lines -- table]]

### GAGA
 {#GAGA}

The Deligne complex is naturally defined in smooth [[differential geometry]] as well as in [[complex analytic geometry]] as well as in [[algebraic geometry]] over the complex numbers. In the spirit of [[GAGA]] it is of interest to know how Deligne cohomology in these different settings relates.

One useful statement is: given an [[smooth scheme|smooth]] [[algebraic variety]] over the [[complex numbers]], then a sufficient condition for a complex-analytic Deligne cocycle over its [[analytification]] to lift to an algebraic Deligne cocycle is that its [[curvature form]] is an [[Kähler form|algebraic form]] ([Esnault 89, corollary 1.3](#Esnault89)). 


## Examples 

As described in some detail at [[electromagnetic field]] in abelian higher [[gauge theory|gauge theories]] the background field naturally arises as a [[?ech cohomology|?ech]]--Deligne cocycle, i.e. a [[?ech cohomology|?ech cocycle]] representative with values in the Deligne complex.

* Degree 2 Deligne cohomology classifies $U(1)$-[[principal bundle]]s [[connection on a bundle|with connection]]. The Deligne complex $\bar \mathbf{B}U(1)$ in this case coincides with the [[groupoid of Lie-algebra valued forms]] for the Lie algebra of $U(1)$.


  * In physics the [[electromagnetic field]] is modeled by a degree 2 Deligne cocycle. See there for a derivation of [[?ech cohomology|?ech]]--Deligne cohomology from physical input.

* Degree 3 Deligne cohomology classifies [[bundle gerbe]]s with connection.

  * In [[electromagnetism]], degree 3 Deligne cocycles (with compact support, possibly) model [[magnetic charge]]. In formal high energy physics the [[Kalb-Ramond field]] is modeled by a Deligne 3-cocycle.

* Degree 4 Deligne cohomology classifies [[bundle 2-gerbe]]s with connection. In particular Chern-Simons bundle 2-gerbes whose degree 4 curvature characteristic class is a multiple of the Pontryagin 4-form on some $SO(n)$-[[principal bundle]]. 

  * In formal high energy physics degree 4 Deligne classes model the [[supergravity C-field]].


## Related concepts

* [[intermediate Jacobian]] ([[self-dual higher gauge theory]])

* [[Abel-Jacobi map]]

* [[Beilinson regulator]]

* [[circle n-bundle with connection]]

* [differential cohomology diagram -- Examples -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)

## References
 {#References}

Deligne cohomology was introduced in [[complex analytic geometry]] (by a [[chain complex]] of [[holomorphic differential forms]]) in 

* {#Deligne71} [[Pierre Deligne]], _Th&#233;orie de Hodge II_ , IHES Pub. Math. (1971), no. 40, 5&#8211;57 ([pdf](http://www.math.jussieu.fr/~ai/d/Theory%20of%20Hodge%202.pdf))

with applications to [[Hodge theory]] and [[intermediate Jacobians]]. The same definition appears in 

* [[Barry Mazur]], [[William Messing]], _Universal extensions and one-dimensional crystalline cohomology_, Springer lecture notes 370, 1974

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], section III.1 of _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)

under the name "multiplicative de Rham complex" (and in the context of studying its [[deformation theory]] by [[Artin-Mazur formal groups]]). The theory was further developed in

* {#Beilinson85} [[Alexander Beilinson]] _[[Higher regulators and values of L-functions]]_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861)) (reviewed in [Esnault-Viehweg 88](#EsnaultViehweg88))

with the application to [[Beilinson regulators]]. Later the evident version of the Deligne complex in [[differential geometry]] over [[smooth manifolds]] gained more attention and is still referred to as "Deligne cohomology".

Surveys and introductions in the context of [[differential geometry]] include

* {#Brylinski93} [[Jean-Luc Brylinski]], section 5 of _Loop Spaces, Characteristic Classes and geometric Quantization_, Birkh&#228;user 1993

* {#Bunke12} [[Ulrich Bunke]], section 3 of _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

Review with more emphasis on [[complex analytic geometry]] and the theory of ([Beilinson 85](#Beilinson85)) with more details spelled out is in

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

* {#Esnault89} [[Hélène Esnault]], _On the Loday-symbol in the Deligne-Beilinson cohomology_, K-theory 3, 1-28, 1989 ([pdf](http://www.mi.fu-berlin.de/users/esnault/preprints/helene/16-loday-symbol.pdf))

See also



* {#PetersSteenbrink08} [[Chris Peters]], [[Jozef Steenbrink]], section 7.2 of _[[Mixed Hodge Structures]]_, Ergebisse der Mathematik (2008) ([pdf](http://www.arithgeo.ethz.ch/alpbach2012/Peters_Steenbrinck))

* {#Voisin02} [[Claire Voisin]], section 12 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

Discussion of Deligne cohomology in terms of [[simplicial presheaves]] and [[higher stacks]] includes

* {#FSS10} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_, Journal of Geometry and Physics, Volume 74, 2013, Pages 130&#8211;163 ([arXiv:1207.5449](http://arxiv.org/abs/1207.5449))

* [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_, [arXiv:1212.2173](http://arxiv.org/abs/1212.2173).

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _A higher stacky perspective on Chern-Simons theory_, in Damien Calaque et al. (eds.) _Mathematical Aspects of Quantum Field Theories_, Mathematical Physics Studies, Springer 2014 ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))


See also the references given at _[differential cohomology hexagon -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)_.


[[!redirects Deligne complex]]

[[!redirects Deligne complexes]]

[[!redirects Deligne-Beilinson cohomology]]
[[!redirects Beilinson-Deligne cohomology]]