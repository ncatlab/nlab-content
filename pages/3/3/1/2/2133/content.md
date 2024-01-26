
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
  B(x,y)  
    \,=\, 
  tr\big(
    ad(x) \circ ad(y)
  \big)
  \,,
$$

where 

$$
  ad(x) \,\coloneqq\, 
  [x,-]
  \,:\,
  \mathfrak{g}
    \longrightarrow 
  \mathfrak{g}
$$ 

is the [[linear map]] given by the [[adjoint action]] of $x$, hence the value on $x$ of the [[adjoint representation]] $ad \colon \mathfrak{g} \to Der(\mathfrak{g})$.

If $\{t_a\}$ is a [[linear basis]] for $\mathfrak{g}$ and $\{C^a{}_{b c}\}$ are the structure constants of the Lie algebra in this basis (defined by $[t_a, t_b] = \sum_c C^c_{a b} t_c$), then 

$$
  B(t_a, t_b) 
    \,=\, 
  \sum_{c,d} C^c{}_{a d} C^{d}_{b c}
  \,.
$$


## Properties
 
The Killing form is an _[[invariant polynomial]]_ in that 

$$
  B\big([x,y],z\big)
  \,=\,
  B\big(x, [y,z] \big)
$$

for all $x,y,z \in \mathbb{g}$. This follows from the cyclic invariance of the [[trace]]],

For complex Lie algebras $\mathfrak{g}$, nondegeneracy of the Killing form (i.e. being the metric making $\mathfrak{g}$ a [[metric Lie algebra]]) is equivalent to [[semisimple Lie algebra|semisimplicity]] of $\mathfrak{g}$. 

{#ForSimple} For [[simple object|simple]] complex Lie algebras, or compact forms of real Lie algebras, any invariant nondegenerate symmetric bilinear form is proportional to the Killing form. Indeed, one often uses a normalisation of the Killing form on a simple Lie algebra that makes it a positive definite [[inner product space|inner product]], such that the algebra elements corresponding to long roots (under the isomorphism $\mathfrak{g}^*\simeq \mathfrak{g}$ induced by the original Killing form) have length $\sqrt{2}$. Both the Killing form and this normalised version give a simple Lie algebra a canonical structure of a [[metric Lie algebra]], one positive definite, and one negative definite. This normalised Killing form is sometimes called, following Pressley and Segal, the **basic inner product** on the Lie algebra.

Here are the basic inner products for the compact forms of the simple real matrix Lie algebras, from ([Wang–Ziller 1985](#Wang-Ziller_85),  page 583):

* $\mathfrak{su}(n)$: $\langle X,Y\rangle = -tr_{\mathbb{C}}(XY)$.
* $\mathfrak{so}(3)$: $\langle X,Y\rangle = -tr_{\mathbb{R}}(XY)/4$.
* $\mathfrak{so}(n)$, $n\geq 5$: $\langle X,Y\rangle = -tr_{\mathbb{R}}(XY)/2$.
* $\mathfrak{sp}(n)$: $\langle X,Y\rangle = -Tr(XY) = -2\Re tr_{\mathbb{H}}(XY)$. 

The trace $tr_{k}(\cdot)$ here is the ordinary trace for matrices over the division ring $k$, and the _reduced trace_ $Tr(\cdot)$ for $n\times n$ quaternionic matrices is the composite of the embedding into $2n\times 2n$ complex matrices (thinking of $\mathbb{H}\simeq \mathbb{C}\oplus j\mathbb{C}$), and the ordinary trace of complex matrices.



## Generalizations

Sometimes one considers more generally a Killing form $B_\rho$ for a more general faithful finite-dimensional [[representation]] $\rho$, $B_\rho(x,y)  = tr\big(\rho(x)\rho(y)\big)$. If the Killing form is nondegenerate and $x_1,\ldots,x_n$ is a basis in $L$ with $x_1^*,\ldots,x_n^*$ the dual basis of $\mathfrak{g}^*$, with respect to the Killing form for $\rho$, then the canonical element $r = \sum_i x_i\otimes x_i^*$ defines the __[[Casimir operator]]__ $C(\rho) =(\rho\otimes\rho)(r)$ in the representation $\rho$; regarding that the representation is faithful, if the ground field is $\mathbb{C}$, by [[Schur's lemma]] $C(\rho)$ is a nonzero scalar operator. Instead of Casimir operators in particular faithful representations it is often useful to consider an analogous construction within the [[universal enveloping algebra]], the __[[Casimir element]]__ in $U(\mathfrak{g})$.


## References

For a general discussion see:

* Wikipedia, *[Killing form](https://en.wikipedia.org/wiki/Killing_form)*

Careful discussion around normalisation and related data is in:

* {#Wang-Ziller_85} McKenzie Y. Wang and Wolfgang Ziller, _On normal homogeneous Einstein manifolds_, Annales scientifiques de l’École Normale Supérieure, Série 4 **18** (1985), no. 4, 563–633.


[[!redirects Killing forms]]


[[!redirects Cartan-Killing form]]
[[!redirects Cartan-Killing forms]]



