
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

every (nonunital) $C^\ast$-algebra $A$ is equivalent to the $C^\ast$-algebra of [[continuous functions]] on the [[topological space]] called its _[[Gelfand spectrum]]_ $sp(A)$.

This theorem is the basis for regarding non-commutative $C^\ast$-algebras as formal duals to spaces in [[noncommutative geometry]].

## Definitions

The statement of Gelfand duality involves the following [[categories]] and [[functors]].

+-- {: .num_defn}
###### Definition

Write

* $C^\ast Alg$ for the category of [[C-star algebras]];

* $C^\ast Alg_{nu}$ for the category of non-unital $C^\ast$-algebras;

* $C^\ast Alg_{com} \subset C^\ast Alg$ for the [[full subcategory]] of commutative $C^\ast$-algebras;

* $C^\ast Alg_{com,nu} \subset C^\ast Alg_{nu}$ for the full subcategory of commutative non-unital $C^\ast$-algebras.

And

* [[Top]]${}_{Haus}$ for the category of [[Hausdorff topological spaces]]

* $Top_{cpt}$ for the [[full subcategory]] of [[Top]]${}_{Haus}$ on the [[compact topological spaces]];

* $*/Top_{cpt}$ for the category of [[pointed topologica]] [[compact Hausorff spaces]], i.e. the [[pointed objects]] in $Top_{cpt}$;

* $Top_{lcpt}$ for the category of Hausdorff and [[locally compact topological spaces]] with morphisms being the [[proper maps]] of topological spaces.

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
  C_0 \;\colon\; */Top_{cpt} \to C^\ast Alg_{com,nu}
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
**(Gelfand duality theorem)**

The pairs of functors 

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
    \stackrel{\overset{ker}{\leftarrow}}{\underset{(-)^+}{\to}}
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

Since [[locally compact Hausdorff spaces are equivalently open subspaces of compact Hausdorff spaces]], via the construction that sends a locally compact Hausdorff space $X$ to its [[one-point compactification]], and since a [[continuous function]] on the compact Hausdorff spce $X^\ast$ which vanishes at the extra point is equivalently a continuous function on $X$ which [[vanishing at infinity|vanishes at infinity]], the above induces an equivalence between locally compact Hausdorff spaces and $C^\ast$-algebras of functions that vanish at infinity.

With due care on defining the right morphisms, the duality generalizes also to [[locally compact topological spaces]]. See for instance ([Brandenburg 07](#Brandenburg07)).

For an overview of other generalizations see also [this MO discussion](http://mathoverflow.net/a/82960/381).

=--


## Generalizations

### In constructive mathematics

Gelfand duality makes sense in [[constructive mathematics]] hence [[internalization|internal]] to any [[topos]]: see [[constructive Gelfand duality theorem]].

### By horizontal categorification

Gelfand duality can be extended by [[horizontal categorification]] to define the notion of [[spaceoid|spaceoids]] as formal duals of commutative $C^*$-[[C-star-category|categories]].

## Related concepts


* [[Isbell duality]]

  * **Gelfand duality**, [[constructive Gelfand duality theorem|constructive Gelfand duality]]

    * [[C-star algebra]], [[topological space]]
    
    * [[Gelfand-Naimark theorem]]   

    * [[Gelfand spectrum]]

    * [[Serre-Swan theorem]]

* [[noncommutative topology]]

## References

Textbook accounts include

* [[Nicolaas Landsman|N. P. Landsman]], _Mathematical topics between classical and quantum mechanics_, Springer Monographs in Mathematics 1998. xx+529 pp. [MR2000g:81081](http://www.ams.org/mathscinet-getitem?mr=1662141) [doi](http://dx.doi.org/10.1007/978-1-4612-1680-3)

* Gerald B. Folland, _A course in abstract harmonic analysis_, Studies in Advanced Mathematics. CRC Press, Boca Raton, FL, 1995. x+276 pp. [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)

An exposition that explicitly gives Gelfand duality as an [[equivalence of categories]] and introduces all the notions of [[category theory]] necessary for this statement is in

* Ivo Dell'Ambrogio, _Categories of $C^\ast$-algebras_ ([pdf](http://www.math.uni-bielefeld.de/~ambrogio/exercise_C_algebras.pdf))

Careful discussion of the duality for the more general case of [[locally compact topological spaces]] includes

* {#Brandenburg07} [[Martin Brandenburg]], _Gefand-Dualit&#228;t ohne 1_, 2007 ([web](http://www.matheplanet.com/matheplanet/nuke/html/article.php?sid=1111))

Some other generalized contexts for Gelfand duality:

* [[Hans Porst]], Manfred B. Wischnewsky, _Every topological category is convenient for Gelfand duality_, Manuscripta mathematica __25__:2, (1978) pp 169-204 

* H. Heunen, [[Klaas Landsman]], [[Bas Spitters]], S. Wolters, _The Gelfand spectrum of a noncommutative $C^\ast$-algebra_, J. Aust. Math. Soc. __90__ (2011), 39&#8211;52 [doi](http://dx.doi.org/10.1017/S1446788711001157) [pdf](http://www.math.ru.nl/~landsman/LandsmanCarey60.pdf)

*  [[Christopher J. Mulvey]], _A generalisation of Gelfand duality_, J. Algebra 56, n. 2, (1979) 499&#8211;505 <a href="http://dx.doi.org/10.1016/0021-8693(79)90352-1">doi</a>

category: analysis, geometry, noncommutative geometry

[[!redirects Gelfand duality]]
[[!redirects Gel'fand duality]]

[[!redirects Gelfand-Naimark duality]]






