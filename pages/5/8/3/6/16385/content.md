
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

## Properties

### Genera properties

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

### Relation to Kähler spaces

+-- {: .num_prop #RelationBetweenKaehlerVectorSpacesAndHermitianSpaces}
###### Proposition
**(relation between [[Kähler vector spaces]] and [[Hermitian spaces]])**

Given a [[real vector space]] $V$ with a [[linear complex structure]] $J$, then the following are equivalent:

1. $\omega \in \wedge^2 V^\ast$ is a [[linear Kähler structure]] (def. \ref{KaehlerVectorSpace});

1. $g \in V \otimes V \to  \mathbb{R}$ is a [[Hermitian metric]] (eq:HermitianMetric)

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

=--


## Related concepts

* [[bilinear form]], [[quadratic form]], [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]]


* [[hermitian matrix]]

* [[Hermitian manifold]]

* [[quadratic form]]

## References

* [[C. T. C. Wall]], _On the axiomatic foundations of the theory of Hermitian forms_, Proc. Camb. Phil. Soc. (1970), 67, 243

* Wikipedia, _[Hermitian form](https://en.wikipedia.org/wiki/Sesquilinear_form#Hermitian_form)_

[[!redirects Hermitian forms]]

[[!redirects hermitian form]]
[[!redirects hermitian forms]]

[[!redirects Hermitian space]]
[[!redirects Hermitian spaces]]

[[!redirects hermitian space]]
[[!redirects hermitian spaces]]

[[!redirects Hermitian metric]]
[[!redirects Hermitian metrics]]

[[!redirects hermitian metric]]
[[!redirects hermitian metrics]]

