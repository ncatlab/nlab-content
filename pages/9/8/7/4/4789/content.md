+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

* [[∞-Lie algebroid cocycle]]

* **Chern-Simons element**

* [[invariant polynomial]]

***

#Contents#
* table of contents
{:toc}

## Definition

For $\mathfrak{g}$ an [[∞-Lie algebra]] or more generally [[∞-Lie algebroid]], $\mu \in CE(\mathfrak{g})$ a [[∞-Lie algebra cocycle]] and $\langle - \rangle \in W(\mathfrak{g})$ an [[invariant polynomial]], a **Chern-Simons element** exhibiting the _transgression_ between the two is an element

$$
  cs \in W(\mathfrak{g})
$$

such that

1. we have $d_{W(\mathfrak{g})} cs = \langle -\rangle$

1. and $cs|_{CE(\mathfrak{g})} = \mu$

where the restriction is along the canonical morphism $W(\mathfrak{g}) \to CE(\mathfrak{g})$ from the [[Weil algebra]] to the [[Chevalley-Eilenberg algebra]].

We may equivalently express these two conditions as asserting the existence of a [[commuting diagram]] of the form

$$
  \array{
    CE(\mathfrak{g}) &\leftarrow& CE(b^{n-1} \mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}& W(b^{n-1} \mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(b^{n-1} \mathbb{R})
  }
  \,.
$$

## Chern-Simons forms


The term _Chern-Simons element_ indicates that when composed with [[∞-Lie algebra valued forms]] on some $U \in $ [[Diff]] 

$$
  \array{
    \Omega^\bullet(U \times \Delta^k)_{vert}
    &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U \times \Delta^k)
    &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)
    &\stackrel{\langle -\rangle}{\leftarrow}&
    inv(\mathfrak{g})
  }
$$

these element produces the corresponding (generalized) [[Chern-Simons form]]

$$
  \Omega^\bullet(U \times \Delta^k)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{cs}{\leftarrow}
  W(b^{n-1}\mathbb{R})
  :
  CS(A)
  \,.
$$

This is part of the [[∞-Chern-Weil homomorphism]].

## Examples

### Classical CS-forms

For $\mathfrak{g}$ a [[semisimple Lie algebra]], $\langle - \rangle$ the [[Killing form]] and $\mu = \langle -,[-,-]\rangle$ the corresponding cocycle, the above reproduces the classical Chern-Simons 3-form

$$
  CS(A) = \langle A \wedge d A\rangle + c \langle A \wedge [A \wedge A]\rangle 
  \,.
$$

### Lie algebroid CS-forms

For $\mathfrak{g}$ a [[schreiber:symplectic ∞-Lie algebroid]] the Chern-Simons elements of the canonical bilinear invariant polynomial yield the integrands of the associated [[action functional]]s. 

See for instance [[Poisson Lie algebroid]] for details.


[[!redirects Chern-Simons elements]]