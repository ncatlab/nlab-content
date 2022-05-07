
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

### Classification of principal $\infty$-bundles

\begin{definition}
  \label{ClassifyingSpaceAsShapeOfDelooping}
  For $\mathcal{G} \,\in\, Groups(SmoothGroupoids_\infty)$
  any [[smooth ∞-group]], write
  $$
    B \mathcal{G}
    \;\;
    \coloneqq
    \;\;
    &#643;
    \mathbf{B} 
    \mathcal{G}
    \;\;
    \simeq
    \mathbf{B} 
    &#643;
    \mathcal{G}
  $$
  for the [[shape modality|shape]] of its [[delooping]], equivalently (since [[shape modality|shape]] preserves the simplicial [[(∞,1)-colimits]] and the [[finite products]] involved in defining the [[delooping]] as the realization of the [[Cech nerve]] of the [[effective epimorphism]] $\ast \to \mathbf{B}\mathcal{G}$) the delooping of its shape.
\end{definition}

\begin{remark}
Recall that $\mathbf{B}\mathcal{G}$ is the [[moduli stack]] of $\mathcal{G}$-[[principal ∞-bundles]], in that for $X \in SmoothGroupoids_\inft$ there is a [[natural equivalence]] (of [[∞-groupoids]])

$$
  \mathcal{G}PrinBund_X
  \;\;
  \simeq
  \;\;
  \mathbf{H}(X,\mathbf{B}\mathcal{G})
  \;\;\;
  \in
  \;
  Groupoids_\infty
  \,.
$$

In particular, upon [[n-truncated object of an (infinity,1)-category|0-truncation]] $\tau_0$, this means that the [[moduli stack]] $\mathbf{B}\mathcal{G}$ classifies [[equivalence classes]] of [[principal ∞-bundles]]:

$$
  \big(\mathcal{G}PrinBund_X\big)_{/\sim_{equ}}
  \;\;
  \simeq
  \;\;
  \tau_0\, \mathbf{H}(X,\mathbf{B}\mathcal{G})
  \;\;\;
  \in
  \;
  Sets
  \,.
$$

But for this reduced information much less than the full [[moduli stack]] may be necessary: A *[[classifying space]]* for $\mathcal{G}$-[[principal ∞-bundles]] is a [[discrete object]] in $Groupoids_\infty \xhookrightarrow{Disc} SmoothGroupoids_\infty$, such that [[homotopy classes]] of maps into its still correspond to [[equivalence classes]] of [[principal ∞-bundles]], at least over suitable domains.
\end{remark}

Slightly coarser than plain equivalence classes of principal $\infty$-bundles are [[concordance classes]] of principal $\infty$-bundles (in fact, often the two notions coincide):

\begin{definition}\label{ConcordanceClassesOfPrincipalInfinityBundles}
  **([[concordance classes]] of [[principal ∞-bundles]])** \linebreak
  For $\mathcal{G} \in Groups(SmoothGroupoids)_\infty$
  and any $X \in SMoothGroupoids_\infty$,  
  we say that a *[[concordance]]* between two [[principal ∞-bundles]]
  $$
    P_0, P_1 \;\in\; \mathcal{G}PrinBund(SmoothGroupoids|infty)_X
  $$
  is a principal $\infty$-bundle on the [[cylinder]] over $X$
  $$
    \widehat P \;\in\; \mathcal{G}PrinBund_{X \times \mathbb{R}}
  $$
  whose restriction to the points $0,1 \,\in\, mathbb{R}$ is 
  [[equivalence in an (∞,1)-category|equivalent]] to the 
  given pair of bundles:
  $$
    {\widehat P}_{\vert X \times \{0\}}
    \;\simeq\;
    P_0
    \;\;\;\;\;\;\;
    \text{and}
    \;\;\;\;\;\;\;
    {\widehat P}_{\vert X \times \{1\}}
    \;\simeq\;
    P_1
    \,.
  $$
  We write
  $$
    \big(
       \mathcal{G}PrinBund_X
    \big)_{/\sim_{conc}}
    \;\;
      \coloneqq
    \;\;
    \big(
       \mathcal{G}PrinBund_X
    \big)
    \big/
    \big(
       \mathcal{G}PrinBund_{X \times \mathbb{R}}
    \big)
  $$
  for the set of [[equivalence classes]] of [[principal ∞-bundles]] under this concordance [[relation]].
\end{definition}

\begin{proposition}
  For 

  * any [[smooth ∞-group]] $\mathcal{G} \,\in\, Groups(SmoothGroupoids_\infty)$;

 * any [[smooth manifold]] $X \,\in\, SmoothManifolds \xhookrightarrow{\;\;y\;\;} SmoothGroupoids_\infty$

the space $B \mathcal{G} \,\in\, Groupoids_\infty \xhookrightarrow{Disc} SmoothGroupoids_\infty$ (Def. \ref{ClassifyingSpaceAsShapeOfDelooping}) is a [[classifying space]] for $\mathcal{G}$-[[principal ∞-bundles]] over $X$, up to [[concordance]] (Def. \ref{ConcordanceClassesOfPrincipalInfinityBundles}), in that we have a [[natural bijection]]:

$$
  \big(
    \mathcal{G}PrinBund_X
  \big)_{/\sim_{conc}}
  \;\;
  \simeq
  \;\;
  \tau_0
  \,
  \mathbf{H}
  \big(
    X,\,
    B \mathcal{G}
  \big)
  \,.
$$

\end{proposition}

\begin{proof}

$$
\begin{aligned}
    \tau_0
    \,
    \mathbf{H}
    \big(
      X, \, B \mathcal{G}
    \big)
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X, \, B \mathcal{G}
    \big]
    \\
    &
    \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X,
      \,
      &#643;
      \, 
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    &#643;
    \,
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    Disc
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    (\Delta^\bullet_{\mathrm{smth}})
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \mathbf{H}
    \big(
      X
      \times
      \Delta^\bullet_{\mathrm{smth}}
      \,
      \mathbf{B}\mathcal{G}
    \big)
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \underset{\longrightarrow}{\mathrm{lim}}
    \,
    \tau_0
    \big(
    {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \Big(
      \tau_0
      \big(
        {\mathcal{G}}PrinBund_{ X }
      \big)
    \Big)
    \big/
    \Big(
      \tau_0
      \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^1_{\mathrm{smth}}}
      \big)
    \Big)
    \\
    & \;\simeq\;
    \big(
      {\mathcal{G}}PrinBund_X
    \big)_{\sim_{\mathrm{conc}}}
  \end{aligned}
$$

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
