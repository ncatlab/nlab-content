

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

_Cartesian logic_ or _finite limit logic_ is the [[internal logic]] of [[finitely complete categories]] (which the [[Elephant]] calls [[cartesian categories]]).

An important property is that every cartesian theory has an initial model. It follows that model reduct functors between cartesian theories have left adjoints: broadly, the free algebra constructions supplied by universal algebra for algebraic theories are also available for cartesian theories.

## Definition

Various definitions and names for the logic can be found in the references.
The [[Elephant]] definition amounts to saying that a cartesian theory is a [[first-order theory]] in which the only connectives used are $=$, $\top$, $\wedge$ and existential quantifiers over provably [[subterminal]] formulae, that is, $\exists x:A. \phi$ can only be used if
$$\phi(x),\phi(y) \vdash x = y$$
is provable. Unlike other first-order theories, this side-condition makes the order of presentation of axioms matter, as an axiom might require another in order to prove that a formula involved is subterminal. 

[Palmgren and Vickers](#PalmgrenVickers07) showed that in a geometric logic of partial terms (with a non-reflexive equality), the cartesian theories are precisely those that can be presented using only $\wedge$, $\top$ and $=$.

## Semantics in Categories with Finite Limits

Cartesian logic can be given models interpreting formulae as [[subobjects]] in a category with [[finite limits]]. See [[internal logic]] for more details. The most interesting component of this is the existential quantifiers. As with [[regular logic]], the existential quantifier is interpreted as an [[image factorization]], but the subterminality side condition ensures the image exists even in an arbitrary category with finite limits. A formula $\phi(x)$ with $x:A$ in a context $\Gamma$ is interpreted as a subobject $\phi \to \Gamma \times A$, and the subterminality side condition is satisfied in the internal logic if and only if the first projection $\Gamma \times A \to \Gamma$ is mono, in which case the composition $\phi \to \Gamma \times A \to \Gamma$ is already the inclusion into its image.

## Related concepts

[[!include categories and logic - table]]

## References

Cartesian logic was introduced in the early seventies by [[John Isbell]], [[Peter Freyd]] and [[Michel Coste]] (cf. [Johnstone 1979](#Johnstone79)). A standard source is Johnstone ([2002](#Johnstone02)).
[Palmgren and Vickers](#PalmgrenVickers07) gave a new proof of the initial model theorem, valid in weak foundational settings.

* {#AdamekRosicky94}[[Jiří Adámek]], [[Jiří Rosický]], _Locally presentable and accessible categories_ ,  Cambridge UP 1994. 

* {#Freyd02}[[Peter Freyd]], _Cartesian Logic_ , Theor. Comp. Sci. **278** (2002) pp.3-21.

* {#Johnstone79}[[Peter Johnstone]], _A Syntactic Approach to Diers' Localizable Categories_ , pp.466-478 in Springer LNM **753** Heidelberg 1979.

* {#Johnstone02}[[Peter Johnstone]], _Sketches of an [[Elephant]] II_ , Oxford UP 2002. (Around D1.3.4 p.833)

* {#PalmgrenVickers07}[[Erik Palmgren]], [[Steve Vickers]], _Partial Horn logic and cartesian categories_, Ann Pure Appl Logic **145 (3)** (2007) pp.314-353.


[[!redirects finite-limit logic]]