

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A $k$-tuply monoidal $n$-category is an $n$-[[n-category|category]] in which [[objects]] can be multiplied in $k$ different ways, all of which [[interchange law|interchange]] with each other up to equivalence.  By the [[Eckmann?Hilton argument]], this implies that these $k$ ways all end up being equivalent, but that the single resulting operation is more and more commutative as $k$ increases.  The [[stabilization hypothesis]] states that by the time we reach $k = n + 2$, the multiplication has become "maximally commutative." 


While there is maybe no generally accepted definition of $k$-tuply monoidal $n$-category yet, it seems that defining it to be an $n$-category with an action of the [[little k-cubes operad]] makes good sense, as discussed further below. With this definition the stabilization hypothesis is a theorem at least for $(n,1)$-[[(n,1)-category|categories]] (see below).

By the [[delooping hypothesis]] a $k$-tuply monoidal $n$-category can be interpreted as a special kind of $(n+k)$-category. One may take this hypothesis as a definition, but it has been verified in many low-dimensional cases; see below.

## Definition

For purposes of this page, a __$k$-tuply monoidal $n$-category__ is a [[pointed object|pointed]] $(n+k)$-[[n-category|category]] such that any two parallel $j$-[[k-morphism|morphisms]] are [[equivalence|equivalent]] for $j \lt k$.  One usually relabels the $j$-morphisms as $(j-k)$-morphisms.  You may interpret this definition as weakly or strictly as you like, by starting with weak or strict notions of $(n+k)$-category.

The given point serves as an equivalence between $(-1)$-[[(-1)-morphism|morphisms]] (for now, see $(n,r)$-[[(n,r)-category|category]] for these), so there is nothing to say if $k \leq 0$ except that the category is pointed.  Thus we may as well assume that $k \geq 0$.  Also, according to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply monoidal $n$-category for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $n$-category.  Unlike the restriction $k\ge 0$,  this one is not trivial.

### Special cases

* A $0$-tuply monoidal $n$-category is simply a [[pointed object|pointed]] $n$-category, that is an $n$-category equipped with a chosen object.  

* A $1$-tuply monoidal $n$-category may be called simply a __[[monoidal n-category]]__. See 

  * [[monoidal category]]

* A **doubly monoidal** $n$-category is a __[[braided monoidal n-category]]. See

  * [[braided monoidal category]],
  * [[braided monoidal 2-category]].

* A __symmetric monoidal $n$-category__ is an $k$-tuply monoidal $n$-category for $k \geq n+2$. (This also called a _stably monoidal $n$-category_, but never a stable monoidal $n$-category.)

  That this is indeed independent of $k$, as soon as $k$ is large enough, is the statement of the [[stabilization hypothesis]], more on which below. 

  See

  * [[symmetric monoidal category]],
  * [[symmetric monoidal (∞,1)-category]].




## The periodic table

There is a [[periodic table]] of $k$-tuply monoidal $n$-categories:
<table markdown="1"><tr><th>$k$&#8595;\$n$&#8594;</th><th>$-1$</th><th>$0$</th><th>$1$</th><th>$2$</th><th>...</th></tr>
<tr><th>$0$</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed object in Cat|pointed category]]</td><td>[[pointed object in 2Cat|pointed 2-category]]</td><td>...</td></tr>
<tr><th>$1$</th><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>...</td></tr>
<tr><th>$2$</th><td>\"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>...</td></tr>
<tr><th>$3$</th><td>\"</td><td>\"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>...</td></tr>
<tr><th>$4$</th><td>\"</td><td>\"</td><td>\"</td><td>[[symmetric monoidal 2-category]]</td><td>...</td></tr>
<tr><th>&#8942;</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>&#8945;</td></tr></table>

### Historical notes ###

Originally the importance of pointedness was not fully appreciated, so any $n$-category was accepted as $0$-tuply monoidal, and $k$-tuply monoidal $n$-categories were identified simply with $(k-1)$-[[k-tuply connected n-category|simply connected]] $(n+k)$-categories (those in which any two parallel $j$-morphisms are equivalent for $j \lt k$).  See [[periodic table]] for this original.

## Low dimensions

### $k=0$

