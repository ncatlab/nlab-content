
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

## Disambiguation

In the [[dependent type theory]] literature, there are different kinds of [[types]] which are called *heterogeneous identity types* or *dependent identity types*:

* *[[indexed heterogeneous identity types]]* are a variant of [[identity types]] for a [[type family]] and parameterized by a pair of elements and a [[identification]] between them; hence the name "indexed"

$$x:A, y:A, p:x =_A y, u:B(x), v:B(y) \vdash u =_{B}^{(x, y, p)} v$$

* *[[fibered heterogeneous identity types]]* are a variant of [[identity types]] for a [[type family]] and parameterized by only a pair of elements. They are equivalent to the [[dependent sum]] of indexed heterogeneous identity types over all relevant [[identifications]]; hence the name "fibered" 

$$x:A, y:A, u:B(x), v:B(y) \vdash u =_{B}^{(x, y)} v \simeq \sum_{p:x = y} u =_{B}^{(x, y, p)} v$$

category: disambiguation

[[!redirects dependent identity type]]
[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]
[[!redirects dependent heterogeneous identity type]]
[[!redirects dependent heterogeneous identity types]]
[[!redirects non-dependent heterogeneous identity type]]
[[!redirects non-dependent heterogeneous identity types]]

[[!redirects weak dependent identity type]]
[[!redirects weak dependent identity types]]
[[!redirects weak heterogeneous identity type]]
[[!redirects weak heterogeneous identity types]]
[[!redirects weak dependent heterogeneous identity type]]
[[!redirects weak dependent heterogeneous identity types]]
[[!redirects weak non-dependent heterogeneous identity type]]
[[!redirects weak non-dependent heterogeneous identity types]]

[[!redirects strict dependent identity type]]
[[!redirects strict dependent identity types]]
[[!redirects strict heterogeneous identity type]]
[[!redirects strict heterogeneous identity types]]
[[!redirects strict dependent heterogeneous identity type]]
[[!redirects strict dependent heterogeneous identity types]]
[[!redirects strict non-dependent heterogeneous identity type]]
[[!redirects strict non-dependent heterogeneous identity types]]

[[!redirects judgmentally strict dependent identity type]]
[[!redirects judgmentally strict dependent identity types]]
[[!redirects judgmentally strict heterogeneous identity type]]
[[!redirects judgmentally strict heterogeneous identity types]]
[[!redirects judgmentally strict dependent heterogeneous identity type]]
[[!redirects judgmentally strict dependent heterogeneous identity types]]
[[!redirects judgmentally strict non-dependent heterogeneous identity type]]
[[!redirects judgmentally strict non-dependent heterogeneous identity types]]

[[!redirects propositionally strict dependent identity type]]
[[!redirects propositionally strict dependent identity types]]
[[!redirects propositionally strict heterogeneous identity type]]
[[!redirects propositionally strict heterogeneous identity types]]
[[!redirects propositionally strict dependent heterogeneous identity type]]
[[!redirects propositionally strict dependent heterogeneous identity types]]
[[!redirects propositionally strict non-dependent heterogeneous identity type]]
[[!redirects propositionally strict non-dependent heterogeneous identity types]]

[[!redirects dependent identification type]]
[[!redirects dependent identification types]]
[[!redirects heterogeneous identification type]]
[[!redirects heterogeneous identification types]]
[[!redirects dependent heterogeneous identification type]]
[[!redirects dependent heterogeneous identification types]]
[[!redirects non-dependent heterogeneous identification type]]
[[!redirects non-dependent heterogeneous identification types]]

[[!redirects weak dependent identification type]]
[[!redirects weak dependent identification types]]
[[!redirects weak heterogeneous identification type]]
[[!redirects weak heterogeneous identification types]]
[[!redirects weak dependent heterogeneous identification type]]
[[!redirects weak dependent heterogeneous identification types]]
[[!redirects weak non-dependent heterogeneous identification type]]
[[!redirects weak non-dependent heterogeneous identification types]]

[[!redirects strict dependent identification type]]
[[!redirects strict dependent identification types]]
[[!redirects strict heterogeneous identification type]]
[[!redirects strict heterogeneous identification types]]
[[!redirects strict dependent heterogeneous identification type]]
[[!redirects strict dependent heterogeneous identification types]]
[[!redirects strict non-dependent heterogeneous identification type]]
[[!redirects strict non-dependent heterogeneous identification types]]

