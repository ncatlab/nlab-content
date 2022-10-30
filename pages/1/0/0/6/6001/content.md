
## Idea

The concept of _$\Omega$-spectra_ is one several [[equivalence of (∞,1)-categories|equivalent]] [[presentable (∞,1)-category|presentation]] of the [[stable (∞,1)-category of spectra]]. 

## Definition

With $\Omega$ the notation for the [[loop space]] construction (whence the name),an $\Omega$-spectrum is a sequence $E_\bullet = (E_n)_{n \in \mathbb{N}}$ of [[pointed object|pointed]] [[∞-groupoids]] ([[homotopy types]]) equipped for each $n \in \mathbb{N}$ with an [[equivalence of ∞-groupoids]]

$$
  E_n \stackrel{\simeq}{\longrightarrow} \Omega E_{n+1}
  \,.
$$ 

Remark: In terms of [[model category]] [[presentable (∞,1)-category|presentation]] one may also consider sequences of [[topological spaces]] equipped with [[homeomorphisms]] $E_n \longrightarrow \Omega E_{n+1}$  See at _[[spectrum]]_ the section <a href="http://nlab.mathforge.org/nlab/show/spectrum#OmegaSpectrum">Omega-spectra</a>.


## Presentation by localization of the generic pointed object

> under construction

+-- {: .num_defn }
###### Definition

Write $\infty Grpd_{fin}$ is the [[(∞,1)-category]] of [[finite homotopy types]].
For $\mathbf{H}$ a given [[base (∞,1)-topos]], write 

$$
  \mathbf{H}[X_\ast]
  \simeq
  [(\infty Grpd_{fin}^{\ast/})^\op, \mathbf{H}]
$$

for the [[classifying (∞,1)-topos]] for [[pointed objects]].

=--

+-- {: .num_prop }
###### Proposition

Parameterized spectra are the [[localization of an (∞,1)-category|localization]] of $\mathbf{H}[X_\ast]$ at the set of morphisms 

$$
  \left\{
    \Sigma \Omega^{n+1} X_\ast \longrightarrow \Omega^n X_\ast
  \right\}_{n \in \mathbb{N}}
  \,.
$$

and at (...)

=--

+-- {: .proof}
###### Proof

For $K \in \infty Grpd_{fin}^{\ast/}$, write $R(K) \in (\infty Grpd_{fin}^{\ast/})^{op} \hookrightarrow \mathbf{H}[X_\ast]$ for its [[formal dual]] under [[(∞,1)-Yoneda embedding]]. Since the [[(∞,1)-Yoneda embedding]] preserves [[(∞,1)-limits]], we have

$$
  \Omega(R(K)) \simeq R(\Sigma K)
  \,.
$$

Now observe that $X_\bullet = R(S^0)$. Hence for $n \in \mathbb{N}$

$$
  \Omega^n X_\bullet \simeq R(S^n)
$$

is the formal dual of (the [[homotopy type]] of) the [[n-sphere]]

Using now the [[(∞,1)-Yoneda lemma]] we have  for each $E \in \mathbf{H}[X_\ast]$ that

$$
  \begin{aligned}
    Hom( \Sigma \Omega R(K), E )
    &\simeq
    \Omega_{E(\ast)} Hom(\Omega R(K),E)
    \\
    & \simeq 
    \Omega_{E(\ast)} Hom( R(\Sigma X), E )
    \\
    & \simeq
    \Omega_{E(\ast)} E(\Sigma X)
  \end{aligned}
$$

Hence

$$
  Hom(\Sigma \Omega R(K) \to R(K), E)
  \simeq
  ( E(K) \longrightarrow  \Omega(\Sigma K) ) 
  \,.
$$

Hence $K$ ranges $S^\bullet$, the condition for [[local objects]] is manifestly that for Omega-spectra. 

Now (...)

=--




[[!redirects Omega-spectra]]

[[!redirects Omega spectrum]]
[[!redirects Omega spectra]]

