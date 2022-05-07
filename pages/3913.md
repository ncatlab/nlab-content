
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Thom space** $Th(V)$ of a real [[vector bundle]] $V \to X$ over a [[topological space]] $X$ is the [[topological space]] obtained by first forming the disk bundle $D(V)$ of (unit) disks in the [[fibers]] of $V$ (with respect to a [[metric]] given by any choice of [[orthogonal structure]]) and then identifying to a point the [[boundaries]] of all the disks, i.e. forming the [[quotient topological space]] by the [[unit sphere bundle]] $S(V)$:

$$
  Th(V) \coloneqq D(V)/S(V)
  \,.
$$

(N.B.: this is a quotient of the *total* spaces of the bundles taken in $Top$, not a bundle quotient in $Top_{/V}$.) 

This is equivalently the [[mapping cone]]

$$
  \array{
    S(V) &\longrightarrow& *
    \\
    {}^{\mathllap{p}}\downarrow &\swArrow& \downarrow
    \\
    X & \longrightarrow & Th(V)
  }
$$

in [[Top]] of the [[sphere]] [[bundle]] of $V$. Therefore more generally, for $P \to X$ any [[n-sphere]]-[[fiber bundle]] over $X$ ([[spherical fibration]]), its Thom space is the the [[mapping cone]]

$$
  \array{
    P &\longrightarrow& *
    \\
    {}^{\mathllap{p}}\downarrow &\swArrow& \downarrow
    \\
    X & \longrightarrow & Th(P)
  }
$$

of the bundle projection.


For $X$ a [[compact topological space]], $Th(V)$ is a model for [[generalized the|the]] [[one-point compactification]] of the total space $V$.

The Thom space of the rank-$n$ [[universal vector bundle]] over the [[classifying space]] $B O(n)$ of the [[orthogonal group]] is usually denoted $M O(n)$. As $n$ ranges, these spaces form the [[Thom spectrum]].



