
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of **$n$-fold category** or **multiple category** is what is obtained by iterating the process of forming [[internal categories]] $n$-times, starting with sets: an $0$-fold category is just an object of the ambient category (say a [[set]]) and then inductively an $n+1$-fold category is a [[internal category]] in the category of $n$-fold categories.

If the ambient category is instead an [[(∞,1)-category]] such as [[∞Grpd]], then an $n$-fold category is an "[[n-fold Segal space]]".  If a "completeness" condition is added (analogous to "globularity" of an n-fold category), one obtaines an [[n-fold complete Segal space]], which is a model for $(\infty,n)$-categories.

## Definition

### $n$-fold categories

A **$0$-fold category** is a [[set]].  A (strict) **$n$-fold category** for $n \gt 0$ is an [[internal category]] in the category of $(n-1)$-fold categories.  An $n$-fold category is also known as an **$n$-tuple category**.

In particular:

* A $1$-fold category is precisely a [[category]].
* A $2$-fold category is precisely a [[double category]] (introduced by [[Charles Ehresmann]] in 1963).
* A $3$-fold category is precisely a [[triple category]].

## Advantages

A key advantage of $n$-fold categories is the ease of expressing multiple compositions, and so  the idea of "algebraic inverse to subdivision". This is important because subdivision is a key tool in many local-to-global problems in mathematics and science, and these themselves are an important class of problems. 

Thus subdividing an $n$-cube amounts to dividing the cube into small cubes by hyperplanes parallel to the faces. For a $2$-fold category, we can define a _composable array_ $(a_{ij})$ of $2$-dimensional elements (called squares) to be such that any $a_{ij}$ is composable with its immediate neighbours. In such case, the associative and interchange laws imply that the composition $[a_{ij}]$ is well defined. This  process is easily extended to $n$-fold categories, using  elements say $a_{(r)}$ where $(r)$ is multi-index, and  is applied  widely in the JPAA papers by Brown and Higgins listed below. It seems much more difficult to express these ideas in the globular or simplicial contexts. 



### $n$-fold groupoids

Analogously, a **$0$-fold groupoid** is again a set, and an **$n$-fold groupoid** is an [[internal groupoid]] in $(n-1)$-fold groupoids; in particular, a $1$-fold groupoid is a [[groupoid]].

Analogous to how a [[group]] is a groupoid with a single object, one can consider $(n+1)$-fold groupoids for which all morphisms in one of the $(n+1)$ directions are endomorphisms. These are the _[[cat-n-groups]]_.

More generally, an **$(n,r)$-fold groupoid** is an $r$-fold category in $(n-r)$-fold groupoids; compare $(n,r)$-[[(n,r)-category|category]].

Note also that a category  object in the category of groups is actually a groupoid object. 




