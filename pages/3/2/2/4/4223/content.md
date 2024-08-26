
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Poincaré Lemma** in [[differential geometry]] and [[complex analytic geometry]] asserts that "every [[differential form]] $\omega$ which is closed, $d_{dR}\omega = 0$, is _locally_ exact, $\omega|_U = d_{dR}\kappa$."

In more detail: if $X$ is [[contractible topological space|contractible]] then for every closed [[differential form]] $\omega \in \Omega^k_{cl}(X)$ with $k \geq 1$ there exists a differential form $\lambda \in \Omega^{k-1}(X)$ such that 

$$
  \omega 
  \,=\, 
  d_{dR} \lambda
  \,.
$$

Moreover, for $\omega$ a smooth family of closed forms, there is a smooth family of $\lambda$s satisfying this condition.


This statement has several more abstract incarnations. One is that it says that on a [[Cartesian space]] (or a complex [[polydisc]]) the [[de Rham cohomology]] (the [[holomorphic de Rham complex|holomorphic de Rham cohomology]]) vanishes in positive degree.

Still more abstractly this says that the canonical morphisms of [[sheaves of chain complexes]]

$$
  \mathbb{R} \to \Omega^\bullet_{dR}
$$

$$
  \mathbb{C} \to \Omega^\bullet_{hol}
$$

