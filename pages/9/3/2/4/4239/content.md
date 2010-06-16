
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _Calabi-Yau category_ is a [[horizontal categorification]] of that of [[Frobenius algebra]] -- a _Frobenius [[algebroid]]_ .

## Definition

### 1-categorical

A **Calabi-Yau category** is a [[Vect]]-[[enriched category]] $C$ equipped for each object $c \in C$ with a [[trace]]-like map

$$
  Tr_C : C(c,c) \to k
$$

to the ground field, such that for all objects $d \in C$ the induced pairing

$$
  \langle -,-\rangle_{c,d} :
  C(c,d) \otimes C(d,c) \to k  
$$

given by 

$$
  \langle f,g \rangle = Tr(g \circ f)
$$

is symmetric and non-degenerate.

A Calabi-Yau category with a single object is the same (or rather the [[delooping]]) of a [[Frobenius algebra]].


### $(\infty,1)$-categorical

A **Calabi-Yau $A_\infty$-category** of _dimension_ $d \in \mathbb{N}$ is an [[A-infinity category]] $C$ equipped for each pair $a,b$ of [[object]]s a morphism of [[chain complex]]es

$$
  \langle -,-\rangle_{a,b}
  : 
  C(a,b) \otimes C(b,a)
  \to
  k[d]
$$

such that

1. this is symmetric in that

   $$
    \langle - , - \rangle_{a,b} =  \langle - , - \rangle_{b,a} \circ \sigma_{a,b}
   $$ 

   for $\sigma_{a,b} : C(a,b)\otimes C(b,a) \to C(b,a) \otimes C(a,b)$
   the symmetry [[isomorphism]] of the [[symmetric monoidal category]]
   of [[chain complex]]es;

1. this is cyclically invariant in that for all elements $(\alpha_i)$
   is the respective hom-complexes we have

   $$
     \langle
       m_{n-1}(\alpha_0 \otimes \cdots \otimes \alpha_{n-2}),
       \alpha_{n-1} 
     \rangle
     =
     (-1)^{(n+1)+ |\alpha_0| \sum_{i = 1}^{n-1}|\alpha_i|}
     \langle
       m_{n-1}(\alpha_1 \otimes \cdots \otimes \alpha_{n-2}),
       \alpha_0
     \rangle
     \,.
   $$




## Examples

### Of $A_\infty$ CY-categories


* Let $X$ be a smooth projective [[Calabi-Yau variety]] of dimension $d$.
  Write $D^b(X)$ for the bounded [[derived category]] of 
  that of [[coherent sheaves]] on $X$. 

  Then $D^b(X)$ is a CY  $A_\infty$-category in a naive way:

  * the non-binary composition maps are all trivial;

  * the pairing is [[Serre duality]].

  This is however not the morally correct CY $A_\infty$-structure associated
  with a Calabi-Yau. The correct one is 
  the $A_\infty$-category of complexes of vector bundles 
  on a [[Calabi-Yau space]] ...


* The [[Fukaya category]] associated with a [[symplectic manifold]] $X$.

* [[string topology]]: for $X$ a [[compact manifold|compact]] [[simply connected]] [[oriented]] [[manifold]], its cohomology $H^{\bullet}(X)$ is naturally a Calabi-Yau $A_\infty$-category with a single object.

## Properties

Calabi-Yau $A_\infty$-categories classify [[TCFT]]s. This is where they get there name from, because these TCFTs in turn may be constructed from [[sigma-model]]s whose targets ar [[Calabi-Yau space]]s.

## References

For instance section 7.1 and 7.2 of

* [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_ ([atXiv:math/0509264](http://arxiv.org/abs/math/0509264))

[[!redirects Calabi-Yau categories]]

[[!redirects CY-category]]
[[!redirects CY-categories]]


[[!redirects Calabi-Yau A-infinity category]]
[[!redirects Calabi-Yau A-infinity categories]]

[[!redirects Calabi-Yau A-∞ category]]
[[!redirects Calabi-Yau A-∞ categories]]