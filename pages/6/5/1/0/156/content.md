
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


> This entry is about the notion of _skeleton_ in [[category theory]]. For the notion of (co)skeletal [[simplicial sets]] see at _[[simplicial skeleton]]_.

# Contents
* table of contents
{:toc}

## Definitions

### Skeleton of a Category

A [[category]] is __skeletal__ if objects that are [[isomorphism|isomorphic]] are necessarily [[equality|equal]].  (So this is a notion irredeemably violating the [[principle of equivalence]] of [[category theory]].)

A __skeleton__ of a category $C$ is defined to be a skeletal [[subcategory]] of $C$ whose [[inclusion functor]] exhibits it as 
[[equivalence of categories|equivalent]] to $C$. A __weak skeleton__ of $C$ is any skeletal category which is [[equivalence of categories|weakly equivalent]] to $C$.

In the absence of the [[axiom of choice]], it is more appropriate to define a __skeleton__ of $C$ to be a weak skeleton as defined above.

#### Existence of Skeletons of Categories

+-- {: .num_theorem}
###### Theorem

If the [[axiom of choice]] holds, then every category $C$ has a skeleton (in the strongest sense).
=--

+-- {: .proof}
###### Proof
Simply choose one object in each isomorphism class and one isomorphism to that object from each other object in that class.

In more detail, generate the full subcategory $sk(C)$ containing just the chosen objects. Denote by $in\colon sk(C)\to C$ the inclusion. We exhibit a weak inverse of $in$ as a functor
$-':x\mapsto x'$ constructed as follows. For every object $x$ one has chosen already the unique object $x'$ in $sk(X)$ isomorphic to $x$, but one also needs to make a choice of isomorphism $i_x\colon x\to x'$ for every $x$. This enables to conjugate between $C(x,y)$ and $C(x',y')$ by 

$$
(x\stackrel{f}\to y)\mapsto (x'\stackrel{i_x^{-1}}\to x\stackrel{f}\to y\stackrel{i_y}\to y').
$$ 

