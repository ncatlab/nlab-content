
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **G-structure** on an $n$-[[manifold]] $M$, for a given structure group $G$, is a $G$-subbundle of the [[frame bundle]] (of the [[tangent bundle]]) of $M$. 

Equivalently, this means that a $G$-structure is a choice of [[reduction of structure groups|reduction]] of the canonical structure group $GL(n)$ of the [[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] along the given inclusion $G \hookrightarrow GL(n)$.

More generally, one can consider the case $G$ is not a [[subgroup]] but equipped with any group homomorphism $G \to GL(n)$. If this is instead an [[epimorphism]] one speaks of a [[lift of structure groups]].

Both cases, in turn, can naturally be understood as special cases of [[twisted differential c-structures]], which is a notion that applies more generally to [[principal infinity-bundles]].

## Definition

### General

Given a [[smooth manifold]] $X$ of [[dimension]] $n$ and given a [[Lie group|Lie]] [[subgroup]] $G \hookrightarrow GL(n)$ of the [[general linear group]], then a _$G$-structure_ on $X$ is a [[reduction of structure groups|reduction of the structure group]] of the [[frame bundle]] of $X$ to $G$.

There are many more explicit (and more abstract) equivalent ways to say this, which we discuss below. There are also many evident variants and generalizations. 

Notably one may consider reductions of the frames in the $k$th order [[jet bundle]]. (e. g. [Alekseevskii](#Alekseevskii)) This yields order $k$ $G$-structure and the ordinary $G$-structures above are then first order.

Moreover, the definition makes sense for generalized [[manifolds]] modeled on other base spaces than just [[Cartesian spaces]]. In particular there are evident generalizations to [[supermanifolds]] and to [[complex manifolds]].

### In terms of $(B,f)$-structures 
 {#InTermsOfBfStructures}

+-- {: .num_defn #BfStructure}
###### Definition

A **$(B,f)$-structure** is 

1. for each $n\in \mathbb{N}$ a [[pointed topological space|pointed]] [[CW-complex]] $B_n \in Top_{CW}^{\ast/}$

1. equipped with a pointed [[Serre fibration]] 

   $$
     \array{
       B_n
       \\
       \downarrow^{\mathrlap{f_n}}
       \\
       B O(n)
     }
   $$

   to the [[classifying space]] $B O(n)$ ([def.](classifying+space#EOn));

1. for all $n_1 \leq n_2$ a pointed continuous function

   $\iota_{n_1, n_2} \;\colon\; B_{n_1} \longrightarrow B_{n_2}$

   which is the identity for $n_1 = n_2$;

such that for all $n_1 \leq n_2 \in \mathbb{N}$ these [[commuting square|squares commute]]

$$
  \array{
    B_{n_1} &\overset{\iota_{n_1,n_2}}{\longrightarrow}& B_{n_2}
    \\
    {}^{\mathllap{f_{n_1}}}\downarrow && \downarrow^{\mathrlap{f_{n_2}}}
    \\
    B O(n_1) &\longrightarrow& B O(n_2)
  }
  \,,
$$

where the bottom map is the canonical one ([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne)).

The $(B,f)$-structure is **multiplicative** if it is moreover equipped with a system of maps $\mu_{n_1,n_2} \colon B_{n_1}\times B_{n_2} \to B_{n_1 + n_2}$ which cover the canonical multiplication maps ([def.](classifying+space#WhitneySumMapOnClassifyingSpaces))

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{\mu_{n_1, n_2}}{\longrightarrow}&
    B_{n_1 + n_2}
    \\
    {}^{\mathllap{f_{n_1} \times f_{n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{f_{n_1 + n_2}}}
    \\
    B O(n_1) \times B O(n_2)
     &\longrightarrow&
    B O(n_1 + n_2)
  }
$$
 
and which satisfy the evident [[associativity]] and [[unitality]], for $B_0 = \ast$ the unit, and, finally, which commute with the maps $\iota$ in that all $n_1,n_2, n_3 \in \mathbb{N}$ these squares commute:


$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{id \times \iota_{n_2,n_2+n_3}}{\longrightarrow}&
    B_{n_1} \times B_{n_2 + n_3}
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1,n_2 + n_3}}}
    \\
    B_{n_1 + n_2}
      &\underset{\iota_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
$$

and

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{\iota_{n_1,n_1+n_3} \times id}{\longrightarrow}&
    B_{n_1+n_3} \times B_{n_2 }
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1 + n_3 , n_2}}}
    \\
    B_{n_1 + n_2}
      &\underset{\iota_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
  \,.
$$


Similarly, an **$S^2$-$(B,f)$-structure** is a compatible system

$$
  f_{2n} \colon B_{2n} \longrightarrow B O(2n)
$$

indexed only on the even natural numbers.

Generally, an **$S^k$-$(B,f)$-structure** for $k \in \mathbb{N}$, $k \geq 1$ is a compatible system

$$
  f_{k n} \colon B_{ kn} \longrightarrow B O(k n)
$$

for all $n \in \mathbb{N}$, hence for all $k n \in k \mathbb{N}$.

=--

([Lashof 63](#Lashof63), [Stong 68, beginning of chapter II](#Stong68), [Kochmann 96, section 1.4](#Kochmann96))

See also at _[[B-bordism]]_.


+-- {: .num_example #ExamplesOfBfStructures}
###### Example

Examples of $(B,f)$-structures (def. \ref{BfStructure}) include the following:

1. $B_n = B O(n)$ and $f_n = id$ is **orthogonal structure** (or "no structure");

1. $B_n = E O(n)$ and $f_n$ the [[universal principal bundle]]-projection is **[[framing]]-structure**;

1. $B_n = B SO(n) = E O(n)/SO(n)$ the classifying space of the [[special orthogonal group]] and $f_n$ the canonical projection is **[[orientation]] structure**;

1. $B_n = B Spin(n) = E O(n)/Spin(n)$ the classifying space of the [[spin group]] and $f_n$ the canonical projection is **[[spin structure]]**.

Examples of $S^2$-$(B,f)$-structures include

1. $B_{2n} = B U(n) = E O(2n)/U(n)$ the classifying space of the [[unitary group]], and $f_{2n}$ the canonical projection is **[[almost complex structure]]**.

=--


+-- {: .num_defn }
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$, and given a $(B,f)$-structure as in def. \ref{BfStructure}, then a **$(B,f)$-structure on the manifold** is an [[equivalence class]] of the following structure:

1. an [[embedding]] $i_X \; \colon \; X \hookrightarrow \mathbb{R}^k$ for some $k \in \mathbb{N}$;

1. a [[homotopy class]] of a  [[lift]] $\hat g$ of the classifying map $g$ of the [[tangent bundle]] 

   $$
     \array{
       && B_{n}
       \\
       &{}^{\mathllap{\hat g}}\nearrow& \downarrow^{\mathrlap{f_n}}
       \\
       X &\overset{g}{\hookrightarrow}& B O(n)
     }
     \,.
   $$

The equivalence relation on such structures is to be that generated by the relation $((i_{X})_1, \hat g_1) \sim ((i_{X})_,\hat g_2)$ if 

1. $k_2 \geq k_1$

1. the second inclusion factors through the first as 

   $$
     (i_X)_2 
       \;\colon\; 
     X 
       \overset{(i_X)_1}{\hookrightarrow}
     \mathbb{R}^{k_1} 
       \hookrightarrow
     \mathbb{R}^{k_2}
   $$

1. the lift of the classifying map factors accordingly (as homotopy classes)

   $$
     \hat g_2
       \;\colon\;
     X 
       \overset{\hat g_1}{\longrightarrow}
     B_{n}
       \longrightarrow
     B_{n}
     \,.
   $$

=--



### In terms of subbundles of the frame bundle
 {#InTermsOfSubbundlesOfTheFrameBundle}

+-- {: .num_defn}
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$ with [[frame bundle]] $Fr(X)$, and given a [[Lie group]] [[monomorphism]]

$$
  G \longrightarrow GL(\mathbb{R}^n)
$$

into the [[general linear group]], then a _$G$-structure_ on $X$ is an $G$-[[principal bundle]] $P \to X$ equipped with an inclusion of [[fiber bundles]]

$$
  \array{
    P &&\hookrightarrow&& Fr(X)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

which is $G$-equivariant. 

=--

([Sternberg 64, section VII, def. 2.1](#Sternberg64)).


+-- {: .num_remark}
###### Remark

From this perspective, a $G$-structure consists of the collection of all $G$-[[frame field|frames]] on a manifold. For instance for an [[orthogonal structure]] it consists of all those frames which are pointwise an [[orthonormal basis]] of the [[tangent bundle]] (with respect to the [[Riemannian metric]] which is defined by the orthonormal structure).

=--

Accordingly: 

+-- {: .num_defn #GStructureGeneratedByFrameField}
###### Definition

Given $G \hookrightarrow GL(n)$ and given any one [[frame field]] $\sigma \colon X \to Fr(X)$ over a [[manifold]] $X$, then acting with $G$ on $\sigma$ at each point produces a $G$-subbundle. This is called the $G$-structure _generated_ by the frame field $\sigma$.

=-- 



### In terms of Cartan connections

A $G$-structure equipped with compatible [[connection on a bundle|connection]] data is equivalently a [[Cartan connection]] for the inclusion $(G \hookrightarrow \mathbb{R}^n \rtimes G)$. 

See at _[Cartan connection -- Examples -- G-structures](Cartan+connection#ExampleGStructures)_

### In higher differential geometry

#### $G$-structure on a $K$-principal bundle

We give an equivalent definition of $G$-structures in terms of [[higher differential geometry]] ("from the [[nPOV]]"). This serves to clarify the slightly subtle but important difference between existence and choice of $G$-structure, and seamlessly embeds the notion into the more general context of [[twisted differential c-structures]].

+-- {: .num_defn}
###### Definition

Let $G \to K$ be a [[homomorphism]] of [[Lie groups]]. Write 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}K
$$

for the morphism of [[delooping]] [[Lie groupoids]] ( the [[smooth infinity-groupoid|smooth]] [[moduli stacks]] of smooth $K$- and $G$-[[principal bundles]], respectively).

For $X$ a [[smooth manifold]] (or generally an [[orbifold]] or [[Lie groupoid]], etc.) Let $P \to X$ be a $K$-[[principal bundle]] and let 

$$
  k \colon X \longrightarrow \mathbf{B}K
$$ 

be any choice of morphism [[modulating morphism|modulating]] it.

Write $\mathbf{H}(X, \mathbf{B}G)$ etc. for the [[derived hom space|hom-groupoid]] of [[smooth infinity-groupoid|smooth groupoids]] / smooth stacks . This is equivalently the groupoid of $G$-principal bundles over $X$ and smooth [[gauge transformations]] between them.

Then the **groupoid of $G$-structure on $P$** (with respect to the given morphism $G \to K$) is the [[homotopy pullback]]

$$
  \mathbf{c}Struc_{[P]}(X)
  :=
  \mathbf{H}(X, \mathbf{B}G)
   \times_{\mathbf{H}(X, \mathbf{B}K)}
  \{k\}
  \,.
$$

$$
  \array{
    \mathbf{c}Struc_{[P]}(X)
    &\longrightarrow&
    \ast
    \\
    \downarrow & \swArrow_\simeq& \downarrow^{\mathrlap{k}}
    \\
    \mathbf{H}(X, \mathbf{B}G)
     &\stackrel{\mathbf{H}(X, \mathbf{c})}{\longrightarrow}&
    \mathbf{H}(X, \mathbf{B}K)
  }
$$

(the groupoid of _[[twisted differential c-structure|twisted c-structures]]_).


=--

+-- {: .num_remark}
###### Remark

If here $k$ is trivial in that it factors through the point, $k \colon X \to \ast \to \mathbf{B}K$ then this homotopy fiber product is $\mathbf{H}(X,K/G)$, where $K/G$ is the [[coset space]] ([[Klein geometry]]) which itself sits in the [[homotopy fiber sequence]]

$$
   K/G \to \mathbf{B}G \to \mathbf{B}K
  \,.
$$

=--

+-- {: .num_example}
###### Example

Specifically, when $X$ is a [[smooth manifold]] of [[dimension]] $n$, the [[frame bundle]] $Fr(X)$ is [[modulating moprhism|modulated]] by a morphism $\tau_X \colon X \to \mathbf{B} GL(n)$ into the [[moduli stack]] for the [[general linear group]] $K := GL(n)$. Then for any group homomorphism $G \to GL(n)$, a **$G$-structure** on $X$ is a $G$-structure on $Fr(X)$, as above.

=--

#### $G$-Structure on an etale $\infty$-groupoid

We discuss the concept in the generality of [[higher differential geometry]], formalized in [[differential cohesion]].

See at _[differential cohesion -- G-Structure](differential+cohesive+%28infinity%2C1%29-topos#structures)_



## Properties

### Integrability of $G$-structure

+-- {: .num_defn #Integrability}
###### Definition

A $G$-structure on a [[manifold]] $X$ is called _locally flat_ ([Sternberg 64, section VII, def. 24](#Sternberg64)) or _integrable_ (e.g. [Alekseevskii](#Alekseevskii)) if it is locally equivalent to the _standard flat $G$-structure_, def. \ref{StandardFlatGStructure}. 

This means that there is an [[open cover]] $\{U_i \to X\}$ by [[open subsets]] of the [[Cartesian space]] $\mathbb{R}^n$ such that the restriction of the $G$-structure to each of these is equivalent to the standard flat $G$-structure.

=--


See at _[[integrability of G-structures]]_ for more on this

The [[obstruction]] to integrability of $G$-structure is the _[[torsion of a G-structure]]_. See there for more.


### Relation to special holonomy

The existence of $G$-structures on tangent bundles of [[Riemannian manifolds]] is closely related to these having [[special holonomy]].

+-- {: .num_theorem}
###### Theorem

Let $(X,g)$ be a [[connected topological space|connected]] [[Riemannian manifold]]
of [[dimension]] $n$ with [[holonomy group]]  $Hol(g) \subset O(n)$.

For $G \subset O(n)$ some other [[subgroup]], $(X,g)$ admits a torsion-free 
G-structure precisely if $Hol(g)$ is [[adjoint action|conjugate]] to 
a [[subgroup]] of $G$.

Moreover, the space of such $G$-structures is the [[coset]] $G/L$,
where $L$ is the group of elements suchthat conjugating $Hol(g)$ with them
lands in $G$.

=--

This appears as ([Joyce prop. 3.1.8](#Joyce))


## Examples

### The standard flat $G$-structure
 {#TheStandardFlatGStructure}

+-- {: .num_defn #StandardFlatGStructure}
###### Definition

For $G \hookrightarrow GL(n)$ a subgroup, then the _standard flat $G$-structure_ on the [[Cartesian space]] $\mathbb{R}^n$ is the $G$-structure which is generated, via def. \ref{GStructureGeneratedByFrameField}, from the canonical [[frame field]] on $\mathbb{R}^n$ (the one which is the identity at each point, under the defining identifications).

=--

### Reduction of tangent bundle structure

* For the [[subgroup]] of $GL(n, \mathbb{R})$ of matrices of positive determinant, a $GL(n, \mathbb{R})^+$-structure defines an [[orientation]].

* For the [[orthogonal group]], an $O(n)$-structure defines a [[Riemannian metric]]. (See the discussion at [[vielbein]] and at

* For the [[special linear group]], an $SL(n,R)$-structure defines a [[volume form]]. 

* For the trivial group, an $\{e\}$-structure consists of an [[absolute parallelism]] of the manifold.

* For $n = 2 m$ even, a $GL(m, \mathbb{C})$-structure defines an [[almost complex structure]] on the manifold. It must satisfy an integrability condition to be a [[complex structure]].

### Lift of tangent bundle structure

An example for a lift of structure groups is

* for the [[spin group]]  $spin(n)$, a $G$-structure is a [[spin structure]].

This continues with lifts to the 

* [[string group]] giving [[string structure]];

* [[fivebrane group]] giving [[fivebrane structure]].

### Reduction of more general bundle structure
 {#ExamplesOfReductionsOfNonTangentBundles}

* For general $G \to K$, the corresponding notion of [[Cartan geometry]] involves $G$-structure on $K$-principal bundles (not necessarily underlying a tangent bundle).

* A $U(n,n) \hookrightarrow O(2n,2n)$-structure is a [[generalized complex structure]];

* For $H_n \to E_{n(n)}$ the inclusion of the [[maximal compact subgroup]] into the [[split real form]] of an [[exceptional Lie group]], the corresponding structure is an [[exceptional generalized geometry]].

### Complex geometric examples

* The choice of $SO(n, \mathbb{C})$ as subgroup of $GL(n, \mathbb{C})$, determines a complex Riemannian structure;

* $CO(n, \mathbb{C}) \hookrightarrow GL(n, \mathbb{C})$, a complex conformal structure;

* $Sp(2n, \mathbb{C})\hookrightarrow GL(2n, \mathbb{C})$, an almost symplectic structure;

* $GL(2, \mathbb{C}) GL(n, \mathbb{C}) \hookrightarrow GL(2n, \mathbb{C}), n \geq 3$,  determines an almost quaternionic structure;

* more generally a $GL(m, \mathbb{C}) GL(n, \mathbb{C})$-structure on a $m n$-dimensional manifold is locally identical to a Grassmannian spinor structure.

### Higher geometric examples

See the list at [[twisted differential c-structure]].

## Further issues

> Need to talk about integrability conditions, and those of higher degree. Also need to discuss [[pseudo-group|pseudo-groups]].

## Related concepts

* [[special holonomy]]

* [[integrability of G-structures]]

* [[homothety]]

## References

### Traditional

The concept of topological $G$-structure (lifts of homotopy classes of classifying maps) originates with [[cobordism theory]]. Early expositions in terms of [(B,f)-structures](#InTermsOfBfStructures) include

* {#Lashof63} [[Richard Lashof]], _Poincar&#233; duality and cobordism_, Trans. AMS 109 (1963), 257-277

* {#Stong68} [[Robert Stong]], beginning of chapter II of _Notes on Cobordism theory_, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [publisher page](http://press.princeton.edu/titles/6465.html))

* {#Kochmann96} [[Stanley Kochmann]], section 1.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996
 
The concept in differential geometry originates around the work of [[Eli Cartan]] ([[Cartan geometry]]) and

* [[Shiing-Shen Chern]], _The geometry of G-structures_, Bull. Amer. Math. Soc. 72(2): 167&#8211;219. 1966 ([pdf](http://www.ams.org/journals/bull/1966-72-02/S0002-9904-1966-11473-8/S0002-9904-1966-11473-8.pdf), [Euclid](http://projecteuclid.org/euclid.bams/1183527777))

Textbook accounts include

* {#Sternberg64} [[Shlomo Sternberg]], chapter VII of _Lectures on differential geometry_, Prentice-Hall (1964)

* [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], _Foundations of differential geometry_ , Volume 1 (1963), Volume 2 (1969), Interscience Publishers, reprinted 1996 by Wiley Classics Library

Surveys include

* {#Alekseevskii} D. V: Alekseevskii, _$G$-structure on a manifold_ in M. Hazewinkel (ed.) _Encyclopedia of Mathematics, Volume 4_

* [Wikipedia](http://en.wikipedia.org/wiki/G-structure)

Discussion with an eye towards [[special holonomy]] is in 

* {#Joyce} [[Dominic Joyce]], section 2.6 of _Compact manifolds with special holonomy_ , Oxford Mathematical Monogrophs (200)

Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

### In supergeometry

Discussion of $G$-structures in [[supergeometry]] includes

* [[Dmitri Alekseevsky]], [[Vicente Cortés]], [[Chandrashekar Devchand]], [[Uwe Semmelmann]], _Killing spinors are Killing vector fields in Riemannian Supergeometry_ ([arXiv:dg-ga/9704002](http://arxiv.org/abs/dg-ga/9704002))

### In complex geometry

* Sergey Merkulov, _On group theoretic aspects of the non-linear twistor transform_, ([pdf](http://people.maths.ox.ac.uk/lmason/Tn/40/TN40-07.pdf))

and his chapter A in

* Yuri Manin, _Gauge Field Theory and Complex Geometry_, Springer.

* Norman Wildberger, _On the complexication of the classical geometries and exceptional numbers_, ([pdf](http://web.maths.unsw.edu.au/~norman/papers/L.pdf))

* Jun-Muk Hwang, _Rational curves and prolongations of G-structures_,[arXiv:1703.03160](https://arxiv.org/abs/1703.03160)

### In higher geometry

Some discussion in [[higher differential geometry]] is in section 4.4.2 of

* _[[schreiber:differential cohomology in a cohesive topos]]_

Formalization in [[homotopy type theory]] is in 

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017

[[!redirects G-structures]]

[[!redirects (B,f)-structure]]
[[!redirects (B,f)-structures]]
