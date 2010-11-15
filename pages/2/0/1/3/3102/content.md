
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition


Given an [[object]] $Y$ of a [[category]] $C$, a __sink__ to $Y$ in $C$ is a [[collection]] of [[morphisms]] of $C$ whose [[targets]] (codomains) are all $Y$:

$$ \array {
   X_1 \\
       & \searrow^{f_1} \\
   X_2 & \overset{f_2}\to & Y \\
       & \nearrow_{f_3} \\
   X_3
} $$

The [[duality|dual]] concept is a collection of morphisms of $C$ whose [[sources]] (domains) are all $Y$:

$$ \array {
   & & X_1 \\
       & {}^{f_1}\nearrow \\
   Y & \overset{f_2}\to & X_2 \\
       & {}_{f_3}\searrow \\
   & & X_3
} $$

Confusingly, this dual concept is called a __source__ from $Y$ in $C$, even though the term 'source' has another meaning, one which we just used in the definition!  One can of course say 'domain' instead of 'source' for this other meaning, but that leads to [[domain|other confusions]].  Or one can say 'cosink' for a source in the sense dual to a sink, since a source from $Y$ in $C$ is the same as a sink to $Y$ in the [[opposite category]] $C^{\mathrm{op}}$.


## Applications

The concept plays a role for instance in the context of [[solid functor]]s.

[[!redirects cosink]]
[[!redirects sinks]]
[[!redirects cosinks]]
