
### Characteristic forms: Chern-, Pontrjagin-, and Euler-forms

#### Preliminaries

Let $X$ be a [[smooth manifold]].

Write 

\[
  \label{RingOfEvenDegreeDifferentialForms}
  \Omega^{2\bullet}(X)
  \;\;
  \in
  \;
  CAlg_{\mathbb{R}}
\]

for the [[commutative algebra]] over the [[real numbers]] of [[even number|even]]-degree [[differential forms]] on $X$, under the [[wedge product]] of differential forms. This is naturally a [[graded commutative algebra]], graded by form degree, but since we consider only forms in even degree it is actually a plain [[commutative ring]], too, after forgetting the grading.

Let $\mathfrak{g}$ be a [[semisimple Lie algebra]] (such as [[special unitary Lie algebra|$\mathfrak{su}(d)$]] or [[special orthogonal Lie algebra|$\mathfrak{so}(d)$]]) with [[Lie algebra representation]] $V \,\in\, Rep_{\mathbb{C}}(\mathfrak{g})$ over the [[complex numbers]] of [[finite number|finite]] [[dimension of a vector space|dimension]] $dim_{\mathbb{C}}(V) \,=\, n \,\in\, \mathbb{N}$ (for instance the [[adjoint representation]] or the [[fundamental representation]]), hence a [[homomorphism]] of [[Lie algebras]]

$$
  \mathfrak{g}
  \xrightarrow{\;\;\;}
  End_{\mathbb{C}}(V)
$$

to the [[linear map|linear]] [[endomorphism ring]] $End_{\mathbb{C}}(V)$, regarded here through its [[commutator]] as the [[endomorphism Lie algebra]] of $V$.

When regarded as an [[associative ring]] this is [[isomorphism|isomorphic]] to the [[matrix algebra]] of $n \times n$ [[square matrices]]

\[
  \label{LinearEndomorphismRing}
  End_{\mathbb{C}}(V)
  \;\;
  \simeq
  \;\;
  Mat_{n \times n}(\mathbb{C})
  \,.
\]

The [[tensor product of vector spaces|tensor product]] of the $\mathbb{C}$-[[associative algebra|algebras]] (eq:RingOfEvenDegreeDifferentialForms) and (eq:LinearEndomorphismRing)


is equivalently the $n \times n$ [[matrix algebra]] with [[coefficients]] in the [[complexification]] of even-degree differential forms:
$$
  \Omega^{2\bullet}
  \big(X\big)
  \otimes_{\mathbb{R}}
  End_{\mathbb{C}}(V)  
  \;\simeq\;
  \Omega^{2\bullet}(X)
  \otimes_{\mathbb{R}}
  \big(
    Mat_{n \times n}( \mathbb{R} )
  \big)
  \;\;
  \simeq
  \;\;
  Mat_{n \times n} 
  \big(
    \Omega^{2\bullet}(X) \otimes_{\mathbb{R}} \mathbb{C}
  \big)
  \,.
$$

The multiplicative [[unit]] 

\[
  \label{UnitInAlgebraOfMatrixValuedEvenDegreeDifferentialForms}
  I
  \;\in\;
  Mat_{n \times n} 
  \big(
    \Omega^{2\bullet}(X) \otimes_{\mathbb{R}} \mathbb{C}
  \big)
\]

in this algebra is the [[smooth function]] ([[differential 0-forms]]) which is [[constant function|constant]] on the $n \times n$ [[identity matrix]] and independent of $t$.

Any [[curvature form]] we regard as an element of this algebra

\[
  \label{CurvatureFormAsElementOfMatrixValuedEvenDegreeDifferentialForm}
  F_\nabla
    \,\in\, 
  \Omega^2(X) \otimes_{\mathbb{R}} End_{\mathbb{C}}(V)
  \xhookrightarrow{\;\;\;}
  \Omega^{2\bullet}(X) \otimes_{\mathbb{R}} End_{\mathbb{C}}(V)[t]
  \;\simeq\;
  Mat_{n \times n}
  \Big(
    \mathbb{C} \otimes_{\mathbb{R}} \Omega^{2}(X)
  \Big)
  \,.
\]


#### The formulas

##### Chern forms

The *[[total Chern form]]* $c(\nabla)$ is the [[determinant]] of the [[sum]] of the unit (eq:UnitInAlgebraOfEndomorphismValuedEvenDegreeDifferentialForms) with the curvature form (eq:CurvatureFormAsElementOfMatrixValuedEvenDegreeDifferentialForm) 
and the *$k$th [[Chern form]]* $c_k(\nabla)$, for $k \in \mathbb{N}$, is its component in degree $2k$:

$$
  c(\nabla)
  \;\;
    \coloneqq
  \;\;
  \sum_k
  \underset{
    \mathclap{
      deg = 2k
    }
  }{
  \underbrace{
    c_k(\nabla)
  }
  }
  \cdot t^k
  \;\;
    \coloneqq
  \;\;
  det
  \left(
    I + t \frac{i F_\nabla}{2\pi}
  \right)
  \,.
$$

By the [[relation between determinant and trace]], this is equal to the [[exponential]] of the [[trace]] of the [[logarithm]] of $I + \frac{i F_\nabla}{2\pi}$, the latter given by the [[Mercator series]] in $\frac{i F_\nabla}{2\pi}$:

$$
  \begin{aligned}
  c(\nabla)
  &
  \;=\;
  det
  \left(
    I + t \frac{i F_\nabla}{2\pi}
  \right)
  \\
  &
  \;=\;
  \exp
  \circ
    tr
    \circ
      ln
      \left(
        I + t \frac{i F_\nabla}{2\pi}
      \right)
  \\
  & 
  \;=\;
  \exp
  \circ
    tr
    \left(
      -
      \underset
        {k \in \mathbb{N}}
        {\sum}
        \tfrac{1}{k}
        \left(\frac{- i F_\nabla}{2\pi}\right) 
    \right)
    \\
    & 
    \;=\;
  \exp
    \left(
      -
      \underset
        {k \in \mathbb{N}}
        {\sum}
        \tfrac{1}{k}
        \left(\frac{- i}{2\pi}\right) 
        \cdot
        tr
        \left(
          F^{\wedge_n}_\nabla
        \right)
    \right)
  \end{aligned}
$$


(...)

