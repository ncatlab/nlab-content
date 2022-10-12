+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In a [[dependent type theory]] with [[identity types]], a term $a:A$ is a **center of contraction** or a **centre of contraction** if in the context of a variable $b:A$ there is an [[identification]] $p(b):a =_A b$. If the type theory also has [[dependent product types]], the above is equivalent to having a dependent function
$$p:\prod_{b:A} a =_A b$$
called a **contraction** of $A$ at $a$. Thus, contractons of $A$ at $a$ are witnesses that $a:A$ is a center of contraction. 

We then define the type of contractions of $A$ at $a$ as
$$\mathrm{Contr}_A(a) \coloneqq \prod_{b:A} a =_A b$$ 

A type $A$ is a [[contractible type]] if there exists a center of contraction
$$\sum_{a:A} \mathrm{Contr}_A(a)$$
and a type $A$ is an [[h-proposition]] if every element in $A$ is a center of contraction 
$$\prod_{a:A} \mathrm{Contr}_A(a)$$

## See also

* [[contractible type]]
* [[h-proposition]]

## References

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

[[!redirects center of contraction]]
[[!redirects centers of contraction]]

[[!redirects centre of contraction]]
[[!redirects centres of contraction]]