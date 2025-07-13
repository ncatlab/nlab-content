
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Extensional type theory_ denotes the flavor of [[type theory]] in which [[identity types]] satisfy the *reflection rule*, saying that if two terms are [[typal equality|typally equal]] then they are also [[judgmental equality|judgmentally equal]].

In particular, this implies that all [[identity types]] are [[propositions]] / of [[h-level 1]], and thus equivalently that all types are required to be [[h-sets]].  Therefore, extensional type theory is a [[set-level type theory]], and hence a form of [[set-level foundations]].  However, there are other set-level type theories, such as those obtained by adding [[UIP]] as an axiom.

__Note:__ *For a while, the nLab incorrectly used "extensional type theory" to refer to what we now call [[set-level type theory]].  If you encounter uses of this sort, please correct them.*

Extensional type theory is poorly behaved metatheoretically, and very difficult to implement in a proof assistant.  However, it is sometimes more convenient to work with informally, and there are conservativity theorems relating it to other set-level type theories that are better-behaved.

Type theory which is not extensional is called _[[intensional type theory]]_.

+-- {: .num_remark}
###### Remark
The word "extensional" in type theory (even when applied to identity types) sometimes refers instead to the axiom of  [[function extensionality]].  In general this property is orthogonal to the one considered here: function extensionality can hold or fail in both extensional and intensional type theory.

In particular, [[homotopy type theory]] is [[intensional type theory|intensional]] in that [[identity types]] are crucially _not_ demanded to be [[propositions]], but [[function extensionality]] is often assumed (in terms of these intensional identity types, of course) --- in particular, it follows from the [[univalence axiom]].  Indeed, univalence itself is arguably an [[extensionality principle]] for the universe (Hofmann and Streicher originally introduced it under the name "universe extensionality"), but it is inconsistent with "extensional type theory" in the sense considered here.
=--

+-- {: .num_remark}
###### Remark
The origin of the names "extensional" and "intensional" is somewhat confusing.  In fact they refer to the behavior of the [[definitional equality]].  The idea is that the [[identity type]] is always an "extensional" notion of equality (although it can be more or less extensional, depending on whether further extensionality principles like [[function extensionality]] and [[univalence]] hold).  Thus, if the definitional equality *coincides* with the identity type, as it does under the reflection rule, the former is also extensional, and so we call the type theory "extensional" --- while if the two equalities do *not* coincide, then the definitional equality has room to be more intensional than the identity type, and so we call the type theory "intensional".
=--


## Definition

The Martin-Lof definition of [[identity types]] as an [[inductive type]] family makes them intensional.  To make the type theory extensional, we add a rule that any [[inhabitant]] of an identity type $p:Id_A(x,y)$ induces a [[definitional equality]] between $x$ and $y$.  In other words, we have an "equality reflection rule" of the form

$$ \frac{p:Id_A(x,y)}{x\equiv y} $$

At first, this may appear to be only a "[[skeleton|skeletality]]" assumption, since it does not assert explicitly that $p$ is [[reflexive relation|reflexivity]] rather than a nontrivial [[automorphism|loop]].  However, we can derive this with the induction rule for identity types.  Consider the [[dependent type]]

$$ (x:A),(y:A),(p:Id_A(x,y)) \;\vdash\; Id_{Id_A(x,y)}(p,refl(x)). $$

This is well-typed because the reflection rule applied to $p$ yields a judgmental equality $x\equiv y$, so that we have $refl(x):Id_A(x,y)$.  Moreover, [[substitution|substituting]] $x$ for $y$ and $refl(x)$ for $p$ yields the type $Id_{Id_A(x,x)}(refl(x),refl(x))$, which is inhabited by $refl(refl(x))$.

Thus, by induction on identity, we have a term in the above type, witnessing a [[typal equality]] between $p$ and $refl(x)$.  Finally, applying the equality reflection rule again, we get a definitional equality $p\equiv refl(x)$.

+-- {: .num_remark}
###### Remark
On the other hand, if in addition to the equality reflection rule we postulate that all equality proofs are definitionally equal to reflexivity, then we can derive the induction rule for identity types.  Extensional type theory is often presented in this form.
=--

