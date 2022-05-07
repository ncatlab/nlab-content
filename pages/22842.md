#Contents#
* table of contents
{:toc}


## Idea ##
A delta lens (or d-lens) is a [[functor]] with additional structure specifying a suitable choice of lifts. Delta lenses can be understood in a number of ways: 

* A morphism between [[categories]] which is both [[functor]] and [[cofunctor]];

* A generalization of split [[Grothendieck fibration|Grothendieck opfibrations]] where the chosen lifts need not be [[Cartesian morphism|opcartesian morphisms]];

* A [[vertical categorification|categorification]] of classical [[lens (in computer science)|lenses]] between [[sets]]. 

## Definition ##

A **delta lens** $(f, \varphi) : A \to B$ from a [[category]] $A$ to a category $B$ consists of a [[functor]] $f : A \to B$ together with a _lifting operation_ sending each pair $(a \in A, u : f a \to b \in B)$ to a [[morphism]] $\varphi(a, u) : a \to a'$ in $A$, where $a' = cod(\varphi(a, u))$, such that 

* $\varphi$ defines a choice of lifts: $f \varphi(a, u) = u$,

* $\varphi$ preserves identity morphisms: $\varphi(a, 1_{f a}) = 1_{a}$, 

* $\varphi$ preserves composition: $\varphi(a, v \circ u) = \varphi(a', v) \circ \varphi(a, u)$ where $a' = cod(\varphi(a, u))$. 

\begin{centre}
\begin{tikzcd}
A
\arrow[d, "{(f, \varphi)}"']
& a
\arrow[d, phantom, "\vdots"]
\arrow[r, "{\varphi(a, u)}"]
& a'
\arrow[d, phantom, "\vdots"]
\\
B
& f a
\arrow[r, "u"]
& b = f a'
\end{tikzcd}
\end{centre}

## Properties ## 

\begin{proposition}
A delta lens $(f, \varphi) : A \to B$ is equivalent to a [[functor]] $f : A \to B$ and a [[cofunctor]] $\varphi : A \nrightarrow B$ such that $f a = \varphi_{0} a$ for all objects $a \in A$, and $f \varphi_{1}(a \in A, u : fa \to b \in B) = u$. 
\end{proposition}
\begin{proof}
See ([Ahman-Uustalu 2017, Section 6](#AhmanUustalu17)) and ([Clarke 2020](#Clarke20a)). 
\end{proof}

## Examples ##

* A delta lens between [[indiscrete category|codiscrete categories]] is precisely a classical [[lens (in computer science)]]; see ([Johnson-Rosebrugh 2016, Proposition 4](#JohnsonRosebrugh16)). 

* Every [[function]] $A \to B$ yields a delta lens $disc(A) \rightarrow disc(B)$ between [[discrete category|discrete categories]]. 

* Every [[discrete fibration|discrete opfibration]] is a delta lens whose lifting operation is determined by the unique [[Cartesian morphism|opcartesian lifts]]. Conversely, a delta lens is a discrete opfibration if the equation $\varphi(a, f w) = w$ holds for all morphisms $w : a \to a'$ in $A$. 

* A split [[Grothendieck fibration|Grothendieck opfibration]] is a delta lens whose chosen lifts are [[Cartesian morphism|opcartesian morphisms]].

* Dually, a split [[Grothendieck fibration]] $A \to B$ is a delta lens $A^{op} \to B^{op}$. 

* Every [[split epimorphism]] of [[monoid|monoids]] with a chosen [[section]] is a delta lens, when the monoids a considered as categories with a single object.

* More generally, every [[bijective on objects functor]] with a chosen [[section]] is a delta lens. 

## References ##

The notion of delta lens was first defined in [[computer science]] as a generalization of the classical [[lens (in computer science)|lenses]] between sets: 

* {#DiskinXiongCzarnecki11} Zinovy Diskin, Yingfei Xiong, Krzysztof Czarnecki, _From State- to Delta-Based Bidirectional Model Transformations: the Asymmetric Case_, Journal of Object Technology, 10, 2011 ([doi:10.5381/jot.2011.10.1.a6](http://dx.doi.org/10.5381/jot.2011.10.1.a6))

The connection between delta lenses and split [[Grothendieck fibration|Grothendieck opfibrations]] was first explored in the paper: 

* {#JohnsonRosebrugh13} [[Michael Johnson]], [[Robert Rosebrugh]], _Delta Lenses and Opfibrations_, Electronic Communications of the EASST, 57, 2013 ([doi:10.14279/tuj.eceasst.57.875](http://dx.doi.org/10.14279/tuj.eceasst.57.875))

The following paper details the connection between delta lenses and the classical [[lens (in computer science)|lenses]]: 

* {#JohnsonRosebrugh16} [[Michael Johnson]], [[Robert Rosebrugh]], _Unifying Set-Based, Delta-Based and Edit-Based Lenses_, CEUR Workshop Proceedings, 1571, 2016 ([pdf](http://ceur-ws.org/Vol-1571/paper_13.pdf))

The characterisation of delta lenses in terms of [[functor|functors]] and [[cofunctor|cofunctors]] first appeared in the paper: 

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf)) 

The notion of delta lens between [[internal category|internal categories]] as well as the link between [[cofunctor|cofunctors]], delta lenses, and split [[Grothendieck fibration|Grothendieck opfibrations]] is developed in the papers: 

* {#Clarke20a} [[Bryce Clarke]], _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} [[Bryce Clarke]], _Internal split opfibrations and cofunctors_, Theory and Applications of Categories, 35, 2020 ([link](http://www.tac.mta.ca/tac/volumes/35/44/35-44abs.html))

[[!redirects delta lenses]]
