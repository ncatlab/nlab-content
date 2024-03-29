+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $k$ be a [[perfect field]] and fix a [[prime number]] $p$.

Write $W(k)$ for the [[ring of Witt vectors]] and 

$$
  R \coloneqq W(k)[ [ v_1, \cdots, v_{n-1} ] ]
$$

for the ring of [[formal power series]] over this ring, in $n-1$ [[variables]]; called the _Lubin-Tate ring_.

There is a canonical [[morphism]]

$$
  p \;\colon\; R \longrightarrow k
$$

whose [[kernel]] is the [[maximal ideal]]

$$
  ker(p) \simeq (p,v_1, \cdots, v_{n-1})
  \,,
$$

This induces (...) for every [[formal group]] $f$ over $k$ a [[deformation]] $\overline{f}$ over $R$. This is the _Lubin-Tate formal group_.

## Properties

### As the universal deformation

The *[[Lubin-Tate theorem]]* asserts that the Lubin-Tate formal group $\overline{f}$ is the [[universal construction|universal]] [[deformation]] of $f$. 

### As inducing Morava E-theory

The Lubin-Tate [[formal group]] is [[Landweber exactness|Landweber exact]] and hence induces a [[complex oriented cohomology theory]]. This is [[Morava E-theory]], see there for more details.

## Related concepts

* [[Lubin-Tate theory]]

* [[Lubin-Tate space]]

## References

For a general review see

* Wikipedia, _[Lubin-Tate formal group law](http://en.wikipedia.org/wiki/Lubin&#8211;Tate_formal_group_law)_

For the role in [[chromatic homotopy theory]] see

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 21 _Lubin-Tate theory_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture21.pdf))
 {#LurieLecture}


[[!redirects Lubin-Tate formal groups]]

[[!redirects Lubin-Tate formal group law]]
[[!redirects Lubin-Tate formal group laws]]