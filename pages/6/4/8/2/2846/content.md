
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--



# Contents
* automatic table of contents goes here
{: toc}

## Definition

In [[model theory]], an **elementary embedding** between [[model|structures]] is an [[injection]] that preserves and reflects all of [[first-order logic]].  That is, it is an injection $f\colon M\to N$ such that for any first-order formula $\varphi$ and parameters $a_1,\dots,a_n\in M$ (of appropriate [[type]]s), we have
$$ M \vDash \varphi(a_1,\dots,a_n) \;\iff\; N \vDash \varphi(f(a_1),\dots, f(a_n)). $$
In particular, this implies that if either $M$ or $N$ is a [[model]] of some first-order [[theory]], then so is the other.

Note that the condition that $f$ be injective is automatic as long as the logic in question includes equality, since reflecting of the formula $x=y$ implies that $f$ is injective.  If $f$ is (interpreted as) the inclusion of a [[subset]], we say that $M$ is an **elementary substructure** of $N$.

More generally, when we consider structures in a [[category]] as in [[categorical logic]], a morphism $f\colon M\to N$ between structures in $C$ is an **elementary embedding** if for any formula $\varphi$, the following square is a [[pullback]]:

$$
 \array{[\varphi]_M & \overset{}{\to} & [\varphi]_N\\
  \downarrow && \downarrow\\
  M A_1 \times\dots \times M A_n & \underset{}{\to} & N A_1 \times \dots \times N A_n}
$$

where $M A_i$ denotes the object of $C$ interpreting the type $A_i$, and $[\varphi]_M$ denotes the corresponding subobject in $C$ interpreting the truth value of the formula $\varphi$.  Note that for an arbitrary morphism of structures, this square need not even commute; one sometimes says that $f$ is an **elementary morphism** if it does.

+-- {: .query}

[[Urs Schreiber]]: let me try to say this more explicitly, to check if I am following:

The [[theory]] $T$ that we are modelling is exhibited by its syntactic category $Syn(T)$ with finite limits. A model of $T$ in a category $C$ with limits -- equivalently a $T$-structure in $C$ -- is a finite-limit preserving functor $N : Syn(T) \to C$. A morphism $f : M \to N : Syn(T) \to C$ of models is a [[natural transformation]] between such functors. We say that such a natural transformation is an _elementary embedding_ if its naturality squares on certain morphisms of $Syn(T)$ are pullback squares.

[[Mike Shulman]]: Not quite.  First of all, the definition officially happens at the more general level of structures rather than models, but we can of course consider those as models for the empty theory.  And whether we need finite-limit categories and functors, or something else like regular ones, geometric ones, or Heyting ones, depends on what fragment of logic we consider our (possibly empty) theories as living in.  Your rephrasing is correct if we mean finitary first-order theories and therefore [[Heyting categories]] and Heyting functors.  Otherwise, the syntactic category $Syn(T)$ won't have the structure required to construct $[\varphi]$, and the structure wouldn't be preserved by the functors into $C$, so that we wouldn't even have naturality squares to ask to commute (I alluded to this in the last sentence above).

I think I didn't explain this very well, but I have to go now, I'll try to come back to it later and rewrite it to make more sense.

=--

## Elementary embeddings between models of set theory

### In material set theory

Elementary embeddings play an important role in the study of [[large cardinals]] in (material) [[set theory]].

For instance, the existence of a [[measurable cardinal]] is equivalent to the existence of a non-[[surjection|surjective]] elementary embedding $j\colon V\to M$, where $V$ is the universe of sets and $M$ is some [[transitive set|transitive]] model of [[ZF]].  If $\kappa$ is a measurable cardinal with a countably-complete [[ultrafilter]] $\mathcal{U}$, we can form the [[ultrapower]] $V^{\mathcal{U}}$ and then take its [[transitive collapse]] to produce $M$.  (Countable completeness of $\mathcal{U}$ is necessary for $V^{\mathcal{U}}$ to be well-founded and thus have a transitive collapse.)

