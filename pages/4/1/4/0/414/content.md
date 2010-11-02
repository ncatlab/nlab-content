
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition 

An [[object]] $P$ of a [[category]] $C$ is **projective** (with respect to epimorphisms) if for any [[morphism]] $f:P \to B$ and any [[epimorphism]] $q:A \to B$, $f$ factors through $q$ by some morphism $P\to A$.

$$
  \array{
    && A
    \\
    &{}^{\mathllap{\exists}}\nearrow& \downarrow^{\mathrlap{q}} 
    \\
    P &\stackrel{f}{\to}& B
  }
  \,.
$$

Another way to say  this is that the [[hom-functor]] $Hom(P,-)$ preserves epimorphisms.


A category $C$ has **enough projectives** if for every object $X$ there is an epimorphism $P\to X$ where $P$ is projective.

**Remarks**

* The [[duality|dual]] notion is [[injective object]]. 

* There are variations of the definition where "epimorphism" is replaced by some other type of morphism, such as a [[regular epimorphism]] or [[strong epimorphism]] or the left class in some [[orthogonal factorization system]].  In this case one may speak of **regular projectives** and so on.  In a [[regular category]] "projective" almost always means "regular projective."

## Properties

* If $C$ has [[pullback|pullbacks]] and epimorphisms are preserved by pullback, as is the case in a [[pretopos]], then $P$ is projective iff any epimorphism $Q\to P$ is [[split epimorphism|split]].

* The [[axiom of choice]] can be phrased as "all objects of [[Set]] are projective."  See also [[internally projective object]] and [[COSHEP]].



[[!redirects enough projectives]]
[[!redirects projective objects]]