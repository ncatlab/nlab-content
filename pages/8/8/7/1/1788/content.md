
To make observables on $\mathfrak{l}A$-valued forms on $X$ need to tensor $H_\bullet(\Omega A)$ with $\Omega_{dR} X$ and take the degree-0 part.

For the following examples we use these notational conventions:

* $\mathbb{K}$ denotes a [[field]] of [[characteristic zero]],

* a subscript on a generator denotes its degree,

* $\mathbb{K}\langle\cdots \rangle$ denotes the [[graded vector space|graded]] $\mathbb{K}$-[[vector space]] [[linear span|spanned]] by the [[linear basis]] of generators listed inside the angular brackets;

* $\mathbb{K}[\cdots]$ denotes the [[underlying]] [[vector space]] of the free [[graded-commutative algebra]] on the set of generators listed inside the square brackets;

* $T(-)$ denotes the graded [[tensor algebra]] on a given [[graded vector space]],

* the [[semifree dgc-algebra]] on a given set $\{\cdots\}$ of generators subject to differential relations we denote, with slight abuse of notation, by

  $$
    \mathbb{K}[\cdots]\big/
    \left(
      \begin{array}{c}
        \mathrm{d}(-) = \ldots
        \\
        \vdots
      \end{array}
    \right)
  $$

\begin{example}
**(rational Pontrjagin ring of loop space of 2-sphere)**
\linebreak
The [[Sullivan model of spheres|Sullivan model of]] the [[2-sphere]] is
$$
  CE(\mathfrak{l} S^2)
  \;\simeq\;
  \mathbb{Q}\big[
    \omega_2, \omega_3
  \big]\big/
  \left(
  \begin{array}{l}
    \mathrm{d} \omega_2 \,=\, 0
    \\
    \mathrm{d} \omega_3 
      \,=\, 
    \tfrac{1}{2} \omega_2 \wedge \omega_2
  \end{array}
  \right)
  \,.
$$
From this it follows (since [[the co-binary Sullivan differential is the dual Whitehead product]])
that the binary [[Whitehead brackets]] of $S^2$ are:
$$
  \begin{array}{l}
    [v_1, v_1] = v_2
    \\
    [v_2, v_2] = 0
    \\
    [v_1, v_2] = 0
  \end{array}
$$

The rational Pontrjagin ring of $\Omega S^2$ is the [[universal enveloping algebra]] of this [[super Lie algebra]], hence:
$$
  H_\bullet\big(
    \Omega S^2
    ;\,
    \mathbb{K}
  \big)
  \;\simeq\;
  T\big(
    \mathbb{K}\langle v_1, v_2\rangle
  \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_1^2 - v_2
      \\
      v_1 v_2 - v_2 v_1 
    \end{array}
  \right)
  \mathrlap{\,.}
$$ 
Hence the underlying vector space of the Pontrjagin ring of $\Omega S^2$ is 
$\mathbb{K}[v_1, v_2]$ but the product of the $v_1$ is quantized to $v_1 \cdot v_1 = \tfrac{1}{2}v_2$.

Similarly, the rational Pontrjagin algebra of the loop space of the [[4-sphere]] is 
$$
  H_\bullet\big(
    \Omega S^4
  \big)
  \;\simeq\;
  T\big( \mathbb{K}\langle v_3, v_6\rangle \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_3^2 - v_6
      \\
      v_3 v_6 - v_6 v_3 
    \end{array}
  \right)
$$
whose [[underlying]] $\mathbb{K}$-[[vector space]] is $\mathbb{K}[v_3, v_6]$ but with the product of the $v_3$ quantized to $v_3 \cdot v_3 = \tfrac{1}{2}v_6$.

On the other hand, the [[Sullivan model of complex projective space|Sullivan model of]] [[complex projective space]] $\mathbb{C}P^n$ for $n \geq 2$ has vanishing co-binary part, so that
$$
  H_\bullet\big(
    \Omega \mathbb{C}P^{n \geq 2}
  \big)
  \;\simeq\;
  T\big( \mathbb{K}\langle v_2, v_{2n}\rangle \big)
  \big/
  \left(
    \begin{array}{l}
      2 v_1^2
      \\
      v_1 v_{2n} - v_{2n} v_1
    \end{array}
  \right)
  \;\simeq\;
  \mathbb{K}[v_1, v_{2n}]
$$ 
is just a plain graded-commutative algebra.
\end{example}




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