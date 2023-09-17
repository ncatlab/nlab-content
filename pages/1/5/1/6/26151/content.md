
\tableofcontents

## Idea

In [[dependent type theory]], there are two notions of [[equality]], 

1. *strict* or *[[judgmental equality]]*,

1. *weak* or *[[typal equality]]*. 

Accordingly there are two corresponding notions of the [[inverse function]] of a function $f:A \to B$:

1. There are the various notions of *weak* [[inverse functions]], such as [[quasi-inverse functions]] and [[coherent inverse functions]], which is a function $f^{-1}:B \to A$ with [[homotopies]] $h:\prod_{x:A} f^{-1}(f(x)) =_A x$ and $k:\prod_{y:B} f(f^{-1}(y)) =_B y$ and possibly other conditions and structure.

1. There is the notion of *strict* inverse function, which is a function $f^{-1}:B \to A$ with [[judgmental equalities]] $x:A \vdash f^{-1}(f(x)) \equiv x:A$ and $y:B \vdash f(f^{-1}(y)) \equiv y:B$. The other structures are unimportant since non-trivial paths for weak inverse functions reduce to [[reflexivity]] for $x:A$ or $y:B$ for strict inverse functions. 

## Examples

* If [[copy types]] are defined using judgmental [[computation rules]] and [[uniqueness rules]], then the constructor and eliminator functions are strict inverse functions of each other. 

* In [[Mike Shulman]]'s [[higher observational type theory]] the $\mathrm{idtoequiv}$ function for the [[univalent universes]] has a strict inverse function. 

## See also

* [[judgmental equality]]

* [[inverse function]]

[[!redirects strict inverse functions]]
[[!redirects strict inverse function]]