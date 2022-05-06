[[!redirects $G$-crossed braided fusion category]]

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

A [[fusion category]] over a field $k$ can be seen as a [[categorification]] of a semisimple $k$-algebra. For example, the group algebra of a finite group $G$ would categorify to the fusion category of $G$-graded vector spaces. On the other hand, the notion of a [[2-group]] is an [[internalisation]] of the notion of a group. A [[strict 2-group]] (which is essentially the same as a [[crossed module]]) in particular has an underlying group.

In this sense, a $G$-crossed braided fusion category can be seen as some kind of categorification of a crossed module $(G, H, \delta\colon H \to G, \alpha\colon G \to Aut(H))$, where the group $H$ is lifted to a fusion category, but $G$ is still a (finite) group. The boundary morphism $\delta$ is replaced by a $G$-grading, and the Peiffer rule ($G$-graded commutativity) is categorified to a _crossed braiding_ on $\mathcal{C}$.

$G$-crossed braided fusion category should also be related to monoidal bicategories.

## Name

There are various names for this particular flavour of fusion category,
involving permutations of the words "braided" and "crossed", or possibly trading "braided" for "$G$-braided".

The latter choice has its justification in the fact that in general, it is _not_ a [[braided category]], but the braiding is in a sense twisted by the grading, just as the second group $H$ in a crossed module need not be abelian, but up to a group action.

## Definition

A $G$-crossed braided fusion category consists of the following:

* A finite group $G$,
* a fusion category $\mathcal{C}$ over a field $k$,
* a $G$-[[graded fusion category|grading]] on $\mathcal{C}$,
* a monoidal $G$-action $\rho$ on $\mathcal{C}$ (i.e. a monoidal functor $(\rho, \rho^2, \rho^0)\colon \underline{G} \to Aut_\otimes(\mathcal{C})$ from $G$ viewed as a discrete monoidal category to the category of tensor automorphisms of $\mathcal{C}$)
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

See also [[equivariantisation]] for more details.

Let $G$ be a finite group, and $\mathcal{C}$ a braided fusion category.

A braided action of the (finite dimensional) representations $\operatorname{Rep}_G$ on $\mathcal{C}$ is the same as an inclusion of $\operatorname{Rep}_G$ in the symmetric centre $\mathcal{C}'$. By deequivariantisation, this is basically the same as a braided $G$-action on $\mathcal{C}_G$ (the category of internal $k[G]$-modules).
This makes $\mathcal{C}_G$ into a $G$-crossed braided fusion category, but most examples don't arise like this, e.g. the grading obtained this way will always be trivial.

The idea is then to generalise the full inclusion $\operatorname{Rep}_G \hookrightarrow \mathcal{C}' \hookrightarrow \mathcal{C}$ to a full inclusion $\operatorname{Rep}_G \hookrightarrow \mathcal{C}$ that need not factor over $\mathcal{C}'$.
One can still deequivariantise the underlying fusion category of $\mathcal{C}$ with respect to the $\operatorname{Rep}_G$-action, but the procedure will not respect the braiding. Naturally, the result is not a braided fusion category, but a $G$-crossed braided fusion category.

Vice versa, given a $G$-crossed braided fusion category $\mathcal{C}$, one can equivariantise it to a braided fusion category with a full inclusion of $\operatorname{Rep}_G$. When $c$ is the crossed braiding of $\mathcal{C}$, the braiding of two equivariant objects $(X \in \operatorname{ob} \mathcal{C}, u_g\colon \rho(g)(X) \to X)$ and $(Y \in \operatorname{ob} \mathcal{C}, v_g\colon \rho(g)(Y) \to Y)$ is given by $X \otimes Y \xrightarrow{c_{X,Y}} \rho(g)Y \otimes X \xrightarrow{v_g \otimes 1_X} Y \otimes X$.

## 4d extended TQFTs

TODO - Cui's thesis

## Higher Categories

TODO Cui's 2-category

## References

* Section 4.4 in _On braided fusion categories I_, Drinfeld, Gelaki, Nikshych, Ostrik. [ArXiv](http://arxiv.org/abs/0906.0620)
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
