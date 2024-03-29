
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[non-archimedean analytic geometry]], affinoid domains are basic model [[spaces]]: a [[Berkovich analytic space]] is, in particular, a [[topological space]] equipped with an [[atlas]] by ([[analytic spectra]] underlying) affinoid domains.

## Definition

+-- {: .num_defn}
###### Definition

An **[[affinoid domain]]** in an [[affinoid space]] $X = Spec_{an} A$ is a [[closed subset]] $V \subset X$ such that there is a [[homomorphism]] of $k$-affinoid spaces 

$$
  \phi : Spec_{an} A_V \to X
$$

for some $A_V$, whose [[image]] is $V$, and such that every other morphism of $k$-affinoid spaces into $X$ whose image is contained in $V$ uniquely factors through this morphism.

=--

([Berkovich 09, def. 2.2.1](#Berkovich09))

+-- {: .num_defn}
###### Definition

A morphism $f\colon X\to Y$ of [[affinoid spaces]] is an _affionoid domain embedding_ if it induces an [[isomorphism]] of $X$ with an affinoid domain in $Y$

=--

([Berkovich 09, def. 2.2.7](#Berkovich09))

These are the "admissible morphisms" in the site of affinoid domains. (...)

## Properties

* [[Tate's acyclicity theorem]]

## Related concepts

* [[closed cover]]

* [[Berkovich space]]

## References

* {#Berkovich09} [[Vladimir Berkovich]], section 2.2 of _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))

* [[Doosung Park]], _Affinoid domains_, lecture notes ([pdf](http://math.berkeley.edu/~sstich/MAT_274/03-07.pdf))


[[!redirects affinoid domains]]

[[!redirects affinoid domain embedding]]
[[!redirects affinoid domain embeddings]]
