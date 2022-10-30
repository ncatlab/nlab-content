
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _excisive (∞,1)-functor_ $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ is one which sends [[homotopy pushout]] sqaures to [[homotopy pullback]] squares. If $\mathcal{C}$ is [[pointed object|pointed]] [[finite homotopy types]] and $\mathcal{D}$ is [[spectra]], then this condition is the [[axiom]] of [[excision]] in [[generalized (Eilenberg-Steenrod) cohomology|generalized homotopy]], whence the name.

Moreover, if here $\mathcal{D}$ is instead [[∞Grpd]] (i.e. [[homotopy types]]), or more generally any [[(∞,1)-topos]] $\mathbf{H}$, then excisive functors that send the point to the point (up to equivalence) are still equivalent to [[spectra]] ([[spectrum objects]]) -- essentially by the [[Brown representability theorem]] -- and those without restriction are equivalent to [[parameterized spectra]], hence form the [[tangent (∞,1)-topos]] $T \mathbf{H}$.

As such, excisive functors are the lowest nontrivial stage in the [[Goodwillie-Taylor tower]] that approximates the [[classifying (∞,1)-topos]] $\\mathbf{H}[X_\bullet]$ for [[pointed objects]]. The higher stages of this tower are given by the [[n-excisive (∞,1)-functors]].

## Definition

