
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $\mathbb{P}^n = \mathbb{P}^n_k$ be the $n$-dimensional [[projective space]] over a [[field]] $k$, whose points are the equivalence classes $[z_0,\ldots,z_n]$ of $(n+1)$-tuples $(z_0,\ldots,z_n)\in k^{n+1}\backslash \{0\}$; the (co)domains of usual open charts in the sense of [[manifolds]], which are [[Zariski topology|Zariski-open]] subsets for general $k$, have $U_i = \{[z_0,\ldots,z_n] | z_i\neq 0\}$.

The __hyperplane line bundle__ $\mathcal{O}(1)$ on $\mathbb{P}^n$ is a [[line bundle]] given by the [[transition functions]] $g_{i j}([z_0,\ldots,z_n])=z_j/z_i$ on $U_i\cap U_j$. Its dual bundle $\mathcal{O}(1)^*$ is the __tautological line bundle__ (or universal bundle) usually denoted by $\mathcal{O}(-1)$ and the tensor powers are $\mathcal{O}(n)=\mathcal{O}(1)^{\otimes n}$, $\mathcal{O}(-n)=\mathcal{O}(-1)^{\otimes n}$ for $n\geq 0$. The total space of the tautological line bundle can be identified with $\mathbb{C}^{n+1}$ and the projection is exactly $(z_0,\ldots,z_m)\mapsto[z_0,\ldots,z_m]$, i.e. the fiber over $[z_0,\ldots,z_m]$ is the line $\{(\lambda z_0,\ldots,\lambda z_n), 0 \neq \lambda\in \mathbb{C}\}$. The __[[canonical line bundle]]__ $K = \Lambda^n T^* \mathbb{P}^n$ equals $\mathcal{O}(-n-1)$. 

The bundles $\mathcal{O}(n)$ are holomorphic if $k=\mathbb{C}$. The sheaves of (regular or holomorphic) sections are also denoted as $\mathcal{O}(n)$ and are said to be the _twists_ of the structure sheaf $\mathcal{O}$; they restrict to the equally denoted sheaves on any projective subvariety and these restrictions up to an isomorphism do not depend on a particular embedding into a particular projective space. 

## Related concepts

* [[hyperplane]]

* [[classifying space]]

* [[canonical line bundle]]

* [[tautological line bundle]]

[[!redirects hyperplane line bundles]]

