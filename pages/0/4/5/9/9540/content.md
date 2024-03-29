
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _Hilbert $C^\ast$-bimodule_ adapts the notion of [[bimodules]] over [[associative algebras]] to [[operator algebra]]/[[C-star-algebra]] theory.


## Definition

+-- {: .num_defn}
###### Definition

For $A,B \in $ [[C*Alg]] two [[C-star algebras]], an $(A,B)$-*Hilbert $C^\ast$-bimodule* (or just _Hilbert bimodule_, for short) is 

* a right $B$-[[Hilbert C*-module]] $(N, \langle -,-\rangle)$;

* equipped with a further left $A$-[[representation of a C-star-algebra|representation]] $A \to \mathcal{B}(N)$ by *adjointable operators*, hence such that $\langle a -,- \rangle = \langle -,a^\ast -\rangle$ for all $a \in A$.

A [[isomorphism]] between two $(A,B)$-bimodules $(N_1, \langle -,-\rangle) \to (N_2, \langle -,-\rangle_2)$ is a [[linear operator]] $N_1\to N_2$ which is [[unitary operator|unitary]] with respect to $\langle -,-\rangle_2$.

=--

+-- {: .num_defn #TensorProductOfHilbertBimodules}
###### Definition

Given an $(A,B)$-Hilbert bimodule $(N_1, \langle -,-\rangle_1)$ and a $(B,C)$-Hilbert bimodule $(N_2, \langle -,-\rangle_2)$, the **tensor product of Hilbert bimodules** $N_1 \otimes_B N_2$ is the $(A,C)$-Hilbert bimodule obtained from the ordinary (algebraic) [[tensor product of modules]] over $\mathbb{C}$ $N_1 \otimes_{\mathbb{C}} N_2$ by

1. equipping it with the $C$-valued [[inner product]] defined by

   $$
     \left\langle \xi_1 \otimes \eta_1 , \xi_2 \otimes \eta_2\right\rangle
     \coloneqq
     \left\langle \eta_1, \left\langle \xi_1, \xi_2\right\rangle \cdot \eta_2 \right\rangle
     \,.
   $$

1. forming the [[quotient]] by the submodule of elements $v$ for which $\langle v,v\rangle = 0$;

1. forming the [[completion]] of this quotient with respect to the induced [[norm]].

=--

+-- {: .num_remark}
###### Remark

Def. \ref{TensorProductOfHilbertBimodules} really does yield a kind of tensor product over $B$: elements of the form

$$
  v \cdot b \otimes w - v \otimes b \cdot w
$$

are in the submodule that it being divided out, because

$$
  \begin{aligned}
    \langle 
      v \cdot b \otimes w - v \otimes b \cdot w \;,\; 
      v \cdot b \otimes w - v \otimes b \cdot w 
    \rangle
     & \coloneqq 
    \langle w , \langle v \cdot b, v \cdot b\rangle \cdot w \rangle
     \\
     & + 
     \langle b \cdot w, \langle v,v\rangle \cdot b \cdot w\rangle
     \\
     &
     -
     \langle w, \langle v\cdot b, v \rangle \cdot b \cdot w\rangle
     \\
     &
     -
     \langle b \cdot w, \langle v, v \cdot b \rangle \cdot w\rangle
     \\
     & = (1+1-1-1) \langle w , \langle v \cdot b, v \cdot b\rangle \cdot w \rangle

     \\
     & = 0
  \end{aligned}
  \,,
$$

where we use that by definition the left actions are required to have adjoints, so that for instance

$$
  \begin{aligned}
    \langle b \cdot w , \langle v,v\rangle \cdot b \cdot w\rangle
    & =
    \langle w , b^\ast \cdot \langle v,v\rangle \cdot b \cdot t\rangle 
    \\
    & =    
    \langle w , \langle v \cdot b,v \cdot b\rangle \cdot w\rangle 
  \end{aligned}
$$

=--


+-- {: .num_prop}
###### Proposition

There is a [[(2,1)-category]] $C^\ast Alg_b$ whose

* [[objects]] are [[C*-algebras]];

* [[1-morphisms]] are Hilbert bimodules;

* [[2-morphisms]] are isomorphisms of Hilbert bimodules;

* [[vertical composition]] is the evident composition of intertwiners;

* [[horizontal composition]] is the tensor product of Hilbert bimodules, def. \ref{TensorProductOfHilbertBimodules}.

=--

([Buss-Zhu-Meyer 09](#BussZhuMeyer))

## Examples

An $(\mathbb{C},B)$-Hilbert $C^\ast$-bimodule is equialently just an $B$-[[Hilbert C*-module]].

An $(A, \mathbb{C})$-Hilbert $C^\ast$-bimodule is equivalently just as [[representation of a C-star-algebra]].

## Properties

(...)

## Related concepts

* [[amplimorphism]]

* [[generalized elliptic operator]]

* [[KK-theory]]

* [[C*-correspondence]]


## References

For instance

* [[Sergio Doplicher]], Claudia Pinzari, Rita Zuccante, _The $C^\ast$-algebra of a Hilbert Bimodule_ &lbrack;[arXiv:funct-an/9707006](http://arxiv.org/abs/funct-an/9707006)&rbrack;

* [[Nik Weaver]], _Hilbert bimodules with involution_, Canad. Math. Bull. **44** 3 (2001) 355–369 &lbrack;[arXiv:math/9908119](http://arxiv.org/abs/math/9908119), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/DC7055E821BEA9438350CCB325EA64CA/S0008439500014466a.pdf/hilbert-bimodules-with-involution.pdf)&rbrack;


The tensor product of Hilbert bimodules and the induced [[2-category]] structure is discussed in 

* {#BussZhuMeyer} Alcides Buss, [[Chenchang Zhu]], [[Ralf Meyer]], _A higher category approach to twisted actions on $C^\ast$-algebras_ ([arXiv:0908.0455](http://arxiv.org/abs/0908.0455))
 

[[!redirects Hilbert bimodules]]

[[!redirects Hilbert C-star-bimodule]]
[[!redirects Hilbert C-star-bimodules]]
[[!redirects Hilbert C-*-bimodule]]
[[!redirects Hilbert C-*-bimodules]]
[[!redirects Hilbert C*-bimodule]]
[[!redirects Hilbert C*-bimodules]]
