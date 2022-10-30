
# $\lambda$-Abstraction
* table of contents
{: toc}

## Idea

$\lambda$-Abstraction is the process of interpreting a formula for a function (or operation) as defining an actual [[function]].


## Notation

If in a [[context]] with a [[free variable]] $x$ of [[type]] $A$ we have a [[term]] $t$ of type $B$, then
\[ \lambda_{x\colon A} t \label{implicit} \]
is a term (in a context *without* the free variable) of the [[dependent product]] type $\prod_{x\colon A} B$.  If $B$ is defined in the context without the free variable, then this expression is a term of the [[function type]] $A \to B$ or $B^A$.

Often we make the presence of the free variable explicit in the notation, saying that $t[x]$ is a term of type $B[x]$; then
\[ \lambda_{x\colon A} t[x] ,\label{explicit} \]
a term of the dependent product $\prod_{x\colon A} B[x]$.  Or if $t[x]$ is a term of the constant type $B$, then the same expression is a term of the function type $A \to B$.


## In set theory

Although developed for [[type theory]] and commonly used in [[computer science]], $\lambda$-abstraction makes sense in ordinary mathematics usually based on [[set theory]].  If the types $A$ and $B$ are interpreted as [[sets]] and we define [[functions]] as certain [[subsets]] of [[cartesian products]], then the notation (eq:explicit) refers to
$$ \{ (x,y) \in A \times B \;|\; y = t[x] \} $$
(at least in the simple case where $B$ is constant).


[[!redirects lambda abstraction]]
[[!redirects lambda abstractions]]
[[!redirects lambda-abstraction]]
[[!redirects lambda-abstractions]]
[[!redirects ? abstraction]]
[[!redirects ? abstractions]]
[[!redirects ∞-abstraction]]
[[!redirects ∞-abstractions]]

[[!redirects function abstraction]]
[[!redirects function abstractions]]
