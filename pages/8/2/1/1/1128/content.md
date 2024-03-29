
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In a [[additive category]] [[category with translation|with translation]] $T : C \to C$ a **complex** is a [[differential object]]

$$
  d_X : X \to T X
$$

such that

$$
  X \stackrel{d_X}{\to} T X \stackrel{T d_X}{\to} T T X
$$

is the [[zero morphism]].

## Examples

* A complex in the category $Gr(C)$ of [[graded object]]s in an [[additive category]] $C$ is called a [[chain complex]].

* For $d_X : X \to T X$ a complex, the shifted [[differential object]] $ d_{T X} : T X \stackrel{-T(d_X)}{\to}  T T X$ is again a complex.

## Related concepts

* [[chain complex]]

## References

For instance section 11 of 

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_,


[[!redirects complexes]]
