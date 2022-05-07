
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


The **Monster group** $M$ is a [[finite group]] that is the largest of the [[sporadic finite simple group]]s. It has [[order of a group|order]]

$$
 \begin{aligned}
& 2^{46}\cdot 3^{20}\cdot 5^9\cdot 7^6\cdot 11^2\cdot 13^3\cdot 17\cdot 19\cdot 23\cdot 29\cdot 31\cdot 41\cdot 47\cdot 59\cdot 71 
  \\
 & = 808017424794512875886459904961710757005754368000000000
 \end{aligned}
$$

and contains all but six (the '[[pariah groups]]') of the other 25 [[sporadic finite simple groups]] as [[subquotients]], called the _[[Happy Family]]_.

See also [[Moonshine]].


## History


The Monster group was predicted to exist by [[Bernd Fischer]] and [[Robert Griess]] in 1973, as a [[simple group]] containing the [[Fischer groups]] and some other sporadic simple groups as [[subquotients]]. Subsequent work by Fischer, Conway, Norton and Thompson estimated the order of $M$ and discovered other properties and subgroups, assuming that it existed. In a famous paper 

* [[Robert Griess]], _The Friendly Giant_ , Inventiones (1982)

Griess proved the existence of the largest simple sporadic group. The author constructs "by hand" a non-associative but commutative algebra of dimension 196883, and showed that the [[automorphism group]] of this algebra is the conjectured friendly giant/monster simple group. The name "Friendly Giant" for the Monster did not take on.

After Griess found this algebra [[Igor Frenkel]], [[James Lepowsky]] and Meurman and/or Borcherds showed that the Griess algebra is just the degree 2 part of the infinite dimensional [[Moonshine vertex algebra]].


