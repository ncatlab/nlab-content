+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Quotient sets
* table of contents
{: toc}

## Definitions

Given a [[set]] $S$ and an [[equivalence relation]] $\equiv$ on $S$, the __quotient set__ of $S$ by $\equiv$ is the set $S/{\equiv}$ whose elements are the elements of $S$ but where two elements are now considered [[equality|equal]] if in $S$ they were merely equivalent.

If changing the definition of equality like this is not allowed in your [[foundations]] of mathematics, then you can still define $S/{\equiv}$ as a [[subset]] of the [[power set]] of $S$ as follows:
\[\label{setdef}
A \in S/{\equiv} \;\Leftrightarrow\; \exists (x: S),\; A = \{y: S \;\mid\; x \equiv y\}\]
If you don\'t have (extensional) power sets either, then you\'ll have to use [[setoids]] (in which case, perhaps you\'d do better to change your terminology as described there).  Alternatively, don\'t worry about any of this and just include the existence of [[quotient objects]] in [[Set]] as an axiom (the __axiom of quotient sets__, which you have if you assume that $\Set$ is a [[pretopos]] or a [[Grothendieck topos]] as given by [[Giraud's axioms]]).

In any case, the element of $S/{\equiv}$ that comes from the element $x$ of $S$ may be denoted $[x]_{\equiv}$, or simply $[x]$ if ${\equiv}$ is understood, or simply $x$ if there will be no confusion as to which set it is an element of.  This $[x]$ is called the __[[equivalence class]]__ of $x$ with respect to $\equiv$; the term 'class' here is an old word for 'set' (in the sense of 'subset') and refers to the definition (eq:setdef) above, where $[x]$ is literally the set $A$.

### As initial objects in a category

Let $S$ be a [[set]] and let $\equiv$ be an [[equivalence relation]] on $S$. Let us define a *quotient set algebra of $S$ and $\equiv$* to be a set $A$ with a function $\iota S \to A$ such that for all $a \in S$ and $b \in S$, $(a \equiv b)$ implies $(\iota(a) = \iota(b))$. 

A *quotient set algebra homomorphism of $S$ and $\equiv$* is a function $f: A \to B$ between two quotient set algebras $A$ and $B$ such that for all $a \in S$, $f(\iota_A(a)) = \iota_B(a)$.

The *category of quotient set algebras of $S$ and $\equiv$* is the category $QSA(S, \equiv)$ whose objects $Ob(QSA(S, \equiv))$ are quotient set algebras of $S$ and $\equiv$ and whose morphisms $Mor(A, B)$ for $A \in Ob(QSA(S, \equiv))$ and $B \in Ob(QSA(S, \equiv))$ are quotient set algebra homomorphisms of $S$ and $\equiv$. The **quotient set** of $S$ and $\equiv$, denoted $S/\equiv$, is defined as the initial object in the category of quotient set algebras of $S$ and $\equiv$. 

## Generalisations

Quotient sets in [[Set]] generalise to [[quotient object]]s in other categories.  In particular, an [[exact category]] is a [[regular category]] in which every [[congruence]] on every object has an effective quotient object.

## See also 

* [[equivalence relation]]
* [[setoid]]

category: foundational axiom

[[!redirects quotient set]]
[[!redirects quotient sets]]

[[!redirects axiom of quotient sets]]
[[!redirects axiom of quotients]]
