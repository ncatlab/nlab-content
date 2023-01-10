> This page is about the notion in [[homotopy type theory|homotopy]] [[type theory]]. For *[[parallel transport]]* via [[connections]] in [[differential geometry]] see there. For the relation see [below](#RelationToParallelTransport).

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##
 {#Idea}

[[Gottfried Leibniz]] said (in translation from [Lewis 1918, p. 373](#Lewis18) with original Latin terms in parenthesis; see also [Cartwright 1971, p. 119](#Cartwright71) and [Gries & Schneider 1998](#GriesSchneider98))

> Two terms are the same (eadem) if one can be substituted for the otherwithout altering the truth of any statement (salva veritate). If we have $P$ and $Q$, and $P$ enters into some true proposition, and the substitution of $Q$ for $P$ wherever it appears results in a new proposition that is likewise true, and if this can be done for every proposition, then $P$ and $Q$ are said to be the same; conversely, if $P$ and $Q$ are the same, they can be substituted for one another.

The converse mentioned at the end of the last sentence is known as the **principle of substitution** or the **indiscernibility of identicals**. In any simply typed first-order theory, given a predicate $P$ on $T$, this principle is formalized as the following

$$\forall x,y:T.(x =_T y) \implies (P(x) \iff P(y))$$

In the interpretation of [[propositions as types]] in [[type theory]], [[propositions]] are interpreted as [[types]], and the above statement has a generalization from the types which are propositions to all types: the [[universal quantifier]] becomes a [[dependent product type]], the [[predicate]] becomes a [[type family]], [[implication]] becomes an a [[function type]], and [[logical equivalence]] of [[propositions]] becomes an [[equivalence type]]. This results in what is known as *transport* in type theory, which for the type $T$ and the type family $x:T \vdash P(x)$ results in the [[dependent function]]:

$$\mathrm{tr}_P:\prod_{x,y:T} (x =_T y) \to (P(x) \simeq P(y))$$

## Definitions

### Using the uniqueness quantifier

Assuming that the type theory has [[uniqueness quantifiers]], a [[type]] $A$, a family of types $x:A \vdash B(x)$, [[elements]] $a:A$ and $b:A$, and an [[identity]] $p:a =_A b$, there is a family of elements between the types $B(a)$ and $B(b)$ called **transport**
$$x:B(a) \vdash \mathrm{tr}_B(a, b, p)(x):B(b)$$
and a witness 
$$y:B(b) \vdash \epsilon(\mathrm{tr}_B(a, b, p))(y):\exists! x:B(a).\mathrm{tr}_B(a, b, p)(x) =_{B(b)} y$$
that for all $y:B(b)$ there exists a unique elemnt $x:B(a)$ up to identity such that $\mathrm{tr}_B(a, b, p)(x) =_{B(b)} y$. 

### Using equivalence types

There are multiple notions of [[equivalence types]] in [[dependent type theory]], which can be used for a definition of univalence for a [[type universe]] $U$; these include

* [[judgmentally strict equivalence types]]
* [[propositionally strict equivalence types]]
* various notions of [[weak equivalence types]]
  * the type of [[functions]] with [[contractible type|contractible]] [[fiber type|fibers]]
  * the type of [[spans]] with contractible fibers
  * the type of [[multivalued partial functions]] which are single-valued and [[total function|total]] and have contractible fibers
  * the type of [[one-to-one correspondences]]
* type of $U$-small equivalences, given a type universe $U$ and a definition of equivalence above

Thus, given a notion of [[equivalence type]] $\simeq$, a [[type]] $A$, a family of types $x:A \vdash B(x)$, [[elements]] $a:A$ and $b:A$, and an [[identity]] $p:a =_A b$, there is an equivalence between the types $B(a)$ and $B(b)$ called **transport** 
$$\mathrm{tr}_B(a, b, p):B(a) \simeq B(b)$$

The transport equivalence is called **judgmentally strict transport** if the equivalence type is a [[judgmentally strict equivalence type]], and similarly it is called **propositionally strict transport** if the equivalence type is a [[propositionally strict equivalence type]]. It is called **weak transport** if the equivalence type is a [[weak equivalence type]]. 

### As an introduction rule for the equivalence type

In some presentations of the [[equivalence type]], transport is formed by one of the [[introduction rules]] for the equivalence type: 
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B \; \mathrm{type}}{\Gamma \vdash \mathrm{tr}_B(a, b, p):B(a) \simeq B(b) \; \mathrm{type}}$$

For the [[inductive definition]] of transport, there are also [[computation rules]] given by

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{tr}_B(a, a, \mathrm{refl}_A(a)) \equiv \mathrm{id}_{B(a)}:B(a) \simeq B(a)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{tr}_B(a, a, \mathrm{refl}_A(a)) \equiv_{B(a) \simeq B(a)} \mathrm{id}_{B(a)} \; \mathrm{true}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash P \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B^{\mathrm{tr}}(a):\mathrm{tr}_B(a, a, \mathrm{refl}_A(a)) =_{B(a) \simeq B(a)} \mathrm{id}_{B(a)}}$$

depending on whether the the computation rules for [[identity types]] use [[judgmental equality]], [[propositional equality]], or the [[identity type]]. 

Alternatively, one has the [[dependent action on identities]] for the [[computation rules]] for transport:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{tr}_B(a, b, p)(w(a)) \equiv w(b):B(b)}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{tr}_B(a, b, p)(w(a)) \equiv_{B(b)} w(b) \; \mathrm{true}}$$ 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash w:B(x)}{\Gamma \vdash \mathrm{apd}_B(a, b, p, w):\mathrm{tr}_B(a, b, p)(w(a)) =_{B(b)} w(b)}$$ 

