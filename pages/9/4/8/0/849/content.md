In a [[closed category]] $C$ (for instance a [[closed monoidal category]]) for any two objects $X,Y$ there is an object $hom(X,Y)$ representing the collection of morphisms from $X$ to $Y$. This is called the **internal hom**, expressing the idea that this the perspective on the collection of morphisms from $X$ to $Y$ from the inside of $C$.

You can distinguish this from the external [[hom-set]] $Hom(x,y)$; however, every closed category comes equipped with a functor to [[Set]] (although it need not be [[faithful functor|faithful]]) and the external hom is the underlying set of the internal hom.  To be explicit, if $I$ is the unit object of the closed category $C$, then
$$Hom(I,hom(x,y)) \cong Hom(x,y)$$
by a [[natural isomorphism]].  More generally in a [[closed monoidal category]],
$$Hom(a,hom(b,c)) \cong Hom(a \otimes b,c)$$
naturally.  The rightward map here is often called __currying__, especially in a [[closed monoidal category]] (and more especially for the $\lambda$-calculus).

Every closed category may be seen as a category [[enriched category|enriched]] over itself.  Accordingly, an internal hom is a special case of a [[hom-object]].

## Examples of internal homs

The following examples are meant to illustrate the concept of an 'internal hom', hopefully showing the utility of the concept.

### Internal hom for super vector spaces
The category $SVect$ of [[super vector space]]s has objects $\mathbb{Z}/2$-[[graded vector space]]s with morphisms being _even_ linear maps between them (linear maps which send even things to even things and odd things to odd things):
$$
 Hom_SVect (V, W) = Even Lin(V,W).
$$
This convention allows one nicely to capture the concepts of superalgebra and so on in succinct categorical terms. But occasionally one does need to refer to the _odd_ linear maps. This is the function of the internal hom:
$$
 hom_SVect (V, W) = Lin(V,W).
$$
Note that $hom_{SVect}$ is indeed a super vector space, with the even elements being those maps which preserve the grading and the odd elements being those which change it. One uses this definition to turn SVect into a [[closed monoidal category]]. 

### Internal hom for Banach spaces
A similar thing happens in the category $Ban$ of [[Banach space]]s.  The external hom consists of only the linear maps bounded by $1$:
$$ Hom_Ban(V,W) = \{ f: Lin(V,W) \;|\; \|f\| \leq 1 \} .$$
This definition of morphism recovers the proper notion of [[isomorphism]] of Banach spaces, as well as defining the [[product]] and [[coproduct]] as the [[direct sum]] completed with $p = \infty$ or $p = 1$ respectively.

But the internal hom is the Banach space of all bounded linear maps:
$$ hom_Ban(V,W) = \{ f: Lin(V,W) \;|\; \|f\| \lt \infty \} .$$
This is a Banach space and makes $Ban$ into a [[closed category]].

## Discussion

Here\'s some discussion on notation:

+-- {: .query}

_[[Ronnie Brown|Ronnie]]_: I have found it convenient in a number of categories to use the convention that if say the set of morphisms is $hom(x,y)$ then the internal hom when it exists is $HOM(x,y)$. In particular we have the exponential law for categories 

$$Cat(x \times y,z) \cong Cat(x,CAT(y,z)).$$ 

Then one can get versions such as $CAT_a(y,z)$ if $y,z$ are objects over $a$. 

Of course to use this the name of the category needs more than one letter. Also it obviates the use of those fonts which do not have upper and lower case, so I have tended to use mathsf, which does not work here! 

How do people like this? Of course, panaceas do not exist.

