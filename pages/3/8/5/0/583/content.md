
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea 

One of the most important observations of [[category theory]] is that large parts of mathematics can be [[internalization|internalized]] in any [[category]] with sufficient structure.  The most basic examples of this involve algebraic structures; for instance, a [[group]] can be defined in any category with finite products, and an [[internal category|internal]] [[strict category]] can be defined in any ambient category with [[pullback]]s. For such [[algebraic theory|algebraic]] (or even [[essentially algebraic theory|essentially algebraic]]) structures, which are defined by _operations_ with _equational axioms_ imposed, it suffices for the ambient category to have (usually finite) limits.

However, if we assume that the ambient category has additional structure, then much more of mathematics can be internalized, potentially including [[field]]s, [[local ring]]s, [[finite set]]s, [[topological space]]s, even the field of [[real number]]s.  The idea is to exploit the fact that all mathematics can be written in the language of [[logic]], and seek a way to internalize logic in a category with sufficient structure.

The basic ideas of the internal logic induced by a given [[category]] $C$ are:

* the [[object]]s $A$ of $C$ are regarded as collections of things of a given [[type]] $A$

* the [[morphisms]] $A\to B$ of $C$ are regarded as terms of type $B$ containing a free [[variable]] of type $A$ (i.e. in a [[context]] $x:A$)

* a [[subobject]] $\phi \hookrightarrow A$ is regarded as a _proposition_ ([[predicate]]): by thinking of it as the sub-collection of all those things of type $A$ for which the statement $\phi$ is [[true]]

  * the maximal subobject is hence the proposition that is always true; this is the logical object of [[truth]] $\top \hookrightarrow A$

  * the minimal subobject is hence the proposition that is always false; this is the logical object of [[falsity]] $\bottom \hookrightarrow A$

  * one proposition [[implication|implies]] another if as subobjects of $A$ they are connected by a morphism in the [[poset]] of subobjects: $\phi \Rightarrow \psi$ means $\phi \hookrightarrow \psi$

* Logical operations are implemented by [[universal construction]]s on [[subobject]]s.
  
  * the conjunction [[and]] is the [[product]] of subobjects (their [[meet]])

  * the conjunction [[or]] is the [[coproduct]] of subobjects (their [[join]])

and so on.

* A [[dependent type]] over an object $A$ of $C$ may be interpreted as a morphism $B\to A$ whose "fibers" represent the types $B(x)$ for $x:A$.  This morphism might be restricted to be a [[display map]] or a [[fibration]].

Once we formalize the notion of "logical [[theory]]", the construction of the internal logic can be interpreted as a [[functor]] $Lang$ from suitably structured categories to theories.  The morphisms of theories are "interpretations", and so an internalization of some theory $T$ (such as the "theory of groups") into a category $C$ is a morphism of theories $T\to Lang(C)$.

Moreover, the functor $Lang$ has a left [[adjoint functor]]: the [[syntactic category]] $Syn$ of a theory.  Thus, a model of $T$ in $C$ is equally well a functor $Syn(T)\to C$.  Frequently, this adjunction is even an [[equivalence of categories]]; see [[relation between type theory and category theory]].


### Kinds of internal logics in different categories

There are many different kinds of of "logical theories", each of which corresponds to a type of category in which such theories can be internalized (and yields a corresponding adjunction $Syn \dashv Lang$).

|Theory| |Category|
|------|-|--------|
|[[Lawvere theory|Lawvere]] (or "finite product")| |category with [[finite products]]|
|[[cartesian logic|cartesian]] (or "left exact" or "finite limit")| |[[finitely complete category]]|
|[[minimal logic]]| |[[cartesian closed category]]
|[[regular logic|regular]]| |[[regular category]]|
|[[coherent logic|coherent]]| |[[coherent category]]|
|[[disjunctive logic|disjunctive]]| |[[extensive category|lextensive category]] (aka finitary disjunctive category)|
|[[geometric logic|geometric]]| |[[coherent category|infinitary coherent category]] (aka [[geometric category]])|
|[[constructive logic|constructive]] [[first-order logic|first-order]]| |[[Heyting category]]|
|[[classical logic|classical]] [[first-order logic|first-order]]| |[[Boolean category]]|
|[[extensional type theory|extensional]] [[dependent types]]| |[[locally cartesian closed category]]|
|[[constructive logic|constructive]] [[higher order logic|higher order]]| |[[topos|elementary topos]]|
|[[classical logic|classical]] [[higher order logic|higher order]]| |[[Boolean topos]]|
|[[linear logic]]| |[[symmetric monoidal category]]|
|[[cohesive homotopy type theory|cohesive modal logic]]| |[[cohesive topos]]|

