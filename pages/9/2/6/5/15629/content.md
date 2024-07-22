
# Contents
* table of contents
{: toc}

## Idea

Let $K$ be a [[local field]] with [[ring of integers]] $\mathcal{O}$, and let $G$ be a [[geometrically connected scheme|geometrically connected]] [[split reductive group]] over $\mathcal{O}$. The _spherical [[Hecke algebra]]_ is the [[ring]] $\mathcal{H}$ of $\mathbf{Z}$-valued compactly supported functions on the [[double coset]] space $G(\mathcal{O}) \backslash G(K) / G(\mathcal{O})$ under [[convolution]]. Although convolution algebras are generally non-commutative, an argument known as [[Gelfand's trick]] implies that $\mathcal{H}$ is [[commutative]].

The _Satake isomorphism_ is a ring isomorphism

\[\mathcal{H} \otimes \mathbf{Z}[q^{\pm 1/2}] \simeq R({}^L G) \otimes \mathbf{Z}[q^{\pm 1/2}]\]

where

* $q$ denotes the cardinality of the [[residue field]] of $\mathcal{O}$,

* ${}^L G$ denotes the [[Langlands dual group]] of $G$, a [[split reductive group]] over $\mathbf{C}$, and

* $R({}^L G) = K_0(\mathrm{Rep}({}^L G))$ denotes the [[representation ring]] of ${}^L G$.

The _geometric Satake equivalence_ categorifies the Satake isomorphism in the setting of local [[geometric Langlands correspondence|geometric Langlands]]. To be precise, let now $G$ denote a [[reductive algebraic group|reductive group]] over $\mathbf{C}$ with Langlands dual group ${}^L G$ also over $\mathbf{C}$. Let $\mathcal{L}G$ denote the [[loop group]] of $G$ and let $\mathcal{L}^+G$ denote the arc group of $G$. Then one has an equivalence of [[symmetric monoidal]] [[abelian categories]]

\[\mathrm{DMod}(\mathrm{Gr}_G)^{\mathcal{L}^+G} \simeq \mathrm{Rep}({}^L G)\]

where:

* $\mathrm{Gr}_G = \mathcal{L}G/\mathcal{L}^+G$ is the [[affine Grassmannian]] of $G$,

* $\mathrm{DMod}(\mathrm{Gr}_G)^{\mathcal{L}^+G}$ denotes the category of $\mathcal{L}^+G$-equivariant [[D-modules]], with the convolution monoidal structure, and

* $\mathrm{Rep}({}^L G)$ denotes the category of algebraic [[geometric representation theory|representations]] of ${}^L G$.

The construction of the correct commutativity constraint on the left hand side of this equivalence is subtle--we warn that this is an additional data and not merely a property of the monoidal structure.

## Related concepts

* [[geometric Langlands correspondence]]

* [[categorification via groupoid schemes]] -- [section on geometric Satake](categorification+via+groupoid+schemes#GeometricSatake)

## References

* Wikipedia, _[Satake isomorphism](http://en.wikipedia.org/wiki/Satake_isomorphism)_

* Benedict Gross, _On the Satake isomorphism_ ([pdf](http://www.math.harvard.edu/~gross/preprints/sat.pdf))

* [[Dennis Gaitsgory]], [Graduate Seminar. Geometric Representation theory. Fall 2009--Spring 2010](http://www.math.harvard.edu/~gaitsgde/grad_2009/), _Feb. 23: Affine Grassmannian-II: the Satake equivalence (Ryan Reich)_ ([pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Feb23%28Gr-II%29.pdf))

* example 1.7 in these rough notes, apparently taken in some talk by [[Jacob Lurie]]: [[lurie.pdf:file]]


[[!redirects geometric Satake equivalence]]
[[!redirects geometric Satake equivalences]]

[[!redirects Satake isomorphism]]
[[!redirects Satake isomorphism]]

[[!redirects Satake equivalence]]
[[!redirects Satake equivalences]]

[[!redirects geometric Satake]]