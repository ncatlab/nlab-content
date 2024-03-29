
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

In great generality, for an [[integer]] $p$ a _$p$-divisible group_ is a [[inductive system|codirected diagram]] of [[abelian group|abelian]] [[group objects]] in a [[category]] $C$ where the abelian-group objects are (equivalently) the [[kernel|kernels]] of the map given by multiplication with a power of $p$; these kernels are also called $p^n$-torsions.

In the classically studied case $p$ is a prime number, $C$ is the category of [[scheme|schemes]] over a commutative ring (mostly a field with prime characteristic) and the abelian [[group scheme|group schemes]] occurring in the diagram are assumed to be finite. In this case the diagram defining the $p$-divisible group can be described in terms of the growth of the [[order of a group|order]] of the group schemes in the diagram.
 
Note that there is also a notion of [[divisible group]].

## Definition

+-- {: .num_defn}
###### Definition

Fix a [[prime number]] $p$, a [[natural number|positive integer]] $h$, and a [[commutative ring]] $R$. Consider the group schemes $G$ over 

A **$p$-divisible group of height $h$ over $R$** is a [[codirected limit|codirected diagram]] $(G_\nu, i_\nu)_{\nu \in \mathbb{N}}$ where each $G_\nu$ is a finite commutative [[group scheme]] over $R$ of [[order of a group|order]] $p^{\nu h}$ that also satisfies the property that

$$0\to G_\nu \stackrel{i_\nu}{\to} G_{\nu +1}\stackrel{p^\nu}{\to} G_{\nu +1}$$

is [[exact sequence|exact]]. In other words, the maps of the system identify $G_\nu$ with the [[kernel]] of multiplication by $p^\nu$ in $G_{\nu +1}$.

Some authors refer to $colim_\nu G_\nu$ (instead of the diagram itself) as the $p$-divisible group.
=--

It can be checked that a $p$-divisible group over $R$ is a $p$-torsion commutative [[formal group]] $G$ for which $p\colon G \to G$ is an [[isogeny]].



## Examples

+-- {: .num_example}
###### Example

The kernel of raising to the $p^\nu$ power on $\mathbb{G}_m$ (sometimes called [[p-torsion]]) is a [[group scheme]] $\mu_{p^\nu}$. The limit $\lim_{\to} \mu_{p^\nu}=\mu_{p^\infty}$ is a $p$-divisible group of height $1$.

