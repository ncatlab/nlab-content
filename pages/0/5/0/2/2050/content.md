+-- {: .un_theorem}
###### Nielsen--Schreier theorem
Every subgroup of a [[free group|free discrete group]] is free.
=--

Nielsen's theorem is the weaker form proved by [[Jakob Nielsen]] in 1921 saying that every finitely generated subgroup of a free group is free. [[Otto Schreier]] proved in 1927 the theorem in full generality.

The algebraic proof of this theorem is rather long and complicated and it is usually based on Nielsen's method of short cancellations in [[combinatorial group theory]] based on words (Nielsen's transformations of words, word length functions, ...). The class of _'projective groups'_ ( that is, in this context, [[projective object]]s in [[Grp|the category of groups]]) coincides with the class of free groups. 

There is however a short proof by the basic methods of [[algebraic topology]], see below for a sketch. There is a good case to be made that really this is a groupoid theoretic proof; see the book by [[Philip Higgins]], listed below.

As stated, the theorem is not valid in [[constructive mathematics]], although Nielsen\'s weaker 1921 version is.

##An  idea of the topological proof:

(For ease, think of it in the simple case of a finitely generated free group, $F$.)

* The fundamental group of a connected graph, $\Gamma$, is a free group.  (Take a maximal tree, $T$, in the graph and the rank of the free group will be the number of edges in $\Gamma \setminus T$.)

* Any free group is the fundamental group of a bouquet of circles, which is, of course, a connected graph, $\Gamma$, (with one vertex).

* If $H\lt F$ is a subgroup, it corresponds to a covering graph of $\Gamma$, and this covering graph will have fundamental group isomorphic to $H$, ...

hence $H$ is a free group.

The rank of $H$ can be calculated by the **Schreier index  formula** if the rank of $F$ is finite and the index of $H$ in $F$ is finite:

_Let $H$ be a subgroup of finite index $i$ in the free group $F$ of finite rank $r$, then $H$ is a free group of rank $i(r-1)+1$._

The proof is by using the maximal tree argument mentioned above;  see Gilbert and Porter, listed below, or as described in [[Ronnie Brown]]'s

##Literature##

* W. Magnus, A. Karras, D. Solitar, _Combinatorial group theory_

* R. Lindon, P. Schupp, _Combinatorial group theory_, Springer 1977 (Russian transl. Mir, Moskva 1980)

* O. Schreier, _Die Untergruppen der freien Gruppen_, Abh. Mat Sem. Univ. Hamburg __3__, 167--169, 1927.

* H. Zieschang, _&#220;ber die Nielsensche K&#252;rzungsmethods in freien Produkten mit Amalgam_, Invent. Math. __10__, 4--37, 1970.

A version of the topological proof can be found towards the end of 

* [[N. D. Gilbert]] and [[T. Porter]], Knots and Surfaces, Oxford U.P., 1994.

The groupoid version and a lot of related results are given in 


* [[Philip Higgins|P. J. Higgins]], _Categories and groupoids_, [Repr. Theory Appl. Categ., 1 &#8211; 178](http://www.emis.de/journals/TAC/reprints/articles/7/tr7abs.html) (electronic), ISSN 
1201-561X, reprint of the 1971 original _Notes on categories and groupoids_, (Van Nostrand 
Reinhold, London; MR0327946) with a new preface by the author. 




Similar material can also be found in 

* [[R. Brown]], _Topology and groupoids_, Booksurge, 2006. 


[[!redirects Nielsen's theorem]]
[[!redirects Nielsen theorem]]
[[!redirects Nielsen–Schreier theorem]]
[[!redirects Nielsen--Schreier theorem]]