depending on whether the [[equivalence type]] uses [[judgmental equality]], [[propositional equality]], or the [[identity type]] in its [[computation rules]]. 

## Examples and applications

### Univalent Tarski universes

Tarski universes are types which behave like internal models of [[dependent type theory]] inside of the type theory itself. We use a very general notion of Tarski universe: a Tarski universe merely consists of a type of encodings for types $\mathcal{U}$ and a universal type family $\mathcal{T}_\mathcal{U}$. Given an encoding $A:\mathcal{U}$, an internal type family indexed by $A$ is a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$. 

There are two ways to say that $A:\mathcal{U}$ and $B:\mathcal{U}$ are the same, by way of the [[identity type]] of the Tarski universe $A =_\mathcal{U} B$, and by way of the [[equivalence in homotopy type theory|type of equivalences]] between the type reflections of $A:\mathcal{U}$ and $B:\mathcal{U}$, $\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B)$. By [[transport]], there is a canonical function 
$$\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B):(A =_\mathcal{U} B) \to (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$
The Tarski universe $\mathcal{U}$ is then said to be a [[univalent universe]] if the transport function $\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B)$ is an equivalence of types
$$\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B):(A =_\mathcal{U} B) \simeq (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$
for all encodings $A:\mathcal{U}$ and $B:\mathcal{U}$. 

One could also internalize the type of equivalences inside of the Tarski universe $\mathcal{U}$, but that requires the Tarski universe be closed under [[identity types]],  [[dependent product types]], and [[dependent sum types]].

A Tarski universe $\mathcal{U}$ is weakly closed under identity types if it has an internal encoding of identity types in the Tarski universe: Given an element $A:\mathcal{U}$, there is a function $\mathrm{Id}_A^\mathcal{U}:\mathcal{T}_\mathcal{U}(A) \times \mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$ and for all elemments $a:\mathcal{T}_\mathcal{U}(A)$ and $b:\mathcal{T}_\mathcal{U}(A)$ an equivalence 
$$\mathrm{canonical}_{\mathrm{Id}_A}(a, b):\mathcal{T}_\mathcal{U}(\mathrm{Id}_A^\mathcal{U}(a, b)) \simeq (a =_{\mathcal{T}_\mathcal{U}(A)} b)$$

A Tarski universe $\mathcal{U}$ is weakly closed under dependent product types if it has an internal encoding of dependent product types in the Tarski universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$, there is an element $\Pi_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Pi(A, B):\mathcal{T}_\mathcal{U}(\Pi_\mathcal{U}(x:A).B(x)) \simeq \prod_{x:\mathcal{T}_\mathcal{U}(A)} \mathcal{T}_\mathcal{U}(B(x))$$

A Tarski universe $\mathcal{U}$ is weakly closed under dependent sum types if it has an internal encoding of dependent sum types in the Tarski universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$, there is an element $\Sigma_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Sigma(A, B):\mathcal{T}_\mathcal{U}(\Sigma_\mathcal{U}(x:A).B(x)) \simeq \sum_{x:\mathcal{T}_\mathcal{U}(A)} \mathcal{T}_\mathcal{U}(B(x))$$

Every Tarski universe $\mathcal{U}$ which is weakly closed under identity types, dependent product types, and dependent sum types types has an internal encoding of type of equivalences $A \simeq_\mathcal{U} B$, defined for all $A:\mathcal{U}$ and $B:\mathcal{U}$ as
$$A \simeq_\mathcal{U} B \coloneqq \Sigma_\mathcal{U}(f:A \to_\mathcal{U} B).\mathrm{isEquiv}_\mathcal{U}(f)$$
with $\mathrm{isEquiv}_\mathcal{U}$ defined by whatever suitable definition of [[equivalence in homotopy type theory]]. 

Thus, there is a third way to say that $A:\mathcal{U}$ and $B:\mathcal{U}$ are the same, by way of the type reflection of the internal encoding of the type of equivalences: $\mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$. It could be proven, from the closure of the universe under identity types, dependent product types, and dependent sum types, that there is an equivalence 
$$\mathrm{canonical}_\simeq(A, B):\mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B) \simeq (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$

There is a more common definition of a univalent Tarski universe: a  Tarski universe $\mathcal{U}$ is a [[univalent universe]] if the canonical function 
$$\mathrm{idtoequiv}(A, B):(A =_\mathcal{U} B) \to \mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$$
is an equivalence
$$\mathrm{idtoequiv}(A, B):(A =_\mathcal{U} B) \simeq \mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$$
These two definitions of univalent universes are the same. In order to show that the two definitions are the same, we need to show that there is an identification 
$$i(p):\mathrm{canonical}_\simeq(A, B)(\mathrm{idtoequiv}(A, B)(p)) =_{\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B)}  \mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B)(p)$$
for all identifications $p:A =_\mathcal{U} B$. By the J rule it is enough to show that $\mathrm{canonical}_\simeq(A, A)$ maps the identity function of $\mathcal{T}_\mathcal{U}(A \to_\mathcal{U} A)$ to the identity function of $\mathcal{T}_\mathcal{U}(A) \to \mathcal{T}_\mathcal{U}(A)$. Since the identity function in $\mathcal{T}_\mathcal{U}(A \to_\mathcal{U} A)$ is just $\mathrm{canonical}_\simeq^{-1}(A, A)(id_A)$ the above statement is always true. Thus, the second definition of a univalent universe is equivalent to the definition by transport. 

