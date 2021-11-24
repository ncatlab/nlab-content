
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Contents
* toc
{: toc}

## Idea

The notion of *geometric theory* has many different incarnations.  A few are:

* A geometric theory is a (possibly infinitary) [[first-order logic|first order]] [[theory]] whose [[model]]s are preserved and reflected by [[geometric morphisms]].

* A geometric theory is a (possibly infinitary) [[first-order logic|first order]] [[theory]] whose axioms can be written as [[sequent|sequents]] in context of formulae constructed from the [[logical connective|connectives]] $\top$ ([[truth]]), $\wedge$ (finite [[logical conjunction|conjunction]]), $\bot$ ([[falsity]]), $\bigvee$ (possibly infinitary [[disjunction]]), and $\exists$ ([[existential quantification]]),
as well as $=$ ([[equality]]).

* A geometric theory is a [[syntax|syntactic]] description of a [[Grothendieck topos]].

The equivalence of these statements involves some serious proofs, including [[Giraud's theorem]] characterizing Grothendieck topoi.


## Logical definition

In logical terms, a geometric theory fits into a hierarchy of theories that can be interpreted in the [[internal logic]] of a hierarchy of types of [[categories]].  Since [[predicates]] in the internal logic are represented by [[subobjects]], in order to interpret any connective or quantifier in the internal logic, one needs a corresponding operation on subobjects to exist in the category in question, and be well-behaved.  For instance:

* Since $\wedge$ and $\top$ are represented by [[intersections]] and identities (top elements), and $=$ is represented by equalizer, these can be interpreted in any [[lex category]].  Theories involving only these are examples of [[cartesian theory|cartesian theories]].

* Since $\exists$ is represented by the [[image]] of a subobject, it can be interpreted in any [[regular category]].  Theories involving only $\wedge$, $\top$, and $\exists$ are [[regular theory|regular theories]].

* Since $\vee$ and $\bot$ are represented by [[union]] and [[bottom elements]], these can be interpreted in any [[coherent category]].  Theories which add these to regular logic are called [[coherent theory|coherent theories]].

* Finally, theories which also involve infinitary $\bigvee$, which is again represented by an infinitary union, can be interpreted in [[infinitary coherent categories]], aka *[[geometric categories]]*.  These are **geometric theories**.

Note that the axioms of one of these theories are actually of the form
$$ \varphi \vdash_{\vec{x}} \psi $$
where $\varphi$ and $\psi$ are formulas involving only the specified connectives and quantifiers, $\vdash$ means entailment, and $\vec{x}$ is a [[context]].  Such an axiom can also be written as
$$ \forall \vec{x}. (\varphi \Rightarrow \psi) $$
so that although $\Rightarrow$ and $\forall$ are not strictly part of any of the above logics, they can be applied "once at top level."  In an axiom of this form for geometric logic, the formulas $\varphi$ and $\psi$ which must be built out of $\top$, $\wedge$, $\bot$, $\bigvee$, and $\exists$ are sometimes called *positive* or *geometric* formulas.

The interpretation of arbitrary uses of $\Rightarrow$ and $\forall$ requires a [[Heyting category]].  In fact, by the [[adjoint functor theorem]] for [[posets]], any geometric category which is [[well-powered category|well-powered]] is automatically a Heyting category, but *geometric functors* are not necessarily Heyting functors.  Likewise, a well-powered geometric category automatically has arbitrary intersections of subobjects as well, so we can interpret infinitary $\bigwedge$ in its internal logic, but again these are not preserved by geometric functors.

By the usual syntactic constructions (see [[internal logic]] and [[context]]), any geometric theory $T$ generates a "free geometric category containing a model of that theory," also known as its *[[syntactic category]]* $G_T$.  This syntactic category $G_T$ has the universal property that for any other geometric category $G'$, geometric functors $G_T \to G'$ are equivalent to $T$-models in $G'$.


## Examples

* Let $\Sigma$ be a signature, then the set of all geometric sequents over $\Sigma$ as well as the empty set are geometric theories called the _inconsistent theory_ $\mathbb{T}^\Sigma_0$ resp. the _empty theory_ $\mathbb{T}^\Sigma_1$ over $\Sigma$. The former admits a more concise axiomatisation as $\{\top\vdash\bot\}$. The most basic examples occur when the signature is empty: $\mathbb{T}^\emptyset_0$ is classified by the initial topos $\mathbf{1}$ and $\mathbb{T}^\emptyset _1$ is classified by the terminal topos $Set$ (see at [[classifying topos]] for details).

* The empty signature occurring in the preceding example is an extreme case of a _propositional signature_ i.e. one lacking sort symbols. These can at most contain 0-ary relation symbols since function symbols and higher order relation symbols require sorts. Whence theories over such signatures can at most contain sequents in the empty context between formulas consisting of quantifier-free nestings of 0-ary relation symbols and $\wedge,\bigvee$ and are therefor called _propositional theories_ - in other words: geometric logic boils down to [[propositional logic]]. Propositional theories are classified by [[localic topos|localic toposes]] (see there for further information).

* Any finitary [[algebraic theory]] is, in particular, a cartesian theory, and hence geometric.  This includes [[monoids]], [[groups]], [[abelian groups]], [[rings]], [[commutative rings]], etc.

* The [[theory of categories|theory $\mathbb{K}$ of categories]] with models the
 ([[strict category|strict]]) [[categories]] is not finitary-algebraic, but it is cartesian, and hence geometric; this generalises to (finitary) [[essentially algebraic theory|essentially algebraic theories]].

* The theory of [[torsion]]-free abelian groups is also cartesian, being obtained from the theory of abelian groups by the addition of the sequents $(n\cdot x = 0) \vdash_{x} (x = 0)$ for all $n\in \mathbb{N}$.

* The theory of [[local rings]] is a coherent theory, being obtained from the theory of commutative rings by adding the sequent $ (0 = 1) \vdash \bot $, for nontriviality, and
  $$\exists z. ((x+y)z = 1) \vdash_{x y} (\exists z.(x z = 1) \vee \exists z.(y z = 1))$$
  saying that if $x+y$ is invertible, then either $x$ or $y$ is so.

* The theory of [[fields]] is also coherent, being obtained from the theory of commutative rings by adding $ (0 = 1) \vdash \bot $ and also 
  $$ \top \vdash_{x} (x=0) \vee (\exists y.(x y = 1)) $$
  asserting that every element is either zero or invertible.  In the [[constructive logic]] that holds internal to the categories in question, this is the notion of a "discrete field;" other classically equivalent axiomatizations (called "Heyting fields" or "residue fields" -- see [[field]]) are not coherent.

* The theory of [[torsion]] abelian groups is geometric but not coherent; it can be obtained from the theory of abelian groups by adding the sequent
  $$ \top \vdash_{x} \bigvee_{n\ge 1} (n \cdot x = 0) $$
  asserting that for each $x$, either $x=0$ or $x+x=0$ or $x+x+x=0$ or ....  Similarly, the theory of fields of finite [[characteristic]] is geometric but not coherent.

* The _theory of the standard successor algebra_ is geometric. Its signature has one sort symbol $N$, one function symbol $s:N\to N$ and one constant $0:N$. The theory axiomaticizes [[natural number object|natural number objects]] by taking advantage of the availability of infinitary disjunctions in geometric logic in order to assert in the third axiom that every natural number is _standard_ i.e. either 0 or obtained from 0 by (repeated) application of the successor function:

  - $0 = s(n) \vdash_{n} \bot$
  - $s(n) = s(n') \vdash_{n n'} n=n'$
  - $\top \vdash_{n} \bigvee_{i} n=\underset{i}{\underbrace{s \dots s}}(0)$

  The [[classifying topos]] is $Set$. But due to the trivial subtopos lattice, theories classified by Set admit no consistent quotient theories; thus the *geometric* theory of natural numbers is [[complete theory|complete]]!  Furthermore, since $Set$ is the terminal topos, classifying also the [[empty theory]], one sees that the object/type $\mathbb{N}$ of natural numbers "comes for free" in geometric logic. This observation underlies the ideas for a [[geometric type theory]] (for more on this see there or the [article by Vickers](#Vickers09)).

* The theory of a [[real number]] is geometric.  This is a [[propositional logic|propositional]] theory, having no sorts, and having one relation symbol "$p\lt x\lt q$" for each pair of rational numbers $p\lt q$.  Its axioms are:
  - $(p_1\lt x\lt q_1) \wedge (p_2\lt x\lt q_2) \vdash (\max(p_1,p_2) \lt x \lt \min(q_1,q_2))$ (if $\max(p_1,p_2)\lt \min(q_1,q_2)$), and $(p_1\lt x\lt q_1) \wedge (p_2\lt x\lt q_2) \vdash \bot$ (otherwise).
  - $(p\lt x\lt q) \vdash (p\lt x\lt q') \vee (p' \lt x\lt q)$ (if $p\lt p' \lt q' \lt q$).
  - $(p\lt x\lt q) \vdash \bigvee_{p\lt p'\lt q'\lt q} (p' \lt x\lt q')$.
  - $\top \vdash \bigvee_{p\lt q} (p\lt x\lt q)$.

  The [[classifying topos]] of this theory is the topos of [[sheaves]] on the [[real numbers]].

* The theory of flat diagrams[^flat] over a small category $\mathcal{C}$ is geometric. For each object $i$ of $\mathcal{C}$ there is a sort $\sigma_i$, and for each morphism $u\colon i \to j$ a function symbol $\alpha_u\colon \sigma_i \to \sigma_j$. The axioms are -

  - $\top \vdash_{x\colon\sigma_i} \alpha_{Id_i}(x) = x$

  - $\top \vdash_{x\colon\sigma_i} \alpha_{v}(\alpha_u(x)) = \alpha_{v u}(x)$ ($u\colon i \to j$ and $v\colon j \to k$)

  - $\top \vdash \bigvee_{i \in \mathcal{C}_0} (\exists x\colon \sigma_i) \top$

  - $\top \vdash_{x\colon\sigma_i, y\colon\sigma_j} \bigvee_{u\colon k\to i, v\colon k\to j} (\exists z\colon\sigma_k) (x = \alpha_u(z) \wedge y = \alpha_v(z))$

  - $\alpha_u(x) = \alpha_v(x) \vdash_{x\colon\sigma_i} \bigvee_{w\colon k\to i, u w = v w} (\exists z\colon \sigma_k) x = \alpha_w(z)$ ($u,v\colon i \to j$)

  This theory is classified by the topos of presheaves over $\mathcal{C}$.

  It is commonly more useful to consider the theory of flat _presheaves_ over $\mathcal{C}$, in other words the flat diagrams over $\mathcal{C}^{op}$. ([[Elephant]] calls these _torsors_ over $\mathcal{C}$, generalizing the established terminology for groups.) This is because the representable presheaves are flat, and so Yoneda's lemma transforms objects of $\mathcal{C}$ covariantly into models of the theory. In fact, the models of the theory are the filtered colimits of representables. For example, a finitary algebraic theory is classified by the topos of covariant functors from the category of finitely presented algebras to $Set$.

[^flat]: This is also sometimes called the theory of flat functors on $\mathcal{C}$.

* If $(\mathcal{C},J)$ is a small site, by adding a geometric axiom schema to express J-continuity to the theory of flat diagrams, one obtains the [[theory of flat functors|theory of J-continuous flat diagrams]], which is classified by $Sh(\mathcal{C},J)$. This answers in principle the question, given a site representation what geometric theory is classified by a Grothendieck topos? Of course, in practice one would like to have more concise and less unwieldy axiomatizations.

* For any [[geometric theory]] $\mathbb{T}$ there exists a geometric theory $\mathbb{T}^\mathbf{2}$ called the [[theory of model homomorphisms|theory of $\mathbb{T}$-model homomorphisms]] whose models in a [[Grothendieck topos]] $\mathcal{E}$ are precisely the homomorphisms between $\mathbb{T}$-models in $\mathcal{E}$:
  $$Mod_{\mathbb{T}^\mathbf{2}}(\mathcal{E})=Mod_{\mathbb{T}}(\mathcal{E})^\mathbf{2}=Mod_\mathbb{T}(\mathcal{E}^\mathbf{2})\quad.$$

* A geometric theory whose [[classifying topos]] is a [[presheaf topos]] is called a _[[theory of presheaf type]]_.


## Other characterizations

### In terms of sheaf topoi {#InTermsOfSheafTopoi}

Categories of each "logical" type can also be "completed" with respect to a suitable "exactness" property, without changing their internal logic.  Any regular category has an completion into an [[exact category]] (see [[regular and exact completion]]), any coherent category has a completion into a [[pretopos]], and any geometric category has a completion into an [[infinitary pretopos]].

However, [[Giraud's theorem]] says that an infinitary pretopos having a [[generating set]] is precisely a [[Grothendieck topos]].  Moreover, a functor between Grothendieck topoi is geometric (preserves all the structure of a geometric category) iff it preserves finite [[limits]] and small [[colimits]].  By the [[adjoint functor theorem]], this implies that it is the [[inverse image]] part of a [[geometric morphism]], i.e. an [[adjunction]] $f^* \dashv f_*$ in which $f^*$ (the "inverse image") preserves finite limits.

Thus:

+-- {: .standout}

Grothendieck topoi and inverse-image functors are in some sense the "natural home" for models of geometric theories.  

=-- 

Note, though, that geometric morphisms are generally considered as pointing in the direction of the *direct* image $f_*$, which is the opposite direction to the geometric functor $f^*$.  (This is because when $E$ and $F$ are the toposes of [[sheaves]] on [[sober space|sober topological spaces]] (or [[locales]]) $X$ and $Y$ respectively, then [[continuous maps]] $X \to Y$ correspond precisely to geometric morphisms $E \to F$.)  Also, of course any Grothendieck topos is an [[elementary topos]] (at least, as long as one works in [[foundations]] for which [[Set]] is an elementary topos), and hence its internal logic also includes "higher-order" constructions such as function-objects and power-objects.  However, these are not preserved by geometric functors, so they (like $\forall$ and $\Rightarrow$) are not part of geometric logic.  (They are, however, preserved by [[logical functors]], a different sort of morphism between topoi.)

In particular, we can apply the "exact completion" operation to the syntactic category $G_T$ of a geometric theory to obtain an infinitary pretopos $Set[T]$.  As long as the theory $T$ was itself small, $Set[T]$ will have a generating set, and therefore will be a Grothendieck topos.  The universal property of the syntactic category, combined with that of the exact completion, implies that for any Grothendieck topos $E$, geometric morphisms $E\to Set[T]$ are equivalent to $T$-models in $E$.  This topos $Set[T]$ is called the **[[classifying topos]]** of $T$.

In the other direction, if $C$ is any small [[site]], we can write down a "geometric theory of cover-preserving [[flat functors]] $C^{op}\to Set$."  By [[Diaconescu's theorem]] classifying geometric morphisms into sheaf topoi, it follows that $Sh(C)$ is a [[classifying topos]] for this theory.  Therefore, not only does every geometric theory have a [[classifying topos]], every Grothendieck topos is the [[classifying topos]] of _some_ theory.  Very different-looking theories can have equivalent classifying topoi; this of course implies that they have all the same models in all Grothendieck topoi (hence a Grothendieck topos is the "extensional essence" of a geometric theory).  We say that two geometric theories with equivalent classifying topoi are [[Morita equivalence|Morita equivalent]].


### Functorial definition {#FunctorialDefinition}

We can approach the same idea by starting instead from the notions of [[Grothendieck topos]] and [[geometric morphism]].  The following approach is described in B4.2 of the [[Elephant]].

Suppose we consider what sorts of "theories" we can define in terms of Grothendieck topoi, that are preserved by inverse image functors.  Any such theory should certainly define a [[2-functor]] $T\colon GrTop^{op}\to Cat$, where $GrTop$ is the 2-category of Grothendieck topoi and geometric morphisms, so for the moment let's call any such $T$ a "theory".  The image $T(E)$ of a functor $E$ is supposed to be "the category of $T$-models," and a *classifying topos* for such a 2-functor will be just a [[representing object]] for it.

Of course, this notion of theory is far too general; we only want to consider theories that are constructed in some reasonable way.  One theory that should certainly be geometric is the [[theory of objects]], $O$.  This 2-functor sends a topos $E$ to itself, considered as a mere category, and an inverse image functor to itself, considered as a mere functor.  The theory $O$ can be shown to have a classifying topos, the [[classifying topos for the theory of objects|object classifier]] $Set[O]$.  Similarly, we have a theory $O_n$ of $n$-tuples of objects that should be geometric.

How can we construct more theories that ought to be geometric?  We should start from some finite collection of objects (i.e. a model of $O_n$), "construct some new objects and morphisms," and then "impose some axioms on them."  For any theory $T$, let's call a transformation $T\to O$ a *geometric construct*.  This is supposed to be "an object constructed out of the axioms of $T$ in a natural way."  More precisely, to every $T$-model in a topos $E$ it assigns an object of $E$, in a way that varies naturally with morphisms of $T$-models and inverse image functors.

Now define a *simple functional extension* of $T$ to be the [[inserter]] of a pair of geometric constructs $T\;\rightrightarrows\; O$.  A model of such a theory will consist of a model of $T$, together with an additional morphism between two objects constructed out of the given $T$-model.  By iteratively applying such constructions, we can add in any number of new morphisms between "constructed objects."

Finally, define a *simple geometric quotient* of $T$ to be the [[inverter]] of a [[modification]] between a pair of geometric constructs $T\;\rightrightarrows\; O$.  That is, we require that a certain naturally defined morphism between objects constructed out of $T$-models must be an isomorphism.  (Applying equalizers, we see that this also includes the ability to set morphisms equal, i.e. to construct [[equifier]]s.)

From this point of view, a **geometric theory** is a theory $GrTop^{op}\to Cat$ obtained from some $O_n$ by a finite sequence of simple functional extensions and simple geometric quotients.  Of course, once we know that each $O_n$ has a classifying topos, it follows immediately that any geometric theory has a classifying topos, since $GrTop$ has inserters and inverters.


### Hybrid definition

The following definition is sort of a "halfway house" between logic and geometry.  Start with a first-order [[signature (in logic)|signature]] $\Sigma$ (this is the logical part).  Then we have a 2-functor $\Sigma Str\colon GrTop^{op}\to Cat$ sending a topos $E$ to the category $\Sigma Str(E)$ of $\Sigma$-structures in $E$.  A **geometric theory** over $\Sigma$ is defined to consist of the following.

* For each Grothendieck topos $E$, we have a [[replete subcategory|replete]] [[full subcategory]] $T(E)$ of $\Sigma Str(E)$, such that
* For each geometric morphism $f\colon E\to F$, if $M\in T(F)$ then $f^*M\in T(E)$ (i.e. $T$ is a subfunctor of $\Sigma Str$), and moreover
* For any set-indexed jointly surjective family $(f_i \colon E_i \to E)_{i\in I}$ of geometric morphisms, and any $M \in \Sigma Str(E)$, if $f_i^* M \in T(E_i)$ for all $i$, then $M\in T(E)$.

The equivalence of this definition with the others can be found in

* Olivia Caramello, "A characterization theorem for geometric logic", [arXiv:0912.1404](http://arxiv.org/abs/0912.1404).

It is not sufficient, in the third condition, to restrict to the case when $I$ is a singleton, but it is sufficient to consider the case when $I$ is a singleton together with all families of coproduct injections $(E_i \to \coprod_i E_i)_{i\in I}$.

## Localization

By framing this notion in the [[internal language]] of a [[topos]] $S$ we can talk of geometric theories over $S$, with models in [[bounded topos|bounded]] $S$-toposes (the [[relative point of view|relative version]] of "Grothendieck topos").  As a simple example, if we have a sheaf $A$ of [[rings]] on a [[topological space]] $X$ we can describe left $A$-[[modules]] as models of a geometric theory over $Sh(X)$, the topos of sheaves on $X$, and this notion is definable in $Sh(X)$-toposes.

Similarly to the $Set$-based case, given a geometric theory $T$ over a topos $S$, we can form the $S$-topos $S[T] \to S$ that classifies $T$, for which the category of $T$-models in a bounded $S$-topos $E$ is naturally equivalent to the category of morphisms of $S$-toposes $E \to S[T]$. In other words

$$T Mod(E) \simeq Top_S(E,S[T])$$

## Morphisms of theories

Since the classifying topos encodes the "extensional essence" of a geometric theory, it makes sense to define a **map of theories** $T \to T'$ to be a morphism of $S$-toposes $h: S[T'] \to S[T]$. Equivalently, of course, this is a $T$-model in $S[T']$.  Composition with $h$ induces a functor, _[[forgetful functor|forget]] along_ $h$, from $T'$-models to $T$-models in any $S$-topos.


## Gros categories of models

Define the [[gros category]] $T Mod$ of $T$-models to have as objects pairs $(E,A)$ where $E$ is an $S$-topos and $A$ is
a $T$-model in $E$. A map $(f,g): (E,A) \to (F,B)$ is given
by a morphism $f: F \to E$ of $S$-toposes and a homomorphism $g: f^*(A) \to B$ of $T$-models in $F$. The
composition of maps should be evident. A map $h: T \to T'$
of geometric theories over $S$ induces a forgetful functor
$T' Mod \to T Mod$ which leaves unchanged the $S$-topos of residence, which has a left adjoint $T Mod \to T' Mod$ which may change the topos.  For if $a: E \to S[T]$ is a $T$-model in $E$, [[base change|pulling]] $a$ back along $h$ yields a $T'$-model, not in $E$ but in the [[pullback]].  This is a consequence of general facts about finite [[2-limits]] of the [[2-category]] of 
[[bounded topos|bounded]] $S$-toposes.

The 2-categorical version of $T Mod$ is useful in generalization of the [[spectrum]] construction: See at [[Cole's theory of spectrum]].

## Properties

* [[Barr's theorem]] says, that if a statement in [[geometric logic]] is deducible from a [[geometric theory]] using classical [[logic]] and the [[axiom of choice]], then it is also deducible from it in [[constructive mathematics]]. 

## Related concepts

* [[geometric type theory]]

* [[geometric homotopy type theory]]

* [[Cole's theory of spectrum]]

* [[classifying topos for the theory of objects]]

* [[theory of objects]]

* [[theory of decidable objects]]

* [[theory of model homomorphisms]]

* [[theory of flat functors|theory of flat diagrams]]

* [[theory of categories]]

## References

Review:

* [[Steven Vickers]], *Continuity and geometric logic*, Journal of Applied Logic Volume 12, Issue 1, March 2014, Pages 14-27 ([doi:10.1016/j.jal.2013.07.004](https://doi.org/10.1016/j.jal.2013.07.004))

Textbook accounts:

* [[Peter Johnstone]], sections B4.2, D1.1 of _[[Sketches of an Elephant]]_

* [[Michael Makkai]], [[Gonzalo E. Reyes]], _First Order Categorical Logic_ , LNM 611, Springer Berlin 1977. ([draft](https://marieetgonzalo.files.wordpress.com/2018/04/makkai-reyes-book.pdf))

A textbook account of (finitary) geometric logic can be found in

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

A systematic introduction to topos theory and geometric logic can be found in the following draft by O. Caramello:

* [[Olivia Caramello]], _Topos-theoretic background_ , ms. 2014. ([pdf](http://www.oliviacaramello.com/Unification/ToposTheoreticPreliminariesOliviaCaramello.pdf))

which has become a chapter of the following monograph exploring first-order model theory in the context of Grothendieck toposes:

* [[Olivia Caramello]], _Theories, Sites, Toposes_ , Oxford UP 2018.

For additional background on (finitary) geometric formulas consider:

* Karel Stokkermans, [[Bill Lawvere]], and [[Steve Vickers]]: _Catlist discussion March 1999_ . ([link](http://comments.gmane.org/gmane.science.mathematics.categories/1058))

* H.J. Keisler: _Theory of models with generalized atomic formulas_ , JSL 25 (1960), pp.1-26.

Discussion in the context of [[computer science]] is in

* [[Steve Vickers]], _Geometric logic in computer science_ ([pdf] (http://www.cs.bham.ac.uk/~sjv/GLiCS.pdf))

Discussion with an eye towards [[geometric type theory]] is in 

* {#Vickers09}[[Steve Vickers]], _Locales and toposes as spaces_ ([pdf](http://www.cs.bham.ac.uk/~sjv/LocTopSpaces.pdf))

[[Stone duality]] for geometric theories is discussed in:

* [[Henrik Forssell]], _Topological representation of geometric theories_,  [arxiv/1109.0699](http://arxiv.org/abs/1109.0699)

A nice short exposition together with an unorthodox proposal to expand geometric logic with fix point operators can be found here:

* [[Andreas Blass]], _Topoi and Computation_, Bull. European Assoc.Theoret. Comp.Sci. **36** (1988) pp.57-65. ([draft](http://www.math.lsa.umich.edu/~ablass/eatcs.pdf))

[[!redirects geometric theory]]
[[!redirects geometric theories]]
[[!redirects geometric logic]]
[[!redirects geometric logics]]
[[!redirects geometric formula]]
[[!redirects geometric formulas]]
[[!redirects geometric formulae]]
[[!redirects geometric sequent]]
[[!redirects geometric sequents]]