A different, also equivalent, way of presenting extensional type theory is with a definitional [[eta-conversion]] rule for the identity types; see _[here](identity+type#EtaConversion)_.

### Using the interval type

If the [[dependent type theory]] has an [[interval type]] $\mathbb{I}$ with judgmental computation rules for the point constructors, it suffices for the two point constructors $0:\mathbb{I}$ and $1:\mathbb{I}$ to be definitionally equal:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0 \equiv 1:\mathbb{I}}$$ 

\begin{proof}
By the recursion principle of the interval type, for elements $x:A$, $y:A$, and $p:\mathrm{Id}_A(x, y)$, we have a function $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$ such that $\mathrm{rec}_\mathbb{I}^A(x, y, p, 0) \equiv x$ and $\mathrm{rec}_\mathbb{I}^A(x, y, p, 1) \equiv y$. If we have $0 \equiv 1:\mathbb{I}$, then by the [[congruence rules]] of [[definitional equality]] we have 
$$x \equiv \mathrm{rec}_\mathbb{I}^A(x, y, p, 0) \equiv \mathrm{rec}_\mathbb{I}^A(x, y, p, 1) \equiv y$$
which is precisely equality reflection. 
\end{proof}

Alternatively, one can add inference rules for [[definitional interval type localization|definitional $\mathbb{I}$-localization]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \mathrm{const}_{A, \mathbb{I}}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{const}_{A, \mathbb{I}}^{-1}(\lambda i:\mathbb{I}.x) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \lambda i:\mathbb{I}.\mathrm{const}_{A, \mathbb{I}}^{-1}(p) \equiv p:\mathbb{I} \to A}$$

The usual notion of [[interval type localization|$\mathbb{I}$-localization]], provable in any [[dependent type theory]] with an [[interval type]], implies definitional $\mathbb{I}$-localization in extensional type theory by [[equality reflection]]. On the other hand, one can prove equality reflection from definitional $\mathbb{I}$-localization. 

\begin{theorem}
Definitional $\mathbb{I}$-localization implies [[equality reflection]]. 
\end{theorem}

\begin{proof}
Given $x:A$, $y:A$, and $p:x =_A y$, by the [[recursion principle]] of the [[interval type]], we have a function $\mathrm{rec}_{\mathbb{I}, A}(x, y, p):\mathbb{I} \to A$. By definitional $\mathbb{I}$-localization and the recursion principle of the [[interval type]], we have an element 
$$\mathrm{const}_{A, \mathbb{I}}^{-1}(\mathrm{rec}_{\mathbb{I}, A}(x, y, p)):A$$
such that 
$$\mathrm{const}_{A, \mathbb{I}}^{-1}(\mathrm{rec}_{\mathbb{I}, A}(x, y, p)) \equiv \mathrm{const}_{A, \mathbb{I}}(\mathrm{const}_{A, \mathbb{I}}^{-1}(\mathrm{rec}_{\mathbb{I}, A}(x, y, p)), 0) \equiv \mathrm{rec}_{\mathbb{I}, A}(x, y, p, 0) \equiv x$$
$$\mathrm{const}_{A, \mathbb{I}}^{-1}(\mathrm{rec}_{\mathbb{I}, A}(x, y, p)) \equiv \mathrm{const}_{A, \mathbb{I}}(\mathrm{const}_{A, \mathbb{I}}^{-1}(\mathrm{rec}_{\mathbb{I}, A}(x, y, p)), 1) \equiv \mathrm{rec}_{\mathbb{I}, A}(x, y, p, 1) \equiv y$$
hence, we can derive by the [[inference rules]] for [[judgmental equality]] that $x \equiv y$, which is precisely equality reflection.
\end{proof}

\begin{theorem}
In the presence of the large recursion principle of the [[interval type]], [[definitional isomorphism types]] imply [[equality reflection]]. 
\end{theorem}

\begin{proof}
In the presence of definitional isomorphism types and the [[inductively defined]] [[identity types]], [[transport]] can be defined as definitional isomorphism via the [[J-rule]], since the [[identity function]] or [[identity equivalence]] is a definitional isomorphism and thus one can apply the J-rule to reflexivity to get the identity as a definitional isomorphism:

