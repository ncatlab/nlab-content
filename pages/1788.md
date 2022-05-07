
[[Chern- and Pontrjagin forms -- section]]

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
  \label{UnitInAlgebraOfEndomorphismValuedEvenDegreeDifferentialForms}
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
  \;\;
    \coloneqq
  \;\;
  det
  \left(
    I + t \frac{i F_\nabla}{2\pi}
  \right)
  \,.
$$

By the [[relation between determinant and trace]], this is equal to the [[exponential]] of the [[trace]] of the [[logarithm]] of $I + \frac{i F_\nabla}{2\pi}$, this being the [[exponential series]] in the trace of the [[Mercator series]] in $\frac{i F_\nabla}{2\pi}$:

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
        I + \frac{i F_\nabla}{2\pi}
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
        {k \in \mathbb{N}_+}
        {\sum}
        \tfrac{1}{k}
        \left(
          \frac{F_\nabla}{2\pi i}
        \right)^k
    \right)
    \\
    & 
    \;=\;
    \exp
    \left(
      \underset
        {k \in \mathbb{N}_+}
        {\sum}
        \tfrac{1}{k}
        \left(
          \frac
            { - (-i)^k }
            {(2\pi)^k}
          tr\big( F_\nabla^{\wedge_k} \big)
        \right)
    \right)
    \\
    & 
    \;=\;
    1 
    \\
    & \phantom{\;=\;}
    +
    \phantom{\frac{1}{1}} 
    \left(
      i
      \tfrac{ tr\big(F_\nabla\big) }{2 \pi} 
      +
      \tfrac{1}{2}
      \tfrac{ tr\big( (F_\nabla)^{2} \big)}{(2 \pi)^2}  
      -i
      \tfrac{1}{3}
      \tfrac{ tr\big( (F_\nabla)^{3} \big)}{(2 \pi)^3}  
      -
      \tfrac{1}{4}
      \tfrac{ tr\big( (F_\nabla)^{4} \big)}{(2 \pi)^4}  
      + 
      \cdots
    \right)
    \\
    & \phantom{\;=\;}  
    + 
    \frac{1}{2}
    \left(
      i
      \tfrac{ tr\big(F_\nabla\big) }{2 \pi} 
      +
      \tfrac{1}{2}
      \tfrac{ tr\big( (F_\nabla)^{2} \big)}{(2 \pi)^2}  
      -i
      \tfrac{1}{3}
      \tfrac{ tr\big( (F_\nabla)^{3} \big)}{(2 \pi)^3}  
      -
      \tfrac{1}{4}
      \tfrac{ tr\big( (F_\nabla)^{4} \big)}{(2 \pi)^4}  
      + 
      \cdots
    \right)^2
    \\
    & \phantom{\;=\;}  
    +
    \frac{1}{6}
    \left(
      i
      \tfrac{ tr\big(F_\nabla\big) }{2 \pi} 
      +
      \tfrac{1}{2}
      \tfrac{ tr\big( (F_\nabla)^{2} \big)}{(2 \pi)^2}  
      -i
      \tfrac{1}{3}
      \tfrac{ tr\big( (F_\nabla)^{3} \big)}{(2 \pi)^3}  
      -
      \tfrac{1}{4}
      \tfrac{ tr\big( (F_\nabla)^{4} \big)}{(2 \pi)^4}  
      + 
      \cdots
    \right)^3
    \\
    & \phantom{\;=\;}  
    +
    \frac{1}{24}
    \left(
      i
      \tfrac{ tr\big(F_\nabla\big) }{2 \pi} 
      +
      \tfrac{1}{2}
      \tfrac{ tr\big( (F_\nabla)^{2} \big)}{(2 \pi)^2}  
      -i
      \tfrac{1}{3}
      \tfrac{ tr\big( (F_\nabla)^{3} \big)}{(2 \pi)^3}  
      -
      \tfrac{1}{4}
      \tfrac{ tr\big( (F_\nabla)^{4} \big)}{(2 \pi)^4}  
      + 
      \cdots
    \right)^4
    \\
    & \phantom{\;=\;}  
    +
    \cdots
    \\
    & \;=\;
    1 
    \\
    & \phantom{\;=\;}
    +
    i
    \frac
      { tr\big(F_\nabla\big) }
      { 2 \pi }    
    \\
    & \phantom{\;=\;}
    +
    \tfrac{1}{2}
    \frac
      { tr\big( (F_\nabla)^2 \big) }
      { (2 \pi)^2 }
    +
    \frac{1}{2}
    \left(
      i
      \frac
        { tr\big( F_\nabla \big) }
        { 2\pi }
    \right)^2
    \\
    & \phantom{\;=\;}
    -
    i
    \tfrac{1}{3}
    \frac
      { tr\big( (F_\nabla)^3 \big) }
      { (2 \pi)^3 }    
    +
    \frac{1}{2}
    \left(
      2
      \left(
        i
        \frac
          { tr\big( F_\nabla \big) }
          { 2 \pi }    
      \right)
      \left(
        \tfrac{1}{2}
        \frac
          { tr\big( (F_\nabla)^2 \big) }
          { (2 \pi)^2 }    
      \right)
    \right)
    +
    \frac{1}{6}
    \left(
      \left(
        i
        \frac
          { tr\big(F_\nabla\big) }
          { 2\pi }
      \right)^3
    \right)
    \\
    & \phantom{\;=\;}
    - 
    \tfrac{1}{4}
    \frac
      {tr\big( (F_\nabla)^4 \big)}
      { (2 \pi)^4 }
    +
    \frac{1}{2}
    \left(
      i 
      \frac
        {tr\big( (F_\nabla)^2 \big)}
        { (2 \pi)^2 }
    \right)^2
    +
    \frac{1}{24}
    \left(
      i
      \frac
        {tr\big( F_\nabla \big)}
        { 2\pi }
    \right)^4
    \\
    & \;=\;
    1 
    \\
    & \phantom{\;=\;}
    +
    \underset{ c_1 }{
    \underbrace{
    i
    \frac
      { tr\big(F_\nabla\big) }
      { 2 \pi }    
    }}
    \\
    & \phantom{\;=\;}
    +
    \underset{ c_2 }{
    \underbrace{
    \frac
      {\tr\big( (F_\nabla)^2 \big) - \big( tr(F_\nabla) \big)^2  }
      { 8 \pi^2  }
    }}
    \\
    & \phantom{\;=\;}
    +
    \underset{ c_3 }{ 
    \underbrace{
    i
    \frac
      {   
        - 2
        \cdot
        tr\big( (F_\nabla)^3  \big)
        + 3
        \cdot
        tr(F_\nabla)
        \cdot
        tr\big( (F_\nabla)^2 \big)
        - 
        \big( tr(F_\nabla ) \big)^3
      }    
      {48 \pi^3}
    }}
    \\
    & \phantom{\;=\;}
    +
    \underset{ c_4 }{
    \underbrace{
    \frac
      {
        -6
        \cdot
        tr\big( (F_\nabla)^4 \big)
        - 12
        \cdot 
        tr\big(  (F_\nabla)^2 \big)^2
        +
        \big( tr(F_\nabla) \big)^4
      }
      {384 \pi^4}
    }}
    \\
    & \phantom{\;=\;}
    + \cdots
  \end{aligned}
