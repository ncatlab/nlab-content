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

### In set theory

Given a [[set]] $S$ and an [[equivalence relation]] $\equiv$ on $S$, the __quotient set__ of $S$ by $\equiv$ is the set $S/{\equiv}$ whose elements are the elements of $S$ but where two elements are now considered [[equality|equal]] if in $S$ they were merely equivalent.

If changing the definition of equality like this is not allowed in the given [[foundations]] of mathematics, then one can still define $S/{\equiv}$ as a [[subset]] of the [[power set]] of $S$. 

* In [[material set theory]] the definition is as follows:
\[\label{setdef}
A \in S/{\equiv} \;\Leftrightarrow\; \exists (x: S),\; A = \{y: S \;\mid\; x \equiv y\}\]
* In [[structural set theory]] the definition is slightly different, because sets are not elements of sets and one cannot in general compare sets for strict equality. 

If there are also no (extensional) power sets in the foundations of mathematics, then there are two alternatives: 

* One could use [[setoids]] (in which case, perhaps one would do better to change your terminology as described there). 
* One could just include the existence of [[quotient objects]] in [[Set]] as an axiom (the __axiom of quotient sets__. 

The latter is the case if one assumes that $\Set$ is a [[pretopos]] or a [[Grothendieck topos]] as given by [[Giraud's axioms]]). There are actually two possible axiom of quotient sets, depending on what definition of relation one uses. 

* The weaker version of the axiom of quotient sets is the one which states that the [[coherent category]] $Set$ is a [[pretopos]]: that every [[internal equivalence relation]] on a set $A$, defined as a subset $\equiv$ of the Cartesian product $A \times A$ satisfying reflexivity, transitivity, and symmetry, has a quotient set $A/\equiv$. 

* The stronger version of the axiom of quotient sets states that every [[proposition]] $x \equiv y$ in the [[context]] of the [[variables]] $x \in A$ and $y \in A$ which satisfies reflexivity, transitivity, and symmetry has a quotient set $A/\equiv$. In some presentations of [[set theory]], this is an [[axiom schema]] of quotient sets.  

In any case, the element of $S/{\equiv}$ that comes from the element $x$ of $S$ may be denoted $[x]_{\equiv}$, or simply $[x]$ if ${\equiv}$ is understood, or simply $x$ if there will be no confusion as to which set it is an element of.  This $[x]$ is called the __[[equivalence class]]__ of $x$ with respect to $\equiv$; the term 'class' here is an old word for 'set' (in the sense of 'subset') and refers to the definition (eq:setdef) above, where $[x]$ is literally the set $A$.

#### As initial objects in a category

Let $S$ be a [[set]] and let $\equiv$ be an [[equivalence relation]] on $S$. Let us define a *quotient set algebra of $S$ and $\equiv$* to be a set $A$ with a function $\iota S \to A$ such that for all $a \in S$ and $b \in S$, $(a \equiv b)$ implies $(\iota(a) = \iota(b))$. 

A *quotient set algebra homomorphism of $S$ and $\equiv$* is a function $f: A \to B$ between two quotient set algebras $A$ and $B$ such that for all $a \in S$, $f(\iota_A(a)) = \iota_B(a)$.

The *category of quotient set algebras of $S$ and $\equiv$* is the category $QSA(S, \equiv)$ whose objects $Ob(QSA(S, \equiv))$ are quotient set algebras of $S$ and $\equiv$ and whose morphisms $Mor(A, B)$ for $A \in Ob(QSA(S, \equiv))$ and $B \in Ob(QSA(S, \equiv))$ are quotient set algebra homomorphisms of $S$ and $\equiv$. The **quotient set** of $S$ and $\equiv$, denoted $S/\equiv$, is defined as the initial object in the category of quotient set algebras of $S$ and $\equiv$. 

### In dependent type theory

Similar to set theory, there are multiple ways of defining quotient sets in [[dependent type theory]]. If the type theory has a [[univalent]] [[type of all propositions]] $(\mathrm{Prop}, \mathrm{El})$ and thus [[power sets]] $\mathcal{P}T \coloneqq T \to \mathrm{Prop}$ of a type $T$, then given a type $T$ with an equivalence relation $(-)\equiv(-):\mathcal{P}(T \times T)$, one could construct the quotient set $T/\equiv$ as a [[subtype]] of the [[power set]], as follows: we first define the [[predicate]] on the powerset $\mathcal{P}T$:

$$P:\mathcal{P}T \vdash \mathrm{isEquivalenceClass}(P) \coloneqq \left[\sum_{x:T} \prod_{y:T} P(x) =_\mathrm{Prop} (x \equiv y) \right]$$

since by [[univalence]] there is an equivalence between the types $P(x) =_\mathrm{Prop} (x \equiv y)$ and $\mathrm{El}(P(x)) \simeq \mathrm{El}(x \equiv y)$, which for propositions is the same as $\mathrm{El}(P(x)) \iff \mathrm{El}(x \equiv y)$. Then we define the subtype 

$$T/\equiv \coloneqq \sum_{P:\mathcal{P}T} isEquivalenceClass(P)$$

Alternatively, if the [[dependent type theory]] does not have a type of all propositions, then the quotient set $T/\equiv$ can still nevertheless be constructed. The analogue of the axiom of quotient sets in dependent type theory is the rules for the quotient set [[higher inductive type]]. In particular, the quotient set $T/\equiv$ is a [[higher inductive type]] inductively generated by the following:

* a function $\iota: T \to T/\equiv$

* a family of dependent terms

  $$
    a \colon T
    ,\; 
    b \colon T 
    \;\;\; \vdash \;\;\; 
    eq_{T/\equiv}(a, b)
    \,\colon\, 
    (a \equiv b) 
    \;\to\; 
    (\iota(a) =_{T/\equiv} \iota(b))
  $$

* a family of dependent terms 
$$a:T/\equiv, b:T/\equiv \vdash \tau(a, b): isProp(a =_{T/\equiv} b)$$

In general, if one doesn't have impredicative quotient sets or quotient sets as a higher inductive type, than one could only construct quotient sets of equivalence relations with a choice of unique representatives, which for equivalence relation $R(x, y)$ indexed by $x:A$ and $y:A$ consists of a type family $C(x)$ indexed by $x:A$, and an element of type

$$\prod_{x:A} \exists!y:A.C(x) \times R(x, y)$$

Then the type $\sum_{x:A} C(x)$ is the quotient set of $A$ with respect to $R$. 

Equivalently, one could use functions instead of type families, and say that a choice of unique representatives is a type $C$ with a function $f:C \to A$ and an element of type 

$$\prod_{x:A} \exists!y:A.\left(\sum_{z:C} f(z) =_A x\right) \times R(x, y)$$

Then 
$$C \simeq \sum_{x:A} \sum_{z:C} f(z) =_A x$$ 
is the quotient set of $A$ with respect to $R$. 

## Generalisations

Quotient sets in [[Set]] generalise to [[quotient object]]s in other categories. In particular, an [[exact category]] is a [[regular category]] in which every [[congruence]] on every object has an effective quotient object.

## See also 

* [[equivalence relation]]

* [[setoid]]

* [[quotient type]]

* [[higher inductive type]]

## Rereferences

For quotient sets in [[dependent type theory]], see:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

See the references at *[[quotient type]]*.

category: foundational axiom

[[!redirects quotient set]]
[[!redirects quotient sets]]

[[!redirects axiom of quotient sets]]
[[!redirects axiom of quotients]]
