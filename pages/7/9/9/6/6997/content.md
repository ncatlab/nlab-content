
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Antisubalgebras
* table of contents
{: toc}


## Idea

In [[constructive mathematics]], we often do [[algebra]] by equipping an [[gebra|algebra]] with a [[tight apartness]] (and requiring the algebraic operations to be [[strongly extensional function|strongly extensional]]), in the sense of [[ring with tight apartness]]. In this context, it is convenient to replace [[subalgebras]] with _anti_-subalgebras, which [[classical mathematics|classically]] are simply the [[complements]] of subalgebras.


## Definitions

Let us work in the context of [[universal algebra]], so an __algebra__ is a [[set]] $X$ equipped with a family of [[functions]] $f_i\colon X^{n_i} \to X$ (where each [[arity]] $n_i$ is a [[cardinal number]]) that satisfy certain equational identities (which are irrelevant here).  As usual, a __subalgebra__ of $X$ is a [[subset]] $S$ such that $f_i(p_1,\ldots,p_{n_i}) \in S$ whenever each $p_k \in S$.  There is no need, in general, to require that any arity $n_i$ be finite or that there be finitely many $f_i$; however, for a few results, we will need a special case of these that we will call having __well-behaved constants__:

* each arity is either $0$ or at least $1$ (so each operation either is a constant or has at least one operand), and
* the number of constants is [[Kuratowski-finite]] (so there is an exhaustive list $c_1, c_2, c_3, \ldots c_n$ of constants for some [[natural number]] $n$, where it remains possible that $c_i = c_j$ might be an equational law).

The first item is true of all derived operations in the theory as long as it is true of the fundamental operations in the signature; but in this last item, we\'re counting all derived constants, not just the fundamental ones.  For example, the theory of (unital) [[rings]] does *not* have well-behaved constants, because there are infinitely many constants (one for each [[integer]]).

