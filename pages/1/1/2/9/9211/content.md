
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--


# Finite abelian categories
* table of contents
{: toc}

## Definition

+-- {: .num_defn #FiniteTensorCategory} 
###### Definition

Let $k$ be a [[field]], and let $\mathcal{C}$ be a $k$-linear [[abelian category]] (i.e. one whose [[Ab-enriched category|Ab-enrichment]] is lifted to a [[Vect]]-[[enriched category|enrichment]]). Then $\mathcal{C}$ is said to be *finite* (over $k$) if 

* For any two [[objects]] $a$, $b$ of $C$, the [[hom-object]] ($k$-[[vector space]]) $\hom(a, b)$ has [[finite]] [[dimension]]; 

* Each object $a$ is of [[object of finite length|finite length]]; 

* There are only [[finite number|finitely many]] [[simple objects]] in $C$, and each of them admits a [[projective presentation]]. 

=--

+-- {: .num_theorem #Deligne} 
###### Theorem (Deligne)

For any finite abelian category $C$, there exists a finite-dimensional $k$-algebra $A$ and an $k$-linear equivalence between $C$ and $A$-$Mod_{fd}$, the [[category of modules]] over $A$ that are finite-dimensional as vector spaces over $k$. 

=-- 


## Reference 

* [[Pavel Etingof]] and [[Victor Ostrik]], _Finite Tensor Categories_, Preprint 2003 ([arXiv:math/0301027](http://arxiv.org/pdf/math/0301027)) 

* {#EGNO15} [[nLab:Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[nLab:Victor Ostrik]], chapter 6 of _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))


[[!redirects finite abelian category]]
[[!redirects finite abelian categories]]