Each type of logic up to and including "geometric" can also be described in terms of [[sketch|sketches]].  Not coincidentally, the corresponding types of category up to and including "geometric" fit into the framework of [[familial regularity and exactness]].  Sketches can also describe theories applicable to categories not even having finite products, such as finite sum sketches, but the type-theoretic approach taken on this page requires at least finite products (or else something closely akin, such as a [[cartesian multicategory]]).

However, there are other sorts of [[internalization]] that do not fit in this framework.  For instance, to describe a [[monoid]] internal to a [[monoidal category]], one needs an internal [[linear logic]].  See [[internalization]] for a discussion of the more  general notion in the context of [[doctrine]]s.


## Internal first-order logic

We begin with the interpretation of internal first-order logic, which is the most used in [[toposes]] and related categories.

### Theories

In this section, what we mean by a _theory_ is a _[[type theory]]_ without dependent types, but with a dependent logic.  This entails the following.

* The [[signature (in logic)|signature]] of the theory consists of

  * Various _[[types]]_ $A,B,C$.  For example, the theory of a group has only one type (group elements), but the theory of a-ring-and-a-module has two types (ring elements and module elements).  There are also generally _type constructors_ that build new types from basic ones, such as product types $A\times B$ and the unit type $1$.

  * The theory will also generally contain _[[function symbol]]s_ such as $f:A\to B$, each with a source and target that are types.  For example, the theory of a monoid has one type $M$, one function symbol $m:M\times M\to M$, and one function symbol $e:1\to M$.  Function symbols of source $1$ are also called _constants_.

  * The theory may also contain _[[relation symbol]]s_ $R:A$, each equipped with a type.  For example, the theory of a [[partial order|poset]] has one type $P$ and one relation $\le:P\times P$.  The most basic relation symbol, which most theories contain, is _[[equality]]_ $=_A:A\times A$ on a type $A$.

* Finally the theory may contain _logical [[axiom]]s_ of the form $\Gamma | \varphi  \vdash \psi$.  Here $\varphi$ and $\psi$ are first-order formulas built up from terms and relation symbols using logical connectives and quantifiers such as $\top,\bot,\wedge,\vee,\Rightarrow,\neg,\forall,\exists$, and $\Gamma$ is a _[[context]]_ which declares the type of every variable occurring in $\varphi$ and $\psi$.

For example, the theory of a group has one type $G$, three function symbols $m:G\times G\to G$, $i:G\to G$, and $e:1\to G$, and axioms
$$\array{
  x:G,y:G,z:G |  \top \vdash m(m(x,y),z) = m(x,m(y,z))\\
  x:G | \top \vdash m(x,i(x)) = e \;\wedge\; m(i(x),x) = e\\
  x:G | \top \vdash m(x,e) = x \;\wedge\; m(e,x) = x.
}$$
This is an _[[equational theory]]_, meaning that each axiom is just one or more equations between terms that must hold in a given context.  For a different sort of example, the theory of a poset has one type $P$, one relation $\le:P\times P$, and axioms
$$\array{
  x:P | \top \vdash x\le x\\
  x:P,y:P | x\le y \;\wedge\; y\le x \vdash x=y\\
  x:P,y:P,z:P | x\le y \;\wedge\; y\le z \vdash x\le z.
}$$


### Categorical semantics {#CategoricalSemantics}

Now suppose that we have a category $C$ with [[finite limit]]s and we want to interpret such a theory internally in $C$. We identify the aspects of the theory with structures in the category by what is called [[categorical semantics]]: 