Conversely, if $j\colon V\to M$ is a nontrivial elementary embedding, it must have a *critical point*, i.e. a least ordinal $\kappa$ such that $j(\kappa)\neq \kappa$.  It follows that $j(\kappa)$ is some [[ordinal]] $\gt \kappa$, so in particular $\kappa\in j(\kappa)$ (using the von Neumann definition of ordinals).  Define $\mathcal{U}\subset P(\kappa)$ by $A\in \mathcal{U}$ iff $\kappa\in j(A)$; then $\mathcal{U}$ is a $\kappa$-complete ultrafilter on $\kappa$.

Stronger large cardinal axioms can be characterized, or defined, as the critical points of elementary embeddings satisfying additional closure axioms on the transitive class $M$.


### In structural set theory

Any elementary embedding of models of ZF induces a [[conservative functor|conservative]] [[logical functor]] between their categories of sets.  In fact, it is much more than that; a conservative logical functor preserves and reflects only first-order logic with [[bounded quantifiers]], while an e.e. preserves and reflects all first-order logic.

The structural meaning of elementary embeddings seems not to be well-explored.


### Inconsistency

The "ultimate" closure property, hence the "strongest" large cardinal axiom, would be having a nontrivial elementary embedding $j\colon V\to V$ (i.e. $M$ is all of $V$).  Sometimes the critical point of such an embedding, if one exists, is called a *Reinhardt cardinal*.  However, having such an e.e. turns out to be inconsistent...sort of.

The technicality is that because any e.e. $V\to V$ is a [[proper class]], the proposition "there does not exist an e.e. $V\to V$" cannot be stated in ZF (one cannot quantify over proper classes).  What we can prove is the following meta-theorem (one instance per formula $\varphi(x,y)$ that might define an e.e.).

+-- {: .un_theorem}
###### Meta-Theorem
For any formula $\varphi(x,y,z)$ and any set $a$, it is not true that defining $j_a(x)=y \iff \varphi(x,y,a)$ makes $j_a$ into an elementary embedding $V\to V$.
=--
+-- {: .proof}
###### Proof
Suppose that $\varphi$ and $a$ exist.  Fix such a $\varphi$.  Fix $\lambda$ as the smallest ordinal such that there exists an $a\in V_\lambda$ such that $\varphi(-,-,a)$ defines an e.e. $V\to V$.  Now the statement "$\lambda$ is the smallest ordinal such that there exists an $a\in V_\lambda$ such that $\varphi(-,-,a)$ defines an e.e. $V\to V$." is definable in the language of ZF (definability of the property "is an e.e. $V\to V$" is tricky, but true).  Therefore, if $b$ is any set such that $j_b$ is an e.e., it preserves the truth of this, so it is also true that $j_b(\lambda)$ is the smallest ordinal such that there exists an $a\in V_{j_b(\lambda)}$ such that $\varphi(-,-,a)$ defines an e.e. $V\to V$.  This clearly implies that $j_b(\lambda)=\lambda$.

Now define $\kappa$ to be the smallest ordinal which is a critical point of an e.e. $V\to V$ of the form $j_a$ for some $a\in V_\lambda$.  Let $b\in V_\lambda$ be such that $j_b$ is an e.e. $V\to V$ and $\kappa$ is the critical point of $j_b$.  The definition of $\kappa$ is again a definable property, so it follows that $j_b(\kappa)$ is the smallest ordinal which is a critical point of an e.e. $V\to V$ of the form $j_a$ for some $a\in V_{j_b(\lambda)} = V_\lambda$.  Therefore, $\kappa= j_b(\kappa)$, a contradiction to $\kappa$ being the critical point of $j_b$.
=--

Now, if we work instead in a theory such as [[NBG]] or [[MK]] which can contain *non-definable* proper classes, in theory there might still be an e.e. $V\to V$ which is not definable.  One can also access such an idea by adding a new symbol "$j$" to ZF and asserting that it is an e.e.  However, it was shown by Kunen in 1971, using a technical combinatorial argument, that the existence of such an e.e. is inconsistent with the [[axiom of choice]].  It is unknown whether it is consistent with [[ZF]].

[[!redirects elementary substructure]]
[[!redirects elementary submodel]]
[[!redirects elementary morphism]]
[[!redirects elementary embeddings]]
[[!redirects elementary substructures]]
[[!redirects elementary submodels]]
[[!redirects elementary morphisms]]
