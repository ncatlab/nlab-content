


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _fibration lemma_ ([Bousfield-Kan 72, Chapter II](#BousfieldKan72)) in ([[rational parametrized homotopy theory|parametrized]]) [[rational homotopy theory]] states sufficient conditions under which [[rationalization]] preserves [[homotopy fibers]].

## Properties


+-- {: .num_prop #RationalFibrationLemma} 
###### Proposition
**(rational fibration lemma)**

Let

$$
  \array{
    F &\overset{fib(p)}{\longrightarrow}& A
    \\
    && \big\downarrow{}^{\mathrlap{p}}
    \\
    && B    
  }
$$

be a [[Serre fibration]] of [[connected topological space|connected]] [[topological spaces]], with [[fiber]] $F$ (over any base point) also connected.

If in addition

1. the [[fundamental group]] $\pi_1(B)$ [[nilpotent module|acts nilpotently]] on the [[homology groups]] $H_\bullet(F,k)$ 

   (e.g. if $B$ is [[simply connected topological space|simply connected]], or if the fibration is a [[principal bundle]]);

1. at least one of $A$, $F$ is rationally [[of finite type]] 

then the [[cofiber]] of any [[relative Sullivan model]] for $p$ is a [[Sullivan model]] for $F$.

=-- 

([Félix-Halperin-Thomas 00, Theorem 15.3](#FelixHalperinThomas00), following [Halperin 83, Section 16](#Halperin83))


Moreover, if $CE(\mathfrak{l}B)$ is a [[minimal Sullivan model]] for $B$, then the cofiber of the corresponding minimal [[relative Sullivan model]] for $p$ is the [[minimal Sullivan model]] $CE(\mathfrak{l}F)$ for $F$:

\[
  \label{SullivanModelForFiber}
  \array{
    CE(\mathfrak{l}F)
    &\overset{
      cofib
      \big(
        CE(\mathfrak{l}p)
      \big)
    }{\longleftarrow}&
    CE(\mathfrak{l}_{{}_B}A)
    \\
    && \big\uparrow{}^{\mathrlap{ CE(\mathfrak{l}p) }}
    \\
    && CE(\mathfrak{l}B)
  }
\]

([Félix-Halperin-Thomas 00, Corollary on p. 199](#FelixHalperinThomas00)) 

But this cofiber, being the cofiber of a [[relative Sullivan model]] and hence of a [[cofibration]] in the [[projective model structure on dgc-algebras]], is in fact the [[homotopy cofiber]], and hence is a model for the [[homotopy fiber]] of the [[rationalization|rationalized]] fibration. 

Therefore (eq:SullivanModelForFiber) implies that:

On fibrations of [[connected topological space|connected]] rational [[finite type]]-spaces, where the [[fundamental group]] of the base space [[nilpotent module|acts nilpotently]] on the [[homology groups]] of the [[fiber]]: _[[rationalization]] preserves [[homotopy fibers]]_.

(This is the _fibration lemma_ orginally due to [Bousfield-Kan 72, Chapter II](#BousfieldKan72).)


## Related concepts

* [[parametrized homotopy theory]]

* [[rational parametrized homotopy theory]]

* [[rational parametrized stable homotopy theory]]

## References


* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], Chapter II "Fiber Lemmas" of: _Homotopy Limits, Completions and Localizations_, Springer 1972 ([doi:10.1007/978-3-540-38117-4](https://doi.org/10.1007/978-3-540-38117-4))

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Sections 14 and 15 of: _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

[[!redirects rational fiber lemmas]]

[[!redirects rational fibre lemma]]
[[!redirects rational fibre lemmas]]

[[!redirects rational fibration lemma]]
[[!redirects rational fibration lemmas]]


[[!redirects fiber lemma]]
[[!redirects fiber lemmas]]

[[!redirects fibre lemma]]
[[!redirects fibre lemmas]]