These results apply to strictly Tarski universes as well, which are strictly closed rather than weakly closed (the equivalences become [[definitional equality]]): since $A \equiv B$ implies that $A \simeq B$ for types $A$ and $B$, every strictly Tarski universe is weakly Tarski. 

### Relation to parallel transport

\begin{remark}\label{RelationToParallelTransport}
**(relation to parallel transport -- [[schreiber:differential cohomology in a cohesive topos|dcct §3.8.5]], [ScSh12 §3.1.2](cohesive+homotopy+type+theory#SchreiberShulman2012))**
\linebreak
  In [[cohesive homotopy type theory]] the [[shape modality]] $\esh$ has the [[shape via cohesive path ∞-groupoid|interpretation]] of turning any cohesive type $X$ into its [[path infinity-groupoid|path $\infty$-groupoid]] $\esh X$: The [[1-morphisms]] $p \colon (x =_{\esh X} y)$ of $\esh X$ have the [[shape via cohesive path ∞-groupoid|interpretation]] of being (whatever identities existed in $X$ composed with) cohesive (e.g. [[continuous function|continuous]] or [[smooth function|smooth]]) *[[paths]]* in $X$, and similarly for the higher order paths-of-paths.

Accordingly, an [[shape modality|$\esh X$]]-[[dependent type]] $B$ has the interpretation of being a "[[local system]]" of $B$-[[coefficients]] over $X$, namely a $B(x)$-[[fiber infinity-bundle|fiber $\infty$-bundle]] equipped with a [[flat infinity-connection|flat $\infty$-connection]]. 

In this case, the identity transport (eq:TheTransportFunctions) along paths in [[shape modality|$\esh X$]] has the interpretation of being the *[[parallel transport]]* (in the original sense of [[differential geometry]]) with respect to this [[flat infinity-connection|flat $\infty$-connection]] (and the [[higher parallel transport]] when applied to paths-of-paths).
\end{remark}

## See also ##

* [[identity type]]

* [[dependent identity type]]

* [[identity of indiscernibles]]

## References ##

* [[Univalent Foundations Project|UVP]], [§2.3 "Type families and fibrations"](https://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf#page=81) in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

Some more details are spelled out in:

* [[Egbert Rijke]], pp. 18 in: *Homotopy Type Theory* (2012) &lbrack;[pdf](https://studenttheses.uu.nl/bitstream/handle/20.500.12932/11704/hott.pdf?sequence=1)&rbrack;

Implementation in [[Agda]]:

* [[Martín Hötzel Escardó]], *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580), [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)&rbrack;

Leibniz's original paragraph (from an unpublished manuscript probably written after 1683) is reproduced in the Latin Original in

* {#Gerhard1890} K. Gerhard (ed.), Section XIX, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) in: *Die philosophischen Schriften von Gottfried Wilhelm Leibniz*, Siebenter Band, Weidmannsche Buchhandlung (1890) &lbrack;[archive.org](https://archive.org/details/diephilosophisc00gerhgoog/page/n7/mode/2up)&rbrack;

and in English translation in:

* {#Lewis18} [[Clarence I. Lewis]], Appendix (p. 373) of: *A Survey of Symbolic Logic*, University of California (1918) &lbrack;[[LewisAppendix-LeibnizIndiscernibles.pdf:file]]&rbrack;

and further discussed in:

* {#Cartwright71} [[Richard Cartwright]], *Identity and Substitutivity*, p. 119-133 of: Milton Munitz (ed.) *Identity and Individuation*, New York University Press (1971) &lbrack;[[Cartwright-IdentityAndSubstitutivity.pdf:file]]&rbrack;

* {#GriesSchneider98} David Gries, Fred Schneider, *Formalizations Of Substitution Of Equals For Equals* (1998) &lbrack;[pdf](https://ecommons.cornell.edu/bitstream/handle/1813/7340/98-1686.pdf?sequence=1&isAllowed=y), [ecommons:1813/7340](https://ecommons.cornell.edu/handle/1813/7340)

The understanding of transport in HoTT as expressing [[Leibniz]]'s principle of "[[indiscernibility of identicals]]" (aka "substitution of equals", "substitutivity") has been made explicit in:

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 in: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], §3.1 in: *Univalent foundations and the equivalence principle*, in: *Reflections on the Foundations of Mathematics*, Synthese Library **407** Springer (2019)  &lbrack;[arXiv:2202.01892](https://arxiv.org/abs/2202.01892), [doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

The converse implication of [[path induction]] from transport (together with the uniqueness principle for id-types) is made explicit in:

* [Ladyman & Presnell 2015, §6.3](#LadymanPresnell15)

* Lennard Götz, §4.2 of: *Martin-Löf's J-rule*, LMU (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Goetz.pdf)&rbrack; 

For the role of transport in defining an equivalent notion of [[univalence]] in [[weakly Tarski universes]], see:

* Madeleine Birchfield, Valery Isaev, *Univalence for weakly Tarski universes*, MathOverflow, ([web](https://mathoverflow.net/q/431723))

[[!redirects transport]]
[[!redirects transports]]

[[!redirects weak transport]]
[[!redirects weak transports]]

[[!redirects strict transport]]
[[!redirects strict transports]]

[[!redirects judgmentally strict transport]]
[[!redirects judgmentally strict transports]]

[[!redirects propositionally strict transport]]
[[!redirects propositionally strict transports]]

[[!redirects transporting]]

[[!redirects identity transport]]
[[!redirects identity transports]]

[[!redirects type transport]]
[[!redirects type transports]]

[[!redirects transport equivalence]]
[[!redirects transport equivalences]]

[[!redirects transport function]]
[[!redirects transport functions]]

[[!redirects indiscernibility of identicals]]

[[!redirects principle of substitutivity]]
[[!redirects principle of substitution]]
[[!redirects principle of substitution of equals for equals]]
[[!redirects principle of substituting equals for equals]]