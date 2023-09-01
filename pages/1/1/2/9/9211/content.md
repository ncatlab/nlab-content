
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

Let $k$ be a [[field]], and let $\mathcal{C}$ be a $k$-linear [[abelian category]] (i.e. one whose [[Ab-enriched category|Ab-enrichment]] is lifted to a [[Vect]]-[[enriched category|enrichment]]). Then $\mathcal{C}$ is called &lbrack;[Etingof & Ostrik 2003 p. 3](#EtingofOstrik03)&rbrack; *finite* (over $k$) if 

* For any two [[objects]] $a$, $b$ of $C$, the [[hom-object]] ($k$-[[vector space]]) $\hom(a, b)$ has [[finite]] [[dimension]]; 

* Each object $a$ is of [[object of finite length|finite length]]; 

* There are only [[finite number|finitely many]] [[simple objects]] in $C$, and each of them admits a [[projective presentation]]. 

=--

+-- {: .num_theorem #Deligne} 
###### Theorem (Deligne)

For any finite abelian category $C$, there exists a finite-dimensional $k$-algebra $A$ and an $k$-linear equivalence between $C$ and $A$-$Mod_{fd}$, the [[category of modules]] over $A$ that are finite-dimensional as vector spaces over $k$. 

=-- 

## Related concepts

* [[semisimple category]]

* [[finite-dimensional vector space]]

* [[finite-dimensional Hilbert space]]


## References

* {#EtingofOstrik03} [[Pavel Etingof]], [[Victor Ostrik]], *Finite Tensor Categories* &lbrack;[arXiv:math/0301027](https://arxiv.org/abs/math/0301027)&rbrack;

* {#EGNO15} [[nLab:Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[nLab:Victor Ostrik]], chapter 6 of _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society (2015) &lbrack;[pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;


[[!redirects finite abelian category]]
[[!redirects finite abelian categories]]