see Lipnowski [pg.2, example (b)](http://math.stanford.edu/~malipnow/expository/pdiv.pdf)

=--

+-- {: .num_example}
###### Example

The eponymous ($p$-divisible groups are sometimes called Barsotti-Tate groups) example is a special case of the previous one - namely [[the Barsotti-Tate group of an abelian variety]]. Let $X$ be an [[abelian variety]] over $R$ of dimension $g$, then the multiplication map by $p^\nu$ has kernel $_{p^\nu}X$ which is a finite [[group scheme]] over $R$ of order $p^{2g \nu}$. The natural inclusions satisfy the conditions for the limit denoted $X(p)$ to be a $p$-divisible group of height $2g$.

=--

+-- {: .num_example}
###### Example

A theorem of [Serre and Tate](#Tate) says that there is an [[equivalence of categories]] between divisible, commutative, formal [[Lie group]]s over $R$ and the category of connected $p$-divisible groups over $R$ given by $\Gamma \mapsto \Gamma (p)$, where $\Gamma(p)=\lim_{\to} \mathrm{ker}(p^n)$. In particular, every connected $p$-divisible group is smooth {#Tate}

=--

## The Cartier dual

* Given a $p$-divisible group $G$, each individual $G_\nu$ has a [[Cartier dual]] $G_\nu^D$ since they are all group schemes. There are also maps $j_\nu$ that make the composite $G_{\nu+1}\stackrel{j_\nu}{\to} G_\nu \stackrel{i_\nu}{\to} G_{\nu +1}$ the multiplication by $p$ on $G_{\nu +1}$. After taking duals, the composite is still the multiplication by $p$ map on $G_{\nu +1}^D$, so it is easily checked that $(G_{\nu}^D, j_{\nu}^D)$ forms a $p$-divisible group called the Cartier dual.

* One of the important properties of the Cartier dual is that one can determine the height of a $p$-divisible group (often a hard task when in the abstract) using the information of the dimension of the formal group and its dual. For any $p$-divisible group, $G$, we have the formula that $ht(G)=ht(G^D)=\dim G + \dim G^D$.

## Dieudonn&#233; modules

For the moment see [[display of a p-divisible group]].

### Examples

* The dual $\mu_{p^\infty}^D\simeq \mathbb{Q}_p/\mathbb{Z}_p$.

* For an abelian variety $X$, the dual is $X(p)^D=X^t(p)$ where $X^t$ denotes the dual abelian variety. Another proof that $X(p)$ has height $2g$ is to note that $X$ and $X^t$ have the same dimension $g$, so using our formula for height we get $ht(X(p))=2g$.

## Properties

The category of &#233;tale $p$-divisible groups is equivalent to the category of $p$-adic representations of the fundamental group of the base scheme .

## p-divisible groups and crystals

(...)

References: [Weinstein](#Weinstein)

## Relation to crystalline cohomology

(...)

## In derived algebraic geometry

See [Lurie](#pLurie). An important notion: [[nonstationary p-divisible group]]


## Related concepts

* Important tools in the study of $p$-divisible groups are [[Witt ring|Witt rings]], [[Dieudonné module|Dieudonné modules]] and more generally [[Dieudonné theory|Dieudonné theories]] assigning to a $p$-divisible group an object of [[linear algebra]] such as a [[display of a p-divisible group]].


* [[formal group]]

* [[group scheme]]

* [[Artin–Mazur formal group]]

* [[height of a variety]]

## Related entries

*  [[lectures on p-divisible groups|Lectures on p-divisible groups]]

## References

For references concerning [[Witt rings]] and [[Dieudonné modules]] see there.

### Original texts and classical surveys
* Barsotti, Iacopo (1962), "Analytical methods for abelian varieties in positive characteristic", Colloq. Th&#233;orie des Groupes Alg&#233;briques (Bruxelles, 1962), Librairie Universitaire, Louvain, pp. 77&#8211;85, MR 0155827

* Demazure, Michel (1972), [[lectures on p-divisible groups|Lectures on p-divisible groups]], Lecture Notes in Mathematics, 302, Berlin, New York: Springer-Verlag, doi:10.1007/BFb0060741, ISBN 978-3-540-06092-5, MR 034426, [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

* Grothendieck, Alexander (1971), "Groupes de Barsotti-Tate et cristaux", Actes du Congr&#232;s International des Math&#233;maticiens (Nice, 1970), 1, Gauthier-Villars, pp. 431&#8211;436, MR 0578496

* Messing, William (1972), The crystals associated to Barsotti-Tate groups: with applications to abelian schemes, Lecture Notes in Mathematics, 264, Berlin, New York: Springer-Verlag, doi:10.1007/BFb0058301, MR 0347836

* Serre, Jean-Pierre (1995) [1966], "Groupes p-divisibles (d'apr&#232;s J. Tate) [web](http://www.numdam.org/item?id=SB_1966-1968__10__73_0), Exp. 318", S&#233;minaire Bourbaki, 10, Paris: Soci&#233;t&#233; Math&#233;matique de France, pp. 73&#8211;86, MR 1610452

* Stephen Shatz, Group Schemes, Formal Groups, and $p$-Divisible Groups in the book Arithmetic Geometry Ed. Gary Cornell and Joseph Silverman, 1986

* Tate, John T. (1967), "p-divisible groups." [pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.295.7566&rep=rep1&type=pdf), in Springer, Tonny A., Proc. Conf. Local Fields( Driebergen, 1966), Berlin, New York: Springer-Verlag, MR 0231827 {#Tate}




### Modern surveys

* de Jong, A. J. (1998), Barsotti-Tate groups and crystals, "Proceedings of the International Congress of Mathematicians, Vol. II (Berlin, 1998)", Documenta Mathematica II: 259&#8211;265, ISSN 1431-0635, MR 1648076

* Dolgachev, I.V. (2001), "P-divisible group" [web](http://www.encyclopediaofmath.org/index.php/P-divisible_group), in Hazewinkel, Michiel, Encyclopedia of Mathematics, Springer, ISBN 978-1-55608-010-4


* Richard Pink, finite group schemes, 2004-2005, [pdf](http://www.math.ethz.ch/~pink/ftp/FGS/CompleteNotes.pdf)

* Hoaran Wang, moduli spaces of p-divisible groups and period morphisms, Masters Thesis, 2009, [pdf](http://people.math.jussieu.fr/~dat/enseignement/M2HaoranWang.pdf)

* [[Jared Weinstein]], [[Weinstein, the geometry of Lubin-Tate spaces|the geometry of Lubi-Tate spaces]],  Lecture 1: Formal groups and formal modules, [pdf](http://www.math.ias.edu/~jaredw/FRGLecture.pdf){#Weinstein}


* Liang Xiao, notes on $p$-divisible groups, [pdf](http://math.uchicago.edu/~lxiao/files/notes/p-Divisble%20Groups.pdf)


### Further development of the theory

* Paul Goerss, p-divisible groups and Lurie's realization result, 2008, [pdf slides](http://www.math.ku.dk/~jg/homotopical2008/goerss.lec9.pdf)

* Jacob Lurie, [[A Survey of Elliptic Cohomology]], section 4.2, [pdf](http://www.math.harvard.edu/~lurie/papers/survey.pdf){#pLurie}

* Peter Scholze, Moduli of p-divisible groups, [arxiv](http://arxiv.org/abs/1211.6357)

* Thomas Zink, a dieudonn&#233; theory for p-divisible groups, [pdf](http://www.math.uni-bielefeld.de/~zink/CFTpaper.pdf)

* Thomas Zink, list of publications and preprints, [web](http://www.math.uni-bielefeld.de/~zink/z_publ.html)

* T. Zink, On the slope filtration, Duke Math. Journal, Vol.109 (2001), No.1, 79-95, [pdf](http://www.math.uni-bielefeld.de/~zink/slopes.pdf)

* T. Zink, the [[display of a p-divisible group|display of a formal p-divisible group]], to appear in [[Astérisque]], [pdf](http://www.math.uni-bielefeld.de/~zink/display.pdf)

* T. Zink, Windows for displays of p-divisible groups. in:Moduli of Abelian Varieties, Progress in Mathematics 195, Birkh&#228;user 2001, [pdf](http://www.math.uni-bielefeld.de/~zink/Texel.pdf)









[[!redirects p-divisible group]]
[[!redirects p-divisible groups]]