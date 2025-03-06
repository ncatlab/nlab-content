
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

[[fusion category|Fusion categories]] over a [[field]] $k$ may be regarded as a [[categorification]] of [[semisimple algebras|semisimple $k$-algebras]]. For example, the [[group algebra]] of a [[finite group]] $G$ would categorify to the fusion category of $G$-[[graded vector spaces]]. On the other hand, the notion of [[2-groups]] is an [[internalisation]] of the notion of [[groups]]. A [[strict 2-group]] (which is essentially the same as a [[crossed module]]) in particular has an [[underlying]] [[group]].

In this sense, *$G$-crossed braided fusion categories* may be seen as some kind of categorification of [[crossed modules]] $\big(G, H, \delta\colon H \to G, \alpha\colon G \to Aut(H)\big)$, where the group $H$ is lifted to a fusion category, but $G$ is still a ([[finite group|finite]]) [[group]]. The boundary morphism $\delta$ is replaced by a $G$-grading, and the [Peiffer rule](crossed+module#eq:PeifferRule) ($G$-graded commutativity) is categorified to a _crossed braiding_ on $\mathcal{C}$.

$G$-crossed braided fusion categories can also be turned into [[monoidal bicategories]].

\begin{remark}
**(Terminology)**
There are various names for this particular flavor of fusion category,
involving permutations of the words "braided" and "crossed", or possibly trading "braided" for "$G$-braided".

The latter choice has its justification in the fact that in general, it is _not_ a [[braided category]], but the braiding is in a sense twisted by the grading, just as the second group $H$ in a crossed module need not be abelian, but up to a group action.
\end{remark}


## Definition

\begin{definition}
A *$G$-crossed braided fusion category consists of the following:

* A [[finite group]] $G$,

* a [[fusion category]] $\mathcal{C}$ over a [[field]] $k$,

* a $G$-[[graded fusion category|grading]] on $\mathcal{C}$,

* a monoidal $G$-[[action]] $\rho$ on $\mathcal{C}$ (i.e. a [[monoidal functor]] $(\rho, \rho^2, \rho^0)\colon \underline{G} \to Aut_\otimes(\mathcal{C})$ from $G$ viewed as a [[discrete category|discrete]] [[monoidal category]] to the category of tensor automorphisms of $\mathcal{C}$)
such that $\rho(g_1)\mathcal{C}_{g_2} \subset \mathcal{C}_{g_1g_2g_1^{-1}}$,

* for each $g \in G$, a [[natural isomorphism]] $c_{g,X,Y}\colon X \otimes Y \to \rho(g)(Y) \otimes X$, where $X \in \mathcal{C}_g, Y \in \mathcal{C}$

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

\end{definition}

TODO Commutative diagrams


\begin{remark}
If $\mathcal{C}$ carries extra structure (e.g. a [[pivotal category|pivotal]] structure), the group action is typically required to preserve it.
\end{remark}


## Examples

\begin{example}
Every braided fusion category can be trivially graded, with the trivial action.
\end{example}

\begin{example}
Every [[crossed module]] $(G, H, \delta, \alpha)$ makes $H$-[[graded vector spaces]] into a $G$-crossed category. 
(Check/reference!)
\end{example}

## Properties

### (De-)Equivariantisation

See also *[[equivariantisation]]* for more details.

Let $G$ be a [[finite group]], and $\mathcal{C}$ a [[braided fusion category]].

A braided action of the (finite dimensional) representations $\operatorname{Rep}_G$ on $\mathcal{C}$ is the same as an inclusion of $\operatorname{Rep}_G$ in the symmetric centre $\mathcal{C}'$. By deequivariantisation, this is basically the same as a braided $G$-action on $\mathcal{C}_G$ (the category of internal $k[G]$-modules).
This makes $\mathcal{C}_G$ into a $G$-crossed braided fusion category, but most examples don't arise like this, e.g. the grading obtained this way will always be trivial.

The idea is then to generalise the full inclusion $\operatorname{Rep}_G \hookrightarrow \mathcal{C}' \hookrightarrow \mathcal{C}$ to a full inclusion $\operatorname{Rep}_G \hookrightarrow \mathcal{C}$ that need not factor over $\mathcal{C}'$.
One can still deequivariantise the underlying fusion category of $\mathcal{C}$ with respect to the $\operatorname{Rep}_G$-action, but the procedure will not respect the braiding. Naturally, the result is not a braided fusion category, but a $G$-crossed braided fusion category.

Vice versa, given a $G$-crossed braided fusion category $\mathcal{C}$, one can equivariantise it to a braided fusion category with a full inclusion of $\operatorname{Rep}_G$. When $c$ is the crossed braiding of $\mathcal{C}$, the braiding of two equivariant objects $(X \in \operatorname{ob} \mathcal{C}, u_g\colon \rho(g)(X) \to X)$ and $(Y \in \operatorname{ob} \mathcal{C}, v_g\colon \rho(g)(Y) \to Y)$ is given by $X \otimes Y \xrightarrow{c_{X,Y}} \rho(g)Y \otimes X \xrightarrow{v_g \otimes 1_X} Y \otimes X$.



### Relation to 4d extended TQFTs

TODO -- [Cui 2019](#Cui19)



### Relation to Higher Categories

TODO -- [Cui 2019](#Cui19)'s 2-category



## References

* [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], Section 4.4 in: *On braided fusion categories I*, Selecta Mathematica. New Series **16** 1 (2010) 1–119 &lbrack;[arXiv:0906.0620](https://arxiv.org/abs/0906.0620), [doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z)&rbrack;

* Turaev

* M&#252;ger

Description of $G$-crossed braided categories as monoidal bicategories and construction of a 4d TQFT:

* {#Cui19} [[Shawn X. Cui]], *Higher Categories and Topological Quantum Field Theories*, Quantum Topology **10** 4 (2019) 593-676 &lbrack;[arXiv:1610.07628] (https://arxiv.org/abs/1610.07628), [doi:10.4171/QT/128](https://doi.org/10.4171/QT/128)&rbrack;

Equivalence of certain Gray categories with $G$-crossed braided categories and strictification:

* [[Corey Jones]], [[David Penneys]], [[David Reutter]], *A 3-categorical perspective on $G$-crossed braided categories*, J. London Math. Soc. **107** 1 (2023) 333-406 &lbrack;[arXiv:2009.00405](https://arxiv.org/abs/2009.00405), [doi:10.1112/jlms.12687](https://doi.org/10.1112/jlms.12687)&rbrack;


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

[[!redirects $G$-crossed braided fusion category]]

