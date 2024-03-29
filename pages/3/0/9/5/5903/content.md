
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

*Note: This page is about [[categories]] (in the sense of [[category theory]]) built out of [[syntax]], i.e. "term models".  The phrase "syntactic category" is also sometimes used to mean a grouping of syntactic objects, so that e.g. [[terms]] belong to one syntactic category and [[formulas]] to another. For this usage, see also [[categorial grammar]].*

# Contents
* table of contents
{: toc}

## Idea

As described at [[relation between type theory and category theory]], for many kinds of [[logic]] and [[type theory]] there is an [[adjunction]] or [[equivalence]]

$$ Theories \;\rightleftarrows\; Categories $$

where on the left we have a [[category]] or [[2-category]] of [[theories]] of some sort (i.e. in some [[doctrine]]), and on the right we have a category or 2-category of categories with some structure (e.g. finite [[limits]], [[cartesian closed category|cartesian closure]], etc.).

The **syntactic category** construction is the functor from theories to categories, denoted $Syn$ or $Con$.  Given a theory, it generates the [[walking structure|walking]] model of that theory, i.e. a structured category of the appropriate sort which is generated by a model of that theory.  Since the objects of the syntactic category are frequently taken to be the [[contexts]] in the theory, the syntactic category is also called the **category of contexts**.

The functor in the other direction associates to any category its [[internal logic]].

## Definition

Given a [[type theory]] $T$, its **syntactic category** or **category of contexts** $Con(T)$ is defined as follows.

* Its [[objects]] are the [[contexts]] in the type theory;

* Its [[morphisms]] between contexts are **[[substitutions]]**, or **interpretations** of [[variables]]. 

A morphism from the context $\Gamma$ to the context $\Delta$ consists of a way of fulfilling the assumptions required by $\Delta$ by appropriately interpreting those provided by $\Gamma$, generally by substituting terms available in $\Gamma$ for variables needed in $\Delta$ and proving whatever is necessary from the assumptions at hand.

More precisely, let $\Gamma$ and $\Delta$ be contexts of some [[type theory]] $T$ of the form
$$\Gamma \;=\; x_0:A_0,\; x_1:A_1(x_0),\; x_2:A_2(x_0,x_1),\;\dots x_n:A_n(x_0,\dots,x_{n-1})$$
and
$$\Delta \;=\; y_0:B_0,\; y_1:B_1(y_0),\; y_2:B_2(y_0,y_1),\;\dots y_m:B_m(y_0,\dots,y_{m-1})
  \,.
$$

(Here we allow the possibility that each type in these contexts [[dependent type|depends]] on the variables occurring earlier in the context, but for simplicity we can ignore that. )

Then a [[morphism]] $\Gamma \to \Delta$ in the category of contexts $Con(T)$ consists of a sequence of terms such as the following:
$$
\begin{aligned}
\Gamma &\vdash t_0 :B_0\\
\Gamma &\vdash t_1 : B_1(t_0)\\
\vdots\\
\Gamma &\vdash t_m : B_m(t_0,t_1,\dots, t_{m-1})
\end{aligned}
$$
In other words, to give such a morphism we must give, for each type (or assumption) required by $\Delta$, a way to construct an element of that type (or a proof of that assumption) out of the data and assumptions contained in $\Gamma$.

+-- {: .query}
This might fit better after the motivating examples below; but maybe those examples don\'t make sense to a newcomer.  This is incomplete, however, since it doesn\'t address contexts that include propositional hypotheses.  ---Toby
=--


## Properties

### Structure

Depending on the type-forming operations available in $T$, the category $Con(T)$ will have categorical structure.  Roughly:

* If $T$ has [[function types]], then $Con(T)$ is [[cartesian closed category]].
* If $T$ has [[sum types]], then $Con(T)$ has binary [[coproducts]].
* If $T$ is a [[dependent type theory]] with [[dependent product types]], then $Con(T)$ is a [[locally cartesian closed category]].
* If $T$ is a [[regular theory]], then $Con(T)$ is a [[regular category]].
* If $T$ is a [[coherent theory]], then $Con(T)$ is a [[coherent category]].
* If $T$ is a [[geometric theory]], then $Con(T)$ is a [[geometric category]].
* If $T$ is a finitary [[first-order theory]], then $Con(T)$ is a [[Heyting category]].

And so on.  (If $T$ lacks [[eta-conversion]], then this categorical structure may only be "weak".)  One thing worth noting is that

* $Con(T)$ always has finite [[products]].

This is due to the objects of $Con(T)$ being contexts rather than types.  A way to avoid this is to work instead with a syntactic [[cartesian multicategory]].

In fact, $Con(T)$ is not just a structured category, it is a [[split model of type theory]] in any of the senses described there.  In constructing formally an internal logic that involves dependent types, this is important to keep track of.


