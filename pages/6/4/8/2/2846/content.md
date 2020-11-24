
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--




# Contents
* table of contents 
{: toc}

##Idea

In [[model theory]], [[model|models]] of a [[first-order theory]] $T$ are certain kinds of [[functor|functors]] from the [[syntactic site]] of $T$ to $\mathbf{Set}$. Elementary embeddings are [[natural transformation|natural transformations]] between these functors.

## Definition

In [[model theory]], an **elementary embedding** between [[model|structures]] (over a given [[signature]] $\sigma$) is an [[injection]] that preserves and reflects all of [[first-order logic]] over $\sigma$.  That is, it is an injection $f\colon M\to N$ such that for any first-order formula $\varphi$ written in the language of $\sigma$ and parameters $a_1,\dots,a_n\in M$ (of appropriate [[type]]s), we have
$$ M \vDash \varphi(a_1,\dots,a_n) \;\iff\; N \vDash \varphi(f(a_1),\dots, f(a_n)). $$

In particular, this implies that if either $M$ or $N$ is a [[model]] of some first-order [[theory]], then so is the other.

Note that the condition that $f$ be injective is automatic as long as the logic in question includes equality, since reflecting of the formula $x=y$ implies that $f$ is injective.  If $f$ is (interpreted as) the inclusion of a [[subset]], we say that $M$ is an **elementary substructure** of $N$. We also say here that $N$ is an **elementary extension** of $M$. 

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

[[Peter Arndt]]: Regarding the statement "this square need not even commute": this suggests that the upper arrow is something that we know to define, but the issue is rather that the restriction of the given morphism to the upper left corner might not factor through the upper right corner. For example given a ring homomorphism $f: R \to S$, we don't necessarily get an induced map $\{x \in R \mid \not \exists y: xy=1\} \to \{x \in S \mid  \not \exists y: xy=1 \}$ because non-units can become units in the codomain ring. 

=-- 

In practice, it is also useful to separate out the weaker notion of **embedding**. 

+-- {: .num_defn} 
###### Definition 
Working over a fixed signature $\Sigma$, an injective homomorphism of structures $f: M \to N$ is an *embedding* if for each relation $R \in \Sigma$ of arity $n$, we have $R_M = (f^n)^\ast R_N$, i.e., $R_M$ is obtained by pulling back the inclusion $R_N \hookrightarrow N^n$ along $f^n: M^n \to N^n$. 
=-- 

Notice this is *stronger* than just being an injective homomorphism (where we demand only that $R_M \hookrightarrow (f^n)^\ast R^n$, or that $R_M(a_1, \ldots, a_n) \vdash R_N(f(a_1), \ldots, f(a_n))$), and it is weaker than being an elementary embedding since here we are not demanding a pullback condition over all the formulas of the language, just the atomic ones (including equality, which is handled by injectivity as we noted earlier). 

A *substructure* is an embedding $f: M \to N$ where $f$ is a set-theoretic inclusion. (In [[structural set theory]], a substructure would just be an isomorphism class of embeddings.) 

## Tarski-Vaught test 

A simple criterion for when one structure is an elementary substructure of another is given by the Tarski-Vaught test. Let $L$ be the language (the set of first-order formulas) over some given signature. 

