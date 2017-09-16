# Definition

A __pre-abelian category__ is an [[additive category]] (an [[Ab]]-enriched category with finite biproducts) such that every morphism has a [[kernel]] and a [[cokernel]].  Equivalently, it is an additive category with all finite [[limit]]s and colimits, since an equalizer of $f$ and $g$ in a (pre-)additive category is the same as a kernel of $f-g$, and dually.

If $C$ is pre-abelian and $c\in C$, the operations $\ker$ and $\coker$ define a [[Galois connection]] between the [[preorder]]s $Sub(c)$ of monomorphisms into $c$ and $Quot(c)$ of epimorphisms out of $c$.  In particular, $f:b\to c$ is a kernel iff $f = ker(coker(f))$ and dually.  Furthermore, every morphism $f:A\to B$ in a pre-abelian category has a canonical decomposition
$$
A\stackrel{p}\to \coker(\ker f)\stackrel{\bar{f}}\to\ker(\coker f)\stackrel{i}\to B
$$
where $p$ is a cokernel, hence [[epimorphism|epic]], and $i$ is a kernel, and hence [[monomorphism|monic]].

An __abelian category__ is a pre-abelian category satisfying the following equivalent conditions.

1. For every $f$, the canonical morphism $\bar{f}$ is an isomorphism.

1. Every monic is a kernel and every epic is a cokernel.

Assuming (1), when $f$ is monic we obtain $f\cong \ker(\coker(f))$ so that $f$ is a kernel, and dually; thus (1) implies (2).  The converse can be found in, among other places, Chapter VIII of [[Categories Work]].

In particular, in an abelian category every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into the composition of an [[epimorphism]] and a [[monomorphism]], via the above decomposition.  Since every monic is [[regular monomorphism|regular]], hence [[strong monomorphism|strong]], it follows that (epi, mono) is an [[orthogonal factorization system]].  Furthermore, again since every monic is regular, every abelian category is [[balanced category|balanced]].

+--{+ .query}
_Zoran_: Strong you mean strict monomorphism ? (like "strict epimorphism" in Kashiwara-Shapira, Adamek etc.)
Let us try to be conventional in the sense of mainstream mathematics as possible. It seems that strong and strict are half half over the literature, but I am not sure if it is completely synonymus for all.

[[Mike Shulman|Mike]]: I've never heard of a strict monomorphism.  Does it mean the same as what I mean by a strong one?  I've only ever heard this one meaning of strong.

_Zoran_: Kashiwara-Shapira page 116, is a different definition, I do not see clearly if it is equivalent; but I know that in regular categories strict epi coincides with regular epi.

http://www.uni-trier.de/fileadmin/fb4/INF/TechReports/semi-abelian_categories.pdf says at one place that Palamodov's version of semi-abelian category is preabelian + canonical morphism is epi and mono (our previous discussion). The same paper is one of many in that area which uses strict monomorphisms. Google search with quotation for the phrase "strict monomorphism" gives 190 hits, "strong monomorphism" 360 hits, similarly and a bit more for epi version with a bit different distribution in areas of usage. 

[[Mike Shulman|Mike]]: Okay, I happened to have a copy of K-S, but it would have been easier for you to just tell me the definition.  For the benefit of those listening who may not have a copy, I created [[strict epimorphism]].  Strict and regular are the same in any category with pullbacks, while regular and strong agree in any regular category but not in general.

Probably this query box can be deleted, and the comment about semi-abelian (which suggests that Gelfand-Manin is wrong?) moved to the discussion below.
=--

Finally, it is interesting to observe that the $Ab$-enrichment of an abelian category need not be specified a priori.  If an arbitrary (not necessarily pre-additive) category $C$ has a [[zero object]], binary products and coproducts, kernels, cokernels and the property that every monic is a kernel arrow and every epi is a cokernel arrow (so that all monos and epis are [[normal monomorphism|normal]]), then it can be equipped with a unique addition on the morphism sets such that composition is bilinear and $C$ is abelian with respect to this structure.  However, in most examples, the $Ab$-enrichment is evident.


