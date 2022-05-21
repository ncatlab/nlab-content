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

## Idea

In [[dependent type theory]], given a [[type]] $A$, a [[type family]] $x:A \vdash B(x)$, [[terms]] $a_0:A$, $a_1:A$, and an [[identification]] $p:a_0 =_A a_1$, a **dependent identity type** or a **heterogeneous identity type** between two elements $b_0: B(a_0)$ and $b_1:B(a_1)$ is a type whose elements witness that $b_0$ and $b_1$ are "equal" over or modulo the identification $p$.  There are different ways to define this precisely, depending partly on the particular type theory used.

## Definition 

### In Martin-Löf type theory

One way to define the dependent identity type in Martin-Lof type theory is using [[transport]] along the identification $p$:

$$(a =_B^p b) \coloneqq (\mathrm{tr}_B^p(a) =_{B(b)} b)$$ 

There are also other possibilities...

### In cubical type theory

... to be written

### In higher observational type theory 

In [[higher observational type theory]], the dependent identity type is a primitive type former (although depending on the presentation, it can also be obtained using $ap$ into the universe).  In its general form, the type family can depend not just on a single type but on a [[type telescope]] $\Delta$.  The resulting dependent identity type then depends on an "identification in that telescope", which is defined by mutual recursion as a telescope of dependent identity types.  The [[type formation|formation rule]] is then

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\ \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\ \mathrm{type}}$$

... needs to be finished

## Categorical semantics

needs to be written

## See also

[[!include notions of type]]

## References

* [[Mike Shulman]], Towards a Third-Generation HOTT Part 2 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]