
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of **weakly open subtopos** is weakening of the concept of a [[dense subtopos]] in topos theory.

## Definition

Let $\mathcal{E}$ be a [[topos]] and $Sh_j(\mathcal{E})$ a subtopos of $\mathcal{E}$ with $j$ the corresponding [[Lawvere-Tierney topology]], $a_j$ the corresponding [[associated sheaf functor]] and $\neg$ and $\neg^j$ the pseudo-complementation operators on the subobject lattices in $\mathcal{E}$ and $Sh_j(\mathcal{E})$, respectively. The subtopos $Sh_j(\mathcal{E})$ is called _weakly open_ if for all subobjects $A\rightarrowtail E$ in $\mathcal{E}$, $a_j(\neg A)\cong \neg^j a_j(A)$.

## Remark

In other words, the sheafification $a_j$ commutes with pseudo-complementation.

If $i:Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ is weakly open then the topology $j$ and the inclusion $i$ are called _weakly open_ as well. 

Since the associated sheaf functor $a_j$ is just the [[inverse image]] of the inclusion $i: Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ the definition can be generalized to general [[geometric morphisms]].

## Properties

As already the name suggests, the concept of a weakly open subtopos can equally be viewed as a weakening of the concept of an [[open subtopos]]. Indeed, since the associated sheaf functor of an open inclusion is [[logical functor|logical]] we have

+-- {: .num_prop}
###### Proposition
An open subtopos $i:Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ is weakly open. $\qed$
=--

Less straightforward is the following

+-- {: .num_prop}
###### Proposition
A dense subtopos $i:Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ is weakly open.
=--

This occurs as prop.6.3 in [Caramello (2012a)](#Caramello12a). See also [Johnstone (1982)](#Johnstone82).

## Remark

The concept and terminology goes back to [Johnstone (1982)](#Johnstone). 

The equivalent concept for [[frames]] is called '_nearly open_' in [Banaschewski-Pultr (1996)](#Banaschewski_Pultr96). The maps they call 'weakly open' are called '[[skeletal geometric morphism|skeletal]]' by Johnstone.

The concept of map in point-set topology that corresponds to weakly open is that of a continuous map $f$ such that $f(U)$ is dense in some open set, for $U$ open (cf. [Pt&#225;k (1958)](#Ptak58)).

## Related entries

* [[dense subtopos]]

* [[open subtopos]]

* [[closed subtopos]]

* [[locally closed subtopos]]

* [[skeletal geometric morphism]]

* [[double negation]]

* [[De Morganization]]

## References


* {#Banaschewski_Pultr94}B. Banaschewski, A. Pultr, _Variants of openness_ , Appl. Cat. Struc. **2** (1994) pp.1-21.

* {#Banaschewski_Pultr96}B. Banaschewski, A. Pultr, _Booleanization_ , Cah. Top. G&#233;om. Diff. Cat. **XXXVII** no.1 (1996) pp.41-60. ([numdam](http://numdam.mathdoc.fr/numdam-bin/fitem?id=CTGDC_1996__37_1_41_0))

* {#Caramello12a}[[Olivia Caramello]], _Universal models and definability_ , Math. Proc. Cam. Phil. Soc. (2012) pp.279-302. ([arXiv:0906.3061](http://arxiv.org/abs/0906.3061))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([abstract](http://arxiv.org/abs/1205.2547))

* {#Johnstone82}[[Peter Johnstone]], _Factorization theorems for geometric morphisms II_ , pp.216-233 in LNM **915** Springer Heidelberg 1982.

* {#Johnstone02} [[Peter Johnstone]], _[[Sketches of an Elephant]] I_, Oxford UP 2002. (pp.209f)

* {#Ptak58}V. Pt&#225;k, _Completeness and the open mapping theorem_ , Bull. Soc. Math. France **86** (1958) pp.41-74. ([pdf](http://archive.numdam.org/article/BSMF_1958__86__41_0.pdf))

[[!redirects weakly open subtoposes]]
[[!redirects weakly open topology]]
[[!redirects weakly open topologies]]
[[!redirects implicationally open subtopos]]
[[!redirects implicationally open topology]]
