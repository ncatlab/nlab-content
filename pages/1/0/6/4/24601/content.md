+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundational axiom
+-- {: .hide}
[[!include foundational axiom - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Boundary separation is a modular reconstruction of the [[uniqueness of identity proofs]] in [[cubical type theory]]. It is a rule which implies UIP as a theorem. 

## Definition

Recall that in [[cubical type theory]], there is an interval primitive $I$ with endpoints $0:I$ and $1:I$, as well as face formulas $\phi:F$ with rules which make $\phi$ behave like a formula in first-order logic ranging over the interval $I$. 

Boundary separation is the following rule: 

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash r:I \quad \Gamma, \partial(r) \vdash a \equiv b:A}{\Gamma \vdash a \equiv b:A}$$

where $I$ is the interval primitive in [[cubical type theory]] and $\partial(r)$ is the boundary face formula for dimension variables:

$$\delta(r) \coloneqq r = 0 \vee r = 1$$

(The interval primitive $I$ has more points than $0$ and $1$, so it is not the case that the sequent $r:I \vdash r = 0 \vee r = 1 \;\mathrm{true}$ holds.)

There is also a typal version of boundary separation which refers to [[cubical path types]] rather than definitional equality, given by the following rule:

$$\frac{\Gamma \vdash A \;  \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash r:I \quad \Gamma, \partial(r) \vdash p:a =_A b}{\Gamma \vdash p:a =_A b}$$

## Proof of UIP from boundary separation

We denote path types by $a =_A b$ and dependent path types by $a =_{i.A} b$, and path application to be $p(i)$ for $p$ a path and $i$ an interval. 

As the first step, consider $p : a =_A a$, the goal is to prove $p =_{a=_A a} \mathrm{refl}_a$. Applying $r$ on both sides we get $p(r) =_{A} a$, and it follows from reflexivity and boundary separation because $\partial{r} \vdash p(r) \equiv a$.

Consider the following context: 

$$\Gamma \coloneqq (\Delta, A \; \mathrm{type}, a:A, b:A, p:a =_{A} b, q: a =_A b)$$

... 

## See also

* [[uniqueness of identity proofs]]

* [[axiom K (type theory)|axiom K]]

## References

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 