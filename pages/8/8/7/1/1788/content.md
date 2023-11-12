Is there an escape from \[brackets\]?

[[LHoTTasQuantumMicroscope.jpg:file]]


\begin{imagefromfile}
    "file_name": "LHoTTasQuantumMicroscope.jpg",
    "float": "right",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

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