
$\rightrightarrows$

$\xleftrightarrow{\sim}$

\begin{proposition}
  The canonical model structure $Cat_{can}$ is [[cartesian monoidal model category]].
\end{proposition}
\begin{proof}
Given a diagram in $Cat$ of for the form
\begin{tikzcd}
  & 
  \mathcal{C} \times \mathcal{D}
  \ar[
    dl,
    "{ F \times \mathrm{Id} }"{swap}
  ]
  \ar[
    dr,
    "{ \mathrm{Id} \times G }"
  ]
  \ar[
    dd,
    phantom,
    "{ \scalebox{.7}{ (po) } }"
  ]
  \\
  \mathcal{C}' \times \mathcal{D}
  \ar[
    ddr,
    "{ \mathrm{Id} \times G }"{swap}
  ]
  \ar[
    dr,
    "{ q_l }"{swap}
  ]
  &&
  \mathcal{C} \times \mathcal{D}'
  \ar[
    ddl,
    "{ F \times \mathrm{Id} }"
  ]
  \ar[
    dl,
    "{ q_r }"
  ]
  \\
  &
  \mathcal{C}' \!\times\! \mathcal{D}
  \underset{ 
    \mathclap{
      \mathcal{C} \times \mathcal{D}
    }
  }{\coprod}
  \mathcal{C} \!\times\! \mathcal{D}'
  \ar[
    d, 
    dashed, 
    "{ F \widehat \times G }"{description}
  ]
  \\
  &
  \mathcal{C}' \times \mathcal{D}'
\end{tikzcd}

First we need to show that $F \widehat{\times} G$ is a cofibrations if both $F$ and $G$ are. By the definition of cofibrations, this means to show that on objects $(F \widehat{\times} G)_0$ is an injective map if both $F_0$ and $G_0$ are injective maps.

Now, since [[limits]] and [[colimits]] in [[Cat]] are computed on the underlying [[graphs]], the functor 
$$
  (-)_0
    \,\colon\,
  Cat \to Set
$$
[[preserved limit|preserves]] both [[limits]] and [[colimits]] and hence in particular preserves [[pushout products]]. Therefore the first statement we are after is that pushout-products of injections of sets are themselves injections, and that is the case, by [this example](pushout-product#InjectionsOfSets).

Second, if $F$ is in addition a weak equivalence, we need to show that then also $F \widehat{\times} G$ is a weak equivalence. 

But with $F$ certainly also $F \times \mathrm{Id}$ is an injective-ob-objects equivalence of categories, hence an acyclic cofibration in the model structure. But since $Cat_{can}$ is a model category, it follows that the pushout $q_r$ (in the above diagram) is an acyclic cofibration, hence in particular a weak equivalence, and by [[2-out-of-3]] applied to the bottom right triangle in the above diagram, it follows that with $F \times Id$ and $q_r$ also $F \widehat{\times} G$ is a weak equivalence.
\end{proof}


\begin{tikzcd}[sep=15pt]
  \mathbf{X}
  \ar[rr]
  \ar[dd]
  \ar[
    rrrr,
    equals,
    to path={
         ([yshift=+00pt]\tikztostart.north)    
      -- ([yshift=+10pt]\tikztostart.north)    
      -- ([yshift=+10pt]\tikztotarget.north)    
      -- ([yshift=+00pt]\tikztotarget.north)    
    }
  ]
  &&
  \widehat{\mathbf{X}}
  \ar[rr]
  \ar[dd]
  \ar[drrr]
  &&
  \mathbf{X}
  \ar[dr]
  \\
  && && & \mathbf{B}G
  \\
  \mathbf{Y}
  \ar[rr]
  &&
  \widehat{\mathbf{Y}}
  \ar[rr]
  \ar[urrr]
  &&
  \mathbf{Y}
  \ar[from=uu, crossing over]
  \ar[ur]
\end{tikzcd} 


Consider

* a [[group]] $G \,\in\, Grp(Set)$, 

* with [[delooping groupoid]] denoted $\mathbf{B}G \,\in\, Grpd(Set) \subset sSet\text{-}Grpd$, 

* an [[inhabited set]] $W \,\in\, Set$,

* equipped with a [[group action]] $G \curvearrowright W \,\in\, G Act(Set)$,

* with [[action groupoid]] denoted $W \sslash G \,\in\, Grpd \hookrightarrow sSet\text{-}Grpd$,

  canonically regarded in the [[slice category|slice]] $sSet\text{-}Grpd_{/\mathbf{B}G}$,

* [[sSet-enriched groupoids]]$\;\mathbf{X}, \mathbf{Y} \,\in\, sSet\text{-}Grpd$ lifted to the [[slice category|slice]] over $\mathbf{B}G$ via $p_\mathbf{X},\, p_\mathbf{Y} \,\in\, sSet\text{-}Grpd_{/\mathbf{B}G}$, where $p_{\mathbf{Y}}$ is an [[isofibration]].

\begin{proposition}
For
$f \colon \mathbf{X} \to \mathbf{Y}$ a morphism in the slice over $\mathbf{B}G$, whose [[underlying]] morphism in $sSet\text{-}Grpd$ is a Dwyer-Kan cofibration, then also (the underlying map of) the fiber product morphism
$$
  (W \sslash G) \times_{\mathbf{B}G} f
  \;\colon\;
  (W \sslash G) \times_{\mathbf{B}G} \mathbf{X}
  \longrightarrow
  (W \sslash G) \times_{\mathbf{B}G} \mathbf{Y}
$$
is a DK-cofibration.
\end{proposition}
\begin{proof}
  If $Obj(\mathbf{Y}) = \varnothing$ then injectivity of $f$ implies that also $Obj(\mathbf{X}) = \varnothing$ and the claim follows readily. Hence assume now that there exists $y_0 \,\in\, Obj(\mathbf{Y})$.

By the assumption that $W$ is inhabited, there is $w_0 \in W$.

If $W \sslash G$ or $\mathbf{Y}$ are not connected, then we may apply the following arguments to all its connected components from which the general claim follows readily. Hence assume now that both $W \sslash G$ and $\mathbf{Y}$ are connected.

By the assumption that $p_{\mathbf{Y}}$ is an isofibration, we may choose for each $g \in G$ and $y \in Obj(\mathbf{Y})$ a [[1-morphism]] 
\[
  \label{LiftedOneMorphism}
  \gamma^y_g \,\colon\, y \to y'
\] 
in $Mor(\mathbf{Y})_1$ with $p_{\mathbf{Y}}(\gamma_g^y) = g$.

Finally we may choose representatives $g' \in G$ for each $[g'] \in G/Stab_G(w_0)$.

