
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
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

\begin{remark}
  A positive-definite and complete Hermitian vector space is called a *[[Hilbert space]]*.
\end{remark}


## Properties

### General properties

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


### As $(\mathbb{Z}/2 \curvearrowright \mathbb{C})$-modules
 {#AsEquivariantModules}

While a non-degenerate [[inner product]] $(-\vert-)$ on a [[finite-dimensional vector space|finite-dimensional]] [[real vector space]] $V$ is equivalently a [[linear isomorphism]] to its [[dual vector space]]

$$
  \array{
    V 
      &\overset{\sim}{\longrightarrow}& 
    V^\ast
      &\overset{\sim}{\longrightarrow}& 
    V
    \\
    v &\mapsto& (v\vert-) &\mapsto& v
  }
$$

the analogous statement for  Hermitian complex inner products $\langle - \vert - \rangle$ fails, since the corresponding maps

$$
  \array{
    \mathscr{H}
      &\overset{\sim}{\longrightarrow}& 
    \mathscr{H}
      &\overset{\sim}{\longrightarrow}& 
    \mathscr{H}
    \\
    \vert \psi \rangle 
    &\mapsto& 
    \langle \psi \vert
    &\mapsto& 
    \vert \psi \rangle    
  }
$$

are now complex *[[anti-linear map|anti-linear]]* and hence not [[morphisms]] in the [[category]] of [[complex vector spaces]].

What one does get is a complex-linear isomorphism to the [[anti-dual space]].

Another way to regard this situation is to observe that complex anti-linear involutions $\mathscr{H} \leftrightarrow \mathscr{H}^\ast$ on non-degenerate Hermitian spaces $\mathscr{H}$ are equivalently $(\mathbb{Z}/2 \curvearrowright \mathbb{C})$-[[module object|module]] structures on the [[direct sum]] $\mathscr{H} \oplus \mathscr{H}^\ast$, regarded in the [[topos]] of [[G-sets|$\mathbb{Z}/2$-sets]], for $(\mathbb{Z}/2 \curvearrowright \mathbb{C})$ the [[ring object]] given by the [[complex numbers]] equipped with their involution by [[complex conjugation]]:

<center>
<img src="/nlab/files/HermitianSpacesAsEquivariantModules-221018.jpg" width="640">
</center>


{#HermitianOperatorsAsZTwoActsCModules} Notice that these $(\mathbb{Z}/2 \curvearrowright \mathbb{C})$-modules arising from (non-degenerate, finite-dimensional) Hermitian vector spaces this way happen to carry also a [[complex structure]], hence a compatible module-structure by the actual [[complex numbers]] (i.e. equipped with the trivial [[involution]]), given by $\underline{\mathrm{i}}$. 

Using this, one may identify:

1. the space of [[linear operators]] on a Hermitian vector space as the [[equalizer]] of this imaginary rotation on the [[tensor product|tensor square]] of the $(\mathbb{Z}/2 \curvearrowright \mathbb{C})$-module with the [[braided monoidal category|braiding]] and the [[identity morphism|identity]],

1. among these that of [[hermitian operators]] as the further [[fixed locus]] of the involution action:

<center>
<img src="/nlab/files/HermitianOperatorsAsEquivariantModules-221019.jpg" width="710">
</center>

\linebreak


## Related concepts

* [[Hilbert space]]

* [[bilinear form]], [[quadratic form]], [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]]


* [[hermitian matrix]]

* [[Hermitian manifold]]

* [[quadratic form]]

## References

Among original articles:

* [[C. T. C. Wall]], _On the axiomatic foundations of the theory of Hermitian forms_, Proc. Camb. Phil. Soc. **67** (1970) 243-250 &lbrack;[doi:10.1017/S0305004100045515](https://doi.org/10.1017/S0305004100045515), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/wall9.pdf)&rbrack;

See also:

* Wikipedia, _[Hermitian form](https://en.wikipedia.org/wiki/Sesquilinear_form#Hermitian_form)_

and see the references at *[[Hilbert space]]*.

[[!redirects Hermitian forms]]

[[!redirects hermitian form]]
[[!redirects hermitian forms]]

[[!redirects Hermitian space]]
[[!redirects Hermitian spaces]]

[[!redirects hermitian space]]
[[!redirects hermitian spaces]]

[[!redirects Hermitian vector space]]
[[!redirects Hermitian vector spaces]]

[[!redirects hermitian vector space]]
[[!redirects hermitian vector spaces]]


[[!redirects Hermitian metric]]
[[!redirects Hermitian metrics]]

[[!redirects hermitian metric]]
[[!redirects hermitian metrics]]

[[!redirects Hermitian inner product]]
[[!redirects Hermitian inner products]]
[[!redirects hermitian inner product]]
[[!redirects hermitian inner products]]

[[!redirects Hermitian inner product space]]
[[!redirects Hermitian inner product spaces]]
[[!redirects hermitian inner product space]]
[[!redirects hermitian inner product spaces]]



