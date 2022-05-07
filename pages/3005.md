
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
* table of contents
{:toc}


## Statement

+-- {: .num_defn #CreationOfCoequalizersOfuSplitPairs}
###### Definition


Given a [[functor]] $U : D \rightarrow C$, then a [[parallel pair]] $f,g : a \rightarrow b$ in $D$ is called **$U$-split** if the pair $U f, U g$ has a [[split coequalizer]] in $C$.  Specifically, this means that there is a diagram in $C$: 

$$U a \;\underoverset{U f}{U g}{\rightrightarrows}\; U b \;\overset{h}{\rightarrow}\; c$$
such that $h \cdot U f = h \cdot U g$, and $h$ and $U f$ have respective [[sections]] $s$ and $t$ satisfying $U g \cdot t = s \cdot h$.  This implies that the arrow $h$ is necessarily a coequalizer of $U f$ and $U g$.  

The functor $U$ is said to *create coequalizers of $U$-split pairs* if for any such $U$-split pair, there exists a coequalizer $e$ of $f,g$ in $D$ which is preserved by $U$, and moreover any [[fork]] in $D$ whose image in $C$ is a split coequalizer must itself be a coequalizer (not necessarily split).

=--


+-- {: .num_theorem}
###### Theorem
**(Beck's monadicity theorem**,  **tripleability theorem)** 

A [[functor]] $U : D \rightarrow C$ is [[monadic]] (tripleable) if and only if

1. $U$ has a [[left adjoint]], and
1. $U$ [[created limit|creates]] [[coequalizers]] of $U$-split pairs, def. \ref{CreationOfCoequalizersOfuSplitPairs}.

=--

The proof is reproduced for instance in ([Borceux, vol 2, theorem 4.4.4](#Borceux), [MacLane, p. 147-150](#MacLane)).


An equivalent, and sometimes easier, way to state these conditions is to say that

+-- {: .num_theorem}
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

The version of the monadicity theorem given in [[Categories Work]] uses a notion of "creation of limits" which fails to observe the [[principle of equivalence]], concluding that the comparison functor is an *isomorphism* of categories, rather than merely an equivalence.  But the versions mentioned above can be found in the exercises. 

Note however that if $U: D \to C$ is an [[amnestic functor|amnestic]] [[isofibration]], then $U$ is monadic iff it is strictly monadic. For an application of this observation, see for example the discussion of algebraically free monads at [[free monad]]. 

## Examples and Applications

### Groups over sets

We will use Duskin's variant to prove that the [[forgetful functor]] $U\colon$[[Grp]]$\to$[[Set]] is monadic.  Of course, this is also easy to show by explicit computation, but it serves as a useful example of how to use a monadicity theorem.  We first need it to have a left adjoint: this is easy to show by a direct construction of [[free groups]], but we could also invoke the [[adjoint functor theorem]].  It is also easy to show that it is conservative (a bijective group homomorphism is a group isomorphism), so it remains to consider congruences.

Since limits in $Grp$ are created in $Set$, a [[congruence]] in $Grp$ on a group $G$ is an [[equivalence relation]] on $G$ which is also a [[subgroup]] of $G\times G$.  This latter condition means that if $g_1\sim g_2$ and $h_1\sim h_2$, then also $g_1^{-1}\sim g_2^{-1}$ and $g_1 h_1 \sim g_2 h_2$.  Since $g\sim g$ for all $g$, it follows that $g\sim h$ if and only if $1\sim h g^{-1}$, so $\sim$ is determined by the subset $H\subseteq G$ of those $h\in G$ such that $1\sim h$.  This $H$ is clearly a subgroup of $G$, and moreover a [[normal subgroup]], since if $h\in H$ and $g\in G$ we have $1 = g^{-1} g \sim g^{-1} h g$, so $g^{-1} h g\in H$.  Conversely, it is easy to construct a congruence from any normal subgroup, so the two notions are equivalent.  It remains only to observe that the quotient of a group by a normal subgroup is, in fact, a quotient of its associated congruence in $Grp$, which is preserved by $U$.  Thus, by Duskin's monadicity theorem, $U$ is monadic.

### Categories over computads

The monadicity theorem becomes more important when the base category $C$ is more complicated and harder to work with explicitly, and when the objects of $D$ are not obviously defined as "objects of $C$ with extra structure."  For instance, the category of [[strict 2-categories]] is monadic over the category of 2-[[globular sets]], essentially by definition, but it is much less trivial to show that it is *also* monadic over the category of [[2-computads]].  This latter fact can, however, be proven using the monadicity theorem.

### Monadic descent

The monadicity theorem also plays a central role in [[monadic descent]].

## In $(\infty,1)$-categories
 {#InInfinityCategories}

There is a version of the monadicity theorem for [[(∞,1)-monad]]s in [section 3.4](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=107) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))

There is also a 2-categorical approach using quasicategories in

* [[Emily Riehl]], [[Dominic Verity]] _The 2-category theory of quasi-categories_ ([arXiv](http://arxiv.org/abs/1306.5144)), _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv](http://arxiv.org/abs/1310.8279))


## Related concepts

* [[monadic functor]], [[comonadic functor]]
* [[functor of descent type]]
* [[monadic decomposition]]

## References

Canonical textbook references include 

* {#Borceux} [[Francis Borceux]], Section 4 in volume 2 of  _[[Handbook of Categorical Algebra]]_, in 3 vols. 


* {#MacLane} [[Saunders MacLane]],  Section VI.7 of _[[Categories for the Working Mathematician]]_.

* Chapter 3 of [[Michael Barr]], [[Charles Wells]], _Triples, toposes, and theories_ , Grundlehren der math. Wissenschaften 278, Springer-Verlag 1983, [ftp](ftp://ftp.math.mcgill.ca/pub/barr/ttt), [web](http://www.cwru.edu/artsci/math/wells/pub/ttt.html), [pdf](http://www.case.edu/artsci/math/wells/pub/pdf/ttt.pdf)

Other references include:

* [[descent]], [[FGA explained]], [[SGA 1]], [[Benabou-Roubaud theorem| Bénabou-Roubaud's theorem]]

* [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_ , C. R. Acad. Sc. Paris, t. 270 (12 Janvier 1970), Serie A, 96--98

* Du&#353;ko Pavlovi&#263;, Categorical interpolation: descent and the Beck-Chevalley condition without direct images,  Category theory Como 1990, pp. 306--325, Lecture Notes in Mathematics 1488, Springer 1991

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_ , Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp. 111-195.

* wikipedia: [monadicity theorem](http://en.wikipedia.org/wiki/Beck%27s_monadicity_theorem)

* John Bourke, _Two dimensional monadicity_, [arxiv/1212.5123](http://arxiv.org/abs/1212.5123)

* [[Fred Linton]], _Some aspects of equational categories_, Proceedings of the Conference on Categorical Algebra. Springer 1966.

There is a version for [[Morita context]]s instead of monads:

* [[Tomasz Brzezinski]], Adrian Vazquez Marquez, Joost Vercruysse, _The Eilenberg-Moore category and a Beck-type theorem for a Morita context_, Appl. Categ. Structures __19__ (2011), no. 5, 821&#8211;858 [MR2836546](http://www.ams.org/mathscinet-getitem?mr=2836546) [doi](http://dx.doi.org/10.1007/s10485-009-9217-0)

Discussion for [[(infinity,1)-monads]] is in 

* [[Jacob Lurie]], section 6.2. of _[[Higher Algebra]]_

and realized in the context of [[quasi-categories]] in 

* [[Emily Riehl]], [[Dominic Verity]], section 7.2 of _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 {#RiehlVerity13}


[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck's Monadicity Theorem]]
[[!redirects Beck Monadicity Theorem]]
[[!redirects Barr-Beck theorem]]
[[!redirects monadicity theorem]]


[[!redirects Barr-Beck monadicity theorem]]


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
[[!redirects monadicity]]