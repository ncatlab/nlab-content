
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Content`s#
* table of contents
{:toc}

## Definition

### Core of a ring

\begin{definition}\label{CoreOfARing}
**(core of a ring)** \linebreak
For $R$ a [[unital ring|unital]] [[commutative ring]], its **[[core of a ring|core]]** is the following [[subobject|sub-ring]] of the [[tensor product of abelian groups]] $R \otimes_{{}_{\mathbb{Z}}} R$:

$$
  c R
  \;\coloneqq\;
  \Big\{
    \,
    r \in R 
    \,\left\vert\,
    1 \otimes r \,=\, r \otimes 1 
    \;\in\; R \otimes_{{}_{\mathbb{Z}}} R 
    \right.
    \,
  \Big\}
$$ 
\end{definition}

([Bousfield & Kan 1972, Sec. 1](#BousfieldKan72))

\begin{remark}\label{CoreAsEqualizerAndAsRegularImage}
**(core as [[equalizer]] and as [[regular image]])** \linebreak
In [[category theory|category-theoretic]] terminology, Def. \ref{CoreOfARing} describes the [[equalizer]] ([Bousfield 1979, 6.4](#Bousfield79))

$$
  c R 
    \xrightarrow{\;equ\;}
  R 
    \overset{\phantom{AAAAAA}}\rightrightarrows
  R \otimes_{{}_{\mathbb{Z}}} R
  \,,
$$

where the top [[morphism]] is

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
    \xrightarrow{\;id \otimes e\;} 
  R \otimes R
  \,,
$$

with

\[
  \label{UniqueRingHomomorphismFromTheIntegers}
  \array{
    \mathbb{Z}
    &\xrightarrow{ \;e\; } &
    R
    \\
    1 &\mapsto& 1
  }
\]

denoting the unique [[ring homomorphism]] form the [[commutative ring]] of [[integers]], which is the [[initial object]] in [[CommutativeRings]].

Observing (by [this Prop.](CRing#CoproductIsTensorProduct))
that the [[tensor product of abelian groups]] $R \otimes_{{}_{\mathbb{Z}}} R$ equipped with its canonically induced [[commutative ring]] [[mathematical structure|structure]] is the [[coproduct]] in [[CommutativeRings]]

$$
  R \otimes_{{}_{\mathbb{Z}}} R
    \;\simeq\;
  R \sqcup R
$$

this means equivalently that the core is the [[equalizer]] of the two [[coprojections]] into the [[coproduct]]:

$$
  c R 
    \xrightarrow{\;equ\;}
  R 
    \overset{\phantom{AAAAAA}}\rightrightarrows
  R \sqcup R  
    \;\simeq\;
  R \underset{\mathbb{Z}}{\coprod} R
  \,,
$$

hence -- since $\mathbb{Z}$ is the [[initial object]] in [[CommutativeRings]] -- into the [[cofiber coproduct]] of $\mathbb{Z} \xrightarrow{e} R$ (eq:UniqueRingHomomorphismFromTheIntegers) with itself.

In this form, the core is manifestly ([here](image#AsEqualizer)) the *[[regular image]]* of the initial morphism $\mathbb{Z} \xrightarrow{e} R$:

$$
  c R 
    \;\simeq\;
  Im_{reg}
  \left( 
    \mathbb{Z} \xrightarrow{e} R 
  \right)
    \xhookrightarrow{\phantom{AA}}
  R
  \,,
$$

hence the smallest [[regular monomorphism]] into $R$ in the [[category]] of [[CommutativeRings]].
\end{remark}

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

Hence the terminal morphism $Spec(R) \to Spec(\mathbb{Z})$ induces the corresponding [[Cech groupoid]] [[internal groupoid|internal]] to $CRing^{op}$

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

\end{remark}




### Solid rings

\begin{definition}\label{SolidRing}
**(solid rings)** \linebreak
A [[commutative ring]] $R$ which is [[isomorphism|isomorphic]] to its [[core of a ring|core]] (Def. \ref{CoreOfARing}), $R \,\simeq\, c R$ is called a **solid ring**.
\end{definition}
([Bousfield-Kan 72, &#167;1, def. 2.1](#BousfieldKan72), [Bousfield 79, 6.4](#Bousfield79))

\begin{proposition}
  A [[commutative ring]] $R$ is solid (Def. \ref{SolidRing}) iff its [[multiplication]] morphism is an [[isomorphism]]:

$$
  R\; \text{is solid}
  \;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;
  R \otimes_{{}_{\mathbb{Z}}} R
    \underoverset
      {\simeq}
      {\;(-) \cdot (-)\;}
      {\longrightarrow}
  R
  \,.
$$
\end{proposition}
([Bousfield & Kan 1972](#BousfieldKan72))



## Classification

+-- {: .num_theorem}
###### Theorem

The following is the complete list of solid rings (Def. \ref{SolidRing}) up to [[isomorphism]]:

1. The [[localization of a ring|localization]] of the ring of [[integers]] at a [[subsetset]] $Pr$ of [[prime numbers]]

   $$
     \mathbb{Z}\big[Pr^{-1}\big]
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

\begin{prop}\label{CoresAreSolid}
**(cores are solid)** \linebreak
The core (Def. \ref{CoreOfARing}) of any ring $R$ is solid (Def. \ref{SolidRing}):
$$
  c c R 
    \;\simeq\; 
  c R
  \,.
$$
\end{prop}
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
