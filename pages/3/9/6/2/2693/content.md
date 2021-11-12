

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[model category]] structure on [[cosimplicial objects]] in unital, [[commutative algebras]] over some [[field]] $k$.

Under the [[monoidal Dold-Kan correspondence]] this is [[Quillen equivalence|Quillen equivalent]] to the [[model structure on dg-algebras|model structure on commutative non-negative cochain dg-algebras]].


## The model structure

Let $k$ be a [[field]] of [[characteristic zero]].

+-- {: .num_defn #CosimplicalCommutativeAlgebras}
###### Definition


Write $cAlg_k^\Delta$ for the [[category]] of [[cosimplicial objects]] in the [[category]] of unital, [[commutative algebras]] over $k$. 


=--

+-- {: .num_remark #ComparisonFunctors}
###### Remark

Sending $k$-[[associative algebras|algebras]] to their underlying $k$-[[modules]] yields a [[forgetful functor]] 

$$
  U \colon cAlg_k^\Delta \longrightarrow k Mod^\Delta
$$

from cosimplicial $k$-allgebras (def. \ref{CosimplicalCommutativeAlgebras}) to [[cosimplicial objects]] in $k$-[[vector spaces]].

Moreover, the [[Dold-Kan correspondence]] provides the [[normalized cochain complex]] functor

$$
  N \colon k Mod_k^\Delta \to Ch^{\geq 0}(k)
$$

from [[cosimplicial objects|cosimplicial]] $k$-[[vector spaces]] to [[cochain complexes]] (i.e. with [[differential]] of degree +1) in non-negative degrees.


=--

+-- {: .num_prop}
###### Proposition

Say that morphism $f \colon A \to B$ in $cAlg_k^{\Delta}$ (def. \ref{CosimplicalCommutativeAlgebras}) is  

1. a _weak equivalence_ if its image $N(U(f)) \colon N(U(A)) \to N(U(B))$ under the comparison functors from remark \ref{ComparisonFunctors} is a [[quasi-isomorphism]] in $Ch^{\geq 0}(k)$;

1.a _fibration_ if $f$ is an [[epimorphism]] (i.e. degreewise a [[surjection]]).

Then 

1. this defines a [[model category]] structure, to be called the _projective model structure_ on comsimplicial commutative $k$-algebras. $(cAlg_k^\Delta)_{poj}$.

1. this is a [[cofibrantly generated model category]]

1. and a [[simplicial model category]].

=--

e.g. [To&#235;n 00, theorem 2.1.2](#Toen00)

+-- {: .proof}
###### Proof

The first two statements follow by observing that $(cAlg_k^{\Delta})_{proj} is$the [[transferred model structure]] along the [[forgetful functor]] $U \circ N$ from remark \ref{ComparisonFunctors} of the [[projective model structure on chain complexes]], by [this prop.](transferred+model+structure#SufficientConditions).

The third statement is the content of prop. \ref{SimplicialModelStructure} below.

=--


## Properties

### Simplicial model category structure

There is also the structure of an [[sSet]]-[[enriched category]] on $cAlg_k^\Delta$ (def. \ref{cAlgDelta})

+-- {: .num_defn #cAlgDelta}
###### Definition

For $X$ a [[simplicial set]] and $A \in Alg_k^{\Delta}$ let $A^X  \in Alg_k^\Delta$ be the corresponding $A$-valued [[cochains on simplicial sets]]

$$
  A^X \;\colon\; [n]  \mapsto (A_n)^{X_n} = \underset{X_n}{\prod} A_n
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


If we write $C(X) \coloneqq Hom_{Set}(X_\bullet,k)$ for the cosimplicial algebra of [[cochains on simplicial sets]] then for $X$ degreewise finite this may be written as

$$
  A^X = A \otimes C(X)
$$ 

where the tensor product is the degreewise tensor product of $k$-algebras.

=--

See also [Castiglioni-Cortinas 03, p. 10] (#CastiglioniCortinas03).

+-- {: .num_defn}
###### Definition


For $A,B \in Alg_k^\Delta$ define the [[sSet]]-[[hom-object]] $Alg_k^\Delta(A,B)$ by

$$
  Alg_k^\Delta(A,B) \coloneqq Hom_{sSet}(A, B^{\Delta[\bullet]})
  = Hom_{sSet}(A, B \otimes C(\Delta[\bullet]))
  \in sSet
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For $B \in Alg_k$ regarded as a constant cosimplicial object under the canonical embedding $Alg_k \hookrightarrow Alg_k^\Delta$ we have

$$
  Alg_k^\Delta(A, B^{\Delta[n]})
  =
  Alg_k^\Delta(A, B \otimes C(\Delta[n]))
  \simeq
  Alg_k(A_n,B)
  \,.
$$ 

=--


+-- {: .proof}
###### Proof

Let $f : A \to B \otimes C(\Delta[n])$ be a morphism of cosimplicial algebras and write

$$
  f_n : A_n \to B 
$$

for the component of $f$ in degree $n$ with values in the copy $B = B \otimes k$ of functions $k$ on the unique non-degenerate $n$-[[simplex]] of $\Delta[n]$. The $n+1$ coface maps $C(\Delta[n])_n \leftarrow C(\Delta[n])_{n-1}$ obtained as the pullback of the $(n+1)$ face inclusions $\Delta[n-1] \to \Delta[n]$  restrict on the non-degenerate $(n-1)$-cells to the $n+1$ projections $k \leftarrow k^{n+1} : p_i$.

Accordingly, from the naturality squares for $f$

$$
  \array{
    A_n &\stackrel{f_n}{\to}& B
    \\
    \uparrow^{\mathrlap{\delta_i}} && \uparrow^{\mathrlap{p_i}}
    \\
    A_{n-1} &\stackrel{f_{n-1}}{\to}& B^{n+1}
  }
$$

the bottom horizontal morphism is fixed to have components

$f_{n-1} = (f_n \circ \delta_0, \cdots, f_n \circ \delta_n)$

in the functions on the non-degenerate simplices. 

By analogous reasoning this fixes all the components of $f$ in all lower degrees with values in the functions on degenerate simplices.




=--



The above [[sSet]]-[[enriched category theory|enrichment]] makes $cAlg_k^\Delta$ into a [[simplicially enriched category]] which is [[copower|tensored]] and [[power|cotensored]] over $sSet$.

And this is compatible with the model category structure: 

+-- {: .num_prop #SimplicialModelStructure}
###### Proposition

With the definitions as above, $(cAlg_k^\Delta)_{proj}$ is a [[simplicial model category]].

=--


[To&#235;n 00, theorem 2.1.2](#Toen00)



### Relation to the model structure on cochain dgc-algebras

Under the [[monoidal Dold-Kan correspondence]] this is related to the [[model structure on dg-algebras|model structure on commutative non-negative cochain dg-algebras]].

## References


Details are in 

* {#Toen00} [[Bertrand Toën]], section 2.1 of _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

See also

* [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_

The generalization to arbitrary cosimplicial rings is proposition 9.2 of

* {#CastiglioniCortinas03} J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv:math/0306289](http://arxiv.org/abs/math/0306289))

There also aspects of relation to the [[model structure on dg-algebras]] is discussed. (See [[monoidal Dold-Kan correspondence]] for more on this).

[[!redirects model structure on cosimplicial algebras]]
