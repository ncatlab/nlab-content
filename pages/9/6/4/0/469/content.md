
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

A *closed monoidal category* is a [[monoidal category]] $\big( \mathcal{C}, \, \mathbb{1},\, \otimes \big)$ that is also a [[closed category]], in a compatible way, i.e. such that for each [[object]] $Y \,\in\, \mathcal{C}$ 

1. the [[functor]] 

   $$
     (-) \otimes Y  \;\colon\; C \longrightarrow C
   $$ 

   of forming the [[tensor product]] with $Y$, 

1. has a [[right adjoint]] [[functor]] 

   $$
     [Y,-] \;\colon\; C \longrightarrow C
   $$ 

   forming the [[internal-hom]] out of $Y$

in that for all [[triples]] of [[objects]] $X,\, Y,\, Z $ there is a [[natural isomorphism|natural]] [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the following form:

$$
  Hom_{\mathcal{C}}(X \otimes Y,\, Z) 
    \;\simeq\; 
  Hom_{\mathcal{C}}\big(X, [Y,Z] \big)
  \,.
$$

The archetypical example is the [[cartesian closed category]] of [[Sets]], where the [[internal hom]] is given by forming [[function sets]], so that the above [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) expresses the fact that a [[function]] $(x,y) \mapsto f(x,y)$ of two variables is equivalently a function of a single variable with values in functions of the other variable: $x \mapsto \big(y \mapsto f(x,y) \big)$. In [[formal logic]] this is known as "[[currying]]".

More abstractly, from the point of view of [[2-category]] theory, closed monoidal categories may be regarded as a special case of the notion of [[closed pseudomonoids]] in a [[monoidal bicategory]].


## Definitions


### Symmetric closed monoidal category


A [[symmetric monoidal category|symmetric]] [[monoidal category]] $C$ is **closed** (cf. *[[symmetric monoidal closed category]]*) if for all [[objects]] $b \in C_0$ the [[tensor product]] [[functor]] $ b \otimes - \colon C \to C$ has a [[right adjoint]] functor $[b,-] \colon C \to C$.

$$
  \underset{b \in C}{\forall}
  \;\;
  C
  \underoverset
    {\underset{[b,-]}{\longrightarrow}}
    {\overset{b \otimes (-)}{\longleftarrow}}
    {\;\;\;\;\;\bot\;\;\;\;\;}
  C
  \,.
$$

This [means](adjoint+functor#InTermsOfHomIsomorphism) that for all $a,b,c \in C_0$ we have a [[natural bijection]]

$$
  Hom_C(a \otimes b, c) 
   \;\simeq\; 
  Hom_C(a, [b,c])
  \,,
$$

[[natural transformation|natural]] in all [[variables|arguments]].

The object $[b,c]$ is called the **[[internal hom]]** of $b$ and $c$. This is commonly also denoted by lower case $hom(b,c)$ (and then sometimes underlined).

### Cartesian closed monoidal category

If the monoidal structure of $C$ is [[cartesian monoidal category|cartesian]] (and so in particular [[symmetric monoidal category|symmetric monoidal]]), then $C$ is called **[[cartesian closed]]**.  In this case the internal hom is often called an **[[exponential object]]** and written $c^b$.

### Left-, right- and bi-closed monoidal category

If $C$ is [[monoidal category|monoidal]] but not necessarily [[symmetric monoidal category|symmetric]] or even [[braided monoidal category|braided]], then left and right [[tensor product]] $-\otimes b$ and $b\otimes -$ may be inequivalent functors, and either one or both may have an adjoint.  The terminology here is less standard, but many people use **left closed**, **right closed**, and **biclosed** monoidal category to indicate, respectively, that the left tensor product, the right tensor product functors or both have [[right adjoints]].  (Other authors simply say **closed** instead of biclosed.)  So in particular a symmetric closed monoidal category is automatically biclosed.

The analogue of exponential objects for monoidal categories are [[residual|left and right residuals]].

## Properties

+-- {: .num_prop #TensorHomIsoInternalizes} 
###### Proposition

For $(\mathcal{C}, \otimes, 1)$ a closed monoidal category with [[internal hom]] denoted $[-,-]$, then not only are there [[natural bijections]]

$$
   Hom_{\mathcal{C}}(X \otimes Y, Z)
  \simeq
   Hom_{\mathcal{C}}(X, [Y,Z])
$$

but these isomorphisms themselves "internalize" to isomorphisms in $\mathcal{C}$ of the form

$$
  [X \otimes Y, Z]
    \simeq
  [X,[Y,Z]]
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the external natural bijections there is for every $A \in \mathcal{C}$ a composite natural bijection

$$
  Hom_{\mathcal{C}}(A, [X \otimes Y, Z])
   \simeq
  Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
   \simeq
  Hom_{\mathcal{C}}((A \otimes X) \otimes Y, Z)
    \simeq
  Hom_{\mathcal{C}}(A \otimes X, [Y,Z])
    \simeq
  Hom_{\mathcal{C}}(A,[X,[Y,Z]])
  \,.
$$

Since this holds for every $A \in \mathcal{C}$, the [[Yoneda lemma]] (namely the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) implies that there is already an isomorphism

$$
  [X \otimes Y, Z] \simeq [X,[Y,Z]]
  \,.
$$

=--



## Examples
 {#Examples}

\begin{example}\label{ExampleSets}
The tautological example is the category [[Set]] of sets with its [[Cartesian product]] (a [[cartesian closed monoidal category]]): the collection of functions between any two sets is itself a set -- the [[function set]].  
\end{example}

\begin{example}\label{ExamplePresheaves}
In generalization of Exp. \ref{ExampleSets} and as a special case of Exp. \ref{FunctorCategory}, every [[category of presheaves]], i.e. every [[functor category]] of the form $Func(\mathcal{C}^{op}, Set)$, is a [[cartesian closed monoidal category]], details are spelled out at *[[closed monoidal structure on presheaves]]*.
\end{example}

\begin{example}
In further generalization of Exp \ref{ExamplePresheaves}, any [[topos]] is a [[cartesian closed monoidal category]].
\end{example}

\begin{example}\label{AbelianGroups}
The category [[Ab]] of [[abelian groups]] with its [[tensor product of abelian groups]] is (non-cartesian!) closed: for any two abelian groups $A, B$ the set of homomorphisms $A \to B$ carries (pointwise defined) abelian group structure. 
\end{example}

\begin{example}\label{ExampleModules}
In generalization of Exp. \ref{AbelianGroups} (which is the case $R =$ [[integers|$\mathbb{Z}$]]), for $R$ a [[commutative ring]], the category $R$[[Mod]] of $R$-[[modules]] with its usual [[tensor product of modules]] is (non-cartesian!) closed monoidal. This is one of the first hom-tensor adjunctions that appeared in [[algebra]].
\end{example}

\begin{example}
In specialization of Exp. \ref{ExampleModules} to the case that $R = \mathbb{K}$ is a [[field]], the category $\mathbb{K}$-[[Vect]] of $\mathbb{K}$-[[vector spaces]] and $\mathbb{K}$-[[linear maps]] between them is (non-cartesian!) closed monoidal with respect to the usual [[tensor product of vector spaces]]. Here the [[internal hom]] assigns vector spaces of [[linear maps]] (with the vector operations given argument-wise):

  $$
    V,\,W \,\in\, \mathbb{K}Vect
    \;\;\;\;\;\;\;\; \vdash \;\;\;\;\;\;\;\;
    [V,W]
    \;\coloneqq\;
    \left(
      \mathbb{K}Vec(V,W)
      ,\,
      \begin{array}{l}
       k \cdot f \,\colon\, v \mapsto k \cdot f(v)
       \\
       f + g \,\colon\, v \mapsto f(v) + g(v)
      \end{array}
    \right)
  $$
\end{example}

\begin{example}
A [[homotopical algebra|higher homotopical]] variant of Exp. \ref{ExampleModules}: For $R$ a [[commutative ring]] the [[category of chain complexes]] over $R$ is closed monoidal, via the [[tensor product of chain complexes]] and the [[internal hom of chain complexes]], see there for more.
\end{example}

\begin{example}
Given a closed monoidal category $C$ with [[equalizers]] and [[coequalizers]] and a [[commutative monad]] $T$, the category of [[algebra over a monad|$T$-algebras]] inherits a closed monoidal structure. See at *[[tensor product of algebras over a commutative monad]]*.
\end{example}

\begin{example}\label{FunctorCategory}
Let $C$ be a [[complete category|complete]] closed monoidal category and $I$ any [[small category]].  Then the [[functor category]] $[I,C]$ is closed monoidal with the pointwise tensor product, $(F\otimes G)(x) = F(x) \otimes G(x)$.
\end{example}
\begin{proof}
Since $C$ is complete, the category $[I,C]$ is [[comonadic functor|comonadic]] over $C^{ob I}$; the comonad is defined by right [[Kan extension]] along the inclusion $ob I \hookrightarrow I$.  Now for any $F\in [I,C]$, consider the following square:
$$
  \array{
    [I,C] 
    & \overset{F\otimes - }{\longrightarrow} & 
    [I,C] 
    \\
    \big\downarrow && \big\downarrow
    \\
    C^{ob I}
    & \underset{F_0 \otimes -}{\longrightarrow} & 
    C^{ob I}
  }
$$
This [[commuting diagram|commutes]] because the tensor product in $[I,C]$ is pointwise (here $F_0$ means the family of objects $F(x)$ in $C^{ob I}$).
Since $C$ is closed, $F_0 \otimes -$ has a [[right adjoint]].
Since the vertical functors are [[comonadic functor|comonadic]], the (dual of the) [[adjoint lifting theorem]] implies that $F\otimes -$ has a right adjoint as well.
\end{proof}


\begin{example}
A [[discrete category|discrete]] monoidal category (i.e., a [[monoid]]) is left closed iff it is right closed iff every object has an inverse, i.e. iff the monoid (aka [[semigroup]]) is in fact a [[group]].
\end{example}

\begin{example}
The [[delooping]] $\mathbf{B}M$ of a [[commutative monoid]] $M$ is a closed monoidal (in fact, [[compact closed]]) category with one object, with both the tensor and internal hom defined (on morphisms) using the multiplication operation $f \otimes g = [f,g] = f g$.  Conversely, any closed monoidal category with one object must be isomorphic to one constructed from a commutative monoid. (See [Eilenberg and Kelly (1965)](#EilenbergKelly65), IV.3, p.553.)
\end{example}

* Certain [[nice category of spaces|nice categories]] of [[topological spaces]] are cartesian closed: for any two nice enough topological spaces $X$, $Y$ the set of continuous maps $X \to Y$ can be equipped with a topology to become a nice topological space itself.

* Certain nice categories of _[[pointed object|pointed/based]]_  topological spaces are closed symmetric monoidal.  The monoidal structure is the [[smash product]] and the internal-hom is the set of basepoint-preserving maps with topology induced from the space of unbased ones.

* The category [[Cat]] is cartesian closed: the internal-hom is the [[functor category]] of functors and natural transformations. There is exactly one other closed monoidal structure on [[Cat]], given by the [[funny tensor product]].

* The category $2 Cat$ of [[strict 2-category|strict 2-categories]] and strict 2-functors is closed symmetric monoidal under the [[Gray tensor product]].  The internal-hom is the 2-category of strict 2-functors, _pseudo_ natural transformations, and modifications.

* The category of strict $\omega$-[[strict omega-category|categories]] is also biclosed monoidal, under the [[Crans-Gray tensor product]].

* If $M$ is a monoidal category and $Set^{M^{op}}$ is endowed with the tensor product given by the induced [[Day convolution]] product, then the [[category of presheaves]] $Set^{M^{op}}$ is biclosed monoidal. 

* The category of [[species]], with the monoidal structure given by substitution product of species, is closed monoidal (each functor $- \circ G$ admits a right adjoint) but not biclosed monoidal. 

* The category of [[modules]] over any [[Hopf monoid]] in a closed monoidal category, or more generally algebras for any [[Hopf monad]], is again a closed monoidal category.  In particular, the category of modules over any [[group object]] in a [[cartesian closed category]] is (cartesian) closed monoidal. For more on this phenomenon see at _[[Tannaka duality]]_.

* The category of [[locally convex topological vector spaces]] with the [[inductive tensor product]] and internal hom the space of continuous linear maps with the topology of pointwise convergence is symmetric closed monoidal.



## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* **closed monoidal category** ,  [[closed monoidal (∞,1)-category]]

  * [[doubly closed monoidal category]]

  * [[closed monoidal functor]]

  * [[internal hom]]

  * [[indexed closed monoidal category]]

  * [[cartesian closed category]], [[exponential object]]

* [[string diagram]], [[Kelly-Mac Lane diagram]], [[linguistics|natural language syntax]]


## References 


* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §III of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

Textbook accounts:

* {#MacLane97} [[Saunders MacLane]], VII.7 in: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**, Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Borceux94} [[Francis Borceux]], vol 2 section 6.1 of: _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)&rbrack;

Original articles studying monoidal biclosed categories are

* {#Lambek68} [[Joachim Lambek]], _Deductive systems and categories_, Mathematical Systems Theory 2 (1968), 287-318. 
 
* {#Lambek69} [[Joachim Lambek]], _Deductive systems and categories II_, Lecture Notes in Math. 86, Springer-Verlag (1969), 76-122. 



For more historical development see at _[linear type theory -- History of linear categorical semantics](linear+type+theory#HistoryCategoricalSemantics)_.

In [[enriched category theory]] the enriching category is taken to be closed monoidal. Accordingly the standard textbook on enriched category theory

* [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press 1982, 245 pp. ([ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029)); 

  republished as:

  Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

has a chapter on just closed monoidal categories.



[[!redirects closed monoidal category]]
[[!redirects closed monoidal categories]]
[[!redirects monoidal closed category]]
[[!redirects monoidal closed categories]]
[[!redirects closed monoidal structure]]
[[!redirects closed monoidal structures]]


[[!redirects biclosed monoidal category]]
[[!redirects biclosed monoidal categories]]
[[!redirects monoidal biclosed category]]
[[!redirects monoidal biclosed categories]]
[[!redirects left closed monoidal category]]
[[!redirects left closed monoidal categories]]
[[!redirects right closed monoidal category]]
[[!redirects right closed monoidal categories]]

[[!redirects hom-tensor adjunction]]
[[!redirects hom-tensor adjunctions]]
[[!redirects hom tensor adjunction]]
[[!redirects hom tensor adjunctions]]
