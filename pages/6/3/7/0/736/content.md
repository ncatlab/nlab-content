
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A binary [[relation]] from a [[set]] $X$ to a set $Y$ is called **functional** if every element of $X$ is related to at most one element of $Y$.  Notice that this is the same thing as a [[partial function]], seen from a different point of view.  A (total) [[function]] is precisely a relation that is both functional and [[entire relation|entire]].

## Properties

Like any relation, a functional relation $r$ can be viewed as a [[span]]
$$ \array {
  &                    & \Delta_r \\
  & \swarrow_{\iota_r} &          & \searrow^{\phi_r} \\
X &                    &          &                   & Y
} $$
Such a span is a relation iff the pairing map from the **domain** $\Delta_r$ to $X \times Y$ is an [[injection]], and such a relation is functional iff the **inclusion** map $\iota_r$ is also an injection. Such a relation is entire iff the inclusion map $\iota_r$ is a [[surjection]]. 

(Total) functions are precisely left adjoints in the bicategory of relations, in other words relations $r: X \to Y$ in $Rel$ for which there exists $s: Y \to X$ satisfying 

$$r \circ s \leq 1_Y; \qquad 1_X \leq s \circ r.$$ 

For if a relation $r: X \to Y$ is a function, then 

1. $r r^{op} \leq 1_Y$: this just says that if $r^{op}(y, x)$ and $r(x, y')$, then $y = y'$. Equivalently, if $r(x, y)$ and $r(x, y')$ then $y = y'$: this holds precisely because $r$ is functional or well-defined. 

1. $1_X \leq r^{op} r$: this says that if $x = x'$, then there exists $y$ such that $r(x, y)$ and $r^{op}(y, x')$, i.e., there exists $y$ such that $r(x, y)$ and $r(x', y)$. This holds precisely because a function is an entire relation. 

On the other hand, suppose $r: X \to Y$ is a left adjoint. (...) 


in which case it may be proven that $s = r^{op}$. A relation is functional if and only if $r \circ r^{op} \leq 1_Y$, and is entire if and only if $1_X \leq r^{op} \circ r$. 

Further to this: surjectivity of a function $r: X \to Y$ can be expressed as the condition $1_Y \leq r \circ r^{op}$, and injectivity as $r^{op} \circ r \leq 1_X$. 


[[!redirects functional relations]]