First, for each _type_ in the theory we choose an [[object]] of $C$.  Then for each _function symbol_ in the theory we choose a [[morphism]] in $C$.  And finally, for each _relation_ in the theory we choose a [[subobject]] in $C$. (We always interpret the relation of _equality_ on a type $A$ by the diagonal $A\hookrightarrow A\times A$ in $C$.)  Thus, for example, to interpret the theory of a group in $C$ we must choose an object $G$ and morphisms $m:G\times G\to G$, $i:G\to G$, and $e:1\to G$, while to interpret the theory of a poset, we must choose an object $P$ and a subobject $[\le] \hookrightarrow P\times P$.

Of course, this is not enough; we need to say somehow that _the axioms are satisfied_.  We first define, inductively, an interpretation of every _term_ that can be constructed from the theory by a morphism in $C$.  For example, given an object $G$ and a morphism $m:G\times G\to G$, there are two evident morphisms $G\times G\times G \to G$ which are the interpretations of the two terms $m(m(x,y),z)$ and $m(x,m(y,z))$.

We then define, inductively, an interpretation of every _[[logical formula]]_ that can be constructed from the theory by a _subobject_ in $C$.  The idea is that if $x:A$ is a variable of type $A$ and $\varphi(x)$ is a formula with $x$ as its free variable, then the interpretation of $\varphi(x)$ should be the "subset" $\{x\in A | \varphi(x)\}$ of $A$.  The base case of this induction is that if $t$ is a term interpreted by a morphism $A\to B$ and $R:B$ is a relation symbol, then $R(t)$ is interpreted by the pullback of the chosen subobject $R\hookrightarrow B$ representing $R$ along the morphism $t:A\to B$.  The building blocks of logical formulas then correspond to operations on the posets $Sub(A)$ of subobjects in $C$, as follows.

|Logical operator| |Operation on $Sub(A)$|
|----------------|-|---------------------|
|[[logical conjunction|conjunction]]: $\wedge$| |[[intersection]] (pullback)|
|[[truth]]: $\top$| |[[top element]] ($A$ itself)|
|[[disjunction]]: $\vee$| |[[union]]|
|[[falsity]]: $\bot$| |[[bottom element]] ([[initial object|strict initial object]])|
|[[implication]]: $\Rightarrow$| |[[Heyting algebra|Heyting implication]]|
|[[existential quantification]]: $\exists$| |[[left adjoint]] to [[pullback]]|
|[[universal quantification]]: $\forall$| |[[right adjoint]] to [[pullback]]|

The fact that existential and universal quantifiers can be interpreted as left and right adjoints to pullbacks was first realized by [[Bill Lawvere]].  One way to realize that it makes sense is to notice that in [[Set]], the image of a subset $R\subset A$ under a function $f:A\to B$ can be defined as
$$\{b\in B | (\exists a\in A)(a\in R \;\wedge\; f(a)=b)\},$$
while its "dual image" (the right adjoint to pullback) can be defined as
$$\{b\in B | (\forall a \in A)(f(a)=b \Rightarrow a\in R)\}.$$

Of course, not in all finitely complete categories $C$ do all these operations on subobjects exist.  Moreover, in order for the relationship with logic to be well-behaved, any of the operations we make use of must be *[[pullback stability|stable]] under* (preserved by) pullbacks.  (Pullbacks of subobjects correspond to "innocuous" logical operations such as adding extra unused variables, duplicating variables, and so on, so they should definitely not affect the meaning of the logical connectives.  However, in [[linear logic]] such operations become less innocuous.)

