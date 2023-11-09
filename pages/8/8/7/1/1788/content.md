

$$
  f \,\colon\, \mathscr{V} \to \mathscr{W}
  \,.
$$

$$
  f^\dagger {\vert w \rangle}
  \;\coloneqq\;
  a^{-1}\big( {\langle w \vert} f\big)
  \;=\;
  a^{-1} \circ f^\ast \circ a {\vert w \rangle}
$$

\begin{example}
  Let $\mathscr{V}$ be a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]] equipped with *both*

1. a non-degenerate [[sesquilinear form|sesquilinear]] ([[Hermitian form|Hermitian]]) [[inner product]] ${\langle - \vert - \rangle}$,

1. a non-degenerate symmetric [[bilinear form|bilinear]] [[inner product]] ${(-\vert-)}$

such that 

* the Hermitian-[[adjoint operator|adjoint]] ${(-\vert-)}^\dagger$ of the bilinear pairing is the [[coevaluation map]] that exhibits $\mathscr{V}$ as a [[self-dual object]],

then this induces a [[real structure]] on $\mathscr{V}$. 

Moreover, for $\mathscr{W}$ another [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]] equipped with a compatible pair of such structures, then the linear maps
$$
  \mathscr{V}
  \longrightarrow
  \mathscr{W}
$$
which preserve both structures also preserve that real structure, hence come from $\mathbb{R}$-[[linear maps]] of underlying [[real vector spaces]].
\end{example}
\begin{proof}
To start with, we note some generalities:

1. the non-degenerate sesquilinear form ${\langle -\vert -\rangle}$ is equivalently given by an [[antilinear map]]  
$a \colon \mathscr{V} \to \mathscr{V}^\ast$ to the [[dual linear space]], via 

   $$ 
     {\langle - \vert -\rangle} 
       \,=\, 
     a(-)(-) 
   $$

1. the non-degenerate bilinear form ${(- \vert -)}$ is equivalently given by a complex [[linear map]] $l \,\colon\, \mathscr{V} \to \mathscr{V}^\ast$, via

   $$
     {(- \vert -)} 
       \,=\, 
     l(-)(-)
   $$

(where the second argument means [[evaluation]]).

In [[bra-ket notation]] this is suggestively written as:

$$
  {( v \vert} \;\;\coloneqq\;\; l {\vert v )} 
  \,\;\;\;\;\;
  {\langle w \vert} \;\;\coloneqq\;\; a {\vert w \rangle} 
  \,.
$$

In particular, if $\big\{ {\vert w \rangle} \big\}_{w \in W}$ is any [[orthonormal basis]] of $\mathscr{V}$ with respect to $\langle - \vert - \rangle$, then the [[coevaluation map]] which exhibits $\mathscr{V}^\ast \,\coloneqq\, Map_{\mathbb{C}}(\mathscr{V}, \mathbb{C})$ as the [[linear dual space]] to $\mathscr{V}$ may be written as

\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}^\ast
  \\
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & \mathcal{V}
  \\[3pt]
  1 
   \ar[r, phantom, "{\mapsto}"]
  &
  \underset{w \in W}{\sum}
  \vert w \rangle \langle w \vert
\end{tikzcd}
and hence equivalently as
\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}
  \ar[r, "{ a }"]
  &
  \mathcal{V}^\ast
  \\
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & 
  \mathcal{V}^\ast
  \ar[r, "{ a^{-1} }"]
  &
  \mathcal{V}
  \mathrlap{\,,}
\end{tikzcd}  
which we use at the very end below.


Now regarding the concrete proof:

The composite

$$
  \tau
  \;\coloneqq\;
  a^{-1} \circ l
  \;\colon\;
  \mathscr{V} \to \mathscr{V}
  \,,
$$

is an [[antilinear map|antilinear]] [[endomorphism]] of $\mathscr{V}$, hence it will be sufficient to show that it is an [[involution]] (and hence the sought-after real structure). For that, in turn, it is clearly sufficient that

\[
  \label{InterchangeOfBiAndSesquilinearForms}
  a^{-1} \circ l
  \,=\,
  l^{-1} \circ a
  \,.
\]

because then

