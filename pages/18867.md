

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #KaehlerVectorSpace}
###### Definition
**([[Kähler vector space]])**

Let $V$ be a [[finite dimensional vector space|finite-dimensional]] [[real vector space]]. Then a _linear Kähler structure_ on $V$ is

1. a _[[linear complex structure]]_ on $V$, namely a [[linear map|linear]] [[endomorphism]]

   $$
     J \;\colon\; V \to V
   $$

   whose [[composition]] with itself is minus the [[identity morphism]]:

   $$
     J \circ J = - id_V
   $$

1. a skew-symmetric [[bilinear form]]

   $$
     \omega \in \wedge^2 V^\ast
   $$

such that

1. $\omega(J(-),J(-)) = \omega(-,-)$;

1. $g(-,-) \coloneqq \omega(-,J(-))$ is a [[Riemannian metric]], namely

   a non-degenerate positive-definite [[bilinear form]] on $V$ 

   (necessarily symmetric, due to the other properties: $g(w,v) = \omega(w,J(v)) = -\omega(J(v),w) = - \omega(J(J(v)), J(w)) = \omega(w,J(w)) = g(v,w)$).

=--

(e.g. [Boalch 09, p. 26-27](#Boalch09))

## Properties

### Relation to Hermitian spaces

Linear Kähler space structure may conveniently be encoded in terms of [[Hermitian space]] structure:

+-- {: .num_defn #HermitianForm}
###### Definition
**([[Hermitian form]] and [[Hermitian space]])**

Let $V$ be a [[real vector space]] equipped with a [[complex structure]] $J\colon V \to V$. Then a _[[Hermitian form]]_ on $V$ is 

* a complex-valued real-[[bilinear form]]

  $$
    h \;\colon\; V \otimes V \longrightarrow \mathbb{C}
  $$

such that this is _symmetric sesquilinear_, in that:

1. $h$ is complex-linear in the first argument;

1. $h(w,v) = \left(h(v,w) \right)^\ast$ for all $v,w \in V$ 

where $(-)^\ast$ denotes [[complex conjugation]].

A Hermitian form is _positive definite_ (often assumed by default) if for all $v \in V$

1. $h(v,v) \geq 0$

1. $h(v,v) = 0 \phantom{AA} \Leftrightarrow \phantom{AA} v = 0$.

A [[complex vector space]] $(V,J)$ equipped with a (positive definite) Hermitian form $h$ is called a (positive definite) _[[Hermitian space]]_.

=--

+-- {: .num_prop #BasicPropertiesOfHermitianForms}
###### Proposition
**(basic properties of [[Hermitian forms]])**

Let $((V,J),h)$ be a positive definite [[Hermitian space]] (def. \ref{HermitianForm}). Then 

1. the [[real part]] of the [[Hermitian form]] 

   $$
     g(-,-) \;\coloneqq\; Re(h(-,-))
   $$
  
   is a [[Riemannian metric]], hence a symmetric positive-definite real-[[bilinear form]] 

   $$
     g \;\colon\; V \otimes V \to \mathbb{R}
   $$

1. the [[imaginary part]] of the [[Hermitian form]]

   $$
     \omega(-,-) \;\coloneqq\; -Im(h(-,-))
   $$

   is a [[symplectic form]], hence a non-degenerate skew-symmetric real-[[bilinear form]]

   $$
     \omega \;\colon\; V \wedge V \to \mathbb{R}
     \,.
   $$

hence

$$
  h = g - i \omega
  \,.
$$

The two components are related by

$$
  \label{RelationBetweennOmegaAndgOnHermitianSpace}
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

Finally 

$$
  h(J(-),J(-)) = h(-,-)
$$

and so the  Riemannian metrics $g$ on $V$ appearing from (and fully determining) Hermitian forms $h$ via $h = g - i \omega$ are precisely those for which

$$  
  \label{HermitianMetric}
  g(J(-),J(-)) = g(-,-)
  \,.
$$

These are called the _[[Hermitian metrics]]_.

=--


+-- {: .proof}
###### Proof

The positive-definiteness of $g$ is immediate from that of $h$. The symmetry of $g$ follows from the symmetric sesquilinearity of $h$:

$$
  \begin{aligned}
    g(w,v)
    & \coloneqq
    Re(h(w,v))
    \\
    & =
    Re\left( h(v,w)^\ast\right)
    \\
    & =
    Re(h(v,w))
    \\
    & =
    g(v,w)
    \,.
  \end{aligned}
$$

That $h$ is invariant under $J$ follows from its sesquilinarity

$$
  \begin{aligned}
    h(J(v),J(w))
    &=
    i h(v,J(w))
    \\
    & =
    i (h(J(w),v))^\ast
    \\
    & =
    i (-i) (h(w,v))^\ast
    \\
    & =
    h(v,w)
  \end{aligned}
$$

and this immediately implies the corresponding invariance of $g$ and $\omega$.


Analogously it follows that $\omega$ is skew symmetric:

$$
  \begin{aligned}
    \omega(w,v)
    & \coloneqq
    -Im(h(w,v))
    \\
    & =
    -Im\left( h(v,w)^\ast\right)
    \\
    & =
    Im(h(v,w))
    \\
    & = - \omega(v,w)
    \,,
  \end{aligned}
$$

and the relation between the two components:

$$
  \begin{aligned}
    \omega(v,w)
    & =
    - Im(h(v,w))
    \\
    & =
    Re(i h(v,w))
    \\
    & =
    Re(h(J(v),w))
    \\
    & = 
    g(J(v),w)
  \end{aligned}    
$$

as well as

$$
  \begin{aligned}
    g(v,w)
    & =
    Re(h(v,w)
    \\
    & =
    Im(i h(v,w))
    \\
    & =
    Im(h(J(v),w))
    \\
    & =
    Im(h(J^2(v),J(w)))
    \\
    & = 
    - Im(h(v,J(w)))
    \\
    & = \omega(v,J(w))
    \,.
  \end{aligned}
$$


=--

As a corollary:

+-- {: .num_prop #RelationBetweenKaehlerVectorSpacesAndHermitianSpaces}
###### Proposition
**(relation between [[Kähler vector spaces]] and [[Hermitian spaces]])**

Given a [[real vector space]] $V$ with a [[linear complex structure]] $J$, then the following are equivalent:

1. $\omega \in \wedge^2 V^\ast$ is a [[linear Kähler structure]] (def. \ref{KaehlerVectorSpace});

1. $g \in V \otimes V \to  \mathbb{R}$ is a positive definite [[Hermitian metric]] (eq:HermitianMetric)

where $\omega$ and $g$ are related by (eq:RelationBetweennOmegaAndgOnHermitianSpace)

$$
  \omega(v,w)
  \;=\;
  g(J(v),w)
  \phantom{AAAAA}
  g(v,w)
  \;=\;
  \omega(v,J(v))
  \,.
$$

Hence Kähler vector spaces are equivalently the [[finite dimensional vector space|finite dimensional]] complex [[Hilbert spaces]].

=--

## Examples

The archetypical elementary example is the following:

+-- {: .num_example #StandardAlmostKaehlerVectorSpaces}
###### Example
**(standard [[Kähler vector space]])**

Let $V \coloneqq \mathbb{R}^2$ be the 2-dimensional [[real vector space]] equipped with the [[complex structure]] $J$ which is given by the canonical identification $\mathbb{R}^2 \simeq \mathbb{C}$, hence, in terms of the canonical [[linear basis]] $(e_i)$ of $\mathbb{R}^2$, this is

$$
  J = (J^i{}_j) 
  \coloneqq 
  \left( 
    \array{
      0 & -1
      \\
      1 & 0
    }
  \right)
  \,.
$$

Moreover let 

$$
  \omega = (\omega_{i j}) \coloneqq \left( \array{0 & 1 \\ -1 & 0} \right)
$$ 

and 

$$
  g = (g_{i j}) \coloneqq \left( \array{ 1 & 0 \\ 0 & 1}  \right)
  \,.
$$ 

Then $(V, J, \omega, g)$ is a [[Kähler vector space]] (def. \ref{KaehlerVectorSpace}). 

The corresponding [[Kähler manifold]] is $\mathbb{R}^2$ regarded as a [[smooth manifold]] in the standard way and equipped with the [[bilinear forms]] $J, \omega g$ extended as constant rank-2 [[tensors]] over this manifold.

If we write 

$$
  x,y \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for the standard [[coordinate functions]] on $\mathbb{R}^2$ with 

$$
  z \coloneqq x + i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

and

$$
 \overline{z} \coloneqq x - i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

for the corresponding complex coordinates, then this translates to 

$$
  \omega
  \in
  \Omega^2(\mathbb{R}^2)
$$ 

being the [[differential 2-form]] given by

$$
  \begin{aligned}
    \omega
    & =
    d x \wedge d y
    \\
    & =
    \tfrac{1}{2i} d z \wedge d \overline{z}
  \end{aligned}
$$

and with [[Riemannian metric]] [[tensor]] given by

$$
  g = d x \otimes d x + d y \otimes d y
  \,.
$$

The [[Hermitian form]] is given by

$$
  \begin{aligned}
    h 
    & = 
    g - i \omega
    \\
    & = 
    d z \otimes d \overline{z}
  \end{aligned}
$$

=--

+-- {: .proof}
###### Proof

This is elementary, but, for the record, here is one way to make it fully explicit (we use [[Einstein summation convention]] and "$\cdot$" denotes [[matrix multiplication]]):

$$
  \begin{aligned}
    \omega_{i j'} J^{j'}{}_j
    & =
    \left(
       \array{
         0 & 1
         \\
         -1 & 0
       }
    \right)
      \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \\
    & 
    =
    \left(
      \array{
        1 & 0
        \\
        0 & 1
      }
    \right)
    \\
    & =
    g_{i j}
  \end{aligned}
$$


and similarly

$$
  \begin{aligned}
    \omega(J(-),J(-))_{i j}
    & =
    \omega_{i' j'} J^{i'}{}_{i} J^{j'}{}_{j}
    \\
    & =
    (J^t \cdot \omega \cdot J)_{i j}
    \\
    & =
    \left(
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)
    \cdot
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)
      \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \right)_{i j}
    \\
    & =
    \left(
    \left(
      \array{
        -1 & 0
        \\
        0 & -1
      }
    \right)
    \cdot
    \left(
      \array{
        0 & -1
        \\
        1 & 0
      }
    \right)
    \right)_{i j}
    \\
    & = 
    \left(
      \array{
        0 & 1
        \\
        -1 & 0
      }
    \right)_{i j}
    \\
    & = 
    \omega_{i j}
  \end{aligned}
$$

=--

## Related concepts

* [[Kähler manifold]]

* [[Hilbert space]]

## References

Lecture notes include

* {#Boalch09} Philip Boalch, p. 26-27 of _Noncompact complex symplectic and hyperkähler manifolds_, 2009 ([pdf](https://www.math.u-psud.fr/~boalch/cours09/hk.pdf))


[[!redirects Kähler vector spaces]]

[[!redirects Kaehler vector space]]
[[!redirects Kaehler vector spaces]]

[[!redirects linear Kähler structure]]
[[!redirects linear Kähler structures]]

[[!redirects linear Kaehler structure]]
[[!redirects linear Kaehler structures]]

[[!redirects Kähler space]]
[[!redirects Kähler spaces]]

[[!redirects Kaehler space]]
[[!redirects Kaehler spaces]]