from the [[locally constant sheaf]] on the [[real numbers]] (the [[complex numbers]]) to the [[de Rham complex]] ([[holomorphic de Rham complex]]) is a [[stalk]]-wise [[quasi-isomorphism]] -- hence an [[equivalence]] in the [[derived category]] and hence induce an equivalence in [[hypercohomology|hyper]]-[[abelian sheaf cohomology]]. (The latter statement _fails_ in general in complex [[algebraic geometry]], see ([Illusie 12, 1.](#Illusie12)) and see also at _[[GAGA]]_.) (A variant of such [[resolutions]] of constant sheaves for the case over [[Klein geometries]] are [[BGG resolutions]].)

The Poincaré lemma is a special case of the more general statement that the pullbacks of differential forms along [[homotopy|homotopic]] [[smooth function]] are related by a [[chain homotopy]].


## Statement
 {#Statement}

### Over contractible domains

\begin{proposition}
\label{HomotopyToChainHomotopy}
Let 

* $f_0, f_1 \,\colon\, X \to Y$ be a [[pair]] of [[smooth functions]] between [[smooth manifolds]] 

* $\Psi \colon [0,1] \times X \to Y$ a [[smooth homotopy]] between them.

Then there is a [[chain homotopy]] between the induced operations of [[pullback of differential forms]]:

$$
  f_0^*, f_1^* 
  \;\colon\; 
  \Omega^\bullet(Y) \to \Omega^\bullet(X)
$$

on the [[de Rham complexes]] of $X$ and $Y$, an explicit formula for which is given by the following "[[homotopy operator]]":

$$
  \psi 
   \;\colon\;
  \omega \mapsto 
  \Big(
    x   
     \mapsto 
    \textstyle{\int}_{[0,1]} 
    \big(
      \iota_{\partial_t} \Psi^*\omega)(x)
    \big) 
    d t
  \Big) 
  \,. 
$$

In particular, $f_0^*$ and $f_1^*$ coincide on [[de Rham cohomology]]:

$$
  H_{dR}^\bullet(f_0^*) 
    \,\simeq\, 
  H_{dR}^\bullet(f_1^*)
  \,.
$$
\end{proposition}

Here $\iota_{\partial t}$ denotes [[tensor contraction|contraction]] (cf. *[[Cartan calculus]]*) with the canonical [[vector field]] tangent to $[0,1]$, and the [[integration]] is that of functions with values in the [[vector space]] of differential forms.

\begin{proof}
\label{ProofOfHomotopyToChainHomotopy}

We compute as follows:

$$
  \begin{array}{l}
    \mathrm{d}_{X} \psi(\omega)
    + 
    \psi( \mathrm{d}_Y \omega )
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{X} 
      \iota_{\partial_t} \Psi^*(\omega) 
    d t 
    + 
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} \Psi^*(\mathrm{d}_Y \omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{X} 
      \iota_{\partial_t} \Psi^*(\omega) 
    d t 
    + 
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} 
      \big(\mathrm{d}_X + \mathrm{d}_{[0,1]}\big)
      \Psi^*( \omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \iota_{\partial_t} 
      \mathrm{d}_{[0,1]}
      \Psi^*(\omega) 
    d t
    \\
    \;=\;
    \textstyle{\int}_{[0,1]} 
      \mathrm{d}_{[0,1]}
      \Psi^*(\omega) 
    \\
    \;=\;
    \Psi_1^\ast(\omega)
    -
    \Psi_0^\ast(\omega)
    \\
    \;=\;
    f_1^\ast \omega - f_0^\ast \omega
    \,,
  \end{array}
$$

where in the second step we used that [[exterior differential]] commutes with [[pullback of differential forms]] ([this Prop.](pullback+of+a+differential+form#CompatibilityWithDeRhamDifferential)), and in the last step the [[Stokes theorem]].
\end{proof}

The **Poincaré lemma** proper is the special case of this statement for the case that $f_2 = const_y$ is a function constant on a point $y \in Y$:

\begin{corollary}
If a [[smooth manifold]] $X$ admits a smooth contraction 

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{(id,0)}} & \searrow^{\mathrlap{id}}
    \\
    X \times [0,1] & \stackrel{\Psi}{\to} & X
    \\
    \uparrow^{\mathrlap{(id,1)}} & \nearrow_{\mathrlap{const_x}}
    \\
    X
  }
$$

then the [[de Rham cohomology]] of $X$ is concentrated on the 
ground field in degree 0. Moreover, for $\omega$ any closed 
form on $X$ in positive degree, an explicit formula for a form
$\lambda$ with $d \lambda = \omega$ is given by

$$
  \lambda 
  \,=\, 
  - \textstyle{\int}_{[0,1]} 
  \iota_{\partial_t}\Psi^*(\omega) 
  d t
  \,.
$$
\end{corollary}

+-- {: .proof}
###### Proof

This is the special case of Prop. \ref{HomotopyToChainHomotopy} where $f_0^\ast = id$ and $f_1^* = 0$ in positive degree.

=--

### Over $n$-connected domains
 {#OverNConnectedDomains}

More generally, the conclusion of the Poincaré lemma for differential forms of bounded degree $\leq n$ follows already on [[n-connected topological spaces|$n$-connected spaces]] (for instance by combining the [[Hurewicz theorem]] first with the [[universal coefficient theorem#UniversalCoefficientTheoremInRationalCohomology|universal coefficient theorem]] and then with the [[de Rham theorem]]).

Explicitly:

\begin{proposition}
\label{ForOneFormsOnSimplyConnectedDomain}
  On a [[simply-connected topological space|simply-connected]] (i.e.: 1-connected) [[smooth manifold]], a closed [[differential 1-form]] $\omega$ is exact, with potential function given at $x \in X$ by the [[integration of differential forms|integral]] of $\omega$ from any fixed base point along any smooth path to $x$.
\end{proposition}

This follows locally for instance by the fiberwise Stokes theorem ([here](Stokes+theorem#StokesTheoremForFiberIntegration)) and then globally due to the independence of the choice of path, by the assumption of simple-connectivity and the plain [[Stokes theorem]].

Textbook accounts which make this explicit include [do Carmo 1994, Prop. 3 (p. 24) in §3](#Carmo94). Exposition is also in [Armstrong 2017](https://unapologetic.wordpress.com/2011/12/17/simply-connected-spaces-and-cohomology/).


## Related concepts

* **Poincar&#233; lemma**

  * [[Kähler potential]]

* [[Stokes theorem]]

* [[de Rham theorem]]

* [[Hodge theorem]]

* [[variational sequence]]


## References

Textbook accounts:

* [[Dominic G. B. Edelen]], Lem 4-1.2 and §5-3 in: *Applied exterior calculus*, Wiley (1985) \[<a href="https://books.google.de/books/about/Applied_Exterior_Calculus.html?id=GUkViODKZ2oC">GoogleBooks</a>\]

* {#Carmo94} [[Manfredo P. do Carmo]], §4.3 of *Differential Forms and Applications*, Springer (1994) &lbrack;[doi:10.1007/978-3-642-57951-6](https://doi.org/10.1007/978-3-642-57951-6)&rbrack;



Course notes:

* [[Daniel Litt]], _The Poincar&#233; lemma and de Rham cohomology_, The Harvard College Math Review **1** 2 (2007) &lbrack;[[Litt-PoincareLemma.pdf:file]]&rbrack;
  > [Litt](https://www.daniellitt.com/expository-notes): An expository account of differential forms and the Poincaré Lemma using modern methods, aimed at beginning undergraduates. Contains some minor errors and omissions (in the exterior power section).

Discussion in [[complex analytic geometry]]:

* {#Illusie12} [[Luc Illusie]], _Around the Poincar&#233; lemma, after Beilinson_, talk notes 2012 ([pdf](https://www.imo.universite-paris-saclay.fr/~luc.illusie/derived-deRham3a1.pdf))

following

* {#Beilinson12} [[Alexander Beilinson]], _$p$-adic periods and de Rham cohomology_, J. of the AMS 25 (2012), 715-738

Generalization to [[supermanifolds]] (where the Lemma and its proof remain formally the same):

* [[Simone Noja]], Thm. 3.9 in: *On the Geometry of Forms on Supermanifolds*, Differential Geometry and its Applications, **88** (2023) 101999 &lbrack;[arXiv:2111.12841](https://arxiv.org/abs/2111.12841), [doi:10.1016/j.difgeo.2023.101999](https://doi.org/10.1016/j.difgeo.2023.101999)&rbrack;


Generalization to non-abelian [[Lie 2-algebra valued differential forms]] (local [[connections on 2-bundles]]):

* Getachew Alemu Demessie, [[Christian Saemann]], *Higher Poincaré Lemma and Integrability*, J. Math. Phys. **56** 082902 (2015) \[<a href="https://doi.org/10.1063/1.4929537">doi:10.1063/1.4929537</a>, [arXiv:1406.5342](https://arxiv.org/abs/1406.5342)\]

Generalization to [[covariant derivatives]]:

* Radosław Antoni Kycia, Josef Šilhan: *Inverting covariant exterior derivative* &lbrack;[arXiv:2210.03663](https://arxiv.org/abs/2210.03663)&rbrack;



[[!redirects Poincaré lemma]]
[[!redirects Poincare lemma]]

