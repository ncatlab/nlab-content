[[!redirects Boolean-valued function]]
[[!redirects Boolean-valued functions]]
[[!redirects boolean-valued functions]]
[[!redirects predicate]]
[[!redirects proposition]]

A __boolean-valued function__ is a function of type $f : X \to \mathbb{B}$, where $X$ is an arbitrary set and where $\mathbb{B}$ is a [[boolean domain]].

In contexts where the elements of $\mathbb{B}$ represent logical values, for example, $0 = \mathop{false}$ and $1 = \mathop{true}$, a boolean-valued function may be referred to as a _predicate_ or a _proposition_.  However, these terms may also be used to describe the syntactic entities that denote or express boolean-valued functions, or that have boolean-valued functions among their canonical or intended models.  When necessary to avoid confusion, terms like _predicate formula_ or _propositional expression_ may be used to distinguish signs from their objects.

Treatments of boolean-valued functions, predicates, and propositions are frequently conducted modulo a coordinate system of type $\mathbb{B}^k$, where $k$ is a nonnegative integer.

$$\array{
X
&& \overset{\ulap{f}}{\longrightarrow}
&& \mathbb{B}
\\
\multiscripts{_{(x_1, \dots, x_k)}^{\kappa \: =}}{}{}
& \searrow
&& \nearrow_{f_\kappa}
\\
&& \mathbb{B}^k
}$$

A $k$-dimensional boolean coordinate system for $X$ is a set of $k$ coordinate projections $x_j : X \to \mathbb{B}$ for $j = 1 \: to \: k$ that collectively define a map $\kappa = (x_1, \ldots, x_k) : X \to \mathbb{B}^k$.

## Remarks ##

Assuming the law of [[excluded middle]], the boolean-valued functions on $X$ correspond precisely to the [[subsets]] of $X$; even in [[constructive mathematics]], they corresond to the [[decidable subsets]] of $X$.  See also [[characteristic function]].
