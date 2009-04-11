# Idea

The **von Neumann hierarchy** is a way of "building up" all [[pure set]]s recursively, starting with the [[empty set]], and indexed by the [[ordinal number]]s.

# Definition

Using [[transfinite recursion]], define a hierarchy of well-founded sets $V_\alpha$, where $\alpha\in\mathbf{Ord}$ is an [[ordinal number]], as follows:

* $V_0 = \emptyset$
* $V_{\alpha+1} = P(V_\alpha)$ (the [[power set]] of $V_\alpha$)
* $V_\alpha = \cup_{\beta\lt\alpha} V_\beta$ if $\alpha$ is a limit ordinal.

The formula for $0$ is actually a special case of the formula for a limit ordinal.  Alternatively, you can do them all at once:

* $V_\alpha = \cup_{\beta \lt \alpha} P(V_\beta)$

The [[axiom of foundation]] in [[ZFC]] is equivalent to the statement that every set is an element of $V_\alpha$ for some ordinal $\alpha$.  The **rank** of a set $x$ is defined to be the least $\alpha$ for which $x\in V_\alpha$ (this is well-defined since the ordinals are [[well-order|well-ordered]]).
