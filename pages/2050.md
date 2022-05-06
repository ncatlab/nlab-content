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

Every [[subgroup]] $H$ of a [[discrete group|discrete]] [[free group]] $G$ is itself a [[free group]]. Moreover, if $G$ is free on $k$ generators and $H$ has index $n$ in $G$, then $H$ is free on $n k - n + 1$ generators. 

=-- 
The second part of this yields what is called the _Schreier index formula_.

This has a number of different proofs. The first proof, perhaps nowadays the most familiar proof, is based on covering space theory (in particular, covering spaces of topological graphs). The second proof is quite similar in spirit but is based on groupoids (another way of viewing homotopy 1-types), and has the advantage that it circumvents the point-set topology considerations inherent to covering space theory. 

+-- {: .proof} 
###### Topological Proof (sketch) 
**of theorem \ref{NielsenSchreierTheorem}**

A free group $G = F(S)$ is, by the [[van Kampen theorem]], a [[fundamental group]] of a bouquet[^fine] of $S$ many circles, which is in particular a [[connected space|connected]] 1-dimensional [[CW-complex]] $X$ (in simpler language, a connected graph). By general [[covering space]] theory, given a (pointed) connected space $X$ with $\pi_1(X, x) = G$, subgroups $H \subseteq G$ are in bijective correspondence with isomorphism classes of connected covering spaces $p: (E, e) \to (X, x)$, with $\pi_1(E, e) \cong H$. Now, a covering space $E$ of a connected graph $X$ is also a connected graph. But any connected graph is [[homotopy equivalence|homotopy equivalent]] to a bouquet of circles, whose fundamental group is a free group. Thus $\pi_1(E, e)$ is a free group. 

The second statement is proved by observing that the Euler characteristic of $X$ is $\chi(X) = 1 - \rho(G)$, where $\rho(G)$ is the number of generators of the free group $G$, and $\chi(E) = n\chi(X)$ if $p \colon E \to X$ is a covering space with $n$ points in each fiber. 