_Toby_:  I see, that fits with using $\CAT$ as the $2$-category of categories but $\Cat$ as the category of categories.  (But I\'m not sure if that\'s a good thing, since I never liked that convention much.)  I only used 'Hom' for the external hom here since Urs had already used 'hom' for the internal hom.

Most of the time, I would actually use the same symbol for both, just as I use the same symbol for both a group and its underlying set.  Every closed category is a [[concrete category]] (represented by $I$), and the underlying set of the internal hom is the external hom.  So I would distinguish them only when looking at the theorems that relate them, much as I would bother parenthesising an expression like $a b c$ only when stating the associative law.

_Ronnie_: In the case of [[crossed complexes]] it would be possible to use $Crs_*(B,C)$ for the internal hom and then $Crs_0(B,C)$ is the actual set of morphisms, with $Crs_1(B,C)$ being the (left 1-) homotopies.  

But if $G$ is a groupoid does $x \in G$ mean $x$ is an arrow or an object? The group example is special because a group has only one object. 

If $G$ is a group I like to distinguish  between the group $Aut(G)$ of automorphisms, and the crossed module $AUT(G)$, some people call it the _actor_,   which is given by the inner automorphism map $G \to Aut(G)$, and this seems convenient. Similarly if $G$ is a groupoid we have a group $Aut(G)$ of automorphisms but also a group groupoid, and so crossed module, $AUT(G)$, which can be described as the maximal subgroup object of the monoid object $GPD(G,G)$ in the cartesian closed closed category of groupoids. 

_Toby_:  'But if $G$ is a groupoid does $x \in G$ mean $x$ is an arrow or an object?':  I would take it to mean that $x$ is an object, but I also use $\mathbf{B}G$ for the pointed connected groupoid associated to a group $G$; I know that groupoid theorists descended from Brandt wouldn\'t like that.  I would use $x \in \Arr(G)$, where $\Arr(G)$ is the [[arrow category]] (also a groupoid now) of $G$, if you want $x$ to be an arrow.  (Actually I don\'t like to use $\in$ at all to introduce a variable, preferring the type theorist\'s colon.  Then $x: G$ introduces $x$ as an object of the known groupoid $G$, $f: x \to y$ introduces $f$ as a morphism between the known objects $x$ and $y$, and $f: x \to y: G$ introduces all three variables.  This generalises consistently to higher morphisms, and of course it invites a new notation for a hom-set: $x \to y$.)

_Ronnie_: I would use, and have used,  $\mathbf{B}G$ for a (the) [[classifying space]] of the group, usually the realisation of the simplicial [[nerve]] of the group, and would often identify a group with its corresponding one-object groupoid. If $G$ is a [[crossed complex]] or multiple groupoid, I would want $\mathbf{B}G$ to be a space, and $Nerv(G)$ to be some combinatorial object, such as simplicial or cubical set, or multi versions of these. Actually, $Nerv(G)$ has in this case the structure of [[T-complex]], so is also a form of higher category. 

Of course Brandt initiated the groupoid idea, coming from the composition of quaternary quadratic forms, generalising ideas of Gauss, but  other later traditions come via Reidemeister in algebraic topology and much wider from Charles Ehresmann, for fibre bundles, Lie groupoids, foliations, and other geometric applications, and these need to be considered for notational decisions. 

I guess the needs of geometry, algebra, analysis, logic and computer science,  and even physics,  will never be completely reconciled.

_Toby_:  We ran into the conflict with $B$ before and somewhat tentatively decided to use $\mathbf{B}G$ for the groupoid and $\mathcal{B}G$ for the space (and maybe $\mathcal{N}G$ for the nerve).  You can read some of that discussion at [[category algebra]] (where it is as out of place as it is here), including reasons for distinguishing $G$ from $\mathbf{B}G$.

Probably it was a mistake to use the letter $B$ again.  I think that the idea was to identify all versions of a [[homotopy 1-type]] (groupoid, simplicial set satisfying certain conditions, nice topological space with no nontrivial higher homotopy groups, etc), but that is not very helpful to other fields.  I would be happy to use a different letter but would want to use something.

By 'groupoid theorists descended from Brandt' I really meant all those who see groupoids as generalised groups (a single set with a partial binary operation satisfying various conditions) rather than those who see them as special kinds of categories (a set of objects, a set ---or even doubly-indexed family of sets--- of isomorphisms, and so on; while it is perfectly possible to view general categories in the Brandt-like way, that seems pretty rare).

[[Mike Shulman]]: I prefer to use $Cat$ for the (1- or 2-)category of small categories and $CAT$ for the (1- or 2-)category of large categories, with 1-categories in bold typeface and 2-categories in script typeface.  And I always write $C(x,y)$ for the set of morphisms from $x$ to $y$, leaving $hom(x,y)$ for the internal hom if you like.  Another nice option is to underline $C$ when writing $C(x,y)$ for the internal hom, although that doesn't appear to work here (although the itex2MML commands summary claims that `\underline` is accepted).

By the way, it's not true that every closed category is [[concrete category|concrete]]: homming out of $I$ need not be faithful.  Take simplicial sets, for instance, or even $Cat$.
=--

[[!redirects internal homs]]
[[!redirects inner hom]]
[[!redirects inner homs]]
