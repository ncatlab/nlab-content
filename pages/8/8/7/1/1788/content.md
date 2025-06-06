

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****

#### Products
 {#Products}

\begin{proposition}\label{ProductOfGrothendieckToposes}
The [[Cartesian product]] of [[presheaf toposes]] $PSh(C_i)$ in $Topos$ is the presheaf topos on the [[product category]] of their sites:
\[
  \label{ToposProductOfPresheafToposes}
  PSh(C_1)
  \times_{Topos}
  PSh(C_2)
  \;\simeq\;
  PSh(C_1 \times_{Cat} C_2 )
  \,.
\]
More generally, for $J_i$ a [[Grothendieck topology]] on $C_i$, the product in $Topos$ of the sheaf topos is the sheaf topos over the product site $(C_1 \times C_2, J_1 \times J_2)$, where $J_1 \times J_2$ is the Grothendieck topology on the [[product category]] generated from products of [[covering sieves]] from $J_1$ and $J_2$:
$$
  Sh(C_1, J_1)
  \times_{Topos}
  PSh(C_2, J_2)
  \;\simeq\;
  PSh(C_1 \times C_2,\,  J_1 \times J_2 )
  \,.
$$
\end{proposition}

(cf. [Pitts 1985, proof of Thm. 2.3](#Pitts85), [Valero 2018 p 98-99](#Valero18))

\begin{proof}
Since every sheaf topos admits a [[site]] that has all [[finite limits]], we first consider the topos-product of preaheaf toposes (eq:ToposProductOfPresheafToposes) under the assumption that the sites $C_i$ have all finite limits. (We refer to these small categories $C_i$ as "sites" already, even though in the presheaf case they are as such equipped with the trivial [[Grothendieck topology]]).

To check the defining [[universal property]] of a [[Cartesian product]], we use that [[geometric morphisms]] 

$$
  f_\ast \,\colon\,
  \mathcal{X} 
    \leftrightarrow 
  \mathcal{Y}
  \,\colon\,
  f^\ast
$$

between [[sheaf toposes]] (generally between [[locally presentable categories]]) correspond bijectively to [[finite limit]]-[[preserved limit|preserving]] [[cocontinuous functors]] 

$$
  \mathcal{X} \overset{f^\ast}{\longleftarrow} \mathcal{Y}
$$

(by the [[adjoint functor theorem]] [for locally presentable categories](adjoint+functor+theorem#StatementForLocPresCategories)).

Then writing

$$
  p_i 
    \,\colon\,
  C_1 \times C_2 
  \longrightarrow
  C_i
$$

for the canonical [[projection]] functors out of the [[product category]] of the given sites, and writing


$$
  p^\ast_i
  \,\colon\,
  PSh(C_i) 
  \longrightarrow
  PSh( C_1 \times C_2 )
$$

for the corresponding pre-composition functor on presheaves (which presverves all (co)limits since (co)[[limits of presheaves are computed objectwise]]), it is sufficient to show that for  $\mathcal{X} \in Topos$ and

$$
  f^\ast_i
  \,\colon\,
  PSh(C_i) \longrightarrow \mathcal{X}
  \,,
  \;\;\;\;
  i \in \{1,2\}
$$

a [[pair]] of cocontinuous and finitely continuous functors, there is a unique such functor

$$
  (f^\ast_1, f^\ast_2) \,\colon\,
  PSh(C_1 \times C_2) \longrightarrow \mathcal{X}
$$

which makes the following [[commuting diagram|diagram commute]]:

\begin{tikzcd}
  & 
  \mathcal{X}  
  \\
  & 
  \mathrm{PSh}(C_1 \times C_2)
  \ar[
    u, 
    dashed,
    "{ (f^\ast_1, f^\ast_2) }"{description}
  ]
  \\
  \mathrm{PSh}(C_1)    
  \ar[
    uur,
    "{ f^\ast_1 }"
  ]
  \ar[
    ur,
    "{ p^\ast_1 }"{swap}
  ]
  &&
  \mathrm{PSh}(C_2)  
  \ar[
    uul,
    "{ f^\ast_2 }"{swap}
  ]
  \ar[
    ul,
    "{ p^\ast_2 }"
  ]
\end{tikzcd}

Now observing that for a [[representable presheaf]]

$$
  c_i \,\in\, C_i \xhookrightarrow{y} PSh(C_i) 
$$

(with the [[Yoneda embedding]] $y$ on the right)

we have

\[
  \label{PullbackOfRepresentablesAlongProductProjection}
  p^\ast_1\big( y(c_1) \big)
    \,\simeq\, 
  y(c_1, \ast_2)
  \;\;\;\;
  \text{and}
  \;\;\;\;
  p^\ast_2\big( y(c_2) \big)
    \,\simeq\, 
  y(\ast_1,  c_2)
\]

(for "$\ast_i$" denoting the [[terminal object]] of $C_i$), 
it follows that to be product-preserving the dashed map must send representable 

$$
  (c_1, c_2) \,\in\, C_1 \times C_2 
  \xhookrightarrow{y} PSh(C_1 \times C_2)
$$

to

$$
  \begin{array}{rcl}
    (f^\ast_1, f^\ast_2)
    \big( 
      y(c_1, c_2)
    \big)
    &\simeq&
    (f^\ast_1, f^\ast_2)
    \big( 
      y\big( 
        (c_1, \ast_2) 
        \times 
        (\ast_1, c_2)
    \big)
    \\
    &\simeq&
    (f^\ast_1, f^\ast_2)
    \big( 
      y(c_1, \ast_2) 
        \times 
      y(\ast_1, c_2))
    \big)
    \\
    &\simeq&
    (f^\ast_1, f^\ast_2)
    \big( 
      y(c_1, \ast_2) 
    \big)
    \times
    (f^\ast_1, f^\ast_2)
    \big( 
      y(\ast_1, c_2) 
    \big)
    \\
    &\simeq&
    (f^\ast_1, f^\ast_2)
    \circ
    p^\ast_1 
    \big(
       y(c_1) 
    \big)
    \;\times\;
    (f^\ast_1, f^\ast_2)
    \circ
    p^\ast_2
    \big( 
      y(c_2) 
    \big)
    \\
    &\simeq&
    f^\ast_1\big(y(c_1)\big)
    \times
    f^\ast_2\big(y(c_2)\big)
    \,,
  \end{array}
$$

where we used, in order of appearance, that:

1. limits in a product category are computed via the limits in the factor categories,

1. the [Yoneda embedding preserves limits](Yoneda+embedding#PreservesLimits),

1. $(f^\ast_1, f^\ast_2)$ is assumed to preserve finite limits,

1. the equivalence (eq:PullbackOfRepresentablesAlongProductProjection) holds,

1. the above triangles commute.

So this fixes the values of $(f^\ast_1, f^\ast_2)$ on all representables. But thereby it actually fixes its values on all of $PSh(C_1 \times C_2)$, since the latter is the [[free cocompletion]] of $C_1 \times C_2$ (all [presheaves are colimits of representables](presheaf#PresheavesAreColimitsOfRepresentables)) and $(f^\ast_1, f^\ast^2)$ is also required to be cocontinuous and hence must [[preserved colimit|preserve]] these colimits. 

This establishes the claim 

$$
  PSh(C_1) \times_{Topos} PSh(C_2)
  \,\simeq\,
  PSh(C_1 \times C_2)
$$

for the case that the $C_i$ have all finite limits. To conclude it is now sufficient to observe that this construction descends to sheaf toposes as claimed

(...)
\end{proof}


\linebreak

## History

More recently, the S-matrix perspective becomes fashionable also in [[Yang-Mills theory]], with people noticing that [[super Yang-Mills theory]] and [[Tr(ϕ³)]] enjoy good structures in its scattering amplitudes which are essentially invisible in the vast summation of [[Feynman diagrams]] that extract the S-matrix from the [[action functional]]. Instead there are entirely different mathematical structures that encode at least some sub-class of scattering amplitudes (see at _[[amplituhedron]]_ and _[[associahedron]]_). This has lead to increasingly close ties between the S-matrix program and the mathematical fields of [[geometry]] and [[combinatorics]], allowing for the development of various other structures in [[quantum field theory]] that encode, for instance, the [[Wheeler superspace|Wheeler]]-[[wavefunction]] of the [[observable universe|universe]] (see at _[[cosmohedron]]_) and the [[ultraviolet divergence|UV]]/[[infrared divergence|IR]] [[divergent series|divergence]] of [[Feynman integrals]] (see at _[[Feynman polytope]]_). 

****


[[KummerSurfaceProjections.png:file]]