The rule for *morphisms* $-': f\mapsto f' := i_y\circ f\circ i_{x}^{-1}$ is clearly functorial. Let us show that $-'$ is a weak inverse of $in$. In one direction, given $y\in sk(C)$ we compute $(in_{y})' = y$ (strict equality); in another direction, given $x\in C$, notice that $i^{-1}_{in_{x'}}:in_{x'}\cong x$  for $x\in C$ is an isomorphism. It suffices to show that these isomorphisms for all $x\in C$ together form a *natural* isomorphism $i^{-1}_{in}:in_{-'}\to id_C$; the naturality diagram is commutative precisely because of the conjugation formula for the functor $-'$ for morphisms. This completes the proof that $-'$ is indeed a weak inverse of $in$.
=--

In fact, the statement that every (possibly [[small category|small]]) category has a skeleton is _equivalent_ to the axiom of choice if "subcategory" and "equivalence" have their naive ('strong') meanings.  For given a [[surjection]] $p:A\to B$ in $Set$, make $A$ into a category with a unique isomorphism $a\cong a'$ iff $p(a)=p(a')$; then a skeleton of $A$ supplies a splitting of $p$.

Even with the more general notion of weak or ana-[[equivalence of categories]], some amount of choice is required to show that every category has a skeleton.  It would be interesting to know the precise strength of the statement "every category is weakly equivalent to a skeletal one."  

### Skeletons as an Endo-Pseudofunctor on $\mathfrak{Cat}$

In the presence of choice we can thusly turn the process of taking the skeleton of a category into an endo-pseudofunctor on $\mathfrak{Cat}$, the $2$-category of categories.

For each category $\mathcal{C}$ let $sk_\mathcal{C}$ denote a skeleton of $\mathcal{C}$ and let $E_\mathcal{C}:sk_\mathcal{C}\simeq\mathcal{C}:E_\mathcal{C}^{\sim1}$ denote the skeletal equivalence at $\mathcal{C}$, with $\epsilon^{sk}_\mathcal{C}:E_\mathcal{C}\circ E^{\sim1}_\mathcal{C}\Rightarrow1_\mathcal{C}$ the skeletal transformation at $\mathcal{C}$. We define an endo-pseudofunctor 

$$
sk:\mathfrak{Cat}\to\mathfrak{Cat}
$$ 

as follows:

1. $sk(\mathcal{C})=sk_\mathcal{C},$
1. $sk(F:\mathcal{C}\to\mathcal{D})=E^{\sim1}_\mathcal{D}\circ F\circ E_\mathcal{C}:sk_\mathcal{C}\to\mathcal{C}\to\mathcal{D}\to sk_\mathcal{D},$
1. $sk(\alpha:F\Rightarrow G)=i\circ\alpha\circ i^{-1}:sk(F)\Rightarrow sk(G),$ where 
$$
i\circ\alpha\circ i^{-1}:sk(F)\Rightarrow sk(G)
$$ 
is defined by 
$$
(i\circ\alpha\circ i^{-1})_X=i_{G(X)}\circ\alpha_X\circ i_{F(X)}^{-1}:F(X)'\to F(X)\to G(X)\to G(X)'.
$$
1. For each category $\mathcal{C}$, the unitor $\iota^{sk}_\mathcal{C}:1_{sk(\mathcal{C})}\Rightarrow sk(1_\mathcal{C})$ is defined by
$$
\iota^{sk}_\mathcal{C}=1_{1_{sk(\mathcal{C})}},
$$
since
$$sk(1_\mathcal{C})=E^{\sim1}_\mathcal{C}\circ1_\mathcal{C}\circ E_\mathcal{C}=E^{\sim1}_\mathcal{C}\circ E_\mathcal{C}=1_{sk(\mathcal{C})}.$$
1. For each pair of composable functors $F:\mathcal{C}\to\mathcal{D}$, $G:\mathcal{B}\to\mathcal{C}$, the associator $\alpha^{sk}_{F,G}:sk(F)\circ sk(G)\Rightarrow sk(F\circ G)$ is defined by
$$
\alpha^{sk}_{F,G}=1_{E^{\sim1}_\mathcal{D}\circ F}\star\epsilon^{sk}_\mathcal{C}\star1_{G\circ E_\mathcal{B}}:E^{\sim1}_\mathcal{D}\circ F\circ E_\mathcal{C}\circ E_\mathcal{C}^{\sim1}\circ G\circ E_\mathcal{B}\Rightarrow E^{\sim1}_\mathcal{D}\circ F\circ G\circ E_\mathcal{B}.
$$

### Skeleton of an Indexed Category

Using the above definition, we can canonically define the skeleton of an indexed category.

Let $\psi:\mathcal{B}^{op}\to\mathfrak{Cat}$ be an indexed category. We define the **indexed skeleton of $\psi$**, denoted

$$
sk(\psi):\mathcal{B}^{op}\to\mathfrak{Cat},
$$

to be the indexed category given by postcomposing $\psi$ with $sk$, so $sk(\psi)=sk\circ\psi.$ That is, for each $I\in\mathcal{B}$ we take a skeleton $sk(\psi(I))$ of the category $\psi(I)$ indexed by $I$ with equivalence $E_I:\psi(I)\simeq sk(\psi(I)):E_I^{\sim1}$, we extend functors using the equivalences at various skeletons, and we extend natural transformations using skeletal isomorphisms in the codomain categories (although $\mathcal{B}^{op}$ has only identity $2$-cells since it's a promoted $1$-category, so the action on $2$-cells is trivial).

### Skeleton of a Fibered Category

Using the above definition and the [[Grothendieck construction]], we can define the skeleton of a fibration using the skeleton of an indexed category.

Let $p:\mathcal{E}\to\mathcal{B}$ be a fibration. We define the **fibered skeleton of $p$**, denoted 

$$
sk(p):sk^p_\mathcal{E}\to\mathcal{B}
$$

to be the Grothendieck completion of the indexed skeleton of the indexing by $p$. That is, $sk(p)$ is the fibration obtained by turning $p$ into an indexed category using the Grothendieck construction, taking the indexed skeleton of this indexed category, then turning the resulting skeletal indexed category back into a fibration (via the Grothendieck construction again). We refer to the total category $sk^p_\mathcal{E}$ in the resulting fibration as the **$p$-skeleton** of $\mathcal{E}$, which is different than $sk_\mathcal{E}$ since we have only skeletalized the fiber categories of our original fibration and not the total category of the original fibration. In general, we will have that 
$$
sk_\mathcal{E}\ncong sk^p_\mathcal{E},
$$
although they are trivially equivalent. As an example of this construction in action, we can pass from the monomorphism fibration on a category with pullbacks to the subobject fibration by taking the fibered skeleton. For details, see the subobject fibration section of [[codomain fibration]].

## Properties

### Skeletons without Choice

Without any choice, we have the following theorems.

+-- {: .num_theorem}
###### Theorem
Any [[thin category]] (i.e. any [[preordered set]]) has a weak skeleton.
=--
+-- {: .proof}
###### Proof
In this case, we can take the objects of the skeleton of $C$ to be the isomorphism classes of $C$.  If $C$ is thin, then we can define a partial ordering on its set of isomorphism classes, making them into a skeleton of $C$.
=--

+-- {: .num_theorem}
###### Theorem
Any two skeletons (in the strong sense) of a category are isomorphic.
=--
+-- {: .proof}
###### Proof
Let $\mathcal{C}$ be a category, with $sk (\mathcal{C})$ and $sk (\mathcal{C})'$ two skeletons of $\mathcal{C}$, and for each object $Y\in\mathcal{C}$ denote by $X_Y$ and $X_Y'$ respectively the unique objects in $sk (\mathcal{C})$ and $sk (\mathcal{C})'$ which are isomorphic to Y, and denote their respective isomorphisms by $i_Y:Y\to X_Y$ and $i_Y':Y\to X_Y'$. We define a functor $F:sk (\mathcal{C})\to sk (\mathcal{C})'$ by 
$$
F(X_Y)=X_Y',
$$
$$
F(f:X_Y\to X_Z)=i_Z'\circ i_Z^{-1}\circ f\circ i_Y\circ i_Y'^{-1}:X_Y'\to Y\to X_Y\to X_Z\to Z\to X_Z'.
$$
We then have 
$$
F(1_{X_Y})=i_Y'\circ i_Y^{-1}\circ 1_{X_Y}\circ i_Y\circ i_Y'^{-1}=i_Y'\circ i_Y^{-1}\circ i_Y\circ i_Y'^{-1}=i_Y'\circ1_Y\circ i_Y'^{-1}=i_Y'\circ i_Y'^{-1}=1_{X_Y'}=1_{F(X_Y)},
$$
$$
F(f:X_B\to X_C)\circ F(g:X_A\to X_B)=i_C'\circ i_C^{-1}\circ f\circ i_B\circ i_B'^{-1}\circ i_B'\circ i_B^{-1}\circ g\circ i_A\circ i_A'^{-1}
$$
$$
=i_C'\circ i_C^{-1}\circ f\circ i_B\circ 1_{B}\circ i_B^{-1}\circ g\circ i_A\circ i_A'^{-1}=i_C'\circ i_C^{-1}\circ f\circ i_B\circ i_B^{-1}\circ g\circ i_A\circ i_A'^{-1}
$$
$$
=i_C'\circ i_C^{-1}\circ f\circ1_{X_B}\circ g\circ i_A\circ i_A'^{-1}=i_C'\circ i_C^{-1}\circ f\circ g\circ i_A\circ i_A'^{-1}=F(f\circ g),
$$
so $F$ is a functor. The inverse $F^{-1}: sk (\mathcal{C})'\to sk (\mathcal{C})$ is defined in the obvious way, and is functorial by similar computations.
=--

Notice that the [[axiom of choice]] fails in general when one considers [[internal category|internal categories]].  Hence not every [[internal category]] has a skeleton. A necessary condition for an internal category $X_1 \rightrightarrows X_0$ to have a skeleton is the existence quotient $X_0/X_1$ - the object of orbits under the action of the core of $X$. If the quotient map $X_0 \to X_0/X_1$ has a section, then one could consider $X$ to have a skeleton, but this condition isn't sufficient for the induced inclusion functor to be a weak equivalence of internal categories when this makes sense (i.e. if the category is internal to a site).

+--{: .query}
[[David Roberts]]: The claim above about the necessity of the existence of the quotient needs to be checked.
=--

### Equivalents of Choice

Define a *coskeleton* of a category $C$ to be a skeletal category $S$ with a surjective equivalence $C\to S$.  In [[Categories, Allegories]] it is shown that the following are equivalent.

1. The axiom of choice holds.
1. Any two ana-equivalent categories are strongly equivalent.
   +-- {: .query}
   I removed 'non-ana', since I don\'t think that 'strongly equivalent' would ever be used in an 'ana-' sense.  ---Toby

   Addendum:  Actually, I don\'t know why I asked whether you meant weakly or strongly here, since obviously one can prove that two ana-equivalent categories are weakly equivalent!  It seems that the discussion above used the terms 'equivalence' and 'ana-equivalence' where [[equivalence of categories]] uses 'strong equivalence' and 'weak equivalence' or 'ana-equivalence'; so I just changed it.  And then I added another entry, which maybe you should remove if Freyd & Scedrov don\'t actually address it.  On the other hand, if they really talk about weak equivalence instead of ana-equivalence (although if they define it in elementary terms, it\'s hard to tell the difference), maybe there\'s no need to say 'ana-' at all on this page.
   =--
1. Any two weakly equivalent categories are strongly equivalent.
1. Every small category has a weak skeleton.
1. Every small category has a coskeleton.
1. Any two weak skeletons of a given small category are isomorphic.
1. Any two coskeletons of a given small category are isomorphic.

For convenience we add:

1. Given an inhabited family $\{S_i\}_I$ of equinumerous sets there exists $0 \in I$  and a family of isomorphisms of the permutation groups $\{Aut(S_0) \to Aut(S_i)\}_I$.
1. Given a family $\{S_i\}_I$ of inhabited equinumerous sets, there exists a family $(x_i)_I$ such that $x_i \in S_i$ for all $i \in I$.

### Uniqueness of Constructions

It is well-known that objects defined by [[universal property|universal properties]] in a category, such as [[limits]] and [[colimits]], are not unique on the nose, but only unique up to unique canonical isomorphism.  It can be tempting to suppose that in a *skeletal* category, where any two isomorphic objects are equal, such objects will in fact be unique on the nose.  However, under the most appropriate definition of "unique," this is *not* true (in general), because of the presence of automorphisms.

More explicitly, consider the notion [[cartesian product]] in a category.  Although we colloquially speak of "a product" of objects $A$ and $B$ as being the *object* $A\times B$, strictly speaking a product consists of the object $A\times B$ *together with* the projections $A\times B\to A$ and $A\times B\to B$ which exhibit its universal property.  Thus, even if the category in question is skeletal, so that there can be only one object $A\times B$ that is a product of $A$ and $B$, in general this object can still "be the product of $A$ and $B$" in many different ways.

For example, given any projections $A\times B\to A$ and $A\times B\to B$ that exhibit $A\times B$ as a product of $A$ and $B$, we can compose them both with any automorphism of $A\times B$ to get a new, different, pair of projections that also exhibit $A\times B$ as a product of $A$ and $B$.  In fact, the universal property of a product implies that any two pairs of projections are related by an automorphism of $A\times B$, so this example is generic.  Thus, even in a skeletal category, we cannot speak of "the" product of $A$ and $B$, except in the same [[generalized the|generalized sense]] that makes sense in any category.  A formal way to say this is that the "category of products of $A$ and $B$," while still *equivalent* to the [[trivial category]], as it is in any category with products, will not be *isomorphic* to the trivial category even when the ambient category is skeletal.

(It is true in a few cases, though, that skeletality implies uniqueness on the nose.  For instance, a [[terminal object]] can have no nonidentity automorphisms, so in a skeletal category, a terminal object (if one exists) really is unique on the nose.)




[[!redirects skeleton of a fibration]]
[[!redirects fibered skeleton]]
[[!redirects skeleta]]
[[!redirects skeletons]]
[[!redirects skeletal]]
[[!redirects skeletal category]]
[[!redirects skeletal categories]]