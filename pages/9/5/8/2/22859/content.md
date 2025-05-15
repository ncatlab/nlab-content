
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of *differential categories* ([Blute, Cocket & Seely 2006](#BluteCocketSeely06) is meant to provide [[categorical semantics]] for 
[[differential linear logic]] ([Ehrhardt & Regnier 2009](#EhrhardtRegnier09)) which in turn is meant to be a [[syntax|syntactic]] [[proof theory|proof-theoretic]] approach to [[differential calculus]]. In fact differential categories are slightly more general than the models of differential linear logic.

## Differential categories
 {#DifferentialCategories}

The main intuition for differential categories, is that in a differential category morphisms $A \rightarrow B$ must be interpreted as linear morphisms from $A$ to $B$ while morphisms $!A \rightarrow B$ must be interpreted as smooth morphisms from $A$ to $B$. One can then differentiate these smooth morphisms from $A$ to $B$. If we have $f:!A \rightarrow B$, then we can obtain $D(f):!A \otimes A \rightarrow B$ which is smooth in the first variable and linear in the second variable. If we are in a [[monoidal closed category]], we can alternatively view $D(f)$ as a morphisms of type $!A \rightarrow (A \multimap B)$ which associate smoothly to every point of $A$ the linear approximation of $f$ around this point.

\begin{definition}
A coalgebra modality in a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$ is given by a [[comonad]] $(!,m,u)$ and two [[natural transformations]] $\epsilon:!A \rightarrow I$ and $\Delta:!A \rightarrow !A \otimes !A$ such that for every $A \in \mathcal{C}$, $(!A, \Delta, \epsilon)$ is a [[cocommutative comonoid]] in $(\mathcal{C},\otimes,I)$ and this diagram commutes:
\begin{tikzcd}
!A \arrow[d, "m"'] \arrow[rr, "\Delta"] &  & !A \otimes !A \arrow[d, "m \otimes m"] \\
!!A \arrow[rr, "\Delta"']             &  & !!A \otimes !!A              
\end{tikzcd}
\end{definition}

The idea is that a coalgebra modality allows us to perform various operations on smooth morphisms. 

* If we start with $f:!A \rightarrow B$ and $g:!A \rightarrow C$, we can "multiply" these two smooth morphisms together to obtain a smooth morphism $!A \rightarrow B \otimes C$ defined as $\Delta;f \otimes g$.

* If we start with $f:A \rightarrow B$ which is a linear morphism, we can say that it is a very simple form of smooth morphism and obtain a morphism $!A \rightarrow B$ from $f$ defined as $u;f$

* If we start with a constant $f:I \rightarrow !A$, we can say that is an even simpler form of smooth morphism and obtain a morphism $!A \rightarrow B$ from $f$ defined as $\epsilon;f$.

* If we start with two smooth morphisms $f:!A \rightarrow B$ and $g:!B \rightarrow C$, we can compose these two smooth morphisms to obtain a smooth morphism $!A \rightarrow C$ defined as $m;!(f);g$.

\begin{definition}
A CMon-enriched [[symmetric monoidal category]] is a [[symmetric monoidal category]] $\mathcal{C}$ such that each hom-set $\mathcal{C}[A,B]$ is a [[commutative monoid]] (in Set) and $- \otimes -$ as well as $-;-$ are bilinear ie. preserve sums and the zero in each variable.
\end{definition}

\begin{definition}
A differential category is a CMon-enriched [[symmetric monoidal category]] together with a coalgebra modality and a deriving transformation ie. a [[natural transformation]] $d:!A \otimes A \rightarrow !A$ such that the following diagrams commute:
...
\end{definition}

###Examples

## Codifferential categories

The definition of a *codifferential category* is the [[formal dual]] of that of a differential category:

A *codifferential category* is a [[category]] $\mathcal{C}$ equipped with [[structure]] such that its [[opposite category]]  $\mathcal{C}^{op}$ is a differential category in the sense [above](#DifferentialCategories) (and vice versa).

The notion of codifferential categories is maybe more intuitively accessible  because it involves [[monoids]] and [[monads]] instead of [[comonoids]] and [[comonads]]; but the [[formal duality|formally dual]] notion of differential categories is closer to [[linear logic]] and [[differential linear logic]] with their comonadic [[modality]]. 

In the following sequence of definitions, the object $S(A)$ is to be interpreted as a [[mapping space]] of [[smooth functions]] with [[variables]] in $A$. 

\begin{definition}
An [[algebra modality]] in a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$ is given by a [[monad]] $(S,m,u)$ and two [[natural transformations]] $\eta:I \rightarrow S(A)$ and $\nabla:S(A) \otimes S(A) \rightarrow S(A)$ such that for every $A \in \mathcal{C}$, $(S(A), \nabla, \eta)$ is a [[commutative monoid]] in $(\mathcal{C},\otimes,I)$ and this diagram commutes:
\begin{tikzcd}
S(S(A)) \otimes S(S(A)) \arrow[dd, "m \otimes m"'] \arrow[rr, "\nabla"] &  & S(S(A)) \arrow[dd, "m"] \\
                                                                            &  &                           \\
S(A) \otimes S(A) \arrow[rr, "\nabla"']                                   &  & S(A)                    
\end{tikzcd}
\end{definition}

The multiplication of the monad must be interpreted as the composition of smooth functions.

\begin{definition}
A codifferential category is a CMon-enriched [[symmetric monoidal category]] together with an algebra modality and a deriving transformation ie. a [[natural transformation]] $d:S(A) \rightarrow S(A) \otimes A$ such that the following diagrams commute:

* [[Leibniz rule]]:
\begin{tikzcd}
S(A) \arrow[rrrrr, "d"]                                                                                &  &  &  &  & S(A) \otimes A                                               \\
                                                                                                        &  &  &  &  &                                                               \\
S(A) \otimes S(A) \arrow[uu, "\nabla"] \arrow[rrrrr, "(d \otimes 1)(1\otimes \gamma) + 1 \otimes d"'] &  &  &  &  & S(A) \otimes S(A) \otimes A \arrow[uu, "\nabla \otimes 1"']
\end{tikzcd}
It expresses that the differential of a product of two functions is the sum of the differential of the first function multiplied by the second one and the first function multiplied by the differential of the second one. 

* [[chain rule|Chain rule]]:
\begin{tikzcd}
S(S(A)) \otimes S(A) \arrow[rrr, "m \otimes d"] &  &  & S(A) \otimes S(A) \otimes A \arrow[rrd, "\nabla \otimes 1"] &  &                 \\
                                                   &  &  &                                                               &  & S(A) \otimes A \\
S(S(A)) \arrow[rrr, "m"'] \arrow[uu, "d"]        &  &  & S(A) \arrow[rru, "d"']                                       &  &                
\end{tikzcd}

This diagram is the most tricky one. It expresses that the differential of the composition of two smooth functions is equal to the differential of the external function applied to the internal function multiplied by the differential of the internal function.

* Linear rule:
\begin{tikzcd}
A \arrow[dd, "u"'] \arrow[rrdd, "\eta \otimes 1"] &  &                 \\
                                                  &  &                 \\
S(A) \arrow[rr, "d"']                            &  & S(A) \otimes A
\end{tikzcd}

It expresses that the differential of a vector, as a formal homogeneous polynomial of degree $1$ is more or less this vector.

* Schwarz rule:
\begin{tikzcd}
S(A) \otimes A \arrow[rrrr, "d \otimes 1"] &  &                                            &  & S(A) \otimes A \otimes A \arrow[dd, "1 \otimes \gamma"] \\
                                            &  &                                            &  &                                                          \\
S(A) \arrow[uu, "d"] \arrow[rr, "d"']      &  & S(A) \otimes A \arrow[rr, "d \otimes 1"'] &  & S(A) \otimes A \otimes A                               
\end{tikzcd}

It expresses that the second differential of a function is invariant by permutation of the two variables with respect to we differentiate successively.

###Examples
If $\mathbb{K}$ is a field, then $Vect_{\mathbb{K}}$ is a codifferential category.

* We define $S(A) = Sym(A)$, the [[symmetric algebra]] of the vector space $A$.
* It is a commutative algebra as usual.
* The unit $A \rightarrow Sym(A)$ of the monad is just the injection $x \mapsto x$.
* The multiplication $Sym(Sym(A)) \rightarrow Sym(A)$ of the monad is given on pure tensors by $(x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)}) \boxtimes_{s} ... \boxtimes_{s}  (x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}) \mapsto x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)} \otimes ... \otimes x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}$. It is a kind of composition of polynomials.
* The deriving transformation $Sym(A) \rightarrow Sym(A) \otimes A$ is defined on pure tensors by $x_{1} \otimes_{s} ... \otimes_{s} x_{n} \mapsto \underset{1 \le k \le n}{\sum}(x_{1} \otimes_{s} ... \otimes_{s} x_{k-1} \otimes_{s} x_{k+1} \otimes_{s} ... \otimes_{s} x_{n}) \otimes x_{k}$. For instance, if $X,Y,Z$ is a basis of $A$, then $d(X^{2}+YZ) = 2X \otimes X + Y \otimes Z + Z \otimes Y$.

The free $\mathcal{C}^{\infty}$-ring monad on $\mathbb{R}$-[[vector spaces]] provides a structure of codifferential category on **$Vect_{\mathbb{R}}$**.

## Differential categories vs codifferential categories

The deriving transformation in a codifferential category is a natural transformation of type $!A \rightarrow !A \otimes A$. In the category of vector spaces with the exponential modality given by symmetric algebras, we have for example $d(X^{2}+YZ) = 2X \otimes X + Y \otimes Z + Z \otimes Y$.

It would seem more natural to have a deriving transformation of type $!A \rightarrow !A \otimes A^{*}$ and to require the category to be [[*-autonomous]]. Thus, we would have $d(X^{2}+YZ) = 2X \otimes dX + Y \otimes dZ + Z \otimes dY$. The concept of [[graded codifferential category]] can help to enlighten why the type $!A \rightarrow !A \otimes A$ is in fact more natural. If we start with an element of the $(n+1)^{th}$ symmetric power $S_{n+1}A$ of $A$, ie. an [[homogeneous polynomial]] of degree $n+1$, the deriving transformation gives us as result an element of $S_{n}A \otimes A$ and not of $S_{n}A \otimes A^{*}$. There is an idea of "conservation of resources", if one starts with $(n+1)$ (symmetrized) elements of type $A$, then a natural transformation must give as a result $n+1$ elements (with a symmetrization performed on the $n$ first here) and not $n-1$ (here it would be $n$ elements together with a "minus" element in $A^*$).

If we wish to obtain a more natural typing, we need to use differential categories. In a differential category, the differential of a smooth function $!A \rightarrow B$ is given by $d;f:!{A} \otimes A \rightarrow B$. If we are in a [[*-autonomous category]], we can then represent it under the form a morphism $!A \rightarrow B \parr A^*$ using the dual tensor product $\parr$ defined by $A \parr B = (A^* \otimes B^*)^*$.

\end{definition}

## Related concepts

* [[differential linear logic]]

* [[cartesian differential category]]

* [[differential cohesion]]

* [[tangent category]], [[tangent (∞,1)-category]]

* [[tangent bundle category]]

## References

The notion is due to:

*  {#BluteCocketSeely06} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]: _Differential categories_. Math. Struct. Comput. Sci. 16(06), 1049–1083 (2006) ([doi:10.1017/S0960129506005676](https://doi.org/10.1017/S0960129506005676))

* [[Richard Blute]], [[Robin Cockett]], [[Jean-Simon Lemay]] and [[Robert Seely]], _Differential categories revisited,_ Appl. Categ. Struct. 28, 171-235 (2020). ([arXiv:1806.04804](https://arxiv.org/abs/1806.04804), [doi:10.1007/s10485-019-09572-y](https://doi.org/10.1007/s10485-019-09572-y))

following discussion of [[differential linear logic]] in:

* {#EhrhardtRegnier09} [[Thomas Ehrhard]], [[Laurent Regnier]]: _The differential lambda-calculus_, Theor. Comput. Sci. **309** 1 (2003) 1–41  (<a href="https://doi.org/10.1016/S0304-3975(03)00392-X">doi:10.1016/S0304-3975(03)00392-X</a>)

* [[Thomas Ehrhard]], [[Laurent Regnier]]: _Differential interaction nets,_ Theor. Comput. Sci. **364** 2 (2006) 166–195 ([doi:10.1016/j.tcs.2006.08.003](https://doi.org/10.1016/j.tcs.2006.08.003)).

The focus is more on codifferential categories in:

* [[Jean-Simon Lemay]]: _Why FHilb is Not an Interesting (Co)Differential Category_, conference proceedings of QPL2019 ([arXiv:1803.02304](https://arxiv.org/abs/1803.02304),  	
[doi:10.4202/EPTCS.318.2](https://doi.org/10.4204/EPTCS.318.2))

* [[Jean-Simon Lemay]]: _Differential algebras in codifferential categories_, Journal of Pure and Applied Algebra (2019) ([arXiv:1803.02304](https://arxiv.org/abs/1803.02304),  	
[doi:10.1016/j.jpaa.2019.01.005](https://doi.org/10.1016/j.jpaa.2019.01.005))

Further references:

* [[G. S. H. Cruttwell]], [[J.-S. P. Lemay]], [[R. B. B. Lucyshyn-Wright]], _Integral and differential structure on the free C^∞-ring modality_, Cahiers de Topologie et Géométrie Différentielle Catégoriques LXII (2021), 116-176.  [arXiv](https://arxiv.org/abs/1902.04555).

* [[Richard Blute]], [[Rory B. B. Lucyshyn-Wright]], Keith O'Neill, _Derivations in Codifferential Categories_, Cahiers de Topologie et Géométrie Différentielle Catégoriques LVII (2016), 243-280.  [arXiv](https://arxiv.org/abs/1505.00220).

* Keith O’Neill, _Smoothness in Codifferential Categories_, [doi](https://doi.org/10393/36703).

* [[G. S. H. Cruttwell]], [[Jean-Simon Pacaud Lemay]], _Differential Bundles in Commutative Algebra and Algebraic Geometry_, Theory and Applications of Categories 39:36, 1077-1120, 2023.  [arXiv](https://arxiv.org/abs/2301.05542).


[[!redirects differential categories]]
[[!redirects codifferential category]]
[[!redirects codifferential categories]]