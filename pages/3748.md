
#Contents#
* table of contents
{:toc}

## Idea ## 

A club is a particular sort of [[doctrine]] or [[monad]] on [[categories]], one which encapsulates the following frequently observed phenomenon: to describe [[free functor|free]] algebras $F(C)$ with respect to the monad, it frequently suffices to describe the free algebra $F(1)$ on the [[terminal category]], and then a certain "[[categorical wreath product]]" gives the free algebra on $C$: 

$$F(C) \cong F(1) \wr C$$

Examples of this phenomenon include the monad for [[monoidal categories]], [[symmetric monoidal categories]], [[braided monoidal categories]], categories with finite [[product]]s, [[closed category|closed symmetric monoidal categories]], and many others.

Clubs were introduced by [[Max Kelly]] in a series of papers (see references), and are akin in spirit to [[operad|operads]].  In fact, many (perhaps even all) types of clubs are a special case of [[generalized multicategories|generalized operads]], and also of [[polynomial monads]].

## Clubs over the permutation category 

This is the most basic sort of club, introduced by Kelly in [MVFC](#KellyMVFC) and [AAC](#KellyAAC).

### Action by substitution product

Let $\mathbf{P}$ be the category of finite sets $[n] = \{1, \ldots, n\}$ (including the empty set $[0]$) and permutations between them, and let $Cat$ be the category of small categories. We define a "wreath product" action of the category $Cat/\mathbf{P}$ on $Cat$, where $Cat/\mathbf{P}$ is the slice category of $Cat$ over $\mathbf{P}$

$$\circ: Cat/\mathbf{P} \times Cat \to Cat$$ 

taking a pair $(\Gamma: C \to \mathbf{P}, D)$ to the category whose objects are tuples 

$$(c; d_1, \ldots, d_n)$$

with $c \in Ob(C)$, $d_i \in Ob(D)$, and $\Gamma(c) = [n]$. A morphism is a tuple 

$$(f; g_1, \ldots, g_n)$$ 

consisting of a morphism $f: c \to c'$ in $C$ and morphisms $g_i: d_i \to d_{\Gamma(f)(i)}'$ in $D$, composed in the obvious way. 

This generalizes the standard notion of wreath product: given a group $G$ and a permutation representation, i.e., a homomorphism $\gamma: G \to Aut([n]) \hookrightarrow \mathbf{P}$, and given a group $H$, the wreath product is defined to be the semidirect product

$$G \int H = G \ltimes H^n$$ 

with the action of $G$ on $H^n$ induced from the action on $[n]$. 

Another, more abstract, way to describe this substitution product is as follows: there is a [[cartesian monad]] $S$ on $Cat$ whose algebras are symmetric strict monoidal categories, and we have $\mathbf{P} = S 1$, where $1$ is the [[terminal category]].  The substitution product $\Gamma \circ D$ can then be described as the following pullback in $Cat$.
$$\array{\Gamma \circ D & \overset{}{\to} & S D\\
  \downarrow && \downarrow^{S !}\\
  C & \underset{\Gamma}{\to} & S 1 & = \mathbf{P}}$$
See below for a general version of this construction.

### Substitution product as monoidal product

We describe how the substitution action $\circ$ lifts to a self-action denoted by the same symbol:

$$\circ: Cat/\mathbf{P} \times Cat/\mathbf{P} \to Cat/\mathbf{P}$$ 

To start, given a pair $(\Gamma: C \to \mathbf{P}, \Delta: D \to \mathbf{P})$, the domain of $\Gamma \circ \Delta$ is the category $\Gamma \circ D$ described above. The functor 

$$\Gamma \circ \Delta: \Gamma \circ D \to \mathbf{P}$$ 

sends an object $(c; d_1, \ldots, d_n)$ to $\sum_i \Delta(d_i)$. 

The effect of $\Gamma \circ \Delta$ on morphisms $(f; g_1, \ldots, g_n)$ may be summarized as "substituting the permutations $\Delta(g_i)$ into the permutation $\Gamma(f)$". To describe this more precisely, we give a little preface. The hom-set $\mathbf{P}([n], [n]) = Aut(n)$ of permutations on $n$ may be identified with the set $Lin(n)$ of total (or linear) orders on $[n]$, if we identify the identity element with the standard order on $\{1, 2, \ldots, n\}$. The sets $Aut(n) = Lin(n)$ are components of an [[operad]] $Lin$ where the operadic multiplication 

$$\mu(n; k_1, \ldots, k_n): Lin(n) \times Lin(k_1) \times \ldots \times Lin(k_n) \to Lin(k_1 + \ldots + k_n)$$ 

takes a linear ordering of $n$ linearly ordered sets and produces the evident linear ordering on the disjoint sum of the sets. 

Then, given a morphism $(f; g_1, \ldots, g_n)$ in $\Gamma \circ D$, we define 

$$(\Gamma \circ \Delta)(f; g_1, \ldots, g_n) \stackrel{def}{=} \mu(n; k_1, \ldots, k_n)(\Gamma(f), \Delta(g_1), \ldots \Delta(g_n))$$ 

Given the abstract description above of the substitution product in terms of the cartesian monad $T$, the functor $\Gamma \circ \Delta$ can be described as the composite
$$ \Gamma \circ D \to T D \overset{T \Delta}{\to} T T 1 \overset{\mu_1}{\to} T 1  = \mathbf{P}$$
where $\mu\colon T T \to T$ is the multiplication of the [[monad]] $T$.

The substitution product thus indicated, 

$$\circ: Cat/\mathbf{P} \times Cat/\mathbf{P} \to Cat/\mathbf{P},$$ 

is the product for a [[monoidal category]] structure on $Cat/\mathbf{P}$. The monoidal unit is the functor $I: 1 \to \mathbf{P}$ which names the 1-element set.  Abstractly, we can observe that the cartesian monad $T$ induces a [[pseudomonad]] on the [[bicategory]] $Span(Cat)$ of spans in $Cat$, which has a [[Kleisli category|Kleisli bicategory]] $Span(Cat)_T$ in which a 1-cell $A\to B$ is a span $A \leftarrow X \to T B$ in $Cat$.  We then have
$$ Cat/\mathbf{P} \simeq Cat / (1 \times T 1) \simeq Span(Cat)_T (1, 1) $$
and the monoidal structure above is that induced from the bicategory composition in $Span(Cat)_T$.

Under this monoidal product, the substitution action indicated earlier, 

$$\circ: Cat/\mathbf{P} \times Cat \to Cat,$$ 

carries a structure of [[actegory]] over the monoidal category $Cat/\mathbf{P}$, in the sense that there is a coherent associativity 

$$(\Gamma \circ \Delta) \circ E \cong \Gamma \circ (\Delta \circ E)$$ 

for $\Gamma: C \to \mathbf{P}$, $\Delta: D \to \mathbf{P}$, and a category $E$, and similarly coherent left and right unit isomorphisms. 

### Clubs over $\mathbf{P}$

+-- {: .un_defn}
###### Definition
A **club** over $\mathbf{P}$ is a monoid in the monoidal category $(Cat/\mathbf{P}, \circ, I)$.  By the abstract characterization above, this is equivalent to a [[monad]] in the bicategory $Span(Cat)_T$ on the object $1$, or equivalently a $T$-[[generalized multicategory|operad]] in the sense of Leinster.
=--

A club over $\mathbf{P}$ induces (via the actegory structure) a 2-monad on $Cat$, and an algebra over the club is an algebra for this monad. That is, an **algebra** over a club $C$ is a category $D$ together with an action $m: C \circ D \to D$ compatible in the usual way with the monoid structure on $C$.

Given a club structure on $\Gamma: C \to \mathbf{P}$, we think of the objects $c$ as formal operations of arity $n = \Gamma(c)$. An algebra $D$ over $C$, $m: C \circ D \to D$, gives in effect an interpretation of each $c$ of arity $n$ as an actual operation $D^n \to D$. 

The free $C$-algebra over a category $D$ is just $C \circ D$. For the free algebra over the terminal category $1$, notice that 

$$C \circ 1 \cong C$$ 

(strictly speaking, the $C$ on the left is a category over $\mathbf{P}$ and the $C$ on the right is just the category). Thus, in a manner of speaking, the free algebra generated by $D$ is obtained by wreathing the free algebra generated by $1$ with $D$, as adumbrated in the idea section above. 

### Examples

* The identity $1_{\mathbf{P}}: \mathbf{P} \to \mathbf{P}$ carries a club structure. The multiplication $\mu$ of the club, on the object level, is given by the assignment
$$(n; k_1, \ldots, k_n) \mapsto k_1 + \ldots + k_n$$ 
and on morphisms, it is given by the operad structure on $Aut(n) = Lin(n)$ discussed above. Algebras over this club are symmetric strict monoidal categories. Algebras in the "pseudo" sense over the induced 2-monad on $Cat$ are [[unbiased]] non-strict [[symmetric monoidal categories]]. Alternatively, if $F(1)$ is the free (biased, non-strict) symmetric monoidal category on one generator, then the symmetric monoidal equivalence $\Gamma: F(1) \to \mathbf{P}$ carries a club structure whose strict algebras are (biased, non-strict) symmetric monoidal categories. 

* Let $\mathbf{B}$ be the [[braid category]], equipped with the usual forgetful functor $\Gamma: \mathbf{B} \to \mathbf{P}$. The club multiplication, at the level of morphisms, is "substitution" of $n$ braids into a braid on $n$ elements. Pseudo-algebras over the induced 2-monad on $Cat$ are unbiased braided monoidal categories. Alternatively, as in the previous example, biased non-strict braided monoidal categories are also strict algebras over a club of the form $\Gamma: F(1) \to \mathbf{P}$ where $F(1)$ is the free braided monoidal category on one generator.

* Let $C$ be any (permutative) operad valued in $Set$, with underlying species $\mathbf{P} \to Set$. The [[category of elements]] gives a functor $\Gamma: El(C) \to \mathbf{P}$, and this carries a club structure induced from the operad structure on $C$. In this way, clubs generalize operads.  In fact, operads in $Set$ can be identified with those clubs for which the functor $\Gamma\colon C\to \mathbf{P}$ is a [[discrete fibration]].

## Clubs over finite sets

Essentially the same construction can be given replacing $\mathbf{P}$ by (a skeleton of) the category $FinSet$ of finite sets and functions, or its opposite.  The corresponding cartesian monads are those whose algebras are categories with strictly associative finite coproducts or strictly associative finite products, respectively.  Examples of such clubs include categories with (not necessarily strictly associative) finite coproducts or products.  Clubs of this sort were also defined in [MVFC](#KellyMVFC) and [AAC](#KellyAAC), and studied further in [OCD](#KellyOCD).

## Clubs over cartesian monads

In fact, the foregoing constructions can be generalized to any [[cartesian monad]] $S$ on $Cat$.  Since a monad is a [[monoid]] in the [[monoidal category]] of [[endofunctors]], the [[slice category]] $[Cat,Cat]/S$ inherits a monoidal structure.  We also have an "evaluate at $1$" functor $[Cat,Cat]/S \to Cat/S1$, which has a right adjoint defined by pulling back: given $A\to S1$, we define an endofunctor $\hat{A}$ of $Cat$ by the following pullbacks:

$$ \array{ \hat{A}(X) & \to & A \\
\downarrow && \downarrow\\
S(X) & \to & S(1) }$$

This right adjoint is fully faithful and embeds $Cat/S1$ into $[Cat,Cat]/S$ as the endofunctors equipped with a [[cartesian natural transformation]] to $S$.  Finally, the cartesianness of $S$ implies that $Cat/S1$ is closed under the monoidal structure of $[Cat,Cat]/S$.  This induced monoidal structure on $Cat/S1$ is, in the case when $S$ is the symmetric strict monoidal category monad, exactly the substitution product defined above.  Thus, a club is a monoid for this monoidal structure, and the inclusion of $Cat/S1$ into $[Cat,Cat]/S$ thereby sends it to a monad over $S$.

Note, however, that this construction depends on no special features of $Cat$; it can be performed for any cartesian monad $S$ on any category with finite limits.  This generalization was performed by Kelly in [CDT](#KellyCDT).  More generally, it can be performed for cartesian monads *in* a suitable 2-category; see [[club in a 2-category]].

## Clubs with many objects

To describe structures on a family of categories rather than a single category (such as a monoidal functor between two monoidal categories), we can generalize to $Cat^\Lambda$ for any set $\Lambda$.  In this case the substitution monoidal product lives on $Cat/(\Lambda \times S\Lambda)$.  This generalization can also be found in [MVFC](#KellyMVFC) and [AAC](#KellyAAC); it amounts to nothing more than considering [[generalized multicategories]] for a cartesian monad (with a [[discrete category]] $\Lambda$ of objects) rather than simply generalized operads (those with the [[terminal category]] of objects).

## Clubs over $Cat$

In [CDT](#KellyCDT) Kelly described a further generalization of clubs over $FinSet$, in which $FinSet$ is replaced by $Cat$.  The crucial feature that allows the substitution product to continue working is the [[Grothendieck construction]] for functors into $Cat$.  In fact, Kelly generalized even further to a substitution product that lives not on the ordinary slice category $CAT/Cat$ but on the [[lax slice 2-category]] $CAT\sslash Cat$ (which Kelly denoted $CAT \int^* Cat$).  This has the advantage that the resulting functor $Mon(CAT\sslash Cat,\circ) \to Mnd(Cat)$ from clubs to [[monads]] on $Cat$ is [[fully faithful functor|fully faithful]], which it is not for the previous notions of club.

There is an analogous generalization of the many-object case, though Kelly did not make this explicit.  Similarly, there is a dual notion of club in $CAT\sslash Cat^{op}$ which generalizes clubs over $FinSet^{op}$.

Kelly did not give any interesting examples of clubs in this generality, only remarking that one is "ineluctably led to" the generalization.  But also worth noting is that there could be interesting morphisms between clubs over $FinSet$ that are only visible when they are viewed as clubs in $CAT\sslash Cat$ (or equivalently as monads on $Cat$).

## Clubs as polynomial monads

The cartesian monads $S$ that are used to define clubs over $\mathbf{P}$, $FinSet$, and $FinSet^{op}$ are in fact [[polynomial monads]] (which immediately implies that they are cartesian).  And an endofunctor equipped with a [[cartesian natural transformation]] to a [[polynomial functor]] is itself automatically polynomial.  Thus, the subcategory of $[Cat,Cat]/S$ identified with $Cat/S1$ by the "clubs over cartesian monads" construction is equivalently the category of polynomial endofunctors of $Cat$ cartesianly-over $S$, and the identification with $Cat/S1$ reduces to the identification of cartesian morphisms between polynomial functors with pullback squares of exponentiable morphisms.  Similarly, considering cartesian natural transformations in the [[double category]] of polynomial functors yields a description of clubs with many objects.

This suggests that an arbitrary polynomial monad could be regarded as a "global club", i.e. one not "over any base".  A polynomial endofunctor of $Cat$ is determined by a single [[exponentiable morphism]] $f:B\to A$ in $Cat$, i.e. a [[Conduche functor]], which in turn is determined by a [[pseudofunctor]] $A\to$ [[Prof]].  Composition of polynomial endofunctors thus yields a monoidal structure on the "slice category" whose objects are categories equipped with a pseudofunctor to $Prof$, monoids with respect to which are polynomial monads; thus a polynomial monad could be viewed as a "club over $Prof$".  Clubs in $CAT/Cat$ and $CAT/Cat^{op}$ are the obvious special cases when $Cat$ and $Cat^{op}$ are embedded into $Prof$ by [[representable profunctor|representable]] and corepresentable profunctors and the pseudofunctor is strict; these correspond to polynomial endofunctors for which $f:B\to A$ is a [[split opfibration]] or [[split fibration]] respectively.

Finally, recall that *non-cartesian* natural transformations between polynomial functors determined by $g:D\to C$ and $f:B\to A$ have a similar description as consisting of a map $h:C\to A$ and a map $C\times_A B \to D$ over $C$.  Translated into the classifying maps $A\to Prof$ and $C\to Prof$ this corresponds to a triangle filled by a lax natural transformation whose components are functors.  Thus in the cases of split (op)fibrations we recover Kelly's lax slice 2-categories $CAT\sslash Cat$ and $CAT\sslash Cat^{op}$.


## Clubs of mixed variance

The clubs described in the preceding sections are all examples of _covariant clubs_: the operations on their algebras $D$ are covariant functors $D^n \to D$. However, many doctrines on $Cat$, such as the doctrine of closed categories, involve functors which are covariant in some arguments and contravariant in others, together with [[extranatural transformations]] between them. For example, in the doctrine for closed monoidal categories, there is an extranatural transformation of the form 

$$ev_{X, Y}: [X, Y] \otimes X \to Y$$ 

which is dinatural in $X$ and natural in $Y$. 

It turns out that many doctrines of "mixed variance" can also be described by an extension of the club notion. This applies particularly to closed monoidal, closed symmetric monoidal, and $*$-autonomous categories. But there are some subtleties, some of which can be explained by looking at a non-example: the doctrine of compact closed categories. 

### Extranaturality graphs 

The underlying arity of an operation of mixed variance will be a _signed set_, i.e., a finite set $\{1, 2, \ldots, n\}$ where a sign $+$ or $-$ is assigned to each element $j$. The element $j$ is given the sign $+$ (resp., $-$) if $j^{th}$ argument of the operation appears covariantly (resp., contravariantly). For example, for the operation 

$$C^{op} \times C \times C \to C: (a, b, c) \mapsto [a, b] \otimes c$$ 

the underlying arity is an ordered list of signs $\{-, +, +\}$. 

The underlying arity of an extranatural transformation for a given doctrine is an arrow of signed sets $A$, $B$ called a **graph** (or EKM graph, for Eilenberg, Kelly and Mac Lane), which by definition is a partition of the signed elements of $A \cup B$ into mated pairs, such that 

* Mated elements, one in $A$ and one in $B$, have the same sign; 

* Mated elements, both in $A$ or both in $B$, have opposite signs. 

An EKM graph may be identified with a directed graph whose edges are mated pairs, oriented in the direction from an $A$-element to a $B$-element if the mates have the same sign, or from $+$ to $-$ if the mates are $A$-elements, or from $-$ to $+$ if the mates are $B$-elements. Such a graph may also be considered as an oriented 1-cobordism between oriented 0-manifolds without loops (circles). 

For example, the arity of the evaluation map in closed monoidal categories, 

$$ev_{X, Y}: [X, Y] \otimes X \to Y$$ 

is an arrow with an oriented edge from the third placeholder of the domain to the first placeholder, and an oriented edge from the second placeholder of the domain to the placeholder of the codomain. 

Hence we obtain a directed graph whose vertices are signed sets and whose edges are EKM graphs between the signed sets. An immediate question is how to compose graphs to form a category, and in particular what to do about "loops" or "islands" which may arise in composing such 1-cobordisms. The first answer that may come to mind is simply to ignore them (in other words, regard the pairings as morphisms in a bicategory of co-relations, and compose them as such). An answer more relevant to clubs will emerge in the next section. 

### Doctrine of compact closed categories 

An example in which loops arise in compositions of extranatural transformations is the doctrine of compact closed (symmetric monoidal) categories. The classic example is the composition 

$$1 \stackrel{\eta}{\to} c^* \otimes c \stackrel{\varepsilon}{\to} 1$$ 

where $1$ denotes a monoidal unit, $\eta$ is a unit for an adjunction $c \dashv c^*$, and $\varepsilon$ is a counit for $c^* \dashv c$ (in a symmetric monoidal category, such adjunctions are inevitably [[ambidextrous adjunction|ambidextrous]]). 

This composition obviously does not define an extranatural transformation from a constant functor to itself, precisely because of dependence on $c$ (for example, when interpreted in the compact closed category of finite-dimensional vector spaces, the value is $dim(c)$). In general, the presence of loops in compositions of extranaturality graphs should be seen as reflecting a fatal ill-definedness of composition of the extranatural transformations giving rise to them, and in such situations an alarm should sound: "[Danger, Will Robinson!](http://en.wikipedia.org/wiki/Danger,_Will_Robinson)". 

The lesson learned is that the doctrine of compact closed categories is not describable by a club, and that for the purposes of clubs there is no use for compositions of graphs which produce loops. If one insists on assigning a value to composition in such cases, it might as well be a junk value $*$, and therefore it is justifiable to regard signed sets and arrows between them as carrying a structure of category enriched in the symmetric monoidal category of pointed sets (= category of sets and partially defined functions). 

### Definition of club of mixed variance 

Let $\mathbf{G}$ be the category enriched in pointed sets whose objects are finite signed sets, and whose morphisms are graphs as described above, composed as in the bicategory of cospans between sets unless this results in the creation of loops (in which case the composition is defined to be the basepoint of the hom-set it belongs to). There is no harm in thinking of $\mathbf{G}$ as an ordinary category. 

Let $(Cat/\mathbf{G})'$ be the full subcategory of $Cat/\mathbf{G}$ whose objects are functors $\Gamma: C \to \mathbf{G}$ such that for every morphism $f$ of $C$, $\Gamma(f)$ is _not_ the basepoint of the hom-set it belongs to. There is an action 

$$\circ: (Cat/\mathbf{G})' \times Cat \to Cat$$ 

for which the objects of $(\Gamma: C \to \mathbf{G}) \circ D$ are pairs 
$(c, \sigma: \Gamma(c) \to Ob(D) \cup Ob(D^{op}))$ where $c$ is an object of $C$ and $\sigma$ is a lift of $sign: \Gamma(c) \to \{+, -\}$ through the function 

$$! \cup !: Ob(D) \cup Ob(D^{op}) \to \{+\} \cup \{-\} = \{+, -\}$$

Morphisms of $(\Gamma: C \to \mathbf{G}) \circ D$ are pairs $(f: c \to c', \phi: \Gamma(f) \to U(D))$ where $\phi$ is a morphism of [[quiver|directed graphs]] to the underlying graph of $D$. Again, this action $\circ$ lifts to a monoidal product 

$$\circ: (Cat/\mathbf{G})' \times (Cat/\mathbf{G})' \to (Cat/\mathbf{G})'$$ 

with monoidal unit $I: 1 \to \mathbf{G}$ naming the 1-point set, positively signed. The action of $(Cat/\mathbf{G})'$ on $Cat$ becomes an actegory with respect to the monoidal category structure. 

+-- {: .un_defn}
###### Definition
A **club** over $\mathbf{G}$ is a monoid in the monoidal category $((Cat/\mathbf{G})', \circ, I)$. 
=--

A club over $\mathbf{G}$ induces (via the actegory structure) a monad on $Cat$, and an **algebra** over the club is an algebra for this monad.  Unlike in the covariant cases, this monad is *not* a 2-monad, but it does give a 2-monad if one restricts to the locally groupoidal 2-category of categories, functors, and natural isomorphisms.

+--{: .query}
[[Mike Shulman]]: Is this sort of club also a generalized operad for some cartesian monad on $Cat$? 

[[Todd Trimble]]: I'm pretty sure that it's a cartesian monad on $Cat$, and actually I don't know any real examples of Kelly's clubs which aren't.
=--

### Examples

As shown above, we cannot expect to describe compact closed categories with a club.  However, we can describe various other structures of mixed variance, such as symmetric monoidal *closed* categories.  Specifically, let $F(1)$ be the free smc category on one generator. There is a "graph functor" $\Gamma: F(1) \to \mathbf{G}$ which takes a morphism of $F(1)$ to its extranaturality graph. The crucial observation is that no basepoint morphism lies in the image of $\Gamma$, i.e., no islands can occur in formal compositions for this doctrine.  This fact is nontrivial; its proof relies on a [[cut-elimination theorem]] (see [KellyCET](#KellyCET)) and works for any structure obtained by adding [[multivariable adjunction|multi-variable right adjoints]] to any of the operations of a club over $\mathbf{P}$.

A morphism in the free symmetric monoidal closed category on a category $C$ is then given by a morphism of $F(1)$ together with a labeling of the oriented edges of its underlying graph (an oriented 1-cobordism) by morphisms of $C$. Then, you compose morphisms of this "[[categorical wreath product]]" in the obvious way, composing the morphism-labels of edges in 1-cobordisms as they get pasted together. 


## References

* [[Max Kelly]], *Many-variable functorial calculus. I*. In "Coherence in categories", LNM 281, pp. 66&#8211;105
 {#KellyMVFC}

* [[Max Kelly]], *An abstract approach to coherence.*  In "Coherence in categories", LNM 281, pp. 106&#8211;147.
 {#KellyAAC}

* [[Max Kelly]], *A cut-elimination theorem.*  In "Coherence in categories", LNM 281, pp. 196&#8211;213.
 {#KellyCET}

* [[Max Kelly]], *On clubs and doctrines*. In "Category Seminar (Proc. Sem., Sydney, 1972/1973)", LNM 420, pp. 181&#8211;256.
 {#KellyOCD}

* [[Max Kelly]], *On clubs and data-type constructors*, Applications of Categories in Computer Science, Proceedings of the London Mathematical Society Symposium, Durham 1991
 {#KellyCDT}

[[!redirects club]]
[[!redirects clubs]]
