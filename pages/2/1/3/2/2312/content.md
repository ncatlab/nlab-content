
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents# 
* table of contents
{:toc}

## Idea

A [[cohomology theory]] $E$ is called _multiplicative_ if $E^\bullet(X)$ is not just a [[graded module|graded]] [[abelian group]], but actually a graded [[ring]] in a compatible way.

## Definition

+-- {: .num_defn }
###### Definition

Let $E_1, E_2, E_3$ be three unreduced [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theories]] ([def.](generalized+cohomology+theory#GeneralizedCohomologyTheory)). A **pairing** 

$$
  \mu \;\colon\; E_1 \Box E_2 \longrightarrow E_3
$$

is a [[natural transformation]] of the form

$$
  \mu_{n_1,n_2}
   \;\colon\;
  E_1^{n_1}(X,A)
    \otimes
  E_2^{n_2}(Y,B)
    \longrightarrow
  E_r^{n_1 + n_2}(X\times Y \;,\; A\times Y \cup X \times B)
$$

such that this is compatible with the connecting homomorphisms $\delta_i$ of $E_i$, in that the following are [[commuting squares]]

$$
  \array{
    E_1^{n_1}(A)
      \otimes 
    E_2^{n_2}(Y,B)
      &\overset{\delta_1 \otimes id_2}{\longrightarrow}&
    E_1^{n_1+1}(X,A) \otimes E_2^{n_2}(Y,B)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1+1, n_2}}}
    \\
   \underoverset
     {E_3^{n_1 + n_2}(A \times Y \cup  \times B , X \times B)}
     {E_3^{n_1 + n_2}(A \times Y, A \times B)}
     {\simeq}
     &\overset{\delta_3}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X \times Y, A \times B)
  }
$$

and



=--


## Properties

### Brown representability

A _multiplicative structure_ on a [[generalized (Eilenberg-Steenrod) cohomology]] theory is the structure of a [[ring spectrum]] on the [[spectrum]] that [[Brown representability theorem|represents]] it.

e.g. [Lurie 10, lecture 4](#Lurie10)

In particular every [[E-∞ ring]] is a [[ring spectrum]], hence represents a multiplicative cohomology theory, but the converse is in general false.

## Examples

* [[ordinary cohomology]] with [[coefficients]] in a [[ring]], in particular [[integral cohomology]]

* [[topological K-theory]], [[K-theory]]

* [[cobordism cohomology theory]]

* [[tmf]]

* etc....

## Related entries

For multiplicative cohomology theories one can consider

* [[universal coefficient theorem]], [[module spectrum|module cohomology theories]], ...

See also

* [[complex oriented cohomology theory]], [[chromatic homotopy theory]]

* [[Thom isomorphism]]

* [[orientation in generalized cohomology]]

* [[fiber integration]]

* [[K-theory of a bipermutative category]]

* [[multiplicative spectral sequence]]

## References
	
* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], chapter 2.6 of _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([[GeneralizedCohomology.pdf:file]])

* [[Jacob Lurie]], _[[A Survey of Elliptic Cohomology - cohomology theories]]_

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ 2010, Lecture 4 _[[complex oriented cohomology theory|Complex-oriented cohomology theories]]_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf))


[[!redirects multiplicative cohomology theories]]

[[!redirects multiplicative cohomology]]



