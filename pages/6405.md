
#Contents#
* table of contents
{:toc}

## Idea

Abelian varieties are higher dimensional analogues of [[elliptic curve]]s (which are included) -- they are [[varieties]] equipped with a structure of an [[abelian group]], hence abelian [[group schemes]], whose multiplication and inverse are regular maps.

## Definition


In his book _Abelian Varieties_, David Mumford defines an **abelian variety** over an algebraically closed field $k$ to be a [[complete algebraic variety|complete]] [[algebraic group]] over $k$.  Remarkably, any such thing is an _abelian_ algebraic group.  The assumption of connectedness is necessary for that conclusion.

##  Automatic abelianness

David Mumford gives at two proofs that every complete algebraic group over an algebraically closed field is automatically abelian.  One of them uses a 'rigidity lemma' which has an interesting category-theoretic interpretation.  We outline this here:

In simple terms, the rigidity lemma says that under certain circumstances "a 2-variable function $f(x,y)$ that is independent of $x$ for one value of $y$ is independent of $x$ for all values of $y$."   

More precisely, in a category with products, say a morphism $f: X \to Y$ is <b>constant</b> if it factors through the unique morphism $X \to 1$.  Say a morphism $f : X \times Y \to Z$ is <b>independent of $X$</b> if it factors through the projection $X \times Y \to Y$.   

Say a <b>point</b> of $Y$ is a morphism $p: 1 \to Y$.  Say a morphism $f: X \times Y \to Z$ is <b>independent of $X$ at some point $p$ of $Y$</b> if $f \circ (1_X \times p) : X \to Z$ is constant.

**Definition.** A category with finite products **obeys the rigidity lemma** if any morphism $f: X \times Y \to Z$ that is independent of $X$ at some point of $Y$ is in fact independent of $X$.

**Theorem 1.** The category of complete algebraic varieties over an algebraically complete field $k$ has finite products and obeys the rigidity lemma.

+-- {: .proof}
######Proof
The hard part, the rigidity lemma, is proved for complete algebraic varieties on page 43 of Mumford's _Abelian Varieties_.  Mumford mentions in a footnote that complete algebraic varieties are automatically irreducible, and he later seems to assume without much explanation that they are connected: these points could use some clarification, at least for amateurs. 
=-- 

**Theorem 2.** Suppose $G,H$ are group objects in a category $C$ with finite products obeying the rigidity lemma.  Suppose $f : G \to H$ is any morphism in $C$ preserving the identity.  Then $f$ is a homomorphism.

+-- {: .proof}
######Proof
The idea is this: suppose $C$ is a [[concrete category]] and look at the function $k : G \times G \to H$ given by

