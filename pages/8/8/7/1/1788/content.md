

## Idea

In ([[higher gauge theory|higher]]) [[gauge theory]], the total (generalized) electric/magnetic [[fluxes]] through given [[surfaces]] (or higher [[submanifolds]]) should be [[observables]] and hence have [[Poisson brackets]] in the [[classical field theory]] To the extent that these induce non-trivial operator [[commutators]] in the corresponding [[quantum field theory]], this means that the corresponding kinds of fluxes would be subject to the [[Heisenberg uncertainty principle]].

A subtlety here is that the usual [[phase space]]-methods for [[Lagrangian field theories]] directly provide these brackets only for the [[differential forms]] which are the [[flux densities]]. These however, provide only a [[rational homotopy theory|rational]] image of the fluxes, which in general may furthermore have [[torsion subgroup|torsion]]-[[cohomology group|cohomology]]-components.

In plain [[electromagnetism]], the [[canonical momentum]] of the [[gauge potential]] $A$ is proportional (by constants to be ignored in the following) to the electric flux density $\star F$ ($F$ the [[Faraday tensor]] [[flux density]] and $\star$ the [[Hodge star operator]] on the given [[spacetime]] [[pseudo-Riemannian manifold]]), which however means that the the Poisson bracket of the magnetic flux density $F \equiv \mathrm{d}_{dR} A$ with the electric flux density is a total derivative (cf. eg. [Riello 2021, p. 2](#Riello21)), so that the bracket of the integrated fluxes $\Phi_E$ and $\Phi_B$ through given [[orientable manifold|orientable]] [[closed manifold|closed]] surfaces $S_E$ and $S_B$, respectively, actually vanishes (cf. [FMS07b (3.6)](#FreedMooreSegal07b)):

$$
  \big\{
    \Phi_E
    ,\,
    \Phi_B
  \big\}
  \;\equiv\;
  \Big\{
  \textstyle{\int}_{S_B} \star F 
  ,\,
  \textstyle{\int}_{S_E} F
  \Big\}
  \;=\;
  0
  \,.
$$

The thrust of [FMS07a](#FreedMooreSegal07a), [07b](#FreedMooreSegal07b) is the claim that this bracket becomes non-vanishing if torsion-components of the fluxes (through their enhancement to [[ordinary differential cohomology]]) are retained, but it seems that this is ultimately by definition ([FMS07a, Def. 1.29](#FreedMooreSegal07a); [FMS07b (3.28)](#FreedMooreSegal07b)) more than by derivation from first principles.

On the other hand, for [[non-abelian group|non-abelian]] [[gauge group]], a careful analysis of the (somewhat subtle) Poisson brackets reveals ([Cattaneo & Perez 2017](#CattaneoPerez17)) that the electric fluxes -- understood as flux densities integrated against [[Lie algebra]] valued functions $\alpha$ -- have a non-trivial bracket among *themselves*:

$$
 \big\{
   \Phi^\alpha_E
   ,\,
   \Phi^{\alpha'}_E
 \big\}
 \;\propto\;
 \Phi_E^{[\alpha, \alpha']}
$$

(where $[-,-]$ is the pointwise [[Lie bracket]]). This result has found a lot of attention (only) in the context of [[first-order formulations of gravity]].

## References

On the canonical phase space structure of [[gauge theory]]:

* {#Haagensen93} P. E. Haagensen, *On The Exact Implementation Of Gauss' Law In Yang-Mills Theory* &lbrack;[arXiv:hep-ph/9307319](https://arxiv.org/abs/hep-ph/9307319)&rbrack;


In [[electromagnetism]], with focus on torsion components that are argued to not generally commute:

* {#FreedMooreSegal07a} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *The Uncertainty of Fluxes*, Commun. Math. Phys. **271**  (2007) 247-274 &lbrack;[arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3)&rbrack;

* {#FreedMooreSegal07b} [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *Heisenberg Groups and Noncommutative Fluxes*,  Annals Phys. **322** (2007) 236-285 &lbrack;[arXiv:hep-th/0605200](http://arxiv.org/abs/hep-th/0605200), [doi:10.1016/j.aop.2006.07.014](https://doi.org/10.1016/j.aop.2006.07.014)&rbrack;


In [[SU(2)]]-[[gauge theory]] (highlighted for the case of the [[first-order formulation of gravity]] but applying verbatim also to [[Yang-Mills theory]]):

* {#CattaneoPerez17} [[Alberto S. Cattaneo]], Alejandro Perez, *A note on the Poisson bracket of 2d smeared fluxes*, Class. Quant. Grav. **34** (2017) 107001 &lbrack;[arXiv:1611.08394](https://arxiv.org/abs/1611.08394), [doi:10.1088/1361-6382/aa69b4](https://doi.org/10.1088/1361-6382/aa69b4)&rbrack;

  > (same argument applies to YM, eg. via [Haagensen 1993 (1) ](#Haagensen93))

* Mikhail A. Savrov, *Commutator of Electric Charge and Magnetic Flux* &lbrack;[arXiv:2003.02225](https://arxiv.org/abs/2003.02225)&rbrack;


* {#Riello21} Aldo Riello, p. 2 of: *Symplectic reduction of Yang-Mills theory with boundaries: from superselection sectors to edge modes, and back*, SciPost Phys. **10** 125 (2021) &lbrack;[doi:10.21468/SciPostPhys.10.6.125](https://scipost.org/SciPostPhys.10.6.125)&rbrack;



***

$\Sigma$ a [[connected topological space|connected]] [[closed manifold|closed]] [[surface]]


$$
  Maps\big(
    \Sigma, 
    \,
    B U(1)
  \big)
  \;\simeq\;
  \underset{ \mathbb{Z} }{
    \underbrace{
      H^2(\Sigma; \mathbb{Z})
    }
  }
  \times
  B H^1(\Sigma; \mathbb{Z})
$$

$$
  Maps\big(
    \Sigma, 
    \,
    B U(1)
    \times
    B U(1)
  \big)
  \;\simeq\;
  Maps\big(
    \Sigma, 
    \,
    B U(1)
  \big)
  \times
  Maps\big(
    \Sigma, 
    \,
    B U(1)
  \big)
  \;\simeq\;
  H^2(\Sigma;\mathbb{Z})
  \times
  H^2(\Sigma;\mathbb{Z})
  \times
  \underset{
    B\big(
      H^1(\Sigma; \mathbb{Z}) \times H^1(\Sigma; \mathbb{Z})
    \big)
  }{
    \underbrace{
      B H^1(\Sigma; \mathbb{Z})
      \times
      B H^1(\Sigma; \mathbb{Z})
    }
  }
$$

$$
  \Omega_{
    \Phi^\Sigma_E,
    \Phi^\Sigma_B
  }
  Maps\big(
    \Sigma, 
    \,
    B U(1)
    \times
    B U(1)
  \big)
  \;\simeq\;
  \Omega
  \Big(
    B 
    \big(
      H^1(\Sigma; \mathbb{Z})
      \times
      H^1(\Sigma; \mathbb{Z})
    \big)
  \Big)
  \simeq
  H^1(\Sigma; \mathbb{Z})
  \times
  H^1(\Sigma; \mathbb{Z})
$$

$$
  H_\bullet
  \Big(
  \Omega_{\Phi^\Sigma_E, \Phi^\Sigma_B}
   Maps\big(
    \Sigma, 
    \,
    B U(1)
    \times
    B U(1)
  \big)
  \Big)
  \;\simeq\;
  \mathbb{C}[
    H^1(\Sigma; \mathbb{Z})
    \times
    H^1(\Sigma; \mathbb{Z})
  ]
$$

(group algebra)


***

$$ T^k_{fc}(x) = \sum_{n = 0}^k \frac{f^{(n)}(c) (x-c)^n}{n!} .$$

\begin{tikzcd}[sep=20pt]
  A
  \ar[
    rr,
    "{ (P,f) }",
    "{\ }"{name=s, pos=.9, swap}
  ]
  \ar[  
    dd, "{ h }"{swap}
  ]
  &&
  B
  \ar[
    dd, "{ l }"
  ]
  &&
  A \odot P
  \ar[
    rr,
    "{ f }"
  ]
  \ar[
    dd,
    "{ h \odot r }"{swap}
  ]
  &&
  B
  \ar[  
    dd,
    "{ k }"
  ]
  \\
  &&&
  :=
  \\
  A' 
  \ar[
    rr,
    "{ (P', f') }"{swap},
    "{\ }"{name=t, pos=.1}
  ]
  &&
  B'
  \ar[
    from=s,
    to=t,
    Rightarrow,
    shorten=10pt,
    "{ r }"
  ]
  &&
  A' \odot B'
  \ar[
    rr,
    "{ f' }"
  ]
  &&
  B'
\end{tikzcd}



***



Notation:

* $G$ a [[finite group]],

* $N(H)/H$ the "[Weyl group](Weyl+group#InEquivariantHomotopyTheory)" of a [[subgroup]] $H \subset G$,

* $Orb_G$ the [[orbit category]] of $G$, equivalently thought of as the [[full subcategory]] of [[G-sets]] $G/H$ of [[cosets]] for [[subgroups]] $H \subset G$,

* $\mathbb{Q}$ the [[ground field]] of [[rational numbers]],

* $Mod_{\mathbb{Q}}^{Orb_G^{op}}$ the [[presheaf category]] on $Orb_G$ with [[coefficients]] in [[rational vector spaces]],

* $\mathbb{Q}[K]$ the [[group algebra]] over the [[rational numbers]], of a [[finite group]] $K$.

\begin{definition}
\label{TheProjectiveGenerators}
([T82, Def. 3.1](#Triantafillou82))
\linebreak

  For 

  * $H \subset G$,

  * $V_H \,\in\, Mod_{ \mathbb{Q}[N(H)/H] }$

define

$$
  \begin{array}{l}
    \underline{V}_H 
    \;\in\;
    Mod_{\mathbb{Q}}^{Orb_G^{op}}
    \\
    \underline{V}_H 
    \;\equiv\;
    \mathbb{Q}\big[
      Orb_G(-,G/H)
    \big]
    \underset{
      \mathbb{Q}[N(H)/H]
    }{\otimes}
    V_H
  \end{array}
$$
\end{definition}


\begin{proposition}
  \label{ProjectiveGeneratorsAreIndeedProjective}
  ([T82, Prop. 3.2](#Triantafillou82))
  \linebreak
  The objects $\underline{V}_H$ from Def. \ref{TheProjectiveGenerators} are [[projective object|projective]] in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$.
\end{proposition}


\begin{proposition}
([T82, Prop. 3.4](#Triantafillou82))
\linebreak
 Every [[projective object]] $P \,\in\, Mod_{\mathbb{Q}}^{Orb_G^{op}}$ is a [[direct sum]] of projective generators as in Prop. \ref{TheProjectiveGenerators}.
\end{proposition}

\begin{proof}
We make a bunch of choices:

First, in each [[conjugacy class]] $[H]$ of [[subgroups]] $G$ choose one representative $H \subset G$.

For that $H \hookrightarrow G$, consider the joint [[span]] of the [[images]] of 

$$
  P(G/H \twoheadrightarrow G/H')
  \;\colon\;
  P(G/H') \to P(G/H)
$$

for all intermediate [[subgroup]]-inclusions $H \hookrightarrow H' \hookrightarrow G$:

$$
  0
  \to
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
  \hookrightarrow
  P(G/H)
  \twoheadrightarrow
  P(G/H)
    \big/
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
  \to 
  0
  \,.
$$

On the right we have exhibited the [[quotient vector space]] of the inclusion of the joint images on the left (hence the joint [[cokernel]]) making a [[short exact sequence]] of [[rational vector spaces]].

Since [every short exact sequence of vector spaces splits](split+exact+sequence#OfVectorSpaces), we may next *choose* a [[split exact sequence|splitting]]:

\[
  \label{TheSplitting}
  \sigma_H 
    \;\;\colon\;\;
  P(G/H)
    \big/
  \underset{ H' \supset H }{
    \textstyle{\sum}
  } 
  im\big(
    P(G/H \twoheadrightarrow G/H')
  \big)
    \xhookrightarrow{\phantom{---}}
  P(G/H)
  \,,
\]

whose [[image]] we denote by

$$
  V_H
  \;\;\;\coloneqq\;\;\;
  \sigma
  \Big(
    P(G/H)
      \big/
    \underset{ H' \supset H }{
      \textstyle{\sum}
    } 
    im\big(
      P(G/H \twoheadrightarrow G/H')
    \big)
  \Big)
  \xhookrightarrow{\phantom{---}}
  P(G/H)
  \,.
$$

Via these (images of) chosen splittings, we may define a morphism in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$ as follows, out of the direct sum of their underlined versions from \ref{TheProjectiveGenerators}:

\[  
  \label{ComparisonMorphismForProjectiveDecomposition}
  \array{
    p 
    &\colon&
    \underset{
      [H] 
    }{\oplus}
    \underline{V}_H
    &\longrightarrow&
    P
    \\
    p_{G/K}
    &\colon&
    \underset{
      [H]
    }{\oplus}
    \mathbb{Q}
    \big[
      Orb_G(G/K, G/H)
      \underset{
        \mathbb{Q}[N(H)/H]
      }{\otimes}
      V_H
    \big]
    &\longrightarrow&
    P(G/K)
    \\
    &&
    \big(
      G/K \xrightarrow{ f } G/H
    \big)
    \,\otimes\,
    v_H
    &\mapsto&
    P(f)(v_H)
    \,,
  }
\]

which is manifestly functorial in $G/K$ (via functoriality of $P$) and hence well-defined.

Since all the direct summands on the left are projective by Prop. \ref{ProjectiveGeneratorsAreIndeedProjective}, it is now sufficient to prove that (eq:ComparisonMorphismForProjectiveDecomposition) is an [[isomorphism]]. Since isomorphisms in [[functor categories]] are detected objectwise and  since [[rational vector spaces]] form a [[balanced category]] (see [there](balanced+category#AbelianCategoriesAreBalanced)) for this it is sufficient to show that for all $K \subset G$ the morphism $p_{G/K}$ (eq:ComparisonMorphismForProjectiveDecomposition) is both an [[epimorphism]] and a [[monomorphism]].

First to see that that $p_{G/K}$ is an epimorphism: To start with, it is clearly surjective onto the summand $V_K$. Hence it is next sufficient to show that given $v_K \in P(G/K)$ which is in the image under $P(G/K \twoheadrightarrow G/H)$ of some $\widehat{v}_H \in P(G/H)$ then it is also in the image of $p_{G/K}$. As before, this is clear for those $\widehat{v}_H \in V_H$. Hence next, as before, it is sufficient to show this for those $\widehat{v}_H$ which are in the image under some $P(G/H \twoheadrightarrow G/H')$ of some $v_{H'} \in P(G/H')$... And so on. Since $G$ is a [[finite group]], this recursive argument eventually terminates with $V_G = P(G/G)$.

Finally, to see that $p_{G/K}$ (eq:ComparisonMorphismForProjectiveDecomposition) is a monomorphism. It is here (only) that we use the assumption that $P$ is [[projective object|projective]]. With the previous point, this implies a [[lift]] $p'$ in the following diagram in $Mod_{\mathbb{Q}}^{Orb_G^{op}}$:

\begin{tikzcd}[sep=25pt]
  & 
  \underset{[H]}{\oplus} \underline{V}_H
  \ar[
    d,
    ->>
  ]
  \\
  P
  \ar[, equals]
  \ar[ur, dashed, "{ p' }"]
  &
  P
\end{tikzcd}

Hence if $v,w \,\in\, P(G/K)$ such that $p'_{G/K}(v) = p'_{G/K}(w)$ then $p_{G/K} \circ  p'_{G/K}(v) = p_{G/k} \circ p'_{G/K}(w)$ hence $v = w$, whence each $p'_{G/K}$ is injective.
\end{proof}

## References

* {#Triantafillou82} [[Georgia Triantafillou]], *Equivariant minimal models*, Trans. Amer. Math. Soc. **274** (1982) 509-532 &lbrack;[jstor:1999119](http://www.jstor.org/stable/1999119)&rbrack;




***

$\underline{ }$

Is there an escape from \[brackets\]?


Consider the [[equivalence of categories]] between [[real vector spaces]] and [Real vector bundles](real+vector+bundle#InKRTheory) over the point, given by [[complexification]] equipped with the [[involution]] by [[complex conjugation]]:


\linebreak

\linebreak

\[\label{RModulesAsRealBundlesViaComplexification}\]
\begin{imagefromfile}
    "file_name": "RModulesAsRealBundles-231110.jpg",
    "width": 520,
    "unit": "px",
    "margin": {
        "top": -75,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\begin{proposition}
  Under this equivalence, a [[real vector space|real]] [[inner product space]] $\mathscr{V} \,\in\, Mod_{\mathbb{R}}$, $g \,\colon\, \mathscr{V} \otimes_{{}_{\mathbb{R}}} \mathscr{V} \to \mathbb{R}$  equipped with an [[isometry|isometric]] [[complex structure]] $J \,\colon\, \mathscr{V} \to \mathscr{V}$, $g\big(J(-), J(-)\big) = g(-,-)$ is sent to corresponding [[Hermitian form]] $\langle -\vert-\rangle \,\equiv\, g(-,-) + \mathrm{i}g\big(J(-),-\big)$, as follows:

\linebreak

\linebreak

\[\label{RealInnerProductsAsHermitianForms}\]
\begin{imagefromfile}
    "file_name": "RealInnerProductsAsHermitianForms-231110b.jpg",
    "width": 530,
    "unit": "px",
    "margin": {
        "top": -75,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\end{proposition}
\begin{proof}
On the right we used this $\mathbb{C}$-linear isomorphism from the plain complexification in (eq:RModulesAsRealBundlesViaComplexification):

[[ComplexificationOfComplexStructure-231111.jpg:file]]

\begin{imagefromfile}
    "file_name": "ComplexificationOfComplexStructure-231110.jpg",
    "width": 510,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

which serves to bring out the [[eigenspaces]] of $J \otimes_{{}_\mathbb{R}} \mathbb{C}$:

\linebreak

\linebreak

\[\label{ComplexifiedComplexStructure}\]
\begin{imagefromfile}
    "file_name": "ComplexifiedComplexStructure-231110.jpg",
    "width": 320,
    "unit": "px",
    "margin": {
        "top": -75,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

With this, the isometry condition $g \circ (J \otimes J) = g$  --- which means that $g$ factors through the $(+1)$-eigenspace of $J \!\otimes_{{}_\mathbb{R}}\! J$ --- implies by functoriality of the equivalence (eq:RModulesAsRealBundlesViaComplexification) that the pairing on the right of (eq:RealInnerProductsAsHermitianForms) factors through the $(+1)$-eigenspace of $\mathrm{I} \otimes \mathrm{I}$ (eq:ComplexifiedComplexStructure), which already makes it a Hermitian form on $\VectorSpace{V}_{+J}$, as shown on the right of (eq:RealInnerProductsAsHermitianForms).
Explicit computation shows that this is indeed the one given by the traditional formula:

\begin{imagefromfile}
    "file_name": "RealInnerProductProducesTradFormula-231110.jpg",
    "width": 880,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\end{proof}

\linebreak

\begin{remark}\label{HermitianFormsViaHermitianMetrics}
**(Hermitian forms via Hermitian metrics)**
\linebreak
The decomposition of a Hermitian form into its [[real part]] and [[imaginary part]] is traditionally written with the symbols
$$
  \langle-\vert-\rangle
  \;=\;
  g(-,-)
  +
  \mathrm{i} \omega(-,-)
$$
or similar, where
$$
  g(-,-)
  \;\coloneqq\;
  \Re \langle-\vert-\rangle
  \,,
$$
$$
  \omega(-,-)
  \;\coloneqq\;
  \Im \langle-\vert-\rangle
  \,.
$$
are real [[bilinear forms]] on the [[underlying]] [[real vector space]].

In fact, the real part fully determines the imaginary part and hence the Hermitian form:
$$
  \begin{array}{l}
    \omega(-,-)
    & =
    \Im \langle-\vert-\rangle
    \\
    & = 
    \Re \big(-\mathrm{i} \langle-\vert-\rangle\big)
    \\
    & =
    \Re \langle \mathrm{i} - \vert - \rangle
    \\
    & =
    \Re \langle J(-) \vert - \rangle
    \\
    & =
    g\big(J(-), -\big)
    \,,
  \end{array}
$$
where in the last line we introduced the [[complex structure]] $J$ on the [[underlying]] real vector space which promotes it back to the original complex vector space.

Notice that the complex structure $J$ is an [[orthogonal map]] with respect to the inner product $g$, equivalently $g$ is a [[Hermitian metric]] with respect to $J$, in that

$$
  \begin{array}{l}
    g\big(J(-), J(-)\big)
    \\
    \;=\;
    \Re 
    \big\langle 
      \mathrm{i}(-) 
    \big\vert 
      \mathrm{i}(-) 
    \big\rangle
    \\
    \;=\;
    \Re 
    \big(
      -\mathrm{i} \cdot \mathrm{i}
      \langle - \vert - \rangle
    \big)
    \\
    \;=\;
    \Re 
      \langle - \vert - \rangle
    \\
    \;=\;
    g(-,-)
    \,.
  \end{array}
$$ 

Conversely, for a real vector space equipped with a [[complex structure]] $J$ and a [[Hermitian metric]] $g$, in that $g\big(J(-), J(-)\big) \,=\, g(-,-,)$, the formula
$$
  \langle-\vert-\rangle
  \;=\;
  g(-,-)
  +
  \mathrm{i} 
  g\big(J(-), -\big)
$$
defines a Hermitian form on the corresponding complex vector space:

The linearity in the second argument is clear. The [[anti-linear map|antilinearity]] in the first argument follows by:
$$
  \begin{array}{l}
    g(\mathrm{i}-,-)
    +
    \mathrm{i} 
    g\big(J(\mathrm{i}-), -\big)
    \\
    \;=\;
    g\big(J(-),-\big)
    +
    \mathrm{i} 
    g\big(J\circ J (-), - \big)
    \\
    \;=\;
    g\big(J(-),-\big)
    -
    \mathrm{i} 
    g\big(-, - \big)
    \\
    \;=\;
    -\mathrm{i}
    \Big(
      g(-,-)
      +
      \mathrm{i} g\big( J(-), - \big)
    \Big)
    \,.
  \end{array}
$$
and Hermiticity follows by:
$$
  \begin{array}{l}
    g(w,v) 
      + 
    \mathrm{i}
    g\big( J(w), v \big)
    \\
    \;=\;
    g(w,v) 
      + 
    \mathrm{i}
    g\big( J \circ J(w), J(v) \big)
    \\
    \;=\;
    g(w,v) 
      - 
    \mathrm{i}
    g\big( w, J(v) \big)
    \\
    \;=\;
    g(v,w) 
      - 
    \mathrm{i}
    g\big( J(v),  w\big)
    \,.
  \end{array}
$$
\end{remark}



\begin{tikzcd}[column sep=2em]
	{T_A T_B} && {T_AT_B} & {T_{T_AB}} & {T^2_{AB}} && {T_{AB}} \\
	& {T^2_AT_B} & {T_{T_AT_B}} & {T^2_{T_AB}} & {T^3_{AB}} & {T^2_{AB}} \\
	{T_AT_B} & {T_{AT_B}} && {T^2_{AB}} & {T^2_{AB}} & {T^2_{AB}} & {T_{AB}}
	\arrow[Rightarrow, no head, from=1-1, to=3-1]
	\arrow[Rightarrow, no head, from=1-1, to=1-3]
	\arrow["t"', from=3-1, to=3-2]
	\arrow["\mu"', from=3-6, to=3-7]
	\arrow["{t'}", from=1-3, to=1-4]
	\arrow["{T_{t}}", from=1-4, to=1-5]
	\arrow["\mu", from=1-5, to=1-7]
	\arrow[Rightarrow, no head, from=1-7, to=3-7]
	\arrow["{T_\eta T_B}"{description}, from=3-1, to=2-2]
	\arrow["{\eta_T T_B}"', from=1-3, to=2-2]
	\arrow["t"', from=2-2, to=2-3]
	\arrow["\eta"{description}, from=1-3, to=2-3]
	\arrow["{T_{t'}}", from=2-3, to=2-4]
	\arrow["{T_\mu}", from=2-5, to=2-6]
	\arrow["\mu"', from=2-6, to=3-7]
	\arrow["{T^2t}", from=2-4, to=2-5]
	\arrow["\mu"{description}, from=2-5, to=3-6]
	\arrow["\eta"', from=1-7, to=2-6]
	\arrow["{T_{\eta T_B}}"{description}, from=3-2, to=2-3]
	\arrow["{T_{t'}}"', from=3-2, to=3-4]
	\arrow["{T^2_{\eta B}}", from=3-4, to=2-4]
	\arrow["{T^2_{\eta}}"{description}, from=3-4, to=2-5]
	\arrow[Rightarrow, no head, from=3-4, to=3-5]
	\arrow["{T_{\eta}}"{description}, from=3-5, to=2-5]
	\arrow[Rightarrow, no head, from=3-5, to=3-6]
\end{tikzcd}