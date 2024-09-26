

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


\tableofcontents

## Idea

There are many possible definitions of the (two-sided, Dedekind) real numbers type in [[dependent type theory]]. If the dependent type theory has a [[type universe]] or a [[type of all propositions]], then one can translate the impredicative definition of the [[Dedekind real numbers]] over to dependent type theory. 

However, in [[dependent type theory]] without a [[type universe]] or a [[type of all propositions]], the impredicative definition of the [[Dedekind real numbers]] no longer works. Nonetheless, it is possible to define the type of [[real numbers]] $\mathbb{R}$ via [[inference rules]] as a type with a type family of [[domains]] of the [[structural Dedekind cut]] associated with each [[real number]]. 

## Definitions

We shall assume the minimum amount of type formers in [[dependent type theory]] to define [[Dedekind cuts]] of the rational numbers: 

* [[dependent product types]], [[dependent sum types]], [[identity types]], [[empty type]], [[unit type]], [[sum types]] or [[booleans]] $\mathbb{2}$, [[bracket types]], and a [[natural numbers type]]

The types in the dependent type theory form the [[(infinity,1)-category theory|(infinity,1)-categorical]] version of a [[Heyting category]] with [[exponential objects]] and a [[natural numbers object]]. 

In addition, if one has a [[type of all propositions]] $\mathrm{Prop}$ in the [[dependent type theory]], one can define the type of real numbers as the type of all (two-sided) Dedekind cuts, which are [[subtypes]] or [[predicates]] $C:(\mathbb{2} \times \mathbb{Q}) \to \mathrm{Prop}$ of the [[product type]] $\mathbb{2} \times \mathbb{Q}$ which satisfy the following axioms:

* Dedekind cuts are bounded:
$$\exists q:\mathbb{Q}.C(0, q) \quad \exists r:\mathbb{Q}.C(1, r)$$

* Dedekind cuts are rounded:
$$\prod_{q:\mathbb{Q}} C(0, q)) \simeq \exists r:\mathbb{Q}.(q \lt r) \times C(0, r))$$
$$\prod_{r:\mathbb{Q}} C(1, r)) \simeq \exists q:\mathbb{Q}.(q \lt r) \times C(1, q))$$

* Dedekind cuts are disjoint:
$$\prod_{q:\mathbb{Q}} \neg (C(0, q)) \times C(1, q)))$$

* Dedekind cuts are located:
$$\prod_{q:\mathbb{Q}} \prod_{r:\mathbb{Q}} (q \lt r) \to (C(0, q)) \vee C(1, r))$$

Usually, Dedekind cuts are presented as pairs of predicates $(L, U):(\mathbb{Q} \to \mathrm{Prop}) \times (\mathbb{Q} \to \mathrm{Prop})$, but this is equivalent to the above definition, since for any types $A$, $B$, and $C$, one has that 
$$((A + B) \to C) \simeq (A \to C) \times (B \to C)$$
and for any type $A$, one has that 
$$(A + A) \simeq (\mathbb{2} \times A)$$

The predicate $\mathrm{isCut}(C)$ is defined as the product of all the axioms above, and the type of real numbers is defined as 
$$\mathbb{R} \coloneqq \sum_{C:(\mathbb{2} \times \mathbb{Q}) \to \mathrm{Prop}} \mathrm{isCut}(C)$$

In dependent type theory with a [[type universe]] $U$, one can take the type of all $U$-small propositions by the dependent sum type 

$$\mathrm{Prop}_U \coloneqq \sum_{A:U} \mathrm{isProp}(A)$$

and define locally $U$-small Dedekind cuts $C:(\mathbb{2} \times \mathbb{Q}) \to \mathrm{Prop}_U$ and the (locally $U$-small) real numbers $\mathbb{R}_U$ using $\mathrm{Prop}_U$. 

So, what happens if the dependent type theory has neither a [[type of all propositions]] nor a [[type universe]], so that we are working in fully [[predicative mathematics]]? It is no longer possible to quantify over all subtypes of $\mathbb{2} \times \mathbb{Q}$, so one cannot define the type of real numbers impredicatively. Also, without impredicativity, a [[subtype]] of the sum type $\mathbb{2} \times \mathbb{Q}$ is a type $C$ with an [[embedding of types]] $e:C \hookrightarrow (\mathbb{2} \times \mathbb{Q})$. One can show from the definition of embedding that given an element $x:\mathbb{2} \times \mathbb{Q}$, the [[fiber type]] of $e$ at $x$ is a [[mere proposition]]
$$\mathrm{isProp}\left(\sum_{z:C} e(z) =_{\mathbb{2} \times \mathbb{Q}} x\right)$$
so everywhere in the definition above where one would have used the type family $C(x)$ one can instead use the [[dependent sum type]] $\mathrm{fiber}(e, x) \coloneqq \sum_{z:C} e(z) =_{\mathbb{2} \times \mathbb{Q}} x$. 

