
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[model category]]-theory, the _Bousfield-Friedlander theorem_ ([Bousfield-Friedlander 78, theorem A.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3](#Bousfield01)) states that if an [[endofunctor]] $Q \colon \mathcal{C} \to \mathcal{C}$ on a [[model category]] $\mathcal{C}$ behaves like an [[idempotent monad]] in an appropriate model category theoretic sense, then the [[left Bousfield localization]] [[model category]] structure of $\mathcal{C}$ at the $Q$-equivalences exists.

The original proof assumed that $\mathcal{C}$ is a [[proper model category]], but this condition turns out not to be necessary ([Stanculescu 08, theorem 1.1](#Stanculescu08)).

## Statement

+-- {: .num_defn #QuillenIdempotentMonad}
###### Definition

Let $\mathcal{C}$ be a [[proper model category]]. 
Say that **Quillen idempotent monad** on $\mathcal{C}$ is
 
1. an [[endofunctor]] 

   $Q \;\colon\;  \mathcal{C} \longrightarrow \mathcal{C}$

1. a [[natural transformation]]

   $\eta \colon id_{\mathcal{C}} \longrightarrow Q$

such that

1. $Q$ preserves weak equivalences;

1. all $Q(\eta_X) \colon Q(X) \longrightarrow Q(Q(X))$ are weak equivalences;

1. if in a [[pullback]] square in $\mathcal{C}$

   $$
     \array{
       f^\ast W &\stackrel{f^\ast h}{\longrightarrow}& X
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       W &\stackrel{h}{\longrightarrow}& Y
     }
   $$

   we have that

   1. $f$ is a fibration and $Y$ is fibrant;

   1. $Q(\eta_X)$, $Q(\eta_Y)$ and $Q(h)$ are weak equivalences

   then $Q(f^\ast h)$ is a weak equivalence.

=--


+-- {: .num_defn #ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}
###### Definition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad}, say that a morphism $f$ in $\mathcal{C}$ is

1. a $Q$-weak equivalence if $Q(f)$ is a weak equivalence;

1. a $Q$-cofibation if it is a cofibration.

1. a $A$-fibration if it ha the [[right lifting property]] against the morphisms that are both $Q$-fibrations as well as $Q$-weak equivalences.

Write $\mathcal{C}_Q$ for $\mathcal{C}$ equipped with these classes of morphisms.

=--

+-- {: .num_prop}
###### Proposition
**(Bousfield-Friedlander theorem)**

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad},
then $\mathcal{C}_Q$, def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad} is a [[model category]].

Moreover

1. a morphism $f\colon X \to Y$ is a $Q$-fibration precisely if 

   1. $f$ is a fibration;

   1. the $\eta$-naturality square on $f$ exhibits a [[homotopy pullback]]

      $$
        \array{
          X &\stackrel{\eta_X}{\longrightarrow}& Q(X)
          \\
          {}^{\mathllap{f}}\downarrow &{}^{(pb)^h}& \downarrow^{\mathrlap{Q(f)}}
          \\
          Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
        }
        \,.
      $$

=--

([Bousfield-Friedlander 78, theorem 8.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3 ](#Bousfield01))


## Examples

### Stable model structure on sequential spectra

The [[Bousfield-Friedlander model structure]] $SeqSpectra_{stable}$ on [[sequential spectra]] (in [[sSet]] or in [[Top]]), modelling [[stable homotopy theory]], arises via the Bousfield-Friedlander theorem from localizing the strict model structure $SeqSpectra_{strict}$ [[transferred model structure|transferred]] from the model structure on sequences (in the [[classical model structure on simplicial sets]]/[[classical model structure on topological spaces|on topological spaces]]) at the [[spectrification]] endofunctor.

## References

The theorem is due to 

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], section A.3 of  _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))

and in improved form due to 

* {#Bousfield01} [[Aldridge Bousfield]], section 9 of _On the telescopic homotopy theory of spaces_, Trans. Amer. Math. Soc. 353 (2001), no. 6, 2391&#8211;2426 ([AMS](http://www.ams.org/journals/tran/2001-353-06/S0002-9947-00-02649-0/), [jstor](http://www.jstor.org/stable/221952))

The properness condition is shown to be unnecessary in 

* {#Stanculescu08} Alexandru E. Stanculescu, _Note on a theorem of Bousfield and Friedlander_, Topology Appl. 155 (2008), no. 13, 1434--1438 ([arXiv:0806.4547](http://arxiv.org/abs/0806.4547))

Textbook accounts include

* [[Paul Goerss]], [[Rick Jardine]], section X.4 of_[[Simplicial homotopy theory]]_, (1996)

