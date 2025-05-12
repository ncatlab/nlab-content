
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of  _lax natural transformation_ is a generalization of the notion of [[natural transformation]] from [[category theory]] to [[higher category theory]].

As a natural transformation is a [[morphism]] between two [[functor]]s between [[categories]], a lax natural transformation is a morphism between [[2-functors]] between [[2-categories]]:

Where a natural transformation has a [[commutative square|commuting]] naturality square, a lax natural transformation has a [[2-morphism]] filling that square.  If that 2-morphism is required to be invertible, one speaks of a [[pseudonatural transformation]], and if it is required to be an identity (which implies that the square commutes), then one speaks of a [[strict 2-natural transformation]] (this latter notion only really makes sense for [[strict 2-functors]] between [[strict 2-categories]]).

In the general terminology of [[higher category theory]], a lax natural transformation may equivalently be called a (lax) [[k-transfor|1-transfor]].


## Definitions ##

Given (possibly weak) [[2-categories]] $C,D$ and (possibly [[lax functor|lax]] or oplax) [[2-functors]]
$F, G : C\to D$, a __lax natural transformation__ $\alpha:F\Rightarrow G$
is given by

* for each $A\in C$ a [[1-morphism]] $\alpha_A:F(A)\to G(A)$ in $D$,
as usual

* for each $f:A\to B$ in $C$ a [[2-morphism]] $\alpha_f: G(f) \circ
\alpha_A \Rightarrow \alpha_B \circ F(f)$:

