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

The _Blakers-Massey theorem_ in the [[homotopy theory]] of [[pointed topological spaces]] is concerned with algebraically describing the first obstruction to [[excision]] for relative [[homotopy groups]]. There is also a weaker version just describing vanishing conditions which should be called the _Blakers-Massey connectivity theorem_. 

## Statement

### Traditional

This [[obstruction]] is measured by triad homotopy groups $\pi_m(X;A,B)$ for a pointed space $X$ with two subspaces $A,B$ each containing the base point. Here the group structure is defined for $m \geq 3$ and is abelian for $m \geq 4$. There is an exact sequence 

$$\cdots \to \pi_{n+1}(X;A,B) \to \pi_n (A, A \cap B) \to^{\epsilon} \pi_n( X,B) \to \pi_n(X;A,B) \to \cdots  $$
where $\epsilon$ is the excision map. The main result of Blakers and Massey is as follows:

+-- {: .num_theorem}
###### Theorem

Suppose the triad **X** $ =(X;A,B)$ is such that: (i) the interiors of $A,B$ cover $X$; (ii) that $A,B$ and $C=A \cap B$ are connected; (iii) that $C$ is simply connected; (iv) and that $(A,C)$ is $(m-1)$-connected and $(B,C)$ is $(n-1)$-connected, $m,n \geq 3$. Then **X**$=(X;A,B)$ is $(m+n-2)$-connected and if $C$ is simply connected then the morphism given by the generalised Whitehead product
$$ \pi_{m}(A,C) \otimes \pi_{n}(B,C) \to \pi_{m+n-1}(X;A,B)$$
_is an isomorphism_. 

=--

