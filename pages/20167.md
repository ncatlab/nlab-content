
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

### In ordinary homotopy theory

+-- {: .num_prop}
###### Proposition
**(Hopf degree theorem)**

Let $n \in \mathbb{N}$ be a [[natural number]] and $X \in Mfd$ be a [[connected topological space|connected]] [[orientation|orientable]] [[closed manifold]] of [[dimension]] $n$. Then the $n$th [[cohomotopy]] classes $\left[X \overset{c}{\to} S^n\right] \in \pi^n(X)$ of $X$ are in [[bijection]] to the [[degree of a continuous function|degree]] $deg(c) \in \mathbb{Z}$ of the representing functions, hence the canonical function

$$
  \pi^n(X) 
    \underoverset{\simeq}{S^n \to K(\mathbb{Z},n)}{\longrightarrow}
   H^n(X,\mathbb{Z}) 
     \;\simeq\;   
   \mathbb{Z}
$$

from $n$th [[cohomotopy]] to $n$th [[integral cohomology]] is a [[bijection]].

=--

(e.g. [Kosinski 93, IX (5.8)](#Kosinski93), [Kobin 16, 7.5](#Kobin16))


### In equivariant homotopy theory
 {#InEquivariantHomotopyTheory}

The following Prop. \ref{EquivariantHopfDegreeTheorem} is a generalization of the Hopf degree theorem to [[equivariant homotopy theory]], due to [tomDieck 79, 8.4](#tomDieck79).

We need the following list of ingredients and assumptions:

Let $G$ be a [[finite group]]. For $H \subset G$ a [[subgroup]], write 

\[
  \label{WeylGroup}
  W_G H \coloneqq (N_G H) / H 
\] 


for its [Weyl group](Weyl+group#in_equivariant_homotopy_theory).

For $X$ a [[G-space]], we write 

\[
  \label{IsotropySubgroups}
  Iso_X(G) \subset Sub(G)
\]

for the [[subset]] of the [[subgroup lattice]] on the [[isotropy groups]] of $X$, hence those [[subgroups]] which appear as [[stabilizer subgroups]] $Stab_G(x)$ of some point $x \in X$. This means that if $H_1, H_2 \in Iso_X(G)$ and $H_1 \lt H_2$ is a strict inclusion, then the [[fixed loci]] differ $X^{H_1} \gt X^{H_2}$.



Let 

1. $X$ be a [[G-CW complex]]

   such that for all [[stabilizer subgroups]] $H \in Iso_X(G)$

   1. the [[fixed point space]] $X^H$ is a $W_G H = (N_G H) / H $-complex, 

      we write $dim\big( X^H\big)$ for its [[dimension]];

   1. $dim(X^H) \geq 1$;

   1. $H^{dim(X^H)}\Big( X^H , \mathbb{Z}\Big) \simeq \mathbb{Z}$ ([[integral cohomology]] of the [[fixed point space]]),

      this implies that the [[action]] of $W_G(H)$ on cohomology induces a [[group homomorphism]]

      $$
        e_{H,X}
        \;\colon\;
        W_G(H) 
          \longrightarrow 
        Aut_{Ab}(\mathbb{Z}) 
          \simeq 
        \mathbb{Z}^\times
      $$

      to be called the _orientation behaviour_ of $H$ on $X$;

1. $Y$ be a [[G-space]]

   such that for all [[stabilizer subgroups]] $H \in Iso_X(G)$

   1. $Y^H$ is $dim(X^H)$-[[n-connected topological space|connected]];

   1. $\pi_{dim(X^H)}\big( Y^H\big) \simeq \mathbb{Z}$ ([[homotopy groups]] of [[fixed point space]]),

      with the previous point this implies (by the [[Hurewicz theorem]]) that  $H^{dim(X^H)}\Big( Y^H , \mathbb{Z}\Big) \simeq \mathbb{Z}$ and hence orientation behaviour $e_{H,Y} \;\colon\; W_G(H) \to \mathbb{Z}^\times$

   1. $e_{H,X} = e_{H,Y}$.

Choose generators in each $H^{dim(X^H)}\big(X^H, \mathbb{Z} \big) \simeq \mathbb{Z}$ ([[orientations]]) and $H^{dim(X^H)}\big(Y^G, \mathbb{Z} \big) \simeq \mathbb{Z}$ This implies that for each equivariant $f \colon X \to Y$ each $f^H \;\colon\; X^H \to Y^H$ has a well-defined [[degree of a continuous function|degree]] $deg(f^H) \in \mathbb{Z}$.

+-- {: .num_prop #EquivariantHopfDegreeTheorem}
###### Proposition
**([[equivariant Hopf degree theorem]])**

Under the above assumptions, the fixed-point-wise degree map

$$
  deg
  \;\colon\;
  \pi_0 \mathrm{Maps}\big( X,Y \big)^G
  \overset{
    \phantom{AAAA}
  }{\hookrightarrow}
  \mathbb{Z}^{ Iso_X(G) }
$$

(from $G$-[[equivariant homotopy theory|equivariant]] [[homotopy classes]] to [[tuples]] of degrees labeled by [[isotropy groups]]) is an [[injective function|injection]].

Moreover, for each $[f] \in \pi_0 \mathrm{Maps}\big( X,Y \big)^G$ and for each $H \in Isotropy_X(G)$ 

1. the $H$-degree modulo the [[order of a group|order]] of the [[Weyl group]]

   $$
     deg\left( f^H\right) \,mod\, {\vert W_G(H)\vert}
     \;\in\;
     \mathbb{Z}/{\vert W_G(H)\vert}
   $$

   is fixed by the degrees $deg\big( f^K\big)$ for all $K \gt H$;


1. there exists $f'$ with these specified degrees $deg\big( (f')^H\big) = deg\big( f^H\big)$ for $K \gt H$ and realizing any of the degrees $deg\big( (f')^H\big) \in \mathbb{Z}$ that satisfy the previous constraint.

=--

([tomDieck 79, 8.4](#tomDieck79))


> the following under construction


+-- {: .num_example #EquivariantHomotopyOfSVInRODegreeV}
###### Example
**(equivariant homotopy of $S^V$ in [[RO(G)-degree]] $V$)**


  Let $G \in \mathrm{Grp}_{\mathrm{fin}}$
  and $V \in \mathrm{RO}(G)$ with $V^G = 0$.
  Then the bipointed [[equivariant cohomotopy]] 
  of the [[representation sphere]] $S^V$ 
  in [[RO(G)-degree]] $V$ is
  the [[Cartesian product]] of one copy of the [[integers]] for
  each [[isotropy group|isotropy]] subgroup (eq:IsotropySubgroups) of $G$ in $S^V$
  except the full subgroup $G \subset G$

$$
  \array{
      \pi^V\left( S^V\right)^{\{0,\infty\}/}
      &
        \overset{\simeq}{\longrightarrow}
      &
      \underset{
        {
          {
              {H \in \mathrm{Isotr}_{S^V}(G)}
              \atop
              {H \neq G}
          }
        }
      }{\prod}
      \;\;
      {\vert W_G(H)\vert } \cdot \mathbb{Z}
      \\
      \big[
        S^V
          \overset{c}{\longrightarrow}
        S^V
      \big]
      &\mapsto&
      \Big(
        H 
          \mapsto
        \mathrm{deg}
        \big(
          c^H
        \big)
        -
        \mathrm{offs}(c,H)
      \Big)
  }
$$
  where on the right 
  $$
    \mathrm{deg}
    \Big(
      \big(
        S^V
      \big)^H
      \overset{
        c^H
      }{\longrightarrow}
      \big(
        S^V
      \big)^H
    \Big)
    \in \mathbb{Z}
  $$
  is the [[integer]] [[winding number]] of the underlying [[continuous function]]
  of $c$ ([[corestriction|co]])[[restriction|restricted]] to $H$-[[fixed points]], and part of the claim is  that this is an integer multiple of the order of the [[Weyl group]] $W_G(H)$ (eq:WeylGroup) up to an offset

$$
  \mathrm{offs}(f,H) 
  \;\in\; 
  \big\{
    0,1, \cdots,  \left\vert W_G(H)\right\vert
  \big\}
  \;\subset\;
  \mathbb{Z}
$$

which depends in a definite way on the degrees of $c^K$ for  all isotropy groups $K \gt H$.

=--

+-- {: .proof}
###### Proof

  This follows as a special case of the equivariant Hopf degree theorem 
  (Prop. \ref{EquivariantHopfDegreeTheorem}). 

  The list of assumptions there is satisfied because [[representation spheres]] are [[G-CW-complexes]], and because we are now mapping from the representation sphere to itself, $S^V \to S^V$, which makes all the assumptions on dimensions and orientation data be satisfied.

  This equivariant Hopf degree theorem
  is stated above under the simplifying assumption that the dimension
  of all fixed loci is positive. But the proof from [tomDieck 79, 8.4](#tomDieck79) immediately applies to our situation where the dimension of the fixed locus at the full subgroup $H = G$ is 0, with $\left( S^V\right)^G = S^0$. Then, our assumption of bipointedness uniquely fixes the choice of map $S^0 \overset{c^G}{\longrightarrow} S^0$ in the first step of the inductive argument in [tomDieck 79, 8.4](#tomDieck79), and from there on the proof applies verbatim.

=--

<br/>

## Related statements

* [[Hurewicz theorem]]

* [[Boardman homomorphism]]

* [[Hopf invariant]]

## References

Due to [[Heinz Hopf]].

Review:

* {#Kosinski93} [[Antoni Kosinski]], chapter IX of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))

* {#Kobin16} Andrew Kobin, _Algebraic Topology_, 2016 ([[KobinAT2016.pdf:file]])

Generalization to [[equivariant cohomotopy]] and [[equivariant cohomology]]

* {#tomDieck79} [[Tammo tom Dieck]], section 8.4 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766 Springer 1979


[[!redirects Hopf theorem]]

[[!redirects equivariant Hopf degree theorem]]

