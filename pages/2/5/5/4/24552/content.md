
#Contents#
* table of contents
{:toc}


## Idea 

A _fixed point operator_ in a [[cartesian monoidal category]], or more generally a [[cartesian multicategory]] is a structure on a category that models that every object of the category has the [[fixed point property]], i.e., every [[endomorphism]] in the category has a [[fixed point]].

In [[denotational semantics]] of [[programming languages]], these can be used to model [[recursive]] [[definitions]].

## Definition

There are several equivalent formulations in the literature, here we present the definition that is most useful (parameterized) and general (multicategorical): that of _parameterized_ fixed point operators in [[cartesian multicategories]].

A parameterized fixed point operator on a cartesian multicategory $M$ is a family of functions $fix \colon M(\Gamma,X;X) \to M(\Gamma;X)$ satisfying:

1. ([[natural transformation |Naturality]] in $\Gamma$) For any substitution $\gamma : M(\Delta,\Gamma)$, $fix(f) \circ \gamma = fix(f \circ \gamma)$
2. ([[dinatural transformation |Dinaturality]] in $X$) For any $f : M(\Gamma, X;Y)$ and $g : M(\Gamma,Y;X)$, $fix(f \circ g) = f \circ fix(g \circ f)$
3. (Diagonal property) For any $f : M(\Gamma, X, X; X)$, $fix(fix(f)) = fix(f \circ (\gamma, x,x))$ where here the substitution $(\gamma, x,x) : M(\Gamma,X;\Gamma,X,X)$ duplicates the input.

Note that picking $g$ to be the [[identity]] in (2) implies the fixed point property: for any $f \in M(\Gamma,X;X)$, $f \circ fix(f) = fix(f)$.

## Related Concepts

A parameterized fixed-point operator is equivalent to a [[traced monoidal category|trace]] structure on a [[cartesian monoidal category]].

For a [[Lawvere theory]], a fixed-point operator is the same thing as the structure of an [[Conway theory]]. 

## References

* [[Masahito Hasegawa]], _Recursion from Cyclic Sharing: Traced Monoidal Categories and Models of Cyclic Lambda Calculi_, TLCA 1997 [doi](https://doi.org/10.1007/3-540-62688-3_37)

* [[Alex Simpson]] and [[Gordon Plotkin]], _Complete Axioms for Categorical Fixed-Point Operators_, LICS '00, [doi](https://doi.ieeecomputersociety.org/10.1109/LICS.2000.855753)

[[!redirects fixed point operators]]

[[!redirects fixed-point operator]]
[[!redirects fixed-point operators]]