$$
  \tau \circ \tau
  \;=\;
  \big(
    a^{-1} \circ l
  \big)
  \circ
  \big(
    a^{-1} \circ l
  \big)
  \;=\;
    a^{-1} \circ l
  \circ
    l^{-1} \circ a
  \;=\;
  id_{\mathscr{V}}
  \,.
$$

We now show that this condition (eq:InterchangeOfBiAndSesquilinearForms) is equivalent to the assumption that $(-\vert-)^\dagger$ is the coevaluation map.

Namely, with 

\begin{tikzcd}[
  row sep=-1pt
]
  &[-5pt]
  \mathcal{V}
  \ar[r, equals]
  &
  \mathcal{V}
  \\
  (-\vert-)
  \;:\;
  &
  \otimes
  &
  \otimes
  \ar[r, "{ \mathrm{ev} }"]
  & 
  \mathbb{C}
  \\
  &
  \mathcal{V}
  \ar[
    r,
    "{ l }"{description}
  ]
  &
  \mathcal{V}^\ast
\end{tikzcd}

we have

\begin{tikzcd}[
  row sep=-1pt
]
  && \mathcal{V}^\ast
  \ar[rrr, "{ a^{-1} }"]
  &&& 
  \mathcal{V}
  \\
  & 
  \mathbb{C}
  \ar[
    r, 
    "{ \mathrm{coev} }"
  ]
  & 
  \otimes
  \\
  &
  &
  \mathcal{V}
  \ar[r, equals]
  &
  \mathcal{V}
  \\
  (-\vert-)^\dagger
  \;:\;
  &
  \otimes
  &
  \otimes
  &
  \otimes
  \ar[r, "{ \mathrm{ev} }"]
  & 
  \mathbb{C}
  \\
  &
  &
  \mathcal{V}
  \ar[
    r,
    "{ l }"{description}
  ]
  &
  \mathcal{V}^\ast
  \\
  &
  \mathbb{C}
  \ar[
    r,
    "{ \mathrm{coev} }"
  ]
  &
  \otimes
  \\
  &&
  \mathcal{V}^\ast
  \ar[rrr, "{ a^{-1} }"]
  &&& 
  \mathcal{V}
  \mathrlap{\,,}
\end{tikzcd}

which by the [[zig-zag identity]] for $ev$ & $coev$ equals

\begin{tikzcd}[
  row sep=-1pt
]
  & 
  &
  \mathcal{V}
  \ar[r, "{ l }"]
  &
  \mathcal{V}^\ast
  \ar[r, "{ a^{-1} }"]
  &
  \mathcal{V}
  \\
  (-\vert-)^\dagger
  \;:
  &
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  &&
  \otimes
  \\
  &&
  \mathcal{V}^\ast
  \ar[rr, "{ a^{-1} }"]
  &&
  \mathcal{V}
  \mathrlap{\,.}
\end{tikzcd}

On the other hand, the coevaluation which exhibits $(-\vert-)$ as a [[self-dual object|self-duality]] is clearly

\begin{tikzcd}[row sep=-1pt]
  & \mathcal{V}^\ast 
  \ar[r, "{ l^{-1} }"]
  & 
  \mathcal{V}
  \\
  \mathbb{C} 
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  &
  \mathcal{V} 
  \ar[r, equals]
  & 
  \mathcal{V}
\end{tikzcd}

which by the above discussion equals

\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}
  \ar[r, "{ a }"]
  &
  \mathcal{V}^\ast 
  \ar[r, "{ l^{-1} }"]
  & 
  \mathcal{V}
  \\
  \mathbb{C} 
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & 
  \mathcal{V}^\ast
  \ar[rr, "{ a^{-1} }"]
  &
  & 
  \mathcal{V}
\end{tikzcd}

This being equal to $(-\vert-)^\dagger$ above is clearly equivalent to (eq:InterchangeOfBiAndSesquilinearForms).
\end{proof}