Now let $\Gamma \subset Mor(\mathbf{Y})$ denote a set of generators which exhibits $f$ as a cofibration. Write 

\[
  \Gamma_{w_0} 
    \,\subset\, 
  Mor\big( \{w_0\} \times \mathbf{Y} \big) 
    \,\subset\, 
  Mor\big( 
    (W \sslash G) 
      \times_{\mathbf{B}G} 
    \mathbf{Y} 
  \big)
\] 

for the corresponding subset in the fiber product.


We claim that
$$
  \widehat \Gamma
  \;\coloneqq\;
  \Gamma_{w_0}
  \cup
  \big\{
    \gamma^y_{g'}
  \big\}_{
    { y \in Obj(\mathbf{Y}) \setminus f(Obj(\mathbf{X})) }
    \atop
    { [g'] \in G/Stab_G(w_0) }
  }
$$
is a set of generators which exhibits $(W \sslash G) \times_{\mathbf{B}G} f$ as a cofibration.

Namely, every morphism $(w_0, y_1) \to (w, y'_2)$ in $(W \sslash G) \times_{\mathbf{B}G} \mathbf{Y}$ is uniquely decomposed in the form
$$
  (w_0, y_1)
    \xrightarrow{ 
      (\mathrm{e}, \gamma)
    }
  (w_0, y_2) 
    \xrightarrow{ (g', \gamma^{y_2}_{g'}) } 
  (w, y'_2)
$$
for some $\gamma \in Mor\big(\{w_0\} \times \mathbf{Y}\big)$. 

Now $\Gamma$ has furthermore a unique $\Gamma$-generation by assuption, which clealy remains $\widehat{\Gamma}$-unique. If this sequence ends on a morphism in the image of $f$ and at the same time $\gamma^{y_2}_{g'}$ is in the image of $f$, then we compose the latter onto the last step in the sequence, otherwise we append $\gamma^{y_2}_{g'}$ to the sequence. In either case we have uniquely obtained a reduced $\widehat{\Gamma}$-decomposition of the given morphism.
\end{proof}

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