There is a school of thought, going back to at least [[Israel Gelfand]], that sporadic groups are really members of some other infinite families of algebraic objects, but due to numerical coincidences or the like, just happen to be groups (see [this nCafe post](http://golem.ph.utexas.edu/category/2006/09/mathematical_kinds.html)). One version of this, in the case of the Monster (and perhaps for other sporadic groups via [[Moonshine]] phenomena) is that what we know as the Monster is just a shadow of a [[2-group]], as the Monster can be constructed as an automorphism group of a [[conformal field theory]], a structure rich enough to have a automorphism 2-group(oid) (see [this nCafe discussion](http://golem.ph.utexas.edu/category/2008/10/john_mckay_visits_kent.html#c019440)).

## Presentation 

### Via Coxeter groups

The Monster admits a reasonably succinct description in terms of [[Coxeter groups]]. Let $[n]$ denote the linear [[graph]] with vertices $0, 1, \ldots, n$ with an edge between adjacent numbers $i, i+1$ and no others. If $1$ is the terminal (1-element) graph, there is a map $0: 1 \to [n]$, mapping the vertex of $1$ to the vertex $0$. Regarding this as an object in the [[undercategory]] $1 \downarrow Graph$, let $Y_{443}$ be the [[coproduct]] of the three objects $0: 1 \to [4]$, $0: 1 \to [4]$, $0: 1 \to [3]$ in $1 \downarrow Graph$. This (pointed) graph has 12 elements and is shaped like a $Y$, with arms of length 4, 4, 3 emanating from a central vertex of valence $3$. 

Regard $Y_{443}$ as a [[Coxeter diagram]]. The associated [[Coxeter group]] $C_{443}$ is given by a [[group presentation]] with 12 generators (represented by the vertices) of order $2$ (so 12 relators of the form $x^2 = 1$), with a relation $(x y)^3 = 1$ if $x, y$ are adjacent vertices (so 11 relators, one for each edge), and $x y = y x$ if $x, y$ are non-adjacent (55 more relators). This Coxeter group (12 generators, 78 relators) is infinite, but by modding out by another strange 'spider' relator 

$$(a b_1 c_1 a b_2 c_2 a b_3 c_3)^{10} = 1$$ 

the resulting quotient $N$ turns out to be a [[finite group]]. Here $a$ is the central vertex of valence $3$, $b_1, c_1$ are on an arm of length $4$ with $b_1$ adjacent to $a$ and $c_1 \neq a$ adjacent to $b_1$; similarly for $b_2, c_2$ on the other arm of length $4$, and for $b_3, c_3$ on the arm of length $3$. See [here](http://www.maths.qmul.ac.uk/~jnb/web/Pres/Mnst.html) if this is not clear. 

It turns out that $N$ has a [[center]] $C$ of order $2$, and the Monster $M$ is the quotient, i.e. the indicated term in the exact sequence  

$$1 \to C \to N \to M \to 1.$$ 

This implicitly describes the Monster in terms of 12 generators and 80 relators. 

Such "$Y$-group" presentations (Coxeter group based on a similar $Y$-diagram, modulo a spider relation) are linked to a number of finite simple group constructions, the most famous of which is perhaps $Y_{555}$ which is a presentation of the "Bimonster" (the [[wreath product]] of the Monster with $\mathbb{Z}/2$). See [Ivanov](#Iv) for a general description of these. The presentation of the Monster given above was established in [Ivanov2](#Iv2). 

### Via automorphisms of a super vertex operator algebra
 {#ViaAutomorphisms}

There is a [[super vertex operator algebra]], the [[Monster vertex operator algebra]], whose [[automorphism group|group of]] of [[automorphisms of a VOA]] is the [[monster group]].

  ([Frenkel-Lepowski-Meurman 89](#FrenkelLepowskiMeurman89), [Griess-Lam 11](#GriessLam11))


## Related concepts

* [[Moonshine]],

* [[Monster vertex algebra]]

* [[Mathieu group]], [[Mathieu moonshine]]


## References 

* [Adam P. Goucher](http://mathoverflow.net/users/39521/adam-p-goucher), _Presentation of the Monster Group_, ([MO comment 2013-09-15](http://mathoverflow.net/q/142216))  

* {#Iv} Alexander Ivanov, _Y-groups via transitive extension_, Journal of Algebra, Volume 218, Issue 2 (August 15, 1999), 412&#8211;435. ([web](http://www.sciencedirect.com/science/article/pii/S0021869399978821)) 
  

*  {#Iv2} A. A. Ivanov, _Constructing the Monster via its Y-presentation_,
in Combinatorics, Paul Erd&#337;s is Eighty, Bolyai Society Mathematical Studies, Vol. 1 (1993), 253-270. 

* {#FrenkelLepowskiMeurman89} [[Igor Frenkel]], [[James Lepowsky]], Arne Meurman, _Vertex operator algebras and the monster_, Pure and Applied Mathematics __134__, Academic Press, New York 1998. liv+508 pp. [MR0996026](http://www.ams.org/mathscinet-getitem?mr=996026)

* {#GriessLam11} [[Robert Griess]] Jr., Ching Hung Lam, _A new existence proof of the Monster by VOA theory_ ([arXiv:1103.1414](https://arxiv.org/abs/1103.1414))
  
* [[Andre Henriques]], _[$H^4$ of the monster](http://mathoverflow.net/questions/69222/h4-of-the-monster)_


Possible relation to [[bosonic M-theory]]:

* [[Alessio Marrani]], [[Michael Rios]], [[David Chester]], _Monstrous M-theory_ ([arXiv:2008.06742](https://arxiv.org/abs/2008.06742))


<div style="float:right;margin:0 20px 10px 20px;"><img width = "80" src="http://t0.gstatic.com/images?q=tbn:nJNML0QhNiejuM:http://open.salon.com/files/cookie-monster3-7769871237963363.jpg
" alt="The Monster" /></div>



[[!redirects Monster]]

[[!redirects monster group]]

[[!redirects Monster simple group]]