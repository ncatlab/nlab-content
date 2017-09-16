Given a [[natural number]] $n$, the __successor__ $n+$ of $n$ is simply $n + 1$.

More generally, in any [[well-order]]ed set $S$, the successor $w+$ or $w + 1$ (if it exists) of an element $w$ is the smallest element of the subset of all elements which are (strictly) greater than $w$.  If $S$ has no maximal element, then the successor map $w \mapsto w + 1$ is always defined; it is sometimes used to make recursive definitions.

This notion is sometimes also used for some well-ordered proper classes, for example for the class $\mathbf{Ord}$ of [[ordinal number]]s. For definitions by [[transfinite recursion]], one usually specifies the value at $0$, the rule for recursion along the successor map and a separate rule of recursion for 
the limiting ordinals (infinite ordinals which are not successors). (For example, the [[von Neumann hierarchy]] of well-founded [[pure set]]s is defined in that way.)  One can (and in [[constructive mathematics]] must) also handle all three cases at once, and the successor function is used there as well.

In a topos, a [[natural numbers object]] $\mathbb{N}$ is equipped with a successor morphism $\mathbb{N}\to\mathbb{N}$;
and it has an abstract property of [[recursion]].