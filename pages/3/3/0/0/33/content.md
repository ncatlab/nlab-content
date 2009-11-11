<div class="rightHandSide toc">
[[!include categorification - contents]]
***
[[!include higher category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

Roughly speaking, _vertical categorification_ is a procedure in which structures are generalized from the context of [[set theory]] to [[category theory]] or from category theory to [[higher category theory]].

What precisely that means may depend on circumstances and authors, to some extent. The following lists some common procedures that are known as categorification. They are in general different but may in cases lead to the same categorified notions, as discussed in the examples.



## Variants ##

### As a section of decategorification ###

What has a more specific definition is the process of [[decategorification]]: this concretely quotients out [[k-morphism]]s in a [[n-category]] to produce a $k$-category for some $k \lt n$, in particular a (possibly large) [[set]] (the set of isomorphism classes or equivalence classes of objects) when $k = 0$.

One may understand _vertical categorification_ as any operation that is a [[section]] of this [[decategorification]] operation, and many examples in the literature are of this kind.

#### Examples ####

* The maybe archetypical example of categorification as something that is taken by decatgeorification to the identity operation is the categorification of the [[set]] $\mathbb{N}$ of [[natural numbers]] to the [[category]] [[FinSet]] of [[finite sets]]:

  The set $\mathbb{N}$ is a [[0-category]], while $FinSet$ is a [[1-category]]. The [[decategorification|isomorphism classes]] of $FinSet$ however are in canonical bijection with the elements of $\mathbb{N}$:

  $$ \mathbb{N} \simeq FinSet_\sim .$$

  So $\mathbb{N}$ is the [[decategorification]] of $FinSet$ and accordingly $FinSet$ is a (vertical) categorification of $\mathbb{N}$. 

  From the point of view of [[category theory]], there is some justification to the converse of this statement: the study of the natural numbers is nothing but the study of the isomorphism classes in $FinSet$. In a way, the very notion of **counting** is about this. This point is made nicely in [BaDo98](http://arxiv.org/abs/math.QA/9802029).

  But there are other categorifications of the natural numbers, for instance the category $FinVect$ of finite dimensional [[vector spaces]] (over any given field). This is not equivalent to $FinSet$, but still, its set of isomorphism classes is also canonically in bijection with the natural numbers:

  $$ \mathbb{N} \simeq FinVect_\sim .$$

### As internalization in $n Cat$ ###

Common structures such as [[group]]s, [[ring]]s, etc. may be defined entirely diagrammatically as a collection of objects, morphisms and 2-morphisms in a [[category]] like [[Set]] (the 2-morphisms then are the identities required to hold between the given morphisms).

For instance a [[group]] is an object $G$ in [[Set]] equipped with a morphism $\mu : G \times G \to G$ and so on, and equipped with a 2-morphism from $\mu \circ Id_G \times \mu $ to $\mu \circ \mu \times Id_G$.

In such diagrammatic incarnation, these definitions may be [[internalization|internalized]] into other categories. For instance a group internal to [[Diff]] is a [[Lie group]].

But similarly one can also internalize in categories of higher categories. Let [[Cat]] be the category of (small) categories, regarded as an ordinary category. Then a group internal to [[Cat]] is a [[strict 2-group]]. This is thought of as a notion of a categorified group.

And under the decategorification functor $Cat \to Set$ every categorified group $\mathbf{G}$ in this sense maps to an ordinarty group $G$ and one could speak of $\mathbf{G}$ being "a categorification" of $G$. Bot notice again how highly non-unique such categorification is. In particular, every ordinary group may trivially be regarded as a strict 2-group. As such every ordinary group is at the same time one of its own categorifications, in this sense.

Not every [[2-group]] is a [[strict 2-group]] that is a group object internal to the 1-category [[Cat]]. In general, a [[2-group]] is a _weak_ group object in [[Cat]]: where in [[Set]] all 2-morphisms in the diagrammatic description of the concept of group necessarily had to be identities, in [[Cat]] they could be taken to be non-triviall. But if they are, one will usually want 3-morphisms (which now are necessarily identities) to relate various combinations of these 2-morphisms.

One speaks of this process of categorification using weak internalization of diagrammatic descriptions as categorification of structures _up to coherent higher equivalences_ or _up to coherent higher homotopies_ . One way to make this systematic is discussed below.

#### Examples ####

In the sense of "weakly internalizing in a higher categorical context" we have the following examples of categorification:

* the categorification of [[sheaf]] is [[stack]], 2-stack, 3, stack, ... [[∞-stack]].

* accordingly, the categorification of ([[sheaf]]-)[[topos]] is ([[stack]]-)2-topos, ... [[∞-stack]] [[(∞,1)-topos]]

* using these [[∞-stack]] [[(∞,1)-topos]] notions one can then speak of [[∞-space]]s [[Lie ∞-groupoid]]s and the like.

* Since [[simplicial object]]s in any category usually [[model category|mocel]] [[higher category theory|higher categorial]] structures, many simplicial objects may be regarded as secretly being objects in [[higher category theory]]. For instance [[simplicial group]]s, being [[Kan complex]]es, may be thought of as [[∞-groupoid]]s equipped with a strict group structure, i.e. as _strict $\infty$-groups_. By the [[Dold-Kan correspondence]] it follows then that many objects in [[homological algebra]] such as [[chain complex]]es are equivalent incarnations of these simplicial (abelian) groups. This way large parts of [[homological algebra]] may be regarded as being secretly about "categorified linear algebra" in some sense. For instance the [[dg-category]] of [[chain complex]]es in many contexts plays the role of a [[stable (∞,1)-category]] of "$(\infty,1)$-vector spaces". Notably [[L-∞-algebra]]s may be thought of as [[Lie algebra]]s weakly internalized in $(\infty,1)$-vector spaces understood in this sense.

* When understanging higher linear algebra in this sense, there are important $\infty$-categorifications of notions like integral transformations, [[Fourier transformation]]s, etc. Examples of such categorified linear algebra are [[Fourier-Mukai transformation]]s. A general theory of this is described at [[geometric ∞-function theory]]. Also [[geometric Langlands]] duality fits into this context.


### As homotopy coherent resolution ###

The above process of categorification by coherently weak internalization into higher categorical contexts can be made systematic at least in some cases.

If the structures being defined are [[algebra over an operad|algebras over]] an [[operad]] $T$ one may think of regarding $T$ as an [[(∞,1)-operad]]s and then consider the structures of its algebras as algebras over an $(\infty,1)$-operad. These are infinity-categorified versions of the original structures.

#### Examples ####

For instance this way 

* the notion of ordinary associative [[algebra]] is sent to that of [[A-∞-algebra]] 

* the notion of ordinary [[Lie algebra]] to [[L-∞ algebra]].


### Contrast to horizontal categorificationn ###

Some people also speak of [[horizontal categorification]] as categorification. This is to be distinguished from vertical categorification.

Some people just say 'oidification' for horizontal categorification, in which case it is consistent to speak of vertical categorificaton as just _categorification_ .






## References##

* [[John Baez]] and [[James Dolan|James Dolan]], [Categorification](http://arxiv.org/abs/math.QA/9802029), in _Higher Category
Theory_, eds. Ezra Getzler and Mikhail Kapranov,
Contemp. Math. 230, American Mathematical Society, Providence, Rhode Island, 1998, pp. 1-36.

An early article where the concept of categorification is described is

* Crane and Yetter, 
[Examples of categorification](http://arxiv.org/abs/q-alg/9607028)

A bit of $n$-Caf&eacute; discussion on this subject can be found here: 

* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)


[[!redirects categorification]]
[[!redirects ∞-categorification]]