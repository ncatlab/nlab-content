
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[metrisable space|metrisable]] [[topological space]] $Y$ is an _absolute neighborhood retract_  (ANR) if ([Borsuk 32, p. 222](#Borsuk32)) for _any_ [[embedding of topological spaces|embedding]] $Y \subset Z$ as a [[closed subspace]] in a [[metrisable topological space]] $Z$, $Y$ is a [[neighborhood retract]] of $Z$.

A [[metrisable space|metrisable]] topological space $Y$ is an _absolute retract_ if for _any_ embedding $Y\subset Z$ as a [[closed subspace]] in a [[metrisable topological space]] $Z$, $Y$ is a [[retract]] of $Z$.

## Properties
 {#Properties}

\begin{prop}\label{ANRIsLocalProperty}
  **(ANR is a local property for metrizable spaces)** \linebreak
  A [[metrizable topological space]] which admits an [[open cover]] by [[absolute neighbourhood retracts]] is itself an [[absolute neighbourhood retract]].
\end{prop}

(review in [Hu 65, III Thm. 8.1](#Hu65))

\begin{prop}
A [[metrisable topological space]] is an [[absolute retract]] precisely if it is 

1. a [[contractible topological space]],

1. an [[absolute neighborhood retract]].

\end{prop}

([Hu 65, Prop. II.7.2](#Hu65))


## Examples
 {#Examples}


\begin{example}
  Every ([[finite number|finite]]-[[dimension of a manifold|dimensional]]) 
  [[metrizable topological space|metrizable]] [[locally Euclidean topological space]] -- in particular every [[topological manifold]] -- is an [[absolute neighbourhood retract]].

\end{example}

By Prop. \ref{ANRIsLocalProperty} (see also [Hu 65, III Cor. 8.3](#Hu65)).

In fact:

\begin{example}\label{ParacompactBanachManifoldsAreANRs}
Every [[paracompact topological space|paracompact]] [[Banach manifold]] is an [[absolute neighbourhood retract]].
\end{example}
By [Palais 1966, Cor. to Thm. 5 on p. 3](#Palais66).

\begin{example}
  Every [[finite number|finite]]-[[dimension of a CW complex|dimensional]] [[locally finite CW complex|locally finite]] [[CW-complex]] is an [[absolute neighbourhood retract]].

\end{example}

([Dugundji 52](#Dugundji52), [Kodama 56](#Kodama56), review in [Hu 65, III Cor. 8.4](#Hu65))


## Related concepts

* [[retract]], 

* [[neighborhood retract]]

* [[deformation retract]]


## References

The notion of _absolute neighbourhood retract_ is due to

* {#Borsuk32} [[Karol Borsuk]], _Über eine Klasse von lokal zusammenhängenden Räumen_, Fund. Math **19** (1932) 220-242 ([dml:212574](https://eudml.org/doc/212574), [pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm19/fm19119.pdf))

Further development:

* [[Olof Hanner]], _Some theorems on absolute neighbourhood retracts_, Arkiv F&ouml;r Matematik Band 1 nr 30 (1950) ([doi:10.1007/BF02591376](https://doi.org/10.1007/BF02591376))

* {#Dugundji52} [[James Dugundji]], _Note on CW polytopes_, Portugaliae mathematica (1952) **11** 1 (1952) 7-10-b ([dml:114693](https://eudml.org/doc/114693))

* {#Kodama56} Yukihiro Kodama, _Note on an absolute neighborhood extensor for metric spaces_, Journal of the Mathematical Society of Japan **8** 3 (1956) 206-215 ([doi:10.2969/jmsj/00830206](https://doi.org/10.2969/jmsj/00830206))

* [[Karol Borsuk]], _Concerning the classification of topological spaces from the stand point of the theory of retracts_, Fundamenta Mathematicae **46** (3) (1959) 321-330 ([dml:213516](https://eudml.org/doc/213516))

Discussion for [[infinite-dimensional manifolds]]:

* {#Palais66} [[Richard S. Palais]], *Homotopy theory of infinite dimensional manifolds*, Topology **5** 1 (1966) 1-16 (<a href="https://doi.org/10.1016/0040-9383(66)90002-4">doi:10.1016/0040-9383(66)90002-4</a>)

Textbook accounts and review:

* [[Karol Borsuk]], _Theory of retracts_, Vol. 44. Państwowe Wydawn. Naukowe, 1967

* {#Hu65} [[Sze-Tsen Hu]], _Theory of Retracts_, Wayne State University Press (1965) ([google-books](https://books.google.ae/books/about/Theory_of_Retracts.html?id=GVTvAAAAMAAJ&redir_esc=y))

* [[Sibe Mardešić]], _Absolute Neighborhood  Retracts and Shape  Theory_ ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/mardesic.pdf))


* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, Def. 4.2.10 in: _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([doi:10.1007/b97586](https://link.springer.com/book/10.1007/b97586), [toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


See also:

* [[eom]], _[Absolute retract for normal spaces](https://www.encyclopediaofmath.org/index.php/Absolute_retract_for_normal_spaces)_

* [[eom]], _[Retract of a topological space](https://encyclopediaofmath.org/wiki/Retract_of_a_topological_space)_

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Retract#Absolute_neighborhood_retract_(ANR)">Absolute neighbourhood retract</a>_

[[!redirects absolute retracts]]

[[!redirects absolute neighborhood retract]]
[[!redirects absolute neighborhood retracts]]

[[!redirects absolute neighbourhood retract]]
[[!redirects absolute neighbourhood retracts]]

[[!redirects ANR]]
[[!redirects ANRs]]