Then a Dedekind cut consists of a type $C$ with an embedding of types $e:C \hookrightarrow (\mathbb{2} \times \mathbb{Q})$, which satisfies the following axioms:

* Dedekind cuts are bounded:
$$\exists q:\mathbb{Q}.\mathrm{fiber}(e, (0, q)) \quad \exists r:\mathbb{Q}.\mathrm{fiber}(e, (1, r))$$

* Dedekind cuts are rounded:
$$\prod_{q:\mathbb{Q}} \mathrm{fiber}(e, (0, q)) \simeq \exists r:\mathbb{Q}.(q \lt r) \times \mathrm{fiber}(e, (0, r))$$
$$\prod_{r:\mathbb{Q}} \mathrm{fiber}(e, (1, r)) \simeq \exists q:\mathbb{Q}.(q \lt r) \times \mathrm{fiber}(e, (1, q))$$

* Dedekind cuts are disjoint:
$$\prod_{q:\mathbb{Q}} \neg (\mathrm{fiber}(e, (0, q)) \times \mathrm{fiber}(e, (1, q)))$$

* Dedekind cuts are located:
$$\prod_{q:\mathbb{Q}} \prod_{r:\mathbb{Q}} (q \lt r) \to (\mathrm{fiber}(e, (0, q)) \vee \mathrm{fiber}(e, (1, r))$$

The predicate $\mathrm{isCut}(C, e)$ is defined as the product of all the axioms above, and the type of all Dedekind cuts with [[domain]] $C$ is given by the dependent sum type

$$\mathrm{Cuts}(C) \coloneqq \sum_{e:C \hookrightarrow \mathbb{2} \times \mathbb{Q}} \mathrm{isCut}(C, e)$$

If there existed a type universe, one can simply define the real numbers as the type of Dedekind cuts in $U$;

$$\mathbb{R}_U \coloneqq \sum_{C:U} \mathrm{Cuts}(C)$$

However, while there is no type universe $U$, one can add inference rules for the type of real numbers $\mathbb{R}$ such that $\mathbb{R}$ behaves as the [[dependent sum type]] $\sum_{C:U} \mathrm{Cuts}(C)$ if the hypothetical $U$ contained every single type in the type theory. 

Formation rules for the real numbers type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{R} \; \mathrm{type}}$$

Introduction rules for real numbers type:

$$\frac{\Gamma \vdash C \; \mathrm{type}}{\Gamma \vdash \mathrm{inR}_C:\mathrm{Cuts}(C) \to \mathbb{R}}$$

Elimination rules for real numbers type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, x:\mathbb{R} \vdash \mathrm{CutDomain}(x) \; \mathrm{type}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma, x:\mathbb{R} \vdash \mathrm{cut}(x):\mathrm{Cuts}(\mathrm{CutDomain}(x))}$$

Computation rules for real numbers type:

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad c:\mathrm{Cuts}(C)}{\Gamma \vdash \mathrm{CutDomain}(\mathrm{inR}_C(c)) \equiv C \; \mathrm{type}} \quad \frac{\Gamma \vdash C \; \mathrm{type} \quad c:\mathrm{Cuts}(C)}{\Gamma \vdash \mathrm{cut}(\mathrm{inR}_C(c)) \equiv c:\mathrm{Cuts}(C)}$$

Uniqueness rules for real numbers type:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, x:\mathbb{R} \vdash \mathrm{inR}_{\mathrm{CutDomain}(x)}(\mathrm{cut}(x)) \equiv x:\mathrm{Cuts}(\mathrm{CutDomain}(x))}$$

The inference rules for the real numbers type imply that the real numbers type are a [[Tarski universe]] with universal type family $\mathrm{CutDomain}(x)$ indexed by $x:\mathbb{R}$, where $\mathrm{CutDomain}(x)$ is the [[domain]] of the [[Dedekind cut]] 
$$\mathrm{cut}(x):\mathrm{CutDomain}(x) \hookrightarrow (\mathbb{2} \times \mathbb{Q})$$ 
associated with the real number $x:\mathbb{R}$. This makes the real numbers type similar to other [[type universes]] such as the [[type of all propositions]] or the [[type of finite types]]. 

