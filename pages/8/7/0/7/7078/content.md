
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _minimal Kan fibration_ is the specialization of the concept of [[minimal fibrations]] to the [[Kan fibrations]] in the [[classical model structure on simplicial sets]].
Hence a _minimal Kan fibration_ is a [[Kan fibration]] whose [[fibers]] are, in some sense, as small as possible in its homotopy class. Moreover, every [[Kan fibration]] has a [[strong deformation retract]] to a minimal Kan fibration (prop. \ref{KanFibrationHasMinimalStrongDeformationRetract} below).
Hence minimal [[Kan complexes]] (i.e. minimal fibrations over the point) are the analogue in [[simplicial sets]] of [[minimal Sullivan models]] in [[rational homotopy theory]].

Minimal Kan fibrations over connected bases happen to be [[fiber bundles]], locally trivial over each simplex (lemma \ref{MinimalKanFibrationAreFiberBundles} below). This implies that their [[geometric realization]] into any [[convenient category of topological spaces]] is also a fiber bundle and hence in particular a [[Serre fibration]].  This is what makes minimal fibrations play a key role in all available proofs of the [[Quillen equivalence]] between the [[model structure on topological spaces]] and the standard [[model structure on simplicial sets]] (see at _[homotopy hypothsis -- for Kan complexes](homotopy+hypothesis#ForKanComplexes)_). 

## Definition


+-- {: .num_defn #MinimalKanFibration}
###### Definition

A [[Kan fibration]] $\phi \colon S \longrightarrow T$, is called a **[[minimal Kan fibration]]** if for any two cells in the same fiber with the same [[boundary]] if they are homotopic relative their boundary, then they are already equal.

More formally, $\phi$ is minimal precisely if for every [[commuting diagram]] of the form

$$
  \array{
    (\partial \Delta[n]) \times \Delta[1]
    &\stackrel{p_1}{\longrightarrow}&
    \partial \Delta[n]
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] \times \Delta[1]
    &\stackrel{h}{\longrightarrow}&
    S
    \\
    \downarrow^{\mathrlap{p_1}} && \downarrow^{\mathrlap{\phi}}
    \\
    \Delta[n] &\longrightarrow& T
  }
$$

then the two composites 

$$
  \Delta[n]
  \stackrel{\overset{d_0}{\longrightarrow}}{\underset{d_1}{\longrightarrow}} 
  \Delta[n] \times \Delta[1]
  \stackrel{h}{\longrightarrow}
  S
$$

are equal.

=--

## Properties

+-- {: .num_prop #PullbackPreservesMinimalFibration}
###### Proposition

The [[pullback]] (in [[sSet]]) of a [[minimal Kan fibration]], def. \ref{MinimalKanFibration}, along any morphism is again a mimimal Kan fibration. 

=--



+-- {: .num_prop #KanFibrationHasMinimalStrongDeformationRetract} 
###### Proposition

For every [[Kan fibration]], there exists a fiberwise [[strong deformation retract]] to a [[minimal Kan fibration]], def. \ref{MinimalKanFibration}.

=--

(e.g. [Goerss-Jardine 96, chapter I, prop. 10.3](#GoerssJardine96), [Joyal-Tierney 05, theorem 3.3.1, theorem 3.3.3](#JoyalTierney05)).

+-- {: .proof}
###### Proof idea

Choose representatives by [[induction]], use that in the induction step one needs lifts of [[anodyne extensions]] against a [[Kan fibration]], which exist.

=--

+-- {: .num_lemma #FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso}
###### Lemma

A morphism between [[minimal Kan fibrations]], def. \ref{MinimalKanFibration}, which is fiberwise a [[homotopy equivalence]], is already an [[isomorphism]].

=--

(e.g. [Goerss-Jardine 96, chapter I, lemma 10.4](#GoerssJardine96))

+-- {: .proof}
###### Proof idea

Show the statement degreewise. In the [[induction]] one needs to lift [[anodyne extensions]] agains a [[Kan fibration]].

=--

+-- {: .num_lemma #MinimalKanFibrationAreFiberBundles}
###### Lemma

Every [[minimal Kan fibration]], def. \ref{MinimalKanFibration}, over a [[connected]] base is a simplicial [[fiber bundle]], locally trivial over every simplex of the base.

=--

(e.g. [Goerss-Jardine 96, chapter I, corollary 10.8](#GoerssJardine96))

+-- {: .proof}
###### Proof

By assumption of the base being connected, the classifying maps for the fibers over any two vertices are connected by a [[zig-zag]] of [[homotopies]], hence by [this lemma](Kan+fibration#PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence) the fibers are connected by [[homotopy equivalences]] and then by prop. \ref{PullbackPreservesMinimalFibration} and lemma \ref{FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso} they are already isomorphic. Write $F$ for this [[typical fiber]].

Moreover, for all $n$ the morphisms $\Delta[n] \to \Delta[0] \to \Delta[n]$ are [[left homotopy|left homotopic]] to $\Delta[n] \stackrel{id}{\to} \Delta[n]$ and so applying [this lemma](Kan+fibration#PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence) and prop. \ref{FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso} once more yields that the fiber over each $\Delta[n]$ is [[isomorphism|isomorphic]] to $\Delta[n]\times F$.

=--



## Related concepts

[[minimal fibration]]

* [[minimal Joyal fibration]]

* [[minimal dendroidal fibration]]

##References

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], chapter VI.5 of _[[Calculus of fractions and homotopy theory]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 35, Springer (1967)  ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))


* E. Curtis, _Simplicial Homotopy Theory_, Advances in Math., 6, (1971), 107 &#8211; 209.

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], chapter I, section 10 of _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1996)

* [[André Joyal]], [[Myles Tierney]], section 3.3 of _Notes on simplicial homotopy theory_, ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern47.pdf))


[[!redirects minimal Kan fibrations]]

[[!redirects minimal Kan complex]]
[[!redirects minimal Kan complexes]]
