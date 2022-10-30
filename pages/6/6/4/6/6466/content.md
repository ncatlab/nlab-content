
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Real numbers object
* tic
{: toc}

## Idea

Recall that it is possible to define an [[internalization]] of the set of [[natural numbers]], called a [[natural numbers object]] (NNO), in any [[cartesian monoidal category]] (a category with finite [[product|products]]). In particular, the notion makes sense in a [[topos]]. But a topos supports [[intuitionistic logic|intuitionistic]] [[higher-order logic]], so once we have an NNO, it is also possible to repeat the usual construction of the [[integer|integers]], the [[rational number|rationals]], and then finally the [[real number|real numbers]]; we thus obtain an internalization of $\mathbb{R}$ in any topos with an NNO.

More generally, we can define a real numbers object (RNO) in any category with sufficient structure (somewhere between a cartesian monoidal category and a topos).  Then we can prove that an RNO exists in any topos with an NNO (and in some other situations).


## Definition

Let $\mathcal{E}$ be a [[Heyting category]].  (This means, in particular, that every [[subobject poset]] has full [[first-order logic|first-order]] [[intuitionistic logic]].)  A (located Dedekind) __real numbers object__ in $\mathcal{E}$ is a [[ring object]] in $\mathcal{E}$ that satisfies (in the [[internal logic]]) the axioms of a [[Dedekind-complete]] [[linearly ordered]] [[Heyting field]].