## Properties
 {#Properties}

### Cartesian closure
 {#CartesianClosure}

The category of $n$-fold categories is a [[cartesian closed category]]. By [[induction]] from the statement at _[Internal category - Cartesian closure](internal+category#CartesianClosure)_.

### Homotopy types

Even though an $n$-fold category is a _strict_ version of an [[n-category]] in that all $n$ composition operations are strictly unital and associative and strictly commute with each other,  still $n$-fold _groupoids_ model all [[homotopy n-types]]. See [[homotopy hypothesis]].

### Relation to strict globular $\omega$-categories

By a theorem by Al-Agl, Brown and Steiner, [[strict omega-category|strict omega-categories]] are equivalent to those $\infty$-fold categories that satisfy a couple of restrictive properties (something like that all 1-categories of $n$-cells for all $n$ are the same and that all the "thin" identity elements exist, called "connections"): these are the "cubical $\omega$-categories with connections". Because it is relatively straightforward to define a monoidal closed category in the cubical theory, using the formula $I^m \otimes I^n = I^{m+n}$, this leads to a monoidal closed structure for strict globular $\omega$ categories. 

This is a category version of a corresponding groupoid theorem of Brown and Higgins which follows from the two papers listed below. 

[[Jean-Louis Loday]] introduced in the paper listed below the category of what he called $n$-cat groups, but are now called cat$^n$-groups as they are exactly $n$-fold groupoids internal to the category of groups. He showed that these objects model weak, pointed homotopy $n$-types,  see [[homotopy hypothesis]]. The paper by Brown and Loday shows that these structures can be used, via a van Kampen type theorem,  for explicit computations in homotopy theory, and this is further developed in the paper by Ellis and Steiner. This paper   relates the theory to that of crossed modules, $n$-ad homotopy groups, and the important $n$-ad connectivity theorem, which is related to results on homotopical excision. 

## Related concepts

* [[double groupoid]]

* [[double bicategory]]

* [[cat-n-group]]

* [[crossed n-cube]]

* [[n-fold complete Segal space]]

* [[(n × k)-category]]


## References ##

$n$-fold categories in general were introduced in Définition 15 of

* {#Ehresmann63} [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure. Vol. 80. No. 4. Elsevier, 1963 ([EUDML:81794](https://eudml.org/doc/urn:eudml:doc:81794))

as _*n*-uple categories_.

See also:

* {#BastianiEhresmann74} [[Andrée Bastiani]], [[Charles Ehresmann]], pages 272-273 of  _Multiple functors. I. Limits relative to double categories_, Cah. Top. G&#233;om. Diff&#233;r. Cat&#233;g. 15 (1974) 215&#8211;292

* [[Andrée Bastiani]], [[Charles Ehresmann]], _Multiple functors. II. The monoidal closed category of multiple categories_, Cahiers de topologie et géométrie différentielle 19.3 (1978): 295-333.

* [[Andrée Bastiani]], [[Charles Ehresmann]], _Multiple functors. III. The cartesian closed category $Cat_n$_, Cahiers de topologie et géométrie différentielle 19.4 (1978): 387-443.

* {#BastianiEhresmann79} [[Andrée Bastiani]] and [[Charles Ehresmann]]. _Multiple functors IV. Monoidal closed structures on $Cat_n$_, Cahiers de topologie et géométrie différentielle, Volume 20 (1979) no. 1, pp. 59-104. ([link](http://www.numdam.org/item/CTGDC_1979__20_1_59_0/))

A thorough theory of multiple categories appears in:

* {#Grandis19} [[Marco Grandis]], _Higher dimensional categories: from double to multiple categories_, [World Scientific]((https://doi.org/10.1142/11406)), 2019

Other references:

* [[Ronnie Brown]] and P.J. Higgins, The equivalence of $\infty$-groupoids and crossed  complexes,  Cah. Top. G\'eom. Diff.  22 (1981) 371--386.

* [[Ronnie Brown]] and P.J. Higgins. On the algebra of cubes, J. Pure
Appl.  Algebra, 21 (1981) 233-260.

* G.J. Ellis, and R.J. Steiner. Higher-dimensional crossed modules and the homotopy groups of $(n+1)$-ads, J. Pure Appl. Algebra, 46  {1987} 117--136. 

* J.-L. Loday. Spaces with finitely many nontrivial homotopy groups, J. Pure Appl. Algebra, 24 (1982) 179--202.

* [[Ronnie Brown]] and J.-L. Loday. Van Kampen theorems for diagrams of spaces. Topology 26 (1987) 311--335. With an appendix by M. Zisman.

*  [[Ronnie Brown]],  and J.-L. Loday. Homotopical excision, and Hurewicz theorems for $n$-cubes of spaces. Proc. London Math. Soc. (3) 54  (1987) 176--192.

* F.A.  Al-Agl, [[Ronnie Brown]] and R.J. Steiner, Multiple categories: the
equivalence between a globular and cubical approach, Advances in
Mathematics, 170 (2002) 71--118.

* S.  Paoli.  Internal categorical structures in homotopical algebra. In  Towards higher categories, 85&#8211;103,
IMA Vol. Math. Appl., 152, Springer, New York, 2010. 

* T.  M. Fiore and  S. Paoli.  A Thomason model structure on the category of small $n$-fold categories. Algebr. Geom. Topol. 10 (2010) 1933&#8211;-2008.

* [[Marco Grandis]], [[Robert Paré]], _An introduction to multiple categories (On weak and lax multiple categories, I) _, Cahiers de Topologie et Géométrie Différentielle Catégoriques, [(pdf)](http://cahierstgdc.com/wp-content/uploads/2017/11/CTGDC_57_2_Grandis-Pare-I.pdf)

* [[Marco Grandis]], [[Robert Paré]], _Limits in multiple categories (On weak and lax multiple categories, II)_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, [(pdf)](http://cahierstgdc.com/wp-content/uploads/2017/11/Grandis-Pare-57-3.pdf)


[[!redirects n-fold categories]]

[[!redirects n-tuple category]]
[[!redirects n-tuple categories]]

[[!redirects n-fold groupoid]]
[[!redirects n-fold groupoids]]

[[!redirects multiple category]]
[[!redirects multiple categories]]