As remarked above, a $0$-tuply monoidal $n$-category is just a pointed one, and functors and transformations between such are required to preserve the chosen object, at least up to specified coherent isomorphism.  (In other words, the $(n+1)$-category of $0$-tuply monoidal $n$-categories is the co-slice $(n+1)$-category $1/n Cat$, where the slicing happens in a suitably weak $(n+1)$-sense.

### $k=1$, $n=0$ 

A 1-tuply monoidal 0-category is a pointed 0-connected 1-category, or a 1-category with a chosen object in which all objects are isomorphic.  Thus we might as well as assume there is exactly one object, in which case we just have a [[monoid]].  A functor between one-object categories, which preserves the basepoint automatically, is exactly a monoid [[homomorphism]].

More interestingly, a natural transformation between functors $f,g:X\to Y$ between one-object categories is just an object $y\in Y$ (its component at the single object) such that $f(x) y = y g(x)$ for all $x\in X$.  So the 2-category of 0-connected 1-categories is not equivalent to the 1-category of monoids.  However, a _pointed_ natural transformation must have its component at the basepoint being the identity; thus $y=1$ and so the only such natural transformations are identities $f=g$.  Therefore, the 2-category of pointed 0-connected 1-categories (that is, 1-tuply monoidal 0-categories) is equivalent to the 1-category of monoids.

### $k=2$, $n=0$

A 2-tuply monoidal 0-category is a pointed 1-connected 2-category.  Interpreting things as weakly as possible, we are talking about a [[bicategory]] $B$ with one object $*$ and one 1-cell (its identity).  By the usual [[Eckmann-Hilton argument]], the set $B(1_*,1_*)$ is a commutative monoid, but there is also additional structure: the associatior and unitors of the bicategory.  The pentagon identity implies that the associator is the identity, and the unitor axioms imply that the two unitors are the same, but they are not necessarily the identity.  Therefore, a 1-connected 2-category (if by 2-category we mean bicategory) is a commutative monoid $X$ equipped with a chosen invertible element $d_X$.  This was apparently first observed by [[Tom Leinster]].

In similar vein, one can work out (see Cheng--Gurski):

* a (weak) functor between 1-connected bicategories is a monoid homomorphism $F:X\to Y$ equipped with a distinguished invertible element $m_F\in Y$.
* a (weak) natural transformation between two monoid homomorphisms is just the assertion that they are equal (and thus, every such transformation is invertible).
* a modification between two such transformations is a distinguished not-necessarily-invertible element $\Gamma\in Y$.

Note that the invertible elements $d_X$ and $m_F$ play no role in the definition of the higher morphisms, so they might as well not be there, up to equivalence.  However, the nonidentity modifications do screw things up, so the tricategory of 1-connected bicategories is not equivalent to the 1-category of commutative monoids.  But if we add in the basepoints, then we get:

* a pointed 1-connected bicategory is one equipped with a functor from $1$, the terminal bicategory.  This is just a monoid homomorphism $1\to X$, which of course is unique, together with a distinguished invertible element in $X$ which we can ignore.  Thus every 1-connected bicategory can be pointed in an essentially unique way.

* a pointed functor between two pointed 1-connected bicategories is a functor $F:X\to Y$ together with a weak natural equivalence, say $t_F$, between $1\to X\to Y$ and $1\to Y$.  Since these are always equal as monoid homomorphisms, there is always a unique (invertible) transformation connecting them, so such a pointed functor is just a monoid homomorphism $F:X\to Y$.

* a pointed transformation from $F$ to $G$ is a transformation $a$ from $F:X\to Y$ to $G:X\to Y$ together with an invertible modification, say $c_a$, relating $a t_F$ to $t_G$.  In other words, it is an assertion that $F=G$ together with a distinguished invertible element $\Gamma_a$ of $Y$.

* a pointed modification from $a$ to $b$ is a modification $m$ such that $m c_a = c_b$.  In other words, it is a distinguished element $\Lambda\in Y$ such that $\Lambda \Gamma_a = \Gamma_b$, or $\Lambda = \Gamma_a^{-1} \Gamma_b$ since $\Gamma_a$ is invertible.  Thus, any two pointed transformations $F\to G$ are related by a unique invertible modification.

We conclude that the tricategory of pointed 1-connected bicategories is equivalent to the category of commutative monoids and monoid homomorphisms, so again the delooping hypothesis is verified.

One might complain that in addition of the single weak natural equivalence $t_F$, $F$ ought also to be equipped with an inverse _adjoint_ equivalence for it.  The modifications involved in this would introduce two distinguished invertible elements in $Y$, which (by the triangle identities) would have to be each other's inverses.  But these elements would again play no role in the higher morphisms, so they might as well be identities.

### $k=1$, $n=1$

A 1-tuply monoidal 1-category is a pointed 0-connected 2-category, which we can identify with a bicategory with one object.  It is well-known that this is precisely the data of a monoidal category. Likewise, (weak) functors between such bicategories correspond precisely (strong) monoidal functors.  However, again the transformations and modifications screw things up in the merely connected case, but by using pointed objects instead we can remedy the situation.

### $k=1$, $n=(\infty,0)$

If we identify $\infty$-[[infinity-groupoid|groupoids]] with spaces, then a 1-tuply monoidal $(\infty,0)$-category, or a monoidal $\infty$-groupoid, can be identified intuitively with an $A_\infty$-[[A-infinity-space|space]].  This is a space equipped with a multiplication which is associative and unital up to all higher homotopies; see [[operad]] for one way to encode these data.

It is a well-known fact in homotopy theory that the homotopy theories (that is, $(\infty,1)$-[[(infinity,1)-category|categories]]) of based connected spaces and of grouplike $A_\infty$-spaces are equivalent, via the [[loop space]] and [[classifying space]] constructions.  This can be regarded as another version of the delooping hypothesis.  The "grouplike" restriction (meaning that $\pi_0$ is a group, or that the multiplication has inverses up to homotopy) is because we consider only based connected $(\infty,0)$-categories, whereas we would need based connected $(\infty,1)$-categories to recover all $A_\infty$-spaces.  It would be interesting to verify the hypothesis in this case using one of the known models for $(\infty,1)$-categories.

### $n = (\infty,0)$ and $\infty$-stacks {#InfStackCase}

A $k$-tuply monoidal [[∞-groupoid]] may be identified, under $k$-fold [[delooping]], with a $(k-1)$-[[connected]] $\infty$-groupoid. This statement holds in fact even for _parameterized $\infty$-groupoids_, i.e. for [[∞-stack]]s.

+-- {: .un_theorem}
###### Theorem (k-tuply monoidal $\infty$-stacks)

Let $k \gt 0$, let $\mathcal{X}$ be an [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathcal{X}_*^{\geq k}$ denote the full [[sub-(∞,1)-category]] of the category $\mathcal{X}_{*}$ of pointed objects, spanned by those pointed objects thar are $k-1$-[[connected]] (i.e. their first $k$ [[homotopy groups in an (∞,1)-topos|∞-stack homotopy groups]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathcal{X}_*^{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathcal{X}) \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EKAlg, theorem 1.3.6.]].

=--

Specifically for $\mathcal{X} = Top$, this reefines to the classical theorem by [[Peter May]]

+-- {: .un_theorem}
###### Theorem 
**(May recognition theorem)**

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $X$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

+-- {: .proof}
###### Proof

This is [[Ek-Algebras|EkAlg, theorem 1.3.16.]]

=--


### $n = (n,1)$ and the stabilization hypothesis {#Inf1Case}

An [[(n,1)-category]] is a $n$-[[truncated]] [[(∞,1)-category]]

In [John Francis' PhD thesis](http://dspace.mit.edu/handle/1721.1/43792) (reference _EnAction_ below ) the theory of [[(∞,1)-categories]] equipped with an action of the [[little k-cubes operad]] is established, so that

* $(\infty,1)$-categories with an $E_1$-action are precisely [[monoidal (∞,1)-categories]]  -- 1-fold monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_\infty$-action are precisely [[symmetric monoidal (∞,1)-categories]] -- $\infty$-tuply monoidal $(\infty,1)$-categories;

* $(\infty,1)$-categories with an $E_n$-action for $1 \lt n \lt \infty$ are the corresponding $k$-tuply monoidal $(\infty,1)$-categories in between.


+-- {: .un_prop}
###### Proposition
**(stabilization for $(n,1)$-categories)


Equipping an [[(n,1)-category]] of $k$ compatible monoidal structures for $k \geq n + 2$ (which is the same as equipping it with a [[little k-cubes operad]] action) is the same as equipping it with the structure of a [[symmetric monoidal (∞,1)-category|symmetric monoidal (n,1)-category]].

=--


An aspect of this was demonstrated in terms of [[Tamsamani n-categories]] in

* [[Carlos Simpson]], _On the Breen-Baez-Dolan stabilization hypothesis for Tamsamani's weak $n$-categories_ ([arXiv:math/9810058](http://arxiv.org/abs/math/9810058))

A proof of the full statement in terms of [[quasi-categories]] is sketched in
[section 43.5](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf#page=187) of 

* [[André Joyal]], _Notes on quasi-categories_ ([pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf)).

Probably the first full proof in print is given in

* [[Jacob Lurie]], _[[Ek-Algebras]]_ ,

where it appears in example 1.2.3 as a direct consequence of a more general statement, corollary 1.1.10.

### Other low-dimensional cases

One expects that 

* pointed 2-connected tricategories can be identified with commutative monoids (again),
* pointed 1-connected tricategories can be identified with braided monoidal categories,
* pointed 0-connected tricategories can be identified with monoidal bicategories,
* and so on.


## References 

Some discussion of the peridodic table is in 

* [[Eugenia Cheng]], [[Nick Gurski]],  The periodic table of n-categories for low dimensions I: degenerate categories and degenerate bicategories.  [arXiv:0708.1178](http://arxiv.org/abs/0708.1178).

* [[John Baez]] and [[Mike Shulman]],  Lectures on $n$-categories and cohomology.  [arXiv:math.CT/0608420](http://arxiv.org/abs/math.CT/0608420).


The theory of $k$-tuply monoidal [[(∞,1)-categories]] was maybe first studied in

* **EnAction** [[John Francis]] PhD thesis ([web](http://dspace.mit.edu/handle/1721.1/43792))

and later further developed in

* [[Jacob Lurie]], _[[Ek-Algebras]]_
 
where also the proof of the [[stabilization hypothesis]] in this context is noticed.


## Discussion

A previous version of this entry led to the following discussion

+--{: .query}

[[Mike Shulman]]: I would like to suggest that we switch to using _symmetric monoidal_ rather than _stably monoidal_, and especially avoid calling these just _stable_.  One advantage of "symmetric monoidal" is that it has a well-established meaning in low-dimensions; if I say "symmetric monoidal $n$-category" then people who are familiar with symmetric monoidal 1-categories are more likely to have an intuitive understanding of what I mean than if I say "stably monoidal $n$-category."

Use of the word "stable" here also creates confusion with its other meanings (see [here](http://golem.ph.utexas.edu/category/2009/01/benzvi_on_geometric_function_t.html#c021217) and [here](http://golem.ph.utexas.edu/category/2009/01/categories_logic_and_physics_i_2.html#c021205)).  Algebraic topologists often use "stable" to mean "related to [[spectrum|spectra]]," and spectra are related to, but distinct from, symmetric monoidal $\infty$-groupoids.  (<i>Connective</i> spectra can be identified with symmetric _groupal_ $\infty$-groupoids.)  Lurie is also using "stable $(\infty,1)$-category" to mean "an $(\infty,1)$-category which behaves like the $(\infty,1)$-category of spectra."  One might not like this, but it is not original with him; several other algebraic topologists use "stable model category" in the same sense.  And since we have the perfectly good alternative term "symmetric monoidal" to use here, which has other things to recommend it as well, why create needless confusion?

_Toby_:  Hopefully John will admit that saying 'stable' instead of 'stably monoidal' (or 'stably groupal') was a slip of the tongue ... pen ... fingers.  I\'m used to 'stably monoidal', and I don\'t think that it should cause confusion ---if used in full.  Also, I think there\'s some historical confusion about 'symmetric monoidal $2$-category' or maybe 'symmetric monoidal $3$-category' that 'stably monoidal' isn\'t subject to, although that\'s a bit parochial.

=--


[[!redirects k-tuply monoidal n-categories]]