[pdf](http://categorified.net/NYUADtalk.pdf)




$$
  \array{
    \phi^{-1}(c)
    &\longrightarrow&
    \phi/c
  }
$$


\begin{tikzcd}[sep=20pt]
  & 
  \phi^{-1}(c)
  \ar[rrrr, hook]
  & && &
  \phi/c
  \\
  x
  \ar[
    rr,
    "{ f }"
  ] 
  && 
  y
  &&
  x
  \ar[
    rr,
    "{ f }"
  ] 
  && 
  y
  \\[-15pt]
  \phi(x) 
    \ar[rr, equals] 
    \ar[dr, equals]
    && 
  \phi(y)
  \ar[dl, equals]
  &&
  \phi(x) 
    \ar[rr, "{ \phi(f) }"] 
    \ar[dr, "{ p_x }"{swap}]
    && 
  \phi(y)
  \ar[dl, "{ p_y }"]
  \\
  & c
  & &&
  & c
\end{tikzcd}

\begin{tikzcd}[
  sep=20pt
]
  &
  z
  \ar[
    drrr, 
    bend left=20, 
   "{ \forall \, g }"{description}
  ]
  \ar[
    dr, 
    dashed, 
    "{ 
       \exists! \, \widehat{w} 
    }"{description}
  ]
  \\
  \mathcal{E}
  \ar[dd, "{ P }"]
  &&
  x 
  \ar[
     rr, 
     "{ f }"{description},
     "{ \mathrm{cartesian} }"{swap, yshift=-1pt}
  ]  
  && 
  y
  \\
  & 
  P(z)
  \ar[drrr, bend left=20, "{ P(g) }"{description}]
  \ar[
    dr,
    "{ \forall \, w }"{description}
  ]
  \\
  \mathcal{B}
  &&
  P(x) 
  \ar[rr, "{ P(f) }"{description}]
  && 
  P(y)
\end{tikzcd}

On the normalized chain complex of Ex. \ref{NormalizedChainsOnEZTwo}, the 
[[group]] [[structure]] on $W \mathbb{Z}_2$ induces a [[simplicial ring]]-[[structure]], the "simplicial [[group ring]]") 
$$
  \mathbb{Z}\big[
    W \mathbb{Z}_2
  \big]
  \;\;
  \in
  \;\;
  Ring^{\Delta^{op}}
  \,.
$$

