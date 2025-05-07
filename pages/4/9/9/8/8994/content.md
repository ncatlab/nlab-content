
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **linearly distributive category** is a [[category]] with two [[monoidal structures]] $\otimes$ ("times") and $\oplus$ ("par" written as $\invamp$ in linear logic)  that "distribute" in the sense that there is a map (not necessarily invertible)

$$
   \delta \colon A \otimes (B \oplus C) \longrightarrow (A \otimes B) \oplus C
$$

Linearly distributive categories are the "representable" form of [[polycategories]], and they are also what "remains" of a [[star-autonomous category]] when the involution is forgotten but the dual tensor $A\invamp B \coloneqq (A^* \otimes B^*)^*$ is remembered.

Another way to say essentially the same thing is that a $\ast$-autonomous category is like a [[compact closed category]] in which the [[unit]] and [[counit]] of the [[dual objects]] refer to two different tensor products: we have $\top \to A \oplus A^*$ but $A^* \otimes A \to \bot$, where $(\otimes,\top)$ and $(\oplus,\bot)$ are two different monoidal structures.  A linearly distributive category encodes the necessary relationship between two such monoidal structures such that this makes sense, i.e. such that the [[triangle identities]] can be stated.

## Definition

A **linearly distributive category** (also called a **weakly distributive category**) is a [[monoidal category]] in two ways, with monoidal structures $(\otimes, \top)$ and $(\oplus, \bot)$ equipped with extra associator natural transformations

\[ \delta^L:A \otimes (B\oplus C) \to (A \otimes B) \oplus C \]

\[ \delta^R:(A \oplus B) \otimes C \to A \oplus (B \otimes C) \]

