

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _strict $\omega$-category_ is a [[globular set|globular]] [[∞-category]] in which all operations obey their respective laws strictly.

This was the original notion of [[∞-category]], and the original meaning of the term [[∞-category]]. Even today, most authors who use that term still mean this notion.

This means that 

 1. all composition operations are strictly associative;

 2. all composition operations strictly commute with all others (strict [[exchange laws]]);

 3. all identity $k$-morphisms are strict identities under all compositions.

## Definition

An **$\omega$-category** $C$ [[internalization|internal to]]  $Sets$ is 

* a [[globular set]] 
$$
  C :=
  (\cdots
  C_3 \stackrel{\to}{\to}
  C_2 \stackrel{\to}{\to}
  C_1 \stackrel{\to}{\to}
  C_0
 )
$$

* together with the structure of a [[category]] on 
all
$(  C_{k} \stackrel{\to}{\to} C_l )$ for all $k \gt l$;

* such that 
$(  C_{k} \stackrel{\to}{\to}
  C_{l} \stackrel{\to}{\to} C_m )$ for all $k \gt l \gt m$;
is a [[strict 2-category]].

Similarly for an $\omega$-category [[internalization|internal to]]  another ambient category $A$.

The category $\omega Cat(A)$ of $\omega$-categories [[internalization|internal to]] $A$ has $\omega$-categories
as its objects and morphism of the underlying globular objects respecting all the above extra structure as morphisms.

## Remarks

* The last condition in the above definition says that all pairs of composition operations satisfy the [[exchange law]].

* $\omega$-Categories can also be understood as the directed limit of the sequence of iterated [[enriched category theory|enrichments]]
$$
  (0 Cat = Set)
  \hookrightarrow
  (1 Cat = Set-Cat)
  \hookrightarrow
  (2 Cat = Cat-Cat)
  \hookrightarrow
  \left(3 Cat = (2Cat)-Cat = (Cat-Cat)-Cat\right)
  \hookrightarrow
  \cdots
  \,.
$$

* The category of strict $\omega$-categories admits a [[closed monoidal category|biclosed monoidal structure]] called the [[Crans-Gray tensor product]].

* The category of strict $\omega$-categories also admits a [[canonical model structure]].

