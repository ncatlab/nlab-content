
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Conntents#
* table of contents
{:toc}

## Definition

An **exact sequence** is a [[chain complex]] with vanishing [[chain homology]].

## Long and short exact sequences

A general exact sequence is sometimes called a **long exact sequence**, to distinguish from the special case of a **short exact sequence** which is an exact sequence of the form
$$ 0 \to A \to B \to C \to 0 .$$
Of course, by adding $0$ to either end (or both!), one turns a short exact sequence into a chain complex and in particular into a long exact sequence.

A short exact sequence may also be defined in more elementary terms as a sequence
$$ A \stackrel{i}\to B \stackrel{p}\to C $$
such that $i$ is a [[monomorphism]], $p$ is an [[epimorphism]], and the [[image]] of $i$ equals the [[kernel]] of $p$ (equivalently, the [[coimage]] of $p$ equals the [[cokernel]] of $i$).

A **split exact sequence** is a short exact sequence in which $i$ is a [[split monomorphism]], or (equivalently) in which $p$ is a [[split epimorphism]].  In this case, $B$ may be decomposed as the [[biproduct]] $A \oplus C$ (with $i$ and $p$ the usual biproduct inclusion and projection); this sense in which $B$ is 'split' into $A$ and $C$ is the origin of the general terms 'split (mono/epi)morphism'.

The above works in any [[abelian category]], and possible more generally.  See also [[exact sequence of Hopf algebras]].


[[!redirects long exact sequence]]
[[!redirects short exact sequence]]
[[!redirects split exact sequence]]