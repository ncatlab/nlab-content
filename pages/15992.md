
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[finite group]] $G$ of [[cardinality]] ${\vert G \vert}$, then the [[complex number|complex]] valued [[class functions]]  $\chi \colon G \to \mathbb{C}$ have an [[inner product]] -- the _Schur inner product_ -- given by

\[
  \langle \alpha, \beta\rangle
  \coloneqq
  \frac{1}{{\vert G \vert}}
  \underset{g \in G}{\sum} \alpha(g) \overline{\beta(g)}
  \,.
\]

The _[[Schur orthogonality relation]]_ is the statement that the [[complex numbers|complex]] [[irreducible representation|irreducible]] [[group characters]] $\{\chi^{(a)}\}_a$ form an [[orthonormal basis]] of the space of [[class functions]] under this [[inner product]]:

\[
  \langle \chi^{(a)}, \chi^{(b)} \rangle 
  = 
  \left\{
    \array{
       1 & if \; a = b
       \\
       0 & otherwise
    }
  \right.
\]


(e.g. [Fulton & Harris 91, Thm. 2.12](#FultonHarris91), [tom Dieck 09, Prop. 2.2.1 & (2.3.3)](#tomDieck09))

In fact, this holds also at the level of complex [[irreducible representations]] $\rho^{(a)}$ ("grand Schur orthogonality"), regarded for each $g \in G$ as [[unitary matrices]] $\rho^{(a)}(g) \in U(\chi^{(a)}(e))$ with matrix entries $\big(\rho^{(a)}(g)_{i j}\big)_{i j}$:

\[
  \label{SchurOrthogonalityForIrreps}
  \underset{g \in G}{\sum}
    \rho^{(a)}(g)_{i_1 j_1}
    \cdot 
    \overline{\rho^{(b)}(g)_{i_2 j_2}}
  \;=\;
  \delta^{a b} \delta_{i_1 i_2} \delta_{j_1 j_2}
  \cdot
  \frac{
    \left\vert G \right\vert
  }{
    dim(\rho^{(a)})
  }  
  \,.
\]

(e.g. [tom Dieck 09 (2.2.7)](#tomDieck09))


Conversely, the sum over all ([[isomorphism classes]]) of [[irreducible characters]] $\chi_i$ yields:

\[
  \underset{\chi^{(a)}}{\sum}
  \chi^{(a)}(g)
  \cdot 
  \overline{
    \chi^{(a)}(h)
  }
  \;=\;
  \left\{
  \array{
    \left\vert Central_G(g) \right\vert
    &
    \text{if} \; h,g \;\text{are conjugate}
    \\
    0 & \text{otherwise}
  }
  \right.
\]

(e.g. [Fulton & Harris 91, Ex. 2.21](#FultonHarris91), [tom Dieck 09, Prop. 2.2.1 & (2.3.3)](#tomDieck09))


## Related concepts

* [[Schur orthogonality relation]]

* [[1d Dijkgraaf-Witten theory]]

## References

Textbook accounts:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], _Representation Theory: a First Course_, Springer, Berlin, 1991 ([doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9))

Lecture notes:

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf), [[tomDieckRepresentationTheory.pdf:file]])


* Andrei Yafaev, _Characters of finite groups_ ([pdf](http://www.ucl.ac.uk/~ucahaya/Characters.pdf))

See also:

* Wikipedia, _[Schur orthogonality relation](http://en.wikipedia.org/wiki/Schur_orthogonality_relations)_ 

[[!redirects Schur orthogonality relations]]
[[!redirects Schur orthogonality]]

[[!redirects grand Schur orthogonality relation]]
[[!redirects grand Schur orthogonality relations]]
[[!redirects grand Schur orthogonality]]

[[!redirects Schur inner product]]
