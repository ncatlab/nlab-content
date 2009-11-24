<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The _shifted tangent bundle_ $\Pi T X$ of a [[manifold]] $X$ is an incarnation of the ordinary [[tangent bundle]] of $X$ as a [[supermanifold]] with the underlying manifold in even degree and the tangent vectors in odd degree.

## Definition ##

For $X$ a smooth [[manifold]] the [[supermanifold]] $\Pi T X$ is defined to be the one specified by the fact that its [[superalgebra]] of functions is the graded-commutative [[exterior algebra]] of [[differential forms]]

$$
  C^\infty(\Pi T X) := \Omega^\bullet(X)
  = \wedge^\bullet_{C^\infty(X)} \Gamma(T^* X)
  \,.
$$

More precisely, for each open $U \subset X$ the value of the [[structure sheaf]] of $\Pi T X$ is $\Omega^\bullet(U)$.

## Alternative characterizations ##

### As an NQ-supermanifold ###

In the context of [[supergeometry]] the algebra $\Omega^\bullet(X)$ is regarded as a $\mathbb{Z}_2$-graded algebra, but of course this $\mathbb{Z}_2$-grading lifts to an $\mathbb{N}$-grading in the obvious way.

Moreover, there is a canonical odd vector field $v_d$ on $\Pi T X$, which as an odd derivation on the function algebra $\Omega^\bullet(X)$ is just the [[deRham complex|deRham differential]].

Equipped with this structure $\Pi T X$ is naturally an [[NQ-supermanifold]]. 

### As the tangent Lie algebroid ###

The [[dg-algebra]] $(\Omega^\bullet(X), d_{dR})$ may also be regarded as the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] of $X$, which identifies the shifted tangent bundle in its refinement to an [[NQ-supermanifold]] with the [[tangent Lie algebroid]] of $X$.

From this perspective, the fact that the vectors are regarded as being in degree one in $\Pi T X$ corresponds to the fact that these are the tangents to the [[k-morphism|1-morphism]]s of the [[fundamental groupoid]] of $X$. (Which is denoted $\Pi(X)$ but with the "$\Pi$" of completely different meaning than the "$\Pi$" as used here, which just indicates degree shift).


### As an internal hom object ###

With $\mathbb{R}^{0|1}$ denoting the [[odd line]], i.e. the [[supermanifold]] with function algebra the algebra of [[dual number]]s, one finds that 

$$
  \Pi T X = [\mathbb{R}^{0|1}, X]
$$

is the [[internal hom]] object in the category of [[supermanifold]]s of maps from $\mathbb{R}^{0|1}$ to $X$. More precisely this means that the [[internal hom]] which exists in the [[closed monoidal structure on presheaves]] on the category of supermanifolds, between the presheaves [[representable functor|represented by]] $\mathbb{R}^{0|1}$ and $X$, is itself [[representable functor|representable]] and is represented by $\Pi T X$.

The existence of the structure of an [[NQ-supermanifold]] is from this point of view a consequence of the fact that $[\mathbb{R}^{0|1},X]$ naturally carries an action of the [[endomorphism]] object $End(\mathbb{R}^{0|1})$.  For more on this see [[NQ-supermanifold]].