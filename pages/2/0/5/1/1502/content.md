
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A _semisimple category_ is a [[category]] in which each [[object]] is a [[direct sum]] of [[finite number|finitely many]] [[simple objects]], and all such direct sums exist.

## Definition
 {#Definition}

\begin{definition}
**([[semisimple abelian category]])**
\linebreak
An [[abelian category]] is called **semisimple** if every [[object]] is a [[semisimple object]], hence a [[direct sum]] of [[finite number|finitely many]] [[simple objects]].
\end{definition}

Alternatively, at least over an [[algebraically closed field|algebraically closed]] [[ground field]] $k$:

\begin{definition}\label{SemisimpleLinearCategory}
**(semisimple linear category)**
\linebreak
A [[linear category]] (that is, a [[category]] [[enriched category|enriched over]] [[Vect]], cf. *[[tensor category]]*) is called **semisimple** if:

1. it has [[finite product|finite]] [[biproducts]] 
 
   (usually called '[[direct sums]]'),

1. [[split idempotent|idempotents split]] 

   (so we say that it 'has [[subobjects]]' or, perhaps better, 'has [[retracts]]'), 

1. there exist [[objects]] $X_i$ labeled by an index [[set]] $I$ such that 

   1. for any [[pair]] $i, j$ of indices we have an [[isomorphism]]

      \[
        \label{SimplicityIsomorphism}
        Hom(X_i, X_j) 
          \;\cong\; 
        \delta_{i j} k
        \,,
      \] 

      where $\delta$ denotes the [[Kronecker delta]] and $k$ the [[ground field]] 

      (such objects are called *[[simple object|simple]]*),

   1. for any [[pair]] of [[objects]] $V,\,W$, the natural [[composition]] map

      \[
        \label{CompositionIsomorphism}
        \bigoplus_{i \in I} 
        \,
        Hom(V, X_i) 
        \,\otimes\, 
        Hom(X_i, W) 
          \longrightarrow
        Hom(V, W)
      \]
    
      is an [[isomorphism]].

   (If the field $k$ is not [[algebraically closed field|algebraically closed]], a [[simple object]] $X$ can have a [[finite-dimensional vector space|finite-dimensional]] [[division algebra]] other than $k$ itself as its [[endomorphism algebra]].)

\end{definition}

(e.g. [Müger (2003, p. 6)](#Müger03))

\begin{proposition}\label{DirectSumDecompositionintoSimples}
**(direct sum decomposition into simple objects)**
\linebreak
Definition \ref{SemisimpleLinearCategory} implies that every object $V$ is a [[direct sum]] of [[simple objects]] $X_i$. 
\end{proposition}
\begin{proof}
The third item of the definition is equivalent to stipulating that the [[vector space]] $Hom(X_i, V)$ is in canonical [[dual vector space|duality]] with the vector space $Hom(V, X_i)$. Indeed, we have:

1. a pairing

   \[
     \begin{array}{ccc}
        Hom(V, X_i) 
         \,\otimes\, 
        Hom(X_i, V) 
        &
          \longrightarrow 
        &
        Hom(X_i, X_i)
        &\simeq&
        k
        \\
        f \,\otimes\, g
        &\mapsto&
        f \,\circ\, g 
        \mathrlap{\,,}
     \end{array}
   \]

   where on the right we used (eq:SimplicityIsomorphism),
  
1. a copairing

   \[
     k \cdot Id_B
     \;\hookrightarrow\;
     Hom(V,V)
        \longrightarrow 
      Hom(X_i, V) 
        \otimes  
     Hom(V, X_i)
     \mathrlap{\,,}
   \]

   where on the right we used (eq:CompositionIsomorphism),
 
and one checks that these satisfy the [[triangle identities]] and as such exhibit [[dual vector spaces]]. 

Hence if we choose a [[linear basis]]

\[
   \big\{ 
     a_{i,p} 
      \,\colon\, 
     X_i 
      \rightarrow V 
   \big\}
\]

for each [[vector space]] $Hom(X_i, V)$, we get a corresponding dual basis

\[
  \big\{ 
    a_i^p 
     \,\colon\, 
    V \rightarrow X_i 
  \big\}
\]

satisfying

\[
  a_i^p a_{j,q} 
   \;=\; 
  \delta_{i j} \delta_p^q 
  \;\;\; \text{and} \;\;\; 
  \sum_{i,p} a_{i,p} a_i^p 
    \;=\; \id_V
  \mathrlap{\,.}
\]

This says precisely that $V$ has been expressed as a [[direct sum]] of the $X_i$.
\end{proof}


\begin{remark}
Def. \ref{SemisimpleLinearCategory} (of semisimple linear categories) does not use the concept of *[[abelian category]]*. This is because the concepts that one thinks about with abelian categories such as [[kernel]]s and [[cokernel]]s do not play an important conceptual role in semisimple categories, being replaced by the more important concepts of [[biproduct]] and [[retract]]. Hence it is best to give a streamlined definition from first principles without going through the language of abelian categories which would have muddied the waters.
\end{remark}

\begin{remark}
For a category to be semisimple, it needs to have a certain directional symmetry in its hom-sets, namely that $Hom(V, W)$ must at least have the same dimension as $Hom(W,V)$. This is the easiest way to check if a category will _fail_ to be semisimple. For instance, the category $Rep(A)$ of [[representations]] of an algebra $A$ will rarely be semisimple, precisely because there is no relation between $Hom(V, W)$ and $Hom(W,V)$ in general. Again, this can be traced back to the original algebra $A$ not having any 'symmetry' like the inverse operation in a group. 
\end{remark}

\begin{remark}
As far as 'duality' on the hom-sets is concerned, one might have a $S \colon C \rightarrow C$ from the category to itself with the property that there are canonical isomorphisms

\[
  Hom(V, W) \cong Hom(W, S V)^\vee
\]

where "$\vee$" denotes the ordinary linear dual of a vector space. Such a functor is called a _Serre functor_ in algebraic geometry, and indeed there is precisely such a functor on the derived category of coherent sheaves on a complex manifold --- it is given by tensoring with the [[canonical line bundle]]. 
\end{remark}

\begin{remark}
For [[2-Hilbert space|2-Hilbert spaces]], there is an antilinear $*$-operation on the hom-sets $* : Hom(V, W) \rightarrow Hom(W,V)$. The presence of this duality in fact forces the category to be semisimple (this comes down to the fact that a finite-dimensional $*$-algebra, such as the hom's between a bunch of objects in the category, must be a full matrix algebra)
\end{remark}

## Examples

* The archetypical simple example is [[FinDimVect]] itself, the [[category]] of [[finite dimensional vector spaces]] over some [[ground field]] $k$. This has a single [[isomorphism]] class of simple objects: given by $k$ itself.

* The [[category of representations|category of finite-dimensional complex representations]] of a [[compact Lie group]] $G$ is semisimple, with the simple objects being precisely the [[irreducible representation]]s (this is the content of [[Schur's lemma]]). If $G$ is not a [[compact Lie group]], one needs to pass from the concept of 'direct sum' to '[[direct integral]]'.

* Every [[fusion category]] is a semisimple category.

## References

Various alternative definitions of semisimple category appear in the literature, and a number are compared here:

* James Bailie, Semisimple categories ([pdf](https://jameshbailie.github.io/Papers/papers/Semisimple.pdf).

For example, he compares a definition of "abelian semisimple category"(an abelian category where every object is a direct sum of a possibly infinite number of simple objects) with  "Müger semisimple" categories as discussed here:

* {#Müger03} [[Michael Müger]], p. 6 in: *From Subfactors to Categories and Topology I. Frobenius algebras in and Morita equivalence classes of tensor categories*, J. Pure Appl. Alg. **180** (2003) 81-157 &lbrack;[arXiv:math/0111204](https://arxiv.org/abs/math/0111204), <a href="https://doi.org/10.1016/S0022-4049(02)00247-5">doi:10.1016/S0022-4049(02)00247-5</a>&rbrack;

There is a [related discussion on the nForum](http://nforum.mathforge.org/discussion/1120/semisimple-category/?Focus=42783#Comment_42783) and a [discussion on MathOverflow](https://mathoverflow.net/questions/442953/what-is-the-correct-definition-of-semisimple-linear-category).

[[!redirects semisimple categories]]
