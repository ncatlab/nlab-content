
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition

Let $C$ and $D$ be [[monoidal categories]], and $F \,\colon\, C \rightleftarrows D \,\colon\, G$ a _comonoidal adjunction_, i.e. an [[adjunction]] $F\dashv G$ in the [[2-category]] of [[colax 2-functor|colax]] [[monoidal functors]].  (By [[doctrinal adjunction]], this is actually equivalent to requiring that $G$ is a [[strong monoidal functor]].)  This adjunction is a **Hopf adjunction** if the canonical morphisms

$$ 
  F(x \otimes G y) 
   \longrightarrow 
  F x \otimes y 
$$

$$ 
  F(G y \otimes x) 
    \longrightarrow 
  y \otimes F x 
$$

are [[isomorphisms]] for any $x\in C$ and $y\in D$.

Of course, if $C$, $D$, $F$, and $G$ are [[symmetric monoidal category|symmetric]], then it suffices to ask for one of these.  If $C$ and $D$ are moreover [[cartesian monoidal category|cartesian monoidal]], then any adjunction is comonoidal, and the condition is also (mis?)named *[[Frobenius reciprocity]]*.

## Properties

* If $C$ and $D$ are closed, then by the calculus of [[mates]], saying that $F\dashv G$ is Hopf is equivalent to asking that $G$ be a [[closed monoidal functor]], i.e. preserve [[internal-homs]] up to isomorphism.

* If $F\dashv G$ is a Hopf adjunction, then its induced monad $G F$ is a [[Hopf monad]].  Conversely, the [[Eilenberg-Moore category|Eilenberg-Moore]] adjunction of a Hopf monad is a Hopf adjunction.

## Related concepts

* [[adjunction]]

* [[Frobenius reciprocity]]

* [[Hopf monad]]

* [[Hopf algebra]]


## References

* [[Alain Bruguières]], [[Steve Lack]], [[Alexis Virelizier]], *Hopf monads on monoidal categories*,  Adv. Math. __227__ 2 (2011) 745-800 &lbrack;[arXiv:1003.1920](https://arxiv.org/abs/1003.1920), [doi:10.1016/j.aim.2011.02.008](https://doi.org/10.1016/j.aim.2011.02.008)&rbrack;

* [[Adriana Balan]], *On Hopf adjunctions, Hopf monads and Frobenius-type properties*, Appl. Categ. Structures **25** 5 (2017) 747-774 &lbrack;[arxiv:1411.2236](https://arxiv.org/abs/1411.2236), [doi:10.1007/s10485-016-9428-0](https://doi.org/10.1007/s10485-016-9428-0)&rbrack;


[[!redirects Hopf adjunctions]]