* Terminology on $\omega$-categories varies. We here follow section 2.2 of [[Sjoerd Crans]]: [Pasting presentations for $\omega$-categories](http://home.tiscali.nl/secrans/papers/thpp.html), where it says 

  * _[[Ross Street|Street]] allowed $\omega$-categories to have infinite dimensional cells. Steiner has the extra condition that every cell has to be finite dimensional, and called them $\infty$-categories, following [[Ronnie Brown|Brown]] and Higgins. I will use Steiner's approach here since that's the one that reflects the notion of higher dimensional homotopies closest, but I will nonethless call them $\omega$-categories, and I agree with [[Dominic Verity|Verity]]'s suggestion to call the other ones $\omega^+$-categories._



* [[Simpson's conjecture]], a statement about [[semi-strict infinity-category|semi-strictness]], states that every weak $\infty$-category should be equivalent to an $\infty$-category in which strictness conditions 1. and 2. hold, but not 3.


## As simplicial sets 

Under the [[oriental|∞-nerve]] 

$$
  N : Str \omega Cat \to SSet
$$

strict $\omega$-categories yield simplicial sets that are called [[complicial sets]]. 

+-- {: .un_prop}
###### Proposition

The categories of $\omega$-categories and complicial sets are [[equivalence of categories|equivalent]].
=--

This is sometimes called the _Street-Roberts conjecture_. It was completely proven in

* Dominic Verity, _Complicial sets_ ([arXiv](http://arxiv.org/abs/math/0410412))

which also presents the history of the conjecture.

Based on this fact, there are attempts to weaken the condition on a [[simplicial set]] to be a [[complicial set]] so as to obtain a notion of [[simplicial weak ∞-category]].


## Related concepts

* [[strict ∞-groupoid]]

* [[parity complex]], [[oriental]]

* [[complicial set]]

## References

Strict $\omega$-categories have probably been independently invented by several people.  

According to [Street 09, p. 10](#Street09) the concept was first brought up by [[John Roberts]] 1977-1978, in an attempt to define [[non-abelian cohomology]] (of [[local nets of observables]] in [[algebraic quantum field theory]]).

Possibly the earliest published definition is due to

* [[Ronnie Brown]] and P.J. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cah. Top. G&#233;om. Diff. 22 (1981) no. 4, 371-386 [web](http://www.numdam.org/item?id=CTGDC_1981__22_4_371_0).

which also contains the definitions of [[n-fold category]] and of what was later called [[globular set]]. There these strict, globular higher categories are called "$\infty$-categories" while "$\omega$-groupoid" is used  to mean a cubical set with connections and compositions, each a groupoid, as in 

* R. Brown and P.J. Higgins,  _On the algebra of cubes_,  J. Pure
Appl.  Algebra 21 (1981) 233-260.

Applications to homotopy theory were given in

* R. Brown and P.J. Higgins,  _Colimit theorems for relative homotopy
groups_, J. Pure Appl. Algebra 22 (1981) 11-41.

* R. Brown, _Non-abelian cohomology and the homotopy classification of maps_,  in Homotopie alg&#233;brique et algebre locale, Conf. Marseille-Luminy 1982,  ed. J.-M. Lemaire et J.-C. Thomas,
Ast&#233;risques 113-114 (1984), 167-172.

Related monoidal closed structures were developed in: 

* R. Brown and P.J. Higgins, _Tensor products and homotopies for
$\omega$-groupoids and crossed complexes_,  J. Pure Appl.
Alg. 47 (1987) 1-33.

Another 1980s reference is

* [[Ross Street]], _The algebra of oriented simplices_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf), <a href="https://doi.org/10.1016/0022-4049(87)90137-X">doi:10.1016/0022-4049(87)90137-X</a>),

in which strict $\omega$-categories are called "$\omega$-categories."  This paper was also the first to define [[orientals]].

A review of some of the theory in the context of some of the history is given in 

* {#Street09} [[Ross Street]], _An Australian conspectus of higher categories_, chapter in _Towards Higher Categories_ Volume 152 of the series The IMA Volumes in Mathematics and its Applications pp 237-264 ([pdf](http://www.math.uchicago.edu/~may/IMA/Street.pdf))

and also in

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

The theory of $\omega$-categories was further developed by Sjoerd Crans in parts 2 and 3 of his [thesis](http://home.tiscali.nl/secrans/papers/comb.html)

* [[Sjoerd Crans]], _Pasting presentations for $\omega$-categories_ ([link](http://home.tiscali.nl/secrans/papers/thpp.html))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([link](http://home.tiscali.nl/secrans/papers/thten.html))

See also the 

* [Introduction](http://home.tiscali.nl/secrans/papers/thintro.ps.gz) 

to his thesis, in particular section I.3 "$\omega$-categories".

The relationship between strict $\omega$-categories and cubical $\omega$-categories was considered in

* F.A. Al-Agl, R. Brown, R. Steiner _Multiple categories: the equivalence of a globular and a cubical approach_,  Adv. Math.  170  (2002),  no. 1, 71--118

where they prove that strict globular $\omega$-categories are equivalent to $\omega$-fold categories (aka "cubical $\omega$-categories") equipped with [[connections]]. This paper also develops the monoidal closed structures. 

* R. Steiner, _Omega-categories and chain complexes_, Homology, Homotopy and Applications __6__(1), 2004, pp.175&#8211;200, [pdf](http://www.intlpress.com/HHA/v6/n1/a12/v6n1a12.pdf)
[[!redirects strict ∞-category]]
[[!redirects strict ∞-categories]]
[[!redirects strict omega-categories]]