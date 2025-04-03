
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

In [[representation theory]], the term _intertwiner_ is a synonym for _[[homomorphism]] of [[representations]]/[[actions]]/[[modules]]_, hence for [[equivariant map|equivariant]] [[linear maps]].

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

* [[equivariant map]]

* [[twisted intertwiner]]

* [[Møller operator]]

## References

All monographs on [[representation theory]] will discuss [[homomorphisms]] of representations, but may call them by other names (such as *[[equivariant maps]]*). Monographs that make explicit the term "intertwiner" include:

* [[Charles Curtis]], [[Irving Reiner]], (29.1) in: _Representation theory of finite groups and associative algebras_, AMS (1962) &lbrack;[ISBN:978-0-8218-4066-5](https://bookstore.ams.org/chel-356.h)&rbrack;

* Asim O. Barut, Ryszard Rączka, p. 141 of: *Theory of group representations and applications*, World Scientific (1986) &lbrack;[doi:10.1142/0352](https://doi.org/10.1142/0352), [ark:/13960/s2131r9mqpj](https://archive.org/details/theoryofgrouprep0000baru/page/n9/mode/2up), [pdf](https://github.com/carlosal1015/Books/blob/master/Physics/A.%20O%20Barut%20Theory%20of%20group%20representations%20and%20applications%20part%201.pdf)&rbrack;


* [[Alexandre Kirillov]] Rem. 4.2 in: *An Introduction to Lie Groups and Lie Algebras*, Cambridge University Press (2008) \[<a href="https://doi.org/10.1017/CBO9780511755156">doi:10.1017/CBO9780511755156</a>\]

* {#Hall15} [[Brian C. Hall]], Def. 4.3 in: *Lie Groups, Lie Algebras, and Representations*, Springer (2015) &lbrack;[doi:10.1007/978-3-319-13467-3](https://doi.org/10.1007/978-3-319-13467-3)&rbrack;



[[!redirects intertwiners]]

[[!redirects bimodule intertwiner]]
[[!redirects bimodule intertwiners]]