In detail, a _commutative ring object_ in $\mathcal{E}$ is an object $R$ equipped with morphisms $0\colon \mathbf{1} \to R$, ${-}\colon R \to R$, ${+}\colon R \times R \to R$, $1\colon \mathbf{1} \to R$, and ${\cdot}\colon R \times R \to R$ (where $\mathbf{1}$ is the [[terminal object]] of $\mathcal{E}$ and $\times$ is the [[product]] operation) that make certain diagrams commute.  (These diagrams may be found at [[ring object]], in principle, although right now they\'re not there.)

Given a commutative ring object $R$ in $\mathcal{E}$, we define a [[binary relation]] $\#$ on $R$ (that is a [[subobject]] of $R \times R$) as
$$ \{ (x,y)\colon R \times R \;|\; \exists z\colon R.\, x \cdot z = y \cdot z + 1 \} ,$$
written in the [[internal language]] of $\mathcal{E}$.  Then $R$ is a (Heyting) _field object_ if $\#$ is a tight [[apartness relation]]; that is if the following axioms (in the internal language) hold:
*  $\forall x\colon R.\, \neg(x \# x)$,
*  $\forall x\colon R.\, \forall y\colon R.\, (x \# y \implies y \# x)$,
*  $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, (x \# z \implies (x \# y \vee y \# z))$,
*  $\forall x\colon R.\, \forall y\colon R.\, (\neg(x \# y) \implies x = y)$.

A (linearly) _ordered field object_ in $\mathcal{E}$ is a field object $R$ equipped with a binary relation $\lt$ such that the following axioms hold:
*  $\forall x\colon R.\, \forall y\colon R.\, (x \lt y \implies x \# y)$,
*  $\forall x\colon R.\, \forall y\colon R.\, (x \# y \implies (x \lt y \vee y \lt x))$,
*  $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, ((x \lt y \wedge y \lt z) \implies x \lt z)$,
*  $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, (x \lt y \implies x + z \lt y + z)$,
*  $\forall x\colon R.\, \forall y\colon R.\, \forall z\colon R.\, ((x \lt y \wedge 0 \lt z) \implies x \cdot z \lt y \cdot z)$.

Given an ordered field object $R$ in $\mathcal{E}$, any object $\Gamma$ in $\mathcal{E}$, and subobjects $L$ and $U$ of $\Gamma \times R$, we say that $(L,U)$ is a _Dedekind cut_ in $R$ parametrised by $\Gamma$ if the following axioms hold:
*  $\forall a\colon \Gamma.\, \exists x\colon R.\, (a,x) \in L$,
*  $\forall a\colon \Gamma.\, \exists x\colon R.\, (a,x) \in U$,
*  $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, ((x \lt y \wedge (a,y) \in L) \implies (a,x) \in L)$,
*  $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (((a,x) \in U \wedge x \lt y) \implies (a,y) \in U)$,
*  $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (x \lt y \implies ((a,x) \in L \vee (a,y) \in U))$,
*  $\forall a\colon \Gamma.\, \forall x\colon R.\, \forall y\colon R.\, (((a,x) \in L \wedge (a,y) \in U) \implies x \lt y)$.

An ordered field object $R$ in $\mathcal{E}$ is _Dedekind complete_ if, given any object $\Gamma$ of $\mathcal{E}$ and any Dedekind cut $(L,U)$ in $R$ parametrised by $\Gamma$, there exists a morphism $x\colon \Gamma \to R$ such that
$$ L = \{ (a,b)\colon \Gamma \times R \;|\; b \lt x(a) \} ,$$
$$ U = \{ (a,b)\colon \Gamma \times R \;|\; x(a) \lt b \} .$$

Finally, a _real numbers object_ in $\mathcal{E}$ is a Dedekind-complete ordered field object.


## Properties

In the last requirement, of Dedekind completeness, we postulate (under certain conditions) the existence of a morphism $x\colon \Gamma \to R$ satisfying certain properties.
+-- {: .un_thm}
###### Theorem
This morphism is in fact unique.
=--
+-- {: .proof}
###### Proof
...
=--

In the definition of a Heyting field object, all of the axioms except the last are [[geometric logic|geometric]] and therefore make sense in any [[geometric category]].
+-- {: .un_thm}
###### Theorem
An object satisfying all but the last axiom of a field object is precisely a [[local ring]] object (so in particular an RNO is a local ring object).
=--
+-- {: .proof}
###### Proof
...
=--

We usually speak of *[[the]]* RNO, if one exists.  This is because any two RNOs in a Heyting category are [[isomorphic]], in an essentially unique way.
+-- {: .un_thm}
###### Theorem
If $R$ and $R'$ are both RNOs in a Heyting category $\mathcal{E}$, then there is a unique isomorphism from $R$ to $R'$ that preserves the structures on them ($0$, $-$, $+$, $1$, $\cdot$, $\lt$).
=--
+-- {: .proof}
###### Proof
...
=--

Any Heyting category with an RNO must also have a [[natural numbers object]] (NNO).  Thus in a topos, or in more general categories as in the other constructions below, the existence of an RNO is equivalent to the existence of an NNO.
+-- {: .un_thm}
###### Theorem
If $R$ is an RNO in a Heyting category, then there is unique subobject $N$ of $R$ that is both a sub-[[rig]] object of $R$ and an NNO under the operations $0\colon \mathbf{1} \to N$ and ${-} + 1\colon N \to N$.
=--
+-- {: .proof}
###### Proof
...
=--


## Constructions

We can construct a real numbers object in the following cases (presumably among others):

1. in a topos with an NNO;
2. in a $\Pi$-[[Pi-pretopos|pretopos]] with an NNO and [[weak countable choice]];
3. in a $\Pi$-pretopos with an NNO and [[subset collection]].

(Actually, (1) is a special case of (3), but the usual construction in (1) is not available in (3).  Thus, we still have three different constructions to consider.)


### In a topos with an NNO

Let $\mathcal{E}$ be an [[elementary topos]] with a natural numbers object $\mathbb{N}$. The **Dedekind real numbers object** of $\mathcal{E}$ is the object of all [[Dedekind cut|Dedekind cuts]]. To be more precise, we will need to make some auxiliary definitions.

We first construct an integers object as follows. Let $a, b\colon E \to \mathbb{N} \times \mathbb{N}$ be the [[kernel pair]] of the addition map ${+}\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$, and let $\pi_1, \pi_2\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ be the [[product]] projections. We define $\mathbb{Z}$ to be the [[coequalizer]] of $(\pi_1 \circ a, \pi_2 \circ b), (\pi_2 \circ a, \pi_1 \circ b)\colon E \to \mathbb{N}$. A similar construction yields a rational numbers object $\mathbb{Q}$. 

We denote by $\mathcal{P}(A)$ the [[power object]] of $A$ in $\mathcal{E}$. A **Dedekind cut** is a [[generalized element]] $(L, U)$ of $\mathcal{P}(\mathbb{Q}) \times \mathcal{P}(\mathbb{Q})$, satisfying the following conditions, expressed in the [[Mitchell–Bénabou language]] of $\mathcal{E}$ and interpreted under [[Kripke-Joyal semantics|Kripke–Joyal semantics]]:

1. Non-degenerate:
   $$ \exists q\colon \mathbb{Q}.\, q \in L ;$$
   $$ \exists r\colon \mathbb{Q}.\, r \in U .$$

2. Inward-closed:
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, ((q \lt r \wedge r \in L) \implies q \in L) ;$$
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, ((r \lt q \wedge r \in U) \implies q \in U) .$$

3. Outward-open:
   $$ \forall q\colon \mathbb{Q}.\, (q \in L \implies \exists r\colon \mathbb{Q}.\, (r \in L \wedge q \lt r)) $$
   $$ \forall q\colon \mathbb{Q}.\, (q \in U \implies \exists r\colon \mathbb{Q}.\, (r \in L \wedge r \lt q)) .$$

4. Located:
   $$ \forall q\colon \mathbb{Q}.\, \forall r\colon \mathbb{Q}.\, (q \lt r \implies (q \in L \vee r \in U)) .$$

5. Mutually exclusive:
   $$ \forall q\colon \mathbb{Q}.\, \neg(q \in L \wedge q \in U) .$$

The relation $\lt$ on $\mathbb{Q}$ is the order relation constructed in the usual way. We define $\mathbb{R}$ to be the subobject of $\mathcal{P}(\mathbb{Q}) \times \mathcal{P}(\mathbb{Q})$ consisting of all Dedekind cuts as defined above.


### In a $\Pi$-pretopos with $WCC$

Summary: construct a [[Cauchy real numbers]] object and use $WCC$ ([[weak countable choice]]) to prove that it is an RNO.

Note that any [[Boolean topos]] with an NNO satisfies $WCC$, so in all we have three different constructions available in that case.


### In a $\Pi$-pretopos with an NNO and subset collection

Summary: modify the construction of a [[Cauchy real numbers]] object to use [[multi-valued function|multi-valued]] [[Cauchy sequences]].


## Examples

### In $Set$

The real numbers object in [[Set]] is the [[real line]], the usual set of (located Dedekind) [[real numbers]].  Note that this is a theorem of [[constructive mathematics]], as long as we assume that $Set$ is an elementary topos with an NNO.


### In sheaves on a topological space

Let $X$ be a [[topological space]], and $\mathrm{Sh}(X)$ its [[category of sheaves]]. It is well-known that $\mathrm{Sh}(X)$ is a [[Grothendieck topos]] (and so, _a fortiori_, an elementary topos), and the [[constant sheaf]] [[functor]] $\Delta\colon \mathbf{Set} \to \mathrm{Sh}(X)$ preserves [[finite limits]] and has the [[global section]] functor $\Gamma\colon \mathrm{Sh}(X) \to \mathbf{Set}$ as a [[right adjoint]]. (Hence, $\Delta$ and $\Gamma$ are the components of a [[geometric morphism]] $\mathrm{Sh}(X) \to \mathbf{Set}$.) The following claims are essentially immediate:

1. If $\mathbf{N}$ is the set of natural numbers, then $\Delta (\mathbf{N})$ must be an NNO in $\mathrm{Sh}(X)$, since $\Delta$ has a right adjoint. 

2. If $\mathbf{Z}$ is the set of integers, then $\Delta (\mathbf{Z})$ is an integers object in $\mathrm{Sh}(X)$ (as defined above), since $\Delta$ preserves finite limits and colimits.

3. Similarly, if $\mathbf{Q}$ is the set of rational numbers, then $\Delta (\mathbf{Q})$ is a rational numbers object in $\mathrm{Sh}(X)$.

Thus, for every topological space $X$, the topos $\mathrm{Sh}(X)$ has a Dedekind real numbers object $\mathbb{R}$. Na&#239;vely one might expect $\mathbb{R}$ to be isomorphic to the constant sheaf $\Delta(\mathbf{R})$, where $\mathbf{R}$ is the classical set of real numbers, but this turns out not to be the case. Instead, we have a rather more remarkable result:

+-- {: .un_theorem}
###### Theorem
A Dedekind real numbers object $\mathbb{R}$ in the topos $\mathrm{Sh}(X)$ is isomorphic to the sheaf of real-valued [[continuous functions]] on $X$.
=--

+-- {: .proof}
###### Proof
See [Mac Lane and Moerdijk](#MM94) (Chapter VI, &#167;8).
=--

This allows us to define various further constructions on $X$ in internal terms in $\mathrm{Sh}(X)$; for example, a [[vector bundle]] over $X$ is an internal [[projective object|projective]] $\mathbb{R}$-[[module]].


## Generalizations

It is also possible to define the notion of a [[Cauchy real number]] object and construct one in any $\Pi$-pretopos with an NNO, but as the internal logic in general lacks [[weak countable choice]], these are usually inequivalent.


## Related concepts

* [[natural numbers object]]

* [[Dedekind cut]]


## References

* [[Saunders Mac Lane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MM94}


[[!redirects real numbers object]]
[[!redirects real numbers objects]]
[[!redirects real number object]]
[[!redirects real number objects]]
[[!redirects real number object in a topos]]
[[!redirects real number objects in a topos]]
[[!redirects real number objects in toposes]]
[[!redirects real number objects in topoi]]
