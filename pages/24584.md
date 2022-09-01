+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

In [[cubical type theory]], there is an interval primitive $I$ with endpoints $0:I$ and $1:I$, as well as face formulas $\phi:F$ with rules which make $\phi$ behave like a formula in first-order logic ranging over the interval $I$. 

The interval primitive $I$ has more points than $0$ and $1$, so it is not the case that the sequent 
$$r:I \vdash r = 0 \vee r = 1 \;\mathrm{true}$$ 
holds. 
The **boundary** is thus defined as the formula
$$\delta(r) \coloneqq r = 0 \vee r = 1$$
The boundary is important for expressing the rules of path types and compositions in [[cubical type theory]]. 

## See also

* [[cubical type theory]]

* [[boundary separation]]

## References

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 