$$x:A, y:A, p:x =_A y \vdash \mathrm{ind}_{\mathrm{Id}}^{A, B(x) \cong B(y)}(p):B(x) \cong B(y)$$ 

$$x:A \vdash \mathrm{ind}_{\mathrm{Id}}^{A, B(x) \cong B(x)}(\mathrm{refl}_A(x)) \equiv \mathrm{toDefIso}(\chi:A.\chi, \chi:A.\chi):B(x) \cong B(x)$$ 

By large recursion of the interval, given two types $A$ and $B$ and an [[equivalence of types]] $e:A \simeq B$, one can construct an interval-indexed type family $(\mathrm{rec}_{\mathbb{I}}^{A, B, e}(x))_{x:\mathbb{I}}$ such that $\mathrm{rec}_{\mathbb{I}}^{A, B, e}(0) \equiv A$, $\mathrm{rec}_{\mathbb{I}}^{A, B, e}(1) \equiv B$, and $q:\mathrm{tr}_{\mathrm{rec}_{\mathbb{I}}^{A, B, e}}(p) =_{A \simeq B} e$. With definitional isomorphism types, the equivalences can be strictified to definitional isomorphisms by 
$$\mathrm{ind}_{\mathrm{Id}}^{\mathbb{I}, \mathrm{rec}_{\mathbb{I}}^{A, B, e}(0) \cong \mathrm{rec}_{\mathbb{I}}^{A, B, e}(1)}(p):A \cong B$$
This implies that for all types $A$, the equivalence 
$$\mathrm{const}_{\mathbb{I}, A} \coloneqq \lambda x:A.\lambda i:\mathbb{I}.x:A \simeq (\mathbb{I} \to A)$$
in [[interval type localization|$\mathbb{I}$-localization]] can be turned into the definitional isomorphism
$$\mathrm{ind}_{\mathrm{Id}}^{\mathbb{I}, \mathrm{rec}_{\mathbb{I}}^{A, \mathbb{I} \to A, \mathrm{const}_{\mathbb{I}, A}}(0) \cong \mathrm{rec}_{\mathbb{I}}^{A, \mathbb{I} \to A, \mathrm{const}_{\mathbb{I}, A}}(1)}(p):A \cong (\mathbb{I} \to A)$$
which is [[definitional interval type localization|definitional $\mathbb{I}$-localization]], and definitional $\mathbb{I}$-localization implies [[equality reflection]] as proven in the [[definitional interval type localization|definitional $\mathbb{I}$-localization]] and [[extensional type theory]] articles. 
\end{proof}

### Using dependent sum types of identity types

In [[extensional type theory]], there are ways of defining certain [[dependent sum types]] of [[identity type]] as a [[negative type]], which all result in equality reflection. 

The idea is that using the inference rules for dependent sum types, the standard J-rule states that the dependent sum type $\sum_{x:A} \sum_{y:A} x =_A y$ is a [[positive copy]] of $A$ with respect to the [[diagonal function]] 
$$\Delta_{A}(x) \coloneqq (x, (x, \mathrm{refl}_A(x))):\sum_{x:A} \sum_{y:A} x =_A y$$
However, there is also a negative version of [[copy types]], whose elimination, computation, and uniqueness rules state that the [[diagonal function]] is a [[definitional isomorphism]]: 

* Elimination rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_A^{-1}(z):A}$$

* Computation rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \Delta_A^{-1}(\Delta_{A}(x)) \equiv x:A}$$

* Uniqueness rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_{A}(\Delta_A^{-1}(z)) \equiv z:\sum_{x:A} \sum_{y:A} x =_A y}$$

The uniqueness rules yield [[equality reflection]]. By the properties of [[judgmental equality]] and [[dependent sum types]], from 
$$(\Delta_A^{-1}(x, y, p), \Delta_A^{-1}(x, y, p), \mathrm{refl}_A(\Delta_A^{-1}(x, y, p))) \equiv (x, y, p)$$
one can derive $x \equiv \Delta_A^{-1}(x, y, p)$ and $y \equiv \Delta_A^{-1}(x, y, p)$ and thus $x \equiv y$. 

