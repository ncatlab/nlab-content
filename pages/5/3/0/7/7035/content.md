
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[representation theory]], the term _intertwiner_ is a synonym for _[[homomorphism]] of [[representations]]/[[actions]]/[[modules]]_.

Notably for [[linear representations]] $\rho_1$, $\rho_2$ of some [[group]] or [[associative algebra]] $A$ on [[vector spaces]] (or more general [[modules]]) $V_1, V_2$, a [[linear map]] $u \colon V_1 \to V_2$ is said to _intertwine_ $\rho_1$ with $\rho_2$ if for all $a \in A$ we have that

$$
  u \circ \rho_1(a) 
    \;=\; 
  \rho_2(a)\circ u   
  \,,
$$

which equivalently means that this [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
  V_1 
    \ar[r, "{ u }"] 
    \ar[d, "{ \rho_1(a) }"{description}  ]
    &
  V_2
    \ar[d, "{ \rho_2(a) }"{description}  ]
  \\
  V_1 
    \ar[r, "{ u }"] 
    &
  V_2
\end{tikzcd}

With the [[representations]] understood as [[functors]] (cf. at *[[action]]*)

$$
  \rho_i \;\colon\; \mathbf{B}A \longrightarrow Mod
$$

from the [[delooping groupoid]] (for $A$ a [[group]]) or [[delooping]] $\mathscr{V}$-[[enriched category]] (for $A$ a [[monoid object]] in a [[symmetric monoidal category]] $\mathscr{V}$) to a suitable [[category of modules]],
these are (as $a$ ranges) just the [naturality squares](natural+transformation#ExplicitDefinition) exhibiting equivalently an ([[enriched natural transformation|enriched]]) [[natural transformation]] $u \,\colon\,\rho_1 \Rightarrow \rho_2$ between these functors:


\begin{tikzcd}
  \mathbf{B}A 
  \ar[
    r, bend left=25,
    "{ \rho_1 }"{description, pos=.4},
    "{\ }"{name=s, swap}
  ]
  \ar[
    r, bend right=25,
    "{ \rho_2 }"{description, pos=.4},
    "{\ }"{name=t}
  ]
  \ar[from=s, to=t, Rightarrow, "{ u }"]
  & 
  \mathrlap{ \mathrm{Mod} }
  \\[-20pt]
  \ast
  \ar[d, "{ a }"]
  \ar[r, phantom, "{ \mapsto }"]
  &
  V_1 
    \ar[r, "{ u }"] 
    \ar[d, "{ \rho_1(a) }"{description}  ]
    &
  V_2
    \ar[d, "{ \rho_2(a) }"{description}  ]
  \\
  \ast
  \ar[r, phantom, "{ \mapsto }"]
  &
  V_1 
    \ar[r, "{ u }"] 
    &
  V_2
\end{tikzcd}


## Related concepts

* [[twisted intertwiner]]

* [[Møller operator]]


[[!redirects intertwiners]]

[[!redirects bimodule intertwiner]]
[[!redirects bimodule intertwiners]]
