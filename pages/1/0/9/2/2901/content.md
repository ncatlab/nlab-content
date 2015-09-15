
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Euclidean geometry_ studies the [[geometry]] of [[Euclidean space]]s.  These spaces come equipped with a canonical [[Riemannian metric]], and Euclidean geometry can be regarded as the _local model_ for [[Riemannian geometry]], in some sense.


## Properties

* [[Pythagorean theorem]]

* [[pentagon decagon hexagon identity]]

* [[conic section]]

* [[Hadwiger's theorem]]

* [[Non-Euclidean geometry]]


## Axiomatizations 
 {#Axiomatizations}

Euclidean geometry in the sense of the Idea section makes reference to the extrinsic notion of [[real number]] (to delineate the notion of Euclidean space) and whatever surrounding structure is used to found that notion, but it has also received more intrinsic [[axiom|axiomatic]] treatments in the spirit of [[synthetic geometry]]. Notable among these are [[Hilbert|Hilbert's]] axioms, as set out in his *Grundlagen der Geometrie*, and [[Alfred Tarski|Tarski]]'s axioms, which form a first-order axiomatic theory. 

### Hilbert's axioms 

Here we will just give an extremely sketchy description (for now, see [Wikipedia](http://en.wikipedia.org/wiki/Hilbert%27s_axioms) for a fuller account). It should be said right away that two of the Hilbert axioms are *not* first-order. 

Hilbert's [[theory]] has 

* Three sorts: points, line, planes (or if you like: tables, chairs, and beer mugs[^1]); 

[^1]: After a famous saying attributed to Hilbert which in some sense heralds the axiomatic spirit: '_Man mu&#223; jederzeit an Stelle von "Punkte, Geraden, Ebenen" "Tische, St&#252;hle, Bierseidel" sagen k&#246;nnen_'. The 1891 anecdote is reported by O. Blumenthal in Hilbert, _Gesammelte Abhandlungen III. Band_ , Springer Berlin 1935, p.403. The three classes became '_Liebe, Gesetz, Schornsteinfeger_' (love, law, chimney-sweep) in Hilbert's letter to [[Gottlob Frege|Frege]] (Dec. 29th 1899). The question raised in Frege's rejoinder (Jan. 6th 1900) whether his pocket watch is a point is still an open problem.

* Six relations: betweenness (a ternary relation on points), three incidence relations (one for points and lines, one for points and planes, one for lines and planes), and two congruence relations (a relation $L(a, b, c, d)$ on points whose intuitive meaning is that the the line segment $a b$ is congruent to the line segment $c d$, and a relation $A(a, b, c, d, e, f)$ on points whose intuitive meaning is that the angle $a b c$ is congruent to the angle $d e f$); 

* A bunch of [[axioms]] (20 or 21 depending on which specific edition or translation or exposition one is working with; Wikipedia says 20 but actually has, confusingly, 21 -- see the Talk page for more information). They are organized as 
  * Axioms of incidence (8), 
  * Axioms of betweenness (4),
  * Axioms of congruence (6), 
  * Axiom of parallels (the parallel postulate) (1), 
  * Axioms of completeness (2), mirroring the archimedean property and the completeness properties of the real numbers. These are not first-order. 

I ([[Todd Trimble]]) assume Hilbert's theory is, or is at least intended to be, [[categoricity|categorical]] in the model-theoretic sense, at least considered against a fixed set-theoretic background. In other words I assume the real numbers as complete ordered field would be a definable structure and the axioms are uniquely modeled by $\mathbb{R}^3$ with its Euclidean structure. 

### Tarski's axioms 
 {#TarskiAxioms}

Tarski's [[theory]] EPG (Elementary Plane [Euclidean] Geometry) is a one-sorted theory in first-order logic with equality, with variables representing points. There are no constants or operations in the signature, and just two relations: 

* A ternary relation $B$ (betweenness), with $B(x, y, z)$ meaning $y$ is between $x$ and $z$ ($y$ is on the line segment between $x$ and $z$) -- we will write instead $B x y z$ to conserve space; 

* A 4-ary relation $C$ (congruence), with $C(x, y, z, w)$ meaning that a line segment $x y$ is congruent (of the same length) as $z w$. For readability, we write this as $x y \equiv z w$. 

The theory can be presented (in some sense very parsimoniously) by 10 axioms and one first-order axiom scheme. Axioms 8 and 9 constrain the dimension to $n = 2$ (Euclidean plane geometry), but there are analogues of 8 and 9 that constrain the dimension to any chosen number. Axiom 10 is an extremely disguised version of the [[parallel postulate|Parallel Postulate]], with a complicated history behind it. The axiom scheme 11 plays the role of a Dedekind cut axiom expressed in first-order terms. 

1. $\vdash \; a b \equiv b a$, 

1. $a b \equiv p q, a b \equiv r s \;\; \vdash \;\; p q \equiv r s$, 

1. $a b \equiv c c \vdash a = b$, 

1. $\vdash \; (\exists x)\; B q a x \wedge a x \equiv b c$ (segment construction: given a line segment $b c$ and a line from $q$ to $a$, one can extend that line in that direction by a segment $a x$ congruent to $b c$), 

1. $a \neq b, B a b c, B a' b' c', a b \equiv a' b', b c \equiv b' c', a d \equiv a' d', b d \equiv b' d' \;\; \vdash \;\; c d \equiv c' d'$ (5 segment axiom), 

1. $B a b a \; \vdash \; a = b$, 

1. $B a p c, B b q c \;\; \vdash \;\; (\exists x)\; B p x b \wedge B q x a$ (Pasch axiom: roughly, if a line goes through one side of a triangle and not through a vertex, then it must go through another side), 

1. $\vdash \; (\exists a, b, c)\; \neg (B a b c \vee B b c a \vee B c a b)$ (there exist three non-collinear points: the dimension is at least 2), 

1. $p \neq q, a p \equiv a q, b p \equiv b q, c p \equiv c q \;\; \vdash \;\; B a b c \vee B b c a \vee B c a b$ (if three points are each equidistant from two given distinct points $p$ and $q$, then those three points are collinear: the dimension is at most 2), 

1. $B a d t, B b d c, a \neq d \;\; \vdash \;\; (\exists x, y)\; B a b x \wedge B a c y \wedge B y t x$ (Parallel Postulate (!)), 

1. (Cut schema) Let $\phi(x)$ be a formula in which variables $a, b, y$ do not occur freely, and let $\psi(y)$ be a formula in which $a, b, x$ do not occur freely. Then 
$$(\forall x, y)\; (\phi(x) \wedge \psi(y) \Rightarrow B a x y) \;\; \vdash \;\; (\exists b)(\forall x, y)\; (\phi(x) \wedge \psi(y) \Rightarrow B x b y)$$ 
(if every element $y$ in the set defined by $\psi$ lies beyond every element $x$ in the set defined by $\phi$ as seen from the perspective of $a$, then there is some $b$ between every such $x$ and every such $y$). 

See [Tarski-Givant](#TG) for a thorough discussion of this and related axiom systems, and an extensive bibliography. 

One important aspect of the meta-theory lies in the relation of models of this theory to [[real closed fields]]. If $R$ is a real closed field, then there is a corresponding model of EPG whose underlying set is $R \times R$ and where the relations $B$ and $C$ are interpreted by expected conditions: 

$$C(x, y, z, w) \;\;\; iff \;\;\; (x_1 - y_1)^2 + (x_2 - y_2)^2 = (z_1 - w_1)^2 + (z_2 - w_2)^2$$ 

$$\,$$ 

$$B(x, y, z) \;\;\; iff \;\;\; (x_1 - y_1)(y_2 - z_2) = (x_2 - y_2)(y_1 - z_1) \; \wedge \; 0 \leq (x_1 - y_1)(y_1 - z_1) \; \wedge \; 0 \leq (x_2 - y_2)(y_2 - z_2).$$ 

It is mostly straightforward to verify that this structure on $R \times R$ satisfies the EPG axioms (all but the cut schema hold for any ordered field). More importantly, 

+-- {: .num_theorem} 
###### Theorem 
For every model $M$ of EPG there is a real closed field $R$ such that $M \cong R \times R$ as models. 
=-- 

Of course there is some arbitrariness involved in the choice of isomorphism; for example, any line segment $x y$ can be used to stipulate a unit length and a coordinate axis. The proof is lightly sketched in [Tarski](#Tar); again only the first ten axioms are needed to produce an ordered field structure on $R$, with the cut schema being used to verify the real closure. 

The significance of this result is that EPG is a complete and decidable theory, just as the theory of real closed fields is complete and decidable. Hence there exists an algorithm which, on being fed a sentence in the language of Elementary Plane Geometry, will produce a proof of the sentence or a proof of its negation in the theory. 

## Related concepts

| [[synthetic geometry]]  |
|-------------------------|
| [[Euclidean geometry]]  |
| [[hyperbolic geometry]] |
| [[elliptic geometry]]   |

* [[parallel postulate]]

* [[trigonometry]]

* [[Riemannian geometry]]

[[!include local and global geometry - table]]

## References

* [[Euclid]], _[[Elements]]_ 

* {#Tarski} [[Alfred Tarski]], _What is elementary geometry?_, in _The axiomatic method. With special reference to geometry and physics_ Proceedings of an International Symposium held at the Univ. of Calif., Berkeley, Dec. 26, 1957-Jan. 4, 1958 (ed. L. Henkin, P. Suppes, and A. Tarski), Studies in Logic and the Foundations of Mathematics, Amsterdam: North-Holland (1959), pp. 16&#8211;29. ([pdf](http://www.geographicknowledge.de/SeminarLFG/Tarski_Whatiselementarygeometry.pdf))  

* {#TG}  [[Alfred Tarski]] and Steven Givant, _Tarski's system of geometry_, Bull. Symb. Logic, Vol. 5 No. 2 (1999), 175&#8211;214. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.27.9012)) 
 
A textbook account of the axiomatization of Euclidean geometry is

* [[Wolfram Schwabhäuser]], [[Wanda Szmielew]], [[Alfred Tarski]], _Mathematische Methoden in der Geometrie_, Springer 1983

Full formalization of this book in [[Coq]] (as [[synthetic geometry]] but following Tarski's work) is discussed at 

* [[Gabriel Braun]], [[Pierre Boutry]], [[Julien Narboux]], _[GeoCoq](http://geocoq.github.io/GeoCoq/)_, _[La g&#233;om&#233;trie de Tarski en Coq](http://gabrielbraun.free.fr/Geometry/Tarski/)_

A formalisation of Euclid using diagrammatic reasoning is in

* J. Avigad, E. Dean, J. Mumma, _A formal system for Euclid's Elements_ , [arXiv:0810.4315](http://arxiv.org/abs/0810.4315v3) (2009).
 
[[!redirects Euclidean geometry]]
[[!redirects Euclidean geometries]]