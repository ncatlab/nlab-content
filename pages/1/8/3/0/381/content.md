#Idea#

A _strict $\omega$-category_ is a [[globular set|globular]] [[infinity-category|infinity-categories]] in which all operations obey their respective laws strictly.



This means that 

 1. all composition operations are strictly associative;

 2. all composition operations strictly commute with all others (strict [[exchange law]]s);

 3. all identity $k$-morphisms are strict identies under all compositons.

#Definition#

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

##Remarks##

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

* Terminology on $\omega$-categories varies. We here follow section 2.2 of Sjoerd Crans: [Pasting presentations for $\omega$-categories](http://crans.fol.nl/papers/thpp.html), where it says 

  * _Street allowed $\omega$-categories to have infinite dimensional cells. Steiner has the extra condition that every cell has to be finite dimensional, and called them $\infty$-categories, following Brown and Higgins. I will use Steiner's approach here since that's the one that reflects the notion of higher dimensional homotopies closest, but I will nonethless call them $\omega$-categoires, and I agree with Verity's suggestion to call the other ones $\omega^+$-categories._



* [[Simpson's conjecture]], a statement about [[semi-strict infinity-category|semi-strictness]], states that every weak $\infty$-category should be equivalent to an $\infty$-category in which strictness conditions 1. and 2. hold, but not 3.


#Literature#

Strict $\omega$-categories were introduced (just called "$\omega$-categories" then), together with [[oriental]]s, in 

* Ross Street, _The algebra of oriented simplices_,
J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).


A review of some of the theory in the context of some of the history is given in 

* Ross Street, _An Australian conspectus of higher categories_ ([pdf](http://www.math.mq.edu.au/~street/Minneapolis.pdf))

and also in

* Ross Street, _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

The theory of $\omega$-categories was further developed by Sjoerd Crans in parts 2 and 3 of his [thesis](http://crans.fol.nl/papers/comb.html)

* Sjord Crans, _Pasting presentations for $\omega$-categories_ ([link](http://crans.fol.nl/papers/thpp.html))

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([link](http://crans.fol.nl/papers/thten.html))

See also the 

* [Introduction](http://crans.fol.nl/papers/thintro.ps.gz) 

to his thesis, in particular section I.3 "$\omega$-categories".


