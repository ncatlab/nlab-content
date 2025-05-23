
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Gelfand duality_ is a [[Isbell duality|duality between spaces and their algebras of functions]] for the case of [[compact space|compact]] [[topological space]]s and [[commutative C-star-algebra|commutative]] [[C-star algebras]]:

> Every (nonunital) commutative $C^\ast$-algebra $A$ is equivalent to the $C^\ast$-algebra of [[continuous functions]] on the [[topological space]] called its _[[Gelfand spectrum]]_ $sp(A)$.

This theorem is the basis for regarding non-commutative $C^\ast$-algebras as formal duals to spaces in [[noncommutative geometry]].

## Definitions

The statement of Gelfand duality involves the following [[categories]] and [[functors]].

+-- {: .num_defn}
###### Definition

Write

* $C^\ast Alg$ for the category of unital [[C-star algebras]];

* $C^\ast Alg_{nu}$ for the category of nonunital $C^\ast$-algebras;

* $C^\ast Alg_{nu,nd}$ for the sub category of nonunital $C^\ast$-algebras
with morphisms being nondegenerate [[C-star algebra|$C^\ast$-algebra]][[homomorphisms]],
i.e., the two-sided ideal generated by the image is dense in the codomain.

* $C^\ast Alg_{com}$, $C^\ast Alg_{com,nu}$, $C^\ast Alg_{com,nu,nd}$
for the full subcategories of the above three categories consisting
of commutative C\*-algebras.

And

* [[Top]]${}_{Haus}$ for the category of [[Hausdorff topological spaces]]

* $Top_{cpt}$ for the [[full subcategory]] of [[Top]]${}_{Haus}$ of the [[compact topological spaces]];

* $*/Top_{cpt}$ for the category of [[pointed topological space|pointed topological]] [[compact Hausdorff spaces]], i.e. the [[pointed objects]] in $Top_{cpt}$;

* $Top_{lcpt,proper}$ for the category of Hausdorff and [[locally compact topological spaces]] with morphisms being the [[proper maps]] of topological spaces.

* $Top_{lcpt,inf}$ for the category of Hausdorff and [[locally compact topological spaces]] with morphisms being the [[continuous maps]] that vanish at infinity.

=--

The duality itself is exhibited by the following [[functors]]:

