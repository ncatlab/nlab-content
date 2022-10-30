
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Definition

A **quantale** is a [[closed monoidal category|closed monoidal]] [[suplattice]].  Equivalently, it is a [[monoid object]] in the closed symmetric monoidal category of suplattices where the 
morphisms are the set maps that preserve arbitrary joins. This means it is a poset having all [[joins]] and an associative, unital [[tensor product]] $\otimes$ which distributes over joins (the internal-homs then come automatically by the [[adjoint functor theorem]]). The internal-homs in a quantale are sometimes called _residuations_ and written $x\backslash y$ and $y/x$.  Unitality is 
skipped by some authors; in that case we can talk about subclass of unital quantales. 

As a semigroup (monoid if unital) in suplattices, a quantale is essentially the same thing as an 1-object [[quantaloid]], i.e., an 1-object category enriched in suplattices. 


## Quantales and Frames

Additional conditions often imposed on a quantale include:

* Commutativity: $x\otimes y = y\otimes x$
* Idempotence: $x\otimes x = x$
* Affineness: the unit for $\otimes$ is the top element: $1=\top$.

(On affineness: see also [[semicartesian monoidal category]].) If idempotence and affineness are assumed, then $\otimes$ is forced to be the [[meet]] (whence commutativity is automatic) and the quantale is thereby a [[frame]]; see Proposition \ref{meet} below.  General quantales are sometimes considered to be a "noncommutative" version of a frame, whose [[opposite category]] would be a category of "noncommutative [[locale]]s."

