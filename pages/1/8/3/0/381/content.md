

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

 3. all identity $k$-morphisms are strict identies under all compositons.

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
as its objects and morphism og the underlying globular objects respecting all the above extra structure as morphisms.

## Remarks

* The last condition in the above definition says that all pairs of composition operations satisfy the [[exchange law]].

* $\omega$-Categories can also be understood as the directed limit of the sequence of iterated [[enriched category theory|enrichements]]
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

Based on this fact, there are attempts to weaken the condition on a [[simplicial set]] to be a [[complicial set]] such as to obtain a notion of [[simplicial weak ∞-category]].


## Literature

Strict $\omega$-categories have probably been independently invented by several people.  Possibly the earliest definition can be found in

* Brown and Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cah. Top. G&#233;om. Diff. 22 no. 4, [web](http://www.numdam.org/item?id=CTGDC_1981__22_4_371_0).

There they are called "$\infty$-categories" while "$\omega$-groupoid" is used to mean an $\omega$-[[n-fold category|fold groupoid]].  Another early reference is

* Ross Street, _The algebra of oriented simplices_,
J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)),

in which strict $\omega$-categories are called "$\omega$-categories."  This paper was also the first to define [[orientals]].

A review of some of the theory in the context of some of the history is given in 

* Ross Street, _An Australian conspectus of higher categories_ ([pdf](http://www.math.mq.edu.au/~street/Minneapolis.pdf))

and also in

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

The theory of $\omega$-categories was further developed by Sjoerd Crans in parts 2 and 3 of his [thesis](http://home.tiscali.nl/secrans/papers/comb.html)

* Sjord Crans, _Pasting presentations for $\omega$-categories_ ([link](http://home.tiscali.nl/secrans/papers/thpp.html))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([link](http://home.tiscali.nl/secrans/papers/thten.html))

See also the 

* [Introduction](http://home.tiscali.nl/secrans/papers/thintro.ps.gz) 

to his thesis, in particular section I.3 "$\omega$-categories".

The relationship between strict $\omega$-categories and $\omega$-fold categories was considered in

* Al-Agl, Brown, and Steiner _Multiple categories: the equivalence of a globular and a cubical approach_,  Adv. Math.  170  (2002),  no. 1, 71--118

where they prove that strict $\omega$-categories are equivalent to $\omega$-fold categories (aka "cubical $\omega$-categories") equipped with [[connections]].


[[!redirects strict ∞-category]]
[[!redirects strict ∞-categories]]
[[!redirects strict omega-categories]]