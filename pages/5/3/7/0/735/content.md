
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--



A binary [[relation]] from a [[set]] $X$ to a set $Y$ is called **entire** if every element of $X$ is related to at least one element of $Y$.  This includes most examples of what the pre-Bourbaki literature calls a (total) [[multi-valued function]] (although that term usually implied some continuity or analyticity properties as well).  An entire relation is sometimes called **total**, although that has another meaning in the theory of [[partial order]]s; see [[total relation]].

A [[function]] is precisely a relation that is both entire and [[functional relation|functional]].

Like any relation, an entire relation $r$ can be viewed as a [[span]]
$$ \array {
  &                  & \Gamma_r \\
  & \swarrow_{\pi_r} &          & \searrow^{\phi_r} \\
X &                  &          &                   & Y
} $$
Such a span is a relation iff the pairing map from the **graph** $\Gamma_r$ to $X \times Y$ is an [[injection]], and such a relation is entire iff the **projection** map $\pi_r$ is a [[surjection]].

The [[axiom of choice]] says precisely that every entire relation contains a [[function]].  Failing that, the [[COSHEP]] axiom may be interpreted to say that, given $X$, there is a single surjection $\pi_X: \Gamma_X \to X$ such that every entire relation from $X$ contains a relation given by a span whose left leg is $\pi_X$.  In any case, entire relations may be preferable to functions in some contexts where the axiom of choice fails.

When [[internalization|internalising]] entire relations to a [[site]], one may want to replace the projection map $\pi_r: \Gamma_r \to X$ by a [[cover|covering family]].

## Related concepts

* [[axiom of fullness]]


[[!redirects entire relation]]
[[!redirects entire relations]]