Similarly, the Paulin-Mohring J-rule states that given $x:A$, the dependent sum type $\sum_{y:A} x =_A y$ is a [[positive unit type]] of $A$ with specified element 
$$(x, \mathrm{refl}_A(x)):\sum_{y:A} x =_A y$$
However, there are also [[negative unit types]], which states that $\sum_{y:A} x =_A y$ is a definitional singleton with [[judgmental equality|judgmental]] [[center of contraction]] $(x, \mathrm{refl}_A(x))$

* Uniqueness rules for negative identity types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, z:\sum_{y:A} x =_A y \vdash (x, \mathrm{refl}_A(x)) \equiv z:\sum_{y:A} x =_A y}$$

Similarly to the case for the standard Martin-Lof identity types, the uniqueness rule yields [[equality reflection]], because by the properties of [[judgmental equality]] and [[dependent sum types]], one can derive $x \equiv y$ from $(x, \mathrm{refl}_A(x)) \equiv (y, p)$. 

## Properties

### Decidability

Extensional [[Martin-Löf type theory]] does not have [[decidability|decidable]] type checking.  See _[[intensional type theory]]_ for more on this.

\begin{theorem}
In addition, extensional type theory does not have decidable [[judgmental equality]]. 
\end{theorem}

\begin{proof}
Already, the equality reflection rule for the [[natural numbers type]] implies undecidability of judgmental equality in the dependent type theory. 
$$\frac{\Gamma \vdash p:\mathrm{Id}_\mathbb{N}(x,y)}{\Gamma \vdash x \equiv y}$$
In order to show that, in an arbitrary [[context]] $\Gamma$, $0 \equiv 1$ in $\mathbb{N}$, we need to determine whether the empty type is a [[pointed type]] in $\Gamma$, which is undecidable in general. 
\end{proof}

## Justification

Extensional type theory is justified by the [[ meaning explanation | meaning explanations ]] of type theory. To see this, it suffices to notice that the equality reflection rule is validated by the meaning explanations. For more on this, see [Dybjer 2012](#Dybjer12), \S11.2.7 and [Bentzen 2024](#Bentzen24), \S3.2.

## Related concepts

* [[axiom K]], [[axiom UIP]]

* [[intensional type theory]], [[homotopy type theory]]

* [[observational type theory]], [[higher observational type theory]]

## Examples

* [[NuPRL]]

* [[Andromeda]]

## References

* {#Dybjer12} [[Peter Dybjer]], Program testing and the meaning explanations of intuitionistic type theory. In Dybjer, P., Lindström, S., Palmgren, E., and Sundholm,
G., editors. _Epistemology Versus Ontology_. Dordrecht: Springer, pp. 215–241. [doi:10.1007/978-94-007-4435-6_11](https://doi.org/10.1007/978-94-007-4435-6_11)

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FSCD.2019.31](https://doi.org/10.4230/LIPIcs.FSCD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

Extensional type theory is discussed in chapter 2 of:

* {#AngiuliGratzer} [[Carlo Angiuli]], [[Daniel Gratzer]], *Principles of Dependent Type Theory* ([pdf](https://www.danielgratzer.com/papers/type-theory-book.pdf))

For a philosophical defense of extensional equality in constructive semantics see:

* {#B22} [[Bruno Bentzen]]: *On different ways of being equal*, Erkenntnis **87** 4 (2022) 1809–1830 &lbrack;[doi:10.1007/s10670-020-00275-8](https://doi.org/10.1007/s10670-020-00275-8), [philarchive:BENODW](https://philarchive.org/rec/BENODW)&rbrack;


* {#B24} [[Bruno Bentzen]]: *Analyticity and syntheticity in type theory revisited*, Review of Symbolic Logic **17** 4 (2024) 1119–1145 &lbrack;[doi:10.1017/s1755020323000199](https://doi.org/10.1017/s1755020323000199), [philarchive:BENAAS-9](https://philarchive.org/rec/BENAAS-9)&rbrack;



[[!redirects extensional type theories]]
[[!redirects equality reflection]]
[[!redirects equality reflection rule]]