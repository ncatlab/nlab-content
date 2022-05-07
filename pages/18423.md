
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In any [[cohesive ∞-topos]], the [[shape modality]] &#643; may be interpreted as sending any cohesive [[space]] to its [[path ∞-groupoid]]. This follows by the defining [[adjoint (∞,1)-functor|adjunction]] $&#643; \dashv \flat$ from the interpretation of the [[flat modality]] as sending any [[delooping]] $\mathbf{B} \mathcal{G}$ to the [[moduli stack]] for [[flat ∞-connections]] with [[structure group|structure]] [[∞-group]] $\mathcal{G}$:

$$
  \frac{
    &#643; X 
      \xrightarrow{\;\nabla\;} 
    \phantom{\flat} 
    \mathbf{B}\mathcal{G}
  }{
    \phantom{&#643;}
    X 
      \xrightarrow{ \;\;\; } 
    \flat 
    \mathbf{B}\mathcal{G}
  }
  \;\;\;\;
  {
    { \text{higher parallel transport} } 
    \atop
    { \text{higher flat bundles} }\,,
  }
$$

because this identifies morphisms out of $&#643; X$ as [[higher parallel transport]]-functors for [[gauge group]] $\mathcal{G}$.

Concretely, in the [[cohesive ∞-topos]] of [[smooth ∞-groupoids]] it is readily checked ([[schreiber:differential cohomology in a cohesive topos|dcct]], see around [here](smooth+infinity-groupoid+--+structures#FlatCoefficientsForDeloopedLieGroup) at *[[smooth ∞-groupoid -- structures]]*) that $\flat \mathbf{B}\mathcal{G}$ indeed classifies [[flat ∞-connections]] in the traditional sense. 

It requires more work to show that, in this case, $&#643; X$ is indeed modeled by a [[path ∞-groupoid]] in the traditional sense (say based on the idea of the smooth [[singular simplicial complex]]). That this is indeed the case is Prop. \ref{SmoothShapeModelityGivenBySmoothPathInfinityGroupod} below, due to [[Dmitri Pavlov]] et al.


## Statement
 {#Statement}

Throughout, 

\[
  \label{TheAmbientInfinityTopos}
  \begin{aligned}
    \mathbf{H} 
    &\,\coloneqq\, 
    SmoothGroupoids_\infty
    \\
    &
    \;\simeq\;
    Sh_\infty(CartesianSpaces)
    \;\simeq\;
    Sh_\infty(SmoothManifolds)
    \;\hookrightarrow\;
    PSh_\infty(SmoothManifolds)
  \end{aligned}
\]

denotes the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]], which is the [[hypercomplete (∞,1)-topos]] over the [[site]] of [[smooth manifolds]] or equivalently over the [[dense subsite]] of [[Cartesian spaces]].

\begin{definition}\label{SmoothExtendedSimplices}
**(smooth extended [[simplices]])** \linebreak
  Write
  $$
    \Delta^\bullet_{smooth}
    \;\colon\;
    \Delta  
      \longrightarrow 
    CartesianSpaces
      \xhookrightarrow{\;\;\y\;\;}
    \mathbf{H}
  $$
  for the [[cosimplicial object]] of smooth extended [[simplices]], hence with

$$
  \Delta^n_{smth}
  \;\coloneqq\;
  \Big\{  
    (x_0, \cdots, x_n)
    \,\in\,
    \mathbb{R}^{n+1}
    \,\left\vert\,
    \sum_i x_i \,=\, 0
    \right.
  \Big\}
  \;\subset\;
  \mathbb{R}^{n+1}
$$

and with co-degeneracy and co-face maps given by addition of consecutive variables, and by insertion of zeros, respectively.
\end{definition}

\begin{definition}\label{PathInfinityGroupoid}
**([[path ∞-groupoid]])** \linebreak
  For $A \,\in\, SmoothGroupoids_\infty = Sh_\infty(CartesianSpaces)$, 
  write
  $$
    Sing(A)
    \;\coloneqq\;
    \underset{\underset{[n] \in \Delta^{op}}{\longrightarrow}}{\lim}
    X
    \big(
       \Delta^n_{smth}
    \big)
    \;\;\;
    \in
    Groupoids_\infty
  $$
  for the [[homotopy colimit]] (in [[∞-groupoids]]) of the evaluation of $A$ (as a [[(∞,1)-presheaf]]) on the smooth extended simplices (Def. \ref{SmoothExtendedSimplices}).
\end{definition}

\begin{proposition}\label{SmoothShapeModelityGivenBySmoothPathInfinityGroupod}
**(smooth [[shape modality]] given by smooth [[path ∞-groupoid]])**

  For $A \,\in\, SmoothGroupoids_\infty = Sh_\infty(CartesianSpaces)$, 
  the **smooth path $\infty$-groupoid**, namely the [[(∞,1)-presheaf]]

  $$
    \mathbf{Sing}
    \;\colon\;
    U 
    \;\mapsto\;
    Sing
    \big(
      [U,A]
    \big)
    \;=\;
    \underset{\underset{[n] \in \Delta^n_{smoth}}{\longrightarrow}}{lim}
    \Big(
      A
      \big(
        \Delta^n_{smth} \times U
      \big)
    \Big)
  $$

of smoothly parameterized path $\infty$-groupoids in $A$ (Def. \ref{PathInfinityGroupoid}), 

1. is in fact an [[(∞,1)-sheaf]]

   $$
     \mathbf{Sing}(A)
     \;\in\;
     Sh_\infty(CartesianSpaces)
     \xhookrightarrow{\;\;\;}
     PSh_\infty(CartesianSpaces)
   $$

1. as such is equivalent to the [[shape modality|shape]] of $A$:

   $$
     &#643; A
     \;\simeq\;
     \mathbf{Sing}(A)
     \,,
   $$

   which means in particular (by $&#643; \simeq Disc \circ Shape$) that it is equivalent to the plain [[path ∞-groupoid]] from Def. \ref{PathInfinityGroupoid}, equipped with [[discrete object|discrete]] smooth structure:

   $$
     \mathbf{Sing}(A) \;\simeq\; Disc \circ Sing(A)
     \,.
   $$
  
\end{proposition}

This is due to [Pavlov et al. 19, Thm. 1.1](#BEBP19) (see discussion [here](https://nforum.ncatlab.org/discussion/11361/shape-via-cohesive-path-groupoid/?Focus=93004#Comment_93004)), announced in [Pavlov 14, Thm. 0.2](#Pavlov). The analogous statement for sheaves of [[stable homotopy types]] (which follows essentially formally) was observed in [BNV 13, Lem. 7.5](#BunkeNikolausVoelkl13) (see at *[[differential cohomology hexagon]]* for more on this case).

## Consequences

### Smooth Oka principle
 {#ConsequenceSmoothOkaPrinciple}

The following may be compared to the [[Oka principle]] in [[complex analytic geometry]].

\begin{proposition}\label{SmoothOkaPrinciple}
**(smooth Oka principle)**
  For

  * $X \,\in\, SmoothManifolds \xhookrightarrow{\;\;y\;\;} SmoothGroupoids_\infty$ a [[smooth manifold]] [[(∞,1)-Yoneda embedding|regarded as]] a [[smooth ∞-groupoid]],

  * $A \,\in\, SmoothGroupoids_\infty$ any [[smooth ∞-groupoid]]

we have a [[natural equivalence]]

\[
  \label{SmoothOkaPrincipleEquivalence}
  \big[
    X,
    \,
    &#643; A
  \big]
  \;\;
  \simeq
  \;\;
  &#643;
  [X,A]
  \;\;\;\;\;
  \in
  \;
  SmoothGroupoids_\infty
\]

between the [[mapping stack]] from $X$ to the [[shape modality|shape]] of $A$ and the [[shape modality|shape]] of the [[mapping stack]] into $A$ itself.
\end{proposition}
See also discussion 
[here](https://nforum.ncatlab.org/discussion/6816/the-shape-of-function-objects/?Focus=55210#Comment_55210)
and
[here](https://nforum.ncatlab.org/discussion/11361/shape-via-cohesive-path-groupoid/#Comment_93145).
\begin{proof}
For any $U \in SmoothManifolds$ consider the following sequence of [[natural equivalences]]  of values ([[∞-groupoids]]) of [[(∞,1)-presheaves]] on [[SmoothManifolds]] (eq:TheAmbientInfinityTopos):
$$
  \begin{aligned}
    [X, &#643;A](U)
    & 
    \;\simeq\;  
    Sh_\infty(SmthMfds)
    \big(
      X \times U, &#643;A
    \big)
    \\
    & \;\simeq\;
    PSh_\infty(SmthMfds)
    \Big(
      X \times U, 
      \,
      \big(
      U' 
      \,\mapsto\,
      \underset{\underset{[n] \in \Delta^{\mathrm{op}}}{\longrightarrow}}{\mathrm{lim}} 
      A(U' \times \Delta^n_{\mathrm{smth}})
      \big)
    \Big)
    \\
    & \;\simeq\;
    \underset{\underset{[n] \in \Delta^{\mathrm{op}}}{\longrightarrow}}{\mathrm{lim}}
    PSh_\infty(SmthMfds)
    \Big(
      X \times U,
      \,
      \big(
      U'
      \,\mapsto\,
      A(U' \times \Delta^n_{\mathrm{smth}})
      \big)
    \Big)
    \\
    & \;\simeq\;
    \underset{\underset{[n] \in \Delta^{\mathrm{op}}}{\longrightarrow}}{\mathrm{lim}}
    PSh_\infty(SmthMfds)
    \Big(
      X \times U,
      \,
      [\Delta^n_{\mathrm{smth}}, A]
    \Big)
    \\
    & \;\simeq\;
    \underset{\underset{[n] \in \Delta^{\mathrm{op}}}{\longrightarrow}}{\mathrm{lim}}
    PSh_\infty(SmthMfds)
    \Big(
      \Delta^n_{\mathrm{smth}} \times X \times U,
      \,
      A
    \Big)
    \\
    & \;\simeq\;
    \underset{\underset{[n] \in \Delta^{\mathrm{op}}}{\longrightarrow}}{\mathrm{lim}}
    \big(
      [X,A]( \Delta^n_{\mathrm{smth}} \times U  )
    \big)
    \\
    & \;\simeq\;
    \big(
      &#643; [X,A]
    \big)(U)
    \,,
  \end{aligned}
$$

Here 

* the first step uses the [[closed monoidal structure on presheaves]];

* the second step is Prop. \ref{SmoothShapeModelityGivenBySmoothPathInfinityGroupod};

* the third step uses that with $X \in SmoothManifolds$, by assumption, and with $\Delta^n_{smth} \in CartesianSpaces \hookrightarrow SmoothManifolds$ by Def. \ref{SmoothExtendedSimplices}, also the [[Cartesian product]] $X \times \Delta^n_{smth} \,\in\, SmoothManifolds \xhookrightarrow{y} PSh_\infty(SmoothManifolds)$ is still [[representable functor|representable]], so that by the [[(∞,1)-Yoneda lemma]], we may [[limits of presheaves are computed objectwise|compute the colimit of presheaves objectwise]];

* the fourth just makes explicit the [[internal hom]] in order to make manifest another appeal to the [[closed monoidal structure on presheaves]] in the fifth and sixth step;

* the last step applies again Prop. \ref{SmoothShapeModelityGivenBySmoothPathInfinityGroupod}.

Since the composite of these equivalences is still [[natural equivalence|natural]] in $U$, the statement (eq:SmoothOkaPrincipleEquivalence) follows by the [[(∞,1)-Yoneda embedding]].
\end{proof}


## Related concepts

* [[concordance]]

## References

This identification Prop. \ref{SmoothShapeModelityGivenBySmoothPathInfinityGroupod} is due to
 
* {#Pavlov14} [[Dmitri Pavlov]], _Structured Brown representability via concordance_, 2014 ([pdf](https://dmitripavlov.org/concordance.pdf), [[Pavlov_Concordance.pdf:file]])

* {#BEBP19} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

with a precursor observation in:

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], Lem. 7.5 of: _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))


[[!redirects shape via cohesive path infinity-groupoid]]

[[!redirects smooth Oka principle]]