### Universal property
 {#UniversalProperty}

The syntactic category $Con(T)$ has the [[universal property]] that for $C$ any suitable category, [[functors]]

$$
  Con(T) \to C
$$

that preserve the relevant structure correspond to [[categorical semantics|interpretations]] of $T$ in $C$.

The construction 

$$
  Con\colon TypeTheories \to Categories
$$

is the [[left adjoint]] in an [[adjunction]] that [[relation between type theory and category theory|relates type theories and categories]], whose [[right adjoint]] $Lan : Categories \to TypeTheories$ extracts the [[internal logic]] of a category.

Accordingly, the [[counit of an adjunction|adjunction counit]] evaluated on any category $C$

$$
  Con(Lan(C)) \to C
$$

says that there a canonical interpretation of the internal logic of a category $C$ in $C$ itself, while the [[unit of an adjunction|unit]] evaluated at a theory $T$:

$$ T \to Lan(Con(T)) $$

says that there is a canonical interpretation of $T$ in the internal logic of its syntactic category.


## Examples

### Substitution and introduction of a single term
 {#SubstitutionAndIntroductionOfTerm}

Given a context $\Gamma$ and a [[type]] $X$, there is a new context $[\Gamma, x : X]$.

Given a [[term]] $t : X$ there is a canonical morphism of contexts

$$
  \Gamma \stackrel{[t/x]}{\to} [\Gamma, x : X] 
$$

which picks that term in $X$. The [[base change]] functor along this morphism

$$
  [t/x]^* : Con(T)_{/[\Gamma, x : X]} \to Con(T)_{/\Gamma}
$$

is the operation of _[[substitution]] of [[variables]]: it sends a [[dependent type]] $\Gamma, x : X \vdash P(x)$ to $\Gamma \vdash P(t)$.

There is also the canonical morphism of contexts

$$
  \hat x : [\Gamma, x : X] \to \Gamma
$$

which simply forgets the type $X$. The [[base change]] along this morphism is the context extension functor

$$
  \hat x^* : Con(T)_{/\Gamma} \to Con(T)_{/[\Gamma , x : X]}
  \,.
$$

Its [[right adjoint]] is the [[dependent product]] functor $\prod_{x : X}$ giving the [[universal quantifier]] $\forall_{x : X}$, and its [[left adjoint]] is the [[dependent sum]] functor $\sum_{x : X}$ giving the [[existential quantifier]] $\exists_{x :X}$.


### The theory of a group
{#group}

For example, consider these contexts in the theory of a group $G$:
$$ \Gamma \;=\; a\colon G,\; b\colon G $$
$$ \Delta \;=\; a\colon G,\; b\colon G,\; (a b)^2 = a^2 b^2 $$
$$ E \;=\; a\colon G,\; b\colon G,\; a b = b a $$
$$ Z \;=\; x\colon G,\; y\colon G $$

One interpretation of $\Gamma$ in $\Delta$ (that is, a morphism from $\Delta$ to $\Gamma$) is given by the substitution
$$ a \coloneqq a,\; b \coloneqq b .$$
The fact that $(a b)^2 = a^2 b^2$ in $\Delta$ is ignored.  In type-theoretic language, this would consist of the two terms
$$\begin{aligned}
a\colon G,\; b\colon G,\; (a b)^2 = a^2 b^2 &\vdash a:G\\
a\colon G,\; b\colon G,\; (a b)^2 = a^2 b^2 &\vdash b:G
\end{aligned}
$$
Note that in this way of presenting things, the names of the variables in $\Gamma$ do not appear; only the order in which the types appear in $\Gamma$ matters.

A less obvious interpretation of $\Gamma$ in $\Delta$ is the substitution
$$ a \coloneqq b,\; b \coloneqq a .$$
There is no reason to keep variable names the same.  (At this point, compare $\Gamma$ and $Z$; when the definition is complete, it ought to follow that these are isomorphic.)

Another, perhaps even less obvious, morphism $\Delta \to \Gamma$ is
$$ a \coloneqq a^2,\; b \coloneqq a^3 .$$
Not only does this ignore that $(a b)^2 = a^2 b^2$; it also ignores the very existence of $b$ in $\Delta$.  (It also uses the existence of $a$ more than once.  Ignoring and reusing information like this is not always allowed in substructural logics such as [[linear logic]].)

We can interpret $E$ in $\Delta$ without renaming variables because the theory of a group allows us to derive the judgment
$$ a\colon G,\; b\colon G,\; (a b)^2 = a^2 b^2 \;\vdash\; a b = b a. $$
That is, we get a morphism from $\Delta$ to $E$ by performing the substitution
$$ a \coloneqq a,\; b \coloneqq b $$
and then inserting a proof of the above judgment.  As it happens, the argument in such a proof is reversible, so you should expect that $\Delta$ and $E$ are also isomorphic.

Are there any morphisms from $\Gamma$ to $\Delta$?  The obvious substitution does not define a morphism, since the required fact cannot be proved.  However, you get one using the substitution
$$ a \coloneqq a,\; b \coloneqq a $$
and then inserting a proof that
$$ \Gamma \;\vdash\; (a a)^2 = a^2 a^2 .$$
All the same, we would not want to say that $\Gamma$ and $\Delta$ are isomorphic contexts; although there are morphisms in each direction, composing them should never produce identity morphisms on both sides.

The category structure of $Con(T)$ can be seen explicitly as well.  First, given a context $\Gamma$, there is an obvious **[[identity morphism|identity]]** morphism where every variable is substituted for itself and every statement assumed is proved immediately from itself.

Given morphisms $\Gamma \overset{f}\to \Delta \overset{g}\to E$, form the **[[composite]]** as follows:  First, for each variable $X$ required by $\Gamma$, $f$ tells us how to substitute a term $T$ built out of the variables in $\Delta$, while $g$ tells us how to substitute a term from $E$ for each of these variables.  So in the end, $X$ is expressed as a term $T[g]$ involving variables available in $E$.  Also, by combining the proofs provided by $f$ and $g$, we get the proofs required for their composite.

To really complete the definition of a category, I should also describe when two morphisms $\Gamma \to \Delta$ are **[[equality|equal]]**.  There are actually many options here; the most strict is to say that they are equal only if the substitutions and proofs used are syntactically identical, and the most weak is to say that any parallel morphisms are equal.  Neither of these is very useful; for purposes of this example, let us require only that the expressions substituted for each variable $X$ in $\Gamma$ can be proved equal in the context $\Delta$.

Now you should be able to prove that composition satisfies the axioms of a [[category]].

Notice that the exact definition of equality of morphisms can depend heavily on the theory in question and your own purposes.  For example, this definition makes sense only because we have a notion of proving equality of elements of a group.  Also, you can sometimes place interesting conditions on whether two proofs count as equivalent, rather than requiring either syntactic identity or (as we do here) accepting proof irrelevance.

+-- {: .num_example}
###### Exercise
Now that the category of contexts (in one sense) of the theory of a group has been completely defined, describe that category (up to [[equivalence of categories|equivalence]]) in terms familiar to an algebraist.  In particular, compare it to the [[Grp|category of groups]].
=--

+-- {: .proof}
###### Answer
In [rot13](http://www.rot13.com/) (so that you have a chance to think about it yourself without accidentally seeing the answer): gur bccbfvgr bs gur pngrtbel bs svavgryl cerfragrq tebhcf.
=--

The result of this [[exercise]] is true in more generality: it works for any finite-limit theory; see in particular [[Lawvere theory]].  Presumably there are also infinitary generalizations.  There's some general discussion in the [[Elephant]].


## Variations

### Cartesian multicategories

Instead of a syntactic category, for a non-dependent type theory one can construct instead a syntactic [[cartesian multicategory]] (or, in the case of a [[linear logic|linear]] type theory, a plain (symmetric) [[multicategory]]).  This avoids the need to take the objects to be contexts rather than single types.

### The syntactic site

For some doctrines, the syntactic category of any theory is naturally equipped with the structure of a [[site]].  For instance, if $T$ is a regular, coherent, or geometric theory, then $Con(T)$ is a regular, coherent, or geometric category, which comes with a naturally defined topology.  When equipped with this topology, the syntactic category is called the **syntactic site**.

In each of these cases, the [[category of sheaves]] on the syntactic site is the [[classifying topos]] of the theory.  In other words, it has the universal property that for any [[Grothendieck topos]] $\mathcal{E}$, [[geometric morphism]]s $\mathcal{E} \to Sh(Con(T))$ are equivalent to [[model]]s of the [[theory]] $T$ in $\mathcal{E}$.

## Related concepts

* More or less the same concept is that of _[[term model]]_.

* [[free topos]]

## References

Sections D4.1 and D4.4 of 

* [[Peter Johnstone]], _[[Sketches of an elephant]]_, 
 {#Johnstone}

A description of the construction of the category of contexts is in

* Andrew Pitts, _Categorical logic_, In Handbook of Logic in Computer Science, volume 5, pages 39&#8211;128. Oxford University Press (2001)

Another description, via [[sketches]], is in chapter VIII of

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_, 

A review of this is around [section 2.8](http://www.paultaylor.eu/ASD/foufct/cattype.html) of 

* [[Paul Taylor]], _Foundations for computable topology_ ([webpage](http://www.paultaylor.eu/ASD/foufct/abstract.html))
 {#Taylor}


[[!redirects syntactic category]]
[[!redirects syntactic categories]]
[[!redirects syntactic site]]
[[!redirects syntactic sites]]
[[!redirects category of contexts]]
[[!redirects categories of contexts]]