# Examples

* Of course, [[Ab]] is abelian, as is the category of [[module|modules]] over any [[ring]].

* The category of [[sheaf|sheaves]] of abelian groups on any [[site]] is abelian.

* The category of torsion-free abelian groups is pre-abelian, but not abelian: the monomorphism $2:\mathbb{Z}\to\mathbb{Z}$ is not a kernel.


# Discussion

The following discussion is about whether a pre-abelian category in which (epi,mono) is a factorization system is necessarily abelian.

+--{: .query}
[[Mike Shulman|Mike]]: In [[Categories Work]], and on [Wikipedia](http://en.wikipedia.org/wiki/Abelian_category), an abelian category is defined to be (in the terms above) a pre-abelian category such that every monic is a kernel and every epi is a cokernel.  This implies that (epi, mono) is an [[orthogonal factorization system]], but I don't see why the converse should hold, as this seems to assert.

[[Zoran Skoda]] It is very late night here in Bonn, so check on my reasoning, but I think that the answer is 
simple. Let $f: A\to B$. The canonical map $\coker(\ker f)\to \ker (\coker f)$ exists as long as we have additive category admitting kernels and cokernels. The arrow from A to coker (ker f) is epi as every cokernel arrow, and the arrow of $\ker(\coker f) \to B$ is mono. Now canonical arrow in between the two is automatically both mono and epi. For all that reasoning I did not yet assume the axiom on uniquely unique factorization. Now assume it and you get
that the canonical map must be isomorphism because it is the unique iso between the two decompositions of $f$: one in which you take epi followed by (the composition of) two monics and another in which you have (the composition of) two epis followed by one monic. Right ?

Now do this for $f$ a monic and you get a decomposition into iso iso kernel and for $f$ an epi and you get 
the cokernel iso iso as required.

[[Mike Shulman|Mike]]: Why is the canonical comparison map mono and epi?  It's late for me too right now, but I think that maybe a counterexample is the "multiplication by 2" map $\mathbb{Z}\to \mathbb{Z}$ in the  category of torsion-free abelian groups.

However, if you assume explicitly that that comparison map is always an isomorphism, then I believe it for the reasons that you gave.

[[Zoran Skoda]] I do not see this as a counterexample, as this is not a pre-abelian category, you do not have cokernels in this category ? In a pre-abelian category always the canonical map from coker ker to ker coker has its own kernel 0 and cokernel 0.

[[Mike Shulman|Mike]]: Torsion-free abelian groups are reflective in abelian groups, and therefore cocomplete.  In particular, they have cokernels, although those cokernels are not computed as in [[Ab]].  In particular, the cokernel of $2:\mathbb{Z}\to\mathbb{Z}$ is 0.

[[Zoran Skoda]] Yes, I was thinking of this reflection argument (equivalence of torsion and localization argument), that is why I put question mark above. Now I tried to prove the assertion that in preabelian cat the canonical map has kernel 0 and cokernel 0 and I can't for more than an hour. But that would mean that for example Gelfand-Manin book is wrong -- it has the discussion on A4 axiom and it says exactly this. Popescu makes an example of preabelian category where canonical map is not iso, but emphasises in his example that it is bimorphism. On the other hand, later, he says that preabelian category is abelian iff it is balanced and the canonical map is bimorphism, hence he requires it explicitly. Let me think more... 

[[Zoran Skoda]] I have rewritten in minimalistic way, leaving just what I can prove, and assuming that you are right and Gelfand-Manin book has one wrong statement (that the canonical map in preabelian category is mono and epi). But let us leave the discussion here for some time, maybe we can improve the question of the difference between preabelian with factorization and abelian. 

[[Mike Shulman|Mike]]: I refactored the page to make clear what we know and what we don't, and include some examples.  Maybe someone will come along and give us a counterexample or a proof.  I wonder what the epimorphisms are in the category of torsion-free abelian groups, and in particular whether it is balanced (since if so, it would be a counterexample).
=--