+-- {: .num_defn #ExcisiveFunctor}
###### Definition

An [[(∞,1)-functor]] $F \colon \mathcal{C} \longrightarrow \mathcal{D}$ out of an [[(∞,1)-category]] with [[finite (∞,1)-colimits]] is **excisive** if it takes [[(∞,1)-pushout]] squares in $\mathcal{C}$ to [[(∞,1)-pullback]] squares $\mathcal{D}$. 

This is the $n=1$ case of the concept [[n-excisive (∞,1)-functor]].

=--

([HigherAlg, def. 1.4.2.1.](#HigherAlg))

## Properties

+-- {: .num_defn #ClassifyingToposForPointedObjects}
###### Definition

Write $\infty Grpd_{fin}$ is the [[(∞,1)-category]] of [[finite homotopy types]].
For $\mathbf{H}$ a given [[base (∞,1)-topos]], write 

$$
  \begin{aligned}
    \mathbf{H}[X_\ast]
    & \simeq
    [\infty Grpd_{fin}^{\ast/}, \mathbf{H}]
    \\
    & \simeq
    PSh((\infty Grpd_{fin}^{\ast/})^{op}, \mathbf{H})
  \end{aligned}
$$

for the [[classifying (∞,1)-topos]] (over $\mathbf{H}$) for [[pointed objects]].

=--

For the moment we focus on properties of the case of excisive functors $\mathcal{C} \to \mathcal{D}$ for $\mathcal{C} = \infty Grpd_{fin}^{\ast/}$ and $\mathcal{D} = \mathbf{H}$, hence on 

$$
  Exc(\infty Grpd_{fin}^{\ast/}, \mathbf{H}) \simeq T \mathbf{H} \hookrightarrow \mathbf{H}[X_\ast]
  \,.
$$


### Reflection and excisive approximation



+-- {: .num_defn #P1}
###### Definition

Write

$$
  T_1 \colon \mathbf{H}[X_\ast] \longrightarrow \mathbf{H}[X_\ast]
$$

for the functor given by

$$
  E \mapsto \Omega_{E(\ast)} E(\Sigma(-))
  \,.
$$

Write

$$
  P_1 \coloneqq \underset{\longrightarrow}{\lim}_{n} T_n^{n}
$$

for the [[homotopy colimit]] of the iterations of this functor, with respect to the canonical comparison map.

=--

Unwinding the definition and using that [[suspension]] is equivalently the [join with the 0-sphere](join%20of%20topological%20spaces#JoinWith0Sphere), this is indeed the functor of the same name in  ([Goodwillie 91, p. 657 (13 of 67)](#Goodwillie91)).

+-- {: .num_theorem #PnLocalizes}
###### Theorem

The inclusion of excisive functors into $\mathbf{H}[X_*]$ is a [[reflective sub-(∞,1)-category]] with reflector given by $P_1$ from def. \ref{P1}:

$$
  T \mathbf{H} 
   \stackrel{\overset{P_1}{\longleftarrow}}{\hookrightarrow}
  \mathbf{H}[X_\ast]
$$

=--

This is due (in the generality of _[n-excisive functor -- n-Excisive Approximation and reflection](https://ncatlab.org/nlab/show/n-excisive+functor#nExcisiveApproximation)_) to ([Goodwillie 91, theorem 1.8](#Goodwillie91)). See also ([Lurie, theorem 6.1.1.10, construction 6.1.1.27](#HigherAlg)).



### Characterization via a generic stable object
 {#CharacterizationViaAGenericStableObject}

The following perspective is being highlighted by [Anel-Finster-Joyal](#AnelFinsterJoyal).

+-- {: .num_defn #PointedPower}
###### Definition

For $X_\ast$ an object in an [[(∞,1)-category]] $\mathcal{C}$ with [[finite (∞,1)-limits]], and for $S_\ast \in \infty Grpd_{fin}^{\ast/}$ a pointed [[finite ∞-groupoid]], then the _pointed power_ 

$$
  X_\ast^{S_\ast} \in \mathcal{C}
$$ 

is the object which is the image of $S$ under the essentially unique [[(∞,1)-functor]]

$$
  (\infty Grpd_{fin}^{\ast/})^\op \longrightarrow \mathcal{C}
$$

which preserves [[finite (∞,1)-limits]] and sends $S^0 \leftarrow \ast$ to $X_\ast \to \ast$.

=--


+-- {: .num_prop }
###### Proposition

Excisive functors $\infty Grpd_{fin}^{\ast/} \longrightarrow \mathbf{H}$, def. \ref{ExcisiveFunctor}, are the [[localization of an (∞,1)-category|localization]] of $\mathbf{H}[X_\ast]$, def. \ref{ClassifyingToposForPointedObjects}, at the set of morphisms 

$$
  \left\{
    \Sigma \Omega (X_\ast^{S_\ast}) \longrightarrow X_\ast^{S_\ast}
  \right\}_{S \in \infty Grpd_{fin}^{\ast/}}
  \,,
$$

(where $X_{\ast}^{S_\ast}$ is the pointed power, def. \ref{PointedPower}, of the generic pointed object $X_\ast \in \mathbf{H}[X_\ast]$ with $S_\ast$):

$$
  T \mathbf{H}\simeq \mathbf{H}[X_\ast][ (\Sigma \Omega X_\ast^\bullet \to X_\ast^\bullet)^{-1} ]
  \,.
$$

In other words, the [[parameterized spectra]] are those objects in $\mathbf{H}[X_\ast]$ which regard each finite pointed power of the generic pointed object $X_\ast$ as a [[stable homotopy type]].

=--

+-- {: .proof}
###### Proof

For $K \in \infty Grpd_{fin}^{\ast/}$, write $R(K) \in (\infty Grpd_{fin}^{\ast/})^{op} \hookrightarrow \mathbf{H}[X_\ast]$ for its [[formal dual]] under [[(∞,1)-Yoneda embedding]]. Since the [[(∞,1)-Yoneda embedding]] preserves [[(∞,1)-limits]], we have

$$
  R(K)^S \simeq R(S \cdot K)
  \,.
$$

Observe that the generic pointed object in $\mathbf{H}[X_\ast]$ is that [[representable functor|represented]] by the [[0-sphere]]:

$$
  X_\ast = R(S^0)
  \,.
$$

Hence

$$
  X_\ast^S \simeq R(S)
  \,.
$$


Now using the [[(∞,1)-Yoneda lemma]] we have  for each $E \in \mathbf{H}[X_\ast]$ that

$$
  \begin{aligned}
    Hom( \Sigma \Omega R(K), E )
    &\simeq
    \Omega_{E(\ast)} Hom(\Omega R(K),E)
    \\
    & \simeq 
    \Omega_{E(\ast)} Hom( R(\Sigma K), E )
    \\
    & \simeq
    \Omega_{E(\ast)} E(\Sigma K)
  \end{aligned}
  \,.
$$

Hence for all $K \in \infty Grpd_{fin}^{\ast/}$

$$
  \begin{aligned}
    Hom(\Sigma \Omega R(K) \to R(K), E)
    & \simeq
    ( E(K) \longrightarrow  \Omega(\Sigma K) ) 
    \\
    & =
    (E \to T_1 E)(K)
  \end{aligned}
  \,,
$$

where in the last line we observe that the expression is that for 
the comparison map in def. \ref{P1}.

This means that the [[local objects]] are precisely those $E$ for which the morphism

$$
  E \longrightarrow T_1 E
$$

from def. \ref{P1} is an equivalence. With this the statement follows from theorem \ref{PnLocalizes}.

=--

## Examples

### Spectrum objects
 {#SpectrumObjects}

Write $\infty Grpd_{fin}$ for the [[(∞,1)-category]] of [[finite homotopy types]], hence those freely generated by [[finite (∞,1)-colimits]] from the point. Write $\infty Grpd_{fin}^{\ast/}$ for the [[pointed object|pointed]] finite homotopy types.


+-- {: .num_defn }
###### Proposition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-limits]]. Then **[[spectrum object]]** in $\mathcal{C}$ are equivalently  [[reduced (infinity,1)-functor|reduced]] [[excisive (∞,1)-functor]] of the form

$$
  \infty Grpd_{fin}^{\ast/} \longrightarrow \mathcal{C}
  \,.
$$

=--

(Sometimes, e.g. in [Lurie, def. 1.4.2.8](#HigherAlg), this is taken as the very definition of spectrum objects).

+-- {: .proof}
###### Proof

Let $F$ be a reduced excisive functor $E$.

For each $n \in \mathbb{N}$, write $S^n \in \infty Grpd_{fin}^{\ast/}$ for the [[n-sphere]] and write $E_{n} \coloneqq E(S^n)$. We have the homotopy pushout squares

$$
  \array{
    S^n &\longrightarrow& \ast
    \\
    \downarrow & & \downarrow
    \\
    \ast &\longrightarrow& S^{n+1}
  }
$$ 

and since $E$ sends them to homotopy pullbacks with the point going to the point, this gives equivalences

$$
  E_n \stackrel{\simeq}{\longrightarrow} \Omega E_{n+1}
  \,.
$$

If this were all the data in $E$, it would manifestly exhibit $E_\bullet$ as being equivalently an [[Omega spectrum]]. And indeed this is all the data in $E$: 

Since [[finite homotopy types]] are given by a finite number of sphere attachments, hence a finite number of [[homotopy pushouts]] with $n$-spheres, it follows that the value of $E$ on any pointed finite homotopy type $X$ is the [[smash product]] $\Omega^\infty(X \wedge E_\bullet)$, hence the [[generalized homology]] $E(X)$ (see also [Lurie, remark 1.4.3.3](#HigherAlg)). That this assignment still sends all possible homotopy pushouts to homotopy pullback is then the excision axiom for the [[generalized homology]] theory thus given, and it does hold due to the [[Brown representability theorem]].

=--

The same proof, with the point going to any space $E(\ast)$, gives that $E$ is a [[parameterized spectrum]] over $E(\ast)$.

### Excisive approximation of reduced functors

Let $\mathcal{C}$ have finite colimits and a terminal object and let $\mathcal{D}$ be differentiable.

+-- {: .num_prop}
###### Proposition

The excisive approximation of a [[reduced functor]] $F \colon \mathcal{C} \to \mathcal{D}$ is the [[(infinity,1)-colimit]]

$$
  P_1 F 
    \simeq 
  \underset{\longrightarrow_{\mathrlap{k}}}{\lim} 
  ( \Omega^k \circ F \circ \Sigma^k)
$$

(where $\Omega$ and $\Sigma$ denote [[looping]] and [[suspension]] in $\mathcal{D}$ and in $\mathcal{C}$, respectively).

=--

([Lurie, example 6.1.1.28](#HigherAlg))


## Related concepts

* [[exact (∞,1)-functor]]

* [[n-excisive (∞,1)-functor]]

* [[spectrum object]]

## References

The notion of [[n-excisive functors]] was introduced in 

* {#Goodwillie91} [[Thomas Goodwillie]], _Calculus II, Analytic functors_, K-Theory 5 (1991/92), no. 4, 295-332

The [[Taylor tower]] formed by $n$-excisive functors was then studied in

* {#Goodwillie03} [[Thomas Goodwillie]], _Calculus III: Taylor Series_, Geom. Topol. 7(2003) 645-711 ([arXiv:math/0310481](http://arxiv.org/abs/math/0310481))
 
A discussion in the general abstract context of [[(∞,1)-category theory]] is in  

* {#HigherAlg} [[Jacob Lurie]], section 6.1.1 of _[[Higher Algebra]]_
 
Review includes

* {#Harpaz2013} [[Yonatan Harpaz]], section 5 of _Introduction to stable $\infty$-categories_, October 2013 ([[HarpazStableInfinityCategory2013.pdf:file]])
   
Discussion in terms of [[stable homotopy types]] is due to 

* {#AnelFinsterJoyal} [[Mathieu Anel]], [[Eric Finster]], [[André Joyal]], in preparation

[[!redirects excisive (∞,1)-functors]]

[[!redirects excisive (infinity,1)-functor]]
[[!redirects excisive (infinity,1)-functors]]

[[!redirects excisive functor]]
[[!redirects excisive functors]]

