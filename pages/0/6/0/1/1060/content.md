
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents
* table of contents
{:toc}

## Idea

There are many ways to describe a $*$-autonomous category; here are a few:

* it is a [[monoidal category]] in which all objects have "duals", but in a weaker sense than in a [[compact closed category]].
* it is a [[closed monoidal category]] in which the [[internal-hom]] can be expressed in terms of the tensor product in a particular way.
* it is a [[linearly distributive category]] in which all objects have "duals" in an appropriate linearly distributive sense.
* it is a semantics for classical multiplicative [[linear logic]].
* it is a representable [[star-polycategory]].
* it is a sort of categorified [[Frobenius algebra]].

In particular, it has two monoidal structures $\otimes$ and $\parr$, as in a linearly distributive category.  However, because of the dualization operation $(-)^\ast$, each of them determines the other by a "multiplicative [[de Morgan's laws|de Morgan]] duality": $A\parr B \cong (A^\ast \otimes B^\ast)^\ast$.  Thus, in the definition we only have to refer to one monoidal structure.

A $\ast$-autonomous category is a special case of the notion of [[star-autonomous pseudomonoid]] (a.k.a. Frobenius pseudomonoid, since it categorifies a [[Frobenius algebra]]) in a [[monoidal bicategory]].

(Regarding the use of "autonomous", this was once used as a bare adjective to describe a [[closed monoidal category]], or sometimes a [[compact closed monoidal category]], but is rarely used in this way today. It has been suggested that in these cases with internal-hom objects the category is autonomous or "sufficient unto itself" without needing hom-sets, or suchlike.)

## Definition ##

There are two useful equivalent formulation of the definition

