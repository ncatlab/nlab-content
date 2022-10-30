+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Blakers-Massey theorem_ in the [[homotopy theory]] of spaces is concerned with describing algebraically the first obstruction to [[excision]] for relative [[homotopy groups]]. 

## Statement

This [[obstruction]] is measured by triad homotopy groups $\pi_m(X:A,B)$ for a pointed space $X$ with two subspaces $A,B$ each containing the base point. Here the group structure is defined for $m \geq 3$ and is abelian for $m \geq 4$. There is an exact sequence 

$$\cdots \to \pi_{n+1}(X;A,B) \to \pi_n (A, A \cap B) \to^{\epsilon} \pi_n( X,B) \to \pi_n(X;A,B) \to \cdots  $$
where $\epsilon$ is the excision map. The main result of Blakers and Massey is as follows:

+-- {: .num_theorem}
###### Theorem

Suppose the triad **X** $ =(X;A,B)$ is such that: (i) the interiors of $A,B$ cover $X$; (ii) that $A,B$ and $C=A \cap B$ are connected; (iii) that $C$ is simply connected; (iv) and that $(A,C)$ is $(m-1)$-connected and $(B,C)$ is $(n-1)$-connected, $m,n \geq 3$. Then **X**$=(X;A,B)$ is $(m+n-2)$-connected and if $C$ is simply connected then the morphism given by the generalised Whitehead product
$$ \pi_{m}(A,C) \otimes \pi_{n}(B,C) \to \pi_{m+n-1}(X;A,B)$$
_is an isomorphism_. 

=--

+-- {: .num_remark}
###### Remark

A more intrinsic statement in the language of [[homotopy theory]] of the connectivity part of the theorem is that for $f_1$ and $f_2$ two [[maps]] out of the same [[domain]] which are $n_1$-[[n-connected morphism|connective]] and $n_2$-connective, respectively, then the canonical map from that domain into the [[homotopy pullback]] of their [[homotopy pushout]]

