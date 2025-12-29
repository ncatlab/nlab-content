
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



\tableofcontents


## Idea

Given a system of finitely many word equations 

$$
  F_\alpha(a_1,\ldots,a_n,x_1,\ldots,x_m) = 1
  \,,
  \;\;\;
  \text{where}\; \alpha \in \{1,\ldots, K\}
$$
with coefficients $a_1,\ldots, a_n$ in a [[group]] $G$, a solution in $G$ for unknowns $x_1,\ldots,x_m$ supplies the evaluation "functional" $Hom(G_F,G)$, where $G_F$ is
the [[direct product]] of $n+m$ copies of $G$ modulo the [[normal subgroup]] determined by $F_\alpha$ for fixed constants $a_i$. 

[Makanin 1982](#Makanin1982) found an [[algorithm]] which for such a finite system of equations over a free group on $s$ letters produces all solutions when at least one exists. In his thesis, [Razborov 1984](#Razborov1984) developed the theory further. 

Later, similar schemes, now called *Makanin-Razborov diagrams*, for finding $Hom(H,G)$ in the larger generality where $H$ is some [[finitely generated group]], were discussed by various authors, including Sela, Reinfeldt, Weidman, Bestvina, and Feighn.


## Literature

The original articles:

* {#Makanin1982} Г. С. Маканин, _Уравнения в свободной группе_, Изв. АН СССР. Сер. матем., 46:6 (1982), 1199--1273 [pdf](https://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=1703&what=fullt&option_lang=rus); engl. transl. G. S. Makanin, _Equations in a free group,_,  Math. USSR-Izv., 21:3 (1983), 483--546 [pdf](https://www.mathnet.ru/php/getFT.phtml?jrnid=sm&paperid=2805&what=fullteng&option_lang=eng)

* {#Razborov1984} А. А. Разборов, _О системах уравнений в свободной группе_, Изв. АН СССР. Сер. матем., 48:4 (1984), 779--832; engl. transl. A. A. Razborov, _On systems of equations in a free group_, Math. USSR-Izv., 25:1 (1985), 115--162

Review:

* Richard Weidmann, Cornelius Reinfeldt: *Makanin–Razborov diagrams for hyperbolic groups*, Annales mathématiques Blaise Pascal **26** 2 (2019) 119--208 &lbrack;[doi:10.5802/ambp.387](https://doi.org/10.5802/ambp.387)&rbrack;

* Montserrat Casals-Ruiz, Ilya Kazachkov: *Makanin-Razborov diagrams*, talk notes (2016) &lbrack;[pdf](https://www.macs.hw.ac.uk/~lc45/Conferences/2016/Slides_for_web/Casals-Ruiz_Kazachkov_2.pdf)&rbrack;

[[!redirects Makanin-Razborov diagrams]]



