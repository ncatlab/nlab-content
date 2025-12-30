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


\tableofcontents

## Idea
 {#Idea}

The concept of a _smooth sets_ (or _smooth spaces_) &lbrack;[Schreiber 2013](#Schreiber13), [2014](#Schreiber14)&rbrack;, is a generalization of that of [[smooth manifolds]] beyond that of [[diffeological spaces]]: A smooth set is a [[generalized smooth space]] that is characterized by how it may be _probed_ by smooth [[Cartesian spaces]].


For example, [[moduli spaces]] of [[differential forms]] exist as smooth sets but not as [[diffeological spaces]] (much less as [[smooth manifolds]]). Thereby, smooth sets constitute a natural foundation for the [[geometry of physics]], specifically of [[variational calculus]] and [[Lagrangian field theory]] &lbrack;[Schreiber 2013b](#Schreiber13b), [2017](#Schreiber17), [Giotopoulos & Sati 2023](#GiotopoulosSati23)&rbrack;.

Hence the category of smooth sets is a *[[nice category of spaces|convenient categories of spaces]]* for [[differential topology]], in a precise technical sense: It is a [[topos]] and in fact a [[cohesive topos]] &lbrack;[Schreiber 2013 §4.4](#Schreiber13)&rbrack;.

From a broader perspective, smooth sets are equivalently the [[set truncation|0-truncated]] [[smooth ∞-groupoids]], the latter generalizing smooth sets from [[geometry]] to [[higher geometry]], specifically from [[differential geometry]] to [[higher differential geometry]], forming a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] (exposition in [Schreiber 2025](#Schreiber25)). Thereby, smooth sets are part of a hierarchy of ever more *[[nice category of spaces|convenient categories of spaces]]* for [[differential topology]]:

\begin{imagefromfile}
    "file_name": "ConvenientCategoriesOfSpaces.png",
    "width": 860,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "From [Sati-Schreiber 2025](#SatiSchreiber25)"
\end{imagefromfile}



## Definition

One way to define category of **smooth sets** is as the [[sheaf topos]]

$$
  SmthSet
  \coloneqq 
  Sh(SmthMfd)
$$

of [[sheaves]] on the [[site]] [[SmthMfd]] of [[smooth manifolds]] equipped with its standard [[coverage]] ([[Grothendieck topology]]) given by [[open covers]].

Since $SmthMfd$ is [[equivalence of categories|equivalent]] to the category of [[manifolds]] _embedded_ into $\mathbb{R}^\infty$, $SmthMfd$ is an [[essentially small category]], so there are no size issues involved in this definition.

But since manifolds themselves are defined in terms of gluing conditions, the [[Grothendieck topos]] $SmthSet$ depends on much less than all of $SmthMfd$.

Let

$$
  Ball 
    \coloneqq
  \big\{ 
     (D^n_{int} 
     \to 
     D^m_{int}) 
     \in SmthMfd 
     \vert 
     n,m \in \mathbb{N}
  \big\}
$$

and

$$
  CartSp 
    \coloneqq 
  \big\{ 
    (\mathbb{R}^n 
      \to 
    \mathbb{R}^m) 
      \in SmthMfd  
    \vert| 
      n,m \in \mathbb{N}
  \big\}
$$

be the [[full subcategories]] $Ball$ and [[CartSp]] of $SmthMfd$ on open balls and on cartesian spaces, respectively. Then the corresponding [[sheaf]] [[toposes]] are still those of smooth spaces:

$$
  \begin{aligned}
    SmthSet
      &\simeq Sh(Ball)
    \\
     & \simeq Sh(CartSp)
  \end{aligned}
  \,.
$$


## Examples

* The category of ordinary [[manifolds]] is a [[full subcategory]] of smooth spaces:
  $$
    SmthMfd \hookrightarrow SmoothSet
    \,.
  $$
  When one regards smooth spaces concretely as sheaves on $SmthMfd$, then this inclusion is of course just the [[Yoneda embedding]].

* The full [[subcategory]] 
  $$
    DiffSp \subset SmoothSet
  $$
  on [[concrete sheaf|concrete sheaves]] is called the category of *[[diffeological spaces]]*.

  * The standard class of examples of smooth spaces that motivate their use even in cases where one starts out being intersted just in [[smooth manifolds]] are **mapping spaces**: for $X$ and $\Sigma$ two smooth spaces (possibly just ordinary smooth manifolds), by the [[closed monoidal structure on presheaves]] the **mapping space** $[\Sigma,X]$, i.e. the space of smooth maps $\Sigma \to X$ exists again naturally as a smooth. By the general formula it is given as a [[sheaf]] by the assignment

    $$
      [\Sigma,X] 
       \colon 
      U \mapsto SmthSet(\Sigma \times U, X)
     \,.
    $$

    If $X$ and $\Sigma$ are ordinary manifolds, then the [[hom-set]] on the right sits inside that of the underlying sets $SmthSet(\Sigma \times U , X) \subset Set({|\Sigma|} \times {|U|}, {|X|} )$ so that $[\Sigma,X]$ is a [[diffeological space]].

    The above formula says that a $U$-parameterized family of maps $\Sigma \to X$ is smooth as a map into the smooth space $[\Sigma,X ]$ precisely if the corresponding map of sets $U \times \Sigma \to X$ is an ordinary morphism of smooth manifolds.

* The canonical examples of smooth spaces that are not diffeological spaces are the sheaves of (closed) [[differential forms]]:
  $$
    K^n \colon U \mapsto \Omega^n_{closed}(U)
    \,.
  $$

* The category 
  $$
    SimpSmthSet 
      \coloneqq
  SmthSet^{\Delta^{op}}
  $$
  equivalently that of sheaves on $SmthMfd$ with values in [[simplicial sets]]
  $$
    \cdots \simeq Sh(SmthMfd, sSet)
  $$
  of [[simplicial objects]] in smooth spaces naturally carries the structure of a  [[homotopical category]] (for instance the [[model structure on simplicial sheaves]] or that of a Brown [[category of fibrant objects]] (if one restricts to locally Kan simplicial sheaves)) and as such is a [[presentable (∞,1)-category|presentation]] for the [[(∞,1)-topos]] of[[smooth ∞-stacks]].


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
    SmthSet
$$

where the [[inverse image]] morphism -- the [[stalk]] --
is given on $A \in SmthSet$ by

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

$SmthSet$ has [[point of a topos|enough points]]: they are given by the $D^n$ for $n \in \mathbb{N}$.

=--

### Distribution theory

Since a space of [[smooth functions]] on a [[smooth manifold]] is canonically a smooth set, it is natural to consider the _smooth_ [[linear functionals]] on such [[mapping spaces]]. These turn out to be equivalent to the [[continuous linear functionals]], hence to [[distributional densities]]. See at _[[distributions are the smooth linear functionals]]_ for details.


## Variants and generalizations
 {#VariantsAndGeneralizations}

### Synthetic differential geometry

The [[site]] [[CartSp]]${}_{smooth}$ may be replaced by the site [[CartSp]]${}_{th}$ (see there) whose objects are products of smooth Cartesian spaces with [[infinitesimally thickened points]]. The corresponding [[sheaf topos]] $Sh(CartSp_{th})$ is called the _[[Cahiers topos]]_. It contains smooth spaces with possibly infinitesimal extension and is a model for [[synthetic differential geometry]] (a "[[smooth topos]]"), which $Sh(CartSp)$ is not.

The two toposes are related by an [[adjoint quadruple]] of functors that witness the fact that the objects of $Sh(CartSp_{th})$ are possiby infinitesimal extensions of objects in $Sh(CartSp)$. 
For more discussion of this see [[synthetic differential ∞-groupoid]].


\linebreak


## Related concepts

* [[smooth groupoid]], [[smooth infinity-groupoid|smooth $\infty$-groupoid]]

[[!include geometries of physics -- table]]

$\,$


## References

The category of sheaves of the site of smooth manifolds is considered as a model for [[homotopy types]] inL

* [[Denis-Charles Cisinski]], Ch. 6 in: *Faisceaux localement asph&eacute;riques* (2003) &lbrack;[pdf](https://cisinski.app.uni-regensburg.de/mtest2.pdf), [[Cisinski-FaisceauxLocAsph.pdf:file]]&rbrack;

and in the context of [[simplicial homotopy theory]] in:

* [[Daniel Dugger]], section 3.4, from page 29 on in:  _Sheaves and Homotopy Theory_ &lbrack;[web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf)&rbrack;
  > (the [[point of a topos|topos points]] of $Sh(Diff)$ are discussed there in example 4.1.2 on p. 36, mentioned before on p. 31)

and as a model for [[generalized smooth spaces]] in

* [[Ib Madsen]], [[Michael Weiss]], appendix A.1 of: *The stable moduli space of Riemann surfaces: Mumford’s conjecture*, Annals of Mathematics **165** 3 (2007) 843–941 &lbrack;[arXiv:math/0212321](https://arxiv.org/abs/math/0212321), [doi:10.4007/annals.2007.165.843](https://doi.org/http://doi.org/10.4007/annals.2007.165.843)&rbrack;
  > (where a special case of the [[smooth Oka principle]] is proven)


The equivalent incarnation over the [[dense subsite]] [[CartSp]] and the understanding as a [[cohesive topos]] is due to:

* {#Schreiber13} [[Urs Schreiber]], Def. 1.2.16, Def. 1.3.58 of: _[[schreiber:differential cohomology in a cohesive topos]]_ &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;

{#TerminologyOrigin} The terminology "smooth set" is due to

* nLab: *[[smooth set]]* --- from [revision 10](https://ncatlab.org/nlab/revision/diff/smooth+set/10) on (Feb 2013)

* [Schreiber 2013](#Schreiber13), [§1.2.2, p. 48](https://arxiv.org/pdf/1310.7930v1#page=48)
  > (which otherwise speaks of "smooth [[0-types]]")

* {#Schreiber14} [[Urs Schreiber]]: *[[geometry of physics -- smooth sets]]* --- from [revision 3](https://ncatlab.org/nlab/revision/diff/geometry+of+physics+--+smooth+sets/3) on (Nov 2014)

* {#KhavkineSchreiber17} [[Igor Khavkine]], [[Urs Schreiber]], Def. 2.1 in: _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ &lbrack;[arXiv:1701.06238](https://arxiv.org/abs/1701.06238)&rbrack;
  > (generalization to [[formal smooth sets]])

further discussed in the context of ([[cohesive (infinity,1)-toposes|higher]], [[singular cohesion|singular]]) [[cohesive toposes]] in:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Ex. 1.26 in: *[[schreiber:The Character Map in Non-Abelian Cohomology]]*, World Scientific (2023) &lbrack;[doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;

* {#SatiSchreiber25} [[Hisham Sati]], [[Urs Schreiber]], Ntn. 4.3.15 in: *[[schreiber:Equivariant Principal infinity-Bundles|Equivariant Principal $\infty$-Bundles]]*, Cambridge University Press (2025) &lbrack;[arXiv:2112.13654](https://arxiv.org/abs/2112.13654)&rbrack;


Discussion of smooth sets as a [[convenient category of spaces|convenient category]] for [[variational calculus]] of [[Lagrangian quantum field theory|Lagrangian]] [[classical field theory]]:

* {#Schreiber13b} [[Urs Schreiber]]: *[[schreiber:Classical field theory via Cohesive homotopy types]]* &lbrack;[arXiv:1311.1172](https://arxiv.org/abs/1311.1172), [pdf](/schreiber/files/classicalinhigher.pdf)&rbrack;

* {#Schreiber17} [[Urs Schreiber]]: *[[geometry of physics -- perturbative quantum field theory|Geometry of Physics -- Perturbative Quantum Field Theory]]*, lecture notes for a course *<a href="https://ncatlab.org/schreiber/show/65-409%3A+Mathematical+Quantum+Field+Theory">Mathematical Quantum Field Theory</a>*, Hamburg University (2017)  &lbrack;[[Schreiber_pQFT20211103.pdf:file]], [PhysicsForums version](https://www.physicsforums.com/insights/a-first-idea-of-quantum-field-theory/)&rbrack;

* {#GiotopoulosSati23} [[Grigorios Giotopoulos]], [[Hisham Sati]]: *Field Theory via Higher Geometry I: [[schreiber:Smooth Sets of Fields]]*, Journal of Geometry and Physics **213** (2025) 105462 &lbrack;[arXiv:2312.16301](https://arxiv.org/abs/2312.16301), [doi:10.1016/j.geomphys.2025.105462](https://doi.org/10.1016/j.geomphys.2025.105462)&rbrack;

Exposition:

* [[Grigorios Giotopoulos]]:  *Classical field theory in the topos of smooth sets*, [talk at](Center+for+Quantum+and+Topological+Systems#GiotopoulosOct2023) [[CQTS]] (Oct 2023) &lbrack;[[Giotopoulos-FieldTheoryInSmoothSets.pdf:file]], video:[YT](https://youtu.be/7Bw9CJct8QY)&rbrack;

* {#Schreiber25} [[Urs Schreiber]]: *[[schreiber:Higher Topos Theory in Physics]]*, [[nLab:Encyclopedia of Mathematical Physics 2nd ed]]$\;$**4** (2025) 62-76 &lbrack;[doi:10.1016/B978-0-323-95703-8.00210-X](https://doi.org/10.1016/B978-0-323-95703-8.00210-X), [ISBN:9780323957038](https://shop.elsevier.com/books/encyclopedia-of-mathematical-physics/szabo/978-0-323-95703-8), [arXiv:2311.11026](https://arxiv.org/abs/2311.11026)&rbrack;

* [[Grigorios Giotopoulos]]: *Towards Non-Perturbative Lagrangian Field Theory via the Topos of Smooth Sets*, [talk at](CQTS##Giotopoulos2024) *[M-Theory and Mathematics 2024](M-Theory+and+Mathematics#2024)* (Jan 2024) &lbrack;video: [kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_z8xmdmu5?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_z8xmdmu5)&rbrack;

* [[Grigorios Giotopoulos]]: *Sheaf Topos Theory as a setting for Physics*, talk at *[Workshop on Noncommutative and Generalized Geometry in String Theory](http://www.physics.ntua.gr/corfu2024/nc.html)*, Corfu Summer Institute (2024) &lbrack;[[Giotopoulos-ToposTheoryForPhysics.pdf:file]]&rbrack;
  > (also on [[super smooth sets]])

* [[Grigorios Giotopoulos]]: *Sheaf Topos Theory: A powerful setting for Lagrangian Field Theory* &lbrack;[arXiv:2504.08095](https://arxiv.org/abs/2504.08095)&rbrack;

* [[Alberto Ibort]], Arnau Mas: *Smooth sets of fields: A pedagogical introduction*, Geometric Mechanics (2025) &lbrack;[arXiv:2510.20422](https://arxiv.org/abs/2510.20422), [doi:10.1142/S2972458925400052](https://doi.org/10.1142/S2972458925400052), [ResearchGate:394210704](https://www.researchgate.net/publication/394210704)&rbrack;




In analogy with smooth sets one may consider "D-topological sets" (among [[D-topological infinity-groupoids]]), forming the sheaf topos over the site $Cart_{top}$ of Cartesian spaces with *continuous* maps between them.

On $Sh(Cart_{top})$ as a [[classifying topos]]:

* [[Jonas Frey]]: *$Sh(Cart)$ as a classifying topos* (2023) &lbrack;[github pdf](https://github.com/jonas-frey/pdfs/blob/master/cartesian-may-2023.pdf)&rbrack;



[[!redirects smooth space]]
[[!redirects smooth spaces]]

[[!redirects smooth sets]]

[[!redirects SmoothSet]]