+-- {: .num_prop #Tarski-Vaught} 
###### Proposition 
A substructure $i: M \hookrightarrow N$ is an elementary substructure if, whenever $\varphi$ is an $(n+1)$-ary formula and $b_1, \ldots, b_n \in M$, there exists $a \in N$ such that $\varphi(a, b_1, \ldots, b_n)$ is satisfied in $N$ only if there exists $c \in M$ such that $\varphi(c, b_1, \ldots, b_n)$ is satisfied in $M$. 
=-- 

+-- {: .proof} 
###### Proof 
By induction on the structure of formulas $\varphi$, using $\neg, \wedge, \exists$ as primitive logical operators. The required pullback condition is satisfied on atomic formulas, by definition of substructure. 

If the pullback condition is satisfied for $\varphi$ (of arity $n$ say), then it is trivially satisfied for $\neg \varphi$ because for all $\bar{a} = (a_1, \ldots, a_n) \in M^n$ we have 

$$M \models \neg \varphi(\bar{a}) \;\; iff \;\; \not [M \models \varphi(\bar{a})] \;\; iff \;\; \not [N \models \varphi(i^n(\bar{a}))] \;\; iff \;\; N \models \neg\varphi(i^n(\bar{a})).$$ 

If the pullback condition is satisfied for $\varphi$ and $\psi$, then it is equally trivially satisfied for $\varphi \wedge \psi$: 

$$\array{
M \models (\varphi \wedge \psi)(\bar{a}) & iff & M \models \varphi(\bar{a}) \; and \; M \models \psi(\bar{a}) \\ 
 & iff & N \models \varphi(i^n(\bar{a})) \; and \; N \models \psi(i^n(\bar{a})) \\ 
 & iff & N \models (\varphi \wedge \psi)(i^n(\bar{a})). 
}$$ 

Using these two steps of the induction, we may say that given a substructure, the pullback condition is satisfied for all quantifier-free formulas in the language. 

Finally, suppose the pullback condition is satisfied for $(n+1)$-ary formulas $\varphi(v, \bar{w})$. If $\bar{b} \in (\exists_v \varphi)_M$, then there exists $c \in M$ such that $(c, \bar{b}) \in \varphi_M$, whence there exists $a = i(c)$ such that $(i(c), i^n(\bar{b})) \in \varphi_N$, so $i^n(\bar{b}) \in (\exists_v \varphi)_N$, just using the fact that $i$ is a homomorphism. Conversely: if $i^n(\bar{b}) \in (\exists_v \varphi)_N$, i.e., if there exists $a \in N$ such that $(a, i^n(\bar{b})) \in \varphi_N$, then by hypothesis there exists $c \in M$ such that $(c, \bar{b}) \in \varphi_M$, i.e., $\bar{b} \in (\exists_v \varphi)_M$. This completes the inductive proof. 
=-- 

+-- {: .num_example} 
###### Example 
In the theory of [[real closed fields]] with signature $(0, 1, +, \cdot, \leq)$, the field of real algebraic numbers is an elementary substructure of the field of real numbers. This follows from the Tarski-Vaught test and the [[Tarski-Seidenberg theorem]] which establishes quantifier elimination over the language generated by the signature (every formula has the same extension as some quantifier-free formula). 
=-- 

Another application is described at [[Löwenheim-Skolem theorem]]. 

## Properties

+-- {: .num_prop #Elementary embeddings are natural transformations}
###### Proposition

Let $T$ be a [[first-order theory]], and $M, N : \mathsf{Syn}(T) \to \mathbf{Set}$ two [[models]] of $T$.

Let $(\mathsf{Syn}(T))_0$ denote the objects (definable sets of $T$) of $\mathsf{Syn}(T)$.

A $(\mathsf{Syn}(T))_0$-indexed collection of maps $f \overset{df}{=} \left(M(X) \overset{f_X}{\to} N(X) \right)_X$ is a [[natural transformation]] if and only if it preserves and reflects [[first-order logic]].

=--

+-- {: .proof}
###### Proof

Suppose $f$ is a natural transformation. Then certainly whenever $X$ is a definable set, $x \in M(X) \implies f(x) \in N(X).$

If $f(x) \in N(X)$ but $x$ is _not_ in $M(X)$, then $x \in M(\neg X)$, which implies $f(x) \in N(\neg X)$. Since the functor $N$ preserves disjoint unions, $N(\neg X) \cap N(X)$ is empty, which is impossible. So whenever $f(x) \in N(X)$, $x \in M(X)$.

Now suppose $f$ preserves and reflects first-order logic. If $X \overset{\gamma}{\to} Y$ is a map in $\mathsf{Syn}(T)$ and $y \in M(Y)$, then

$$
M \models \gamma(y) \in M(X) \iff N \models \gamma(f(y)) \in N(X)
$$

and $\gamma(f(y)) = f(\gamma(y))$ since

$$
M \models \Gamma(y,\gamma(y)) \iff N \models \Gamma(f(y), f \gamma(y))
$$

where $\Gamma$ is the graph of the definable function $\gamma$.
=--

+-- {: .num_remark}
###### Remark

In the above, we can actually weaken the assumption that we start with a collection of $(\mathsf{Syn}(T))_0$-indexed maps to just starting with a collection of maps $f_C : M(C) \to N(C)$, where $C$ runs along the maximal objects (the [[types]]) in $\mathsf{Syn}(T)$.

Then: the $(\mathsf{Syn}(T))_0$-indexed collection of _pullbacks_ along the canonical embeddings $N(X) \hookrightarrow N(C)$ is a natural transformation $M \to N$ if and only if the maps $f_C$ preserved and reflected first-order logic.

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
[[!redirects elementary extension]]
