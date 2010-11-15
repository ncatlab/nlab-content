
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Statement


+-- {: .un_theorem}
###### Theorem
**(Beck's monadicity theorem**,  **tripleability theorem)** 

A [[functor]] $U : D \rightarrow C$ is [[monadic]] (tripleable) if and only if

1. $U$ has a [[left adjoint]], and
1. $U$ [[created limit|creates]] [[coequalizers]] of $U$-split pairs.

=--

A proof is reproduced at ([Borceux, vol 2, theorem 4.4.4](#Borceux)).

Here a [[parallel pair]] $f,g : a \rightarrow b$ in $D$ is **$U$-split** if the pair $U f, U g$ has a [[split coequalizer]] in $C$.  Specifically, this means that there is a diagram in $C$: 

$$U a \;\underoverset{U f}{U g}{\rightrightarrows}\; U b \;\overset{h}{\rightarrow}\; c$$

where $h$ has a [[section]] $s$ and $U f$ has a section $t$ such that $U g \cdot t = s \cdot h$.  This implies that the arrow $h$ is necessarily a coequalizer of $U f$ and $U g$.  To say that $U$ *creates coequalizers of $U$-split pairs* is to say that for any such $U$-split pair, there exists a coequalizer $e$ of $f,g$ in $D$ which is preserved by $U$, and moreover any fork in $D$ whose image in $C$ is a split coequalizer must itself be a coequalizer (not necessarily split).

An equivalent, and sometimes easier, way to state these conditions is to say that

+-- {: .un_theorem}
###### Theorem

A functor $U : D \to C$ is monadic precisely if

1. $U$ has a [[left adjoint]],
1. $U$ reflects [[isomorphisms]] (i.e. it is [[conservative functor|conservative]]), and
1. $D$ has, and $U$ [[preserved limit|preserves]], coequalizers of $U$-split pairs.

=--


This is equivalent because a conservative functor [[reflected limit|reflects]] any limits or colimits which exist in its domain and which it [[preserved limit|preserves]], while monadic functors are always conservative.

## Variations

### The crude monadicity theorem

The __crude monadicity theorem__ gives a *sufficient*, but not necessary, condition for a functor to be monadic.  It states that a functor $U : D \rightarrow C$ is [[monadic]] if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $D$ has and $U$ preserves coequalizers of [[reflexive coequalizer|reflexive pairs]].

(Recall that a parallel pair $f,g : a \rightarrow b$ is __reflexive__ if $f$ and $g$ have a common [[section]].)  This sufficient, but not necessary, condition is sometimes easier to verify in practice.  In contrast to the crude monadicity theorem, the necessary and sufficient condition above is sometimes called the __precise monadicity theorem__.

### Duskin's monadicity theorem

Duskin's monadicity theorem gives a different sufficient, but not necessary, condition which refers only to quotients of [[congruences]].  It says that a functor $U \colon D \to C$ is monadic if

1. $U$ has a left adjoint
1. $D$ and $C$ are [[finitely complete category|finitely complete]]
1. $U$ [[created limit|creates]] coequalizers for [[congruences]] in $D$ whose images in $C$ have split coequalizers.

We can weaken the hypothesis a bit further to obtain the theorem:

* A right adjoint between finitely complete categories is monadic if it creates [[quotients]] for [[congruences]].

As usual, we can also modify it by replacing reflection of limits by reflection of isomorphisms.

* A conservative right adjoint $U\colon D \to C$ between finitely complete categories is monadic if any congruence in $D$ which has a quotient in $C$ already has a quotient in $D$, and that quotient that is preserved by $U$.

If we view the objects of $D$ as underlying $C$-objects with structure, this says that any congruence in $D$ induces a $D$-structure on its quotient in $C$.  As with the crude monadicity theorem, this condition is sometimes easier to verify since quotients of congruences are often better-behaved than arbitrary coequalizers.  This is the case in many "algebraic" situations.

Duskin actually gave a slightly more precise version only assuming the categories $C$ and $D$ to have particular finite limits, rather than all of them.

### Monadicity over Set

In the case when the base category $C$ is [[Set]], one can further refine the requisite conditions.  Linton proved that a functor $U\colon D\to Set$ is monadic if and only if

1. $U$ has a left adjoint,
1. $D$ admits [[kernel pairs]] and [[coequalizers]],
1. A [[parallel pair]] $R \rightrightarrows S$ in $D$ is a kernel pair if and only if its image under $U$ is so, and
1. A morphism $A\to B$ in $D$ is a [[regular epimorphism]] if and only if its image under $U$ is so.

There are other versions of this theorem, including generalizations to monadicity over [[presheaf categories]], which can be viewed as analogues of [[Giraud's theorem]].

### Strict monadicity

The version of the monadicity theorem given in [[Categories Work]] uses an [[evil]] notion of "creation of limits" and concludes that the comparison functor is an *isomorphism* of categories, rather than merely an equivalence.  But the versions mentioned above can be found in the excercises.


## In $(\infty,1)$-categories

There is a version of the monadicity theorem for [[(∞,1)-monad]]s in [section 3.4](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=107) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))


## Applications

The monadicity theorem plays a central role in [[monadic descent]].

## References

A canonical textbook reference is section 4 in volume 2 of

* [[Francis Borceux]], _Handbook of categorical algebra_ , in 3 vols. 
{#Borceux}

* [[Michael Barr]], [[Charles Wells]], _Triples, toposes, and theories_ , Grundlehren der math. Wissenschaften 278, Springer-Verlag 1983, [ftp](ftp://ftp.math.mcgill.ca/pub/barr/ttt), [web](http://www.cwru.edu/artsci/math/wells/pub/ttt.html), [pdf](http://www.case.edu/artsci/math/wells/pub/pdf/ttt.pdf)

* [[descent]], [[FGA explained]], [[SGA 1]], [[Benabou-Roubaud theorem| Bénabou-Roubaud's theorem]]

* [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_ , C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98

* Du&#353;ko Pavlovi&#263;, Categorical interpolation: descent and the Beck-Chevalley condition without direct images,  Category theory Como 1990, pp. 306--325, Lecture Notes in Mathematics 1488, Springer 1991

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_ , Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp. 111-195.


* wikipedia: [monadicity theorem](http://en.wikipedia.org/wiki/Beck%27s_monadicity_theorem)


[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck Monadicity Theorem]]
[[!redirects Barr-Beck theorem]]
[[!redirects monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck monadicity theorem]]
[[!redirects tripleability theorem]]
[[!redirects Beck's tripleability theorem]]
[[!redirects Beck's tripleability theorem]]
[[!redirects Beck tripleability theorem]]
[[!redirects Beck's theorem]]
[[!redirects Beck's theorem]]
[[!redirects Beck theorem]]
[[!redirects crude monadicity theorem]]
[[!redirects crude tripleability theorem]]
