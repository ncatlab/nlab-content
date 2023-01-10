
\tableofcontents


## Overview

The **principle of finite choice** states that the [[dependent product]] of a [[finite set|finite]] [[indexed set|family]] of [[inhabited sets]] is itself inhabited. 

Finite choice is provable in most set theories, including [[strongly predicative]] and [[constructive mathematics|constructive]] set theories, as well as set theories without [[quotient sets]]. 

In [[dependent type theory]], finite choice is definable and provable, provided one has [[identity types]], [[dependent sum types]], [[bracket types]], [[finite sets]], and [[dependent tuple types]] in the type theory:

$$\frac{\Gamma \vdash n:\mathbb{N} \quad \Gamma, i:\mathrm{Fin}(n) \vdash A(i) \; \mathrm{type}}{\Gamma, a:(i:\mathrm{Fin}(n)) \to \left[A(i)\right] \vdash \mathrm{finitechoice}(a):\left[(i:\mathrm{Fin}(n)) \to A(i)\right]}$$

One could express the principle of finite choice as two separate cases representing the case with zero and two inhabited sets:

* Every [[singleton]] is an [[inhabited set]]

* The [[product]] of two [[inhabited sets]] is inhabited. 

In [[dependent type theory]], the former follows from the definition of a singleton or [[contractible type]] as an inhabited [[mere proposition]], and the latter is given by the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, a:[A], b:[B] \vdash \mathrm{binarychoice}(a, b):\left[A \times B\right]}$$

## See also

* [[countable choice]]
* [[axiom of choice]]

## References

* *Which axioms of ZF are used for finite choice?*, MathOverflow, ([web](https://mathoverflow.net/questions/179361/which-axioms-of-zf-are-used-for-finite-choice))

* *Finite choice without AC*, Mathematics Stackexchange, ([web](https://math.stackexchange.com/questions/64237/finite-choice-without-ac))

* *Finite axiom of choice: how do you prove it from just ZF?*, MathOverflow, ([web](https://mathoverflow.net/questions/32538/finite-axiom-of-choice-how-do-you-prove-it-from-just-zf))

[[!redirects finite choice]]
[[!redirects axiom of finite choice]]
[[!redirects principle of finite choice]]