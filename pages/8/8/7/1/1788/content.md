
### Characteristic forms: Chern-, Pontrjagin-, and Euler-forms

Let $X$ be a [[smooth manifold]].

Write 

\[
  \label{RingOfEvenDegreeDifferentialForms}
  \Omega^{2\bullet}(X)
  \;\;
  \in
  \;
  CRings
\]

for the [[commutative ring]] of [[even number|even]]-degree [[differential forms]] on $X$, under the [[wedge product]] of differential forms. This is naturally a [[graded commutative algebra]], graded by form degree, but since we consider only forms in even degree it is actually a plain [[commutative ring]], too, after forgetting the grading.

Let $\mathfrak{g}$ be a [[semisimple Lie algbera]] (such as [[special unitary Lie algebra|$\mathfrak{su}(d)$]] or [[special orthogonal Lie algebra|$\mathfrak{so}(d)$]]) with [[Lie algebra representation]] $V \,\in\, Rep_{\mathbb{C}}(\mathfrak{g})$ over the [[complex numbers]] of [[finite number|finite]] [[dimension of a vector space|dimension]] $dim_{\mathbb{C}}(V) \,=\, n \,\in\, \mathbb{N}$ (for instance the [[adjoint representation]] or the [[fundamental representation]]), hence a [[homomorphism]] of [[Lie algebras]]

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

The multiplicative [[unit]] $I$ in this ring is the [[smooth function]] ([[differential 0-forms]]) which is [[constant function|constant]] on the $n \times n$ [[identity matrix]]. 

For

$$
  R 
    \,\in\, 
  \Omega^2(X) \otimes_{\mathbb{R}} End_{\mathbb{C}}(V)
  \xhookrightarrow{\;\;\;}
  \Omega^{2\bullet}(X) \otimes_{\mathbb{R}} End_{\mathbb{C}}(V)
  \;\simeq\;
  Mat_{n \times n}
  \Big(
    \mathbb{C} \otimes_{\mathbb{R}} \Omega^{2}(X)
  \Big)
$$

a [[curvature form]]



