\tableofcontents

## Idea 

Just as the classical notion of [[pointed object]] refers to a morphism whose domain is [[terminal object|terminal]], which in the context or [[doctrine]] of [[cartesian monoidal categories]] is the monoidal unit, so one can generalize such "pointing": a pointed object in a [[monoidal category]] is an object $X$ equipped with a morphism $I \to X$ from the [[monoidal unit]] $I$. 

## Examples 

* A [[pointed endofunctor]] on a category $C$ is an [[endofunctor]] $F$ together with a [[natural transformation]] $1_C \to F$. When the [[endofunctor category]] $[C, C]$ is viewed as a [[strict monoidal category]] whose monoidal unit is the identity functor, this notion can be seen as an example of a pointed object in a monoidal category. 

* A [[pointed abelian group]] is a an [[abelian group]] $A$ equipped with a morphism $\mathbb{Z} \to A$, where $\mathbb{Z}$ is the unit for the [[tensor product of abelian groups]]. 

* Under change of [[base of enrichment]], pointed objects in the current sense may be compared to pointed objects in the classical sense. For example, if $V$ is a monoidal category, there is a change of base functor 
$$U = V(I, -): V \to Set$$ 
and a pointing of an object $v$ of $V$ is equivalent to a pointing of its underlying object in the classical sense, $1 \to U(v)$. 