Now we require $S$ to have a [[tight apartness]] $\ne$, which induces a tight apartness on each $X^{n_i}$ (via [[existential quantification]]), and we require the operations $f_i$ to be [[strongly extensional function|strongly extensional]].  An algebra $X$ with these properties is called an **inequality algebra**.  (For much of the theory we don't need the apartness to be tight, but for some purposes it is necessary.)

A [[subset]] $A$ of $X$ is __[[open subset|open]]__ (or $\ne$-open) if, whenever $p \in A$, $q \in A$ or $p \ne q$.  An __antisubalgebra__ of $X$ is an open subset $A$ such that $p_j \in A$ for some $j$ whenever $f_i(p_1,\ldots,p_{n_i}) \in A$ for any $i$.  By taking the [[contrapositive]], we see that the [[complement]] of $A$ is a subalgebra $S$, but we cannot (in general) start with a subalgebra $S$ and get an antisubalgebra $A$.  (Impredicatively, we can take the antisubalgebra generated, as described below, by the $\ne$-complement of $S$, that is the set of those elements of $X$ that $\ne$ every element of $S$, but its complement will generally only be a superset of $S$.)


## Examples
 {#Examples}

Unless otherwise noted, all of the constructions in these examples should be [[predicative mathematics|predicative]].

\begin{example}
The [[empty subset]] of any algebra is an antisubalgebra, the __empty antisubalgebra__ or __improper antisubalgebra__, whose complement is the [[improper subset|improper]] subalgebra (which is all of $X$).  An antisubalgebra is __[[proper subset|proper]]__ if it is [[inhabited subset|inhabited]]; the ability to have a positive definition of when an antisubalgebra is proper is a significant motivation for the concept.
\end{example}

\begin{example}
If $A$ is an antisubalgebra and $c$ is a constant (given by an operation $X^0 \to X$ or a composite of same with other operations), then $p \ne c$ whenever $p \in A$.  If the theory has well-behaved constants, then we can define the __trivial antisubalgebra__ to be the subset of those elements $p$ such that $p \ne c$ for each constant $c$ (the $\ne$-complement of the [[trivial subalgebra]]).  In general, we may also take the __trivial antisubalgebra__ to be the [[union]] of all antisubalgebras (but this is not predicative).
\end{example}



The anti-analog of [[subgroups]], are anti-subgroups. Their  definition can be simplified a bit:
\begin{example}
A subset $A$ of an inequality group $X$ is an __antisubgroup__ if $p \ne 1 $ whenever $p \in A$, $p \in A$ or $q \in A$ whenever $p q \in A$, and $p \in A$ whenever $p^{-1} \in A$.  We need not assume that $A$ is open; this can be proved from strong extensionality of the group operations on $X$ and the stronger form of the nullary anticlosure condition ("$p \ne 1 $ whenever $p \in A$" is a strengthening of the condition $\neg (1\in A)$ that would be the literal nullary case of the general definition.)  An antisubgroup $A$ is __[[normal subgroup|normal]]__ if $p q \in A$ whenever $q p \in A$.  The __[[trivial subgroup|trivial]] antisubgroup__ is the $\ne$-complement of $\{1\}$.
\end{example}

The anti-analog of [[ideals]] (of [[rings]]) are [[antiideals]]. (Technically, these are antisubalgebras of the ring as a module over itself.)  Again we can omit $\ne$-openness by strengthening the nullary condition:

\begin{example}\label{AntiIdeals}
A subset $A$ of $X$ is a __two-sided antiideal__ (or simply an __[[antiideal]]__ in the commutative case) if $p \ne 0 $ whenever $p \in A$, $p \in A$ or $q \in A$ whenever $p + q \in A$, and $p \in A$ and $q \in A$ whenever $p q \in A$.  $A$ is a __left antiideal__ if instead the last condition requires only that $p \in A$, and $A$ is a __right antiideal__ if instead the last condition requires only that $q \in A$.  It follows that an antiideal $A$ is proper iff $1 \in A$.  $A$ is __[[prime ideal|prime]]__ (or _antiprime_) if it is proper and $p r q \in A$ for some $r$ whenever $p \in A$ and $q \in A$; in the commutative case, we can say that $p q \in A$ whenever $p \in A$ and $q \in a$.  $A$ is __[[maximal ideal|minimal]]__ (or _antimaximal_) if it is proper and, for each $p \in A$, for some $q$, for each $r \in A$, $p q + r \ne 1$ and $q p + r \ne 1$ (which is constructively stronger than being prime and [[minimal element|minimal]] among proper ideals); of course, we only need one of these two inequalities in the commutative case.  The __[[trivial ideal|trivial]] antiideal__ is the $\ne$-complement of $\{0\}$.
\end{example}

\begin{example}
Note that a [[union]] of antisubalgebras is again an antisubalgebra.  

Given any subset $B$ of $X$, the antisubalgebra __generated__ by $B$ is the union of all antisubalgebras contained in $B$.  (This construction is not predicative, although it may still be true predicatively that the generated subalgebra exists in some situations.)
\end{example}

\begin{example}
In some cases, we may prefer to anti-generate: given any subset $B$ of $X$, the antisubalgebra __antigenerated__ by $B$ is the union of all antisubalgebras whose elements are all distinct from ($\ne$) each element of $B$, in other words the antisubalgebra generated by the $\ne$-complement of $B$.  For example, the trivial antisubgroup of a group is antigenerated by $\{1\}$, and the trivial antiideal of a ring is antigenerated by $\{0\}$.  More generally than these examples, we may talk of the __[[cyclic subgroup|cyclic antisubgroup]]__ or __[[principal ideal|principal antiideal]]__ antigenerated by a given element of the group or ring.
\end{example}


## Quotient algebras

To form a [[quotient group]] or a [[quotient ring]], it\'s enough to have a [[normal subgroup]] or a [[two-sided ideal]].  However, if we want the quotient algebra to inherit an apartness from the original algebra, then we need antisubgroups and antiideals.

In general, instead of [[congruence relations]], use anticongruence relations.  An __anticongruence relation__ $K$ on $X$ is an [[apartness relation]] on $X$ that is also an antisubalgebra of $X \times X$.  Given this, let $R$ be the [[negation]] of $K$; then $R$ is a congruence relation, giving a quotient algebra $X/R$.  Furthermore, $K$ becomes a [[tight relation|tight]] apartness on $X/R$, relative to which the algebra operations on $X/R$ are strongly extensional.  We denote the resulting algebra-with-apartness by $X/K$.  (This notation should cause no confusion; if an apartness relation on a set $X$ is also an equivalence relation, then $X$ must be the [[empty set]], which has a unique apartness and at most one algebra structure, and the only [[quotient set]] of the empty set is itself.)  The quotient map $X \twoheadrightarrow X/K$ is also strongly extensional.

Conversely, any strongly extensional map $f\colon X \to Y$ between algebras with apartness gives rise to an anticongruence $\aker f$ on $X$ (the __antikernel__ of $f$), where $(p, q) \in \aker f$ iff $f(p) \ne f(q)$.  The complement of the antikernel is (because the apartness of $Y$ is tight) the [[kernel]] in the usual sense of universal algebra.  Thus, the quotient algebra $X/(\aker f)$ is [[naturally isomorphic]] to a [[subalgebra]] $im f$ of $Y$; the maps $X \twoheadrightarrow X/(\aker f) \cong \im f \hookrightarrow Y$ are strongly extensional.  Similarly, a sequence $X \overset{f}\to Y \overset{g} \to Z$ is [[exact sequence|exact]] iff $\im f$ is the complement of $\aker g$.

(We would like to say that there is an antisubalgebra $\aim f$ of $Y$ whose complement is $\im f$; then we could, for example, define a stronger notion of exactness requiring that $\aker g$ equal the antiimage of $f$.  In principle, $\aim f$ should be the $\ne$-complement of $\im f$.  If $X$ is Kuratowski-finite, then this works, but in general, we can prove neither that this is open nor that its complement is all of $\im f$.)

Given a group-with-apartness and a normal antisubgroup $A$, we define an anticongruence $K$, where $(p, q) \in K$ iff $p q^{-1} \in A$.  Similarly, given a ring-with-apartness and a two-sided antiideal $A$, we define an anticongruence $K$, where $(p, q) \in K$ iff $p - q \in A$.  This allows us to form quotient groups or quotient rings by modding out by normal antisubgroups or two-sided antiideals.  Conversely, we can interpret the antikernel as a normal antisubgroup or two-sided antiideal: $p \in \aker f$ iff $f(p) \ne 1$, $p \in \aker f$ iff $f(p) \ne 0$, etc.  In general, this works for any [[Omega-group]] structure.


## Localic point of view

As noted at [[apartness relation]], an apartness relation on a set $X$ is equivalent to a (strongly) closed [[equivalence relation]] on the corresponding [[discrete locale]], and the $\ne$-open subsets are those whose complementary closed sublocales are stable under this equivalence relation, and the $\ne$-topology itself is the corresponding quotient locale.  From this point of view, an algebra structure is strongly extensional if it respects the equivalence relation, hence passes to the quotient; and an antisubalgebra is an $\ne$-open set whose complementary closed sublocale is additionally a localic subalgebra, since the operation $\mathsf{C}$ from open sublocales to closed ones takes arbitrary (not only finite) unions to intersections.

In other words, antisubalgebras of an inequality algebra are equivalent to closed subalgebras of a localic algebra, in the case when the latter is the quotient of a discrete algebra by a closed localic congruence.


## Related entries

* [[anti-ideal]]


## References

According to [Troelstra and van Dalen](#TroelstraVanDalen88):

> The study of algebraic structures in an intuitionistic setting was undertaken by Heyting ([1941](#Heyting1941))... in full generality, equipped with an apartness relation.  The notion of an antisubstructure, implicit in Heyting's treatment of ideals in polynomial rings, was formulated explicitly by D.S. Scott ([1979](#Scott1979)) (N.B. the first draft of this paper contains a good deal more than the published version).  Ruitenburg ([1982](#Ruitenberg1982Thesis), [1982A](#Ruitenberg1982)) deals with intuitionistic algebra in the spirit of Heyting and Scott.

* {#Heyting1941} [[Arend Heyting]], _Untersuchungen &#252;ber intuitionistische Algebra_, 1941
  

* {#Scott1979} [[Dana Scott]], _Identity and existence in intuitionistic logic_, 1979
  

* {#Ruitenberg1982Thesis} [[Wim Ruitenberg]], _Intuitionistic Algebra_, Ph.D. Thesis, Rijksuniversiteit Utrecht, 1982
  

* {#Ruitenberg1982} [[Wim Ruitenberg]], _Primality and invertibility of polynomials_, 1982
  
* {#TroelstraVanDalen88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume II, Studies in Logic and the Foundations of Mathematics **123**: North Holland (1988) &lbrack;[ISBN:9780444703583](https://shop.elsevier.com/books/constructivism-in-mathematics-vol-2/troelstra/978-0-444-70358-3)&rbrack;

Surprisingly, antisubalgebras make hardly any appearence in 

* [[Ray Mines]], [[Fred Richman]], [[Wim Ruitenburg]]: _A Course in Constructive Algebra_, Springer (1987)



[[!redirects antisubalgebra]]
[[!redirects antisubalgebras]]
[[!redirects anti-subalgebra]]
[[!redirects anti-subalgebras]]

[[!redirects empty antisubalgebra]]
[[!redirects empty antisubalgebras]]
[[!redirects empty anti-subalgebra]]
[[!redirects empty anti-subalgebras]]

[[!redirects improper antisubalgebra]]
[[!redirects improper antisubalgebras]]
[[!redirects improper anti-subalgebra]]
[[!redirects improper anti-subalgebras]]

[[!redirects proper antisubalgebra]]
[[!redirects proper antisubalgebras]]
[[!redirects proper anti-subalgebra]]
[[!redirects proper anti-subalgebras]]

[[!redirects antisubgroup]]
[[!redirects antisubgroups]]
[[!redirects anti-subgroup]]
[[!redirects anti-subgroups]]

[[!redirects normal antisubgroup]]
[[!redirects normal antisubgroups]]
[[!redirects normal anti-subgroup]]
[[!redirects normal anti-subgroups]]

[[!redirects trivial antisubgroup]]
[[!redirects trivial antisubgroups]]
[[!redirects trivial anti-subgroup]]
[[!redirects trivial anti-subgroups]]

[[!redirects generated antisubalgebra]]
[[!redirects generated antisubalgebras]]
[[!redirects antisubalgebra generated]]
[[!redirects antisubalgebras generated]]
[[!redirects generated anti-subalgebra]]
[[!redirects generated anti-subalgebras]]
[[!redirects anti-subalgebra generated]]
[[!redirects anti-subalgebras generated]]

[[!redirects generated antisubgroup]]
[[!redirects generated antisubgroups]]
[[!redirects antisubgroup generated]]
[[!redirects antisubgroups generated]]
[[!redirects generated anti-subgroup]]
[[!redirects generated anti-subgroups]]
[[!redirects anti-subgroup generated]]
[[!redirects anti-subgroups generated]]

[[!redirects generated antiideal]]
[[!redirects generated antiideals]]
[[!redirects antiideal generated]]
[[!redirects antiideals generated]]
[[!redirects generated anti-ideal]]
[[!redirects generated anti-ideals]]
[[!redirects anti-ideal generated]]
[[!redirects anti-ideals generated]]

[[!redirects antigenerated antisubalgebra]]
[[!redirects antigenerated antisubalgebras]]
[[!redirects antisubalgebra antigenerated]]
[[!redirects antisubalgebras antigenerated]]
[[!redirects anti-generated anti-subalgebra]]
[[!redirects anti-generated anti-subalgebras]]
[[!redirects anti-subalgebra anti-generated]]
[[!redirects anti-subalgebras anti-generated]]

[[!redirects antigenerated antisubgroup]]
[[!redirects antigenerated antisubgroups]]
[[!redirects antisubgroup antigenerated]]
[[!redirects antisubgroups antigenerated]]
[[!redirects anti-generated anti-subgroup]]
[[!redirects anti-generated anti-subgroups]]
[[!redirects anti-subgroup anti-generated]]
[[!redirects anti-subgroups anti-generated]]


[[!redirects cyclic antisubgroup]]
[[!redirects cyclic antisubgroups]]
[[!redirects cyclic anti-subgroup]]
[[!redirects cyclic anti-subgroups]]


[[!redirects anticongruence]]
[[!redirects anticongruences]]
[[!redirects anti-congruence]]
[[!redirects anti-congruences]]
[[!redirects anticongruence relation]]
[[!redirects anticongruence relations]]
[[!redirects anti-congruence relation]]
[[!redirects anti-congruence relations]]

[[!redirects antikernel]]
[[!redirects antikernels]]
[[!redirects anti-kernel]]
[[!redirects anti-kernels]]

[[!redirects strongly exact sequence]]
[[!redirects strongly exact sequences]]
