
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_theorem #NielsenSchreierTheorem}
###### Theorem
**(Nielsen--Schreier theorem)**

Every [[subgroup]] of a [[discrete group|discrete]] [[free group]] is itself a [[free group]].

=--


+-- {: .proof}
###### Proof

By the discussion at _[free groupoid -- fundamental group](http://ncatlab.org/nlab/show/free+groupoid#FundamentalGroup)_, we may think of the [[free group]] $F(S)$ as the [[fundamental group]] of a [[homotopy n-type|homotopy 1-type]] which is freely built from a single vertex and one loop from that vertex to itself for each element in $S$. This is the _[[free groupoid]]_ $*\sslash F(S)$ on this [[directed graph]] (sometimes called a "bouquet of circles"). It is a classical fact (see at _[[universal principal bundle]]_) that the [[universal cover]] of this is the [[contractible]] groupoid $\mathbf{E}(F(S))$, the [[action groupoid]] $F(S)\sslash F(S)$ of $F(S)$ acting on itself from the right and that its [[quotient]] by the $F(S)$-action from the left recovers the original groupoid with fundamental group $F(S)$. The idea of the following proof is to instead quotient only by the given subgroup $H \hookrightarrow F(S)$ and hence obtain a groupoid with fundamental group $H$. It is then sufficient to observe that this quotient is still a [[free groupoid]] on a directed graph to conclude that $H$ is a free group.

So let  $\mathbf{E} F(S) \coloneqq  F(S)\sslash F(S)$ be the [[action groupoid]] of $F(S)$ acting on itself (see also at [[universal principal bundle]]). This is [[contractible]], $\mathbf{E}F(S) \simeq *$, and comes with a canonical $F(S)$-[[action]] (from the other side). Hence it comes with an induced $H$-action and the [[quotient]] $H \backslash \backslash\mathbf{E}F(S) \simeq H \backslash \backslash *$ is [[generalized the|the]] connected groupoid whose [[fundamental group]] is $\pi_1 = H$. By the properties of [[free groupoids]] discussed at _[free groupoid -- fundamental group](http://ncatlab.org/nlab/show/free+groupoid#FundamentalGroup)_ it is sufficient to show that $H \backslash \backslash\mathbf{E}F(S)$ is isomorphic to the [[free groupoid]] on a connected [[directed graph]]. But $\mathbf{E}F(S)$ itself is the free groupoid on a directed graph, namely on the _action graph_ $F(S)\sslash S$. So 

$$
  H \backslash \backslash \mathbf{E}F\left(S\right) = H  \backslash F\left( F\left(S\right)\sslash S \right) =  F \left(\left(H \backslash F\left(S\right)\right)\sslash S\right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The original algebraic proof of theorem \ref{NielsenSchreierTheorem} was rather long and complicated, based on Nielsen's method of short cancellations in [[combinatorial group theory]] based on words (Nielsen's transformations of words, word length functions, ...). The class of _'projective groups'_ ( that is, in this context, [[projective object]]s in [[Grp|the category of groups]]) coincides with the class of free groups. 

The above simple [[homotopy theory|homotopy-theoretic]] proof was indicated in ([Higgins](#Higgins)), also ([Gilbert-Porter](#GilbrtPorter)).

=--



## Related concepts

* [submodules of a free module](free+module#SubmodulesOfFreeModules)

## References

The restricted statement that every subgroup of a free _[[abelian group]]_ is itself free was originally given by [[Richard Dedekind]].

[[Jakob Nielsen]] proved the statement for finitely-generated subgroups in 1921. The full theorem was proven in

* [[Otto Schreier]], _Die Untergruppen der freien Gruppen_, Abh. Mat Sem. Univ. Hamburg __3__, 167--169, 1927.

The topological proof is due to 

* [[Reinhold Baer]], [[Friedrich Levi]], _Freie Produkte und ihre Untergruppen_, Compositio Math. 3: 391&#8211;398. 

and another one due to [[Jean-Pierre Serre]].

A version of the topological proof can be found reviewed towards the end of 

* [[N. D. Gilbert]], [[T. Porter]], _Knots and Surfaces_, Oxford U.P., 1994.
 {#GilbertPorter}

Other related texts include

* H. Zieschang, _&#220;ber die Nielsensche K&#252;rzungsmethode in freien Produkten mit Amalgam_, Invent. Math. __10__, 4--37, 1970.

* W. Magnus, A. Karras, D. Solitar, _Combinatorial group theory_

* R. Lyndon, P. Schupp, _Combinatorial group theory_, Springer 1977 (Russian transl. Mir, Moskva 1980)

The groupoid version and a lot of related results are given in 


* [[Philip Higgins|P. J. Higgins]], _Categories and groupoids_, [Repr. Theory Appl. Categ., 1 &#8211; 178](http://www.emis.de/journals/TAC/reprints/articles/7/tr7abs.html) , ISSN 
1201-561X, reprint of the 1971 original _Notes on categories and groupoids_, (Van Nostrand 
Reinhold, London; MR0327946) with a new preface by the author. 
 {#Higgins}


Similar material can also be found in 

* [[R. Brown]], _Topology and groupoids_, Booksurge, 2006. 


[[!redirects Nielsen's theorem]]
[[!redirects Nielsen theorem]]
[[!redirects Nielsen–Schreier theorem]]
[[!redirects Nielsen--Schreier theorem]]