[[!redirects judgmentally strict dependent identification type]]
[[!redirects judgmentally strict dependent identification types]]
[[!redirects judgmentally strict heterogeneous identification type]]
[[!redirects judgmentally strict heterogeneous identification types]]
[[!redirects judgmentally strict dependent heterogeneous identification type]]
[[!redirects judgmentally strict dependent heterogeneous identification types]]
[[!redirects judgmentally strict non-dependent heterogeneous identification type]]
[[!redirects judgmentally strict non-dependent heterogeneous identification types]]

[[!redirects propositionally strict dependent identification type]]
[[!redirects propositionally strict dependent identification types]]
[[!redirects propositionally strict heterogeneous identification type]]
[[!redirects propositionally strict heterogeneous identification types]]
[[!redirects propositionally strict dependent heterogeneous identification type]]
[[!redirects propositionally strict dependent heterogeneous identification types]]
[[!redirects propositionally strict non-dependent heterogeneous identification type]]
[[!redirects propositionally strict non-dependent heterogeneous identification types]]

[[!redirects dependent equality type]]
[[!redirects dependent equality types]]
[[!redirects heterogeneous equality type]]
[[!redirects heterogeneous equality types]]
[[!redirects dependent heterogeneous equality type]]
[[!redirects dependent heterogeneous equality types]]
[[!redirects non-dependent heterogeneous equality type]]
[[!redirects non-dependent heterogeneous equality types]]

[[!redirects weak dependent equality type]]
[[!redirects weak dependent equality types]]
[[!redirects weak heterogeneous equality type]]
[[!redirects weak heterogeneous equality types]]
[[!redirects weak dependent heterogeneous equality type]]
[[!redirects weak dependent heterogeneous equality types]]
[[!redirects weak non-dependent heterogeneous equality type]]
[[!redirects weak non-dependent heterogeneous equality types]]

[[!redirects strict dependent equality type]]
[[!redirects strict dependent equality types]]
[[!redirects strict heterogeneous equality type]]
[[!redirects strict heterogeneous equality types]]
[[!redirects strict dependent heterogeneous equality type]]
[[!redirects strict dependent heterogeneous equality types]]
[[!redirects strict non-dependent heterogeneous equality type]]
[[!redirects strict non-dependent heterogeneous equality types]]

[[!redirects judgmentally strict dependent equality type]]
[[!redirects judgmentally strict dependent equality types]]
[[!redirects judgmentally strict heterogeneous equality type]]
[[!redirects judgmentally strict heterogeneous paequalityth types]]
[[!redirects judgmentally strict dependent heterogeneous equality type]]
[[!redirects judgmentally strict dependent heterogeneous paequalityth types]]
[[!redirects judgmentally strict non-dependent heterogeneous equality type]]
[[!redirects judgmentally strict non-dependent heterogeneous paequalityth types]]

[[!redirects propositionally strict dependent equality type]]
[[!redirects propositionally strict dependent equality types]]
[[!redirects propositionally strict heterogeneous equality type]]
[[!redirects propositionally strict heterogeneous equality types]]
[[!redirects propositionally strict dependent heterogeneous equality type]]
[[!redirects propositionally strict dependent heterogeneous equality types]]
[[!redirects propositionally strict non-dependent heterogeneous equality type]]
[[!redirects propositionally strict non-dependent heterogeneous equality types]]

[[!redirects dependent identity]]
[[!redirects dependent identities]]
[[!redirects heterogeneous identity]]
[[!redirects heterogeneous identities]]
[[!redirects dependent heterogeneous identity]]
[[!redirects dependent heterogeneous identities]]
[[!redirects non-dependent heterogeneous identity]]
[[!redirects non-dependent heterogeneous identities]]

[[!redirects dependent identification]]
[[!redirects dependent identifications]]
[[!redirects heterogeneous identification]]
[[!redirects heterogeneous identifications]]
[[!redirects dependent heterogeneous identification]]
[[!redirects dependent heterogeneous identifications]]
[[!redirects non-dependent heterogeneous identification]]
[[!redirects non-dependent heterogeneous identifications]]

[[!redirects dependent equality]]
[[!redirects dependent equalities]]
[[!redirects heterogeneous equality]]
[[!redirects heterogeneous equalities]]
[[!redirects dependent heterogeneous equality]]
[[!redirects dependent heterogeneous equalities]]
[[!redirects non-dependent heterogeneous equality]]
[[!redirects non-dependent heterogeneous equalities]]
