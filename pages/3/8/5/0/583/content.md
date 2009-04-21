# Idea #

One of the most important observations of [[category theory]] is that large parts of mathematics can be [[internalization|internalized]] in any [[category]] with sufficient structure.  The most basic examples of this involve algebraic structures; for instance, a [[group]] can be defined in any category with finite products, and an [[internal category]] can be defined in any ambient category with [[pullback]]s. For such [[algebraic theory|algebraic]] (or even [[essentially algebraic theory|essentially algebraic]]) structures, which are defined by _operations_ with _equational axioms_ imposed, it suffices for the ambient category to have (usually finite) limits.

However, it turns out that if we assume some additional structure on the ambient category, then much more of mathematics can be internalized, potentially including [[field]]s, [[local ring]]s, [[finite set]]s, [[topological space]]s, even the field of [[real number]]s.  The idea is to exploit the fact that all mathematics can be written in the language of logic, and seek a way to internalize logic in a category with sufficient structure.

(There are other sorts of internalization that do not fit in this general framework.  For example, a [[monoid]] internal to a [[monoidal category]] is not an example of the sort of internalization discussed here; the framework we consider here can only deal with monoids in [[cartesian monoidal category|cartesian monoidal categories]], or at least cartesian [[multicategory|multicategories]].   However, [[linear logic]] holds out the hope of some reconciliation between the two.  See [[internalization]] for a discussion of the more  general notion in the context of [[doctrine]]s.)


# Internal first-order logic #

It turns out that there is a hierarchy of types of logical theories, each of which corresponds to a type of category in which such theories can be internalized.

<table><tr><th>Theory</th><th>Category</th></tr>
<tr><td>finite limit (aka "left exact" or "cartesian")</td><td>[[finitely complete category]]</td></tr>
<tr><td>regular</td><td>[[regular category]]</td></tr>
<tr><td>coherent</td><td>[[coherent category]]</td></tr>
<tr><td>disjunctive</td><td>[[extensive category|lextensive category]] (aka finitary disjunctive category)</td></tr>
<tr><td>geometric</td><td>[[coherent category|infinitary coherent category]] (aka geometric category)</td></tr>
<tr><td>first-order</td><td>[[Heyting category]]</td></tr>
<tr><td>dependent types</td><td>[[locally cartesian closed category]]</td></tr>
<tr><td>higher order</td><td>[[topos|elementary topos]]</td></tr>
</table>

Each type of logic up through "geometric" can also be described in terms of [[sketch|sketches]], which we do not discuss here.  Not coincidentally, the corresponding types of category up through "geometric" fit into the framework of [[familial regularity and exactness]].  Sketches can also describe theories applicable to categories not even having all finite limits, such as finite product sketches or finite sum sketches, but the logical approach taken here seems to require at least finite limits.

For purposes of this page, what we mean by a _theory_ is a _[[type theory]]_.  This entails the following.

* The theory may have many different _types_ $A,B,C$.  For example, the theory of a group has only one type (group elements), but the theory of a-ring-and-a-module has two types (ring elements and module elements).  There are also generally _type constructors_ that build new types from basic ones, such as product types $A\times B$ and the unit type $1$.

* The theory will also generally contain _function symbols_ such as $f:A\to B$, each with a source and target that are types.  For example, the theory of a monoid has one type $M$, one function symbol $m:M\times M\to M$, and one function symbol $e:1\to M$.  Function symbols of source $1$ are also called _constants_.

* The theory may also contain _relation symbols_ $R:A$, each equipped with a type.  For example, the theory of a [[partial order|poset]] has one type $P$ and one relation $\le:P\times P$.  The most basic relation symbol, which most theories contain, is _equality_ $=_A:A\times A$ on a type $A$.

* Finally the theory may contain _logical axioms_ of the form $\Gamma | \varphi  \vdash \psi$.  Here $\varphi$ and $\psi$ are first-order formulas built up from terms and relation symbols using logical connectives and quantifiers such as $\top,\bot,\wedge,\vee,\Rightarrow,\neg,\forall,\exists$, and $\Gamma$ is a _[[context]]_ which declares the type of every variable occurring in $\varphi$ and $\psi$.