### As a terminal object

An [[Archimedean ordered field]] can be defined in any dependent type theory with the following types:

* [[dependent product types]], [[dependent sum types]], [[identity types]], [[empty type]], [[unit type]], [[sum types]], [[bracket types]], and a [[natural numbers type]]

Then the real numbers type $\mathbf{R}$ is the homotopy terminal Archimedean ordered field. 

If the [[dependent type theory]] has [[quotient sets]], then it is provable that $\mathbf{R}$ is Cauchy complete. From the definition of homotopy terminal Archimedean ordered field, $\mathbf{R}$ is an algebra of the endofunctor $X \mapsto \mathcal{C}(X)$ which takes Archimedean ordered fields $X$ to the Archimedean ordered field $\mathcal{C}(X)$ of [[equivalence classes]] of Cauchy sequences in $X$. Every algebra of the endofunctor $X \mapsto \mathcal{C}(X)$ in the type of Archimedean ordered field is a Cauchy complete Archimedean ordered field. 

Similarly, if [[power sets]] of Archimedean ordered fields exist, then it is provable that $\mathbf{R}$ is Dedekind complete. From the definition of homotopy terminal Archimedean field, $\mathbf{R}$ is an algebra of the endofunctor $X \mapsto \mathcal{D}(X)$ which takes Archimedean ordered fields $X$ to the Archimedean ordered field $\mathcal{C}(X)$ of two-sided Dedekind cuts in $X$. Every algebra of the endofunctor $X \mapsto \mathcal{D}(X)$ in the type of Archimedean ordered field is a Dedekind complete Archimedean ordered field. 

If a real numbers type $R$ as defined in the previous section also exists, then it is a [[subtype]] of this real numbers type $\mathbb{R}$ defined as the terminal Archimedean ordered field, since $R$ is provably Archimedean ordered, and any [[ring homomorphisms]] between two field objects is an [[embedding of types]], and by definition of terminal object, there is always a ring homomorphism $R \to \mathbb{R}$. 

## Properties

The type of real numbers is the Coquand universe of all Dedekind cuts. Since real numbers and Dedekind cuts are interdefinable via the rules of Coquand universes, we shall just be directly defining the algebraic operations and order relations on Dedekind cuts; the corresponding operations on real numbers follow from the rules of Coquand universes. 

### Algebraic structure on real numbers

\begin{definition}
Addition of two Dedekind cuts $(C, e_C)$ and $(D, e_D)$ is given by the type

$$C + D \coloneqq \sum_{(b, q):\mathbb{2} \times \mathbb{Q}} \exists r, s:\mathbb{Q}.\mathrm{fiber}(e_C, (b, r)) \times \mathrm{fiber}(e_D, (b, s)) \times (q =_\mathbb{Q} r + s)$$

with the [[embedding]] $e_{C + D}$ given by the first projection function of the [[dependent sum type]] into the product type $\mathbb{2} \times \mathbb{Q}$. 
\end{definition}

The swap function $\mathrm{swap}:\mathbb{2} \to \mathbb{2}$ on the booleans is inductively defined by $\mathrm{swap}(0) \coloneqq 1$ and $\mathrm{swap}(1) \coloneqq 0$. 

\begin{definition}
The additive inverse of a Dedekind cut $(C, e_C)$ is given by the type

$$-C \coloneqq \sum_{(b, q):\mathbb{2} \times \mathbb{Q}} \exists r:\mathbb{Q}.\mathrm{fiber}(e_C, (\mathrm{swap}(b), r)) \times (q =_\mathbb{Q} -r)$$

with the [[embedding]] $e_{-C}$ given by the first projection function of the [[dependent sum type]] into the product type $\mathbb{2} \times \mathbb{Q}$. 
\end{definition}

With these operations, the real numbers form an abelian group. 

## Related concepts

* [[real numbers object]]

* [[Dedekind real numbers]]

## References

For the impredicative definition of the real numbers using a type of propositions, as well as the algebraic operations and order relations for real numbers see section 11.2 of:

* [[Univalent Foundations Project]], section 11.2 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

[[!redirects real numbers type]]
[[!redirects real numbers types]]

[[!redirects type of real numbers]]
[[!redirects types of real numbers]]

[[!redirects universe of real numbers]]
[[!redirects universes of real numbers]]