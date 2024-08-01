
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An **isogeny** is a [[surjection]] of [[algebraic groups]] that has a [[finite set|finite]] [[kernel]]. For [[abelian varieties]], this is equivalently a [[rational map]] between groups of the same dimension that preserves the neutral element (which implies that it is a [[group homomorphism]]).


##Lang isogeny

Let $G$ be a commutative [[algebraic group]] over a [[finite field]] $\mathbf{F}_q$, and write $\mathrm{Fr}$ for its $q$-power [[Frobenius morphism|Frobenius]]. The **Lang isogeny** is the morphism

\[
\mathrm{Lang} : G \to G
\qquad
g \mapsto \mathrm{Fr}(g) \cdot g^{-1}.
\]

Observe that

\[
\mathrm{ker}(\mathrm{Lang}) = G(\mathbf{F}_q).
\]

One may view the Lang isogeny as defining a multiplicative $G(\mathbf{F}_q)$-[[local system]] over $G$. It follows that every [[character#MultiplicativeCharacterOfAGroup|character]]

\[
\chi : G(\mathbf{F}_p) \to \overline{\mathbf{Q}}_\ell^\times
\]

induces a character sheaf $\mathscr{F}_\chi$ on $G$, and one verifies that applying the [[fonctions-faisceaux dictionary]] to $\mathscr{F}_\chi$ recovers $\chi$.

## References

* This Stack Exchange discussion, _[What is isogeny?](https://math.stackexchange.com/questions/36724/what-is-isogeny)_

* Wikipedia, _[Isogeny](http://en.wikipedia.org/wiki/Isogeny)_

Examples of sporadic (exceptional) isogenies from [[spin groups]] onto [[orthogonal groups]] are discussed in

* {#Garrett13} [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_ (July 2013) &lbrack;[pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf), [[Garrett-SporadicIsogenies.pdf:file]] &rbrack;

[[!redirects isogenies]]