In any category with finite limits, the posets $Sub(A)$ always have finite intersections (given by pullback), including a top element (given by $A$ itself).  Thus in any such category, we can interpret logical theories that use only the connectives $\wedge$ and $\top$.  This includes both the theories of groups and posets considered above.  
In a [[regular category]], the existence of pullback-stable [[image]]s implies that the [[base change]] functor $f^*:Sub(B)\to Sub(A)$ along any map $f:A\to B$ has a left adjoint, usually written $\exists_f$, and that these adjoints "commute with pullbacks" in an appropriate sense (given by the [[Beck-Chevalley condition]].  Thus, in a regular category we can interpret any theory in so-called _[[regular logic]]_, which uses only $\wedge$, $\top$, and $\exists$.

Actually, some instances of $\exists$ can be interpreted in any category with finite limits: if $f$ is itself a monomorphism, then $f^*$ always has a left adjoint, given simply by composition with $f$. On the logical side, this means that we can interpret "provably unique existence" in any category with finite limits.  Logic with $\wedge$, $\top$, and "provably unique existence" is called _cartesian logic_ or _finite-limit logic_.

A [[coherent category]] is basically defined to be a [[regular category]] in which the subobject posets additionally have pullback-stable finite unions.  Thus, in a coherent category we can interpret so-called _coherent logic_, which adds $\vee$ and $\bot$ to [[regular logic]].  Likewise, in an infinitary-coherent (or "geometric") category we can interpret _geometric logic_, which adds infinitary disjunctions $\bigvee_i \varphi_i$ to coherent logic.  Geometric logic is especially important because it is preserved by the inverse image parts of [[geometric morphism]]s, and because any geometric theory has a [[classifying topos]].

On the other hand, in a [[extensive category|lextensive category]], we do not have images or all unions, but if we have two subobjects of $A$ which are _disjoint_ (their intersection is initial), then their coproduct is also their union in $Sub(A)$.  Therefore, in a lextensive category we can interpret _disjunctive logic_, which is cartesian logic plus $\bot$ and "provably disjoint disjunction."  Likewise, in an infinitary-lextensive category we can interpret "infinitary-disjunctive logic."

Finally, in a [[Heyting category]] the base change functors $f^*:Sub(B)\to Sub(A)$ also have right adjoints, usually written $\forall_f$, and it is easy to see that this implies that each $Sub(A)$ is also a [[Heyting algebra]], hence has an "implication" $\Rightarrow$ as well.  (We define "negation" by $\neg \varphi \equiv \varphi \Rightarrow \bot$.)  Thus, in a Heyting category we can interpret all of (finitary, first-order) [[intuitionistic logic]].

Now that we know how to interpret logic, we can say that a **model** of a given theory in $C$ consists of a choice of objects, morphisms, and subobjects for the types, function symbols, and relation symbols as above, such that for each axiom $\Gamma | \varphi \vdash \psi$, we have $[\varphi]\le [\psi]$ in $Sub([\Gamma])$.  Here, $[\Gamma]$ is the product of the objects that correspond to the types of the variables in $\Gamma$, $[\varphi]$ and $[\psi]$ are the interpretations of the formulas $\varphi$ and $\psi$ as subobjects of $[\Gamma]$, and $\leq$ is the relation of subobject inclusion.

It is easy to verify that a model of the theory of a group in $C$ is precisely an internal [[group]] object in $C$, as usually defined.  For instance, the validity of the axiom
$$x:G,y:G,z:G | \top \vdash m(m(x,y),z) = m(x,m(y,z))$$
 means that the [[equalizer]] of the two morphisms $G\times G\times G \to G$ must be all of $G\times G\times G$, or equivalently that those two morphisms must be equal.  The same happens in most other cases.


### The internal logic as a functor

As described above, a model of a given theory $T$ in a category $C$ consists of an assignment

| | | |
|---------------- |-| ---------------------|
|types of $T$|$\to$|objects of $C$|
|function symbols of $T$|$\to$|morphisms of $C$|
|relation symbols of $T$|$\to$|subobjects in $C$|
|axioms of $T$|$\to$|containments in $C$|

This is a sort of [[heteromorphism]] in that it changes the name of things as it operates on them.  We can describe it more simply as a "translation of theories" as follows.

Given a category $C$ (which may be regular, coherent, geometric, Heyting, etc.), we define its **internal type theory (with first-order logic)** $Lang(C)$ to be the theory whose

* types are the objects of $C$;
* function symbols are the morphisms on $C$;
* relation symbols are the subobjects in $C$;
* axioms are the containments in $C$.

Now a model of $T$ in $C$ can be described simply as a morphism of theories (a "translation" or "interpretation")

$$T \to Lang(C).$$

The functor $Lang : Categories \to Theories$ has a left adjoint, the [[syntactic category]] of a theory.  Thus we have a chain of natural isomorphisms

$$ Theories(T,Lang(C)) \cong Models(T,C) \cong Categories(Syn(T),C)). $$