(This is the origin of the name "quantale," a [portmanteau](http://en.wikipedia.org/wiki/Portmanteau) of "quantum" and "locale".  Note, though, that quantales seem to be generally treated in the literature more as "quantum frames" than "quantum locales," and in particular their morphisms usually go in the "frame direction."  Possibly this can be explained by the fact that in the past, it was common to use the word "locale" for what we now call a "frame" and simply distinguish between "locale homomorphisms" (now called "frame homomorphisms") and "continuous maps."  The name "quantale" was introduced by C.J. Mulvey.) 

+-- {: .num_prop #meet} 
###### Proposition 
If a [[monoid object]] in the [[cartesian monoidal category]] of [[posets]] is idempotent and affine, then the monoid multiplication is the meet operation. 
=-- 

+-- {: .proof} 
###### Proof 
Let $(M, \otimes, 1)$ be the monoid. If $a \leq x$ and $a \leq y$, then $a = a \otimes a \leq x \otimes y$. On the other hand, we have $x \otimes y \leq x \otimes 1 = x$ and similarly $x \otimes y \leq y$, so $a \leq x \otimes y$ implies $a \leq x$ and $a \leq y$ by transitivity. Thus $a \leq x \otimes y$ iff $a \leq x$ and $a \leq y$, i.e., $x \otimes y$ satisfies the defining property of the meet $x \wedge y$. 
=-- 

Along similar lines, the following construction provides passage from commutative affine quantales to frames: 

+-- {: .num_lemma}
###### Lemma 
Let $(Q, \cdot, 1)$ be a commutative affine quantale, and let $Idem(Q)$ be the subposet of elements $x \cdot x = x$. Then $Idem(Q)$ is a frame, where the meet operation is given by multiplication in $Q$. The functor $Idem$ is right adjoint to the forgetful functor from commutative affine quantales to frames. 
=-- 

+-- {: .proof}
###### Proof 
If $x, y$ are idempotent, then so is $x \cdot y$ using the fact that $\cdot$ is commutative. Thus $Idem(Q)$ is an idempotent affine submonoid of $Q$, which by Proposition \ref{meet} forces $\cdot$ to be the meet. Next, we show that $Idem(Q)$ is closed under taking joins in $Q$: if $x_i$ is a collection of idempotents, we have 

$$x_i \leq x_i x_i \leq (\bigvee_i x_i) (\bigvee_i x_i)$$ 

for all $i$, whence 

$$\bigvee_i x_i \leq (\bigvee_i x_i) (\bigvee_i x_i),$$

which is all we need (the opposite inequality is automatic since $a \cdot a \leq a \cdot 1 = a$ for all $a \in Q$). Since joins in $Idem(Q)$ are calculated just as they are in $Q$, and since multiplication in $Q$ distributes over arbitrary joins, we have that binary meets distribute over arbitrary joins in $Idem(Q)$. 

Finally, if $A$ is a frame and $Q$ is a commutative affine quantale, it is clear that a quantale map $f \colon A \to Q$ takes elements in $A$ (which are idempotent under meet) to idempotents in $Q$. Hence $f$ factors uniquely through $Idem(Q) \hookrightarrow Q$, and the map $A \to Idem(Q)$ is a frame map. This shows that $Idem$ is the right adjoint as claimed. 
=-- 

In fact, we may also observe that the forgetful functor from commutative affine quantales to commutative quantales also has a right adjoint, just by passing from a commutative quantale to the principal downset given by the quantale unit. (However, the forgetful functor from commutative quantales to quantales does _not_ have a right adjoint.) 

On very general grounds, the forgetful functor from the category of frames to the category of quantales has a left adjoint (see [here](/nlab/show/colimits+in+categories+of+algebras#relatively_free_functors)). This forgetful functor is full and faithful, and as a result the unit of the adjunction is a regular epi described by a suitable quantale congruence; see the next section. 

## Quantale congruences and nuclei 

A *quantale congruence* is simply an [[equivalence relation]] $({\equiv}) \hookrightarrow Q \times Q$ on a quantale $Q$ that respects the quantale multiplication and the taking of sups: if $a \equiv b$ and $x \equiv y$, then $a x \equiv b y$, and if $x_i \equiv y_i$ for all $i \in I$, then $\bigvee_{i \in I} x_i \equiv \bigvee_{i \in I} y_i$. 

Consequently, $Q/{\equiv}$ defines a quantale $\tilde{Q}$ with operations inherited along a quantale quotient map $q: Q \to \tilde{Q}$. Since $q$ preserves arbitrary sups, it has a right adjoint $r: \tilde{Q} \to Q$ by the [[adjoint functor theorem]] applied to posets. Thus we have a [[monad]] or [[closure operator]] $r q: Q \to Q$, and the algebras/fixpoints of the monad/closure operator are identified with the elements of $\tilde{Q}$, i.e., $r: \tilde{Q} \to Q$ is isomorphic to the inclusion $Fix(r q) \hookrightarrow Q$. 

The monad $r q$ is a quantale nucleus in the sense of the following definition: 

+-- {: .num_defn} 
###### Definition 
A function $j: Q \to Q$ on a quantale $Q$ is a *nucleus* if it is a [[monad]] ($x \leq y$ implies $j(x) \leq j(y)$, $x \leq j(x)$, $j j(x) = j(x)$ for all $x, y \in Q$) and is [[monoidal functor|lax monoidal]]: $1 \leq j(1)$ and $j(x) \cdot j(y) \leq j(x \cdot y)$ for all $x, y \in Q$. 
=-- 

There is a natural bijective correspondence between congruences on a quantale $Q$ and nuclei on $Q$. 

## Enrichment over quantales

Aside from being "noncommutative frames", a different way of thinking about quantales views them as a [[(0,1)-category|(0,1)-categorical]] analogue of a [[cosmos]] (in the sense of Benabou).  In particular, one can then study [[enriched categories]] over a quantale. A classic example is Lawvere [[metric space]]s, seen as categories enriched in the quantale $([0, \infty], \geq)$ with $+$ taken as tensor product. 

Enrichment is often particularly interesting for $*$-quantales (see below), where one can study $*$-enriched categories. 

## Examples ##

{#compsci}Quantales are a surprisingly commonplace structure in computer science. See the [automata references](#automata). A very simple example is the power set of strings (i.e., the [[power set]] of the [[free monoid]] over some set of characters $\Sigma$). The order is the inclusion order on sets, and meet and join are just intersection and union, respectively. Taking $\epsilon$ to be the empty string, and $a \cdot b$ to be the join of two strings, the quantalic operations are then:

* $1 = \{\epsilon\}$
* $I \otimes J = \{ i\cdot j \mid i \in I, j \in J \}$ 
* $K/J = \{ i \mid \forall_{j\in J} i\cdot j \in K \}$
* $I\backslash K = \{ j \mid \forall_{i\in I} i\cdot j \in K \}$

This example generalizes as follows: given any [[monoidal category|monoidal]] [[preorder]] $M$ (for instance, a monoid equipped with the discrete order, as in the previous example), the collection of down-closed subsets of $M$ carries a quantale structure given by [[Day convolution]] with respect to categories enriched in $\mathbf{2} = TV$, the [[Heyting algebra]] of truth values. Explicitly, if $e$ denotes the unit of $M$ and $\cdot$ the multiplication, then 

* $1 = \{x\in M \mid x \leq e\}$ 
* $I \otimes J = \{x\in M \mid \exists_{i \in I} \exists_{j \in J} x \leq i \cdot j\}$
* $K/J = \{i \in M \mid \forall_{j\in J} i\cdot j \in K \}$
* $I\backslash K = \{j \in M \mid \forall_{i\in I} i\cdot j \in K \}$

Another class of examples: internal homs $\hom_{sLat}(X, X)$ in the closed monoidal category of suplattices. For example, when the suplattice $X$ is a power set $P(S)$, one may identify $\hom_{sLat}(P(S), P(S))$ with the poset of binary relations $P(S \times S)$, ordered by inclusion and where the quantalic multiplication is relational composition.

An example in algebra is given by the lattice of ideals of a commutative ring, with the tensor product given by ideal multiplication, which makes it into a commutative affine quantale. Residuation in this case is *ideal division* $(\mathfrak{a} : \mathfrak{b}) = \{x | x\mathfrak{b} \subseteq \mathfrak{a}\}$.

Quantales, as monoids in the symmetric monoidal category $sLat$, can be tensored to produce new quantales. 


## $*$-quantales

A $*$-quantale is a quantale $Q$ equipped with an additional structure of an involution 

$$ * : Q \to Q$$ 

for which $(x \otimes y)^* = y^* \otimes x^*$ and $1^* = 1$, where $1$ denotes the monoidal unit. (The operator is assumed to be covariant with respect to the poset structure.) 

An example of a $*$-quantale is the quantale of binary relations on a set $S$, where the $*$-operation is relational opposite: 

* $R^* = \{(y, x): (x, y) \in R\}$ 

Another example is obtained by taking the quantale of down-closed subsets of a $*$-monoidal poset $M$ (which is the same thing as a $*$-[[star-monoid|monoid]] in the [[cartesian monoidal category]] of posets), with the quantale structure given by Day convolution as described above, and the $*$-operator obtained by cocontinuously extending the $*$-operator on $M$. Explicitly, 

* $L^* = \{x^*: x \in L\}$ 

A _$*$-enriched category_ over a $*$-quantale $Q$ is a category $(X, d: X \times X \to Q)$ enriched in the underlying quantale, such that 

$$d(y, x) = d(x, y)^*$$ 

This notion can also be expressed in terms of lax morphisms of $*$-quantales; see below. 

## Relation to linear logic
 {#RelationToLinearLogic}

A commutative quantale is in particular a [[symmetric monoidal category]] (a symmetric monoidal [[(0,1)-category]]). As such it may be thought of as a model for [[linear logic]] in the general sense. Precisely if it has a [dualizing object](dualizing+object+in+a+closed+category) then it is a [[star-autonomous category]] and hence a model for [[linear logic]] in the original sense. (see e.g. [Yetter 90, page 43](#Yetter90)). Indeed, quantales have been argued to provide models for [[quantum logic]], see there for more.

## Morphisms of quantales ##

There is a variety of notions of morphism of quantale, just as there is a variety of notions of morphism between closed monoidal categories. All the notions considered here are morphisms between the underlying sup-lattices, in other words preserve arbitrary joins, hence are left adjoints as functors between the underlying categories. 

* At the weak end of the scale, one may consider _lax morphisms_ of quantales, i.e., (lax) [[monoidal functor]]s of quantales seen as monoidal categories. 

  * An important example of this is that [[enriched category|categories enriched]] in a monoidal poset $M$, such as Lawvere [[metric space]]s, amount to the same thing as lax quantale morphisms of the form $2^d: 2^{M} \to 2^{X \times X}$ where the domain is the quantale of upward-closed subsets of $M$ with the Day convolution structure, and the codomain is the quantale of binary relations on $X$, with multiplication being relational composition. 

* A stronger notion is of _strong morphisms_ of quantales seen as monoidal categories. As noted above, all quantale morphisms considered here are already left adjoints in $Cat$, and if the adjunction lifts to $MonCat$ (the 2-category of monoidal categories, lax monoidal functors, and monoidal transformations), then the left adjoint is strong monoidal. This often occurs in practice. 

* An even stronger notion is where the morphisms also strongly preserve the closed structure, i.e., the internal homs or residuations. (An example is to be developed for [[building]]s.) 

* There are corresponding notions of morphisms of $*$-quantales, where in each case morphisms strongly respect the $*$ operations. For instance, the notion of $*$-enriched category over a $*$-monoidal poset $M$ can be equivalently recast as a lax morphism between $*$-quantales, $2^d: 2^M \to 2^{X \times X}.$


##Related entries: 

* [[locale]], 

* [[quantaloid]], [[semiquantale]]

* [[module over a quantale]]

## References



The initial paper to use the term `quantale' was

*  [[Christopher J. Mulvey]], _["&"](http://www.maths.sussex.ac.uk/Staff/CJM/research/pdf/&.pdf)_, Rend. Circ. Mat. Palermo, II. Ser., Suppl. 12, 99-104 (1986) [Zbl 0633.46065](http://zbmath.org/?q=an:0633.46065)


* [[eom]]: [quantale](http://www.encyclopediaofmath.org/index.php/Quantale)

Discussion of how quantales serve as a model for [[linear logic]] and [[quantum logic]] is in 

* [[David Yetter]], _Quantales and (noncommutative) linear logic_, Journal of Symbolic Logic 55 (1990), 41-64.
 {#Yetter90}

A monograph on quantales:

* Kimmo I. Rosenthal, _Quantales and their applications_, Pitman Res. Notes in Math. Series 234, Longman 1990

{#automata}Relations with automata and process semantics

* [[Samson Abramsky]],  [[Steve Vickers]], _Quantales, observational logic and process
semantics_, Math. Struct. in Comput. Sci. __3__  (1993) 161-227. [doi](https://doi.org/10.1017/S0960129500000189), [CiteSeer<sup>X</sup>](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.210.1485)


Connections to operator algebras and etale groupoids is discussed in 

* [[Pedro Resende]], _&#201;tale groupoids and their quantales_, Adv. Math. __208__ (2007) 147-209; also published electronically: [doi](http://dx.doi.org/10.1016/j.aim.2006.02.004); [math/0412478](http://arxiv.org/abs/math/0412478)
* M.C. Protin, P. Resende, _Quantales of open groupoids_, J. Noncommut. Geom. __6__ (2012) 199&#8211;247.
* [[Pedro Resende]], Lectures on &#233;tale groupoids, inverse semigroups and quantales, Lecture Notes for the GAMAP IP Meeting, Antwerp, 4&#8211;18 September, 2006, 115 pp.; [pdf](http://www.math.ist.utl.pt/%7Epmr/poci55958/gncg51gamap-version2.pdf)
* [[Pedro Resende]], _Groupoid sheaves as quantale sheaves_, J. Pure Appl. Algebra 216 (2012), 41&#8211;70; [arxiv/0807.4848](http://arxiv.org/abs/0807.4848v3)
[doi](http://dx.doi.org/10.1016/j.jpaa.2011.05.002)
* D. Kruml, J.W. Pelletier, P. Resende, [[J. Rosický]], _On quantales and spectra of $C^\ast$-algebras_, Appl. Categ. Structures __11__ (2003) 543&#8211;560.
* D. Kruml, P. Resende, _On quantales that classify $C^\ast$-algebras_, Cah. Topol. Geom. Differ. Categ. __45__ (2004) 287&#8211;296.
* [[F. Borceux]], [[J. Rosický]], G. Van den Bossche, _Quantales and $C^\ast$-algebras, J. London Math. Soc. __40__ (1989) 398&#8211;404 [doi](http://dx.doi.org/10.1112/jlms/s2-40.3.398)

A connection between topoi, "Grothendieck" quantales and $C^\ast$-algebras

* Simon Henry, _Toposes, quantales and C* algebras in the atomic case_, [arxiv/1311.3451](http://arxiv.org/abs/1311.3451)


 Sheaves on a quantale

* [[Francis Borceux]], Rosanna Cruciani, Sheaves on a quantale, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1993) 34:3, page 209-228 [pdf](http://archive.numdam.org/article/CTGDC_1993__34_3_209_0.pdf)

category: order, noncommutative geometry
[[!redirects quantale]]
[[!redirects quantales]]
[[!redirects *-quantale]]
[[!redirects *-quantales]]
[[!redirects star-quantale]]
[[!redirects star-quantales]]