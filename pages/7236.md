
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Adhesive categories
* table of contents
{: toc}

## Idea

An *adhesive category* is a [[category]] in which [[pushouts]] of [[monomorphisms]] exist and "behave more or less as they do in the category of [[Set|sets]]", or equivalently in any [[topos]].

## Definition

+-- {: .num_defn}
###### Definition

The following conditions on a [[category]] $C$ are equivalent.  When they are satisfied, we say that $C$ is **adhesive**.

1. $C$ has [[pullbacks]] and [[pushouts]] of [[monomorphisms]], and pushout squares of monomorphisms are also pullback squares and are stable under pullback.

1. $C$ has pullbacks, and pushouts of monomorphisms, and the latter are also [[2-colimit|(bicategorical)]] pushouts in the [[bicategory]] of [[spans]] in $C$.

1. (If $C$ is small) $C$ has pullbacks and pushouts of monomorphisms, and admits a [[fully faithful functor|full embedding]] into a [[Grothendieck topos]] preserving pullbacks and pushouts of monomorphisms.

1. $C$ has pullbacks and pushouts of monomorphisms, and in any cubical diagram:

   ![cube](http://quicklatex.com/cache3/ql_af6fe9cbb3a7ee55b65eda25feb2062b_l3.png)

   if $X\to Y$ is a monomorphism, the bottom square is a pushout, and the left and back faces are pullbacks, then the top face is a pushout if and only if the front and right face are pullbacks.  In other words, pushouts of monomorphisms are [[van Kampen colimits]].

=--

## Properties

+-- {: .num_prop}
###### Proposition
In an adhesive category, suppose given a [[pushout]] square
$$ \array{ C & \xrightarrow{m} & A \\ ^f\downarrow && \downarrow^g \\ B & \xrightarrow{n} & D } $$
such that $m$ is a monomorphism.  Then:

1. $n$ is also a monomorphism.
2. The square is also a [[pullback]] square.
3. The square is also a [[distributivity pullback]] around $(g,m)$; hence in particular $n = \forall_g m$ is the [[universal quantification]].
=--

(Notice that generally [[monomorphisms]] (as discussed there) are preserved by [[pullback]].)  For a proof of the above proposition, see ([Lack, prop. 2.1](#Lack)) and ([Lack-Sobocinski, Lemmas 2.3 and 2.8](#LS1)).  The latter Lemma 2.8 states only that $n = \forall_g m$ (a weaker universal property since it refers only to other *monomorphisms* into $D$), but the proof applies more generally.

+-- {: .num_prop}
###### Proposition
An adhesive category with a [[strict initial object]] is automatically an [[extensive category]].
=--

We define a [[pushout complement]] of $m:C\to A$ and $g:A\to D$ to be a pair of arrows $f:C\to B$ and $n:B\to D$ such that $n f = g m$ and this [[commutative square]] is a [[pushout]].  The following proposition is crucial in [[double pushout graph rewriting]].

+-- {: .num_prop}
###### Proposition
In an adhesive category, if $m:C\to A$ is mono and $g:A\to D$ is any morphism, then if a pushout complement exists, it is unique up to unique isomorphism.
=--
+-- {: .proof}
###### Proof
We give only a sketch; details are in [(LS, Lemma 4.5)](#LS).  If $(f,n)$ and $(f',n')$ are two pushout complements, consider the two pushout squares as morphisms in the [[arrow category]] with target $g$, and take their pullback.  The resulting commutative cube can be viewed as a morphism in the category of commutative squares from the pullback square of $m$ against itself (which is again $m$, since $m$ is mono) to the pullback square of $n$ against $n'$.  Denote the vertex of the latter pullback square by $U$.  Applying the van Kampen property in two directions, we find that the maps $U\to B$ and $U\to B'$ are both pushouts of $1_C$, hence isomorphisms.  This gives an isomorphism between the pushout complements; it is unique since $n$ and $n'$ are mono (being pushouts of the mono $m$).
=--



## Examples
 {#Examples}

* Any [[topos]] is adhesive ([Lack-Sobocisnki](#LSToposes)).  For [[Grothendieck toposes]] this is easy, because $Set$ is adhesive and adhesivity is a condition on colimits and finite limits, hence preserved by functor categories and left-exact localizations.  For [[elementary toposes]] it is a theorem of [Lack and Sobocinski](#LSToposes).

* The fact that monomorphisms are stable under pushouts in toposes plays a central role for [[Cisinski model structures]] such as notably the standard [[model structure on simplicial sets]], where the monomorphisms are [[cofibrations]] and as such required to be closed under pushout (in particular).


## Related concepts

Adhesiveness is an [[exactness property]], similar to being a [[regular category]], an [[exact category]], or an [[extensive category]].  In particular, it can be phrased in the language of "lex colimits".

## References

* {#LS1} [[Steve Lack]] and [[Pawel Sobocinski]], *Adhesive and quasiadhesive categories*, RAIRO - Theoretical Informatics and Applications - Informatique Théorique et Applications, Tome 39 (2005) no. 3, pp. 511-545, [Numdam](http://www.numdam.org/item/ITA_2005__39_3_511_0/),
[author PDF](https://www.ioc.ee/~pawel/papers/adhesivejournal.pdf)


* {#LS} [[Steve Lack]] and [[Pawel Sobocinski]], *Adhesive categories*, 
In: Walukiewicz I. (eds) Foundations of Software Science and Computation Structures. FoSSaCS 2004. Lecture Notes in Computer Science, vol 2987. Springer, Berlin, Heidelberg. doi:[10.1007/978-3-540-24727-2_20](https://doi.org/10.1007/978-3-540-24727-2_20),
[author PDF](https://www.ioc.ee/~pawel/papers/adhesive.pdf)


* {#LSToposes} [[Steve Lack]] and [[Pawel Sobocinski]], *Toposes are adhesive*, In: Corradini A., Ehrig H., Montanari U., Ribeiro L., Rozenberg G. (eds) Graph Transformations. ICGT 2006. Lecture Notes in Computer Science, vol 4178. Springer, Berlin, Heidelberg. doi:[10.1007/11841883_14](https://doi.org/10.1007/11841883_14),
[author PDF](http://users.ecs.soton.ac.uk/ps/papers/toposesAdhesive.pdf)


* {#Lack} [[Steve Lack]], *An embedding theorem for adhesive categories*, Theory and Applications of Categories, Vol. 25, 2011, No. 7, pp 180-188. [journal page](http://www.tac.mta.ca/tac/volumes/25/7/25-07abs.html), arXiv:[1103.0600](https://arxiv.org/abs/1103.0600)


* {#GarnerLack} [[Richard Garner]] and [[Steve Lack]], *On the axioms for adhesive and quasiadhesive categories*, Theory and Applications of Categories, Vol. 27, 2012, No. 3, pp 27-46. ([arXiv:1108.2934](http://arxiv.org/abs/1108.2934), [journal page](http://www.tac.mta.ca/tac/volumes/27/3/27-03abs.html))


[[!redirects adhesive categories]]