For example, the theory of a group has one type $G$, three function symbols $m:G\times G\to G$, $i:G\to G$, and $e:1\to G$, and axioms
$$\array{
  x:G,y:G,z:G |  \top \vdash m(m(x,y),z) = m(x,m(y,z))\\
  x:G | \top \vdash m(x,i(x)) = e \;\wedge\; m(i(x),x) = e\\
  x:G | \top \vdash m(x,e) = x \;\wedge\; m(e,x) = x.
}$$
This is an _equational theory_, meaning that each axiom is just one or more equations between terms that must hold in a given context.  For a different sort of example, the theory of a poset has one type $P$, one relation $\le:P\times P$, and axioms
$$\array{
  x:P | \top \vdash x\le x\\
  x:P,y:P | x\le y \;\wedge\; y\le x \vdash x=y\\
  x:P,y:P,z:P | x\le y \;\wedge\; y\le z \vdash x\le z.
}$$

Now suppose that we have a category $C$ with finite limits and we want to interpret such a theory internally in $C$.  First, for each _type_ in the theory we choose an [[object]] of $C$.  Then for each _function symbol_ in the theory we choose a [[morphism]] in $C$.  And finally, for each _relation_ in the theory we choose a [[subobject]] in $C$. (We always interpret the relation of _equality_ on a type $A$ by the diagonal $A\hookrightarrow A\times A$ in $C$.)  Thus, for example, to interpret the theory of a group in $C$ we must choose an object $G$ and morphisms $m:G\times G\to G$, $i:G\to G$, and $e:1\to G$, while to interpret the theory of a poset, we must choose an object $P$ and a subobject $[\le] \hookrightarrow P\times P$.

Of course, this is not enough; we need to say somehow that _the axioms are satisfied_.  We first define, inductively, an interpretation of every _term_ that can be constructed from the theory by a morphism in $C$.  For example, given an object $G$ and a morphism $m:G\times G\to G$, there are two evident morphisms $G\times G\times G \to G$ which are the interpretations of the two terms $m(m(x,y),z)$ and $m(x,m(y,z))$.

We then define, inductively, an interpretation of every _logical formula_ that can be constructed from the theory by a _subobject_ in $C$.  The idea is that if $x:A$ is a variable of type $x$ and $\varphi(x)$ is a formula with $x$ as its free variable, then the interpretation of $\varphi(x)$ should be the "subset" $\{x\in A | \varphi(x)\}$ of $A$.  The base case of this induction is that if $t$ is a term interpreted by a morphism $A\to B$ and $R:B$ is a relation symbol, then $R(t)$ is interpreted by the pullback of the chosen subobject $R\hookrightarrow B$ representing $R$ along the morphism $t:A\to B$.  The building blocks of logical formulas then correspond to operations on the posets $Sub(A)$ of subobjects in $C$, as follows.

<table><tr><th>Logical operator</th><th>Operation on Sub(<i>A</i>)</th></tr>
<tr><td>[[conjunction]]: &and;</td><td>[[intersection]] (pullback)</td></tr>
<tr><td>truth: &top;</td><td>top element (<i>A</i>)</td></tr>
<tr><td>[[disjunction]]: &or;</td><td>[[union]]</td></tr>
<tr><td>falsity: &bot;</td><td>bottom element ([[initial object|strict initial object]])</td></tr>
<tr><td>implication: &rarr;</td><td>[[Heyting algebra|Heyting implication]]</td></tr>
<tr><td>[[existential quantification]]: &exist;</td><td>[[adjoint functor|left adjoint]] to pullback</td></tr>
<tr><td>[[universal quantification]]: &forall;</td><td>[[adjoint functor|right adjoint]] to pullback</td></tr>
</table>

The fact that existential and universal quantifiers can be interpreted as left and right adjoints to pullbacks was first realized by Lawvere.  One way to realize that it makes sense is to notice that in [[Set]], the image of a subset $R\subset A$ under a function $f:A\to B$ can be defined as
$$\{b\in B | (\exists a\in A)(a\in R \;\wedge\; f(a)=b)\},$$
while its "dual image" (the right adjoint to pullback) can be defined as
$$\{b\in B | (\forall a \in A)(f(a)=b \Rightarrow a\in R)\}.$$

Of course, in not all finitely complete categories $C$ do all these operations on subobjects exist.  Moreover, in order for the relationship with logic to be well-behaved, any of these operations we make use of must be *[[pullback stability|stable]] under* (preserved by) pullbacks.  (Pullbacks of subobjects correspond to "innocuous" logical operations such as adding extra unused variables, duplicating variables, and so on, so they should definitely not affect the meaning of the logical connectives.  However, in [[linear logic]] such operations become less innocuous.)

