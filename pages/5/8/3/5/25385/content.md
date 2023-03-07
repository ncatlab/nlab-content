
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[quantum information theory]] a pair of [[orthonormal basis|orthonormal]] [[linear bases]] of a given (usually [[finite number|finite]]-[[dimension of a vector space|dimensional]]) [[Hilbert space]] [[space of quantum states|of quantum states]] is called *mutually unbiased* if the [[absolute value]] of the [[inner products]] of any one element in one basis with any in the other basis all have the same value.

## Examples

In the 2-dimensional Hilert space of [[qbits]] $\simeq \mathbb{C}^2$ the pair consisting of

* the "measurement basis" ([[Pauli-Z]]-[[eigenstates]])

  $$
    \Big\{
      \left\vert 0 \right\rangle
      ,\, 
      \left\vert 1 \right\rangle 
    \Big\}
  $$ 

* the [[Hadamard gate|Hadamard]] basis ([[Pauli-X]]-[[eigenstates]])

  $$
    \Big\{
      \tfrac{1}{\sqrt{2}}
      \big(
        \left\vert 0 \right\rangle 
        \pm
        \left\vert 1 \right\rangle 
      \big)
    \Big\}
  $$ 

are (each [[orthonormal basis|orthonormal]] and) mutually unbiased: The [[absolute value]]-[[square]] of the mutual [[inner product]] is

$$
  \tfrac{1}{\sqrt{2}}
  \left\vert
  \left\langle 
     b 
  \vert
     0
  \right\rangle
  \,\pm\,
  \left\langle 
     b 
  \vert
     1
  \right\rangle
  \right\vert
  \;\;\;
    =
  \;\;\;
  \tfrac{1}{\sqrt{2}}
$$

for all $b \,\in\, \{0,1\}$ and $\pm \in \{+,-\}$.

## Related concepts

* [[quantum measurement]]

* [[ZX-calculus]]

## References

Original articles:

* [[William K. Woooters]], [[Brian D. Fields]], *Optimal state-determination by mutually unbiased measurements*, Annals of Physics **191** 2 (1989) 363-381 &lbrack;<a href="https://doi.org/10.1016/0003-4916(89)90322-9">doi:10.1016/0003-4916(89)90322-9</a>&rbrack;

Review:

* [[Ingemar Bengtsson]], *Three ways to look at mutually unbiased bases*, AIP Conference Proceedings **889** (2007) 40-51 &lbrack;[arXiv:quant-ph/0610216](https://arxiv.org/abs/quant-ph/0610216), [doi:10.1063/1.2713445](https://doi.org/10.1063/1.2713445)&rbrack;

See also:

* Wikipedia, *[Mutually unbiased bases](https://en.wikipedia.org/wiki/Mutually_unbiased_bases)*