$$
  \array{
    X &\stackrel{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{\mathrlap{f_2}} & \searrow
    \\
    Y_2 && Y_2 \underset{Y_2 \underset{X}{\coprod} Y_1}{\times} Y_1
  }
$$

is $(n_1 + n_2 - 1)$-[[n-connected morphism|connective]].


In the original connectivity statement of the theorem ([Blakers-Massey 51](#BlakersMassey51)) this was considered for the [[homotopy theory]] of [[topological spaces]], hence for "bare" [[homotopy types]]/[[∞-groupoids]] but the statement holds true in all [[(∞,1)-toposes]] ([[Charles Rezk]]) and in fact in [[homotopy type theory]] ([HoTTBook, theorem 8.10.2](#HoTTBook), [Lumsdaine-Finster-Licata 13](#LumsdaineFinsterLicata13)), hence also for "[[geometric homotopy types]]".

=--


+-- {: .num_remark}
###### Remark

For the special case that $Y_1 \simeq Y_2 \simeq \ast$ are point contractible, the Blakers-Massey theorem reduces to the [[Freudenthal suspension theorem]].

=--


+-- {: .num_remark}
###### Remark

Since the tensor product is zero if one of its factors is zero, this result also gives criteria for the excision morphism $\epsilon$ to be an isomorphism in a certain range of dimensions. For this reason the excision consequences of that sequence are  also  called the _excision theorem of Blakers and Massey_ and have been given quite separate proofs for example in ([Hatcher](#Hatcher)), and in ([tom Dieck](#tomDiek08)). The  first non zero triad homotopy group is also called the _critical group_. Note that in _algebraic topology_ one wants _algebraic_ results, not just connectivity results. 

=--

### Generalizations

The natural question is what happens if the conditions  that $m,n \geq 3$ and $C$ simply connected are weakened.   For example in the case $m=n=2$  we have the additional structure that the morphisms $\pi_2(A,C) \to \pi_1(C), \pi_2(B,C) \to \pi_1(C)$ are crossed modules, and so the required relative homotopy groups are in general nonabelian. If $m \geq 3 ,n \geq 3$ then $\pi_m(A,C), \pi_n(B,C)$ are still $\pi_1(C)$-modules.


The extension to the non simply connected case was given by Brown and Loday; one simply replaces the usual tensor product by the nonabelian tensor product of groups which act on each other and on themselves by conjugation. This result is a special case of Seifert-van Kampen Theorem for $n$-cubes of spaces. Notice that the assumption (i) of the theorem is reminiscent of such a type of theorem. The useful fact is that one gets such a theorem for a certain kind of _structured space_ which allows for the development of algebraic structures which have structures in a range of dimensions.

Thus one of the intuitions is that the Blakers-Massey Theorem, and hence also the FST,  is of the Seifert-van Kampen type, since we are assuming that $X$ is the union of the interiors of $A,B$. 




## References

### Classical

The original connectivity  statement of the theorem is due to 

* [[Albert Blakers]], [[William  Massey]], _The homotopy groups of a triad I_ , Annals of Mathematics 53: 161&#8211;204, (1951)
  {#BlakersMassey51}

This is reviewed for instance as Theorem 4.23 in the textbook

* {#Hatcher} [[Alan Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

and as Theorem 6.4.1 in 

* {#tomDiek08} [[Tammo tom Dieck]],  _Algebraic Topology_, EMS Textbooks in Mathematics, (2008). 

The algebraic statement and proof is in 

* [[Albert Blakers]], [[William Massey]], _The homotopy groups of a triad. {III}_,  Ann. of Math. (2), 58: (1953) 409--417. 

The generalisation of the algebraic statement is Theorem 4.3 in: 

* [[Ronnie Brown|R. Brown]] and J.-L. Loday, Homotopical excision, and Hurewicz
theorems, for $n$-cubes of spaces, _Proc. London Math. Soc._
(3) 54 (1987) 176-192.

which relies essentially on the paper 

* [[Ronnie Brown| R. Brown]] and J.-L. Loday, Van Kampen theorems for diagrams of
spaces,  _Topology_ 26 (1987) 311-334, 

for the van Kampen Theorem and for the nonabelian tensor product of groups. Here is a link to a bibliography of 131 items on the [nonabelian tensor product](http://pages.bangor.ac.uk/~mas010/nonabtens.html ). 

Further applications are explained in 

[[Ronnie Brown|R. Brown]],  Triadic Van Kampen theorems and Hurewicz theorems, _
Algebraic  Topology, Proc. Int. Conf. March 1988_, Edited
M.Mahowald and S.Priddy,  Cont. Math. 96 (1989) 39-57.

The following paper  applies the methods of the above two Brown-Loday papers to the well known problem of $n$-ad connectivity and to determination of the critical group, see Theorem 3.8 of: 

* Ellis, G.J. and Steiner, R. Higher-dimensional crossed modules and the homotopy groups  of $(n+1)$-ads. _J. Pure Appl. Algebra_ 46 (1987) 117--136. 

The methods work because of their equivalence between cat$^n$-groups and crossed $n$-cubes of groups. This can be explained by saying that wee need two kinds of algebraic categories for calculations with $(n+1)$-types: _broad_ categories for conjecturing and proving theorems, and _narrow_ algebraic categories for calculations and relations with classical ideas. In this case the broad category is that of cat$^n$-groups, and the narrow category is that of crossed $n$-cubes of groups, which are related geometrically to the homotopy groups of $r$-ads and to generalised Whitehead products. The tricky equivalence between the two kinds of categories is one of the engines behind the results, since it enables the use of whichever category is most convenient at any given time. Note also these two categories model weak, pointed, homotopy $(n+1)$-types, as shown by Loday in his paper

* J.-L. Loday,  Spaces with finitely many non-trivial homotopy groups, _J. Pure Appl. Algebra_ 24 (1982)  179-202. 


Discussion of Blakers-Massey for [[ring spectra]]/[[E-∞ rings]] and other [[algebras over operads]] is in 

* Michael Ching, [[John Harper]], _Higher homotopy excision and Blakers-Massey theorems for structured ring spectra_ ([arXiv:1402.4775](http://arxiv.org/abs/1402.4775))


###  In homotopy type theory and $\infty$-topos theory
 {#ReferencesInHoTT}

The general version of the connectivity theorem in [[homotopy type theory]]
(and thus in [[(infinity,1)-topos theory]]) appears as theorem 8.10.2 of

* {#HoTTBook} [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

The proof formalized in HoTT-[[Agda]] is in

* {#LumsdaineFinsterLicata13} [[Peter LeFanu Lumsdaine]], [[Eric Finster]], [[Dan Licata]], _[BlakersMassey.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/BlakersMassey.agda)_

* {#Lumsdaine13} [[Peter LeFanu Lumsdaine]], _The Blakers-Massey theorem in homotopy type theory_ talk at [CONFERENCE ON TYPE THEORY, HOMOTOPY THEORY AND UNIVALENT FOUNDATIONS](http://www.crm.cat/en/Activities/Pages/ActivityFoldersAndPages/Curs%202013-2014/CHomotopy/chomotopy.aspx) (2013) ([talk abstracts pdf]( http://www.crm.cat/en/Activities/Documents/AbstractsTypeTheory.pdf
)):

> One such result, the Blakers-Massey connectivity theorem, is of particular interest in that all classical proofs use some specifics of their settings (usually, $Top$ or $SSet$) not available to us; so the type-theoretic proof was, by necessity, new in parts. This allowed us, as a by-product, to translate the proof back into classical language and obtain the theorem in wider generality than was previously known: we show that it holds in any infinity-topos (in the sense of Lurie). I will introduce the Blakers-Massey theorem and our approach to it, and discuss the process of translating a type-theoretic proof into infinity-categorical language