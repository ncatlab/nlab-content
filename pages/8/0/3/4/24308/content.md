+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In [[type theory]], the *family of finite types* is the analog of the [[natural numbers]]-[[indexed set]] of [[finite sets]] in [[set theory]].

## Definition ##

In [[type theory]], given a [[natural number]] $n \colon\mathbb{N}$, the __family of finite types__ $\mathrm{Fin}_\mathcal{U}(n)$ of a [[type universe]] $\mathcal{U}$ 

* with [[empty type]] $\varnothing_\mathcal{U} \colon \mathcal{U}$, 

* unit type $\ast_\mathcal{U}:\mathcal{U}$, 

* and binary [[coproducts]] $(-) \sqcup_\mathcal{U}(-) \colon \mathcal{U} \times \mathcal{U} \to \mathcal{U}$ 

is an [[inductive family]], [[induction|inductively]] defined by:

$$
  \begin{array}{lcl}
  \mathrm{Fin}_\mathcal{U}(0) 
  &\coloneqq& 
  \underset
    {A \colon \mathcal{U}}
    {\sum} 
  \big(
    A 
    \cong_\mathcal{U}
    \varnothing_\mathcal{U}
  \big)
  \\
  \mathrm{Fin}_\mathcal{U}(s(n)) 
  &\coloneqq& 
  \underset
    {A:\mathcal{U}}
    {\sum}
  \bigg[
    \sum_{B:\mathrm{Fin}_\mathcal{U}(n)} 
    \Big(
      A \cong_\mathcal{U} 
      \big(
        B
        \sqcup_\mathcal{U} 
        \ast_\mathcal{U}
      \big)
    \Big)
  \bigg]
  \end{array}
$$

(where "$\sum$" denotes [[dependent sum]] and "$\cong$" denotes [[identity types]], as usual).

## See also ##

* [[natural numbers]]

* [[inductive family]]

* [[finite type]], [[finite set]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: *[[Symmetry]]* (2021) 

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*