Since the [[normalized chain complex]]-functor $N_\bullet \,\colon\, Ab^{\Delta^{op}} \to Ch_{\geq 0}$ is (see [here](monoidal+Dold-Kan+correspondence#ChainsIsLaxMonoidal)) a [[lax monoidal functor]] via the [[Eilenberg-Zilber map]], this induces on $N_\bullet\big( \mathbb{Z}[W \mathbb{Z}_2] \big)$ the [[structure]] of a [[dg-algebra]].

To write this out, denote the two generators in each degree by
$$
  (0), (1)
  \;\in\;
  \mathbb{Z}_{0\cdots} 
  \oplus
  \mathbb{Z}_{1\cdots} 
  \;=\;
  N_n\big( \mathbb{Z}[W \mathbb{Z}_2] \big)
  \,.
$$
The non-degenerate cells of the tensor product simplicial group are similarly labeled (via [this Prop.](product+of+simplices#NonDegenerateSimplicesInProductOfSimplices)) by 

1. a pair of first elements of $n+1$-sequences in $\{0,1\}$ 

1. an $(p, q)$-[[shuffle]], 

hence:
$$
  \big(
    (g, g'), sh
  \big)
  \;\in\;
  \mathbb{Z}
  \big[
    \{0,1\}^2 
      \times 
    \sqcup_{p+q = n}  
    Sh(p,q)
  \big]
  \;\simeq\;
  N_{n}
  \Big(
    \mathbb{Z}\big[
      W \mathbb{Z}_2
      \times
      W \mathbb{Z}_2
    \big]
  \Big)
  \;\simeq\;
  N_{n}
  \Big(
    \mathbb{Z}\big[
      W \mathbb{Z}_2
    \big]
    \otimes
    \mathbb{Z}\big[
      W \mathbb{Z}_2
    \big]
  \Big)
  \,.
$$
One immediately finds that on these generators the induced product map is just the group operation, independent of the shuffle:
$$
  \array{
    N_\bullet
    \big(
      \mathbb{Z}[W \mathbb{Z}_2]
      \otimes
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    &
    \xrightarrow{
      N_\bullet
      \big( 
        \mathbb{Z}[(\text{-})\cdot(\text{-})] 
      \big)
    }
    &
    N_\bullet
    \big(
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    \\
    \big(
      g, g', sh
    \big)
    &\mapsto&
    (g \cdot g')
    \mathrlap{\,.}
  }
$$
Composed with the [[Eilenberg-Zilber map]] this gives
$$
  \array{
    \big(
      N_\bullet
      \,
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    \otimes
    \big(
      N_\bullet
      \,
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    &\xrightarrow{\phantom{----}}&
    N_\bullet
    \big(
      \mathbb{Z}[W \mathbb{Z}_2]
      \otimes
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    &
    \xrightarrow{
      N_\bullet
      \big( 
        \mathbb{Z}[(\text{-})\cdot(\text{-})] 
      \big)
    }
    &
    N_\bullet
    \big(
      \mathbb{Z}[W \mathbb{Z}_2]
    \big)
    \\
    (g)_p 
      \otimes 
    (g')_q
    &\mapsto&
    \displaystyle{
      \underset{
        \mathclap{ 
          sh \in Sh(p,q) 
        }
      }{\sum}
    }
    \;
    sgn(sh)
    \,
    \big(
      g,g', sh
    \big)
    &\mapsto&
    \Big(
      \displaystyle{
        \underset{
          \mathclap{
            sh \in Sh(p,q)
           }
        }{\sum}
      }
      \;
     sgn(sh)
   \Big)
   \,
   (g \cdot g')_{p + q}
   \mathrlap{\,.}
  }
$$


***

Let $X$ be a [[compact Hausdorff space]]. By a [[vector bundle]] (over $X$) we mean a [[topological vector bundle|topological]] [[complex vector bundle]].

Let $X$ be equipped with an [[involution]] $\sigma \,\colon\, X \to X$ (a [[homeomorphism]] such that $\sigma \circ \sigma = Id_X$ is the [[identity function]]).

\begin{definition}
\label{SigmaQuadraticFormOnComplexVectorBundle}
A *$\sigma$-[[quadratic form]]* on a topological complex vector bundle $\mathscr{V}$ over $X$ is:

* a morphism of complex topological bundles from the [[tensor product of vector bundles|tensor product]] of $\mathscr{V}$ with the [[pullback bundle|pullback]] of itself along $\sigma$ to the [[trivial bundle|trivial]] [[complex line bundle]]:

  $$
    g
    \,\colon\,
    \mathscr{V}
    \otimes
    \sigma^\ast \mathscr{V}
    \longrightarrow
    \underline{\mathbb{C}}
  $$

> (notice that [[fiber]]-wise this is a [[bilinear map]], *not* a [[sesquilinear map]])

such that:

1. $g$ is non-degenerate, in that its [[adjunct]] is an [[isomorphism]]

   $$
      \begin{array}{ccl}
       \mathscr{V} 
       &
       \overset{ \sim }{\longrightarrow}
       &
       \big(\sigma^\ast \mathscr{V}\big)^\ast
       \\
       v 
         &\mapsto& 
      \big(v' \mapsto g(v, v')
      \big)
     \end{array}
   $$

1. $g$ is $\sigma$-symmetric, in that

   $$
    \left.
     \begin{array}{l}
     v_1 
       \,\in\, 
     \mathscr{V}_x \,=\, (\sigma^\ast \mathscr{V})_{\sigma(x)}
     \\
     v_2 
       \,\in\, 
     (\sigma^\ast \mathscr{V})_{x} \,=\, \mathscr{V}_{\sigma(x)}
     \end{array}
     \right\}
     \;\;\;\;\;\;
     \vdash
     \;\;\;\;\;\;
     g_x(v_1, v_2)
     \;=\;
     g_{\sigma(x)}(v_2, v_1)
   $$

A [[homomorphism]] of such vector bundles with $\sigma$-quadratic form is a morphism of the underling topological complex vector bundles $f \,\colon\, \mathscr{V} \to \mathscr{V}$ over $X$, which is an [[isometry]] in that $g'\big(f(-),f(-)\big) = g(-,-)$.
\end{definition}

Write 
$$
  QVect_{\mathbb{C}}(X,\sigma)
$$ 
for the resulting [[category]].

The [[direct sum of vector bundles|direct sum of]] [[underlying]] vector bundles with $\sigma$-quadratic form (Def. \ref{SigmaQuadraticFormOnComplexVectorBundle}) inherits a $\sigma$-quadratic form in the evident summand-wise way. This operation makes the set of [[isomorphism classes]] into a [[commutative monoid]]:
\[
  \label{MonoidOfSigmaQuadraticComplexVectorBundles}
  \big(
    QVect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
    \oplus
  \big)
  \;\;\;
    \in
  \;\;\;
  CMnd.
\]

\begin{definition}\label{TopologicalHermitianKTheoryDueToCrabb}
  The [[group completion]] of the monoid (eq:MonoidOfSigmaQuadraticComplexVectorBundles) is the $\mathbb{Z}/2$-equivariant Hermtian K-theory of $(X, \sigma)$:
$$
  KH(X, \sigma)
  \;\;
  \coloneqq
  \;\;
  G
  \big(
    QVect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
    \oplus
  \big)
  \,.
$$
\end{definition}

\begin{example}
**([[hyperbolic functor]])**
For $\mathscr{V}$ an ordinary complex topological vector bundle over $X$, the [[direct sum of vector bundles|direct sum]] with the [[dual vector bundle|dual]] of its [[pullback bundle|pullback]] along $\sigma$
$$
  \mathscr{V}
  \,\mapsto\,
  \mathscr{V}
  \otimes
  (\sigma^\ast\mathscr{V})^\ast
$$
is canonically self-$\sigma$-dual
$$
  \array{
    \sigma^\ast
    \Big(
      \mathscr{V}
      \otimes
      (\sigma^\ast\mathscr{V})^\ast
    \Big)^\ast
    &\simeq&
      \mathscr{V}
      \otimes
      (\sigma^\ast\mathscr{V})^\ast
  }
$$
and carries a canonical $\sigma$-quadratic form (Def. \ref{SigmaQuadraticFormOnComplexVectorBundle}), given componentwise by the [[evaluation map]] $ev \,\colon\,\mathscr{V} \otimes \mathscr{V}^\ast \to \underline{\mathbb{C}}$.

This construction extends to an [[additive functor]] from the [[core groupoid]] of [[VectBund|$Vect_{\mathbb{C}}(X)$]] to $QVect_{\mathbb{C}}(X,\sigma)$, called the *[[hyperbolic functor]]*, and hence define a [[group homomorphism]] from the ordinary [[topological K-theory]]-group of $X$ to its topological Hermtian K-theory (eq:TopologicalHermitianKTheoryDueToCrabb):
$$
  K(X) \to KH(X,\sigma)
  \,.
$$
\end{example}

\begin{proposition}
  There is an isomorphism
$$
  KH(X,\sigma)
  \,\simeq\,
  KR(X,\sigma)
$$
between the $\mathbb{Z}/2$-equivariant topological Hermitian K-theory of Def. \ref{TopologicalHermitianKTheoryDueToCrabb} and the [[KR-theory]] of the [[real space]] $(X,\sigma)$.
\end{proposition}
\begin{proof}
To define a comparison map
$$
  KH(X,\sigma)
  \longrightarrow
  KR(X,\sigma)
$$  
given any representative $(\mathscr{V}, g)$, we may *choose* (see [here](inner+product+on+vector+bundles#ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)) a [[Hermitian form|Hermitian]] [[inner product of vector bundles]]
$$
  \langle \cdot \vert \cdot \rangle
  \;\colon\;
  \mathscr{V} \otimes \mathscr{V}
  \to 
  \underline{\mathbb{C}}
  \,.
$$

Now since both $g(-,-)$ and $\langle-\vert-\rangle$ are non-degenerate, with adjunct [[bijections]]
$$
  \tilde g 
    \,\colon\,
  \mathscr{V}
  \to 
  (\sigma^\ast\mathscr{V})^\ast
  \,,
  \;\;\;\;\;\;
  \tilde h 
    \,\colon\,
  \mathscr{V}
  \to 
  \mathscr{V}^\ast
  \,,
$$
we obtain an [[anti-linear map|anti-linear]] isomorphism
$$
  \tau
  \,\coloneqq\,
  \sigma^\ast(\tilde h)^{-1}
  \circ
  \tilde g
  \;\colon\;
  \mathscr{V} \to \sigma^\ast\mathscr{V}
$$
such that
$$
  g(-,-)
  \;=\;
  \langle
    \tau(-)
    ,
    -
  \rangle
  \,.
$$

Similarly
$$
  \langle
    v_1
    ,
    \tau(v_2)
  \rangle
  \;=\;
  \langle
    \tau(v_2)
    ,
    v_1
  \rangle^\ast
  \;=\;
  g(v_2, v_1)^\ast
  \;=\;
  g(v_1, v_2)^\ast
  \;=\;
  \langle \tau(v_1) \vert v_2 \rangle^\ast
$$
This means that
$$
  \tau_{\sigma(x)} \circ \tau_x
  \,\colon\,
  \mathscr{V}_x \to \mathscr{V}_x
$$
is a self-adjoint operator with respect to $\langle -, - \rangle$.

(...)

\end{proof}


$\lhd$
<!--% https://q.uiver.app/#q=WzAsOSxbMCwwLCJhIl0sWzEsMCwiYSJdLFsyLDAsImEiXSxbMCwxLCJhIl0sWzIsMSwiYSJdLFszLDEsImEiXSxbNCwxLCJhIl0sWzMsMF0sWzQsMF0sWzMsNCwidCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImJhcnJlZCJ9fX1dLFswLDEsInQiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJiYXJyZWQifX19XSxbMSwyLCJ0IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiYmFycmVkIn19fV0sWzAsMywiIiwxLHsibGV2ZWwiOjIsInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMiw0LCIiLDEseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDgsIiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs1LDYsInQiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJiYXJyZWQifX19XSxbMSw5LCJcXG11IiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFsxNCw1LCIiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9LCJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzE0LDYsIiIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMH0sInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTQsMTUsIlxcZXRhIiwyLHsibGFiZWxfcG9zaXRpb24iOjYwLCJzaG9ydGVuIjp7InNvdXJjZSI6NDAsInRhcmdldCI6MjB9fV1d-->
\begin{tikzcd}[row sep=scriptsize]
	a & a & a & {} & {} \\
	a && a & a & a
	\arrow[""{name=0, anchor=center, inner sep=0}, "t"', "\shortmid"{marking}, from=2-1, to=2-3]
	\arrow["t", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["t", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow[Rightarrow, no head, from=1-1, to=2-1]
	\arrow[Rightarrow, no head, from=1-3, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, draw=none, from=1-4, to=1-5]
	\arrow[""{name=2, anchor=center, inner sep=0}, "t"', "\shortmid"{marking}, from=2-4, to=2-5]
	\arrow["\mu"', shorten >=3pt, Rightarrow, from=1-2, to=0]
	\arrow[shorten <=4pt, Rightarrow, no head, from=1, to=2-4]
	\arrow[shorten <=4pt, Rightarrow, no head, from=1, to=2-5]
	\arrow["\eta"'{pos=0.6}, shorten <=9pt, shorten >=4pt, Rightarrow, from=1, to=2]
\end{tikzcd}

[[Kobal-HermitianKTheory.pdf:file]]

## Commuting diagrams

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
  \,.
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
  \,.
$$

Diagram test


\begin{center}
\begin{tikzcd}[column sep=small]
	V && U \\
	& X
	\arrow[hook, from=1-1, to=1-3]
	\arrow[from=1-1, to=2-2]
	\arrow[from=1-3, to=2-2]
\end{tikzcd}
\end{center}

## Definition

Given a [[topological space]] $X$, the **category of open subsets** $Op(X)$ of $X$ is the [[category]] whose

* [[object | objects]] are the [[open subset | open subsets]] $U \hookrightarrow X$ of $X$;

* [[morphism | morphisms]] are the inclusions 

## Properties

* The category $Op(X)$ is a [[poset]], in fact a [[frame]] (dually a [[locale]]): it is the [[frame of opens]] of $X$.

* The category $Op(X)$ is naturally equipped with the
structure of a [[site]], where a collection $\{U_i \to U\}_i$ of morphisms is a cover precisely if their [[union]] in $X$ equals $U$:
$$ \bigcup_i U_i = U .$$

  The [[category of sheaves]] on $Op(X)$ equipped with this site structure is typically referred to as the _[[category of sheaves on a topological space|category of sheaves on the topological space]]_ and denoted

  $$
    Sh(X) \;\coloneqq\; Sh(Op(X))
    \,.
  $$

* The category $Op(X)$ is also a [[suplattice]].


## Related concepts

* [[spatial locale]]

* [[spatial topos]]