and the obvious six pentagon equations and four triangle equations that make the monoidal structures work together nicely ([Cockett-Seely 1997](#CockettSeely97)).  (Some of these equations can be interpreted as saying that the $\delta$s are [[tensorial strengths]] for the functors $(A\oplus -)$ and $(-\oplus C)$ with respect to the $\otimes$ monoidal structure.)  A **symmetric linearly distributive category** is one in which both monoidal structures are symmetric and three squares commute relating the symmetries to the $\delta$s.

These extra associators are sometimes called "distributors", and should not be confused with [[profunctors]].  The term is a pun on the distributivity of multiplication over addition, but "linearized" so that each variable only appears once in the result.

In a symmetric LDC, the symmetry maps induce the following **permuting** distributivity maps:
\[ \delta^L_R : A \otimes (B \oplus C) \to B \oplus (A \otimes C) \]
 
\[  \delta^R_L : (B \oplus C) \otimes A \to (B \otimes A) \oplus C \]

An LDC which is equipped with all the four linear distributivity maps is said to be **non-planar**.

**Warning:** a [[distributive category]] *cannot* be made into a linearly distributive category with $\otimes = \times$ and $\oplus = +$ unless it is a [[partial order]] (but every [[distributive lattice]] is indeed a linearly distributive category) (for a proof, see [Cockett-Seely 1997](#CockettSeely97)).  This mistake is easy to make and even appears in print in one or two places.

## Examples

* Any [[star-autonomous category]] is linearly distributive, with $A \oplus B = (A^* \otimes B^*)^*$.  See that page for many examples of this.

* Any [[distributive lattice]] is linearly distributive, with $A\otimes  B = A\wedge B$ and $A\oplus B = A\vee B$.  (This does *not* extend to [[distributive categories]].)

* Any monoidal category is linearly distributive trivially with $\oplus = \otimes$.

* If $D$ is an [[invertible object]] in a monoidal category, then defining $A\oplus B = A\otimes D \otimes B$ yields a linearly distributive structure whose linear distributors are isomorphisms.

* The category of modules for a [[bialgebra]] in any linearly distributive category (hence, in particular, in any [[star-autonomous category]]) is again linearly distributive.  It is generally only star-autonomous if the bialgebra is a [[Hopf algebra]].

## Linear functors and transformations

A **linear functor** $F:C\to D$ between linearly distributive categories consists of a pair of functors $F_\otimes, F_\oplus$ such that, $F_\otimes$ is a [[lax monoidal functor]] with respect to $\otimes$, $F_\oplus$ is a [[colax monoidal functor]] with respect to $\oplus$, and there are "linear strengths"

$$ F_\otimes (A\oplus B) \to F_\oplus(A) \oplus F_\otimes (B) $$

$$ F_\otimes (A\oplus B) \to F_\otimes(A) \oplus F_\oplus(B) $$

$$ F_\otimes (A) \otimes F_\oplus(B) \to F_\oplus(A\otimes B)$$

$$ F_\oplus (A) \otimes F_\otimes(B) \to F_\oplus(A\otimes B)$$

satisfying appropriate coherence conditions ([Cockett-Seely 1999](#CockettSeely99)).  A **linear natural transformation** $\alpha: F\to G$ consists of a monoidal transformations $\alpha_\otimes: F_\otimes \to G_\otimes$  and $\alpha_\oplus: G_\oplus \to F_\oplus$ satisfying further coherence conditions.  This defines a 2-category of linearly distributive categories, which has the property of embedding the 2-category of $\ast$-autonomous categories and arbitrary lax monoidal functors (see below).

On the other hand, a linear functor in this sense is more general than a functor between underlying [[polycategories]] (see below).  The latter probably coincide with linear functors having the property that $F_\otimes = F_\oplus$ as functors (so that the same functor $F$ is $\otimes$-lax monoidal and $\oplus$-colax monoidal) and the linear strengths are identities.  We might call these **Frobenius linear functors**, since such a $1\to C$ is the same as a [[Frobenius algebra]] in $C$, and when specialized to the monoidal case $\otimes=\oplus$ they coincide with [[Frobenius monoidal functors]].

Yet stronger is the notion of *strong* Frobenius linear functor, in which the lax and colax monoidal structures are [[strong monoidal functor|strong]].


## Related structures


### Mix, isomix and compact linearly distributive categories

There are a series of structural steps by which linearly distributive categories collapses to a monoidal categories as shown in the picture below. 

\begin{center}
\begin{imagefromfile}
        "file_name": "LDC_schematic.jpg",
        "width": 600,
        "unit": "px"
\end{imagefromfile}
\end{center}
 
A **mix category** is an LDC with a **mix map** ${ m}:\bot\to\top$, and a  such that:

1) The following diagram commutes

\begin{tikzcd}
	{A \otimes B} & {A \otimes(\bot \oplus B)} & {(A \otimes \bot) \oplus B} \\
	{(A \oplus \bot) \otimes B} && {(A  \otimes \top) \oplus B} \\
	{A \oplus ( \bot \otimes B)} & {A \oplus ( \top \otimes B)} & {A \oplus B}
	\arrow["\simeq", from=1-1, to=1-2]
	\arrow["\simeq"', from=1-1, to=2-1]
	\arrow["{{mx} := }"{description}, dashed, from=1-1, to=3-3]
	\arrow["{\delta^L}", from=1-2, to=1-3]
	\arrow["{A \otimes {m} \oplus B}", from=1-3, to=2-3]
	\arrow["{\delta^R}"', from=2-1, to=3-1]
	\arrow["\simeq", from=2-3, to=3-3]
	\arrow["{A \oplus {m} \otimes B}"', from=3-1, to=3-2]
	\arrow["\simeq"', from=3-2, to=3-3]
\end{tikzcd}


2) The map, $\mx_{A,B}: A \otimes B \to A \oplus B$, called the mixor is natural in both the arguments.

An **isomix category** is a mix category in which the mix map is a natural isomorphism, $m: \bot \simeq \top$.

In an isomix category, the mixor is automatically a natural transformation. The mix map being an isomorphism does not imply that the mixor is a natural isomorphism.

An isomix category in which the mixor is a natural isomorphism is a **compact LDC**. The term "compact" here refers to the fact that both the monoidal structures are isomorphic. All compact LDCs are linearly equivalent to the underlying monoidal categories on the tensor $\otimes$ and the par $\oplus$.

### Star-autonomous category

Any [[star-autonomous category]] has an underlying symmetric linearly distributive category where we define $A\oplus B \coloneqq (A^* \otimes B^*)^*$, or equivalently $A\oplus B \coloneqq A^* \multimap B$, where $\multimap$ is the internal-hom.  The left distributor, for instance, is obtained as follows:
$$\array{\arrayopts{\rowlines{solid}}
\array{\arrayopts{\rowlines{solid}}
(A\otimes B)^* \longrightarrow (A\otimes B)^* \\
A \otimes (A\otimes B)^* \longrightarrow B^*} \qquad
\array{\arrayopts{\rowlines{solid}}
B^* \multimap C \longrightarrow B^* \multimap C\\
B^* \otimes (B^* \multimap C) \longrightarrow C\\
B^* \longrightarrow (B^* \multimap C) \multimap C} \\
A \otimes (A\otimes B)^* \longrightarrow (B^* \multimap C) \multimap C \\
A\otimes (B^*\multimap C) \longrightarrow (A \otimes B)^* \multimap C
}$$

Conversely, we say that a symmetric linearly distributive category with monoidal structures $(\otimes,\top)$ and $(\oplus,\bot)$ has a **negation** if every object $A$ has a [[dualizable object|dual]] $\neg A$ and arrows

$$\top \to A \oplus \neg A, \qquad \neg A \otimes A \to \bot$$ 

subject to triangular equations 

$$1_A = \left( A \cong \top \otimes A \to (A \oplus \neg A) \otimes A \stackrel{dist}{\to} A \oplus (\neg A \otimes A) \to A \oplus \bot \cong A \right)$$ 

$$\,$$ 

$$1_{\neg A} = \left( \neg A \cong \neg A \otimes \top \to \neg A \otimes (A \oplus \neg A) \stackrel{dist}{\to} (\neg A \otimes A) \oplus \neg A \to \bot \oplus \neg A \cong \neg A \right).$$ 

Then symmetric linearly distributive categories with negations are the same as $\ast$-autonomous categories; see ([Cockett-Seely 1997](#CockettSeely97)).  Moreover:

* the [[forgetful functor]] from $\ast$-autonomous categories to symmetric linearly distributive ones has a [[left adjoint]] that "freely adjoins negations".  I don't know which kind of functors this statement refers to, but it's probably strong Frobenius ones.

* This functor also has a [[right adjoint]] that picks out (in the linear sense) the "nucleus" of [[dualizable objects]] ([Cockett-Seely 1999](#CockettSeely99)).  This adjunction uses lax monoidal functors between $\ast$-autonomous categories and linear functors between linearly distributive categories.

* Analogous facts hold relating non-symmetric linearly distributive categories with [[non-symmetric star-autonomous categories]].


### Polycategories

Any linearly distributive category has an underlying [[polycategory]] where we define $Hom(A_1,\dots,A_n; B_1,\dots,B_m)$ to be $Hom(A_1\otimes \cdots \otimes A_n; B_1 \oplus \cdots \oplus B_m)$.
The polycategorical compositions are obtained using the distributors.  For instance, we should be able to compose $f:(A,B) \to (C,D,E)$ with $g:(F,D,G) \to H$ to get $g\circ f : (F,A,B,G) \to (C,H,E)$; in a linearly distributive category this is the composite
$$\begin{aligned}
  F\otimes (A\otimes B)\otimes G
  &\xrightarrow{1_F\otimes f\otimes 1_G} F\otimes (C\oplus D\oplus E)\otimes G\\
  &\xrightarrow{\delta} ((F\otimes (C\oplus D)) \oplus E)\otimes G\\
  &\xrightarrow{\delta} ((C\oplus (F\otimes D)) \oplus E)\otimes G\\
  &\xrightarrow{\cong} ((C\oplus E) \oplus (F\otimes D))\otimes G\\
  &\xrightarrow{\delta} (C\oplus E) \oplus ((F\otimes D)\otimes G)\\
  &\xrightarrow{1_{C\oplus E}\oplus g} (C\oplus E) \oplus H\\
  &\xrightarrow{\cong} C\oplus H\oplus E
\end{aligned}$$
Conversely, a polycategory that is suitably "representable" yields a linearly distributive category.  Also, the forgetful functor from linearly distributive categories and *strong Frobenius* linear functors to polycategories has a left adjoint ([Cockett-Seely 1997](#CockettSeely97)).


### Symmetric monoidal categories

Any [[symmetric monoidal category]] becomes a linearly distributive category in which both monoidal structures are the same; all the required structure and coherence conditions follow straight from coherence for symmetric monoidal categories.  Note that such examples are almost never [[star-autonomous]].

These examples satisfy the extra property that the distributors $\delta$ are [[isomorphisms]].  However, not every linearly distributive category in which the distributors are isomorphisms are of this form; the rest are "shifted monoidal categories" in which $A \oplus B \coloneqq A \otimes \bot^{-1} \otimes B$, where $\bot$ is a chosen $\otimes$-invertible object.

### Linear bicategories

[[linear bicategory|Linear bicategories]] are a [[horizontal categorification]] of linearly distributive categories ([Cockett-Koslowski-Seely 1999](#CKS99)).

## Internal structures

Some structures normally defined in a monoidal category can more generally be defined in a linearly distributive category.  This includes [[dual objects]] (yielding the above "negations") and also [[Frobenius algebras]] ([Egger 2010](#Egger2010)).

## As lax Frobenius algebras

Linearly distributive categories that are both closed and co-closed can be identified with lax [[Frobenius algebras]] in the [[polycategory]] [[MVar]] of [[multivariable adjunctions]]; see [this blog post](https://golem.ph.utexas.edu/category/2017/11/starautonomous_categories_are.html).

## History

A key feature of linearly distributive categories is the existence of [[morphisms]] of the form

$$
   \delta \colon A \otimes (B \oplus C) \longrightarrow (A \otimes B) \oplus C
$$

which exhibit linear [[distributivity]].  The importance of this map had previously  been overlooked in the [[linear logic]] community due to the (continuing) tendency to write [[sequents]]  in a one-sided manner.  However, the importance of the map was eventually realized by a number of people, albeit usually in the case of [[posets]]. [Cockett-Seely 1997](#CockettSeely97) referred to [Lambek 1993](#Lambek93) for a survey of some of those developments.

This concept was called a _weakly distributive category_  when it was presented by [[Robin Cockett]] and [[Robert Seely]] at the 1991 Durham LMS symposium on applications of categories in computer science ([Cockett-Seely 1992](#CockettSeely92) and [Cockett-Seely 1997](#CockettSeely97)). Independently, [[Valeria de Paiva]], a student of [[Martin Hyland]], also presented this concept in her PhD thesis as the category $\mathbf{GC}$, and credited conversations with [[Jean-Yves Girard]] at a 1987 Boulder conference for inspiring the construction. ([de Paiva 1991](#dePaiva91))

Subsequently, in recognition of the concept's fundamental role in the [[categorical semantics]] for the [[proof theory]] of [[linear logic]], and the fact that such categories are not a "weakening" of [[distributive categories]] in any standard sense, these categories were called _linearly distributive categories_.

Linearly distributive categories allowed the modularization of the [[proof theory]] of [[linear logic]] and a more systematic approach to the then unsolved [[coherence]] problems associated with the units in linear logic. This program of work culminated in a solution which was published in ([BCST 1996](#BCST))

These techniques also solved a classical open problem in [[closed monoidal categories]] concerning the behaviour of the triple dual.  [[Todd Trimble]], who was completing his PhD. at the time, provided a vital insight to the group on how this problem could be solved and this unlocked the solution to the general problem.

Linearly distributive categories are to [[polycategories]] as [[monoidal categories]] are to [[multicategories]].  Namely, when one represents "the commas" of a polycategory one obtains a linearly distributive category.  Crucially, the key coherence issues of (the multiplicative fragment of) linear logic concerning the units is already present at the linearly distributive level -- but it is no longer cluttered by the other features of linear logic.  Thus, this provided a clean substrate from which to study and isolate this coherence problem.

Contrary to the general direction of work in coherence (and, indeed, in the linear logic community), the solution to the problem, which was given in ([BCST 1996](#BCST)), involved an expansion reduction rewriting system modulo equations. At that time, the prevailing proof theoretic strategy for solving coherence problems was simply to [[cut elimination|cut-eliminate]]: usually this suffices to leave proofs in a normal form. However, this system was notable as this strategy clearly failed: it was necessary to leave some equations in the system. These equations, of course, involved the possible "rewiring"s of the units.  

At that time this was generally thought to be a rather unsatisfactory and unnecessarily technical solution especially when compared to the normal forms to which the community was accustomed. However, in 2014, Willem Heijltjes and Robin Houston ([HH2014](#HH)) showed that equality of morphism is a [[PSPACE]]-complete problem. This essentially implies that there is no practical way round this problem beyond a search of the rewiring equivalence class.

Linearly distributive categories have now been used as the substrate for a number of systems. 

## Related pages

* [[distributive law]]

* [[distributivity for monoidal structures]]

  * [[distributive monoidal category]]

  * [[bipermutative category]]

  * [[linearly distributive category]]

  * [[rig category]]

* [[polycategory]], [[star-autonomous category]]

* A linearly distributive category in which the units of the two monoidal structures coincide is an (iso-)[[mix category]].

* [[linear bicategory]]

## References

* {#Szabo} M.E. Szabo, *Polycategories*, Comm. Algebra 3 (1975) 663-689.  ([doi](http://www.tandfonline.com/doi/abs/10.1080/00927877508822067))

* {#dePaiva91} [[Valeria de Paiva]], _The Dialectica categories_, University of Cambridge Technical Report UCAM-CL-TR-213, 1991. ([pdf](http://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-213.pdf))

* {#CockettSeely92} [[Robin Cockett]], [[Robert Seely]],  _Weakly Distributive Categories_, in M.P. Fourman, P.T. Johnstone, A.M. Pitts, eds., _Applications of Categories in Computer Science_, London Mathematical Society Lecture Note Series 177 (1992), pp. 45&#8211;65. ([book website](https://www.cambridge.org/au/academic/subjects/mathematics/logic-categories-and-sets/applications-categories-computer-science-proceedings-london-mathematical-society-symposium-durham-1991))

* {#Lambek93} [[Joachim Lambek]], _From categorial grammar to bilinear logic_, in Kosta Dosen and Peter Schroder-Heister, eds., _Substructural Logics_, Clarendon Press, 1993, pp. 207&#8211;237. ([book website](https://global.oup.com/academic/product/substructural-logics-9780198537779))

* {#BCST}  [[Richard Blute|R. Blute]], [[Robin Cockett|J.R.B. Cockett]], [[Robert Seely|R.A.G. Seely]], [[Todd Trimble|T. Trimble]], _Natural deduction and coherence for weakly distributive categories_, J. Pure Appl. Algebra, 113 (1996), pp. 229&#8211;296. ([web](http://www.sciencedirect.com/science/article/pii/002240499500159X)) 

* {#CockettSeely97} [[Robin Cockett]], [[Robert Seely]],  _Weakly Distributive Categories_, J. Pure Appl. Algebra, 114 (1997) 2, pp 133-173. (corrected version: [ps.gz](http://www.math.mcgill.ca/rags/linear/wdc.ps.gz), [pdf](http://www.math.mcgill.ca/rags/linear/wdc-fix.pdf))

* {#CockettSeely99} [[Robin Cockett]] and [[Robert Seely]], _Linearly distributive functors_, J. Pure Appl. Algebra 143 (1999), pp. 155&#8211;203. ([doi](https://doi.org/10.1016/S0022-4049%2898%2900110-8))

* [[Paul-André Melliès]], [Categorical Semantics of Linear Logic](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf), published in [[Pierre-Louis Curien]], Hugo Herbelin, Jean-Louis Krivine, Paul-Andr&#233; Melli&#232;s. _Interactive models of computation and program behaviour_, Panoramas et Synth&#232;ses 27, Soci&#233;t&#233; Math&#233;matique de France, 2009. 

* {#HH} Willem Heijltjes, [[Robin Houston]], _No proof nets for MLL with units: proof equivalence in MLL is PSPACE-complete_, CSL-LICS '14 Proceedings of the Joint Meeting of the Twenty-Third EACSL Annual Conference on Computer Science Logic (CSL) and the Twenty-Ninth Annual ACM/IEEE Symposium on Logic in Computer Science (LICS), Article No. 50. ([web](http://dl.acm.org/citation.cfm?id=2603126)) 

* {#CKS99} [[Robin Cockett]], [[Jürgen Koslowski]], [[Robert Seely]], *Introduction to linearly distributive categories*, Mathematical Structures in Computer Science, Vol. 10, 2000 pp 165-.203 [pdf](https://www.math.mcgill.ca/rags/bicats/bicat.pdf)

* {#CS97}[[Robin Cockett]] and [[R.A.G. Seely]], 1997. _Proof theory for full intuitionistic linear logic, bilinear logic, and mix categories_. 1997. [[TAC]] 5:3. [Web](http://tac.mta.ca/tac/volumes/1997/n5/3-05abs.html).

 
Frobenius algebras in linearly distributive categories are discussed in

* {#Egger2010} [[Jeff Egger]], *The Frobenius relations meet linear distributivity*, Theory and Applications of Categories, Vol. 24, 2010, No. 2, pp 25-38. ([web](http://tac.mta.ca/tac/volumes/24/2/24-02abs.html))


[[!redirects weakly distributive category]]
[[!redirects weakly distributive categories]]

[[!redirects linearly distributive categories]]