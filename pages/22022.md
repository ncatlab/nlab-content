
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[homology groups]]/[[cohomology groups]] of a ([[reduced homology|reduced]]) [[Whitehead-generalized homology theory]]/[[Whitehead-generalized cohomology theory|cohomology theory]] evaluated on an [[long homotopy cofiber sequence]] of [[pointed homotopy types|pointed spaces]] form a [[long exact sequence]] of [[abelian groups]]. 

## Definition

Let $X \overset{f}{\longrightarrow} Y$ be a [[morphism]] of [[pointed homotopy types]] (typically presented as a [[continuous function]] of [[pointed topological spaces]] or a morphism of [[pointed object|pointed]] [[simplicial sets]]) and write

\[
  \label{HomotopyCofiberSequenceOfSpaces}
  \cdots 
  \to 
  X 
    \overset{f}{\longrightarrow} 
  Y 
    \longrightarrow 
  C_f
    \overset{\delta}{\longrightarrow} 
  \Sigma X
    \overset{ \Sigma f }{ \longrightarrow }
  \Sigma Y
    \to
  \cdots
\]

for its induced long [[homotopy cofiber sequence]], where $C_f \coloneqq cof(f)$ denotes the [[homotopy cofiber]] of $f$ and $\Sigma(-)$ is [[reduced suspension]]. 
(If $f$ is presented by a [[cofibration]] in the [[classical model structure on topological spaces]] or the [[classical model structure on simplicial sets]] then $C_f \,\simeq\, Y/X$ is represented simply by the [[quotient space]] of $Y$ by $X$ under $f$. )

Now for $E$ a [[Whitehead-generalized homology theory]] its evaluation on the sequence (eq:HomotopyCofiberSequenceOfSpaces) yields a [[long exact sequence]] of [[abelian groups]] -- the [[reduced homology|reduced]] $E$-[[homology groups]]:

$$
  \cdots 
  \to 
  \widetilde  E_\bullet(X) 
    \overset{f_\ast}{\longrightarrow} 
  \widetilde  E_\bullet(Y) 
    \longrightarrow 
  \widetilde  E_\bullet(C_f)
    \overset{\delta_\ast}{\longrightarrow} 
  \widetilde  E_{\bullet-1}(X)
    \overset{ \Sigma f_\ast }{ \longrightarrow }
  \widetilde  E_{\bullet-1}(Y)
    \to
  \cdots
$$ 

[[duality|Dually]], for $E$ a [[Whitehead-generalized cohomology theory]] its evaluation on the sequence (eq:HomotopyCofiberSequenceOfSpaces) yields a [[contravariant functor|contravariant]] [[long exact sequence]] of [[abelian groups]]  -- the $E$-[[cohomology groups]]:

$$
  \cdots 
    \leftarrow
  \widetilde  E^\bullet(X) 
    \overset{f^\ast}{\longleftarrow} 
  \widetilde  E^\bullet(Y) 
    \longleftarrow 
  \widetilde  E^\bullet(C_f)
    \overset{\delta^\ast}{\longleftarrow} 
  \widetilde  E_{\bullet-1}(X)
    \overset{ \Sigma f^\ast }{ \longleftarrow}
  \widetilde  E^{\bullet-1}(Y)
    \leftarrow
  \cdots
$$ 

Here $f^\ast$ denotes [[pullback in cohomology]] and $\delta^\ast$ is known as a _[[connecting homomorphism]]_.

That we have these _long exact sequences in (co)homology_ is, depending on perspective:

* an _[[axiom]]_ in [[Whitehead-generalized homology theory]]/[[Whitehead-generalized cohomology theory|cohomology theory]];

* a consequence of the [[long exact sequence of homotopy groups]] under the identifications

  * $\widetilde E_\bullet(X) \;\simeq\; \pi_\bullet \big( \Sigma^\infty X \wedge E  \big)$

  * $\widetilde E^\bullet(X) \;\simeq\; \pi_{-\bullet} Maps\big( \Sigma^\infty X, E \big)$,

  where 

  * $E$ denotes now the [[spectrum]] [[Brown representability theorem|representing]] the (co)homology theory,

  * $\pi_\bullet(-)$ denotes the [[homotopy groups of spectra]], 

  * applied here to [[smash product of spectra]] $(-)\wedge E$ and to [[mapping spectra]] $Maps(-,E)$, respectively.

The second perspective, via [[Brown representability theorem|representing]] [[spectra]], makes manifest that we also have long exact sequences over a fixed space $X$, but now induced from a [[homotopy cofiber sequence]] (equivalently a [[homotopy fiber sequence]] by [this Prop.](Spectrum#InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences)) 

$$
  \cdots
  \to
  E 
    \overset{\phi}{\longrightarrow} 
  F
    \overset{}{\longrightarrow}
  G
   \overset{}{\longrightarrow}
  \Sigma E
  \to \cdots
$$

of [[cohomology operations]] of [[coefficient]] theories  (of [[spectra]]), in that

$$
  \cdots
  \to
  \widetilde E_\bullet(X) 
    \overset{\phi_\ast}{\longrightarrow}
  \widetilde  F_\bullet(X)
    \overset{}{\longrightarrow}
  \widetilde  G_\bullet(X)
  \to
  \cdots
$$

and

$$
  \cdots
  \to
  \widetilde  E^\bullet(X) 
    \overset{\phi_\ast}{\longrightarrow}
  \widetilde F^\bullet(X)
    \overset{}{\longrightarrow}
  \widetilde  G^\bullet(X)
  \to
  \cdots
$$

are [[long exact sequences]] of [[abelian groups]].


## Related concepts

* [[long exact sequence in homology]]

  * [[long exact sequence in chain homology]]

* [[long exact sequence of homotopy groups]]

## References

Textbook accounts:

* {#Adams74} [[Frank Adams]], p. 197 in: _[[Stable homotopy and generalised homology]]_, Chicago Lectures in Mathematics, The University of Chicago Press 1974 ([ucp:bo21302708](https://www.press.uchicago.edu/ucp/books/book/chicago/S/bo21302708.html), [pdf](https://www.uio.no/studier/emner/matnat/math/MAT9580/v17/documents/adams-shgh.pdf))

For more references see those at _[[Whitehead-generalized cohomology theory]]_.

[[!redirects long exact sequences in generalized homology]]

[[!redirects long exact sequence in generalized cohomology]]
[[!redirects long exact sequences in generalized cohomology]]

[[!redirects long exact sequence of generalized homology groups]]
[[!redirects long exact sequences of generalized homology groups]]

[[!redirects long exact sequence of generalized cohomology groups]]
[[!redirects long exact sequences of generalized cohomology groups]]