## Soundness and internal reasoning 

Internal logic is not just a way to concisely describe internal structures in a category, but also gives us a way to _prove_ things about them by "internal reasoning."  We simply need to verify that the "usual" methods of logical reasoning (for example, from $\varphi\vdash \psi$ and $\psi\vdash \chi$ deduce $\varphi\vdash\chi$) are _internally valid_, in the sense that if the premises are satisfied in some model $C$ (in the example, if $[\varphi]\le [\psi]$ and $[\psi]\le [\chi]$) then so is the conclusion (in the example, $[\varphi]\le [\chi]$).  This is called the _Soundness Theorem_.

It then follows that if we start from the axioms of a theory and "reason normally" within type theory, which in practice amounts to pretending that the types are sets, the function symbols are functions, and the relation symbols are subsets, then anything we prove will still be true when the theory is interpreted in an _arbitrary_ category, not just [[Set]].  For example, by easy equational reasoning from the theory of a group, we can prove that inverses are unique, which is expressed by the logical sequent
$$x:G,y:G,z:G | m(x,y)=e \;\wedge\; m(x,z)=e \vdash y=z.$$
It follows that this is also true, suitably interpreted, as a statement about internal group objects in _any_ category.

There are (at least) three caveats.  Firstly, we must take care to use only the rules appropriate to the fragment of logic that is valid in the particular categories we are interested in.  For example, if we want our conclusions to be valid in any [[regular category]], we must restrict ourselves to reasoning "within regular logic."  Most mathematicians are not familiar with making such distinctions in their reasoning, but in practice most things one would want to say about a regular theory turn out to be provable in regular logic.  (We will not spell out the details of what this means.)  And once we are in a Heyting category, and in particular in a topos, this problem goes away and we can use full first-order logic.

The second, more important, caveat is that the internal logic of all these categories is, in general, [[constructive mathematics|constructive]]. This means that, among other things, the interpretation of $\neg\neg\varphi$ is, in general, distinct from that of $\varphi$, and that $\varphi\vee \neg\varphi$ is not always valid.  So even if we believe that [[classical logic]] (including the principle of [[excluded middle]] and even the [[axiom of choice]]) is "true," as many mathematicians do, there is still a reason to look for proofs that are constructively acceptable, since it is only these which are valid in the internal logic of most categories.  If the category is [[Boolean category|Boolean]] and/or satisfies the internal [[axiom of choice]], however, then this problem goes away, but these fail in many categories in which one wants to internalize (such as many [[Grothendieck topos]]es).

The third caveat is that one must take care to distinguish the _internal_ logic of a category from what is _externally_ true about it.  In general, internal validity is "local" truth, meaning things which become true "after passing to a [[cover]]."  This is particularly important for formulas involving _disjunction_ and _existence_.  For example, an object's being [[projective object|projective]] in the category $C$ is a different statement from its being _internally_ projective, meaning that "$X$ is projective" is true in the internal logic.  Another good example can be found in the different notions of [[finite object]] in a topos.  This problem goes away if the ambient category is [[well-pointed topos|well-pointed]], but well-pointed categories are even rarer than Boolean ones satisfying choice; the only well-pointed Grothendieck topos is [[Set]] itself.


