
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

1. $1_X \leq r^{op} r$: this says that if $x = x'$ in $X$, then there exists $y$ in $Y$ such that $r(x, y)$ and $r^{op}(y, x')$, i.e., there exists $y$ such that $r(x, y)$ and $r(x', y)$. This holds precisely because a function is an entire relation. 

On the other hand, suppose $r: X \to Y$ is a left adjoint. 

1. From $1_X \leq s r$ we deduce that if $x = x'$ in $X$, then there exists $y$ in $Y$ such that $r(x, y)$ and $s(y, x')$; in particular $r$ is entire. 

1. Suppose $r(x, y)$. From $x = x$ there exists $y'$ such that $r(x, y')$ and $s(y', x)$. Thus $s(y', x)$ and $r(x, y)$; from $s r \leq 1_Y$ we infer $y' = y$. We conclude at most one $y$ satisfies $r(x, y)$, making $r$ functional. 

Since $r$ is a function, it has a right adjoint $r$, and by uniqueness of right adjoints, we may conclude $s = r^{op}$. The [[monad]] $t = r^{op} r$ has a unit $1_X \leq t$ ($t$ is reflexive) and a multiplication $t t \leq t$ ($t$ is transitive), and also $t^{op} = (r^{op} r)^{op} = r^{op} r^{op\; op} = r^{op} r = t$ ($t$ is symmetric). So the monad $t$ is an [[equivalence relation]]. The above reasoning may be internalized to apply to the [[bicategory of relations]] internal to a [[regular category]], in which case this equivalence relation is exactly the [[kernel pair]] of the map $r$. The [[comonad]] $c = r r^{op}$ has a counit $c \leq 1_Y$ ($c$ is coreflexive), and such coreflective relations in $Set$ correspond to subsets of $Y$. More generally, in a regular category, the subobject of $Y$ named by $c$ is the [[image]] of $r$ (the [[coequalizer]] of the kernel pair). 

Further remarks: surjectivity of a function $r: X \to Y$ can be expressed as the condition $1_Y \leq r \circ r^{op}$, and injectivity as $r^{op} \circ r \leq 1_X$. 

## Related pages

* [[anafunction]]

## References 

* [[Peter Freyd]] and Andr&#233; Scedrov, *[[Categories, Allegories]]*, Mathematical Library Vol. 39, North-Holland (1990). 

* [[Robin Houston]], *Fun with Rel*, blog post at Bosker Blog (June 14, 2006). ([link](https://bosker.wordpress.com/2006/06/14/fun-with-rel/)) 


[[!redirects functional relations]]
