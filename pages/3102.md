
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


Given an [[object]] $Y$ of a [[category]] $C$, a __sink__ to $Y$ in $C$ is a [[family]] of [[morphisms]] of $C$ whose [[targets]] (codomains) are all $Y$, or equivalently, a family of objects in the [[over category]] $C / Y$:

$$ \array {
   X_1 \\
       & \searrow^{f_1} \\
   X_2 & \overset{f_2}\to & Y \\
       & \nearrow_{f_3} \\
   X_3
} $$

We do not, in general, require that this family be [[small category|small]]; if it is so we would call it a "small sink".

The [[duality|dual]] concept is a family of morphisms of $C$ whose [[sources]] (domains) are all $Y$, or equivalently, a family of objects in the [[under category]] $Y / C$:

$$ \array {
   & & X_1 \\
       & {}^{f_1}\nearrow \\
   Y & \overset{f_2}\to & X_2 \\
       & {}_{f_3}\searrow \\
   & & X_3
} $$

Confusingly, this dual concept is called a __source__ from $Y$ in $C$, even though the term 'source' has another meaning, one which we just used in the definition!  One can of course say 'domain' instead of 'source' for this other meaning, but that leads to [[domain|other confusions]].  Or one can say 'cosink' for a source in the sense dual to a sink, since a source from $Y$ in $C$ is the same as a sink to $Y$ in the [[opposite category]] $C^{\mathrm{op}}$.

### Structured sinks

If $U\colon C\to D$ is a functor, then a **$U$-structured sink** is a collection of objects $X_i\in C$ together with a sink in $D$ of the form $\{U(X_i) \to Y\}$.  This notion figures in the definition of a [[final lift]].

## Examples

* Any [[cocone]] under a [[diagram]] is a sink; indeed a cocone is precisely a sink indexed by the objects of the domain of the diagram together with a commutativity condition for the arrows in the diagram.

* A source with two morphisms is a [[span]], a sink with two morphisms is a [[cospan]]. 

* A [[terminal object|terminal source]] is a [[dependent product]], while an [[initial object|initial sink]] is a [[dependent sum]]. 

## Related pages

* [[final lift]], [[topological concrete category]], [[solid functor]]

* [[factorization structure for sinks]]

[[!redirects cosink]]
[[!redirects sinks]]
[[!redirects cosinks]]
