+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **star-polycategory** is to a [[star-autonomous category]] what a [[multicategory]] is to a [[monoidal category]]. It is a [[polycategory]] in which 
every object has a dual. As such it is a model of classical linear logic with no connectives except negation.

## Definition

There are a number of candidate definitions, depending on what we make strict.

### Definition in terms of duals

Let $A$ be an object in a symmetric polycategory. A _dual_ for $A$ comprises an object $A^*$ together with a morphism $Hom(A,A^*;-)$ making the induced composition $Hom(\Gamma;A,\Delta)\to Hom(\Gamma,A^*;\Delta)$ a bijection for all $\Gamma$ and $\Delta$. 

A symmetric _star-polycategory_ is a symmetric polycategory in which every object has a dual. 

### Strict involution

In any star-polycategory there is an isomorphism $A^{**}\cong A$ for all $A$. We could also require equality, $A^{**}=A$. This holds in many concrete examples, and it holds in syntactic examples that are based on negation-normal-form. The following definition is used in ([Hyland, Sec 5.3](#Hyland)):

* A collection of objects, together with an involution operation $(-)^*$ (so $A^{**}=A$).
* For lists $\Gamma$, $\Delta$ of objects, a set $Hom(\Gamma;\Delta)$.
* _Exchange and negation structure:_ Two lists $\Gamma$ and $\Delta$ induce a single list $\Gamma^*,\Delta$ by concatenating $\Gamma^*$ with $\Delta$. Each object-preserving-bijection $\Gamma^*,\Delta\to\Pi^*,\Sigma$ should induce a function $Hom(\Gamma;\Delta)\to \Hom(\Pi;\Sigma)$, compatible with composition of bijections.
* For each object $A$, an identity morphism $Hom(A;A)$.
* For lists $\Gamma,\Delta,\Pi,\Sigma$ and objects $A$, a composition function
$$Hom(\Gamma;A,\Delta)\times Hom(\Pi,A;\Sigma)\to Hom(\Gamma,\Pi;\Delta,\Sigma)$$
respecting the exchange and negation structure, and satisfying the same identity and associativity laws as for an ordinary polycategory.

In the last axiom, "respecting the exchange and negation structure" has two pieces.  The first, more obvious, one is that the composition functions are natural with respect to object-preserving bijections $\Gamma_1^*,\Delta_1 \to \Gamma_2^*,\Delta_2$ and $\Pi_1^*,\Sigma_1 \to \Pi_2^*,\Sigma_2$ which leave the $A$'s untouched.  The second, perhaps less obvious, one is that composing along $A$ is the same as composing along $A^*$, in that the following diagram commutes:

$$
\array{
Hom(\Gamma;A,\Delta) \times Hom(\Pi,A;\Sigma) &\xrightarrow{\circ_A} & Hom(\Gamma,\Pi;\Delta,\Sigma) \\
\downarrow && \downarrow \\
Hom(\Gamma,A^*;\Delta) \times Hom(\Pi;A^*,\Sigma) && \downarrow \\
\downarrow && \downarrow \\
Hom(\Pi;A^*,\Sigma) \times Hom(\Gamma,A^*;\Delta) & \xrightarrow{\circ_{A^*}} & Hom(\Pi,\Gamma;\Sigma,\Delta)
}
$$

Note that because of symmetry, we can get away with requiring composition only when $A$ is the first object in $A,\Delta$ and the last object in $\Pi,A$.  If we included composition operations along an object $A$ with arbitrary placement in these lists, then there would be an axiom asserting that these compositions are invariant with respect to permutations that rearrange the location of $A$, hence essentially reducing them to the special case of a fixed placement (such as "first in $A,\Delta$ and last in $\Pi,A$").

### Entries only 

In a star-polycategory we have natural bijections $Hom(\Gamma;\Delta)\cong Hom(-;\Gamma^*,\Delta)\cong Hom(\Gamma,\Delta^*;-)$. In many concrete examples these bijections are equalities. Moreover, it could be argued that in many concrete examples the explicit direction of morphisms in a two-sided polycategory isn't meaningful. This leads us to the following one-sided or entries only definition. It corresponds to one-sided presentation of sequent calculus. 

* A collection of objects, together with an involution $(-)^*$ (so $A^{**}=A$).
* For any list $\Gamma$ of objects, a set $Hom(\Gamma)$ of "morphisms".
* Each object-preserving-bijection $\Gamma\to \Delta$ should induce a function $Hom(\Gamma)\to \Hom(\Delta)$, compatible with composition of bijections.
* For each object $A$, an identity morphism $Hom(A,A^*)$.
* For lists $\Gamma,\Delta$ and objects $A$, a composition function
$$Hom(\Gamma,A)\times Hom(A^*,\Delta)\to Hom(\Gamma,\Delta)$$
respecting the exchange structure and satisfying identity and associativity laws.

## Examples

* Recall that a [[linearly distributive category]] can be understood as a representable polycategory. It is star-autonomous if the corresponding polycategory is a star-polycategory. 

* For example, [[profunctors]] form a (weak) star-polycategory. The objects are categories, $A^*=A^{\mathrm{op}}$, and (using the entries-only definition) $Hom(A_1,\dots,A_n)=Cat(A_1\dots\times\dots A_n,\mathbf{Set})$. The hom-functors are identities, and composition is given by [[coends]]. 

* The unit interval forms a thin star polycategory. The objects are real numbers in the interval $[0,1]$, and the involution is $A^*=(1-A)$. $Hom(A_1,\dots A_n)$ is inhabited if $\sum_{i=1}^n A_i = 1$, i.e. if the list partitions the interval. Note that this polycategory is not representable, for example, we cannot combine $1$ with anything except $0$. 

* More generally, any [[effect algebra]] forms a thin star-polycategory in the same way. Sequences $\Gamma$ for which $Hom(\Gamma)$ is inhabited are usually called "tests". The tensor in the polycategorical sense is the partial monoid in the effect algebra sense. 

## References

* [[Martin Hyland]], _Proof theory in the abstract_ ([pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2002/pta02.pdf))
 {#Hyland}

[[!redirects star-polycategories]]
[[!redirects *-polycategories]]
[[!redirects *-polycategory]]