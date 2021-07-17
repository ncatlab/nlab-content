
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #CoreOfARing}
###### Definition
**(core of a ring)**

For $R$ a [[commutative ring]], its **[[core of a ring|core]]** $c R$ is the [[regular image]] of the unique [[ring]] [[homomorphism]] $\mathbb{Z} \overset{e}{\longrightarrow} R$ from the [[integers]] (which are the [[initial object]] among [[CommutativeRings]]).  That is, it is the smallest [[regular monomorphism]] into $R$ in the [[category]] of [[CommutativeRings]].

By the general construction of [[regular images]] ([here](image#AsEqualizer)), this can be computed as the [[equalizer]] of the two inclusions from $R$ into the [[pushout]] $R\sqcup_{\mathbb{Z}} R$.  Since $\mathbb{Z}$ is [[initial object|initial]], this is just the [[coproduct]] $R\sqcup R$ in [[CommutativeRings]], which is the [[tensor product of abelian groups]] $R\otimes R$ equipped with its canonically induced commutative ring structure ([this Prop.](CRing#CoproductIsTensorProduct)).

Thus, a more explicit characterization of $c R$ is as the [[equalizer]] in

$$
  c R 
    \overset{equ}{\longrightarrow}
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,,
$$

where the top morphism is

$$
  R 
    \;\simeq\; 
  \mathbb{Z} \otimes R 
  \xrightarrow{e \otimes id} 
  R \otimes R
$$

and the bottom one is

$$
  R 
    \;\simeq\; 
  R \otimes \mathbb{Z}  
    \xrightarrow{id \otimes e} 
  R \otimes R
  \,.
$$

=--

\begin{definition}\label{SolidRing}
**(solid rings)** \linebreak
A [[commutative ring]] $R$ which is [[isomorphism|isomorphic]] to its [[core of a ring|core]] (Def. \ref{CoreOfARing}), $R \,\simeq\, c R$ is called a **solid ring**.
\end{definition}

([Bousfield-Kan 72, &#167;1, def. 2.1](#BousfieldKan72), [Bousfield 79, 6.4](#Bousfield79))

\begin{remark}\label{DualInterpretation}
**(geometric interpretation)** \linebreak
By [[duality between algebra and geometry]], we may think of the [[opposite category]] $CommutativeRings^{op}$ as that of [[affine scheme|affine]] [[arithmetic schemes]]. Here for $R \in CRing$ we write $Spec(R)$ for the same object, but regarded in $CRing^{op}$. 

So the [[initial object]] $\mathbb{Z}$ in [[CRing]] becomes the [[terminal object]] [[Spec(Z)]] in $CRing^{op}$, and so for every $R$ there is a unique morphism

$$
  Spec(R) \longrightarrow Spec(Z)
$$

in $CRing^{op}$, exhibiting every affine [[arithmetic scheme]] $Spec(R)$ as equipped with a map to the base scheme [[Spec(Z)]].

Since the [[coproduct]] in [[CRing]] is the [[tensor product]] of rings ([prop.](CRing#CoproductIsTensorProduct)), this is the dually the [[Cartesian product]] in $CRing^{op}$ and hence

$$
  Spec(R \otimes R) \simeq Spec(R) \times Spec(R)
$$

exhibits $R \otimes R$ as the ring of functions on $Spec(R) \times Spec(R)$. 

Hence the terminal morphism $Spec(R) \to Spec(\mathbb{Z})$ induced the corresponding [[Cech groupoid]] [[internal groupoid|internal]] to $CRing^{op}$

$$
  \array{
    Spec(R) \times Spec(R) \times Spec(R)
    \\
    \downarrow
    \\
    Spec(R) \times Spec(R)
    \\
    {}^{\mathllap{s}}\downarrow \uparrow \downarrow^{\mathrlap{t}}
    \\
    Spec(R)
  }
  \,.
$$

This exhibits $R \otimes R$ (the ring of functions on the scheme of morphisms of the Cech groupoid) as a [[commutative Hopf algebroid]] over $R$. 

Moreover, the arithmetic scheme of [[isomorphism classes]] of this groupoid is the [[coequalizer]] of the [[source]] and [[target]] morphisms

$$
  Spec(R) \times Spec(R)
   \underoverset
     {\underset{s}{\longrightarrow}}
     {\overset{t}{\longrightarrow}}
     {\phantom{AA}}
   Spec(R)
     \overset{coeq}{\longrightarrow}
   Spec(c R)
  \,,
$$

also called the _[[coimage]]_ of $Spec(R) \to Spec(\mathbb{Z})$. Since [[limits]] in the [[opposite category]] $CRing^{op}$ are equivaletly colimits in $CRing$, this means that the ring of functions on the scheme of isomorphism classes of the Cech groupoid is precisely the core $c R$ or $R$ according to def. \ref{CoreOfARing}.

This is morally the reason why for $E$ a [[homotopy commutative ring spectrum]] then the core $c \pi_0(E)$ of its underlying ordinary ring in degree 0 controls what the $E$-[[Adams spectral sequence]] converges to ([Bousfield 79, theorems 6.5, 6.6](#Bousfield79), see [here](Adams+spectral+sequence#ConvergenceStatements)), because the $E$-Adams spectral sequence computes [[E-nilpotent completion]] which is essentially the analog in [[higher algebra]] of the above story: namely the coimage ([(infinity,1)-image](infinity-image#ViaColimitOfCechNerve)) of $Spec(E) \to $ [[Spec(S)]] (see [here](Adams+spectral+sequence#DefinitionInHigherAlgebra)). 

=--



## Classification

+-- {: .num_theorem}
###### Theorem

The following is the complete list of solid rings (def. \ref{CoreOfARing}) up to [[isomorphism]]:

1. The [[localization of a ring|localization]] of the ring of [[integers]] at a set $J$ of [[prime numbers]]

   $$
     \mathbb{Z}[J^{-1}]
     \,;
   $$

1. the [[cyclic rings]]

   $$
     \mathbb{Z}/n\mathbb{Z}
   $$

   for $n \in \mathbb{N}$, $n \geq 2$;

1. the [[Cartesian product|product]] rings 

   $$
     \mathbb{Z}[J^{-1}]
       \times
     \mathbb{Z}/n\mathbb{Z}
     \,,
   $$

   for $n \geq 2$ such that each [[prime factor]] of $n$ is contained in the set of primes $J$;

1. the ring cores of product rings

   $$
     c(\mathbb{Z}[J^{-1}] \times \underset{p \in K}{\prod} \mathbb{Z}/p^{e(p)})
     \,,
   $$

   where $K \subset J$ are infinite sets of primes and $e(p)$ are positive natural numbers.

=--

([Bousfield-Kan 72, prop. 3.5](#BousfieldKan72), [Bousfield 79, p. 276](#Bousfield79))


## Properties

+-- {: .num_prop}
###### Proposition

The core of any ring $R$ is solid (def. \ref{CoreOfARing}):

$$
  c c R \simeq c R
  \,.
$$

=--

([Bousfield-Kan 72, prop. 2.2](#BousfieldKan72))

## Related concepts

* [[nilpotent completion of spectra]]

* [[Adams spectral sequence]]


## References

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], _The core of a ring_, Journal of Pure and Applied Algebra, Volume 2, Issue 1, April 1972, Pages 73-81 ([link](http://www.sciencedirect.com/science/article/pii/0022404972900230))



* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))

[[!redirects cores of rings]]

[[!redirects solid ring]]
[[!redirects solid rings]]
