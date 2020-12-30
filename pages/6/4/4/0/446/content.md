
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##

In [[category theory]], an _allegory_ is a [[category]] with properties meant to reflect properties that hold in a category [[Rel]] of [[relations]]. The notion was first introduced (as far as we know) and certainly first made famous in the book _[[Categories, Allegories]]_ ([Freyd-Scedrov](#FreydScedrov)). 

Freyd and Scedrov argue that a categorical calculus of relations is an alternative and often more amenable framework for developing concepts traditionally couched in "functional" language (i.e., concepts which apply to [[sets]] and [[functions]]); for instance, a principal _raison d'etre_ for [[regular categories]] is precisely that one can do [[relational calculus]] in them (as had been long known, e.g., [[Saunders MacLane]] showed how to calculate with relations to do [[diagram chasing|diagram chases]] in [[abelian categories]]). Allegories, and correlative notions such as [[bicategory of relations|bicategories of relations]], also offer a smooth approach to [[regular and exact completion|regular and exact completions]], as used for example in the construction of [[realizability topos|realizability toposes]]. 

A signal feature of allegories is emphasis on the _modular law_ (see def. \ref{Allegory} below), which generalizes the [[modular lattice|modular law]] in lattices to more general relations, and which generalizes also so-called [[Frobenius reciprocity]] in [[categorical logic]]. 

## Definition


+-- {: .num_defn #Allegory}
###### Definition

An **allegory** is a [[locally posetal 2-category]] $A$ equipped with an [[involution]] $(-)^o \colon A^{op} \to A$ which is the [[identity]] on [[objects]], such that

1. the involution is order preserving and distributes over composition, i.e. $ (\psi\phi)^o = \phi^o\psi^o $,
1. each [[hom-object|hom-poset]] $A(x,y)$ has binary [[meet|meets]], and
1. the *[[modular lattice|modular law]]* holds: for $\phi\colon x\to y$, $\psi\colon y\to z$, and $\chi\colon x\to z$, we have $\psi \phi \cap \chi \le \psi (\phi \cap \psi^o \chi)$. 

=--

From these properties we immediately get that 
\[
(\phi \cap \psi)^o = \phi^o \cap \psi^o
\]
and
\[
  (\phi \cap \psi) \chi \leq \phi\chi \cap \psi\chi
\quad\text{and}\quad
  \chi (\phi \cap \psi) \leq \chi\phi \cap \chi\psi.
\]
\begin{proof}
The first claim follows from the observation that
$$
\begin{aligned}
    \chi \leq (\phi \cap \psi)^o
  &\iff
    \chi^o \leq \phi \cap \psi
&\quad&(.)^o\;\text{monotone and involutive}
\\
  &\iff
    \chi^o \leq \phi \; \text{ and } \; \chi^o \leq \psi
&&\text{meet properties}
\\
  &\iff
    \chi \leq \phi^o \; \text{ and } \; \chi \leq \psi^o
&&(.)^o\;\text{ monotone and involutive}
\\
  &\iff
    \chi \leq \phi^o \cap \psi^o
&&\text{meet properties.}
\end{aligned}
$$

For the claim $(\phi \cap \psi) \chi \leq \phi\chi \cap \psi\chi$ we use the [[horizontal composition]] in a [[locally posetal 2-category]], i.e. the fact that composition is monoton. Due to $\phi \cap \psi \leq \phi$ we get $(\phi \cap \psi)\chi \leq \phi\chi$. Analogously, we get that $(\phi \cap \psi)\chi \leq \psi\chi$. Hence $(\phi \cap \psi) \chi \leq \phi\chi \cap \psi\chi$. The claim $\chi (\phi \cap \psi) \leq \chi\phi \cap \chi\psi$ follows the the same arguments or by applying involution and the first claim.
\end{proof}

## Examples 

* If $C$ is a [[regular category]] and $Rel(C)$ is the [[locally posetal 2-category|locally posetal]]  [[bicategory]] of [[internal relation|internal relations]], then $Rel(C)$ is an allegory. 

* Any [[first-order hyperdoctrine with equality]] similarly gives rise to an allegory, as does any abstract [[bicategory of relations]] in the sense of Carboni-Walters. 

* Any [[modular lattice]] can be regarded as a one-object allegory if we take composition to be union and the involution to be the identity. 

## Maps, tabulations, and units

A __map__ $ r\colon x \to y $ in an allegory is a morphism that has a [[right adjoint]]. If $r \dashv s$, then $s = r^o$ (hint: use the modular law to show $r \dashv s \cap r^o$ and $r \cap s^o \dashv s$). 
The [[unit of an adjunction|unit of the adjunction]] $ id_x \leq r^o r $ entails that the morphism is __[[entire relation|entire]]__ (sometimes also called _total_) while the [[unit of an adjunction|counit of the adjunction]] $ r r^o \leq id_y $ states the fact hat the morphism is __[[functional relation|functional]]__ (sometimes also called _univalent_).

Any 2-category has a [[bicategory of maps]].  In an allegory, the ordering between maps is discrete, meaning that if $f \leq g$ then $f = g$.  Consequently, the bicategory of maps of an allegory is a [[category]].

A __tabulation__ of a morphism $\phi$ is a pair of maps $f,g$ such that $\phi = g f^o$ and $f^o f \cap g^o g = 1$.  An allegory is **tabular** if every morphism has a tabulation, and **pretabular** if every morphism is contained in one that has a tabulation.

Every [[regular category]], and indeed every [[locally regular category]], has a tabular allegory of internal binary relations.  Conversely, by restricting to the morphisms with left adjoints ("maps") in a tabular allegory, we obtain a locally regular category.  These constructions are inverse, so tabular allegories are equivalent to locally regular categories.

A locally regular category has finite products if and only if its tabular allegory of relations has top elements in its hom-posets.

Finally, a **unit** in an allegory is an object $U$ such that $1_U$ is the greatest morphism $U\to U$, and every object $X$ admits a morphism $\phi\colon X\to U$ such that $1_X\le \phi^o\phi$.  A locally regular category has a terminal object (hence is regular) if and only if its tabular allegory of relations has a unit.

Thus, regular categories are equivalent to unital (or unitary) tabular allegories.  For more details, see [[Categories, Allegories]] ([Freyd-Scedrov](#FreydScedrov)), the [[Elephant]] ([Johnstone](#Johnstone)), or [[toddtrimble:Theory of units and tabulations in allegories]].


## Division allegories 

A **union allegory** is an allegory whose hom-posets have finite joins that are preserved by composition.  Thus a union allegory is locally a [[lattice]].  If additionally it is locally a [[distributive lattice]], it is called a **distributive allegory**.  The category of maps in a unitary tabular union allegory is a [[coherent category]] (a "pre-logos"), and conversely the bicategory of relations in a coherent category is a (unitary tabular) distributive allegory.  In particular, every unitary tabular union allegory is distributive, but in the non-tabular case this can fail: for instance, any [[modular lattice]] can be regarded as a one-object union allegory and need not be distributive.

A **division allegory** is a distributive allegory in which composition on one (and therefore the other) side has a right adjoint (left or right division). That is: given $r: A \to B$ and $s \colon A \to C$, there exists $r/s: B \to C$ such that

$$t \leq s/r \in \hom(B, C) \Leftrightarrow t \circ r \leq s \in \hom(A, C)$$ 

(so that $- \circ r$ has right adjoint $-/r$: an example of a right [[Kan extension]]). Composition on the other side, $r \circ -$, has a right adjoint (an example of a right Kan lift) given by 

$$r\backslash u \coloneqq (u^o/r^o)^o.$$ 

In the bicategory of sets and relations, with notation as above, we have 

$$(s/r)(b, c) \dashv \vdash \forall_{a \colon A} r(a, b) \Rightarrow s(a, c)$$

where $r(a, b)$ is shorthand for "$(a, b)$ belongs to $r$". 

The category of maps (functional relations) of a unitary/unital tabular division allegory is a [[logos]], and conversely the bicategory of relations in a logos is a unitary tabular division allegory. ([Freyd-Scedrov](#FreydScedrov), 2.32, p. 227.) 

## Power allegories 

A **power allegory** is, *more or less*, an allegory $\mathcal{A}$ such that the inclusion functor $i: Map(\mathcal{A}) \to \mathcal{A}$ has a right adjoint $P$. The idea is that $P$ assigns to an object $A$ a power object $P(A)$, as in topos theory; if we summarize the notion of topos as a regular category $\mathbf{E}$ for which the inclusion $i: \mathbf{E} \to Rel(\mathbf{E})$ has a right adjoint $P$, then it becomes apparent that the notion of power allegory is similar except that it takes the "relation side" as primary and derives the "function side" as $Map(\mathcal{A})$, whereas in topos theory it's just the other way around. But in either case the adjunction $i \dashv P$ is fundamental. 

Since the inclusion $i$ is the identity on objects, the counit of the adjunction $i \dashv P$ at an object $B$ may be written 

$$\ni_B: P(B) \to B$$ 

and we have a kind of [[comprehension scheme]] that to each $r: A \to B$ there is a unique map $\chi_r: A \to P(B)$, the *characteristic map* of $r$, such that $r = \ni_B \circ \chi_r$. (If $A$ and $B$ are related by a property $r$, then for each $a$ there is a subobject $\chi_r(a)$ of $B$ consisting of elements $b$ so related to $a$.) In the case $r = 1_A: A \to A$, the characteristic map $\chi_{1_A}: A \to P(A)$ is called the *singleton map* of $A$, and more general $\chi_r$ may be defined as $P(r) \sigma_A$. 

### Freyd-Scedrov definition 

The exact definition of power allegory is a matter for consideration. One can get a certain distance just by adopting the naive definition suggested above, that a power allegory is nothing more than an allegory for which the inclusion $Map(\mathcal{A}) \to \mathcal{A}$ has a right adjoint $P$. (Below we introduce a similar notion that we call a $P$-allegory.) But it seems hard to develop a theory from the naive notion that rises to a level comparable to topos theory. 

Freyd and Scedrov start with a structure of division allegory (thus packing in a good amount of internal logic from the start) and introduce the fundamental adjunction $i \dashv P$ in terms of that structure. For them, a *power allegory* is defined to be a division allegory which associates to each object $B$ a morphism $\ni_B \colon P(B) \to B$ such that for all $r \colon A \to B$

* $1_A \leq (r \backslash \ni_B) \circ (\ni_B \backslash r)$ 

which expresses the truth of the formula $\forall_{a \colon A} \exists_{S: P(B)} \forall_{b \colon B} S \ni_B b \Leftrightarrow r(a, b)$, and 

* $(\ni_B \backslash \ni_B) \wedge (\ni_B \backslash \ni_B)^o \leq 1_{P(B)}$ 

which internalizes an axiom of extensionality, which reads $\forall_{b \colon B} (S \ni_B b) \Leftrightarrow (T \ni_B b) \vdash S = T$. Given those axioms, and given $r: A \to B$, one may define

$$\chi_r \coloneqq (\ni_B \backslash r) \wedge (r\backslash \ni_B)^o,$$ 

which internalizes the formula-definition $\chi_r(a, S) \coloneqq \forall_b S \ni_B b \Leftrightarrow r(a, b)$, and then show $\chi_r$ is a map. ([Freyd-Scedrov](#FreydScedrov), pp. 235-236.) 

The bicategory of relations in a [[topos]] is a power allegory; conversely, the category of maps in a unitary tabular power allegory is a topos. 

### Variant notion  

Nevertheless, the spare elegance of the naive definition gives one something to shoot for. It appears that quite a decent theory can be developed just by adding the assumption of coproducts in an allegory: a reasonable and fairly mild assumption. (Most allegories don't admit many colimits; for example having coequalizers is pretty rare. But the standard examples do have finite coproducts, coinciding with coproducts on the maps/functional side.) 

+-- {: .num_defn} 
###### Definition 
A $P$-allegory is an allegory $\mathcal{A}$ with finite coproducts[^1] for which the inclusion $i: Map(\mathcal{A}) \to \mathcal{A}$ has a right adjoint $P$. 
=-- 

[^1]: We mean coproducts as certain conical colimits *qua* [[locally posetal 2-category]]. 

As before, the counit is denoted $\ni: i P \to 1_{\mathcal{A}}$. It is perhaps surprising that the notion of $P$-allegory is at least as strong as power allegory in the Freyd-Scedrov sense: 

+-- {: .num_theorem} 
###### Theorem 
Any $P$-allegory is a division allegory in which the Freyd-Scedrov conditions on $\ni$ are satisfied. 
=-- 

+-- {: .proof} 
###### Proof (sketch) 
For now we content ourselves with a description of the division structure. 
Let $r: A \to C$ and $s: B \to C$ be morphisms; we construct a right Kan lift $s \backslash r$ of $r$ through $s$. This means that for all $t: A \to B$ we have $s \circ t \leq r$ if and only if $t \leq s \backslash r$. We begin by constructing the right Kan lift for the case $r = s = \ni_C: P C \to C$. 

Define the internal union $\bigcup_C$ by $\bigcup_C = P(\ni_C): P P C \to P C$, and define an internal order relation $[\Rightarrow]_C: P C \to P C$ by $P C \stackrel{\in_{P C}}{\to} P P C \stackrel{\bigcup_C}{\to} P C$. (Here $\in \coloneqq \ni^o$.) Define $[\Leftarrow]_C \coloneqq [\Rightarrow]_C^o$. 

We now show $[\Leftarrow]_C = \ni_C \backslash \ni_C$. That is, for $R: P C \to P C$, we show $\ni_C R \leq \ni_C$ is equivalent to $R \leq [\Leftarrow]$. The backward implication is easy; for the forward implication, one may prove it first for *reflexive* $R$ where we have an actual equation $\ni_C R = \ni_C$. It follows that $P(\ni_C) P(R) = P(\ni_C)$, whence $P(R) \leq \bigcup_C^o \bigcup_C$. A short calculation then yields $R = \ni_C P(R) \sigma_{P C} = \ni_C \bigcup_C^o \bigcup_C \sigma_{P C} = \ni_C \bigcup_C^o = [\Leftarrow]$. The case for general $R$ reduces to the reflexive case: form the reflexive completion $1 \vee R$ as the composite 

$$C \stackrel{\langle 1_{P C}, R \rangle}{\to} C + C \stackrel{\nabla}{\to} C$$ 

which is where coproducts come in; here $\nabla$ is the codiagonal and we use the fact that $C + C$ in an allegory is a biproduct to form the pairing for the first arrow. It is easy to show that $\ni_C(1 \vee R) = \ni_C \vee \ni_C R = \ni_C$, and then we derive $R \leq 1 \vee R \leq [\Leftarrow]$ from before. Thus we have shown $[\Leftarrow]_C = \ni_C \backslash \ni_C$. 

For general $r: A \to C, s: B \to C$, we claim the right Kan lift $s \backslash r: A \to B$ is given by $\chi_s^o (\ni_C \backslash \ni_C) \chi_r$. For, we have $r = \ni_C \chi_r$, whence 

$$
\begin{aligned}
    s t &\leq r & 
  \;&\iff & \ni_C \chi_s t &\leq \ni_C \chi_r 
\\ 
 &&& \iff & \ni_C \chi_s t \chi_r^o &\leq \ni_C 
\\ 
 &&& \iff & \chi_s t \chi_r^o &\leq \ni_C \backslash \ni_C 
\\ 
 &&& \iff & t &\leq \chi_s^o (\ni_C \backslash \ni_C) \chi_r
\end{aligned}
$$ 

thus proving the claim. 

Further details may be found [here](https://ncatlab.org/toddtrimble/published/Note+on+power+allegories). 
=--

Thus the notion of $P$-category is just as strong as the Freyd-Scedrov notion of power allegory, and one can then piggy-back on their further developments. 

## Syntactic allegories

Let $T$ be a [[regular theory]].  There is then an allegory $\mathcal{A}_T$ given as follows:

* the objects are finite strings of [[sorts]] of $T$;

* a morphism $\vec X \to \vec Y$ is a predicate $P(\vec x, \vec y)$ of sort $\vec X, \vec Y$ (or rather a provable-equivalence class of such predicates);

* the identity $\vec X \to \vec X$ is (named by) $x_1 = x_1 \wedge x_2 = x_2 \wedge \cdots \wedge x_n = x_n$;

* the composite of $R \colon \vec X \to \vec Y$ and $S \colon Y \to \vec X$ is named by $\exists \vec y. R(\vec x, \vec y) \wedge S(\vec y, \vec z)$.

That $\mathcal{A}_T$ is an allegory is B.311 in [Freyd--Scedrov](#FreydScedrov); that it is in fact unitary and pre-tabular is B.312.

Further structure on $T$ gives rise to further structure on $\mathcal{A}_T$ (B.313): if $T$ is a [[coherent theory|coherent]], [[first-order theory|first-order]] or [[higher-order logic|higher-order]] theory, then $\mathcal{A}_T$ will be a distributive, division or power allegory respectively.

Every pre-tabular allegory has a tabular completion, given by splitting its coreflexive morphisms (i.e. those endomorphisms $R$ such that $R \subset id$).  The category of maps in the coreflexive splitting of $\mathcal{A}_T$ is precisely the [[syntactic category]] of $T$.

### The existential quantifier

There are two possible ways to interpret a regular formula of the form $\exists y. R(x,y) \wedge S(y,z)$ in a unitary pre-tabular allegory, if $R$ and $S$ are interpreted as $r \colon X \to Y$ and $s \colon Y \to Z$ respectively:  as the composite $s \cdot r$, or more 'literally' by:

* pulling $r$ and $s^o$ back to the same hom set and taking their intersection: $(p_1^o r p_1) \cap (p_2^o s^o p_2) \colon X \times Z \to Y \times Y$;

* then forcing the two $Y$s to be equal by post-composing with $\Delta_Y^o \colon Y \times Y \to Y$, applying the existential quantifier by post-composing with the unique map $!_Y$ to the unit, and post-composing with $!_Z^o$ to get a morphism into $Z$;

* then forcing the $Z$ in the domain to be equal to the $Z$ in the codomain by taking the meet with $p_2 \colon X \times Z \to Z$;

* and finally pulling back along (precomposing with the right adjoint of) $p_1 \colon X \times Z \to X$ to get a morphism $X \to Z$.

We would like to know that these morphisms are equal, so that an existential formula will have a unique interpretation:

+-- {: .num_prop}
###### Proposition
$$ s r = (p_2 \cap !_Z^o !_Y \Delta_Y^o ((p_1^o r p_1) \cap (p_2^o s^o p_2))) p_1^o  $$
=--

+-- {: .proof}
###### Proof
We show inclusion in each direction.

Firstly, $s r = s r \cap p_2 p_1^o$, because the product projections tabulate the top morphism.  Notice also that the RHS above is equal to
$$ (\top_{Y Z} (r p_1 \cap s^o p_2) \cap p_2) p_1^o  $$
where $\top_{Y Z}$ is the top morphism $Y \to Z$.

Now we can calculate:
$$
\begin{aligned}
  s r \cap p_2 p_1^o
  & = (s r p_1 \cap p_2) p_1^o &\quad& \text{modular law} \\
  & = (s r p_1 \cap p_2 \cap p_2) p_1^o \\
  & \leq (s(r p_1 \cap s^o p_2) \cap p_2) p_1^o && \text{modular law} \\
  & \leq (\top_{Y Z} (r p_1 \cap s^o p_2) \cap p_2) p_1^o
\end{aligned}
$$

In the other direction, we have
$$
\begin{aligned}
  (\top_{Y Z} (r p_1 \cap s^o p_2) \cap p_2) p_1^o
  & \leq (\top_{Y Z} s^o (s r p_1 \cap p_2) \cap p_2) p_1^o 
&\quad& \text{modular law} \\
  & \leq (\top_{Y Y} (s r p_1 \cap p_2) \cap p_2) p_1^o
&& \top_{Y Z} s^0 \leq \top_{Y Y}\\
  & = (p_2 (p_1^o s r p_1 \cap p_1^o p_2) \cap p_2) p_1^o 
&& \top{Y Y} = p_2 p_1^o \\
  & = p_2 (p_1^o s r p_1 \cap p_1^o p_2 \cap p_2^o p_2) p_1^o
&& \text{modular law} \\
  & = p_2 (p_1^o s r p_1 \cap (p_1^o \cap p_2^o) p_2) p_1^o
&& \text{maps distribute} \\
  & = p_2 (p_1^o s r p_1 \cap \Delta p_2) p_1^o
&& \text{see below} \\
  & = p_2 \Delta (\Delta^o p_1^o s r p_1 \cap p_2) p_1^o
&& \text{modular law} \\
  & = (s r p_1 \cap p_2) p_1^o 
&& p_1 \Delta = p_2 \Delta = id \\
  & = s r \cap p_2 p_1^o
&& \text{modular law}
\end{aligned}
$$
and we are back to where we started.  In the fourth-last step we used the fact that if $p_1, p_2 \colon Z \times Z \to Z$ are the projections, then $p_1 \cap p_2 = \Delta^o$.  But $\Delta = \langle id, id \rangle$, and from lemma 1 [[finnlawler:allegory|here]] we have that $\langle id, id \rangle = p_1^o \cap p_2^o$.
=--

## Related entries

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[bicategory of relations]] (a special sort of [[cartesian bicategory]])

* [[1-category equipped with relations]]

Discussion of the relation between pretabular unitary allegories and bicategories of relations, and also between tabular unitary allegories and regular categories is in 

* [[toddtrimble:Theory of units and tabulations in allegories]]

## References

The standard monograph is 

* {#FreydScedrov}[[Peter Freyd]] and Andre Scedrov, _[[Categories, Allegories]]_, Mathematical Library Vol 39, North-Holland (1990). ISBN 978-0-444-70368-2.

The notion is discussed also in chapter A3 of

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]]_

In

* [[Bob Walters]], _Categorical algebras of relations_ ([blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) )

it is shown that any [[bicategory of relations]] is an allegory.

See also

* Wikipedia, _[Allegory](http://en.wikipedia.org/wiki/Allegory_%28category_theory%29)_

An introduction headed towards applications in computer science and, in particular, fuzzy controllers can be found in

* Michael Winter, _Goguen Categories_ (2007)


[[!redirects tabular allegory]]
[[!redirects union allegory]]
[[!redirects division allegory]]
[[!redirects power allegory]]

[[!redirects allegories]]
[[!redirects tabular allegories]]
[[!redirects union allegories]]
[[!redirects division allegories]]
[[!redirects power allegories]]