## Completeness, syntactic categories, and Morita equivalence
{#syntactic_categories}

The converse of the Soundness Theorem is called the _Completeness Theorem_, and states that if a sequent $\varphi\vdash\psi$ is valid in every model of a theory, then it is _provable_ from that theory.  This is noticeably less trivial.  In classical first-order logic, where the only models considered are set-valued ones, the completeness theorem is usually proven using [[ultraproduct]]s.  However, in categorical logic there is a more elegant approach (which additionally no longer depends on any form of the [[axiom of choice]]).

The **[[syntactic category]]** $C_T = Syn(T)$ of a theory $T$ was mentioned above, as the left adjoint to the "internal logic functor" $Lang$.  By the [[Yoneda lemma]], the syntactic category $C_T$ contains a "generic" model of the theory.  Moreover, by the construction of $C_T$ (see [[syntactic category]]), the valid sequents in this model are *precisely* those provable from the theory.  Therefore, if a sequent is valid in all models, it is in particular valid in the generic model in $C_T$, and hence provable from $T$.

The universal property of $C_T$ is also sometimes useful for semantic conclusions.  For instance, sometimes one can prove something about the generic model and then carry it over to all models.

Furthermore, if $T$ lives in a sub-fragment of geometric logic (such as regular, coherent, lextensive, or geometric logic), then the [[Grothendieck topos]] of [[sheaf|sheaves]] on $C_T$ for its appropriate (regular, coherent, extensive, or geometric) [[coverage]] contains a $T$-model which is generic for models in Grothendieck toposes: any $T$-model in a Grothendieck topos is its image under the inverse image of a unique [[geometric morphism]].  This topos is called the **[[classifying topos]]** of the theory.

The [[syntactic category]] of a theory can be considered as the "extensional essence" of that theory, since functors out of $C_T$ completely determine the $T$-models in any category $D$ with suitable structure.  It therefore makes sense, in some contexts, to define a _morphism_ of theories to be a functor between their [[syntactic categories]], and an _equivalence_ of theories (sometimes called a _Morita equivalence_) to be an equivalence between their syntactic categories.

A morphism $T\to T'$ between theories, in this sense, induces a functor from $T'$-models in $D$ to $T$-models in $D$, for any category $D$ with suitable structure, in a way which is natural in $D$.  In particular, theories which are "Morita equivalent" in this sense have naturally equivalent categories of models in all categories $D$ with suitable structure; so they have the same "meaning" even though they may be presented quite differently.  (Note that this is a much stronger sort of equivalence than merely having equivalent categories of models in some particular category, such as $Set$.)  Moreover, the fact that the syntactic category is defined "syntactically" means that a morphism $T\to T'$ actually induces a "translation" of the types, functions, and relations of $T$ into those of $T'$.

By first applying various "completion" processes to syntactic categories before asking about equivalence, we obtain coarser notions of equivalence, which only induce equivalences of models in more restricted sorts of categories.  For instance, if we compare the [[exact completion]]s of syntactic categories of regular theories, we obtain a notion of equivalence that induces equivalences of categories of models in all exact categories (not necessarily all regular ones).  Likewise for coherent theories and [[pretopos]]es, and for geometric theories and infinitary pretoposes.  Note, though, that the infinitary-pretopos completion of a (small) geometric theory is in fact already a (Grothendieck) topos, and coincides with the classifying topos considered above.  Thus, passage to classifying toposes is also an instance of this construction, and an equivalence of classifying toposes means that two theories have equivalent categories of models in all toposes.  (This is still much stronger than just having equivalent categories of models in $Set$.)


## Kripke--Joyal semantics

To be written, but see [[Kripke-Joyal semantics]].


## Dependent type theory

We now consider the internal language of a [[locally cartesian closed category]] as a [[dependent type theory]].

+--{: .standout}
Material to be moved here from [[relation between type theory and category theory]].
=--


## Higher-order logic 

To be written, but see [[Mitchell–Bénabou language]] for the version in a [[topos]].


## Examples

### Internal logic in $Set$ {#LogicOfSet}

The [[topos]] [[Set]] in [[classical mathematics]] of course has as its internal logic the "ordinary" logic. This is reproduced by following the abstract nonsense as follows:

the [[terminal object]] of [[Set]] is [[generalized the|the]] one-element set ${*}$, the [[subobject classifier]] in [[Set]] is the two-element set $\Omega = \{true, false\}$ equipped with the map

$$
  T : {*} \to \Omega
$$

that picks the element $true$ in $\Omega$. The [[Heyting algebra]] of [[subobject]]s of the [[terminal object]] is the [[poset]]

$$
  L = \{  \emptyset \hookrightarrow {*} \}
$$

consisting only of the two trivial subobjects of $*$, the point itself and the empty set, and the unique inclusion morphism between them. These are classified, respectively, by the [[truth value]]s ${*} \stackrel{true}{\to} \Omega$ and ${*} \stackrel{false}{\to} \Omega$, so that we can also write our [[poset]] of [[subobject]]s of the [[terminal object]] as

$$
  L = \{  false \to true \}
  \,.
$$

The logical operation $\wedge = AND$ is the [[product]] in the [[poset]] $L$. Indeed we find pullback diagrams in $L$

$$
  \array{
    true \times \true = true &\to& true
    \\
    \downarrow
    \\
    true
  }
  \;\;\;
  \;\;\;
  \;\;\;
  \array{
    true \times false = false &\to& false
    \\
    \downarrow
    \\
    true
  }
  \;\;\;
  \;\;\;
  \;\;\;
  \array{
    false \times false = false &\to& false
    \\
    \downarrow
    \\
    false
  }
  \,.
$$

The logical operation $\vee = OR$ is the [[coproduct]] in the [[poset]] $L$. Indeed we find [[pushout]] diagrams in $L$

$$
  \array{
    && true
    \\
    && \downarrow
    \\
    true
    &\to&
    true \coprod \true = true   
  }
  \;\;\;\;
  \;\;\;
  \;\;\;
   \array{
    && false
    \\
    && \downarrow
    \\
    true
    &\to&
    true \coprod false = true
  }
  \;\;\;\;
  \;\;\;
  \;\;\;
   \array{
    && false
    \\
    && \downarrow
    \\
    false
    &\to&
    false \coprod false = false
  }
 \,.
$$

The logical operation $\not = NOT$ is given by the [[internal hom]] into the [[initial object]] in $L$:

$$
  \not = hom(-, false) : L^{op} \to L
  \,.
$$

We find the value of the [[internal hom]] by its defining [[adjunction]]. For $hom(true,false)$ we have

$$
  Hom_L(true, hom(true,false)) \simeq Hom_L(true \times true, false) = Hom_L(true, false) = \emptyset
$$

and

$$
  Hom_L(false, hom(true,false)) \simeq Hom_L(false \times true, false) = Hom_L(false, false) = {*}
$$

from which we deduce that

$$
  hom(true,false) = false\,.
$$

Similarly for $hom(false,false)$ we have

$$
  Hom_L(true, hom(false,false)) \simeq 
  Hom_L(true \times false, false)
  = Hom_L(false, false) = {*}
$$

and

$$
  Hom_L(false, hom(false,false)) \simeq 
  Hom_L(false \times false, false)
  = Hom_L(false, false) = {*}
$$

from which we deduce that 

$$
  hom(false,false) = true
  \,.
$$

This way all the familiar logical operations are recovered from the internal logic of the [[topos]] [[Set]].



### Internal logic in a sheaf topos on open subsets 
 {#LogicOfPresheaves}

Let $X$ be a [[topological space]] and $Op(X)$ its [[category of open subsets]] and $Sh(X) := Sh(Op(X))$ the [[Grothendieck topos]] of [[category of sheaves|of sheaves]] on $X$.

We discuss the internal logic of this sheaf topos (originally [Tarski, 1938 ](#Tarski)).

The [[terminal object]] is the sheaf [[representable functor|represented by]] $X$: the one that is constant on the one-element set

$$
  X : U \mapsto {*}
  \,.
$$

The [[subobject]]s of this object are the [[representable functor|representable presheaves]]

$$
  hom(-,V) : U \mapsto
  \left\{
    \array{
      {*} & | if U \subset V
      \\
      \emptyset & otherwise
    }
  \right.
$$

for $V \in Op(X)$.

+-- {: .num_remark}
###### Remark
In the *[[presheaf]]* topos $PSh(Op(X))= Func(Op(X)^{op},Set)$, the subobjects of $1$ are arbitrary [[sieves]] in $Op(X)$, not just representables.  For instance, for any two open sets $U$ and $V$ there is a sieve consisting of all open sets contained in either $U$ or $V$, which doesn't necessarily contain $U\cup V$.  It's only in the *sheaf* topos $Sh(X)$ that the representables are precisely the subobjects of $1$.  
=--

The [[poset]] of [[subobject]]s formed by these is just the [[category of open subsets]] itself:

$$
  L = Op(X)
  \,.
$$

* The logical operation $AND$ is the [[product]] in $Op(X)$: this is the **intersection** of open subsets.

* The logical operation $OR$ is the [[coproduct]] in $Op(X)$: this is the **union** of open subsets.

* The [[internal hom]] in $Op(X)$ is given by

  $$
    hom(U,V) = (U^c \vee V)^\circ
  $$

  (the interior of the union of the complement of $U$ 
  with V).

  So **negation** is given by sending an open subset 
  to the interior of its complement:
 
  $$
    \not U = hom(U,\emptyset)
    = (U^c \vee \emptyset)^\circ = (U^c)^\circ
    \,.
  $$

In particular we find that in the internal logic of $PSh(X)$ the law of the [[excluded middle]] fails in general, as in general we do not have that 

$$
  (\not U) \vee U = true
$$

because $\not U \vee U = (U^c)^\circ \cup U = X \backslash \partial U$ is the total space $X$ without the boundary (frontier) of $U$, and not $true = X$, all of the total space.

Thus, the internal logic of this [[Grothendieck topos|sheaf topos]] is (in general) [[intuitionistic logic]].  As remarked above, this is the case in many toposes.


## Related concepts


* [[type theory]], [[homotopy type theory]]

* [[relation between category theory and type theory]]


## References 

### General

Most books on topos theory develop some internal logic, at least in the context of a topos.  For example:

* [[Saunders Mac Lane]] [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ 

* Goldblatt, _Topoi: the categorial analysis of logic_

* [[Francis Borceux]], Section 6 of: _[[Handbook of Categorical Algebra]]_, Vol 3: _Categories of Sheaves_, Encyclopedia of Mathematics and its Applications **50**

* [[Peter Johnstone]], Part D of: _[[Sketches of an Elephant]]_

is comprehensive.

Phoa has a presentation of the internal logic of a topos over a dependent type theory, as opposed to other systems which use simple type theory. This is system is not minimal, but close to what is used in practice [PS](http://www.lfcs.inf.ed.ac.uk/reports/92/ECS-LFCS-92-208/ECS-LFCS-92-208.ps.gz).

The book

* [[Bart Jacobs]], _Categorical Logic and Type Theory_ 

works in the even more general context of [[Grothendieck fibration|fibrations]], allowing us to associate to each object $A$ an arbitrary poset instead of $Sub(A)$.

The book

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_ 

is arguably all about this subject (although you wouldn\'t know it until about Chapter VIII), but from a different perspective.  In particular, Taylor allows us to replace having *all* pullbacks with pullbacks along a pullback-stable class of [[display morphisms]].

A discussion of [[dependent type theory]] as the [[internal language]] of [[locally cartesian closed categories]] is in 

* R. A. G. Seely, _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

The observation that the poset of open subsets of a topological space serve as a model for [[intuitionistic logic]] is apparently originally due to

* {#Tarski} [[Alfred Tarski]], _Der Aussagenkalk&#252;l und die Topologie_, Fundamenta Mathemeticae 31 (1938), pp. 103&#8211;134.
 

### Applications
 {#Applications}

Discussion of fundamental constructions of [[algebraic geometry]] from the perspective of the internal logic of the [[sheaf topos]] over a [[scheme]] ([[Zariski topos]], [[etale topos]]) is in 

* {#Blechschmidt15} [[Ingo Blechschmidt]], _Using the internal language of toposes in algebraic geometry_, talk at [Toposes at IHES](https://indico.math.cnrs.fr/event/747/), November 2015 ([pdf](https://github.com/iblech/internal-methods/blob/master/slides-ihes2015.pdf), [recording](https://www.youtube.com/watch?v=7S8--bIKaWQ))

* {#Blechschmidt16} [[Ingo Blechschmidt]], _Using the internal language of toposes in algebraic geometry_, thesis ([pdf](http://rawgit.com/iblech/internal-methods/master/notes.pdf))

* [[Ingo Blechschmidt]], _Internal methods_ [github repository](https://github.com/iblech/internal-methods)


[[!redirects internal logic]]
[[!redirects internal logics]]
[[!redirects internal language]]
[[!redirects internal languages]]