$$

##### Pontrjagin forms

$$
  \begin{aligned}
    p(\nabla)
    &
    \;\coloneqq\;
    \underset{ k \in \mathbb{N} }{\sum}
    (-1)^k
    \underset{
      \mathclap{
        deg = 4k
      }
    }{
    \underbrace{
      p_{k}(\nabla)
    }
    }
    \\
    &
    \;\coloneqq\;
    c\big(  \nabla \otimes \mathbb{C} \big)
    \\
    &
    \;=\;
    c\big(  \nabla \oplus \overline{\nabla} \big)  
    \\
    & 
    \;=\;
    c\big(\nabla\big)\cdot c\big(\overline{\nabla} \big)  
    \\
    & 
    \;=\;
    \left( 
      \underset{k \in \mathbb{N}}{\sum} c_{k}(\nabla)
    \right)
    \left( 
      \underset{k \in \mathbb{N}}{\sum} (-1)^k c_k(\nabla)
    \right)
    \\
    & \;=\;
    1
    \\
    &
    \phantom{\;=\;}
    - 
    \big( c_1(\nabla) \big)^2
    +
    2 \cdot c_2(\nabla)
    \\
    &
    \phantom{\;=\;}
    +
    \big( c_2(\nabla) \big)^2
    - 
    2 \cdot c_1(\nabla) c_3(\nabla)
    +
    2 \cdot c_4(\nabla)
    \\
    & \phantom{\;=\;}
    + \cdots
    \\
    & \;=\;
    1
    \\
    &
    \phantom{\;=\;}
    -
    \left(
      i 
      \frac
        {tr(F_\nabla)}
        {2 \pi}
    \right)^2
    +
    2
    \frac
      {
        tr\big( (F_\nabla)^2  \big) 
        -
        \big( tr(F_\nabla) \big)^2 
      }
      {8 \pi^2}
    \\
    & 
    \phantom{\;=\;}
    +
    \left(
      \frac
        {
          tr\big( (F_\nabla)^2  \big) 
          -
          \big( tr(F_\nabla) \big)^2 
        }
        {8 \pi^2}
    \right)^2
    +
    2
    \frac
      {
        -6
        \cdot
        tr\big( (F_\nabla)^4 \big)
        - 12
        \cdot 
        tr\big(  (F_\nabla)^2 \big)^2
        +
        \big( tr(F_\nabla) \big)^4
      }
      {384 \pi^4}
    \\
    & 
    \phantom{\;=\;}
    \phantom{+}    
    - 
    2
    \left(
      i 
      \frac
        {tr(F_\nabla)}
        {2 \pi}
    \right)
    \left(
    i
    \frac
      {   
        - 2
        \cdot
        tr\big( (F_\nabla)^3  \big)
        + 3
        \cdot
        tr(F_\nabla)
        \cdot
        tr\big( (F_\nabla)^2 \big)
        - 
        \big( tr(F_\nabla ) \big)^3
      }    
      {48 \pi^3}
    \right)
    \\
    & \phantom{\;=\;}
    \cdots
    \\
    & \;=\;
    1
    \\
    &
    \phantom{\;=\;}
    +
    \underset{ p_1 }{
    \underbrace{
    \frac
      { tr\big( (F_\nabla)^2 \big) }
      {4 \pi^2}
    }}
    \\
    & 
    \phantom{\;=\;}
    \frac
      {-}
      {-}
  \end{aligned}  
$$



(...)

