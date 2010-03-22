
> under construction -- something is amiss here...


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **tangent category** of a [[category]] $C$ is an approximation to the notion of [[tangent (∞,1)-category]] in ordinary [[category theory]]. 

For the moment see there for further motivation.

The tangent category $T_C$ of $C$ is effectively the _fiberwise abelianization_ of the [[codomain fibration]] $cod : [I,C] \to C$:

we may think of it as obtained from the codomain fibration by replacing each [[overcategory]] fiber $[I,C]_A = C/A$ by the corresponding category of abelian [[group object]]s and restricting the morphisms such as to respect the abelian group object structure.

## Definition

Let $C$ be a [[category]] with [[pullback]]s. Then the **tangent category** $T_C$ of $C$ is the category whose

* [[object]]s are pairs $(A,\mathcal{A})$ with $A \in Ob(C)$ and with $\mathcal{A}$ an abelian [[group object]] in the [[overcategory]] $C/B$;

  notice that for $\mathcal{B} \to B$ an object in the overcategory that is equipped with the structure of an abelian group object -- notably with a product $prod_{\mathcal{B}} : \mathcal{B} \times_B \mathcal{B} \to  \mathcal{B}$ -- and for $f : A \to B$ any morphism in $C$, the [[pullback]] $f^* \mathcal{B} := A \times_B \mathcal{B}$ in $C$ is naturally equipped with the structure of an abelian group object in $C/A$;
  

* [[morphism]]s $(f, \mathcal{f}) : (A,\mathcal{A}) \to (B, \mathcal{B})$ are commuting squares

  $$
    \array{
      \mathcal{A} &\stackrel{\mathcal{f}}{\to}& \mathcal{B}
      \\
      \downarrow && \downarrow 
      \\
      A &\stackrel{f}{\to}& B
    }
  $$

  such that the induced morphism $\mathcal{A} \to f^*\mathcal{B}$ is a morphism of abelian group objects in $C/A$; 

* composition of morphisms is given in the evident way by $(f_2, \mathcal{f}_2) \circ (f_1, \mathcal{f}_1) = (f_2 \circ f_1, \mathcal{f}_2 \circ \mathcal{f}_1) $.


## Examples

For $C = $ [[CRing]] we have $T_C = $ [[Mod]]. This is described in detail at [[module]].