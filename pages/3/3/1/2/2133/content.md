
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Killing form_ or _Cartan-Killing form_ is a binary [[invariant polynomial]] that is present on any finite-dimensional [[Lie algebra]].

## Definition


Given a finite-dimensional $k$-[[Lie algebra]] $\mathfrak{g}$ its __Killing form__ $B:\mathfrak{g}\otimes \mathfrak{g}\to k$ is the symmetric bilinear form given by the formula

$$
  B(x,y)  = tr(ad(x)ad(y))
$$

where $ad(x) = [x,-]:\mathfrak{g}\to \mathfrak{g}$ is the $ad$-operator giving the [[adjoint representation]] $ad: \mathfrak{g}\to Der(\mathfrak{g})$.

In terms of a [[basis]]: if $\{t_a\}$ is a basis for $\mathfrak{g}$ and $\{C^a{}_{b c}\}$ the structure constants of the Lie algebra in this basis (defined by $[t_a, t_b] = \sum_c C^c_{a b} t_c$), then 

$$
  B(t_a, t_b) = \sum_{c,d} C^c{}_{a d} C^{d}_{b c}
  \,.
$$

## Properties
 
The Killing form is am _[[invariant polynomial]]_ in that 

$$
  B([x,y],z)=B(x,[y,z])
$$

for all $x,y,z \in \mathbb{g}$. This follows from the cyclic invariance of the [[trace]]],

For complex Lie algebras, nondegeneracy of the Killing form is equivalent to [[semisimple Lie algebra|semisimplicity]] of $\mathfrak{g}$. For [[simple object|simple]] complex Lie algebras, any invariant nondegenerate symmetric bilinear form is proportional to the Killing form. 

## Generalizations

Sometimes one considers more generally a Killing form $B_\rho$ for a more general faithful finite-dimensional [[representation]] $\rho$, $B_\rho(x,y)  = tr(\rho(x)\rho(y))$. If the Killing form is nondegenerate and $x_1,\ldots,x_n$ is a basis in $L$ with $x_1^*,\ldots,x_n^*$ the dual basis of $\mathfrak{g}^*$, with respect to the Killing form for $\rho$, then the canonical element $r = \sum_i x_i\otimes x_i^*$ defines the __[[Casimir operator]]__ $C(\rho) =(\rho\otimes\rho)(r)$ in the representation $\rho$; regarding that the representation is faithful, if the ground field is $\mathbb{C}$, by [[Schur's lemma]] $C(\rho)$ is a nonzero scalar operator. Instead of Casimir operators in particular faithful representations it is often useful to consider an analogous construction within the [[universal enveloping algebra]], the __[[Casimir element]]__ in U(\mathfrak{g}).

[[!redirects Cartan-Killing form]]