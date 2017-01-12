
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
##### Fusion categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Intuition

A [[fusion category]] can be seen as a [[categorification]] of a semisimple algebra, like the group ring of a finite group. A [[2-group]] is an [[internalisation]] of a group. A [[strict 2-group]] (which is essentially the same as a [[crossed module]] in particular has an underlying group.

In this sense, a $G$-crossed braided fusion category can be seen as some kind of categorification of a crossed module $(G, H, \delta\colon H \to G, \alpha\colon G \to Aut(H))$, where the group $H$ is lifted to a fusion category, but $G$ is still a (finite) group. The boundary morphism $\delta$ is replaced by a $G$-grading, and the Peiffer rule ($G$-graded commutativity) is categorified to a _crossed braiding_ on $\mathcal{C}$.

$G$-crossed braided fusion category should also be related to monoidal bicategories.

## Name

There are various names for this particular flavour of fusion category,
involving permutations of the words "braided" and "crossed", or possibly trading "braided" for "$G$-braided".

The latter choice has its justification in the fact that in general, it is _not_ a [[braided category]], but the braiding is in a sense twisted by the grading, just as the second group $H$ in a crossed module need not be abelian, but up to a group action.

## Definition

A $G$-crossed braided fusion category consists of the following:

* A finite group $G$,
* a fusion category $\mathcal{C}$,
* a $G$-[[graded fusion category|grading]] on $\mathcal{C}$,
* a monoidal $G$-action $\rho$ on $\mathcal{C}$ (i.e. a monoidal functor $(\rho, \rho^2, \rho^0)\colon \ul{G} \to Aut_\otimes(\mathcal{C})$ from $G$ viewed as a monoidal category to the category of tensor automorphisms of $\mathcal{C}$)
such that $\rho(g_1)\mathcal{C}_{g_2} \subset \mathcal{C}_{g_1g_2g_1^{-1}}$,
* for each $g \in G$, a natural isomorphism $c_{g,X,Y}\colon X \otimes Y \to \rho(g)(Y) \otimes X$, where $X \in \mathcal{C}_g, Y \in \mathcal{C}$

satisfying

* a $G$-graded hexagon equation for $c$:

$$
  \array{
      &
        & (X \otimes Y) \otimes Z
    \\
      & \mathllap{{}^{\alpha_{X,Y,Z}}\swarrow}
        &
          & \mathrlap{\searrow^{c_{X,Y} \otimes 1_Z}}
    \\
    X \otimes (Y \otimes Z)
      &
        &
          &
            & (\rho(g)(Y) \otimes X) \otimes Z
    \\
    {}^{c_{X,Y \otimes Z}}\downarrow
      &
        &
          &
            & \downarrow^{\alpha_{\rho(g)(Y), X, Z}}
    \\
    \rho(g)(Y \otimes Z) \otimes X
      &
        &
          &
            & \rho(g)(Y) \otimes (X \otimes Z)
    \\
    {}^{\rho^2(g)_{Y, Z} \otimes 1_X}\downarrow
      &
        &
          &
            & \downarrow^{1_{\rho(g)(Y)} \otimes c_{X, Z}}
    \\
    (\rho(g)(Y) \otimes \rho(g)(Z)) \otimes X
      &
        & \mathclap{\underset{\alpha_{\rho(g)(Y), \rho(g)(Z), X}}{\longrightarrow}}
          &
            & \rho(g)(Y) \otimes (\rho(g)(Z) \otimes X)
  }
$$

* compatibility of the crossed braiding and the group action.

TODO Commutative diagrams

If $\mathcal{C}$ carries extra structure (e.g. a [[pivotal category|pivotal]] structure), the group action is typically required to preserve it.

## Examples

* Every braided fusion category can be trivially graded, with the trivial action.
* Every crossed module $(G, H, \delta, \alpha)$ makes $H$-graded vector spaces into a $G$-crossed category. (Check/reference!)

## (De-)Equivariantisation

TODO

## 4d extended TQFTs

TODO - Cui's thesis

## References

* Turaev
* M&#252;ger
* Cui

[[!redirects $G$-crossed braided fusion categories]]
[[!redirects Braided $G$-crossed fusion categories]]
[[!redirects Braided G-crossed fusion categories]]
[[!redirects G-crossed braided fusion categories]]
[[!redirects G-crossed G-braided fusion categories]]
[[!redirects $G$-crossed $G$-braided fusion categories]]
[[!redirects Braided $G$-crossed fusion category]]
[[!redirects Braided G-crossed fusion category]]
[[!redirects G-crossed braided fusion category]]
[[!redirects G-crossed G-braided fusion category]]
[[!redirects $G$-crossed $G$-braided fusion category]]