([Blakers-Massey 51](#BlakersMassey51), [tomDieck 08, theorem 6.4.1](#tomDieck08)).

+-- {: .num_remark #InTermsOfPushouts}
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

=--

+-- {: .num_remark}
###### Remark

For the special case that $Y_1 \simeq Y_2 \simeq \ast$ are point contractible, the Blakers-Massey theorem reduces to the [[Freudenthal suspension theorem]].

=--

+-- {: .num_remark}
###### Remark

Since the tensor product is zero if one of its factors is zero, this result also gives criteria for the excision morphism $\epsilon$ to be an isomorphism in a certain range of dimensions. For this reason the excision consequences of that sequence are  also  called the _excision theorem of Blakers and Massey_ and have been given quite separate proofs for example in ([Hatcher](#Hatcher)), and in ([tom Dieck](#tomDieck08)). The  first non zero triad homotopy group is also called the _critical group_. Note that in _algebraic topology_ one wants _algebraic_ results, not just connectivity results. 

=--

+-- {: .num_remark}
###### Remark

A natural question is what happens if the conditions  that $m,n \geq 3$ and $C$ simply connected are weakened.   For example in the case $m=n=2$  we have the additional structure that the morphisms $\pi_2(A,C) \to \pi_1(C), \pi_2(B,C) \to \pi_1(C)$ are crossed modules, and so the required relative homotopy groups are in general nonabelian. If $m \geq 3 ,n \geq 3$ then $\pi_m(A,C), \pi_n(B,C)$ are still $\pi_1(C)$-modules.


The extension to the non simply connected case was given by Brown and Loday; one simply replaces the usual tensor product by the nonabelian tensor product of groups which act on each other and on themselves by conjugation. This result is a special case of a Seifert-van Kampen Theorem for $n$-cubes of spaces. Notice that the assumption (i) of the theorem is reminiscent of such a type of theorem. The useful fact is that one gets such a theorem for a certain kind of _structured space_ which allows for the development of algebraic structures which have structures in a range of dimensions.

Thus one of the intuitions is that the Blakers-Massey Theorem, and hence also the FST,  is of the Seifert-van Kampen type, since we are assuming that $X$ is the union of the interiors of $A,B$. 

=--

### In higher topos theory

+-- {: .num_prop}
###### Proposition

The Blakers-Massey connectivity theorem in the form of remark \ref{InTermsOfPushouts} holds in every [[(∞,1)-topos]] of [[(∞,1)-sheaves]].

=--

This is shown in ([Rezk 10, prop. 8.16](#Rezk10)) with reference to [[(∞,1)-sites]].
An intrinsic proof in [[homotopy type theory]] is announced in ([HoTTBook, theorem 8.10.2](#HoTTBook), [Lumsdaine-Finster-Licata 13](#LumsdaineFinsterLicata13)). The fully formal computer-checked version of this proof appears as HoTT-[[Agda]] code in ([Favonia 14](#Favonia)).

This translates to an [[internal language]] proof of Blakers-Massey valid in all [[(∞,1)-toposes]] (including [[elementary (∞,1)-toposes]]). Unwinding of the fully formal HoTT proof to ordinary mathematical language is, for the special case of the [[Freudenthal suspension theorem]], in ([Rezk 14](#Rezk14)).


### Higher cubical BM-theorems and analytic $\infty$-functors
 {#HigherCubical}

There are higher analogs of the BM-theorem with (pushout) squares replaced by higher dimensional cubes. The higher BM-theorem ([Goodwillie 91](#Goodwillie91)) says equivalently that the identity [[(∞,1)-functor]] on [[∞Grpd]] is a 1-[[analytic (∞,1)-functor]]. See ([Munson-Volic 15, section 6](#MunsonVolic15)).




## References

### Classical

The original connectivity  statement:

* {#BlakersMassey51} [[Albert Blakers]], [[William  Massey]], _The homotopy groups of a triad I_ , Annals of Mathematics 53: 161&#8211;204, (1951) ([jstor:1969346](https://www.jstor.org/stable/1969346))

The algebraic statement and proof:

* [[Albert Blakers]], [[William Massey]], _The homotopy groups of a triad. {III}_,  Ann. of Math. (2), 58: (1953) 409--417 ([jstor:1969744](https://www.jstor.org/stable/1969744))
  

Textbook accounts:

* {#tDKP70} [[Tammo tom Dieck]], [[Klaus Heiner Kamps]], [[Dieter Puppe]], Section 15 of: *Homotopietheorie*, Lecture Notes in Mathematics **157** Springer 1970 ([doi:10.1007/BFb0059721](https://link.springer.com/book/10.1007/BFb0059721))


* {#Kochmann96} [[Stanley Kochmann]], theorem 3.2.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Hatcher} [[Alan Hatcher]], theorem 4.23 _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

* {#tomDieck08} [[Tammo tom Dieck]],  theorem 6.4.1 _Algebraic Topology_, EMS Textbooks in Mathematics, (2008) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/diecktop.pdf))



The Blakers-Massey's Connectivity Theorem was shown to be a consequence of Farjoun's "cellular inequalities" 

* [[Emmanuel Dror Farjoun]], _Cellular spaces, null spaces and homotopy localization_m No. 1621-1622. Springer, 1996]

is Theorem 1.B of 

* [[Wojciech Chachólski]], _A generalization of the triad theorem of Blakers-Massey_ Topology 36.6 (1997): 1381-1400

This would constitute a purely [[homotopy theory|homotopy-theoretic]] proof.

The generalisation of the algebraic statement is Theorem 4.3 in: 

* [[Ronnie Brown|R. Brown]] and [[Jean-Louis Loday]], Homotopical excision, and Hurewicz theorems, for $n$-cubes of spaces, _Proc. London Math. Soc._
(3) 54 (1987) 176-192.  [pdf](https://groupoids.org.uk/pdffiles/VKTEVANS2.pdf) 

which relies essentially on the paper 

* [[Ronnie Brown| R. Brown]] and J.-L. Loday, Van Kampen theorems for diagrams of
spaces,  _Topology_ 26 (1987) 311-334, 

for the van Kampen Theorem and for the nonabelian tensor product of groups. Here is a link to a bibliography of 170 items on the [nonabelian tensor product](http://groupoids.org.uk/nonabtens.html ). 

Further applications are explained in 

[[Ronnie Brown|R. Brown]],  Triadic Van Kampen theorems and Hurewicz theorems, _
Algebraic  Topology, Proc. Int. Conf. March 1988_, Edited
M.Mahowald and S.Priddy,  Cont. Math. 96 (1989) 39-57.  [pdf](http://groupoids.org.uk//pdffiles/VKTEVANS2.pdf) 


The following paper  applies the methods of the above two Brown-Loday papers to the well known problem of $n$-ad connectivity and to determination of the critical group, see Theorem 3.8 of: 

* Ellis, G.J. and Steiner, R. Higher-dimensional crossed modules and the homotopy groups  of $(n+1)$-ads. _J. Pure Appl. Algebra_ 46 (1987) 117--136. 

The methods work because of their equivalence between cat$^n$-groups and crossed $n$-cubes of groups. This can be explained by saying that we need two kinds of algebraic categories for calculations with $(n+1)$-types: _broad_ categories for conjecturing and proving theorems, and _narrow_ algebraic categories for calculations and relations with classical ideas. In this case the broad category is that of cat$^n$-groups, and the narrow category is that of crossed $n$-cubes of groups, which are related geometrically to the homotopy groups of $r$-ads and to generalised Whitehead products. The tricky equivalence between the two kinds of categories is one of the engines behind the results, since it enables the use of whichever category is most convenient at any given time. Note also these two categories model weak, pointed, homotopy $(n+1)$-types, as shown by Loday in his paper

* [[Jean-Louis Loday]],  Spaces with finitely many non-trivial homotopy groups, _J. Pure Appl. Algebra_ 24 (1982)  179-202. 

Further background to these ideas is in 

* [[Ronnie Brown| R. Brown]] "A philosophy of modelling and computing homotopy types" Presentation to CT2015, Aveiro, Portugal, June 14-19. [pdf](https://groupoids.org.uk//pdffiles/aveiro-beamer-handout.pdf) and in "Modelling and computing homotopy types: I" Indag.Math.  29  (2018) 459-482 [pdf](https://www.sciencedirect.com/science/article/pii/S0019357717300460)

Discussion of Blakers-Massey connectivity for [[ring spectra]]/[[E-∞ rings]] and other [[algebras over operads]] is in 

* Michael Ching, [[John Harper]], _Higher homotopy excision and Blakers-Massey theorems for structured ring spectra_ ([arXiv:1402.4775](http://arxiv.org/abs/1402.4775))

The higher cubical version of Blakers-Massey connectivity is due to 

* {#Goodwillie91} [[Tom Goodwillie]], _Calculus II: Analytic functors_, K-Theory  01/1991; 5(4):295-332. DOI: 10.1007/BF00535644

a textbook account is in 

* {#MunsonVolic15} [[Brian Munson]], [[Ismar Volic]], _Cubical homotopy theory_, Cambridge University Press, 2015 [pdf](http://palmer.wellesley.edu/~ivolic/pdf/Papers/CubicalHomotopyTheory.pdf)


### In $\infty$-topos theory and homotopy type theory
 {#ReferencesInHoTT}

A proof of Blakers-Massey connectivity in general [[∞-stack]] [[(∞,1)-toposes]] is in prop. 8.16 of

* {#Rezk10} [[Charles Rezk]], _Toposes and homotopy toposes_ (2010) ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

A general version of the connectivity theorem in [[homotopy type theory]] 
(and thus in [[(infinity,1)-topos theory]]) was found by

* {#LumsdaineFinsterLicata13} [[Peter LeFanu Lumsdaine]], [[Eric Finster]], [[Dan Licata]] (to appear) 

A fully computer-checked version of this proof in HoTT-[[Agda]] was produced in

* {#Favonia} [[Favonia]], _[BlakersMassey.agda](https://github.com/HoTT/HoTT-Agda/blob/1.0/Homotopy/BlakersMassey.agda)_

the statement appeared also as

* {#HoTTBook} [[Univalent Foundations Project]], theorem 8.10.2 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

and an announcement was given in

* {#Lumsdaine13} [[Peter LeFanu Lumsdaine]], _The Blakers-Massey theorem in homotopy type theory_ talk at [Conference on Type Theory, Homotopy Theory and Univalent Foundations](http://www.crm.cat/en/Activities/Pages/ActivityFoldersAndPages/Curs%202013-2014/CHomotopy/chomotopy.aspx) (2013) ([talk abstracts pdf](http://www.crm.cat/en/Activities/Documents/AbstractsTypeTheory.pdf)).

A writeup finally appeared as

* {#FFLL16} Kuen-Bang Hou ([[Favonia]]), [[Eric Finster]], [[Dan Licata]], [[Peter LeFanu Lumsdaine]], _A mechanization of the Blakers-Massey connectivity theorem in Homotopy Type Theory_ ([arXiv.1605.03227](https://arxiv.org/abs/1605.03227))

Another unwinding to ordinary mathematical language of the above [code](#Favonia) was meanwhile given in

* {#Rezk14} [[Charles Rezk]], _Proof of the Blakers-Massey theorem_, 2014 [pdf](http://www.math.uiuc.edu/~rezk/freudenthal-and-blakers-massey.pdf).

prompted by online discussion at

* {#Schreiber14} [[Urs Schreiber]], _Explaining the point of HoTT on FOM_, Google+ thread 2014-10-22 ([archived version](https://github.com/DavidMichaelRoberts/Sandbox/blob/master/Schreiber_Gplus_post.md))

  (scroll down a fair bit through the list of replies there to see the exchange between [[Charles Rezk]] and [[Favonia]]).

Further developments along these lines are in

* {#AnelBiedermanFinsterJoyal17a} [[Mathieu Anel]], [[Georg Biedermann]], [[Eric Finster]], [[André Joyal]], _A Generalized Blakers-Massey Theorem_ ([arXiv:1703.09050](https://arxiv.org/abs/1703.09050))

* {#AnelBiedermanFinsterJoyal17b} [[Mathieu Anel]], [[Georg Biedermann]], [[Eric Finster]], [[André Joyal]], _Goodwillie's Calculus of Functors and Higher Topos Theory_ ([arXiv:1703.09632](https://arxiv.org/abs/1703.09632))

### In shape theory

* &#352;ime Ungar, $n$-Connectedness of inverse systems and applications to shape theory, Glasnik Matemati&#269;ki 13 (1978), 371-396 [pdf](http://www.irb.hr/korisnici/zskoda/ungarConnwoabsh.pdf)

> Let (X, A, x) be an n-connected inverse system of CW-pairs such that the restriction (A, x) is m-connected. We prove that there exists an isomorphic inverse system (Y, B, y) having n-connected terms such that the terms of the restriction (B, y) are m-connected. This result is then applied in proving analogues of Hurewicz and Blakers-Massey theorems for homotopy pro-groups and shape groups.