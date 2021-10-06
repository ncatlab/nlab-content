
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* tableofcontents
{:toc}

## Idea

A _dual adjunction_ between [[category|categories]] $C$ and $D$ is an [[adjoint functor|adjunction]] between the [[opposite category]] $C^{op}$ of $C$ and $D$.

The concept arises in the context of [[duality]].

Dual adjunctions between [[concrete category|concrete categories]] are frequently represented by [[dualizing objects]].

Dual adjunctions between [[posets]] are also called _[[Galois connections]]_.

## Definition 

A _dual adjunction_ consists of [[contravariant functors]] $F: C \to D$, $G: D \to C$ together with natural transformations $\eta: 1_C \to G F$ and $\theta: 1_D \to F G$ such that $F \eta \circ \theta F = 1_F$ and $G \theta \circ \eta G = 1_G$. In diagrams, the following must commute. 
\begin{tikzcd}
F \ar{dr}[swap]{1} \ar{r}{\theta F} & FGF \ar{d}{F\eta}  & & G \ar{dr}[swap]{1} \ar{r}{\eta G} & GFG \ar{d}{G\theta} \\
& F & & & G
\end{tikzcd}

Reformulated in terms of covariant functors, a dual adjunction can be viewed as an ordinary adjunction $F \dashv G$ with $F: C \to D^{op}$ and $G: D^{op} \to C$, or as $G \dashv F$ with $G: D \to C^{op}$ and $F: C^{op} \to D$. However, it is often useful not to break the symmetry of the contravariant formulation. 

A _self-dual_ adjunction is a dual adjunction for which $F = G: C \to C$ and $\eta = \theta: 1 \to F F$. An example is where $C$ is a [[symmetric monoidal closed category]] and $F = [-, d]$ is an internal hom into an object $d$, where the unit is the usual double-dual embedding $\delta_c: c \to [[c, d], d]$. 

## Related concepts

* [[adjunction]]

  * [[strong adjoint functor]]

  * [[adjoint triple]], [[adjoint quadruple]], [[recollement]]

  * [[ambidextrous adjunction]]

  * [[adjoint monad]]

  * [[fixed point of an adjunction]]

  * [[enriched adjunction]]

  * [[two-variable adjunction]]



[[!redirects dual adjunctions]]
