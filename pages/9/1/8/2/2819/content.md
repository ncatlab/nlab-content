
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

[[Serre fibration]] $\Leftarrow$ **Hurewicz fibration** $\Rightarrow$ [[Dold fibration]] $\Leftarrow$ [[shrinkable map]]

***

# Contents
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

A [[continuous map]] $p \;\colon\; E\longrightarrow B$ of [[topological space]] is called a **Hurewicz fibration**  it it satisfies the [[right lifting property]] with respect to maps of the form 
$\sigma_0 \;\colon\; X\cong X\times\{0\}\hookrightarrow X\times I$ for all topological spaces $X$.

=--

+-- {: .num_remark}
###### Remark

This right lifting property is in this context called the [[homotopy lifting property]], because the maps from $X\times I$ are understood as [[homotopies]]. In more detail, for every space $X$, any homotopy $F:X\times I\to B$, and a continuous map $f:X\to E$, there is a homotopy $\tilde{F}:X\times I\to E$ such that $f =\tilde{F}
\circ\sigma_0 :=\tilde{F}_0$ and $F=p\circ\tilde{F}$: 

$$
  \array{
    X &\stackrel{f}\to& E
    \\
    \downarrow^{\sigma_0} &{}^{\tilde{F}}\nearrow&  \downarrow^p
    \\
    X\times I &\stackrel{F}{\to}& B
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Strictly speaking, the "all" in this context should be interpreted to refer to all spaces in whatever ambient category of spaces one is working in, since frequently this is a [[convenient category of spaces]].  In theory, therefore, a map in such a category could be a Hurewicz fibration in that category without necessarily being a Hurewicz fibration in the category of *all* topological spaces, but in practice this usually doesn't make a whole lot of difference.

=--

Instead of checking the homotopy lifting property, one can instead solve a universal problem:


+-- {: .num_theorem}
###### Theorem

A map is a Hurewicz fibration precisely if it admits a [[Hurewicz connection]]. (See there for details.)

=--


## Appearance in a model structure

There is a [[Quillen model category]] structure on [[Top]] where fibrations are Hurewicz fibrations, cofibrations are closed [[Hurewicz cofibrations]] and weak equivalences are [[homotopy equivalences]]; see [[model structure on topological spaces]] and [[Strøm's model category]]. There is a version of Hurewicz fibrations for [[pointed spaces]], as well as in the [[slice category]] $Top/B_0$ where $B_0$ is a fixed base.

## Abstract Hurewicz fibrations
 {#Abstractly}

The concept of Hurewicz fibrations makes sense also more generally in the presence of a (well behaved) [[interval object]], see for instance the early example of such in ([Kamps](#Kamps))([Williamson 13](#Williamson13)) for review and further developments. Discussion with a view towards [[homotopy type theory]] is in ([Warren 08](#Warren08)).


## References

The historical paper of Hurewicz is

* [[Witold Hurewicz]], _On the concept of fiber space_, Proc. Nat. Acad. Sci. USA __41__ (1955) 956--961; MR0073987 (17,519e) [PNAS,pdf](http://www.pnas.org/content/41/11/956.full.pdf).

A decent review of Hurewicz fibrations, [[Hurewicz connections]] and related issues is in 

* [[James Eells]], Jr., _Fibring spaces of maps_, in Richard Anderson (ed.) _Symposium on infinite-dimensional topology_

A textbook account of the [[homotopy lifting property]] is for instance in

* [[Alan Hatcher]], from p. 61 on in _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))

See also 

* [[R. Schwänzl]] and [[R. Vogt]], _Strong cofibrations and fibrations in enriched categories_, 2002.

* the textbooks on algebraic topology by Whitehead and Spanier.

Abstract analogues of Hurewicz fibrations can be found in 

* {#Kamps}[[K.H.Kamps]],_Kan-Bedingungen und abstrakte Homotopietheorie_, Math. Z. 124,1972, 215 -236

summarised in 

* K. H. Kamps and T. Porter, _Abstract Homotopy and Simple Homotopy Theory_ ([GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))

and further developed in 

* {#Williamson13} [[Richard Williamson]], _Cylindrical model structures_ ([arXiv:1304.0867](http://arxiv.org/abs/1304.0867), [web](http://rwilliamson-mathematics.info/cylindrical_model_structures.html))

Discussion with an eye towards [[homotopy type theory]] is in

* {#Warren08} [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, 2008 ([PDF](http://mawarren.net/papers/phd.pdf)) {#Warren}

[[!redirects Hurewicz fibration]]
[[!redirects Hurewicz fibrations]]