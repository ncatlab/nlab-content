+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##
In [[homotopy type theory]], given a [[dagger category]] $A$ and objects $a,b:A$, then by induction on identity, there is a function

$$idtouiso : (a=b) \to (a \cong^\dagger b)$$

as we may assume $a$ and $b$ are the same, which means $1_a:hom_A(a,a)$, which is a unitary isomorphism.

$A$ is a **univalent dagger category** or a **saturated dagger category** if for all $a,b:A$, $idtouiso_{a,b}$ is an equivalence.

The inverse of $idtouiso$ is denoted $uisotoid$.

## Examples ##

* Every [[univalent groupoid]] is a univalent dagger category with $f^\dagger = f^{-1}$. 

* The dagger category $Rel$ of [[set]]s and relations is a univalent dagger category with $f^\dagger$ representing the opposite relation of a relation $f$. 

* The dagger category $Hilb\mathbb{R}$ of Hilbert spaces over the real numbers and linear maps is a univalent dagger category with $f^\dagger$ representing the adjoint linear map of $f$. 

## See also ##

* [[dagger category]]

* [[univalent setoid]]

* [[univalent groupoid]]

* [[poset]]

* [[univalent category]]

## References ##

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects univalent dagger categories]]
[[!redirects saturated dagger category]]
[[!redirects saturated dagger categories]]