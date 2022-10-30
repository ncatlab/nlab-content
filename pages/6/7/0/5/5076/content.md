[[!redirects pro-object in an (∞,1)-category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For small (∞,1)-categories

For $C$ a [[small (∞,1)-category]] and $\kappa$ a [[regular cardinal]], the $(\infty,1)$-category of $\kappa-$**pro-objects** in $C$ is the [[opposite (∞,1)-category]] of [[ind-object in an (∞,1)-category|ind-objects]] in the opposite of $C$:

$$
  Pro_\kappa(C) := (Ind_\kappa(C^{op}))^{op}
  \,.
$$

For $\kappa = \omega$ we write just $Pro(C)$.

By the properties listed there, if $C$ has all $\kappa$-small [[(∞,1)-limit]]s then this is equivalent to

$$
  \cdots \simeq Lex_\kappa(C, \infty Grpd)^{op} \subset Func(C,\infty Grpd)^{op}
$$

the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that preserve these limits.


### For large (∞,1)-categories

Generalizing this definition, if $C$ is a non-small $(\infty,1)$-category with finite limits, we write

$$
  Pro(C) := AccLex(C,\infty Grpd)^{op}
  \,.
$$

for the category of left exact functors $C\to \infty Gprd$ which are moreover [[accessible (∞,1)-functor|accessible]].  In other words, when $C$ is large, $Pro(C)$ consists only of those left-exact functors which are "*small* cofiltered limits of representables".


## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* [[pro-object]] / **pro-object in an $(\infty,1)$-category**

## References

The large version is mentioned around def. 7.1.6.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
