
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[equivariant cohomology|equivariant]] version of [[elliptic cohomology]], the higher [[chromatic homotopy theory|chromatic]] analogue of [[equivariant K-theory]].

## Definition 

### 1-Equivariant elliptic cohomology

Let $G$ be a [[compact Lie group]]. Write $T \hookrightarrow G$ for its [[maximal torus]] and $W$ for its [[Weyl group]].

Let $E \in CRing_\infty$ be an [[elliptic spectrum|elliptic]] [[E-∞ ring]] [[spectrum]] with [[elliptic curve]] $A \to Spec E$. 

+-- {: .num_defn #TheModuliSpace}
###### Definition

Write 

$$
  A_G \coloneqq \left[\left[T,\mathbb{T}\right],A\right]/W
  \;\;
  \in Sch_{/Spec E}
$$

for the [[derived scheme]] formed from the [[character group]] of the [[maximal torus]] mapped into the given [[elliptic curve]].

=--

+-- {: .num_remark}
###### Remark

This $A_G$ is the [[moduli space|moduli scheme]] of [[stable bundle|semistable]] $G$-[[principal bundles]] over the dual elliptic curve $A^\vee$ ([Ginzburg-Kapranov-Vasserot 95, (1.4.5)](#GinzburgKapranovVasserot95)). 

=--

+-- {: .num_remark #ModuliSpaceOfFlatConnections}
###### Remark

For geometry over the [[complex numbers]] and  $A = \mathbb{C}/\tau$ a 2-[[torus]], the scheme $A_G$ is the [[moduli space of flat connections]] on $A$, by the discussion at _[moduli space of connections -- flat connections over a torus](moduli+space+of+connections#FlatConnectionsOverATorus)_.

=--


Wtite $L Top_G$ for the collection of [[G-CW complexes]].
Write $Orb(G)$ for the [[orbit category]] of $G$.

We have a [[equivalence of (∞,1)-categories]]

$$
  L Top_G
  \stackrel{\simeq}{\longrightarrow}
  PSh_\infty(Orb(G))
  \,.
$$

Let the [[global points]] of the [[elliptic curve]] $A$ over $Spec E$ be equipped with an _orientation_ in the sense of a non-degenerate [[∞-group]] homomorphism of the form

$$
  B U(1) \longrightarrow A(Spec E)
$$


+-- {: .num_prop}
###### Proposition

Induced form this (...) is an [[essential geometric morphism]]

$$
  PSh_\infty(Orb(G))
  \stackrel{\overset{(-)\otimes_G A}{\longrightarrow}}{\stackrel{\overset{}{\leftarrow}}{\underset{}{\longrightarrow}}}
  Sh_\infty(Aff_E)_{/A_G}
$$

to the [[slice (∞,1)-topos]] over $A_G$. 

=--

([Gepner 05, theorem 3](#Gepner05))

+-- {: .num_defn}
###### Definition

Let 

$$
  \mathcal{O}
  \;\colon\;
  Sh_\infty(Aff_E)
  \longrightarrow
  Aff_E 
  \simeq
  E Alg^{op}
$$ 

be the [[left adjoint]] to the [[(∞,1)-Yoneda embedding]] as discussed at _[[function algebras on ∞-stacks]]_.

=--

+-- {: .num_prop}
###### Proposition

The composite

$$
  L Top_G
  \hookrightarrow
  PSh_\infty(Orb(G))
   \stackrel{(-)\otimes_G A}{\longrightarrow}
  Sh_\infty(Aff_E)_{/A_G}
  \stackrel{\mathcal{O}}{\longrightarrow}
  E Alg^{op}
$$

takes a space with $G$-[[action]] to its $G$-equivariant elliptic cohomology spectrum.

=--

([Gepner 05, theorem 4](#Gepner05))


### 2-Equivariant elliptic cohomology

> under construction, tentative

In ([Lurie, section 5.1](#Lurie)) is a vague mentioning of a more general perspective, where one evaluates elliptic cohomology not just on [[action groupoids]] of a [[group]], such as $B G$ but also on [[homotopy quotients]] of [[2-groups]], such as notably the [[string 2-group]], and how that gives a more conceptual picture. 

The following are some remarks on how to possibly realize this and at the same time refine it to geometric cohomology ([[differential cohomology]]). Tentative. Handle with care.


So let $G$ be a simple, simply connected [[compact Lie group]].

Regard $\mathbf{B}G$ in [[Smooth?Grd|]] = $Sh_\infty(SmthMfd)$. Then by the discussion at [[Lie group cohomology]] we have

$$
  \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}\mathbb{C}^\times)
  \simeq
  H(B G, K(\mathbb{Z},4))
  \simeq
  \mathbb{Z}
  \,.
$$

The [[∞-group extension]] classified by $k \in \mathbb{Z} \in \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}\mathbb{C}^\times)$ is the [[string 2-group]] at level $k$

$$
  \array{
    \mathbf{B}\mathbb{C}^\times &\longrightarrow& \mathbf{B}String_k(G)
    \\
    && \downarrow
    \\
    && \mathbf{B}G &\stackrel{k\mathbf{c}}{\longrightarrow}& \mathbf{B}^3 \mathbb{C}^\times
  }
$$ 

This cocycle has a [[differential cohomology]]-refinement to the [[universal Chern-Simons 3-conenction]]

$$
  k \mathbf{L} \;\colon\; \mathbf{B}G_{conn} \longrightarrow \mathbf{B}^3 \mathbb{C}^\times_{conn}
$$

Now given a [[torus]] $E = T^2$, regarded, for the moment, as a [[smooth manifold]], we have the [[transgression]] of the definition cocycle

$$
  \exp\left(
    \tfrac{i}{\hbar}
    \int_{E} k \mathbf{L}
  \right)
  \;\colon\;
  [E, \mathbf{B}G_{conn}]
   \stackrel{[E, k \mathbf{c}]}{\longrightarrow}
  [E, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp\left(\tfrac{i}{\hbar} \int_{E}(-)\right)}{\longrightarrow}
  \mathbf{B}\mathbb{C}^\times_{conn}
$$ 

which now defines a [[circle-bundle with connection]] on the [[moduli stack of connections]] on $E$.  We can restrict to the [[moduli stack of flat connection]], the [[phase space]] of $G$-[[Chern-Simons theory]]. This is the [[Hitchin connection]].

Consider then a collection of tori $E$ parameterized trivially over some parameter space $B$. 

$$
  E \times B \to B
  \,.
$$

Then the above yields

$$
  [(\shape E) \times B, \mathbf{B}G]
   \stackrel{}{\longrightarrow}
  \mathbf{B}[B,\mathbb{C}]^\times
$$

hence yields a $[B,\mathbb{C}^\times]$-bundle over the [[moduli space]] of $B$-collections of flat connections on $E$.

Now we want to consider this for the case that $B$ is a space in [[spectral geometry]].

To that end, pass to the larger spring 



## Properties
 {#Properties}

### Relation to conformal blocks of the WZW model
 {#RelationToConformalBlocks}


For $G$ a compact, simple and simply connected Lie group,
consider the [[string 2-group]] [[∞-group extension]]

$$
  \array{
    \mathbf{B}^2 U(1) &\to& \mathbf{B}String
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

The corresponding [[higher moduli stacks]] of [[flat ∞-connections]] on an [[elliptic curve]] $T$ form the [[∞-group extension]]

$$
  \array{
    [\Pi(T),\mathbf{B}^2 U(1)] &\to& [\Pi(T),\mathbf{B}String]
    \\
    && \downarrow
    \\
    && [\Pi(T), \mathbf{B}G]
  }
  \,.
$$

Now passing to the [[0-truncation]] turns the bottom piece into the [[moduli space of flat connections]] on the torus, which is $A_G$, def. \ref{TheModuliSpace}, remark \ref{ModuliSpaceOfFlatConnections}.

By the discussion at [smooth higher holonomy](smooth+infinity-groupoid#StrucChernSimons) the 0-truncation of the top left piece is $U(1)$, so under 0-truncation we should get a $U(1)$-[[principal bundle]]

$$
  \array{
    U(1) &\longrightarrow& \tau_0 [\Pi(T),\mathbf{B}String]
    \\
    && \downarrow
    \\
    && A_G
  }
  \,.
$$

This state of affairs is hinted at in ([Lurie, section 5.1](#Lurie)).

More in detail, notice that the [[string 2-group]] extension is modulated by a map

$$
  \mathbf{c} \;\colon\; \mathbf{B}G_{conn} \longrightarrow \mathbf{B}^3 U(1)_{conn}
$$

and the above circle-bundle is modulated by the [[transgression]] of that 

$$
  \exp\left(
    \tfrac{i}{\hbar}
    \int_{T} \mathbf{c}
  \right)
  \;\colon\;
  [T, \mathbf{B}G_{conn}]
   \stackrel{[T,\mathbf{c}]}{\longrightarrow}
  [T, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp(\tfrac{i}{\hbar} (-) )}{\longrightarrow}
  \mathbf{B}U(1)_{conn}
  \,.
$$

(By the discussion at [[schreiber:differential cohomology in a cohesive topos|dcct]].)

By the general discussion at [[quantization of Chern-Simons theory]] and the [[holography|holograpic]] [[AdS3-CFT2 and CS-WZW correspondence|CS-WZW correspondence]], the space of [[sections]] of this line bundle is the space of [[conformal blocks]] of the [[Wess-Zumino-Witten model]] on $T$. 

(This statement also appears as ([Lurie, remark 5.2](#Lurie))). 


### Relation to loop group representations
 {#RelationToLoopGroupRepresentations}

When restricting the above general construction
to the [[Tate curve]], then the confromal blocks become
[[loop group representations]].

In terms of differential geometry [[schreiber:differential cohomology in a cohesive topos|dcct]] consider the map

$$
  G \longrightarrow [S^1, \mathbf{B}G_{conn}]
$$

which locally sends a group elemnent $g$ to the constant [[principal connection]] on the circle with $g$ as its [[holonomy]].

This induces an inclusion

$$
  [S^1, G]
    \hookrightarrow
  [S^1, [S^1, \mathbf{B}G_{conn}]]
    \simeq
  [T, \mathbf{B}G_{conn}]
$$ 

and pulling the above WZW circle bundle back along this inclusion
yields the bundle on the [[loop group]] which is the [[prequantum bundle]]
whose [[geometric quantization]] yields the [[loop group representations]]
of [[positive energy representations|positive energy]].

Algebraically, this corresponds to evaluating equivariant elliptic cohomology on the [[Tate curve]], this is ([Lurie, theorem 5.1](#Lurie)).

+-- {: .num_remark}
###### Remark

In the full [[derived algebraic geometry]] the space of sections of the line
bundle on the moduli space has the structure of a $K((q))$-[[∞-module]], hence of an actual [[spectrum]] ([Lurie, below remark 5.4](#Lurie)).

=--

(...)

## Related concepts

* [[equivariant elliptic genus]]

## References

### General

In

* [[Victor Ginzburg]], [[Mikhail Kapranov]], Eric Vasserot, _Elliptic Algebras and Equivariant Elliptic Cohomology_ ([arXiv:q-alg/9505012](http://arxiv.org/abs/q-alg/9505012))
 {#GinzburgKapranovVasserot95}

a set of axioms was proposed that an equivariant elliptic cohomology theory should satisfy. See also

* Ioanid Rosu, _Equivariant Elliptic Cohomology and Rigidity_, American Journal of Mathematics 123 (2001), 647-677 ([arXiv:math/9912089](http://arxiv.org/abs/math/9912089))

In 

* [[David Gepner]], _[[Homotopy topoi and equivariant elliptic cohomology]]_, PhD thesis, University of Illinois at Urbana-Champaign, 2005.
 {#Gepner05}

the proposal of [Ginzburg-Kapranov-Vasserot 95](#GinzburgKapranovVasserot95) was formalized in terms of [[geometric morphisms]] of [[(infinity,1)-toposes]].

See also

* [[Ioanid Rosu]], _Equivariant Elliptic Cohomology and Rigidity_, American Journal of Mathematics, Vol. 123, No. 4, Aug., 2001 ([JSTOR](http://www.jstor.org/stable/25099077))


* [[Jacob Lurie]], section 5.1 of _[[A Survey of Elliptic Cohomology]]_
 {#Lurie}


### Relation to loop group representations

That equivariant elliptic cohomology is related to [[representations]] of [[loop groups]] as [[equivariant K-theory]] is related to the [[representation theory]] of the underlying groups had long been conjectured. The idea appears in

* I. Grojnowski, _Delocalised equivariant elliptic cohomology_, in _Elliptic
cohomology_, volume 342 of London Math. Soc. Lecture Note
Ser., pages 114&#8211;121. Cambridge Univ. Press, Cambridge, 2007

took shape in 

* [[Matthew Ando]], _The sigma orientation for analytic circleequivariant
elliptic cohomology_ . Geom. Topol., 7:91&#8211;153,
2003

* [[Matthew Ando]], _Power operations in elliptic cohomology and representations of loop groups_ Transactions of the American
Mathematical Society 352, 2000, pp. 5619-5666.

and was then further refined in section 5.2 of ([Lurie](#Lurie)) and in ([Gepner 05](#Gepner05)).


More is in 

* [[Nora Ganter]], _The elliptic Weyl character formula_ ([arXiv:1206.0528](http://arxiv.org/abs/1206.0528))
 {#Ganter12}

### Relation to superstrings and the Witten genus

Relation to the [[Witten genus]] [[partition function]] of [[superstrings]] is discussed in

* [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:math/0008192](http://arxiv.org/abs/math/0008192))

[[!redirects equivariant elliptic cohomology theory]]
[[!redirects equivariant elliptic cohomology theories]]