Full details may be found in [May](#Maybook). Key technical ingredients include: (1) each connected graph $E$ contains a maximal [[tree]] $T$ (using [[Zorn's lemma]]), (2) the quotient map $E \to E/T$ is a homotopy equivalence, and $E/T$ is a bouquet of circles. 
=-- 

This topological proof can be reformulated in more algebraic language, using a little groupoid theory (groupoids being [[homotopy n-type|homotopy 1-types]]). A key construction here is the [[action groupoid]] $X \sslash G$ formed from a $G$-set $X$, also called a homotopy quotient or homotopy orbit space. 

+-- {: .proof}
###### Groupoidal Proof 
**of theorem \ref{NielsenSchreierTheorem}**

By the discussion at _[free groupoid -- fundamental group](http://ncatlab.org/nlab/show/free+groupoid#FundamentalGroup)_, we may think of the [[free group]] $F(S)$ as the [[fundamental group]] of a homotopy 1-type which is freely built from a single vertex and one loop from that vertex to itself for each element in $S$. This is the _[[free groupoid]]_ $*\sslash F(S)$ on this [[directed graph]] (a bouquet of circles). It is a classical fact (see at _[[universal principal bundle]]_) that the [[universal cover]] of this is the [[contractible]] groupoid $\mathbf{E}(F(S))$, the [[action groupoid]] $F(S)\sslash F(S)$ of $F(S)$ acting on itself from the right and that its [[quotient]] by the $F(S)$-action from the left recovers the original groupoid with fundamental group $F(S)$. If we instead quotient only by the given subgroup $H \hookrightarrow F(S)$, we obtain a connected groupoid with fundamental group $H$ (meaning simply that at any point or object $x$ of the groupoid, the group $\hom(x, x)$ is isomorphic to $H$). 

Thus, consider the [[quotient]] $H \backslash \mathbf{E}F(S) \simeq H \backslash \backslash *$, [[generalized the|the]] connected groupoid whose [[fundamental group]] is $\pi_1 = H$. By the properties of [[free groupoids]] discussed at _[free groupoid -- fundamental group](http://ncatlab.org/nlab/show/free+groupoid#FundamentalGroup)_ it is sufficient to show that $H \backslash \mathbf{E}F(S)$ is isomorphic to the [[free groupoid]] on a connected [[directed graph]]. But $\mathbf{E}F(S)$ itself is the free groupoid on a directed graph, namely on the _action graph_ $F(S)\sslash S$ (which is the same as the [[Cayley graph]] given by a set $S$ of generators and no relations), and we may consider the quotient graph $H \backslash (F(S) \sslash S)$. The free groupoid functor $F$ preserves this quotient. Thus we have  

$$
  H \backslash \mathbf{E}F\left(S\right) = H  \backslash F\left( F\left(S\right)\sslash S \right) =  F \left(\left(H \backslash F\left(S\right)\right)\sslash S\right)
  \,.
$$
as desired. 
=--

+-- {: .num_remark}
###### Remark

The original algebraic proof of theorem \ref{NielsenSchreierTheorem} was rather long and complicated, based on Nielsen's method of short cancellations in [[combinatorial group theory]] based on words (Nielsen's transformations of words, word length functions, ...). The class of _'projective groups'_ ( that is, in this context, [[projective object]]s in [[Grp|the category of groups]]) coincides with the class of free groups. 

The above simple [[homotopy theory|homotopy-theoretic]] proof was indicated in ([Higgins](#Higgins)), also ([Gilbert-Porter](#GilbrtPorter)).

=--
##Related entries

* [[Cayley graph]]


## Related concepts

* [submodules of a free module](free+module#SubmodulesOfFreeModules)

+-- {: .num_theorem #DedekindTheorem}
###### Theorem
**(Dedekind's theorem)**

Every subgroup of a [[free abelian group]] is itself a free abelian group.

=--

See at _[pid - Structure theory of modules](http://ncatlab.org/nlab/show/principal+ideal+domain#StructureTheoryOfModules)_ for details.

## References

The restricted statement that every subgroup of a free _[[abelian group]]_ is itself free was originally given by [[Richard Dedekind]].

[[Jakob Nielsen]] proved the statement for finitely-generated subgroups in 1921. The full theorem was proven in

* [[Otto Schreier]], _Die Untergruppen der freien Gruppen_, Abh. Mat Sem. Univ. Hamburg __3__, 167--169, 1927.

The topological proof is due to 

* [[Reinhold Baer]], [[Friedrich Levi]], _Freie Produkte und ihre Untergruppen_, Compositio Math. 3: 391&#8211;398. 

and another one due to [[Jean-Pierre Serre]]. 

Versions of the topological proof are given in many places. One is 

* [[Peter May]], _A Concise Course in Algebraic Topology_, Chicago Lectures in Mathematics, U. Chicago Press (1999), pp. 34-35. Revised version available online ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf)), chapter 4. 
{#Maybook}

Another can be found reviewed towards the end of 

* [[N. D. Gilbert]], [[T. Porter]], _Knots and Surfaces_, Oxford U.P., 1994.
 {#GilbertPorter}

Other related texts include

* H. Zieschang, _&#220;ber die Nielsensche K&#252;rzungsmethode in freien Produkten mit Amalgam_, Invent. Math. __10__, 4--37, 1970.

* W. Magnus, A. Karras, D. Solitar, _Combinatorial group theory_

* R. Lyndon, P. Schupp, _Combinatorial group theory_, Springer 1977 (Russian transl. Mir, Moskva 1980)

A groupoid-based proof of the Nielsen-Schreier theorem appears as theorem 9 in chapter 14 in

* [[Philip Higgins|P. J. Higgins]], _Categories and groupoids_, [Repr. Theory Appl. Categ., 1 &#8211; 178](http://www.emis.de/journals/TAC/reprints/articles/7/tr7abs.html) , ISSN 
1201-561X, reprint of the 1971 original _Notes on categories and groupoids_, (Van Nostrand 
Reinhold, London; MR0327946) with a new preface by the author. 
 {#Higgins}


Similar material can also be found in 

* [[R. Brown]], _Topology and groupoids_, Booksurge, 2006. 

[^fine]: A bouquet of circles is the [[coproduct]] of a collection of circles, each with a basepoint, in the category of [[pointed spaces]]. In other words, a [[pushout|wide pushout]] in [[Top]] of inclusions of a 1-point space into circles, with the evident pointing. 

Discussion in [[homotopy type theory]]/[[univalent foundations]] (see also [[mathematics presented in HoTT]]):

* {#Swan20} [[Andrew Swan]], _On the Nielsen-Schreier Theorem in Homotopy Type Theory_ ([arXiv:2010.01187](https://arxiv.org/abs/2010.01187))


[[!redirects Nielsen's theorem]]
[[!redirects Nielsen theorem]]
[[!redirects Nielsen–Schreier theorem]]
[[!redirects Nielsen--Schreier theorem]]

[[!redirects Dedekind-Nielsen-Schreier theorem]]