In any category with finite limits, the posets $Sub(A)$ always have finite intersections (given by pullback), including a top element (given by $A$ itself).  Thus in any such category, we can interpret logical theories that use only the connectives $\wedge$ and $\top$.  This includes both the theories of groups and posets considered above.  
In a [[regular category]], the existence of pullback-stable [[image]]s implies that the [[base change]] functor $f^*:Sub(B)\to Sub(A)$ along any map $f:A\to B$ has a left adjoint, usually written $\exists_f$, and that these adjoints "commute with pullbacks" in an appropriate sense (given by the [[Beck-Chevalley condition]].  Thus, in a regular category we can interpret any theory in so-called _regular logic_, which uses only $\wedge$, $\top$, and $\exists$.

Actually, some instances of $\exists$ can be interpreted in any category with finite limits: if $f$ is itself a monomorphism, then $f^*$ always has a left adjoint simply given by composition with $f$. On the logical side, this means that we can interpret "provably-unique existence" in any category with finite limits.  Logic with $\wedge$, $\top$, and "provably-unique-existence" is called _cartesian logic_ or _finite-limit logic_.

A [[coherent category]] is basically defined to be a regular category in which the subobject posets additionally have pullback-stable finite unions.  Thus, in a coherent category we can interpret so-called _coherent logic_, which adds $\vee$ and $\bot$ to regular logic.  Likewise, in an infinitary-coherent (or "geometric") category we can interpret _geometric logic_, which adds infinitary disjunctions $\bigvee_i \varphi_i$ to coherent logic.  Geometric logic is especially important because it is preserved by the inverse image parts of [[geometric morphism]]s, and because any geometric theory has a [[classifying topos]].

On the other hand, in a [[extensive category|lextensive category]], we do not have images or all unions, but if we have two subobjects of $A$ which are _disjoint_ (their intersection is initial), then their coproduct is also their union in $Sub(A)$.  Therefore, in a lextensive category we can interpret _disjunctive logic_, which is cartesian logic plus $\bot$ and "provably-disjoint disjunction."  Likewise, in an infinitary-lextensive category we can interpret "infinitary-disjunctive logic."

Finally, in a [[Heyting category]] the base change functors $f^*:Sub(B)\to Sub(A)$ also have right adjoints, usually written $\forall_f$, and it is easy to see that this implies that each $Sub(A)$ is also a [[Heyting algebra]], hence has an "implication" $\Rightarrow$ as well.  (We define "negation" by $\neg \varphi \equiv \varphi \Rightarrow \bot$.)  Thus, in a Heyting category we can interpret all of (finitary, first-order) [[intuitionistic logic]].

Now that we know how to interpret logic, we can say that a **model** of a given theory in $C$ consists of a choice of objects, morphisms, and subobjects for the types, function symbols, and relation symbols as above, such that for each axiom $\Gamma | \varphi \vdash \psi$, we have $[\varphi]\le [\psi]$ in $Sub([\Gamma])$.  Here, $[\Gamma]$ is the product of the objects that correspond to the types of the variables in $\Gamma$, $[\varphi]$ and $[\psi]$ are the interpretations of the formulas $\varphi$ and $\psi$ as subobjects of $[\Gamma]$, and $\leq$ is the relation of subobject inclusion.

It is easy to verify that a model of the theory of a group in $C$ is precisely an internal [[group]] object in $C$, as usually defined.  For instance, the validity of the axiom
$$x:G,y:G,z:G | \top \vdash m(m(x,y),z) = m(x,m(y,z))$$
 means that the [[equalizer]] of the two morphisms $G\times G\times G \to G$ must be all of $G\times G\times G$, or equivalently that those two morphisms must be equal.  The same happens in most other cases.


# Soundness and internal reasoning #

Internal logic is not just a way to concisely describe internal structures in a category, but also gives us a way to _prove_ things about them by "internal reasoning."  We simply need to verify that the "usual" methods of logical reasoning (for example, from $\varphi\vdash \psi$ and $\psi\vdash \chi$ deduce $\varphi\vdash\chi$) are _internally valid_, in the sense that if the premises are satisfied in some model $C$ (in the example, if $[\varphi]\le [\psi]$ and $[\psi]\le [\chi]$) then so is the conclusion (in the example, $[\varphi]\le [\chi]$).  This is called the _Soundness Theorem_.

It then follows that if we start from the axioms of a theory and "reason normally" within type theory, which in practice amounts to pretending that the types are sets, the function symbols are functions, and the relation symbols are subsets, then anything we prove will still be true when the theory is interpreted in an _arbitrary_ category, not just [[Set]].  For example, by easy equational reasoning from the theory of a group, we can prove that inverses are unique, which is expressed by the logical sequent
$$x:G,y:G,z:G | m(x,y)=e \;\wedge\; m(x,z)=e \vdash y=z.$$
It follows that this is also true, suitably interpreted, as a statement about internal group objects in _any_ category.

There are (at least) three caveats.  Firstly, we must take care to use only the rules appropriate to the fragment of logic that is valid in the particular categories we are interested in.  For example, if we want our conclusions to be valid in any regular category, we must restrict ourselves to reasoning "within regular logic."  Most mathematicians are not familiar with making such distinctions in their reasoning, but in practice most things one would want to say about a regular theory turn out to be provable in regular logic.  (We will not spell out the details of what this means.)  And once we are in a Heyting category, and in particular in a topos, this problem goes away and we can use full first-order logic.

The second, more important, caveat is that the internal logic of all these categories is, in general, [[constructive mathematics|constructive]]. This means that, among other things, the interpretation of $\neg\neg\varphi$ is, in general, distinct from that of $\varphi$, and that $\varphi\vee \neg\varphi$ is not always valid.  So even if we believe that classical logic (including the principle of [[excluded middle]] and even the [[axiom of choice]]) is "true," as many mathematicians do, there is still a reason to look for proofs that are constructively acceptable, since it is only these which are valid in the internal logic of most categories.  If the category is [[Boolean category|Boolean]] and/or satisfies the internal [[axiom of choice]], however, then this problem goes away, but these fail in many categories in which one wants to internalize (such as many [[Grothendieck topos]]es).

The third caveat is that one must take care to distinguish the _internal_ logic of a category from what is _externally_ true about it.  In general, internal validity is "local" truth, meaning things which become true "after passing to a [[cover]]."  This is particularly important for formulas involving _disjunction_ and _existence_.  For example, an object's being [[projective object|projective]] in the category $C$ is a different statement from its being _internally_ projective, meaning that "$X$ is projective" is true in the internal logic.  Another good example can be found in the different notions of [[finite object]] in a topos.  This problem goes away if the ambient category is [[well-pointed topos|well-pointed]], but well-pointed categories are even rarer than Boolean ones satisfying choice; the only well-pointed Grothendieck topos is [[Set]] itself.


# Completeness and syntactic categories  #

The converse of the Soundness Theorem is called the _Completeness Theorem_, and states that if a sequent $\varphi\vdash\psi$ is valid in every model of a theory, then it is _provable_ from that theory.  This is noticeably less trivial.  In classical first-order logic, where the only models considered are set-valued ones, the completeness theorem is usually proven using [[ultraproduct]]s.  However, in categorical logic there is a more elegant approach: from any theory $T$ we can construct a category, called its **syntactic category** $C_T$, containing a "generic" model of the theory, in which the valid sequents are precisely those provable from the theory.  It turns out that $C_T$ is precisely the category of [[context]]s described on the page [[context]].  Therefore, if a sequent is valid in all models, it is also valid in the generic model in $C_T$, and hence provable from $T$.

The syntactic category $C_T$ also has a universal property: any $T$-model in a category $D$ with suitable structure (regular, coherent, etc.) is the image of the generic model in $C_T$ under an essentially unique functor (of the appropriate type) $C_T\to D$.  In other words, the generic model is also the _initial_ model.

Furthermore, if $T$ lives in a sub-fragment of geometric logic (such as regular, coherent, lextensive, or geometric logic), then the [[Grothendieck topos]] of [[sheaf|sheaves]] on $C_T$ for its appropriate (regular, coherent, extensive, or geometric) [[coverage]] contains a $T$-model which is generic for models in Grothendieck toposes: any $T$-model in a Grothendieck topos is its image under the inverse image of a unique [[geometric morphism]].


# Kripke-Joyal semantics #

(to be written...)


# Higher-order logic #

(to be written...)


# References #

* Most books on topos theory develop some internal logic, at least in the context of a topos.  For example:

  * "Sheaves in Geometry and Logic" by Mac Lane and Moerdijk
  * "Topoi: the categorical analysis of logic" by Goldblatt 

* Part D of [[Elephant|Sketches of an Elephant]] is comprehensive.

* "Categorical Logic and Type Theory" by Jacobs works in the even more general context of [[Grothendieck fibration|fibrations]], allowing us to associate to each object $A$ an arbitrary poset instead of $Sub(A)$.

* Paul Taylor\'s book _[[Practical Foundations|Practical Foundations of Mathematics]]_ is arguably all about this subject (although you wouldn\'t know it until about Chapter VIII), but from a different perspective.  In particular, Taylor allows us to replace having *all* pullbacks with pullbacks along a pullback-stable class of _display morphisms_.
