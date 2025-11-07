

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--



\tableofcontents



## Idea 

The *Atiyah-Jänich theorem* ([Jänich 1965](#Jänich65), [Atiyah 1967 Thm A1](#Atiyah67)) states that the space of [[Fredholm operators]] $Fred(\mathscr{H})$ on a (countably infinite-dimensional [[separable Hilbert space|separable]], [[complex vector space|complex]]) [[Hilbert space]] $\mathscr{H}$ is a [[classifying space]] for [[topological K-theory]] $K(-)$:

For $X$ a [[compact Hausdorff space]], the [[homotopy classes]] of [[continuous maps]] from $X$ (hence the [[connected components]] of the [[mapping space]]) to $Fred(\mathscr{H})$ are in [[natural bijection]] with $K(X)$

\[
  \label{IndexMap}
  \pi_0 \, 
  Map\big(
    X,
    \,
    Fred(\mathscr{H})
  \big)
  \xrightarrow[\sim]{\phantom{-}ind_X\phantom{-}}
  K(X)
  \,,
\]

where $ind_X$ forms the *index bundle*, an $X$-parameterized enhancement of the [[Fredholm index]] (see Prop. \ref{IndexViaVirtualKernelBundlesOfConstantDimPerturbation} below).

This statement generalizes:

1. to any degrees and to [[KO-theory]] ([Atiyah & Singer 1969 Thm. B](#AtiyahSinger1969), [Karoubi 1970 Lem 1.4 & Prop. 1.5](#Karoubi1970)), given by maps to Fredholm operators satisfying further (anticommutation) conditions,

1. to a definition of [[twisted K-theory]] and of [[equivariant K-theory]] (hence of [[twisted equivariant K-theory]]), given by homotopy classes of [[sections]] of $Fred(\mathscr{H})$-[[fiber bundles]] ([Atiyah & Segal 2004](#AtiyahSegal04)).


## Statement
 {#Statement}

The original Atiyah-Jänich theorem theorem concerns complex [[topological K-theory]], $K(-) = KU^0(-)$ in degree 0 (and hence in any [[even number|even]] degree), see:

* [Statement for $K \mathrm{U}^0$](#StatementForKU0).

Generalization to [[KO-theory]] and [[KSp-theory]] in degree 0 is fairly straightforward by just replacing the [[ground field]] of [[complex numbers]] by the [[real numbers]] or [[quaternions]], respectively, see:

* [Statement for $K \mathrm{O}^0$ and $K \mathrm{O}^4 = K Sp^0$](#StatementForKO0andKSp0).

Generalization to any degree over any ground field is due to [Atiyah & Singer 1969](#AtiyahSinger1969), [Karoubi 1970](#Karoubi1970), see below:

* [Statement for $KU^1$](#StatementForKU1).

* [Statement for $K \mathrm{O}^{\pm 2}$](#StatementForKO2andKO6)

* [Statement for $K \mathrm{O}^{\pm 1}$](#StatementForKO1andKO7)

* [Statement for $K \mathrm{O}^{\pm 3}$](#StatementForKO3andKO5)

In stating these, we mostly review results from [Karoubi 1970 §I](#[Karoubi1970](#Karoubi1970), but we reformulate these (in a straightforward though consequential manner) to bring out (following [Sati & Schreiber 2023 §2.2](#SatiSchreiber2023)) how they exhibit the *[[10-fold way]]* of [[quantum symmetries]] as known from the [[K-theory classification of topological phases of matter]].



### For $K \mathrm{U}^0$
 {#StatementForKU0}

Let [[Fredholm operator|$Fred(\mathscr{H})$]] denote the space of [[Fredholm operators]], equipped with the [[norm topology]], on the countably infinite-dimensional complex [[Hilbert space]] $\mathscr{H}$.

> (A more ambitious construction modifies $Fred(\mathscr{H})$ up to [[homotopy equivalence]] to have it carry a continuous action of the [[PU(ℋ)]] with the [[operator topology]], cf. [Atiyah & Segal 2004](#twisted K-theory#AtiyahSegal04).)


\begin{proposition}
\label{KernelBundles}
  If $f \colon X \longrightarrow Fred(\mathscr{H})$ is such that the [[dimension of a vector space|dimension]] of the [[kernels]] of $f(x)$ is [[locally constant function|locally constant]], hence that they form a [[continuous map]] to the [[integers]]
$$
  dim\Big(
    ker\big(
     f(-)
    \big)
  \Big)
  \,\colon\, 
  X \longrightarrow \mathbb{Z}
$$
then the collection of [[kernels]] and [[cokernels]] themselves, as [[subspaces]] of $X \times \mathscr{H}$, form [[topological vector bundles]]
$$
  ker\big(
    f(-)
  \big),
  \;
  coker\big(
    f(-)
  \big)
  \in
  \mathbb{C}Vec_{X}
  \,.
$$

\end{proposition}

([Jänich 1965 Lemma 4](#Jänich65)).

\begin{proposition}
\label{ConstantKernelDeformationsExist}
Every [[continuous map]] $f \colon X \longrightarrow Fred(\mathscr{H})$ is [[homotopy|homotopic]] to a map $f'$ for which $dim\big(ker(f')\big)$ is continuous.
\end{proposition}
([Jänich 1965 below Lemma 4 using Lemma 3](#Jänich65)).


\begin{proposition}
\label{IndexViaVirtualKernelBundlesOfConstantDimPerturbation}
The index (eq:IndexMap) is given by

$$
  \begin{array}{ccc}
    \pi_0 Map\big(X,Fred(\mathscr{H})\big)
      &\xrightarrow{ ind_X }&
    K(X)
    \\
    [f]  
      &\mapsto&
    \big[ker(f') \ominus coker(f')\big]
    \mathrlap{\,,}
  \end{array}
$$

where $f'$ is any representative of the class $[f]$ according to Prop. \ref{ConstantKernelDeformationsExist}, $ker(f')$ and  $coker(f')$ are its (co)kernel bundles according to Prop. \ref{KernelBundles}, and $(-) \ominus (-)$ is their their [[virtual vector bundle|virtual difference bundle]].
\end{proposition}
([Jänich 1965 Lemma 5](#Jänich65))

\begin{remark}
  The construction of the index map (eq:IndexMap) by [Atiyah 1967 Lem A3, Cor A4](#Atiyah67) is a little different (though the result, of course, is the same). Exposition is in [Sheth §2](#Sheth).
\end{remark}


\begin{remark}
\label{TheSpaceOfGradedFredholmOperators}
**(Graded Fredholm operators)**
\linebreak
  It turns out to be useful (such as for the discussion of [[twisted equivariant K-theory]] and of the [[K-theory classification of topological phases of matter]]) to reformulate, here and in the following, the space of Fredholm operators in the following more structured way (due to [Atiyah & Segal 2004 Def. 3.2](Fredholm+operator#AtiyahSegal04), following [Atiyah & Singer 1969 p 7](#AtiyahSinger69), see also [here](Fredholm+operator#FredZero) at *[[Fredholm operator]]*):

  Given any [[cyclic group of order 2|$C_2$]]-[[graded vector space|graded]] infinite-dimensional ([[separable Hilbert space|separable]] [[complex vector space|complex]]) [[Hilbert space]] 
$$
  \mathscr{H}_{gr} 
    \;\simeq\; 
  \mathscr{H}_+ \oplus \mathscr{H}_-
$$ 
write 
$$
  Fred_{gr}(\mathscr{H}_{gr})
  \;\subset\;
  \mathcal{B}(\mathscr{H}_{gr})
$$ 
for the set of [[bounded linear operators]] $F \,\colon\, \mathscr{H} \to \mathscr{H}$ which are

1. [[self-adjoint operator|self-adjoint]]: $F^\dagger = F$,

1. odd-graded: $F(\mathscr{H}_{\pm}) \subset \mathscr{H}_{\mp}$,

1. [[Fredholm operator|Fredholm]] in that there exists such $\tilde F$ which is a [[parametrix]],

equipped with the [[norm topology]].

This just means that $F \in Fred_{gr}(\mathscr{H}_{gr})$ is of the form

\[
  \label{GradedFredholmOperatorInComponents}
  F 
  \;=\; 
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0 
  \end{matrix}
  \right)
  \;\in\;
  End\big(
    \mathscr{H}_+ \oplus \mathscr{H}_-
  \big)
\]

for $f$ an ordinary [[Fredholm operator]]. 

Therefore this space is [[homeomorphism|homeomorphic]] to the standard space of Fredholm operators:
$$
  \begin{array}{ccc}
    Fred(\mathscr{H})
    &\overset{\sim}{\longrightarrow}&
    Fred_gr(\mathscr{H}_{gr})
    \\
    f 
      &\mapsto&
   \left(
   \begin{matrix}
     0 & f^\dagger
     \\
     f & 0 
   \end{matrix}
   \right)
   \mathrlap{\,,}
  \end{array}
$$
but the way it is presented by graded operators makes manifest that there is "charge conjugation" [[quantum symmetry]] acting on this space, namely by swapping the two homogeneously graded Hilbert space summands. This is useful in the following for neatly expressing (anti-)self-adjointness conditions on Fredholm operators.

(The point of [Atiyah & Segal 2004 §4](Fredholm+operator#AtiyahSegal04) is to further modify this space so that it carries a non-contractible [[compact-open topology]] which allows for more general [[PU(ℋ)]] actions on it. The commutation relations discussed in the following immediately apply also to this modified space and constrain the components $f$ of its elements $F$ in the same way. It seems plausible that the correspondingly constrained modified spaces are accordingly classifying spaces for the various flavors of K-theory as is the case for the unmodified space --- as summarized [below](#SummaryInTermsOfGradedFredholmOperators) --- but this is not actually obvious.)
\end{remark}





### For $K \mathrm{U}^1$
 {#StatementForKU1}

\begin{proposition}
  The space of [[complex numbers|complex]] [[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  \[
    \label{SpaceOfSelfAdjointFredholmOperators}
    Fred^{sa}(\mathscr{H})
    \subset
    \Big\{
      f \in Fred 
      \;\Big\vert\;
      f^\dagger = f
    \Big\}
  \]
  has three [[connected components]]
  $$
    Fred^{sa}(\mathscr{H})
    \;\simeq\;
    Fred_+^{sa}(\mathscr{H})
    \,\sqcup\,
    Fred_-^{sa}(\mathscr{H})
    \,\sqcup\,
    Fred_\ast^{sa}(\mathscr{H})
    \mathrlap{\,,}
  $$
  corresponding to those Fredholm operators whose [[essential spectrum]] (which is [[real number|real]], by [[self-adjoint operator|self-adjointness]]) is, respectively:

  1. $Fred_+^{sa}(\mathscr{H})$: purely [[positive number|positive]],

  1. $Fred_-^{sa}(\mathscr{H})$: purely [[negative number|negative]],

  1. $Fred_{\ast}^{sa}(\mathscr{H})$: both, hence [[inhabited set|nonempty]] both above and below [[zero]].

Moreover, 

1. the first two components are [[contractible topological space|contractible]]

   $$
     Fred^{sa}_{\pm}(\mathscr{H}) \simeq \ast
     \,,
   $$

1. the last component is [[homotopy equivalence|homotoppy equivalent]] to the [[stable unitary group]], hence to the [[classifying space]] for [[complex numbers|complex]] [[topological K-theory]] in odd degree:

   $$
     Fred^{sa}_{\ast} \simeq U \simeq KU_1
     \,.
   $$

\end{proposition}

Up to some straightforward re-identifications (for instance one may equivalently use *skew* self-adjoint operators whose spectrum is then purely [[imaginary number|imaginary]]), this is the statement of [Atiyah & Singer 1969 Thm. B](#AtiyahSinger1969) and [Karoubi 1970 Lem 1.4 & Prop. 1.5](#Karoubi1970).


\begin{remark}
\label{SelfAdjointViaCommutingWithP}
  In terms of the graded Fredholm operators $F$ (eq:GradedFredholmOperatorInComponents) from Rem. \ref{TheSpaceOfGradedFredholmOperators}, the self-adjoint Fredholm operators (eq:SpaceOfSelfAdjointFredholmOperators) are equivalently those that commute with the operator
\[
  \label{TheChargeSwappingOperator}
  \widehat{P}
  \coloneqq 
  \left(
    \begin{matrix}
       0 & id
       \\
       id & 0
    \end{matrix}
  \right)
  \,.
\]
\end{remark}



### For $K \mathrm{O}^0$ and $K \mathrm{O}^4 = K Sp^0$
  {#StatementForKO0andKSp0}

The directly analogous discussion as for complex K-theory $KU^0$ in degree 0 ([above](#StatementForKU0)) applies when replacing the underlying complex Hilbert space $\mathscr{H}$ with a [[real vector space|real]] or [[quaternionic vector space|quaternionic]] [[Hilbert space]], where it yields real K-theory ([[KO-theory]]) and [[quaternionic K-theory]] ([[KSp-theory]]) in degree=0, respectively.

It is useful to express this in terms of [[complex vector spaces|complex]] [[Hilbert spaces]] but equipped with [[real structure]] or [[quaternionic structure]], respectively, namely with a [[complex numbers|complex]] [[antilinear map]]

$$
  \widehat{T} 
    \,\colon\, 
  \mathscr{H} \longrightarrow \mathscr{H}
$$

which squares to $\pm 1$, respectively, whence the statement reads as follows:

\begin{proposition}
Let $\widehat T$ be an [[antilinear map]] on the [[complex numbers|complex]] [[Hilbert space]] $\mathscr{H}$ such that 
$$
  \widehat T^2 = + id
  \mathrlap{\,,}
$$
then the space of [[real numbers|real]]-[[Fredholm operators]]

$$
  Fred_{\mathbb{R}}
  \,\coloneqq\,
  \Big\{
    F \in Fred
    \,\Big\vert\,
    F \circ \widehat T
    = 
    \widehat{T} \circ F
  \Big\}
  \;\simeq\;
  B O
  \;\simeq\;
  KO_0
$$

is [[homotopy equivalence|homotopy equivalent]] to the [[classifying space]]/[[delooping]] of the [[stable orthogonal group]] and hence is a classifying space for [[KO-theory]].
\end{proposition}

([Jänich 1965 p. 132](#Jänich65); [Atiyah 1969 §2 p. 102](#Atiyah69); [Karoubi 1970 Prop. 1.3 p. 78](#Karoubi1970))

\begin{proposition}  
Let $\widehat T$ be an [[antilinear map]] on the [[complex numbers|complex]] [[Hilbert space]] $\mathscr{H}$ such that 
$$
  \widehat T^2 = - id
  \mathrlap{\,,}
$$
then the space of [[quaternions|quaternionic]]-[[Fredholm operators]]

$$
  Fred_{\mathbb{H}}
  \,\coloneqq\,
  \Big\{
    F \in Fred
    \,\Big\vert\,
    F \circ \widehat T
    = 
    \widehat{T} \circ F
  \Big\}
  \;\simeq\;
  B Sp
  \;\simeq\;
  KO_4
$$

is [[homotopy equivalence|homotopy equivalent]] to the [[classifying space]]/[[delooping]] of the stable [[quaternionic unitary group]] and hence is a classifying space for [[KSp-theory]].

\end{proposition}

([Atiyah & Singer 1969 p. 323](#AtiyahSinger1969); [Karoubi 1970 Prop. 1.12 p. 81](#Karoubi1970))




### For $K \mathrm{O}^{\pm 2}$
 {#StatementForKO2andKO6}


First some basic preliminaries:

\begin{lemma}
\label{SelfAdjointAntiLinearOperator}
  For a [[complex numbers|complex]] [[anti-linear operator]] $A$ on a [[Hilbert space]] $\mathscr{H}$, the following are equivalent:

1. $A$ is Hermitian self-adjoint, $A^\dagger = A$, as an anti-linear operator (cf. [there](antilinear+map#DefinitionOnHermitianSpaces)) with respect to the [[Hermitian inner product]] $\langle -,-\rangle$,

1. $A$ is [[self-adjoint operator|self-adjoint]], $A^\ast = A$, as a [[real numbers|real]] [[linear operator]] with respect to the [[underlying]] real inner product, $Re\big(\langle -,-\rangle\big)$, given by the [[real part]] of the [[Hermitian inner product]].

\end{lemma}
\begin{proof}
  One direction is immediate: 
$$
  \big\langle A v , w \big\rangle 
  =
  \overline{
    \big\langle v , A w \big\rangle 
  }
  \;\;\;\;\;\; 
  \Rightarrow
  \;\;\;\;\;\;
  Re\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  Re\Big(
  \overline{
    \big\langle v , A w \big\rangle 
  }
  \Big)
  =
  Re\Big(
    \big\langle v , A w \big\rangle 
  \Big)
  \mathrlap{\,.}
$$

In the other direction: Assuming that 
$$
  Re\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  Re\Big(
    \big\langle v , A w \big\rangle 
  \Big)
$$
we need to show that then 
$$
  Im\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  -
  Im\Big(
    \big\langle v , A w \big\rangle 
  \Big)
  \mathrlap{\,.}
$$
For that we compute as follows (where we use the convention that $\langle-,-\rangle$ is anti-linear in the first and linear in the second argument, but the same conclusion holds of course with the other convention):
$$
  \begin{array}{lll}
    Im\Big(
      \big\langle A v , w \big\rangle 
    \Big)
    & =
    Re\Big(
      -\mathrm{i}
      \big\langle A v , w \big\rangle 
    \Big)   
    & \text{basic property of complex arithmetic}
    \\
    & =
    Re\Big(
      \big\langle A v , - \mathrm{i} w \big\rangle 
    \Big)   
    & \text{sesqui-linearity of inner product}
    \\
    & =
    Re\Big(
      \big\langle v , A(-\mathrm{i} w) \big\rangle 
    \Big)   
    & \text{assumption of real self-adjointness}
    \\
    & =
    Re\Big(
      \big\langle v , \mathrm{i} A w \big\rangle 
    \Big)   
    & \text{assumption of complex anti-linearity}
    \\
    & =
    Re\Big(
      \mathrm{i}
      \big\langle v , A w \big\rangle 
    \Big)   
    & \text{sesqui-linearity of inner product}
    \\
    & =
    -Im\Big(
      \big\langle v , A w \big\rangle 
    \Big)   
    & \text{basic property of complex arithmetic}
    \mathrlap{\,.}
  \end{array}
$$
\end{proof}


\begin{example}
  The canonical [[real structure]] on $\mathbb{C}$
  $$
    \begin{array}{ccc}
      \mathbb{C} 
        &\xrightarrow{\; \widehat{T} \;}& 
      \mathbb{C}
      \\
      z &\mapsto& \overline{z}
    \end{array}
  $$
  is self-adjoint (cf. Lem. \ref{SelfAdjointAntiLinearOperator}):
  $$
    \begin{aligned}
      \big\langle
        \widehat{T} z
        ,
        w
      \big\rangle
      & =
      \big\langle
        \overline{z}
        ,
        w
      \big\rangle
      \\
      & =
      \overline{\overline{z}} \, w
      \\
      & =
      z \, w
      \\
      & =
      \overline{
        \overline{z} \, \overline{w}
      }
      \\
      & =
      \overline{
        \big\langle
           z, \overline{w}
        \big\rangle
      }
      \\
      & =
      \overline{
        \big\langle
           z, \widehat{T} w
        \big\rangle
      }
      \mathrlap{\,.}
    \end{aligned}
  $$
\end{example}

\begin{example}
  The canonical [[quaternionic structure]] on $\mathbb{C}^2$
  $$
    \begin{array}{ccc}
      \mathbb{C}^2 
        &\xrightarrow{\; \widehat{T} \;}& 
      \mathbb{C}^2
      \\
      \left(
      \begin{matrix}
        z_1
        \\
        z_2
      \end{matrix} 
      \right)
        &\mapsto& 
      \left(
      \begin{matrix}
        -\overline{z_2}
        \\
        \overline{z_1}
      \end{matrix} 
      \right)
    \end{array}
  $$
  is anti-self-adjoint (cf. Lem. \ref{SelfAdjointAntiLinearOperator}):

$$
  \begin{aligned}
    \Big\langle
      \widehat{T}\vec z
      ,\,
      \vec w
    \Big\rangle
    & =
    \left\langle
    \left(
      \begin{matrix}
        -\overline{z_2}
        \\
        \overline{z_1}
      \end{matrix} 
    \right)
    ,
    \left(
      \begin{matrix}
        w_1
        \\
        w_2
      \end{matrix} 
    \right)
    \right\rangle
    \\
    & =
    - z_2 \, w_1 \;+\; z_1 \, w_2
    \\
    & =
    \overline{
      - \overline{z_2} \, \overline{w_1}
      +
      \overline{z_1} \, \overline{w_2}
    }
    \\
    & =
    \overline{
      \left\langle
      \left(
        \begin{matrix}
          z_1
          \\
          z_2
        \end{matrix} 
      \right)
      ,
      \left(
        \begin{matrix}
          \overline{w_2}
          \\
          -\overline{w_1}
        \end{matrix} 
      \right)
    \right\rangle
    }
    \\
    & = 
    -
    \Big\langle
      \vec z
      ,\,
      \widehat{T} \vec w
    \Big\rangle
    \mathrlap{\,.}
  \end{aligned}
$$
\end{example}

Now:

\begin{proposition}
\label{KaroubiModelForKO2}
  The space of [[Fredholm operators]] on the complex Hilbert space $\mathscr{H}$ which are

1. [[anti-linear maps|anti-linear]],

1. (skew) [[self-adjoint operator|self-adjoint]] (cf. Lem. \ref{SelfAdjointAntiLinearOperator}):

   $F^\dagger = \pm F$

is a classifying space for $K\mathrm{O}^{\pm 2}$ (where $K\mathrm{O}^{-2} \simeq K \mathrm{O}^6$).
\end{proposition}
([Karoubi 1970 Props. 1.9, 1.12](#Karoubi1970))

It is useful to reformulate Prop. \ref{KaroubiModelForKO2} as follows:

\begin{proposition}
On the complex Hilbert space $\mathscr{H}$ consider a [[real structure|real]]/[[quaternionic structure]] $\widehat T$, in that

1. $\widehat{T}$ is [[anti-linear map|anti-linear]],

2. $\widehat{T}^2 = \pm 1$,

3. $\widehat{T}^\dagger = \pm \widehat{T}$ (cf. Lem. \ref{SelfAdjointAntiLinearOperator}).

On the $\mathbb{Z}/2$-graded Hilbert space $\mathscr{H} \oplus \mathscr{H}$ (cf. Rem. \ref{TheSpaceOfGradedFredholmOperators}) consider 

$$
  \widehat{C}
  \,\coloneqq\,
  \left(
  \begin{matrix}
    0 & \widehat{T} 
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \mathrlap{\,.}
$$

Then the space
 
$$
  \bigg\{
    F \in Fred(\mathscr{H} \oplus \mathscr{H})
    \;\bigg\vert\;
    \substack{
      F\;\text{is odd},
      \\
      F^\dagger = F,
    }
    \;\;
    F \circ \widehat{C} = \widehat{C} \circ F
  \bigg\}
$$

is a classifying space for $K\mathrm{O}^{\pm 2}$.
\end{proposition}
\begin{proof}
  The fact that $F$ in our space is odd and self-adjoint implies that it is of the form
$$
  F 
    = 
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  \,.
$$
From this, the further condition that it commutes with $\widehat{C}$,
$$
  \left(
  \begin{matrix}
    0 & \widehat{T}
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \cdot
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  =
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  \cdot
  \left(
  \begin{matrix}
    0 & \widehat{T}
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \mathrlap{\,,}
$$
means equivalently that
$$
  \widehat{T} \circ f 
    \;=\; 
  f^\dagger \circ \widehat{T}
  \,,
$$
and hence our space is equivalently given by
$$
  \Big\{
    f \in Fred(\mathscr{H})
    \;\Big\vert\;
    \widehat{T} \circ f 
      \;=\; 
    f^\dagger \circ \widehat{T}
  \Big\}
  \,.
$$
For $f$ of this form, notice that $\widehat{T} \circ f$ is (anti-linear and) self-adjoint/anti-self-adjoint:
$$
  \big(
    \widehat{T} \circ f
  \big)^\dagger
  \;=\;
  f^\dagger \circ (\pm)\widehat{T}
  \;=\;
  \pm
  \widehat{T} \circ f
  \mathrlap{\,.}
$$

Therefore this space is homeomorphic to the space from Prop. \ref{KaroubiModelForKO2}, via the map
$$
  f \;\mapsto\; \widehat{T} \circ f 
  \,,
$$
and hence the claim follows by Prop. \ref{KaroubiModelForKO2}.
\end{proof}




### For $K \mathrm{O}^{\pm 1}$
 {#StatementForKO1andKO7}


\begin{proposition}
  The space of [[real numbers|real]] [[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  \[
    \label{SpaceOfSelfAdjointFredholmOperators}
    Fred^{sa}(\mathscr{H}_{\mathbb{R}})
    \subset
    \Big\{
      f \in Fred(\mathscr{H}_{\mathbb{R}}) 
      \;\Big\vert\;
      f^\dagger = f
    \Big\}
  \]
  has three [[connected components]]
  $$
    Fred^{sa}
    \;\simeq\;
    Fred_+^{sa}(\mathscr{H}_{\mathbb{R}})
    \,\sqcup\,
    Fred_-^{sa}(\mathscr{H}_{\mathbb{R}})
    \,\sqcup\,
    Fred_\ast^{sa}(\mathscr{H}_{\mathbb{R}})
    \mathrlap{\,,}
  $$
  corresponding to those Fredholm operators whose [[essential spectrum]] is, respectively:

  1. $Fred_+^{sa}(\mathscr{H}_{\mathbb{R}})$: purely [[positive number|positive]],

  1. $Fred_-^{sa}(\mathscr{H}_{\mathbb{R}})$: purely [[negative number|negative]],

  1. $Fred_{\ast}^{sa}(\mathscr{H}_{\mathbb{R}})$: both, hence [[inhabited set|nonempty]] both above and below [[zero]].

Moreover, 

1. the first two components are [[contractible topological space|contractible]]

   $$
     Fred^{sa}_{\pm}(\mathscr{H}_{\mathbb{R}}) \simeq \ast
     \,,
   $$

1. the last component is [[homotopy equivalence|homotoppy equivalent]] to the [[stable orthogonal group]], hence to the [[classifying space]] for [[real numbers|real]] [[topological K-theory]] ([[KO-theory]]) in degree=1:

   $$
     Fred^{sa}_{\ast}(\mathscr{H}_{\mathbb{R}}) 
      \;\simeq\; 
     O 
      \;\simeq\; 
     KO_1
     \,.
   $$

\end{proposition}
([Atiyah & Singer 1969 Cor. to Thm. A(k)](#AtiyahSinger1969), [Karoubi 1970 Lem 1.4, Dem. 1.4, Prop. 1.5](#Karoubi1970))

\begin{proposition}
  The space of [[real numbers|real]] anti-[[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  \[
    \label{SpaceOfSelfAdjointFredholmOperators}
    Fred^{sa}(\mathscr{H}_{\mathbb{R}})
    \subset
    \Big\{
      f \in Fred 
      \;\Big\vert\;
      f^\dagger = -f
    \Big\}
  \]
  is a classifying space for $K\mathrm{O}^{-1} \simeq K\mathrm{O}^7$.
\end{proposition}
([Atiyah & Singer 1969 Theorem A](#AtiyahSinger1969), [Karoubi 1970 Lem 1.6, Cor. 1.7](#Karoubi1970))

\begin{remark}
  In terms of graded Fredholm operators $F$ (Rem. \ref{TheSpaceOfGradedFredholmOperators}), these real (skew) self-adjoint operators $f$ are equivalently those $F$ which commute both with a [[real structure]] [[anti-linear map]] $\widehat{T}$, $\widehat{T}^2 = +1$, and with the operator $\widehat{P}$ (eq:TheChargeSwappingOperator).
\end{remark}



### For $K \mathrm{O}^{\pm 3}$
 {#StatementForKO3andKO5}

\begin{proposition}
  The space of [[quaternions|quaternionic]] [[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  \[
    \label{SpaceOfSelfAdjointFredholmOperators}
    Fred^{sa}(\mathscr{H}_{\mathbb{H}})
    \subset
    \Big\{
      f \in Fred(\mathscr{H}_{\mathbb{H}}) 
      \;\Big\vert\;
      f^\dagger = f
    \Big\}
  \]
  has three [[connected components]]
  $$
    Fred^{sa}(\mathscr{H}_{\mathbb{H}})
    \;\simeq\;
    Fred_+^{sa}(\mathscr{H}_{\mathbb{H}})
    \,\sqcup\,
    Fred_-^{sa}(\mathscr{H}_{\mathbb{H}})
    \,\sqcup\,
    Fred_\ast^{sa}(\mathscr{H}_{\mathbb{H}})
    \mathrlap{\,,}
  $$
  corresponding to those Fredholm operators whose [[essential spectrum]] (which is [[real numbers|real]], due to self-adjointness) is, respectively:

  1. $Fred_+^{sa}(\mathscr{H}_{\mathbb{H}})$: purely [[positive number|positive]],

  1. $Fred_-^{sa}(\mathscr{H}_{\mathbb{H}})$: purely [[negative number|negative]],

  1. $Fred_{\ast}^{sa}(\mathscr{H}_{\mathbb{H}})$: both, hence [[inhabited set|nonempty]] both above and below [[zero]].

Moreover, 

1. the first two components are [[contractible topological space|contractible]]

   $$
     Fred^{sa}_{\pm}(\mathscr{H}_{\mathbb{H}}) \simeq \ast
     \,,
   $$

1. the last component is [[homotopy equivalence|homotoppy equivalent]] to the stable [[quaternionic unitary group]], hence to the [[classifying space]] for [[quaternionic K-theory]] in degree 1, hence of [[real number|real]] [[topological K-theory]] ([[KO-theory]]) in degree=5:

   $$
     Fred^{sa}_{\ast}(\mathscr{H}_{\mathbb{H}}) 
      \;\simeq\; 
     KSp_1
      \;\simeq\;
     KO_5
     \,.
   $$

\end{proposition}
([Atiyah & Singer 1969 Thm. A(k)](#AtiyahSinger1969), [Karoubi 1970 Prop. 1.13](#Karoubi1970))

\begin{proposition}
  The space of [[quaternion|quaternionic]] anti-[[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  \[
    \label{SpaceOfSelfAdjointFredholmOperators}
    Fred^{sa}(\mathscr{H}_{\mathbb{H}})
    \subset
    \Big\{
      f \in Fred(\mathscr{H}_{\mathbb{H}}) 
      \;\Big\vert\;
      f^\dagger = -f
    \Big\}
  \]
  is a classifying space for $K\mathrm{O}^{3}$.
\end{proposition}
([Atiyah & Singer 1969 Theorem A(k)](#AtiyahSinger1969), [Karoubi 1970 Prop. 1.14](#Karoubi1970))

\begin{remark}
  In terms of graded Fredholm operators $F$ (Rem. \ref{TheSpaceOfGradedFredholmOperators}), these quaternionic (skew) self-adjoint operators $f$ are equivalently those $F$ which commute both with a [[quaternionic structure]] [[anti-linear map]] $\widehat{T}$, $\widehat{T}^2 = -1$, and with the operator $\widehat{P}$ (eq:TheChargeSwappingOperator).
\end{remark}



### Summary

#### In terms of plain Fredholm operators
 {#SummaryInTermsOfPlainFredholmOperators}

In terms of ordinary [[Fredholm operators]] (on a countably infinite dimensional [[Hilbert space]]) we have ([Karoubi 1970 Thm. 1.16](#Karoubi1970)):

| The space of such Fredholm operators | classifies |
|---|---|
| complex  |  $K \mathrm{U}^0$ |
| complex self-adjoint | $K \mathrm{U}^1$ |
| real  |  $K \mathrm{O}^0$ |
| real self-adjoint | $K \mathrm{O}^1$ |
| real anti-self-adjoint | $K\mathrm{O}^7$ |
| quaternionic  |  $K \mathrm{O}^4$ |
| quaternionic self-adjoint | $K \mathrm{O}^5$ |
| quaternionic anti-self-adjoint | $K \mathrm{O}^{3}$ |
| complex anti-linear self-adjoint  |  $K \mathrm{O}^2$ |
| complex anti-linear anti-self-adjoint | $K \mathrm{O}^6$ |

hence, conversely:

| this K-theory | is classified by such Fredholm operators |
|---|---|
| $K \mathrm{U}^0$ | complex  |  
| $K \mathrm{U}^1$ | complex self-adjoint | 
| $K \mathrm{O}^0$ | real  |  
| $K \mathrm{O}^1$ | real self-adjoint  |
| $K \mathrm{O}^2$ | complex anti-linear self-adjoint |
| $K \mathrm{O}^3$ | quaternionic anti-self-adjoint |
| $K \mathrm{O}^4$ | quaternionic |
| $K \mathrm{O}^5$ | quaternionic self-adjoint |
| $K \mathrm{O}^6$ | complex anti-linear anti-self-adjoint |
| $K \mathrm{O}^7$ | real anti-self-adjoint, |

except that, in the cases of 

* $K \mathrm{U}^n$ with $n = 1 \,mod\, 2$ 

* $K\mathrm{O}^n$ with $n = 1 \,mod\, 4$, 

the given space of Fredholm operators is actually the disjoint union with two contractible components of $K \mathrm{U}^n$ or $K\mathrm{O}^n$, respectively. To discard these spurious contractible components 

* read "self-adjoint" in the above tables as short for:

  "self-adjoint with essential spectrum both positive and negative".


#### In terms of graded Fredholm operators
 {#SummaryInTermsOfGradedFredholmOperators}

Equivalently, the classifying spaces for topological K-theory in its various degrees (including those contractible components) are those of graded self-adjoint complex Fredholm operators (Rem. \ref{TheSpaceOfGradedFredholmOperators}) that in addition commute with some *[PCT quantum symmetries](Wigner+theorem#PCTQuantumSymmetries)* from this list:

1. $\widehat{P}$ an odd-graded complex [[linear operator]] with $P^2 = \pm id$ (enforcing self-adjointness),

1. $\widehat{T}$ an even complex [[anti-linear operator]] with $\widehat{T}^2 = \pm id$ (a [[real structure]] or [[quaternionic structure]], respectively),

1. $\widehat{C}$ an odd complex [[anti-linear operator]] with $\widehat{C}^2 = \pm id$,

according to the following table, where 
$$
  G 
   \;\subset\;
  \underset{
    \{\mathrm{e}, T\}
  }{
    \underbrace{
      \mathbb{Z}^{t}_2
    }
  }
  \times
  \underset{
    \{\mathrm{e}, C\}
  }{
    \underbrace{
      \mathbb{Z}^{c}_2
    }
  }
$$
is the [[subgroup]] of the [[Klein 4-group]] which has generators $T$, $C$ (with product $P \coloneqq T C$) depending on whether commutation with $\widehat{T}$, $\widehat{C}$ or $\widehat{P} = \widehat{T}\widehat{C}$ appears as a constraint, respectively:

\begin{imagefromfile}
    "file_name": "QSfixedFredholms-251106.png",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

Here the group $QS$ of "[graded quantum symmetries](Wigner+theorem#PCTQuantumSymmetryDefinitionAndClassification)" is the [[semidirect product]] 

\[
  QS
  \;\coloneqq\;
  \tfrac{
    \mathrm{U}(\mathscr{H})^2
  }{  
    \mathrm{U}(1)
  }  
  \rtimes 
  \big(
    \mathbb{Z}_2^c \times \mathbb{Z}_2^t
  \big)
  \,.
\]

of

* the *graded* version of the stable [[projective unitary group]] [[PU(ℋ)]] (with the [[norm topology]]) 

with 

* the group generated by $T$ and $C$ acting by [[complex conjugation]] and in addition by swapping of the two Hilbert space summands, respectively.

Hence a lift $\widehat{(-)}$ of $T$ or $C$ or $P = T C$ to this group is represented by an (anti-)linear operator $\widehat{T}$ or $\widehat{C}$ or $\widehat{P}$, respectively, and homomorphy of the lift requires that $\widehat{T}^2, \widehat{C}^2 \in \{\pm 1\}$. Asking the graded Fredholm operators to commute with such lifts $\widehat{G}$ of subgroups $G \subset \mathbb{Z}_2^t \times \mathbb{Z}_2^c$ is equivalent, by the above discussion, to one of the ten constrains that lead to the 10 possible classifying spaces for K-theory, as shown in the above table.

Tables of related or analogous structures are well-known in the discussion of the "[[10-fold way]]" of [[topological phases of matter]] (cf. [Schnyder, Ryu, Furusaki & Ludwig 2008 Table 1](K-theory+classification+of+topological+phases+of+matter#SchnyderRyuFurusakiLudwig2008), [Kitaev 2009 Table 1](K-theory+classification+of+topological+phases+of+matter), [Freed & Moore 2013 Prop. B.4 & 6.4](K-theory+classification+of+topological+phases+of+matter#FreedMoore13)), which follow the [classication of PCT quantum symmetries](Wigner+theorem#TenFoldWayOfPCTQuantumSymmetries) (see there); the concrete relation to the Atiyah-Jänich theorem as per the above table was made more explicit by [Sati & Schreiber 2023 around Table 3](#SatiSchreiber2023).

\linebreak




## Examples

\begin{example}
  For discussion of the [[basic complex line bundle on the 2-sphere]] realized as a Fredholm index bundle see [there](basic+complex+line+bundle+on+the+2-sphere#AsAFredholmIndexBundle). 
\end{example}


## References

The original articles:

* {#Jänich65} [[Klaus Jänich]]: *Vektorraumbündel und der Raum der Fredholm-Operatoren*, Mathematische Annalen **161** (1965) 129–142 &lbrack;[doi:10.1007/BF01360851](https://doi.org/10.1007/BF01360851)&rbrack;

* {#Atiyah67}  [[Michael Atiyah]], Thm. A.1 in: *K-theory*, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

* {#Atiyah69} [[Michael Atiyah]], §2 in: *Algebraic Topology and Operators in Hilbert Space*, in: *Lectures in Modern Analysis and Applications I*, Lecture Notes in Mathematics **103**, Springer (1969) 101-121 &lbrack;[doi:10.1007/BFb0099987](https://doi.org/10.1007/BFb0099987), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/atiyah002.pdf), [[Atiyah-AlgTopAndOperators.pdf:file]]&rbrack;


Generalization to general degree and to [[KO-theory]]/[[KSp-theory]]:

* {#AtiyahSinger1969} [[Michael F. Atiyah]], [[Isadore M. Singer]]: *Index theory for skew-adjoint Fredholm operators*, Publications Mathématiques de l'IHÉS **37** (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [numdam:PMIHES_1969__37__5_0](https://www.numdam.org/item/PMIHES_1969__37__5_0), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/askew.pdf)&rbrack;

* {#Karoubi1970} [[Max Karoubi]]: *Espaces Classifiants en K-Théorie*, Trans. Amer. Math. Soc. **147** (1970) 75-115 &lbrack;[doi:10.2307/1995218](https://doi.org/10.2307/1995218), [jstor:1995218](https://www.jstor.org/stable/1995218), Engl. transl: [[Karoubi-EspacesClassifiants-English-251105.pdf:file]]&rbrack;


In monographs:

* {#Karoubi78} [[Max Karoubi]], §I.7.10 in: _K-Theory -- An Introduction_, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;
  > (related discussion)

Lecture notes:

* {#Sheth} Arshay Sheth: *The Atiyah-Jänich Theorem* &lbrack;[pdf](https://warwick.ac.uk/fac/sci/maths/people/staff/sheth/report_talk12_arshaysheth.pdf), [[Sheth-AtiyahJanich.pdf:file]]&rbrack;


As the basis of a definition of [[twisted K-theory]] and [[equivariant K-theory]] and [[twisted equivariant K-theory]]:

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;

See also:

* [[Byungdo Park]]: *The Atiyah-Jänich theorem and its twisted refinement -- An introduction to category theory for freshmen*, talk notes (2018) &lbrack;[pdf](https://byungdo.github.io/slides/2018-03-13_incheonU_printerfriendly.pdf), [[Park-AJTheorem.pdf:file]]&rbrack;

Further development:

* Kamran Sharifi: *Atiyah-Jänich theorem for  $\sigma$-$C^\ast$-algebras* &lbrack;[arXiv:1612.03287](https://arxiv.org/abs/1612.03287)&rbrack;

Formulation in the context of the [[10-fold way]] of [[quantum symmetries]] and the [[K-theory classification of topological phases of matter]]:

* {#SatiSchreiber23} [[Hisham Sati]], [[Urs Schreiber]], §2.2 in: *[[schreiber:Anyonic topological order in TED K-theory]]*, Reviews in Mathematical Physics **35** 03 (2023) 2350001 \[<a href="https://doi.org/10.1142/S0129055X23500010">doi:10.1142/S0129055X23500010</a>, [arXiv:2206.13563](https://arxiv.org/abs/2206.13563)\]


[[!redirects Atiyah-Janich theorem]]
[[!redirects Atiyah-Jaenich theorem]]
