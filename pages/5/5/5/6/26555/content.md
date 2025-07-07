
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Quantum sets are a generalization of sets in [[noncommutative geometry]]. They have many equivalent definitions.

* A quantum set is a $C^*$-algebra that is $c_0$-direct sum of full matrix algebras.
$$
\mathcal{A} \cong \bigoplus_{i \in I}^{c_0} M_{n_i}(\mathbb{C})
$$

* A quantum set is a [[von Neumann algebra]] that is an $\ell^\infty$-direct sum of full matrix algebras.
$$
\mathcal{M} \cong \bigoplus_{i \in I}^{\ell^\infty} M_{n_i}(\mathbb{C})
$$

* A quantum set is an indexed family of nonzero finite-dimensional Hilbert spaces.
$$
X = \{\mathcal{H}_i\}_{i \in I}
$$

These definitions do not define equal classes of objects, but they can be extended to define equivalent categories in two natural ways. Using the second definition of quantum sets, we can take the morphisms to be quantum relations or, inequivalently, to be unital normal $*$-homomorphisms. In the former case, we obtain the category $qRel$, and in the latter case, we obtain the opposite of the category $qSet$. Note that $qRel$ is equivalent to its own opposite. Quantum sets can be further generalized to "nontracial" quantum sets. This article will use the third definition of quantum sets because this definition avoids operator topologies, making it more accessible to a wider audience.


## Basic definitions

\begin{definition}
A quantum set $X$ is a family of nonzero finite-dimensional Hilbert spaces over $\mathbb{C}$ that is indexed by a set $\mathrm{At}(X)$, which may be empty, finite, or infinite.
$$
X = \{X_\alpha\}_{\alpha \in \mathrm{At}(X)}
$$
\end{definition}

Very little changes if we allow zero-dimensional Hilbert spaces in this definition. Allowing zero-dimensional Hilbert spaces is more mathematically natural but less intuitive.

\begin{definition}
\linebreak

* The *disjoint union* $X + Y$ is defined by $\mathrm{At}(X + Y) = \mathrm{At}(X) + \mathrm{At}(Y)$ and
$$
(X + Y)_\alpha = \begin{cases} X_\alpha & \alpha \in \mathrm{At}(X), \\ Y_\alpha & \alpha \in \mathrm{At}(Y). \end{cases}
$$

* The *Cartesian product* $X \times Y$ is defined by $\mathrm{At}(X \times Y) = \mathrm{At}(X) \times \mathrm{At}(Y)$ and
$$
(X \times Y)_{(\alpha, \beta)} = X_\alpha \otimes Y_\beta.
$$

* The *dual* $X^*$ is defined by $\mathrm{At}(X^*) = \mathrm{At}(X)$ and
$$
(X^*)_\alpha = X_\alpha^*,
$$
where $\mathcal{H}^*$ is the dual Hilbert space.

\end{definition}


## Quantum sets as bundles

In mild paraphrase (following the discussion at *[[dependent linear type]]* and *[[quantum circuits via dependent linear types]]*):

* **quantum sets** are  [[indexed sets]] of [[finite-dimensional Hilbert spaces]] --- hence finite-[[rank of a vector bundle|rank]] [[Hilbert bundle|Hilbert]]-[[vector bundles]] over [[discrete topological spaces]] regarded as a [[sets]] --- and regarded as equipped with the [[external tensor product]] $\boxtimes$ [of vector bundles](VectBund#TensorMonoidalStructure);

* a **[[quantum relation]]** between quantum sets $(x \colon X) \times \mathscr{H}_x$ and $(x' \colon X') \times \mathscr{H}'_x$ is a [[monomorphism]] from a quantum set $\big((x,x') \colon X \times X'\big) \times \mathscr{R}_{(x,x')}$ to $\mathscr{H}^\ast_\bullet \boxtimes \mathscr{H}'_\bullet$:

  $$
    (x,x') \colon X \times X'
    \;\;\;
    \vdash
    \;\;\;
    \mathscr{R}_{(x,y)}
    \hookrightarrow
    \mathscr{H}^\ast_{(x,y)} 
      \otimes
    \mathscr{H}^'_{(x,y)} 
  $$

With [[composition]] the evident [[matrix multiplication]] ([Kornell 2020 (5)](#Kornell20)), quantum relations between quantum sets form a [[category]] $qRel$, which is a [[dagger-compact category]]. 

As such, this serves as [[categorical semantics]] for [[quantum programming languages]] like [[Quipper]] equipped with term recursion, via [[quantum CPOs]] ([Kornell, Lindenhovius & Mislove 2021](#KornellLindenhoviusMislove21)).

## Related concepts

* [[quantum CPO]]

## References

* {#Weaver12} Nik Weaver, *Quantum relations*, Mem. Amer. Math. Soc. **215** (2012).

* {#DeCommerKasprzakSkalskiSoltan18} Kenney De Commer, Paweł Kasprzak, Adam Skalski, and Piotr M. Sołtan, *Quantum actions on discrete quantum spaces and a generalization of Clifford's theory of representations*, Israel J. Math. **226** (2018).

* {#Kornell20} [[Andre Kornell]], *Quantum Sets*, J. Math. Phys. **61** 102202 (2020) &lbrack;[doi:10.1063/1.5054128](https://doi.org/10.1063/1.5054128)&rbrack;

* {#KornellLindenhoviusMislove21} [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], §2 in: *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;

  > (in the context of [[quantum CPOs]])

[[!redirects quantum sets]]