## Definition 
 {#Definition}


+-- {: .num_defn #ThomSpace}
###### Definition

Let $X$ be a [[topological space]] and let $V \to X$ be a [[vector bundle]] ([[topological vector bundle]]) over $X$ of [[rank]] $n$, which is [[associated bundle|associated]] to an [[orthogonal group|O(n)]]-[[principal bundle]]. Equivalently this means that $V \to X$ is the [[pullback]] of the [[universal vector bundle]] $E_n \to B O(n)$ over the [[classifying space]]. Since $O(n)$ preserves the [[metric]] on $\mathbb{R}^n$, by definition, such $V$ inherits the structure of a [[metric space]]-[[fiber bundle]]. With respect to this structure:

1. the **unit disk bundle** $D(V) \to X$ is the subbundle of elements of [[norm]] $\leq 1$;

1. the **[[unit sphere]] bundle** $S(V)\to X$ is the subbundle of elements of norm $= 1$;

   $S(V) \overset{i_V}{\hookrightarrow} D(V) \hookrightarrow V$;

1. the **Thom space** $Th(V)$ is the [[cofiber]] (formed in [[Top]] ([prop.](Top#DescriptionOfLimitsAndColimitsInTop))) of $i_V$ 

   $$
     Th(V) \coloneqq cofib(i_V)
   $$

   canonically regarded as a [[pointed topological space]].

$$
  \array{
    S(V) &\overset{i_V}{\longrightarrow}& D(V)
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V)
  }
  \,.
$$

If $V \to X$ is a general real vector bundle, then there exists an isomorphism to an $O(n)$-[[associated bundle]] and the Thom space of $V$ is, up to based [[homeomorphism]], that of this orthogonal bundle.

=--


+-- {: .num_remark #ThomSpaceForRankZeroBundle}
###### Remark

If the [[rank]] of $V$ is positive, then $S(V)$ is non-empty and then the Thom space is the [[quotient topological space]]

$$
  Th(V) \simeq D(V)/S(V)
  \,.
$$

However, in the degenerate case that the [[rank]] of $V$ vanishes, hence the case that $V = X\times \mathbb{R}^0 \simeq X$, then $D(V) \simeq V \simeq X$, but $S(V) = \emptyset$. Hence now the [[pushout]] defining the cofiber is

$$
  \array{
    \emptyset &\overset{i_V}{\longrightarrow}& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V) \simeq X_*
  }
  \,,
$$

which exhibits $Th(V)$ as the [[coproduct]] of $X$ with the point, hence as $X$ with a basepoint freely adjoined.

$$
  Th(X \times \mathbb{R}^0) = Th(X) \simeq X_+
  \,.
$$

=--


## Properties
 {#Properties}

### Homotopy-theoretic nature
 {#HomotopyTheoreticNature}

+-- {: .num_prop #ThomSpaceOverCWComplexIsHomotopyCofiber}
###### Proposition

Let $V \to X$ be a [[vector bundle]] over a [[CW-complex]] $X$. Then the Thom space $Th(V)$ (def. \ref{ThomSpace}) is equivalently the [[homotopy cofiber]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)) of the inclusion $S(V) \longrightarrow D(V)$ of the sphere bundle into the disk bundle.

=--

+-- {: .proof}
###### Proof

The Thom space is defined as the ordinary [[cofiber]] of $S(V)\to D(V)$. Under the given assumption, this inclusion is a [[relative cell complex]] inclusion, hence a cofibration in the [[classical model structure on topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure)). Therefore in this case the ordinary cofiber represents the homotopy cofiber ([def.](#Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)).

=--

The equivalence to the following alternative model for this homotopy cofiber is relevant when discussing [[Thom isomorphisms]] and [[orientation in generalized cohomology]]:

+-- {: .num_prop #ThomSpaceOverCWEquivalentToConeOnInclusionOfComplementOf0Section}
###### Proposition

Let $V \to X$ be a [[vector bundle]] over a [[CW-complex]] $X$. Write $V \setminus X$ for the [[complement]] of its 0-[[section]].  Then the Thom space $Th(V)$ (def. \ref{ThomSpace}) is [[homotopy equivalence|homotopy equivalent]] to the [[mapping cone]] of the inclusion $(V \setminus X) \hookrightarrow V$ (hence to the pair $(V,V \setminus X)$ in the language of [[generalized (Eilenberg-Steenrod) cohomology]]).

=--

+-- {: .proof}
###### Proof

The [[mapping cone]] of any map out of a [[CW-complex]] represents the [[homotopy cofiber]] of that map ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#StandardTopologicalMappingConeIsHomotopyCofiber)). Moreover, transformation by (weak) homotopy equivalences between morphisms induces a (weak) homotopy equivalence on their homotopy fibers ([prop.](Introduction+to+Stable+homotopy+theory+--+P#FiberOfFibrationIsCompatibleWithWeakEquivalences)). But we have such a weak homotopy equivalence, given by contracting away the fibers of the vector bundle:

$$
  \array{
    V\setminus X &\longrightarrow& V
    \\
    {}^{\mathllap{\in W_{cl}}}\downarrow && \downarrow^{\mathrlap{\in W_{cl}}}
    \\
    S(V) &\hookrightarrow& D(V)
  }
  \,.
$$

=--


### Behaviour under direct sum of vector bundles

+-- {: .num_prop #ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks}
###### Proposition

Let $V_1,V_2 \to X$ be two real [[vector bundles]]. Then the Thom space (def. \ref{ThomSpace}) of the [[direct sum of vector bundles]] $V_1 \oplus V_2 \to X$ is expressed in terms of the Thom space of the [[pullback bundles]] $V_2|_{D(V_1)}$ and $V_2|_{S(V_1)}$ of $V_2$ to the disk/sphere bundle of $V_1$ as

$$
  Th(V_1 \oplus V_2)
  \simeq
  Th(V_2|_{D(V_1)})/Th(V_2|_{S(V_1)})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that 

1. $D(V_1 \oplus V_2) \simeq D(V_2|_{Int D(V_1)}) \cup S(V_1)$;

1. $S(V_1 \oplus V_2) \simeq S(V_2|_{Int D(V_1)}) \cup Int D(V_2|_{S(V_1)})$.

(Since a point at radial distance $r$ in $V_1 \oplus V_2$ is a point at radius $r_1 \leq r$ in $V_2$ and a point at radius $\sqrt{r^2 - r_1^2}$ in $V_1$.)

=--

+-- {: .num_prop #SuspensionOfThomSpaces}
###### Proposition

For $V$ a [[vector bundle]] then the Thom space (def. \ref{ThomSpace}) of $\mathbb{R}^n \oplus V$, the [[direct sum of vector bundles]] with the trivial rank $n$ vector bundle, is [[homeomorphism|homeomorphic]] to the [[smash product]] of the Thom space of $V$ with the $n$-[[sphere]] (the $n$-fold [[reduced suspension]]).


$$
  Th(\mathbb{R}^n \oplus V) \simeq S^n \wedge Th(V) = \Sigma^n Th(V)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks} with $V_1 = \mathbb{R}^n$ and $V_2 = V$. Since $V_1$ is a trivial bundle, then

$$
  V_2|_{D(V_1)} \simeq V_2\times D^n
$$

(as a bundle over $X\times D^n$) and similarly

$$
  V_2|_{S(V_1)} \simeq V_2\times S^n
  \,.
$$


=--

+-- {: .num_remark #SuspensionPropertyOfThomSpacesInducesThomSpectra}
###### Remark

Prop. \ref{SuspensionOfThomSpaces} implies that for every vector bundle $V$ the sequence of spaces $Th(\mathbb{R}^n \oplus V)$ forms a [[suspension spectrum]]: this is _the [[Thom spectrum]]_ of $V$.

=--

+-- {: .num_example #ThomSpaceConstructionReducingToSuspension}
###### Example

By prop. \ref{SuspensionOfThomSpaces} and remark \ref{ThomSpaceForRankZeroBundle}  the Thom space (def. \ref{ThomSpace}) of a trivial vector bundle of rank $n$ is the $n$-fold [[suspension]] of the base space 

$$
  \begin{aligned}
    Th(X \times \mathbb{R}^n) 
    & \simeq S^n \wedge Th(X\times \mathbb{R}^0) 
    \\
    & \simeq S^n \wedge (X_+)
  \end{aligned}
  \,.
$$

Therefore a general Thom space may be thought of as a "twisted [[reduced suspension]]", with twist encoded by a vector bundle (or rather by its underlying [[spherical fibration]]). See at _[Thom spectrum -- For infinity-module bundles](Thom+spectrum#ForInfinityModuleBundles)_ for more on this.

Correspondingly the _[[Thom isomorphism]]_ for a given Thom space is a twisted version of the _[[suspension isomorphism]]_.

=--

+-- {: .num_prop #ThomSpaceOfExternalProductOfVectorBundles}
###### Proposition

For $V_1 \to X_1$ and $V_2 \to X_2$ to vector bundles, let $V_1 \boxtimes V_2 \to X_1 \times X_2$ be the [[direct sum of vector bundles]] of their [[pullbacks]] to $X_1 \times X_2$. The corresponding Thom space is the [[smash product]] of the individual Thom spaces:

$$
  Th(V_1 \boxtimes V_2)
  \simeq
  Th(V_1) \wedge Th(V_2)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{ThomSpaceOfExternalProductOfVectorBundles} induces on the [[Thom spectra]] of remark \ref{SuspensionPropertyOfThomSpacesInducesThomSpectra} the structure of [[ring spectra]].

=--

### CW-structure

If the base space of the vector bundle carries the structure of a [[CW-complex]], then its Thom space (def. \ref{ThomSpace}) canonically inherits the structure of a CW-complex, too:

+-- {: .num_lemma #ThomSpaceCWStructure}
###### Lemma

Let $V \to X$ be a [[vector bundle]] of [[rank]] $n \geq 1$. over a [[CW-complex]] $X$.

Then $Th(V)$ has the structure of a [[CW-complex]] with 

1. $S(E)/S(E)$ the only 0-cell 

1. precisely one $(n+k)$-cell $D^{k+n}\to Th(V)$ for each $k$-cell $D^k \to X$ of $X$, given as the [[pullback]]
   
   $$
     \array{
       D^{k+n} &\longrightarrow& D(V) &\longrightarrow& D(V)/S(V) = Th(V)
       \\
       \downarrow &(pb)& \downarrow
       \\
       D^k &\longrightarrow& X
     }
     \,.
   $$

=--

(e.g. [Cruz 04, lemma 6](#Cruz04))

In particular, $Th(V)$ has a single $n$-cell and an $(n+1)$-cell for each 1-cell of $X$.  There are no cells in $Th(C)$ between dimension $0$ and $n$. The cellular boundary of an $(n+1)$-cell is 0 if $V$ is orientable over the corresponding 1-cell of $X$, and it is twice the $n$-cell in the opposite case.  Thus $H^n(Th(V);\mathbb{Z})$ is $\mathbb{Z}$ if $V$ is orientable and $0$ if $V$ is non-orientable. In the orientable case a generator of $H^n(Th(V);\mathbb{Z})$ restricts to a generator of $H^n(S^n;\mathbb{Z})$ in the "fiber" $S^n$ of $Th(V)$ over the 0-cell of $X$, hence the same is true for all the "fibers" $S^n$ and so one has a [[Thom class]].

([MO discussion](http://mathoverflow.net/a/107864/381))

### Cohomology

+-- {: .num_remark #OrdinaryCohomologyOfThomSpaceInLowDegree}
###### Remark

Given a [[vector bundle]] $V \to X$ of [[rank]] $n$, then the [[reduced cohomology|reduced]] [[ordinary cohomology]] of its [[Thom space]] $Th(V)$ (def. \ref{ThomSpace}) vanishes in degrees $\lt n$:

$$
 \tilde H^{\bullet \lt n}(Th(V))
  \simeq
  H^{\bullet \lt n}(D(V), S(V))
  \simeq 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the [[long exact sequence]] of [[relative cohomology]] ([here](generalized+cohomology#ExactnessUnreduced))

$$
  \cdots
    \to
  H^{\bullet-1}(D(V))
   \overset{i^\ast}{\longrightarrow}
  H^{\bullet-1}(S(V))
   \longrightarrow
  H^\bullet(D(V), S(V))
    \longrightarrow
  H^{\bullet}(D(V))
   \overset{i^\ast}{\longrightarrow}
  H^{\bullet}(S(V))
    \to
  \cdots  
  \,.
$$

Since the cohomology in degree $k$ only depends on the $k$-skeleton, and since for $k \lt n$ the $k$-skeleton of $S(V)$ equals that of $X$, and since $D(V)$ is even homotopy equivalent to $X$, the morhism $i^\ast$ is an isomorphism in degrees lower than $n$. Hence by exactness of the sequence it follows that $H^{\bullet \lt n}(D(V),S(V)) = 0$.

=--



## Related concepts

* [[cobordism theory]]

* [[one-point compactification]]

* [[Thom spectrum]]

* [[Thom isomorphism]]

* [[projective bundle]]

## References

The [[Thom isomorphism]] for Thom spaces was originally found in

* [[René Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

For general discussion see

* [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. __11__  (1961)  pp. 291&#8211;310

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability, and cobordism_, Springer 1998 [googB](http://books.google.hr/books?isbn=3540620435)

* [[eom]], _[Thom space](http://eom.springer.de/t/t092680.htm)_

* [[Dale Husemöller]], _Fibre bundles_ , McGraw-Hill  (1966)

* myyn.org [Thom space](http://myyn.org/m/article/thom-space), [Thom class](http://myyn.org/m/article/thom-class), [Thom isomorphism theorem](http://myyn.org/m/article/thom-isomorphism-theorem)

See also

* [[Robert Stong]], _Notes on cobordism theory_ , Princeton Univ. Press  (1968)

* W.B. Browder, _Surgery on simply-connected manifolds_ , Springer  (1972)

* {#Cruz04} Martin Vito Cruz, _An introduction to cobordism_, 2004 ([pdf](https://math.berkeley.edu/~hutching/teach/215b-2004/vitocruz.pdf))

On [[Cohomotopy sets]] of [[Thom spaces]]:

* [[Thomas Rot]], _Homotopy classes of proper maps out of vector bundles_,  Arch. Math. 114, 107–117 (2020 ([arXiv:1808.08073](https://arxiv.org/abs/1808.08073), [doi:10.1007/s00013-019-01372-z](https://doi.org/10.1007/s00013-019-01372-z))


[[!redirects Thom spaces]]