\begin{tikzcd}
F A \ar[r,"F(f)"] \ar[d,"\alpha_A"']\ar[dr,phantom,"\Rightarrow"] & F B \ar[d,"\alpha_B"]\\
G A \ar[r,"G(f)"'] & G B
\end{tikzcd}

such that

* for each $A,B$, the $\alpha_f$ are the components of a
(strict) [[natural transformation]] $\alpha_{A,B}:
(\alpha_A)^* \circ G_{A,B} \dot{\to} (\alpha_B)_* \circ
F_{A,B}$

* the assignment $f\mapsto \alpha_f$ behaves sensibly with
respect to identities and composition (see the
references for details).

An __oplax natural transformation__ is as above, only with the $2$-cells $\alpha_f$ reversed.  This distinction is not entirely consistent in the literature; see the discussion of terminology below.

An (op)lax natural transformation $\alpha$ is a __[[pseudonatural transformation]]__ if each $\alpha_f$ is [[isomorphism|invertible]], and a __strict natural transformation__ or __[[strict 2-natural transformation]]__ if each is an [[identity morphism|identity]].  

In all of these cases, the word 'natural' is often dropped for brevity.


## Categories and $n$-categories of lax transformations ##

Lax transformations from $F$ to $G$ and [[modification]]s between them form a [[category]] $Lax(F,G)$; likewise we have $Ps(F,G)$ and $Oplax(F,G)$ consisting of pseudo-natural and oplax transformations, respectively.

Pushing it up a notch, for 2-categories $C$ and $D$ we have hom-2-categories $2Cat_{lax}(C,D)$, $2Cat_{ps}(C,D)$, and $2Cat_{oplax}(C,D)$ whose objects are 2-functors (generally taken to be strong or strict), whose morphisms are lax, pseudo, or oplax transformations respectively, and whose 2-cells are modifications.  These hom-2-categories are the [[internal homs]] for the various version of the [[Gray tensor product]] on $2Cat$.

Finally, there is a [[3-category]] consisting of 2-categories, (strong or strict) 2-functors, pseudo-natural transformations, and modifications.  No laxness is possible at this level (without "laxifying" the notion of 3-category).


## "Lax" versus "oplax" ##

The choice of which direction to call "lax" and which to call "oplax" is not made consistently in the literature.  The convention used above is Benabou's original choice, as well as that of Leinster, Borceaux, and the majority of Australian writing on category theory.  However, some references, such as the [[Elephant]], make the opposite choice.  One or two references use "left lax" and "right lax" instead.

It is arguably the case that the direction we call "oplax" occurs more commonly in practice.  For instance, [[icons]] are a special sort of oplax transformations (although if "lax" and "oplax" were switched, then the acronymic derivation of the word "icon" would no longer work).  Likewise, when monoidal categories are viewed as one-object 2-categories, [[monoidal natural transformation]]s are special oplax transformations (in fact, they are precisely the icons).

On the other hand, the convention used above (besides having a little more weight of tradition) has the advantage that there is a [[2-monad]] whose algebras are 2-functors, and for which [[lax morphism|lax and oplax algebra morphisms]] are precisely lax and oplax transformations, respectively, under this convention.  Thus, for instance, theorems such as [[doctrinal adjunction]] can be applied to lax and oplax transformations without needing to switch back and forth between two different meanings of "lax."


## The Yoneda Lemma ##

Given a bicategory $C$, a lax functor $F:C^{op}\to Cat$ and a $0$-cell $A\in C$, there
are [[adjoint functor]]s

$$ I : Lax(y A,F) \stackrel{\to}{\leftarrow} F(A) : J $$

such that $J \dashv I$.  Here $y A:C \to Cat^{C^{op}}$ is the image of $A$ under the
bicategorical [[Yoneda embedding]].

+-- {: .proof}
###### Proof (sketch)

For $a\in F(A)$, let $J(a):y A\Rightarrow F$ be the lax transformation defined by $J(a)_B(f) = (F f)(a)$.  The components

$$  J(a)_g : F(g) \circ J(a)_X \dot{\to} J(a)_Y \circ g_* $$

for $g:X\to Y$ in $C$ are given by $F$'s comparison map $(F_{g,-})_a$.  The coherence conditions follow from those on $F$ wrt the associator and left unitor of $C$.  For $x:a\to b$ in $F(A)$, $J(x)$ is a modification because $F_{g,f}$ is a natural transformation (i.e. 2-cell in $Cat$).

Let $I(\alpha) = \alpha_A(1_A)$ as usual.  For $m:\alpha\ddot{\to}\beta$ a modification, $I(m)=(m_A)(1_A)$.

The unit $\eta: F A \dot{\to} I J$ at $a\in F A$ is the component $(F_A)_a$ of $F$'s comparison map, which is natural in $a$ by definition.  The counit $\epsilon_\alpha$ is obtained via the usual 1-chasing, and is given in components by

\[ (\epsilon_\alpha)_B(f) = \alpha_B(r_f) \circ (\alpha_f)(1_A) \]

where $r$ is the right unitor of $C$.  Some diagram-chasing confirms that this is indeed natural in everything, and so $\epsilon: J I \dot{\to} Lax(y A,F)$.

The triangle identities may be proved by expanding the definitions above and using the coherence conditions on lax functors and transformations and coherence of $C$.

See Gray for the case [[strict 2-categories]] and strict 2-functors.
=--

## Related concepts

* [[homotopy]]

* [[transfor]]

  * [[natural transformation]]

    * [[extranatural transformation]], [[dinatural transformation]]

  * [[pseudonatural transformation]]

    * [[pseudo-extranatural transformation]]

  * **lax natural transformation**

  * [[2-dinatural transformation]]

  * [[lax F-natural transformation]]



## References ##

See the references at [[2-category]]. For instance (note slightly outdated terminology)

* Gray, _[[Gray-adjointness-for-2-categories|Adjointness For
2-Categories]]_

The definition is spelled out explicitly in the following, where they are called *lax transformations*:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

In the following **oplax natural transformations** are defined, but called, simply, "transformations":

* [[Tom Leinster]], _Basic bicategories_,
[arXiv:math/9810017](http://arxiv.org/abs/math/9810017).

* [[Ross Street]], _Two constructions on lax functors_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 13 (1972) no. 3 , p. 217-264 [numdam](http://www.numdam.org/item?id=CTGDC_1972__13_3_217_0)

[[!redirects lax natural transformations]]
[[!redirects lax transformation]]
[[!redirects lax transformations]]
[[!redirects oplax natural transformation]]
[[!redirects oplax natural transformations]]
[[!redirects oplax transformation]]
[[!redirects oplax transformations]]

[[!redirects lax 2-natural transformation]]
[[!redirects lax 2-natural transformations]]
[[!redirects oplax 2-natural transformation]]
[[!redirects oplax 2-natural transformations]]
