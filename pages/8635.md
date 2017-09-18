
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _localization of a module_ is the result of application of an [[additive functor|additive]] [[localization functor]] on a [[category of modules]] over some [[ring]] $R$.

When $R$ is a [[commutative ring]] of functions, and under the [interpretation of modules as generalized vector bundles](module#RelationToVectorBundlesInIntroduction) the _localization_ of a module corresponds to the restriction of the bundle to a subspace of its base space.

## Definition

### For modules over rings

For $R$ a (possibly noncommutative) unital ring, let $\mathcal{A} = R$[[Mod]] be the [[category]] $R$-[[modules]]. Here $R$ may be the [[structure sheaf]] of some [[ringed topos]] and accordingly the modules may be [[sheaves of modules]].

Consider a [[reflective localization]] functor 

$$
  Q^* = Q^*_\Sigma \colon \mathcal{A}\to \Sigma^{-1}\mathcal{A}
$$ 

with [[right adjoint]] $Q_*$. The application of this functor to a [[module]] $M\in \mathcal{A}$ is some object $Q^*(M)$ in the localized category $\Sigma^{-1}\mathcal{A}$, which is up to isomorphism determined by its image $Q_* Q^*(M)$. 

The __localization map__ is the component of the [[unit of an adjunction|unit of the adjunction]] (usually denoted by $i$, $j$ or $\iota$ in this setup) $\iota_M : M\to Q_* Q^*(M)$.

Depending on an author or a context, we say that a (reflective) localization functor of category of modules is __flat__ if either $Q^*$ is also left [[exact functor]], or more strongly that the composed endofunctor $Q_* Q^*$ is exact. For example, [[Gabriel localization]] is flat in the first, weak sense, and left or right Ore localization is flat in the second, stronger, sense. 

### For chain complexes

... Greenlees-May duality...

### For spectra ($\mathbb{S}$-modules)
 {#ForSpectra}


+-- {: .num_prop}
###### Claim

Suppose that $L \colon Spectra \to Spectra$ is a [[smashing localization]] given by [[smash product]] with some [[spectrum]] $T$. Write $F$ for the [[homotopy fiber]]

$$
  F \longrightarrow \mathbb{S} \longrightarrow T
  \,.
$$

Then there is a [[fracture diagram]] of operations

$$
  \array{
    T \wedge (-) && \longleftarrow  &&  [T,-]
    \\
    & \nwarrow && \swarrow
    \\
    && \mathbb{S}
    \\
    & \swarrow & & \nwarrow
    \\
    [F,-] && \longleftarrow && F \wedge (-)
  }
$$

where $[F,-]$ and $T \wedge (-) \colon Spectr \to Spectra$ are [[idempotent (∞,1)-monads]] and $[T,-]$, $[F,-]$ are idempotent $\infty$-comonad, the diagonals are [[homotopy fiber sequences]].

=--

([[Charles Rezk]], [MO comment,August 2014](http://mathoverflow.net/a/178316/381))

+-- {: .num_example}
###### Example

For $T = S \mathbb{Z}[p^{-1}]$ the [[Moore spectrum]] of the [[integers]] [[localization of a ring|localized away from]] $p$, then 

$$
  F = \Sigma^{-1} S (\mathbb{Z}[p^{-1}]/\mathbb{Z})
   \to 
  \mathbb{S}
   \to
  S \mathbb{Z}[p^{-1}]
$$

and hence

* $\Sigma^{-1} S (\mathbb{Z}[p^{-1}]/\mathbb{Z}) \wedge (-)$ is $p$-[[torsion approximation]];

* $[\Sigma^{-1} S (\mathbb{Z}[p^{-1}]/\mathbb{Z}),-]$ is $p$-[[completion of a module|completion]];

* $S \mathbb{Z}[p^{-1}] \wedge (-)$ is localization away from $p$ ($p$-[[rationalization]])

* $[T,-]$ is forming $p$-[[adic residual]].

$$
  \array{
    &&  localization\;away\;from\;\mathfrak{a} && \stackrel{}{\longrightarrow} && \mathfrak{a}\;adic\;residual
    \\
    & \nearrow & & \searrow & & \nearrow && \searrow
    \\
    && && X &&  &&  
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow
    \\
    && formal\;completion\;at\;\mathfrak{a}\; && \longrightarrow && \mathfrak{a}\;torsion\;approximation
  }
  \,,
$$

=--

With ([Bousfield 79, prop.2.5](#Bousfield79))

### For $\infty$-modules over $E_\infty$-rings

Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 

+-- {: .num_defn #LocalInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-local module_ if for every $\mathfrak{a}$-[[torsion module]] $T$ (def. \ref{TorsionInfinityModule}), the [[derived hom space]]

$$
 Hom_A(T,N) \simeq \ast
$$

is contractible.

=--

([Lurie "Completions", def. 4.1.9](#LurieCompletions)).

+-- {: .num_prop #LocalizationAwayByColimit}
###### Proposition

For $\mathfrak{a} = (a)$ generated from a single element, then the [localization of an (∞,1)-ring](localization+of+a+commutative+ring#ForEInfinityRings)-map $A \to A[a^{-1}]$ is given by the [[(∞,1)-colimit]] over the sequence of right-multiplication with $a$

$$
  A[a^{-1}]
  \simeq
  \underset{\rightarrow}{\lim}
  (
    A \stackrel{\cdot a}{\longrightarrow} A
    \stackrel{\cdot a}{\longrightarrow} A
    \stackrel{\cdot a}{\longrightarrow}  \cdots
  )
  \,.
$$

=--

([Lurie "Completions", remark 4.1.11](#LurieCompletions))

+-- {: .num_prop}
###### Proposition

The [[full sub-(∞,1)-category]]


$$
  A Mod_{\mathfrak{a}loc}
  \hookrightarrow
  A Mod
$$

of [[∞-modules]] [[localization of a module|local]] away from $\mathfrak{a}$ is [[reflective sub-(∞,1)-category|reflective]]. The reflector


$$
  \Pi_{\mathfrak{a}dR} \colon A Mod \longrightarrow A Mod_{\mathfrak{a}loc}
$$

is called _localization_.

=--

+-- {: .num_prop}
###### Proposition

There is a [[natural transformation|natural]] [[homotopy fiber sequence]]

$$
  &#643;_{\mathfrak{a}} \longrightarrow id \longrightarrow &#643;_{\mathfrak{a}dR}
$$

relating $\mathfrak{a}$-[[torsion approximation]] on the left with $\mathfrak{a}$-localization on the right.

=--

## Properties

### Eilenberg-Watts theorem

By the [[Eilenberg-Watts theorem]], if $\mathcal{A}= R$[[Mod]] then the localization of a module

$$
  Q^*(M) = Q^*(R)\otimes_R M
$$

is given by forming the [[tensor product of modules]] with the localizatin of the ring $R$, regarded as a module over itself.

If the localization is a left [[Ore localization]] or [[commutative localization]] at a set $S\subset R$ then $Q^*(R) = S^{-1} R$ is the [[localization of a ring|localization of the ring]] itself 
and hence in this case the localization of the module 

$$
  Q^*(M) = S^{-1} R\otimes_R M
$$

is given by [[extension of scalars]] along the localization map $R \to S^{-1}R$ of the ring itself.

In these cases there are also direct constructions of $Q^*(M)$ (not using to $Q^*(R)$) which give an isomorphic result, also denoted by $S^{-1}M$. 

### Relation with torsion approximation and completion

[[!include arithmetic cohesion -- table]]

## Related concepts

* [[localization of an abelian group]]

* [[localization of a ring]], [[Ore localization]], [[Gabriel localization]], [[Cohn localization]]

* [[localization of a space]] (and of a [[spectrum]])

* [[localization of a category]] (= localization functor)

* [[locally free module]]

## Literature

Standard discussion over [[commutative rings]] is for instance in 

* {#Gathmann} Andreas Gathmann, _Localization_ ([[GathmannLocalization.pdf:file]])

Discussion in the general case of [[noncommutative geometry]] is in

* [[Z. Škoda]], _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276)

Discussion in the context of [[spectra]] originates in

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, Vol 304, Springer 1972

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_ , Topology vol 18 (1979) ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

* {#Sullivan05} [[Dennis Sullivan]], _Geometric topology: localization, periodicity and Galois symmetry_, volume 8 of K- Monographs in Mathematics. Springer, Dordrecht, 2005. The 1970 MIT notes, Edited and with a preface
by [[Andrew Ranicki]] ([pdf](http://www.maths.ed.ac.uk/~aar/books/gtop.pdf)) 

Discussion in the context of [[higher algebra]] is in 


* {#LurieCompletions} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

[[!redirects localizations of a module]]
[[!redirects localizations of modules]]
