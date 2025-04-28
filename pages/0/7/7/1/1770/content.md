+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohesive toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


# Smooth spaces
* table of contents
{: toc}

## Idea

The concept of a _smooth set_ or _smooth space_, in the sense discussed here, is a generalization of that of [[smooth manifolds]] beyond that of [[diffeological spaces]]: A smooth set is a [[generalized smooth space]] that may be _probed_ by smooth [[Cartesian spaces]].

For expository details see at _[[geometry of physics -- smooth sets]]_.

Alternatively, the smooth test spaces may be taken to be more generally all [[smooth manifolds]]. But since [[manifolds]] themselves are built from gluing together smooth [[open balls]] $D^n_{int} \subset \mathbb{R}^n$ or equivalently [[Cartesian spaces]] $\mathbb{R}^n$, one may just as well consider Cartesian spaces test spaces. Finally, since $D^n$ is diffeomorphic to $\mathbb{R}^n$, one can just as well take just the cartesian smooth spaces $\mathbb{R}^n$ as test objects.


## Definition

The category of **smooth spaces** is the [[sheaf topos]]

$$
  SmoothSp := Sh(Diff)
$$

of [[sheaves]] on the [[site]] [[Diff]] of smooth manifolds equipped with its standard [[coverage]] ([[Grothendieck topology]]) given by open covers of manifolds.

Since $Diff$ is [[equivalence of categories|equivalent]] to the category of [[manifolds]] _embedded_ into $\mathbb{R}^\infty$, $Diff$ is an [[essentially small category]], so there are no size issues involved in this definition.

But since manifolds themselves are defined in terms of gluing conditons, the [[Grothendieck topos]] $SmoothSp$ depends on much less than all of $Diff$.

Let

$$
  Ball := \{ (D^n_{int} \to D^m_{int}) \in Diff | n,m \in \mathbb{N}\}
$$

and

$$
  CartSp := \{ (\mathbb{R}^n \to \mathbb{R}^m) \in Diff  | n,m \in \mathbb{N}\}
$$

be the full [[subcategory|subcategories]] $Ball$ and [[CartSp]] of $Diff$ on open balls and on cartesian spaces, respectively. Then the corresponding [[sheaf]] [[topos|toposes]] are still those of smooth spaces:

$$
  \begin{aligned}
    SmoothSp &\simeq Sh(Ball)
    \\
     & \simeq Sh(CartSp)
  \end{aligned}
  \,.
$$


## Examples

* The category of ordinary [[manifolds]] is a
  full subcategory of smooth spaces:
  $$
    Diff \hookrightarrow SmoothSp 
    \,.
  $$
  When one regards smooth spaces concretely as sheaves
  on $Diff$, then this inclusion is of course just the
  [[Yoneda embedding]].

* The full [[subcategory]] 
  $$
    DiffSp \subset SmoothSp
  $$
  on [[concrete sheaf|concrete sheaves]] is 
  called the
  category of [[diffeological spaces]].

  * The standard class of examples of smooth spaces that motivate their use even in cases where one starts out being intersted just in [[smooth manifolds]] are **mapping spaces**: for $X$ and $\Sigma$ two smooth spaces (possibly just ordinary smooth manifolds), by the [[closed monoidal structure on presheaves]] the **mapping space** $[\Sigma,X]$, i.e. the space of smooth maps $\Sigma \to X$ exists again naturally as a smooth. By the general formula it is given as a [[sheaf]] by the assignment

    $$
      [\Sigma,X] : U \mapsto SmoothSp(\Sigma \times U, X)
     \,.
    $$

    If $X$ and $\Sigma$ are ordinary manifolds, then the [[hom-set]] on the right sits inside that of the underlying sets $SmoothSp(\Sigma \times U , X) \subset Set(|\Sigma| \times |U|, |X| )$ so that $[\Sigma,X]$ is a [[diffeological space]].

    The above formula says that a $U$-parameterized family of maps $\Sigma \to X$ is smooth as a map into the smooth space $[\Sigma,X ]$ precisely if the corresponding map of sets $U \times \Sigma \to X$ is an ordinary morphism of smooth manifolds.

* The canonical examples of smooth spaces that
  are not diffeological spaces are the sheaves of
  (closed) differential forms:
  $$
    K^n : U \mapsto \Omega^n_{closed}(U)
    \,.
  $$

