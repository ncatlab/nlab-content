+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

[[!redirects HTS]]

# Contents
* table of contents
{: toc}

## Idea

Proposed by [[Vladimir Voevodsky]], **Homotopy Type System (HTS)** is a type theory with two equality types, an "exact" or "strict" one which satisfies a [[reflection rule]], and a "path" or "homotopical" one which does not. It also distinguishes between "[[fibrant]]" and "non-fibrant" types: the path type only eliminates into fibrant types.

## Specification

* [[HTS.pdf:file]], [Slides](https://uf-ias-2012.wikispaces.com/file/view/HTS_slides.pdf/410105196/HTS_slides.pdf)
* [TTS](http://uf-ias-2012.wikispaces.com/file/view/TTS.pdf) is a precursor for this system. [Implementation](https://github.com/DanGrayson/checker)

## Implementation

* In progress: <https://github.com/andrejbauer/andromeda>

## Remarks and Variations

### Points that are homotopic but not strictly equal

Let $I$ be the type of pointed fibrant types that are merely equal to $Bool$, i.e.

$$I = \sum_{(A:U_F)} A. $$

Define $zero,one:I$ by

$$zero = (Bool,false)$$
$$one = (Bool,true)$$

Then we have $Paths(zero,one)$, since by univalence we have a $p:Paths(Bool,Bool)$ such that $p_*(false) = true$.

However, if $e:Id(zero,one)$, then by $apd$ for strict equality, we have $Id(q_*(false),true)$, where $q$ is the image of $e$ under the map $proj_1:I \to U_F$.  But all strict equalities are equal to reflexivity, so $Id(q_*(false),false)$, and thus $Id(false,true)$, a contradiction.

Therefore, the fibrant type $I$ contains two points $zero,one$ such that $Paths(zero,one)$, but $\neg Id(zero,one)$ (both provable inside the theory).

### The universe of non-fibrant types

The universe $U$ of non-fibrant types is itself *fibrant*.  Moreover, in standard models (such as the simplicial set model, and other model-category-theoretic models) it is *[[contractible type|contractible]]* (in the usual sense of homotopy type theory, with respect to the $Paths$ identity type).

The reason that the universe of non-fibrant types (type families) is contractible is that if you have a type $I$ with two objects $a b : I$ and an object $e : Paths_I a b$ such that for any two types $A, B$ there is a function $(A \coprod B ) \to I$ whose strict fiber over $a$ is isomorphic to $A$ and strict fiber over $b$ is isomorphic to $B$ then the family of fibers of this function gives a map from $I$ to the universe of all types which, when applied to $e$, gives an isomorphism in this universe from $A$ to $B$.
This is sufficient to create a path from a type which is isomorphic to empty to a type which is isomorphic to unit and therefore a path from 0 to 1 in nat. 

It is not *provably* contractible in the theory, since we can take its coproduct with pretty much any other type and still have a universe of non-fibrant types.  However, it is "almost" contractible by the following argument.  Let $A$ and $B$ be arbitrary types, and let $I,zero,one$ be as defined above.  Define $f:A+B \to I$ by $f(inl(a)) = zero$ and $f(inr(b)) = one$, and define $P:I\to U_S$ (the universe of non-fibrant types) by

$$P(i) = \sum_{x:A+B} Id(f(x),i). $$

In other words, $P(i)$ is the fiber of $f$ over $i$, computed using strict equality.  It's straightforward to show that $P(zero) \cong A$ and $P(one)\cong B$.  However, since $I$ and $U_S$ are both fibrant, we can apply $P$ to the path $Paths(zero,one)$ to obtain a $Paths(P(zero),P(one))$.  This is not the same as a path $Paths(A,B)$, of course.

### Fibrant replacement

It is natural to wonder whether we can have a "fibrant replacement" type former which makes non-fibrant types into fibrant ones.  However, surprisingly, this is actually inconsistent, essentially because it cannot be made to respect substitution.

Suppose we had a type forming rule

$$\frac{\Gamma \vdash A \, Type}{\Gamma \vdash R A \, Fib} $$

with introduction rule

$$\frac{\Gamma \vdash a:A}{\Gamma \vdash r a : R A} $$

and elimination rule

$$\frac{\Gamma,(x:R A) \vdash T\, Fib\qquad \Gamma,(a:A) \vdash t:T[x:=r a]}{\Gamma,(x:R A) \vdash Relim(a.t,x) : T}. $$

Let $A=0$ and $B=1$, and let $P:I\to U_S$ be defined as above, so that $P(zero) \cong 0$ and $P(one)\cong 1$.  Now consider

$$ (x:I) \vdash R(P(x))\,Fib. $$

Since this is a fibrant type family over a fibrant type, we can transport the element $r(\star) : R(P(one))$ along the known $Paths(zero,one)$ to obtain an element of $R(P(zero))$.  However, by $Relim$, we can define a map $R(P(zero))\to 0$ by defining a map $P(zero)\to 0$, which we have.  Thus, we obtain an element of $0$.

It does, however, seem to be possible to allow fibrant replacement of types in the empty context.  In other words, we could have a rule 

$$\frac{\vdash A \, Type}{\vdash R A \, Fib} $$

and so on.  Of course, this does not fit very well in the usual framework of type theory.

### Fibrancy of inductive types

[[Mike Shulman]] has argued that rather than assuming the natural numbers type to be fibrant and yet able to eliminate into non-fibrant types, there should be two natural numbers types: a fibrant one which can only eliminate into fibrant types, and a non-fibrant one which can eliminate into all types.  The same applies to other positive inductive types such as coproducts (even coproducts of fibrant types) and the empty type.

This is because while these types in simplicial sets happens to be fibrant, that is not the case in other categorical models.  It may also pose similar problems for constructing new models of HTS out of old ones.


### Semisimplicial types

[[Vladimir Voevodsky]] claims that HTS allows a definition of [[semisimplicial types]] and other infinite objects, in which diagrams of types commute strictly using the exact equality.  See the comments in the file:

* [[hts-semisimplicial.v:file]]


### Voevodsky's conjecture

Voevodsky has conjectured that any fibrant type definable in HTS is equivalent to one definable in [[Martin-Löf Type Theory|MLTT]], i.e. without using the strict equality.

### Model invariance

The [[model invariance problem]] seems more likely to fail for HTS than for theories that do not include strict equality.  In other words, distinct model categories presenting the same $(\infty,1)$-topos might have different "internal languages" according to HTS, even if we restrict to the fibrant types.  It is unclear whether or not this is true; Voevodsky's conjecture above would imply that model invariance holds if it holds for MLTT.

The following argument, however, shows that model invariance definitely fails if we include fibrant replacement (of types in the empty context), and split inductive types into fibrant and non-fibrant versions (or simply don't include inductive types in the system).

Let $E$ be the poset with four objects $a,b,c,d$ such that $d\lt a$, $d\lt b$, and $d\lt c$ are the only nonidentity relations; thus an $E$-diagram is four
objects $X_a$, $X_b$, $X_c$, $X_d$ with maps $X_d \to X_a$, $X_d \to X_b$, and $X_d \to X_c$.  Since $E$ is an [[nlab:inverse category]], there is a [[nlab:Reedy model structure]] on $sSet^E$ in which the cofibrations are levelwise monomorphisms, the weak equivalences are levelwise weak equivalences, and the fibrant objects are diagrams such that $X_a$, $X_b$, and $X_c$ are fibrant and the induced map $X_d \to (X_a \times X_b \times X_c)$ is a fibration.  Moreover, this model has [[univalent] [[universes]] induced from those of $sSet$: if $U$ is a univalent universe in $sSet$, then $V$ is a univalent universe in $sSet^E$, where $V_a = V_b = V_c = U$, and the fiber of $V_d$ over $(A,B,C)$ is the type $A \to B \to C \to U$.

Now we can [[nlab:Bousfield localization|localize]] this Reedy model structure at the maps $0\to a$, $0\to b$, and $0\to c$, where $a$, $b$, and $c$ denote the corresponding [[nlab:representable functor|representables]].  A local object is a fibrant object such that $X_a$, $X_b$, and $X_c$ are contractible, and the local weak equivalences are just the maps that induce a weak equivalence on $d$-components.  In particular, the homotopy category of the localized model structure is equivalent to that of $sSet$.  Moreover, locality and localization (of fibrant objects) can be represented internally as a subobject and an endomorphism, respectively, of the universe $V$.  Because localization is left exact, the subuniverse of local objects is itself local, and thus provides a univalent universe for the localized model structure.

In conclusion, we have two model structures, one on $sSet$ and one on
$sSet^E$, which both model homotopy type theory with univalent
universes, and have equivalent homotopy categories.  Both model HTS as well, although their inductive types come in fibrant and non-fibrant versions.

Now, inside HTS, define a (non-fibrant) type $Y$ to be a "strict [[nlab:homotopy level|hprop]]"
if $\prod_{(x,y:Y)} Id(x,y)$.  Write $sProp$ for the subtype of the universe of non-fibrant types determined by the strict hprops.  Consider the following type

$$\prod_{P,Q,R:sProp} (\neg P \to (Q \vee R)) \to ((\neg P \to Q) or (\neg P \to R)) $$

Call this type KP (for Kreisel-Putnam).  Note that "false" and "or"
for strict hprops can be defined impredicatively by quantification
over $sProp$.

For semantics of HTS in a model category whose underlying category is
a topos, the type $sProp$ will be interpreted by the [[nlab:subobject
classifier]] *of that topos* (independently of what the model structure
might look like).  Thus, KP will be interpreted by the assertion, in
the internal language of that topos (again independently of the model
structure), that the Kreisel-Putnam axiom holds.

Now as pointed out by [Francois Dorais](http://mathoverflow.net/questions/159989/internal-logic-of-the-topos-of-simplicial-sets/), the Kreisel-Putnam axiom holds in the
internal logic of (the 1-topos) $sSet$; thus the interpretation of KP
there is globally inhabited.  However, the Kreisel-Putnam axiom does
not hold in the internal logic of (the 1-topos) $sSet^E$.  For this it
suffices to exhibit subterminal objects $P,Q,R$ such that $(\neg P \to (Q
\vee R))$ is not contained in $((\neg P \to Q) \vee (\neg P \to R))$.  Let $P = a$, $Q = b$, and $R = c$.  Then $(\neg P) = (Q \vee R) = \{b,c\}$, so that $(\neg P \to (Q \vee R)) = 1 = \{a,b,c,d\}$, but $(\neg P \to Q) = \{a,b\}$ and $(\neg P \to R) = \{a,c\}$, so that $((\neg P \to Q) \vee (\neg P \to R)) = \{a,b,c\}$.  Thus, the interpretation of KP in $sSet^E$ is not globally inhabited.

It follows that $R(KP)$ is a fibrant type which is inhabited in the model in $sSet$, but not in the model in $sSet^E$.

## See also

* [[two-level type theory]]

* [[semi-simplicial types in homotopy type theory]]