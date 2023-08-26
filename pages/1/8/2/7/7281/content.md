
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

\begin{definition}
\label{BasisOfAVectorSpace}
For $\mathbb{K}$ a [[field]] and $V$ a $\mathbb{K}$-[[vector space]], hence a $\mathbb{K}$-[[module]], a *[[linear basis]]* for $V$ is 

1. a [[set]] $B$ (of *basis elements*)

1. a $\mathbb{K}$-[[linear map|linear]] [[isomorphism]] 

   $$
     \underset{B}{\oplus}  
     \mathbb{K}
     \xrightarrow{\;\; \simeq \;\;}
     V
   $$ 

to $V$ from the $B$-indexed [[direct sum]] (the [[coproduct]] in $\mathbb{K}$[[Vect]]) of copies of $\mathbb{K}$ (canonically regarded as a vector space over itself), also known as the free $\mathbb{K}$-[[linear span]] of $B$, hence the vector space of free $\mathbb{K}$-[[linear combinations]] of elements of $B$.
\end{definition}

Hence if a basis for $V$ exists it means in particular that $V$ is a [[free module]] over $\mathbb{K}$. 

\begin{remark}
**(finiteness of linear combinations)**
\linebreak
Beware that a certain finiteness-condition is hidden in Def. \ref{BasisOfAVectorSpace}: Since a [[linear combination]] is defined to be a [[sum]] of [[finite set|finitely]] many vectors, a basis of a vector space must be such that every vector in the space is the (unique) combination of *finitely* many basis elements -- even if there are infinitely many elements in the basis.

More abstractly this is to do with the appearance of the [[coproduct]] $\amalg_b = \oplus_B$ ([[direct sum]]) in Def. \ref{BasisOfAVectorSpace} instead of the [[product]] $\prod_B$. Many vector spaces in practice arise as (subspaces) of products $\prod_W \mathbb{K}$ ([[function spaces]] $W \to \mathbb{K}$), but if $W$ here is not a [[finite set]] then it is not going to be a basis set. 

(On the other hand, if $W$ *is* a [[finite set]], then we have a *[[biproduct]]* $\prod_W \,\simeq\, \coprod_W \,\simeq\, \oplus_W$ in the [[additive category]] $\mathbb{K}$[[Vect]], see [there](additive+category#ProductsAreBiproducts).)
\end{remark}

Related to this are the following phenomena:

\begin{remark}
**(basis and dimension of finitely-generated spaces)**
\linebreak
For every *finitely generated* vector space $V$ (Def. \ref{GeneratedVectorSpace}) it is straightforward to *[[constructive mathematics|construct]]* a linear basis, and to see that the [[cardinality]] of all bases is the same finite [[natural number]] $dim(V) \in \mathbb{N}$, called the *[[dimension of a vector space|dimension]]* of the vector space (whence a *[[finite-dimensional vector space]]*).
\end{remark}

On the other hand:

\begin{remark}
**(Hamel-bases of infinite-dimensional vector spaces)**
\linebreak
While the definition \ref{BasisOfAVectorSpace} applies also to not-necessarily finitely generated vector spaces -- such as for instance the space of ([[continuous function|continuous]]) [[functions]] from a non-finite ([[topological space|topological]]) [[space]] to the ([[topological field|topological]]) [[ground field]] -- it turns out to be subtle and somewhat ill-behaved in this generality. 

In fact, in practice infinite-dimensional vector spaces tend to appear and to be understood with [[extra structure]] (typically that of [[topological vector spaces]] such as [[Banach spaces]] or [[Hilbert spaces]]) in which cases there are more appropriate notions of linear bases for them (such as that of [[Schauder bases]], which allow infinite-[[linear combinations]] subject to a condition of [[convergence of a sequence]]). 

In order to distinguish the plain notion of basis (Def. \ref{BasisOfAVectorSpace}) from these more refined notions, one also speaks of *Hamel bases* here. 

(This is in honor of [Hamel 1905 pp. 460](#Hamel1905) who considered this notion for the special case of $V = \mathbb{R}$ the [[real numbers]] regarded as a [[rational vector space]], hence  over the [[ground field]] $\mathbb{K} = \mathbb{Q}$ of [[rational numbers]]).

Hence, in principle, also a linear basis of a finitely generated vector space is thus a *Hamel basis*, but rarely called this way unless in the context of infinite-dimensional vector spaces.
\end{remark}

\begin{remark}
**(basis theorem and dimension)**
\linebreak
For an infinitely-generated vector space it is *not* in general possible to *[[constructive mathematics|construct]]* a (Hamel-)basis, but the *existence* of such a basis is nevertheless implied, in [[classical mathematics]], by [[Zorn's lemma]] (essentially a form of the [[axiom of choice]]):  This is the content of the *[[basis theorem]]*.  

With this classical context understood, it follows that every vector vector space admits a linear basis (even if non-constructible in general) and that each basis is of the same [[cardinality]], then called the [[dimension of a vector space|dimension]] of the vector space.
\end{remark}

## Background definitions

\begin{definition}\label{GeneratedVectorSpace}
**(generated vector space)**
\linebreak
  For $V$ a vector space, a [[subset]] $G \subset V$ of its [[underlying]] set is called a *generating set* or *spanning set* if every element of $V$ can be expressed as a [[linear combination]] of elements of $G$ in $V$, hence if the [[linear span]] of $G$ inside $V$ is all of $V$.

The vector space $V$ is called *finitely generated* if it admits a generating set (spanning set) which is a [[finite set]].
\end{definition}




## Related concepts

* [[orthogonal basis]]

* [[basis in functional analysis]]

* [[Schauder basis]]

* [[dual basis]]

* [[basis]]

* [[mutually unbiased bases]]

* [[Gelfand-Tsetlin basis]] (in [[representation theory]])

* [[seminormal basis]] (in [[representation theory of the symmetric group]])


## References

Lecture notes with much conceptual exposition:

* Karen E Smith, *Bases for infinite-dimensional vector spaces* &lbrack;[pdf](https://dept.math.lsa.umich.edu/~kesmith/infinite.pdf), [[Smith-InfiniteDimBases.pdf:file]]&rbrack;

Lecture notes with the proofs concisely spelled out:

* [[Christoph Schweigert]], *Basis und Dimension*, §2.4 in:  *Lineare Algebra*, lecture notes, Hamburg (2022) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schweigert/skripten/laskript.pdf)&rbrack;

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Basis_(linear_algebra)">Basis (linear algebra)</a>*

The original discussion (for [[real numbers|$\mathbb{R}$]] regarded as a [[rational vector space]]) after which *Hamel bases* are named:

* {#Hamel1905} [[Georg Hamel]], pp. 460 of: *Eine Basis aller Zahlen und die unstetigen Lösungen der Funktionalgleichung: $f(x + y) = f(x) + f(y)$*, Mathematische Annalen **60** (1905) 459–462 &lbrack;[doi:10.1007/BF01457624](https://doi.org/10.1007/BF01457624)&rbrack;

[[!redirects Hamel basis]]
[[!redirects Hamel bases]]
[[!redirects Hamel basises]]

[[!redirects linear basis]]
[[!redirects linear bases]]

