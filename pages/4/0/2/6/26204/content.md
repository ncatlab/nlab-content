
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In [[quantum information theory]], by the *maximally mixed state* of a [[quantum systems]] represented by a [[finite-dimensional Hilbert space]] $\mathscr{H}$ one means the [[mixed state]] whose [[density matrix]] is a multiple of the [[identity matrix]] on $\mathscr{H}$. 

Hence if $\big(\left\vert w \right\rangle\big)_{w \colon W}$ is any [[orthonormal linear basis]] for $\mathscr{H}$, then the maximally mixed state is (in [[bra-ket notation]]) given by

$$
  \frac{1}{dim(\mathscr{H})}
  \,
  \underset{w}{\sum}
  \left\vert w \right\rangle
  \left\langle w \right\vert
  \;\;\colon\;\;
  \mathscr{H} \otimes \mathscr{H}^\ast
  \,,
$$

representing the uniform [[probability distribution]] on $W$.

## Properties

### Relation to quantum channels

A [[quantum channel]] which preserves the maximally mixed state is called a *[[unital quantum channel]]*.

A [[quantum channel]] with an [environmental representation](quantum+channel#QuantumChannelsAndDecoherence) given by coupling to a maximally mixed state of the environment is called a *[[unistochastic quantum channel]]* or (ambiguously) *noisy quantum operation*. Such operation on single [[qbits]] constitute the "[[DQC1]]-model" of [[quantum computation]].

## Related concepts

* [[open quantum systems]]

* [[quantum noise]]

## References

See references at *[[unistochastic quantum channel]]*.



[[!redirects maximally mixed quantum states]]

[[!redirects maximally mixed state]]
[[!redirects maximally mixed states]]



