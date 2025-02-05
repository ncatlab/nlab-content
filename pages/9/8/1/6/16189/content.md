
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[vector space]] $V$ and an element $\phi$ in the [[exterior product]] $\wedge^p V^\ast$ (a $p$-covector), then a [[differential form|differential p-form]] $\omega$ on a [[smooth manifold]] $X$ whose [[tangent spaces]] look like $V$ is called _definite on $\phi$_ ([Bryant 05, section 3.1.1](#Bryant05)) or _stable at each point_ ([Hitchin, p. 3](#Hitchin)) if at each point $x \in X$ the restriction $\omega|_x \in \wedge^p T^\ast X \simeq \wedge^p V^\ast$ is equal to $\phi$, up to a [[general linear group|general linear transformation]].

The existence of a definite form implies a [[G-structure]] on $X$ for $G$ the [[stabilizer subgroup]] of $\phi$. 

A class of examples of definite forms are the 3-forms on [[G₂-manifolds]], these are definite on the "[[associative 3-form]]" on $\mathbb{R}^7$.

The [[higher prequantization]] of a definition form is a [[definite globalization of a WZW term]].



## Definition

Given a [[vector space]] $V$ and a [[stable form]] $\phi \in \wedge^p V^\ast$ (hence a form whose [[orbit]] under the [[general linear group]] $GL(V)$ is an [[open subspace]] in $\wedge^p V$), and given a [[smooth manifold]] modeled on the [[vector space]] $V$, then a [[differential form]] $\omega \in \Omega^p(X)$ is _definite_ on $\phi$ if at each point it is in this open orbit.


## Examples

### $G_2$-manifolds

See at _[G₂-manifold -- Definite forms](G₂-manifold#Definite3Forms)_

## References



* {#Hitchin} [[Nigel Hitchin]], _Special holonomy and beyond_, Clay Mathematics Proceedings ([pdf](https://people.maths.ox.ac.uk/hitchin/hitchinlist/clay.pdf))

* {#Bryant05} [[Robert Bryant]], _Some remarks on $G_2$-structures_, Proceedings of the 12th G&#246;kova Geometry-Topology Conference 2005, pp. 75-109 [pdf](http://gokovagt.org/proceedings/2005/ggt05-bryant.pdf)


[[!redirects definite forms]]
[[!redirects definite differential form]]
[[!redirects definite differential forms]]

[[!redirects definite 3-form]]
[[!redirects definite 3-forms]]

[[!redirects definite differential 3-form]]
[[!redirects definite differential 3-forms]]