+-- {: .num_defn #DefByDualizingObject}
###### Definition

A _$*$-autonomous category_  is a [[symmetric monoidal
category|symmetric]] [[closed monoidal category]] $\langle
C,\otimes, I,\multimap\rangle$ with a _[[dualizing object in a closed category|global dualizing object]]_: an object
$\bot$ such that the canonical morphism
$$ d_A \;\colon\; A \to (A \multimap \bot) \multimap \bot ,$$
which is the transpose of the [[evaluation map]]
$$ ev_{A,\bot} \;\colon\; (A \multimap \bot) \otimes A \to \bot\,,$$
is an [[isomorphism]] for all $A$.  (Here, $\multimap$ denotes the [[internal hom]].)

=--

+-- {: .num_defn #DefByDualization}
###### Definition

A _$*$-autonomous category_  is a [[symmetric monoidal category]] $\mathcal{C}$
equipped with a [[full and faithful functor|full and faithful]] [[functor]]

$$
  (-)^\ast \colon \mathcal{C}^{op} \longrightarrow \mathcal{C}
$$

such that there is a [[natural isomorphism]]

$$
  \mathcal{C}(A \otimes B, C^\ast) \simeq \mathcal{C}(A, (B\otimes C)^\ast)
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

These two definitions, def. \ref{DefByDualizingObject}
and def. \ref{DefByDualization}, are indeed equivalent.

=--

+-- {: .proof}
###### Proof

Given def. \ref{DefByDualizingObject}, 
define the dualization functor as the [[internal hom]] into the [[dualizing object in a closed category|dualizing object]]

$$
  (-)^ \ast  \coloneqq (-)\multimap\bot
  \,.
$$  

Then the morphism $d_A$
is natural in $A$, so that there is a [[natural isomorphism]]
$d:1\Rightarrow(-)^{**}$.  We also have

$$\begin{aligned}
\hom(A\otimes B,C^*)& = \hom(A\otimes B, C\multimap\bot) \\
& \cong \hom((A\otimes B)\otimes C,\bot) \\
& \cong \hom(A\otimes(B\otimes C), \bot) \\
& \cong \hom(A,(B\otimes C)\multimap\bot) \\
& = \hom(A,(B\otimes C)^*)
\end{aligned}$$

This yields the structure of def. \ref{DefByDualization}.

Conversely, given the latter then the [[dualizing object]] $\bot$ is defined as the dual of the [[tensor unit]] $\bot \coloneqq I^*$ and the [[internal hom]] by $A \multimap B \coloneqq A^* \parr B$ (where $\parr$ is defined as below).

=--

(See [this discussion](https://github.com/punkdit/categories/blob/master/www.mta.ca/cat-dist/archive/2007/07-12#L2488-L2574) on the [categories mailing list](https://www.mta.ca/~cat-dist/) for alternative definitions and remarks about coherence.)

+-- {: .num_remark}
###### Remark

A $\ast$-autonomous category in which the [[tensor product]] is compatible with duality in that there is a [[natural isomorphism]]

$$
  (A \otimes B)^\ast \simeq A^\ast \otimes B^\ast
$$

is a [[compact closed category]].  This follows from a stronger result of Dold and Puppe [DP83]{#DP83}.
=--

More generally, even if the $\ast$-autonomous category is not compact closed, then by this linear "[[de Morgan duality]]" the tensor product induces a second binary operation

$$
  A \parr B \coloneqq  (A^\ast \otimes B^\ast)^\ast
  \,.
$$

making it into a [[linearly distributive category]].  Here the notation on the left is that used in [[linear logic]], see below at _[Properties -- Internal logic](#InternalLogic)_.

A general $\ast$-autonomous category can be thought of as like a [[compact closed category]] in which the [[unit]] and [[counit]] of the [[dual objects]] refer to two different tensor products: we have $\top \to A \parr A^*$ but $A^* \otimes A \to \bot$, where $(\otimes,\top)$ and $(\parr,\bot)$ are two different monoidal structures.  The necessary relationship between two such monoidal structures such that this makes sense, i.e. such that the [[triangle identities]] can be stated, is encoded by a linearly distributive category; then an $\ast$-autonomous category is precisely a linearly distributive category in which all such "mixed duals" (or "negations") exist.


=--


## Functors and transformations

It may not be clear from the above definitions what the appropriate notion of "$\ast$-autonomous functor" is.  In fact, from at least one perspective it suffices to consider ordinary [[lax monoidal functors]], at least in the symmetric case; no interaction with the $\ast$-autonomy is required.

Let $\ast Aut$ denote the full sub-2-category of $SymMonCat_{lax}$ on the (symmetric) $\ast$-autonomous categories; hence its morphisms and 2-cells are lax symmetric monoidal functors and monoidal natural transformations.  Let $SymLinDist$ denote the 2-category of symmetric [[linearly distributive categories]], symmetric linear functors, and linear transformations (defined at [[linearly distributive category]]).

+-- {: .un_theorem}
###### Theorem
There is a functor $\ast Aut \to SymLinDist$ that is 2-fully-faithful, i.e. an equivalence on hom-categories, and has both a left and a right [[2-adjoint]].
=--
+-- {: .proof}
###### Proof
A linearly distributive functor consists of a functor $F_\otimes$ that is lax monoidal for $\otimes$ and a functor $F_\parr$ that is lax monoidal for $\parr$.  Recalling that $\parr$ is defined in a $\ast$-autonomous category as $A\parr B = (A^* \otimes B^*)^*$, if $F$ is a lax monoidal functor between $\ast$-autonomous categories we define $F_\otimes = F$ and $F_\parr(A) = (F(A^*))^*$.  See [Cockett-Seely 1999](#CockettSeely99) for details.
=--

In the non-symmetric case, we need to additionally require of an "$\ast$-autonomous functor" that $^*(F(A^*)) \cong (F({}^*A))^*$, and define $F_\parr$ to be their common value.

On the other hand, if we consider instead "Frobenius linear functors" between linearly distributive categories, then such functors necessarily preserve duals.  Thus, the corresponding notion of $\ast$-autonomous functor would need to preserve the dualization functors as well, $F(A^*) \cong (F(A))^*$.


## Properties

### Internal logic
 {#InternalLogic}

The [[internal logic]] of star-autonomous categories is the multiplicative fragment of [[classical linear logic]], conversely star-autonomous categories are the [[categorical semantics]] of [[classical linear logic]] ([Seely 89, prop. 1.5](#Seely89)). See also at _[[relation between type theory and category theory]]_.

## Examples ##

* A simple example of a $*$-autonomous category is the category of [[finite-dimensional vector space]]s over some field $k$.  In this case $k$ itself plays the role of the dualizing object, so that for an f.d. vector space $V$, $V^*$ is the usual [[dual vector space|dual space]] of linear maps into $k$.

* More generally, any [[compact closed category]] is $*$-autonomous with the unit $I$ as the dualizing object.

* A more interesting example of a $*$-autonomous category is the category of [[sup-lattice]]s and sup-preserving maps (= left adjoints). Clearly the poset of sup-preserving maps $hom(A, B)$ is itself a sup-lattice, so this category is closed. The free sup-lattice on a poset $X$ is the internal hom of posets $[X^{op}, \Omega]$; in particular the poset of truth values $\Omega$ is a unit for the closed structure. Define a duality $ (-)^* $ on sup-lattices, where $ X^* = X^{op} $ is the opposite poset (inf-lattices are sup-lattices), and where $ f^*: Y^* \to X^* $ is the left adjoint of $f^{op}: X^{op} \to Y^{op}$. In particular, take as dualizing object $D = \Omega^{op}$. Some simple calculations show that under the tensor product defined by the formula $ (X \multimap Y^*)^* $, the category of sup-lattices becomes a $*$-autonomous category. 

* Another interesting example is due to Yuri Manin: the category of [[quadratic algebra]]s. A **quadratic algebra** over a [[field]] $k$ is a graded algebra $A = T(V)/I$, where $V$ is a finite-dimensional vector space in degree 1, $T(V)$ is the tensor algebra (the free $k$-algebra generated by $V$), and $I$ is a graded ideal generated by a subspace $R \subseteq V \otimes V$ in degree 2; so $R = I_2$, and $A$ determines the pair $(V, R)$. A morphism of quadratic algebras is a morphism of graded algebras; alternatively, a morphism $(V, R) \to (W, S)$ is a linear map $f: V \to W$ such that $(f \otimes f)(R) \subseteq S$. Define the dual $A^*$ of a quadratic algebra given by a pair $(V, R)$ to be that given by $(V^*, R^\perp)$ where $R^\perp \subseteq V^* \otimes V^*$ is the kernel of the transpose of the inclusion $i: R \subseteq V \otimes V$, i.e., there is an exact sequence 
$$0 \to R^\perp \to V^* \otimes V^* \overset{i^*}{\to} R^* \to 0$$ 
Define a tensor product by the formula 
$$(V, R) \otimes (W, S) = (V \otimes W, (1_V \otimes \sigma \otimes 1_W)(R \otimes S))$$
where $\sigma: V \otimes W \to W \otimes V$ is the symmetry. The unit is the tensor algebra on a 1-dimensional space. The hom that is adjoint to the tensor product is given by the formula $A \multimap B = (A \otimes B^*)^*$, and the result is a $*$-autonomous category. 

* In a similar vein, I am told that there is a $*$-autonomous category of [[quadratic operad]]s. 

* Girard's [[coherence spaces]], developed as models of [[linear logic]], give an historically important example of a $*$-autonomous category.  These are closely related to a general construction of $*$-autonomous categories (and related types of categories) called [[poset-valued sets]].

* The category of [[finiteness spaces]] and their relations is $*$-autonomous.  Probably so is any category of [[arity spaces]], which includes coherence spaces and finiteness spaces.

* Hyland and Ong have given a completeness theorem for multiplicative linear logic in terms of a $*$-autonomous category of _fair games_, part of a series of work on game semantics for closed category theory (compare Joyal's interpretation of Conway games as forming a compact closed category). 

* The [[Chu construction]] can be used to form many more examples of $*$-autonomous categories.

* If $V$ is a [[closed monoidal category]] with finite products, then $V \times V^{op}$ is $*$-autonomous ([Barr 1996](#Barr96)).  This is a special case of the Chu construction where the dualizing object is terminal.

* Various [[subcategories]] of Chu constructions are also $*$-autonomous.  For instance, if [[Vect]] is the category of [[vector spaces]] over a [[field]] $k$, then $Chu(Vect,k)$ is the category of vector spaces equipped with a specified "dual" having no further structure than an evaluation map $V\otimes W\to k$.  One often wants to impose nondegeneracy conditions on this "dual", which in turn can be reflected as [[topological vector space|topological]] properties of the original space $V$. 
Write $(V,V')$ for an object of $Chu(Vect,k)$ and $\langle v,w \rangle$ the evaluation of $w$ on $v$. We say that $(V,V')$ is separated if for each $v \neq 0 \in V$, there exists $v' \in V'$ such that $\langle v,v' \rangle \neq 0$ and we say that it is extensional if for each $v' \neq 0 \in V'$, there exists $v \in V$ such that $\langle v,v' \rangle \neq 0$. Then, the full subcategory $chu(Vect,k)$ of separated, extensional pairs is $*$-autonomous.

* A [[quantale]] (see there) is a $\ast$-autonomous category if it has a [[dualizing object]].

* Suppose $\langle C,\otimes, I,\multimap\rangle$ is a closed symmetric monoidal category equipped with a "pre-dualizing object" $\bot$, in the sense that the contravariant self-adjunction $(-\multimap\bot) \dashv (-\multimap\bot)$ is [[idempotent adjunction|idempotent]], i.e. the double-dualization map $A \to (A \multimap \bot) \multimap \bot$ is an isomorphism whenever $A$ is of the form $B\multimap\bot$.  (Note that idempotence is automatic if $C$ is a poset.)  Then the category of [[fixed point of an adjunction|fixed points]] of this adjunction, i.e. the full subcategory of objects of the form $B\multimap\bot$, is $*$-autonomous.  For it is closed under $\multimap$, as $(A\multimap (B\multimap \bot)) \cong (A\otimes B\multimap \bot)$, and reflective with reflector $(-\multimap\bot)\multimap\bot$, and it contains $\bot$ since $\bot\cong (I\multimap \bot)$.  Hence it is closed symmetric monoidal with tensor product $((A\otimes B)\multimap\bot)\multimap\bot$, and all its double-dualization maps are isomorphisms by assumption.  A historically important example is Girard's [[phase semantics]] of [[linear logic]].  Note that this category is a full subcategory of $Chu(C,\bot)$ closed under duality --- indeed, it is the intersection of the two embeddings of $C$ and $C^{op}$ therein --- but its tensor product is *not* the restriction of the tensor product of $Chu(C,\bot)$.

* Phase semantics is also a special case of a [[ternary frame]], which is the case of the previous example when $\langle C,\otimes, I,\multimap\rangle$ has the [[Day convolution]] structure induced from a [[promonoidal category|promonoidal]] poset.  There is also another way to obtain negation in a ternary frame involving a "compatibility relation"...

* The [[unit interval]] $[0,1]$ is a [[semicartesian monoidal category|semicartesian]] $\ast$-autonomous poset with the monoidal structure $x \otimes y = \max(x+y-1,0)$ and dualizing object $0$.  The involution is $x^\ast = 1-x$ and the dual [[multiplicative disjunction]] is $x\parr y = \min(x+y,1)$.  This is known as [[Lukasiewicz logic]] and is used in [[fuzzy logic]]; it is also a special case of a [[t-norm]].

* A summary of many different ways to construct examples is in [Hyland-Schalk](#HylandSchalk01).

## Relation to other structures

* A $\ast$-autonomous category is a [[linearly distributive category]] with the cotensor product $x\parr y = (x^* \otimes y^*)^*$.  Conversely, any linearly distributive category with "duals" in the appropriate sense is $\ast$-autonomous.

* Since a linearly distributive category is a representable [[polycategory]], a $\ast$-autonomous category is a representable polycategory with duals.  If the duals are strictly involutive, then it is a [[*-polycategory]].

* As noted above, a [[compact closed]] category is a degenerate sort of $\ast$-autonomous category.

* It is shown in [HH13](#HH13) that a $\ast$-autonomous category that is [[traced monoidal category|traced]] must be compact closed.

* We can weaken the requirement that the canonical morphism
$ d_A: A \to (A \multimap \bot) \multimap \bot $ is an isomorphism to the one that it is a monomorphism: [[weak (star)-autonomous category]].


## References ##

The notion is originally due to:

* [[Michael Barr]], _$\ast$-Autonomous Categories_, Lecture Notes in Mathematics **752**, Springer (1979) &lbrack;[doi:10.1007/BFb0064579](https://doi.org/10.1007/BFb0064579)&rbrack;

See also:

* [[Michael Barr]], [[Heinrich Kleisli]], *Topological balls*, [[Cahiers|Cahiers Topologie Géométrie Différentielle Catégorique]], **40** 1 (1999) 3–20 &lbrack;[numdam:CTGDC_1999__40_1_3_0](http://www.numdam.org/item/?id=CTGDC_1999__40_1_3_0)&rbrack;


* [[Michael Barr]], _$\ast$-Autonomous categories: once more around the track_, Theory and Applications of Categories **6** 1 (1999) 5-24 &lbrack;[tac:6-01](http://www.tac.mta.ca/tac/volumes/6/n1/6-01abs.html)&rbrack;

* [[Michael Barr]], _Topological $\ast$-autonomous categories, revisited_, rewrite of TAC, 16 (2006), 700-708 ([arXiv:1609.04241](http://arxiv.org/abs/1609.04241))

* [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *On $\ast$-autonomous categories of topological modules*, Theory Appl. Categories, **24** 14 (2010) 278–293 &lbrack;[tac:24-14](http://www.tac.mta.ca/tac/volumes/24/14/24-14abs.html)&rbrack;


The relation to [[linear logic]] was first described in 

* {#Seely89} [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 
further discussed in

* [[Michael Barr]], *$\ast$-Autonomous categories and linear logic*, Math. Structures Comp. Sci. **1** 2 (1991) 159–178 &lbrack;[doi:10.1017/S0960129500001274](https://doi.org/10.1017/S0960129500001274), [pdf](https://www.math.mcgill.ca/barr/papers/scatll.pdf), [[Barr-AutomomousCatAndLinLogic.pdf:file]]&rbrack;

* [[Michael Barr]], *Accessible categories and models of linear logic*, J. Pure Appl. Algebra **69** (1990) 219–232 &lbrack;<a href="https://doi.org/10.1016/0022-4049(91)90020-3">doi:10.1016/0022-4049(91)90020-3</a>[pdf](https://www.math.mcgill.ca/barr/papers/accll.pdf), [[Barr-AccCatLinearLogic.pdf:file]]&rbrack;

and a detailed review (also of a fair bit of plain monoidal category theory) is in 
 
* [[Paul-André Melliès]], _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))

Examples from algebraic geometry are given here:

* Mitya Boyarchenko and Vladimir Drinfeld, A duality formalism in the spirit of Grothendieck and Verdier, arXiv:1108.6020 ([pdf](http://arxiv.org/pdf/1108.6020v2.pdf))

These authors call any closed monoidal category with a [[dualizing object in a closed category|dualizing object]] a **Grothendieck-Verdier category**, thanks to the examples coming from [[Verdier duality]].

Here it is explained how $*$-autonomous categories give Frobenius pseudomonads in the 2-category where morphisms are [[profunctors]]:

*  [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Physics **45** (2004) 3930-3948 &lbrack;[pdf](http://www.math.mq.edu.au/~street/Frob.pdf)&rbrack;

Examples using toplogical vector spaces are given here:

* [[Michael Barr]], *On $*$-autonomous categories of topological vector spaces*, Cahiers de topologie et géométrie différentielle catégoriques **41** 4 (2000) 243-254 &lbrack;[numdan:CTGDC_2000__41_4_243_0] (http://www.numdam.org/item/CTGDC_2000__41_4_243_0.pdf)&rbrack;

Relation to [[linearly distributive categories]]:

* {#CockettSeely99} [[Robin Cockett]], [[Robert Seely]], _Linearly distributive functors_ (1999) &lbrack;<a href="https://doi.org/10.1016/S0022-4049(98)00110-8">doi:10.1016/S0022-4049(98)00110-8</a>&rbrack;
 

Combination with traces yields compact closure:

* {#HH13} Tamás Hajgató and [[Masahito Hasegawa]], *Traced $\ast$-autonomous categories are compact closed*, [TAC](http://www.tac.mta.ca/tac/volumes/28/7/28-07abs.html), 2013
 

A wide-ranging summary of different model constructions:

* {#HylandSchalk01 [[Martin Hyland]] and [[Andrea Schalk]], _Glueing and orthogonality for models of linear logic_, [pdf](http://www.cs.man.ac.uk/~schalk/publ/gomll.pdf)
 

The fact that a $\ast$-autonomous category for which there is a [[natural isomorphism]] $(A \otimes B)^\ast \simeq A^\ast \otimes B^\ast$ is a [[compact closed category]] has a purely [[string diagram|string diagrammatic]] proof, but it also follows from the implication (a)$\implies$ (b) of Theorem 1.3 in this paper:

* {#DP83} [[Albrecht Dold]], [[Dieter Puppe]], *Duality, Trace and Transfer*, Proceedings of the Steklov Institute of Mathematics **154** (1984) 85–103 &lbrack;[mathnet:tm2435](http://mi.mathnet.ru/tm2435), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/doldpup2.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/doldpup2.pdf)&rbrack;


According to Tobias Fritz (on the [Category Theory Community Server](https://categorytheory.zulipchat.com/#narrow/stream/229136-theory.3A-category-theory/topic/From.20*-autonomous.20to.20compact.20closed)):

>  They apparently didn't know about $\ast$-autonomous categories (which were introduced a few years prior to that), and their statement has slightly weaker assumptions in that they start with a natural isomorphism $\mathscr{C}(A \otimes B, I) \cong \mathscr{C}(A, B^*)$ only, but they also require the induced morphisms $A^* \otimes B^* \to (A \otimes B)^*$ to be isomorphisms.

See also:

* {#Barr96} [[Michael Barr]], *The Chu construction*, Theory Appl. Categories **2** 2 (1996) 17–35 &lbrack;[tac:2-02](http://www.tac.mta.ca/tac/volumes/1996/n2/2-02abs.html)&rbrack;

* [[Michael Barr]], *Topological $\ast$-autonomous categories*, Theory Appl. Categories, 16 (2006) 700–708 &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/mack.pdf), [[Barr-TopologicalStarAutonomous.pdf:file]]&rbrack;

* [[Michael Barr]], *Topological $\ast$-autonomous categories, revisited*, Tbilisi Math. J. **10** 3 (2017) 51–64 &lbrack;[arXiv:1609.04241](https://arxiv.org/abs/1609.04241)&rbrack;

* [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *The $\ast$-autonomous category of uniform sup semi-lattices*,  Theory and Applications of Categories **27** 11 (2012) 222–241 &lbrack;[tac:27-11](http://www.tac.mta.ca/tac/volumes/27/11/27-11abs.html)&rbrack;

With an eye towards apication in [[2d CFT]] (to [[representations]] of [[vertex operator algebras]] and their [[bimodules]]):

* [[Jürgen Fuchs]], [[Gregor Schaumann]], [[Christoph Schweigert]], [[Simon Wood]], *Grothendieck-Verdier duality in categories of bimodules and weak module functors* &lbrack;[arXiv:2306.17668](https://arxiv.org/abs/2306.17668)&rbrack;

For enriched *-autonomous categories, and *-autonomy for [[promonoidal categories]], see:

* [[Brian Day]] and [[Ross Street]], _Quantum categories, star autonomy, and quantum groupoids_ [arXiv:math/0301209](https://arxiv.org/abs/math/0301209) ([pdf](http://science.mq.edu.au/~street/Qcat.pdf)) (2003).


[[!redirects star-autonomous categories]]
[[!redirects *-autonomous category]]
[[!redirects *-autonomous categories]]
[[!redirects star-autonomous]]
[[!redirects *-autonomous]]