* The category 
  $$
    SimpSmoothSp :=
    SmoothSp^{\Delta^{op}}
  $$
  equivalently that of sheaves on $Diff$ with
  values in [[simplicial sets]]
  $$
    \cdots \simeq Sh(Diff, SSet)
  $$
  of [[simplicial objects]] in smooth spaces
  naturally carries the structure of a 
  [[homotopical category]] 
  (for instance the 
    [[model structure on simplicial sheaves]]
  or that of a Brown [[category of fibrant objects]]
  (if one restricts to locally Kan simplicial sheaves))
  and as such is a 
  [[presentable (∞,1)-category|presentation]]
  for the [[(∞,1)-topos]] of 
  [[smooth ∞-stacks]].


## Properties
 {#Properties}

### Cohesion
 {#Cohesion}

+-- {: .num_prop #SmoothSetsFormACohesiveTopos}
###### Proposition
**([[smooth sets]] form a [[cohesive topos]])**

The [[category]] $SmoothSet$ of [[smooth sets]] is a [[cohesive topos]] 

\[
  \label{SheafToposAdjointQuadruple}
  SmoothSet
    \array{
      \overset{\phantom{AAA} \Pi_0 \phantom{AAA}}{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\longleftarrow}
    }
  Set
\]


=--

+-- {: .proof}
###### Proof

First of all (by [this Prop](geometry+of+physics+--+smooth+sets#CategoryOfSmoothSets)) smooth sets indeed form a [[sheaf topos]], over the [[site]] [[CartSp]] of [[Cartesian spaces]] $\mathbb{R}^n$ with [[smooth functions]] between them, and equipped with the [[coverage]] of differentiably-[[good open covers]] ([this def.](geometry+of+physics+--+smooth+sets#DifferentiallyGoodOpenCover))

$$
  SmoothSet \simeq Sh(CartSp)
  \,.
$$

Hence, by Prop. \ref{CategoriesOfSheavesOnCohesiveSiteIsCohesive}, it is now sufficient to see that [[CartSp]] is a [[cohesive site]] (Def. \ref{OneCohesiveSite}).

It clearly has [[finite products]]: The [[terminal object]] is the [[point]], given by the 0-[[dimension|dimensional]] [[Cartesian space]]

$$
  \ast = \mathbb{R}^0
$$

and the [[Cartesian product]] of two [[Cartesian spaces]] is the Cartesian space whose [[dimension]] is the [[sum]] of the two separate dimensions:

$$
  \mathbb{R}^{n_1} \times \mathbb{R}^{n_2}
  \;\simeq\;
  \mathbb{R}^{ n_1 + n_2 }
  \,.
$$

This establishes the first clause in Def. \ref{OneCohesiveSite}. 

For the second clause, consider a differentiably-[[good open cover]] $\{U_i \overset{}{\to} \mathbb{R}^n\}$ ([this def.](geometry+of+physics+--+smooth+sets#DifferentiallyGoodOpenCover)). This being a [[good cover]] implies that its [[Cech groupoid]] is, as an [[internal groupoid]] (via [this remark](geometry+of+physics+--+categories+and+toposes#PresheavesOfGroupoidsAsInternalGroupoidsInPresheaves)), of the form

\[
  \label{CechGroupoidForCartSp}
  C(\{U_i\}_i)
  \;\simeq\;
  \left( 
    \array{
       \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
       \\
       \big\downarrow \big\uparrow \big\downarrow
       \\
       \underset{i}{\coprod} y(U_i)
    }
  \right)
  \,.
\]

where we used the defining property of [[good open covers]] to identify $y(U_i) \times_X y(U_j) \simeq y( U_i \cap_X U_j )$. 

The [[colimit]] of (eq:CechGroupoidForCartSp), regarded just as a [[presheaf]] of [[reflexive graph|reflexive]] [[directed graph|directed]] [[graphs]] (hence ignoring [[composition]] for the moment), is readily seen to be the [[graph]] of the [[colimit]] of the components (the [[universal property]] follows immediately from that of the component colimits):


\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
         y(U_i)
      }
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} \ast
          \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} \ast
      }
    \right)
  \end{aligned}
  \,.
\]

Here we first used that [[colimits commute with colimits]], hence in particular with [[coproducts]] ([this prop.](geometry+of+physics+--+categories+and+toposes#LimitsCommuteWithLimits)) and then that the colimit of a [[representable presheaf]] is [[generalized the|the]] [[singleton]] set ([this Lemma](geometry+of+physics+--+categories+and+toposes#ColimitOfRepresentableIsSingleton)).

This colimiting [[graph]] carries a unique [[composition]] structure making it a [[groupoid]], since there is at most one morphism between any two objects, and every object carries a morphism from itself to itself. This implies that this groupoid is actually the colimiting groupoid of the Cech groupoid: hence the groupoid obtained from replacing each representable summand in the Cech groupoid by a point.

Precisely this operation on [[Cech groupoids]] of [[good open covers]] of [[topological spaces]] is what _[[Borsuk's nerve theorem]]_ is about, a classical result in [[topology]]/[[homotopy theory]]. This theorem implies directly that the set of [[connected components]] of the groupoid (eq:ColimitOfCechGroupoidOverCartSp) is in [[bijection]] with the set of [[connected components]] of the [[Cartesian space]] $\mathbb{R}^n$, regarded as a [[topological space]]. But this is evidently a [[connected topological space]], which finally shows that, indeed

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longrightarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  \ast
  \,.
$$

The second item of the second clause in Def. \ref{OneCohesiveSite} follows similarly, but more easily: The [[limit]] of the [[Cech groupoid]] is readily seen to be, as before, the unique groupoid structure on the limiting underlying graph of presheaves. Since $CartSp$ has a [[terminal object]] $\ast = \mathbb{R}^0$, which is hence an [[initial object]] in the [[opposite category]] $CartSp^{op}$, limits over $CartSp^{op}$ yield simply the evaluation on that object:

\[
  \label{ColimitOfCechGroupoidOverCartSp}
  \begin{aligned}
    \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
    & \simeq
    \left( 
      \array{
        \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i,j}{\coprod} y(U_i \underset{\mathbb{R}^n}{\cap} U_j)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
         \underset{i}{\coprod} y(U_i)
      }
      \phantom{A}
    \right)
    \\
    & \simeq
    \left( 
      \array{
         \underset{i,j}{\coprod} 
         Hom_{CartSp}\left( \ast,  U_i \underset{\mathbb{R}^n}{\cap} U_j \right)
         \\
         \big\downarrow \big\uparrow \big\downarrow
         \\
         \underset{i}{\coprod} 
         Hom_{CartSp}( \ast, U_i )
      }
    \right)
  \end{aligned}
  \,.
\]

Here we used that [[colimits]] (here [[coproducts]]) of [[presheaves]] are computed objectwise, and then the definition of the [[Yoneda embedding]] $y$.

But the [[equivalence relation]] induced by this graph on its set of objects $\underset{i}{\coprod}  Hom_{CartSp}( \ast, U_i )$ precisely identifies pairs of points, one in $U_i$ the other in $U_j$, that are actually the same point of the $\mathbb{R}^n$ being covered. Hence the set of [[equivalence classes]] is the set of points of $\mathbb{R}^n$, which is just what remained to be shown:

$$
  \pi_0
  \underset{\underset{CartSp^{op}}{\longleftarrow}}{\lim}
    C(\{U_i\}_i)
  \;\simeq\;
  Hom_{CartSp}(\ast, \mathbb{R}^n)
  \,.
$$


=--






### Topos points and stalks

+-- {: .num_lemma }
###### Lemma

For every $n \in N$ there is a 
[[point of a topos|topos point]]

$$
  D^n : Set \stackrel{\stackrel{(D^n)^*}{\leftarrow}}
    {\stackrel{D^n_*}{\to}}
    SmoothSp
$$

where the [[inverse image]] morphism -- the [[stalk]] --
is given on $A \in SmoothSp$ by

$$
  (D^n)^* A :=
  \colim_{\mathbb{R}^n \supset U \ni 0} A(U)
  \,,
$$

where the colimit is over all open neighbourhoods of the
origin in $\mathbb{R}^n$.

=--

+-- {: .num_lemma }
###### Lemma

SmoothSp has [[point of a topos|enough points]]:
they are given by the
$D^n$ for $n \in \mathbb{N}$.

=--

### Distribution theory

Since a space of [[smooth functions]] on a [[smooth manifold]] is canonically a smooth set, it is natural to consider the _smooth_ [[linear functionals]] on such [[mapping spaces]]. These turn out to be equivalent to the [[continuous linear functionals]], hence to [[distributional densities]]. See at _[[distributions are the smooth linear functionals]]_ for details.


## Variants and generalizations
 {#VariantsAndGeneralizations}

### Synthetic differential geometry

The [[site]] [[CartSp]]${}_{smooth}$ may be replaced by the site [[CartSp]]${}_{th}$ (see there) whose objects are products of smooth Cartesian spaces with [[infinitesimally thickened points]]. The corresponding [[sheaf topos]] $Sh(CartSp_{th})$ is called the _[[Cahiers topos]]_. It contains smooth spaces with possibly infinitesimal extension and is a model for [[synthetic differential geometry]] (a "[[smooth topos]]"), which $Sh(CartSp)$ is not.

The two toposes are related by an [[adjoint quadruple]] of functors that witness the fact that the objects of $Sh(CartSp_{th})$ are possiby infinitesimal extensions of objects in $Sh(CartSp)$. 
For more discussion of this see [[synthetic differential ∞-groupoid]].

### Higher smooth geometry

The topos of smooth spaces has an evident generalization from [[geometry]] to [[higher geometry]], hence from [[differential geometry]] to [[higher differential geometry]]: to an [[(∞,1)-topos]] of _[[smooth ∞-groupoids]]_. See there for more details. 

$\,$

## Related concepts

[[!include geometries of physics -- table]]

$\,$

## References

The category of sheaves of the site of smooth manifolds appears as a model for [[homotopy types]] in

* [[Denis-Charles Cisinski]], Ch. 6 in: *Faisceaux localement asph&eacute;riques* (2003) &lbrack;[pdf](https://cisinski.app.uni-regensburg.de/mtest2.pdf), [[Cisinski-FaisceauxLocAsph.pdf:file]]&rbrack;

and in the context of [[simplicial homotopy theory]] in:

* [[Daniel Dugger]], section 3.4, from page 29 on in:  _Sheaves and Homotopy Theory_ &lbrack;[web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf)&rbrack;

  > (the [[point of a topos|topos points]] of $Sh(Diff)$ are discussed there in example 4.1.2 on p. 36, mentioned before on p. 31)

The equivalent incarnation over the smaller site [[CartSp]] and discussion as a [[cohesive topos]] appears in

* {#Schreiber13} [[Urs Schreiber]], Def. 1.2.16, Def. 1.3.58 of: _[[schreiber:differential cohomology in a cohesive topos]]_ &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;


{#TerminologyOrigin} The terminology "smooth set" is due to

* nLab: *[[smooth set]]* --- from [revision 10](https://ncatlab.org/nlab/revision/diff/smooth+set/10) on (Feb 2013)

* [Schreiber 2013](#dcct), [§1.2.2, p. 48](https://arxiv.org/pdf/1310.7930v1#page=48)

  (which otherwise speaks of "smooth [[0-types]]")

* [[Urs Schreiber]]: *[[geometry of physics -- smooth sets]]* --- from [revision 3](https://ncatlab.org/nlab/revision/diff/geometry+of+physics+--+smooth+sets/3) on (Nov 2014)

* [[Igor Khavkine]], [[Urs Schreiber]], Def. 2.1 in: _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ &lbrack;[arXiv:1701.06238](https://arxiv.org/abs/1701.06238)&rbrack;



Discussion of smooth sets as a [[convenient category of spaces|convenient category]] for [[variational calculus]] of [[Lagrangian quantum field theory|Lagrangian]] [[classical field theory]]:

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]], *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]*, Journal of Geometry and Physics **213** (2025) 105462 &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301), [doi:10.1016/j.geomphys.2025.105462](https://doi.org/10.1016/j.geomphys.2025.105462)&rbrack;

Exposition:

* [[Grigorios Giotopoulos]]:  *Classical field theory in the topos of smooth sets*, [talk at](Center+for+Quantum+and+Topological+Systems#GiotopoulosOct2023) [[CQTS]] (Oct 2023) &lbrack;[[Giotopoulos-FieldTheoryInSmoothSets.pdf:file]], video:[YT](https://youtu.be/7Bw9CJct8QY)&rbrack;

* [[Grigorios Giotopoulos]]: *Towards Non-Perturbative Lagrangian Field Theory via the Topos of Smooth Sets*, [talk at](CQTS##Giotopoulos2024) *[M-Theory and Mathematics 2024](M-Theory+and+Mathematics#2024)* (Jan 2024) &lbrack;video: [kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_z8xmdmu5?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_z8xmdmu5)&rbrack;

* [[Grigorios Giotopoulos]]: *Sheaf Topos Theory as a setting for Physics*, talk at *[Workshop on Noncommutative and Generalized Geometry in String Theory](http://www.physics.ntua.gr/corfu2024/nc.html)*, Corfu Summer Institute (2024) &lbrack;[[Giotopoulos-ToposTheoryForPhysics.pdf:file]]&rbrack;
  > (also on [[super smooth sets]])

* [[Grigorios Giotopoulos]]: *Sheaf Topos Theory: A powerful setting for Lagrangian Field Theory* &lbrack;[arXiv:2504.08095](https://arxiv.org/abs/2504.08095)&rbrack;





[[!redirects smooth space]]
[[!redirects smooth spaces]]

[[!redirects smooth sets]]

[[!redirects SmoothSet]]