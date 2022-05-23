
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

In [[categories]] like [[sSet]], the [[internal hom]] $[X,Y]$ between two [[objects]] is often called the _function complex_ ("[[simplicial complex]] of [[functions]] from $X$ to $Y$).

## Definition

Suppose $C$ is a [[category]] that admits small [[coproducts]].

Given [[simplicial objects]] $A,B\in C^{\Delta^{op}}$,
their __function complex__ is a [[simplicial set]]
$$Hom(A,B)$$
whose set of $n$-simplices
is the set of maps
$$\Delta^n\otimes A\to B,$$
where $\otimes$ denotes the [[copowering]] of [[simplicial objects]] over [[simplicial sets]] given by
$$(C\otimes D)_n=\coprod_{i\in C_n}D_n.$$

## Related concepts

* [[internal hom]]

* [[simplicial object]]

* [[simplicial set]]

## References

The original definition of a function complex in the generality stated above is due to [[Daniel M. Kan]]:

* [[Daniel M. Kan]], _On c.s.s. categories_, Boletín de la Sociedad Matemática Mexicana 2 (1957), 82–94.  [PDF](https://dmitripavlov.org/scans/kan-on-css-categories.pdf).

[[!redirects function complexes]]

