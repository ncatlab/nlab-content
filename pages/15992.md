
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

$$
  \langle \alpha, \beta\rangle
  \coloneqq
  \frac{1}{{\vert G \vert}}
  \underset{g \in G}{\sum} \alpha(g) \overline{\beta(g)}
  \,.
$$

The _[[Schur orthogonality relation]]_ is the statement that the [[irreducible representation|irreducible]] [[group characters]] $\{\chi_i\}_i$ form an [[orthonormal basis]] of the space of [[class functions]] under this [[inner product]]:

$$
  \langle \chi_i, \chi_j \rangle 
  = 
  \left\{
    \array{
       1 & if \; i = j
       \\
       0 & otherwise
    }
  \right.
$$


(e.g. [Fulton & Harris 91, Thm. 2.12](#FultonHarris91), [tom Dieck 09, Prop. 2.2.1 & (2.3.3)](#tomDieck09))


Conversely, the sum over all ([[isomorphism classes]]) of [[irreducible characters]] $\chi_i$ yields

$$
  \underset{\chi_i}{\sum}
  \chi_i(g)
  \cdot 
  \overline{
    \chi_i(h)
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
$$

(e.g. [Fulton & Harris 91, Ex. 2.21](#FultonHarris91), [tom Dieck 09, Prop. 2.2.1 & (2.3.3)](#tomDieck09))

## Related concepts

* [[Schur orthogonality relation]]

* [[1d Dijkgraaf-Witten theory]]

## References

Textbook accounts:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], _Representation Theory: a First Course_, Springer, Berlin, 1991 ([doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9))

Lecture notes

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf), [[tomDieckRepresentationTheory.pdf:file]])


* Andrei Yafaev, _Characters of finite groups_ ([pdf](http://www.ucl.ac.uk/~ucahaya/Characters.pdf))

See also:

* Wikipedia, _[Schur orthogonality relation](http://en.wikipedia.org/wiki/Schur_orthogonality_relations)_ 

[[!redirects Schur orthogonality]]

[[!redirects Schur orthogonality relations]]

[[!redirects Schur inner product]]
