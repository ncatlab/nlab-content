
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

## Definition

Given a [[homotopy theory]], i.e. an [[(infinity,1)-category]], then a _tower of homotopy fibers_ or _tower of fibrations_ or similar is a [[tower]] [[diagram]] of the form

$$
  \array{
    \vdots
    \\
    {}^{\mathllap{hofib(f_2)}}\downarrow
    \\
    X_2 &\stackrel{f_2}{\longrightarrow}& A_2
    \\
    {}^{\mathllap{hofib(f_1)}}\downarrow
    \\
    X_1 &\stackrel{f_1}{\longrightarrow}& A_1
    \\
    {}^{\mathllap{hofib(f_0)}}\downarrow
    \\
    X &\stackrel{f_0}{\longrightarrow}& A_0
  }
$$

where each hook is a [[homotopy fiber sequence]].

## Properties

The [[long exact sequences of homotopy groups]] for each of the hooks in the tower combine to yield an [[exact couple]]. The corresponding [[spectral sequence of an exact couple]] is a means to (approximately) compute the [[homotopy groups]] of the base object $X$ of the tower

## Examples

* [[Postnikov tower]]

* [[Adams tower]]

## Related concepts

* [[filtered object in an (infinity,1)-category]]

  * [[filtered chain complex]]

  * [[filtered spectrum]]

* [[spectral sequence of a tower of fibrations]]

## References

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], chapter IX of _Homotopy limits, completions and localization_, Springer 1972


* [[Paul Goerss]], [[Rick Jardine]], chapter VI of _[[Simplicial homotopy theory]]_, 1996

[[!redirects towers of homotopy fibers]]

[[!redirects tower of fibrations]]
[[!redirects towers of fibrations]]

[[!redirects fibrational tower]]
[[!redirects fibrational towers]]

