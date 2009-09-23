[[!redirects Boolean-valued function]]
[[!redirects Boolean-valued functions]]
[[!redirects boolean-valued functions]]
[[!redirects predicate]]
[[!redirects proposition]]

A __boolean-valued function__ is a function of type $f : X \to \mathbb{B}$, where $X$ is an arbitrary set and where $\mathbb{B}$ is a [[boolean domain]].

In contexts where the elements of $\mathbb{B}$ represent logical values, for example, $0 = \mathop{false}$ and $1 = \mathop{true}$, a boolean-valued function may be referred to as a _predicate_ or a _proposition_.  However, these terms may also be used to describe the syntactic entities that denote or express boolean-valued functions, or that have boolean-valued functions among their canonical or intended models.  When necessary to avoid confusion, terms like _predicate formula_ or _propositional expression_ may be used to distinguish signs from their objects.

Treatments of boolean-valued functions, predicates, and propositions are frequently conducted relative to a $k$-dimensional boolean coordinate system, where $k$ is a nonnegative integer.  This means that the consideration of arbitrary maps of type $X \to \mathbb{B}$ can be approached only through their approximations by _coordinate compatible maps_ or _representable predicates_, that is, maps of the form $f = \kappa \:\text{&#9005;}\: f_\kappa$, where $\kappa (x)$ is the coordinate $k$-tuple of $x$ in a given coordinate system and $f_\kappa$ is a [[boolean function]] of arity $k$.

$$\array{
\rowopts{\colalign{right center}}
X
&& \overset{f \:=\: \kappa \:\text{&#9005;}\: f_\kappa}{\longrightarrow}
&& \mathbb{B}
\\
\rowopts{\colalign{right center}}
\multiscripts{}{}{_{(x_1, \dots, x_k)}^{\kappa \: =}}
& \searrow
&& \nearrow_{f_\kappa}
\\
&& \mathbb{B}^k
}$$

__Note on notation.__  The sign "$\text{&#9005;}$" is used here to indicate an order of relation composition, in particular, function composition, where $f \:\text{&#9005;}\: g$ means that a relation of the form $f \subseteq X \:\times\: Y$ is composed with a relation of the form $g \subseteq Y \:\times\: Z$.

A $k$-dimensional boolean coordinate system for $X$ is a set of $k$ coordinate projections $x_j : X \to \mathbb{B}$ for $j = 1 \: to \: k$ that collectively define a map $\kappa = (x_1, \ldots, x_k) : X \to \mathbb{B}^k$.

## Remarks ##

Assuming the law of [[excluded middle]], the boolean-valued functions on $X$ correspond precisely to the [[subsets]] of $X$; even in [[constructive mathematics]], they corresond to the [[decidable subsets]] of $X$.  See also [[characteristic function]].