$$k(g,g') = f(g\cdot g')\cdot (f(g) \cdot f(g'))^{-1} $$

Assume $f(1) = 1$.  Then $k(1,g') = 1$ for all $g' \in G$, so by the rigidity lemma $k(g,g')$ is independent of $g'$ and we can write $k(g,g') = r(g)$.  Furthermore $k(g,1) = 1$ for all $g \in G$ so $k(g,g')$ is independent of $g$.  This means that $r(g)$ is independent of $g$, but $r(1) = k(1,1) = 1$ so $r(g) = 1$ for all $g$.  This says that $f(g \cdot g') = f(g) \cdot f(g')$, so $f$ preserves multiplication. This in turn implies that $f$ preserves inverses, so $f$ is a group homomorphism.

In fact a version of this argument works in any category with finite products obeying the rigidity lemma.  The expression $f(g\cdot g')\cdot (f(g) \cdot f(g'))^{-1}$ compiles to a particular morphism $G\times G \xrightarrow{k} H$.  The fact that $f$ preserves the identity $e_G:1\to G$ implies that both composites $G \xrightarrow{(id,e_G)} G\times G \xrightarrow{k} H$ and $G \xrightarrow{(e_G,id)} G\times G \xrightarrow{k} H$ are constant at the identity $e_H:1\to H$.  (This is a straightforward calculation in the internal logic of a category with products, or alternatively a slightly tedious diagram chase.)

In particular, $k$ is independent of the first $G$ in its domain at the point $e_G : 1\to G$ of the second $G$ in its domain.  So by the rigidity lemma, there exists a morphism $r : G\to H$ such that the composite $G\times G \xrightarrow{\pi_2} G \xrightarrow{r} H$ is equal to $k$.  Now precompose both of these with $G \xrightarrow{(e_G,id)} G\times G$: the first gives $r \circ \pi_2 \circ (e_G,id) = r$ and the second gives $k \circ (e_G,id) = e_H \circ !$.  Thus, $r$ is constant at the identity of $H$, and hence so is $k$.  This implies $f$ preserves multiplication, and thus also inverses (again, by a calculation in internal logic or a diagram chase).
=-- 

**Corollary 1.** If $C$ is a category with finite products obeying the rigidity lemma, any group object in $C$ is abelian.

+-- {: .proof}
######Proof
If $G$ is a group object in $C$, the inverse map $inv: G \to G$ preserves the identity, so by the above theorem it is a group homomorphism.  This in turn implies that $G$ is abelian.
=-- 

**Corollary 2.** Let $Var_*$ be the category of pointed complete varieties over an algebraically closed field $k$, and let $AbVar$ be the category of abelian varieties over $k$.  Then the forgetful functor $U : AbVar \to Var_*$ is full.

+-- {: .proof}
######Proof
This follows immediately from the two theorems above.
=-- 

A consequence of Corollary 2 is that if $Alb : Var_* \to AbVar$ is the left adjoint to $U$, sending any connected pointed projective variety to its Albanese variety, the monad $T = U \circ Alb$ is an [[idempotent monad]].  For more on this see [[Albanese variety]].

## Related concepts

* [[theta function]]

* [[Cartier duality]]

* [[dual abelian group scheme]]

* [[Albanese variety]]

## Literature

* C. Bartocci, [[Ugo Bruzzo]], D. Hernandez Ruiperez, _Fourier-Mukai and Nahm transforms in geometry and mathematical physics_, Progress in Mathematics 276, Birkhauser 2009.

* [[M. Demazure]], [[P. Gabriel]], _Groupes algebriques_, tome 1 (later volumes never appeared), Mason and Cie, Paris 1970 &#8211; has functor of points point of view; for review see Bull. London Math. Soc. (1980) 12 (6): 476-478, [doi](http://dx.doi.org/10.1112/blms/12.6.476b)

* [[Daniel Huybrechts]], _Fourier-Mukai transforms in algebraic geometry_, Oxford Mathematical Monographs. 2006. 307 pages.

* J. S. Milne, _Abelian varieties_, course notes, [pdf](http://www.jmilne.org/math/CourseNotes/AV.pdf)

* David Mumford, _Abelian varieties_, Oxford Univ. Press 1970.

* [[Alexander Polishchuk]], _Abelian varieties, theta functions and the Fourier transform_, Cambridge Univ. Press 2003.

* Goro Shimura, _Abelian varieties with complex multiplication and modular functions_, Princeton Univ. Press 1997.

* [[André Weil]], _Courbes alg&#233;briques et vari&#233;t&#233;s ab&#233;liennes_, Paris: Hermann 1971

In [[E-infinity geometry]]:

* {#LurieI} [[Jacob Lurie]], _Elliptic Cohomology I: Spectral Abelian Varieties_ ([pdf](http://www.math.harvard.edu/~lurie/papers/Elliptic-I.pdf))


For a discussion of how the rigidity lemma gives 'automatic abelianness' see:

* [Two miracles in algebraic geometry](https://golem.ph.utexas.edu/category/2016/08/the_magic_of_algebraic_geometr.html), _The n-Category Caf&eacute_.


[[!redirects abelian varieties]]
[[!redirects abelian group scheme]]
[[!redirects abelian group schemes]]