+-- {: .num_defn #FunctorsOfFunctionAlgebras}
###### Definition

Write 
$$
  C \;\colon\; Top_{cpt} \to C^\ast Alg_{com}^{op}
$$ 
for the functor which sends a [[compact topological space]] $X$ to the algebra of [[continuous function]]s $C(X) = \{f : X \to \mathbb{C} | f \; continuous\}$, equipped with the structure of a $C^\ast$-algebra in the evident way (...).

Write
$$
  C_0 \;\colon\; */Top_{cpt} \to C^\ast Alg_{com,nu}^{op}
$$
for the functor that sends a [[pointed topological space|pointed topological]] [[compact Hausdorff space]] $(X,x_0)$ to the algebra of [[continuous function]]s $f : X \to \mathbb{C}$ for which $f(x_0) = 0$.

=--


+-- {: .num_defn}
###### Definition

Write
$$
  sp : C^\ast Alg_{com}^{op} \to Top_{cpt}
$$
for the [[Gelfand spectrum]] functor: it sends a commutative $C^\ast$-algebra $A$ to the set of _[[character]]s_ -- non-vanishing $C^\ast$-algebra [[homomorphisms]] $x : A \to \mathbb{C}$ -- equipped with the [[spectral topology]].

Similarly write 
$$
  sp : C^\ast Alg_{com,nu}^{op} \to Top_{lcpt}
  \,.
$$

=--

## Statement

+-- {: .num_theorem #GelfandDualityTheorem}
###### Theorem
**(Unital Gelfand duality theorem)**

The pair of functors 
$$
  C^\ast Alg_{com}^{op} \stackrel{\overset{C}{\leftarrow}}{\underset{sp}{\to}} Top_{cpt}
$$
is an [[equivalence of categories]].

=--

Here $C^\ast Alg^{op}_{\cdots}$ denotes the [[opposite category]] of $C^\ast Alg_{\cdots}$.


+-- {: .num_cor}
###### Corollary

On non-unital $C^\ast$-algebras the above induces an [[equivalence of categories]]
$$
  C^\ast Alg_{com,nu}^{op} \stackrel{\overset{C_0}{\leftarrow}}{\underset{sp}{\to}} */Top_{cpt}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The operation of [[unitalization]] $(-)^+$ constitutes an [[equivalence of categories]]
$$
  C^\ast Alg_{nu}
    \underoverset
    {\underset{(-)^+}{\longrightarrow}}
    {\overset{ker}{\longleftarrow}}
    {\simeq}
  C^\ast Alg / \mathbb{C}
$$
between non-unital $C^\ast$-algebras and the [[over-category]] of $C^\ast$-algebras over the [[complex number]]s $\mathbb{C}$.

Composed with the equivalence of theorem \ref{GelfandDualityTheorem} this yields 
$$
  C^\ast Alg_{com,nu}^{op}
    \underoverset{\simeq}{(-)^+}{\to}
  (C^\ast Alg_{com}/\mathbb{C})^{op}
    \underoverset{\simeq}{C}{\to}
  * / Top_{cpt}
  \,.
$$

The weak inverse of this is the composite functor
$$
  C_0 : */Top_{cpt} 
    \underoverset{\simeq}{sp}{\to}
  (C^\ast Alg_{com}/\mathbb{C})^{op}
    \underoverset{\simeq}{ker}{\to}
  C^\ast Alg_{com,nu}^{op}
$$
which sends $(* \stackrel{x_0}{\to} X)$ to 
$ker(C(X) \stackrel{ev_{x_0}}{\to} \mathbb{C})$, hence to 
$\{f \in C(X) | f(x_0) = 0\}$. This is indeed $C_0$ from 
def. \ref{FunctorsOfFunctionAlgebras}.


=--

+-- {: .num_remark #ForLocallyCompactTopologicalSpaces}
###### Remark

Since [[locally compact Hausdorff spaces are equivalently open subspaces of compact Hausdorff spaces]], via the construction that sends a locally compact Hausdorff space $X$ to its [[one-point compactification]], and since a [[continuous function]] on the compact Hausdorff space $X^\ast$ which vanishes at the extra point is equivalently a continuous function on $X$ which [[vanishing at infinity|vanishes at infinity]], the above induces a contravariant equivalence
$$Top_{lcpt,inf} \leftrightarrows C^\ast Alg_{com,nu}$$
between the category of locally compact Hausdorff spaces and continuous maps vanishing at infinity
and the category of commutative nonunital C\*-algebras.

The duality also works with [[real numbers]] instead of [[complex numbers]] ([Johnstone 82, chapter IV](#Johnstone82))

For an overview of other generalizations see also [this MO discussion](http://mathoverflow.net/a/82960/381).

=--

If one uses nondegenerate morphisms of C\*-algebras instead, the duality works for [[locally compact topological spaces]] and [[proper maps]]. See for instance ([Brandenburg 07](#Brandenburg07)).

\begin{theorem}
The is an equivalence of categories
$$Top_{lcpt,proper} \leftrightarrows C^\ast Alg_{com,nu,nd}$$
between the category of [[locally compact]] [[Hausdorff spaces]] and [[proper maps]]
and the category of commutative nonunital [[C*-algebras]] with nondegenerate \*-homomorphisms as morphisms.
\end{theorem}


## Generalizations

### In constructive mathematics

Gelfand duality makes sense in [[constructive mathematics]] hence [[internalization|internal]] to any [[topos]]: see [[constructive Gelfand duality theorem]].

### By horizontal categorification

Gelfand duality can be extended by [[horizontal categorification]] to define the notion of [[spaceoid|spaceoids]] as formal duals of commutative $C^*$-[[C-star-category|categories]].

## Related concepts

* [[Isbell duality]]

  * [[Gelfand-Kolmogorov theorem]]

  * **Gelfand duality**, [[constructive Gelfand duality theorem|constructive Gelfand duality]]

    * [[C-star algebra]], [[topological space]]
    
    * [[Gelfand-Naimark theorem]]   

    * [[Gelfand spectrum]]

    * [[Serre-Swan theorem]]

    * [[noncommutative topology]]

* [[Stone duality]]

The analogous statement in [[differential geometry]]:

* [[embedding of smooth manifolds into formal duals of R-algebras]]

[[!include Isbell duality - table]]

## References

The original reference is

* [[Israel Gelfand]], _Normierte Ringe_, Recueil Mathématique 9(51):1 (1941), 3–24.

Formulation of Gelfand duality in terms of [[category theory]] ([[adjoint functors]], [[monads]] ("triples") and [[adjoint equivalences]]) originates with

* {#Negropontis71} Joan W. Negrepontis, _Duality in analysis from the point of view of triples_, Journal of Algebra, 19 (2): 228–253, (1971) (<a href="https://doi.org/10.1016/0021-8693(71)90105-0">doi</a>, ISSN 0021-8693, MR 0280571)

Quick exposition is in

* Ivo Dell'Ambrogio, _Categories of $C^\ast$-algebras_ ([pdf](https://idellambrogio.github.io/exercise_C_algebras.pdf))

Textbook accounts include

* {#Johnstone82} [[Peter Johnstone]], section IV.4 of _[[Stone Spaces]]_, Cambridge Studies in Advanced Mathematics 3, Cambridge University Press 1982. xxi+370 pp. MR85f:54002, reprinted 1986.

* [[Nicolaas Landsman|N. P. Landsman]], _Mathematical topics between classical and quantum mechanics_, Springer Monographs in Mathematics 1998. xx+529 pp. [MR2000g:81081](http://www.ams.org/mathscinet-getitem?mr=1662141) [doi](http://dx.doi.org/10.1007/978-1-4612-1680-3)

* [[Gerald B. Folland]], *A course in abstract harmonic analysis*, Studies in Advanced Mathematics. CRC Press (1995) &lbrack;[pdf](https://sv.20file.org/up1/1415_0.pdf), [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)&rbrack;


Careful discussion of the duality for the more general case of [[locally compact topological spaces]] includes

* {#Brandenburg07} [[Martin Brandenburg]], _Gelfand-Dualität ohne 1_, 2007 ([web](http://www.matheplanet.com/matheplanet/nuke/html/article.php?sid=1111))

{#ReferencesCenterOfAction} Discussion of Gelfand duality as a [[fixed point equivalence of an adjunction]] between includes

* {#PorstTholen91} [[Hans-E. Porst]], [[Walter Tholen]], section 4-c of _Concrete Dualities_ in H. Herrlich, [[Hans-E. Porst]] (eds.) _Category Theory at Work_, Heldermann Verlag 1991 ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf))

following

* {#DubucPorta71} [[Eduardo Dubuc]], [[Horacio Porta]], _Convenient categories of topological algebras_, Bull. Amer. Math. Soc., Volume 77, Number 6 (1971), 975-979 [euclid](https://projecteuclid.org/euclid.bams/1183533170)



Some other generalized contexts for Gelfand duality:

* [[Hans Porst]], Manfred B. Wischnewsky, _Every topological category is convenient for Gelfand duality_, Manuscripta mathematica __25__:2, (1978) pp 169-204 

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], Sander Wolters, _The Gelfand spectrum of a noncommutative $C^\ast$-algebra_, J. Aust. Math. Soc. __90__ (2011), 39&#8211;52 [doi](http://dx.doi.org/10.1017/S1446788711001157) [pdf](http://www.math.ru.nl/~landsman/LandsmanCarey60.pdf)

*  [[Christopher J. Mulvey]], _A generalisation of Gelfand duality_, J. Algebra 56, n. 2, (1979) 499&#8211;505 <a href="http://dx.doi.org/10.1016/0021-8693(79)90352-1">doi</a>

* {#Parzygnat17} [[Arthur Parzygnat]], _Discrete probabilistic and algebraic dynamics: a stochastic commutative Gelfand-Naimark Theorem_ ([arXiv:1708.00091](https://arxiv.org/abs/1708.00091))

category: analysis, geometry, noncommutative geometry

[[!redirects Gelfand duality]]
[[!redirects Gel'fand duality]]

[[!redirects Gelfand-Naimark duality]]

[[!redirects Gelfand duality theorem]]





