
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The Albanese variety $Alb(X)$ of a [[projective variety|projective]] [[algebraic variety]] $X$ with a chosen basepoint is the universal way of turning this pointed variety into an [[abelian variety]].  Moreover, the Albanese variety of the Albanese variety is the Albanese variety.  Thus, taking the Albanese variety defines an [[idempotent monad]] on the category of pointed projective algebraic varieties.

## Definition

By 'variety' let us mean a connected complete algebraic variety over an algebraically closed field.  Given any variety $X$ with a chosen basepoint there is an abelian variety called the **Albanese variety** $Alb(X)$.  This is defined by the following universal property: there is a map of pointed varieties called the **Albanese map**

$$i_X \colon X \to A(X)$$ 

such that any map of pointed varieties $f: X \to A$ where $A$ is abelian factors uniquely as $i_X$ followed by a map of abelian varieties (in particular, a group homomorphism):

$$\overline{f} \colon Alb(X) \to A.$$  

That is:

$$  f = \overline{f} \circ i_X $$

This process defines a functor

$$ Alb: Var_* \to AbVar $$

from pointed varieties to abelian varieties which has a right adjoint

$$ U: AbVar \to Var_* $$

sending any abelian variety to its underlying pointed variety.  The right adjoint $U$ is [[faithful functor|faithful]], but more remarkably it is also [[full functor|full]]: any basepoint-preserving map of varieties between abelian varieties is automatically a group homomorphism.  (A proof of this fact is outlined in the article [[abelian variety]].)   Moreover, $U$ is [[monadic functor|monadic]].   As a consequence the composite functor

$$ T = U \circ Alb $$

is an [[idempotent monad]] on $Var_*$, and its algebras are the abelian varieties. 

It follows that the Albanese map $i_X \colon X \to A(X)$ is the unit of the monad $T$, and $Alb(Alb(X)) \cong Alb(X)$.   For more details, see the nCaf&#233; discussion [Two miracles in algebraic geometry](https://golem.ph.utexas.edu/category/2016/08/the_magic_of_algebraic_geometr.html).

## Properties 

The Albanese variety of $X$ is dual, as an abelian variety, to its [[Picard scheme| Picard variety]].

For $X$ a suitably well behaved ([[smooth variety|smooth]] [[complex variety|complex]], [[projective variety|projective]]) [[algebraic variety]] of [[dimension]] $dim(X)$, its Albanese variety is the [[intermediate Jacobian]] in degree $2 dim(X)-1$:

$$
  Alb(X) \coloneqq J^{2 dim(X)-1}(X)
 \,.
$$ 

## Related concepts

* [[Picard scheme]], [[Jacobian variety]]

## References

* [Is forming the Albanese variety a monad?](http://mathoverflow.net/questions/247104/is-forming-the-albanese-variety-a-monad), MathOverflow.

* [[Patrick Walls]], _Intermediate Jacobians and Abel-Jacobi maps_, 2012 ([[WallsJacobian.pdf:file]])

[[!redirects Albanese varieties]]


---
&lt;http://mathoverflow.net/questions/2548/albanese-schemes-when-does-an-initial-abelian-scheme-exist-under-a-given-sch>

nLab page on [[nlab:Albanese variety]]
