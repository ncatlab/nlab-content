

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents 
{: toc}

## Introduction 

Both [[category theory]] and [[graph theory]] study patterns based on [[diagrams]] consisting of nodes and edges. Despite this surface impression, there is in fact very little interaction between the scientific communities of category theorists and of graph theorists. 

This article is a modest bridge, indicating that the _[[category]] of [[graphs]]_ (in the usual graph-theorist's sense -- see for example [Diestel](#Diestel)) has some very nice properties. 


## Simple graphs as relations 

By a **simple [[graph]]**, we mean a [[set]] $V$ whose elements are called *vertices*, together with a collection of 2-element subsets $\{x, y\}$ of $V$; these are called *edges* of the graph. 

There are various ways of forming a category of simple graphs. Perhaps the most straightforward is to define a morphism of graphs $G \to H$ to be a function $f: V \to W$ between the vertex sets to be a graph morphism if $\{f(x), f(y)\}$ is an edge of $H$ whenever $\{x, y\}$ is an edge of $G$. 

Another option -- and this is the one chosen for this article -- starts by regarding a simple graph as carrying the same information as a set $V$ equipped with a [[symmetric relation|symmetric]] [[reflexive relation|reflexive]] [[relation]] $E$. Indeed, such a relation determines (and is uniquely determined by) a simple graph $G$ where for given vertices $x, y \in V$, there is an edge $\{x, y\}$ between $x$ and $y$ in $G$ iff both $(x, y) \in E$ and $x \neq y$. We will write $E(x, y)$ to mean $(x, y) \in E$. 

Then, under the relational formulation, we define a morphism $(V, E) \to (W, F)$ between simple graphs straightforwardly[^1] as a function $f: V \to W$ that preserves the relevant structure, i.e., that $E(x, y)$ implies $F(f(x), f(y))$. One reason for preferring this notion of morphism is that it allows, for example, consideration of arbitrary edge contractions of a simple graph as [[quotients]] in the category (cf. [[graph minor]]), something that is not possible under the prior notion of morphism. 

[^1]: In other words, the usual notion of morphism between structures or models as in [[model theory]]. 

Thus we will adopt the latter notion of morphism which takes reflexive symmetric relations $E$ as primary. The resulting [[category]] of simple graphs is denoted by $SimpGph$. 

Note that graphs and their morphisms can also be understood in functorial language, by regarding simple graphs as special types of [[presheaves]], as follows. Let $C$ be the category of sets $1 \coloneqq \{\ast\}$ and $2 \coloneqq \{s, t\}$ and functions between them. Then a presheaf $X: C^{op} \to Set$ is given by sets $V = X(1)$ and $E = X(2)$ and maps 

* $d_0: X(2) \stackrel{X(\ast \mapsto s)}{\to} X(1)$ (source map), 

* $d_1: X(2) \stackrel{X(\ast \mapsto t)}{\to} X(1)$ (target map), 

* $i: X(1) \stackrel{X(s, t \mapsto \ast)}{\to} X(2)$ (reflexive map), 

* $\sigma: X(2) \stackrel{X(s \mapsto t, t \mapsto s)}{\to} X(2)$ (symmetry map). 

satisfying appropriate identities imposed by equations in $C$. Simple graphs can then be regarded [[equivalence|equivalently]] as such presheaves where the map 

$$\langle d_0, d_1 \rangle: X(2) \to X(1) \times X(1)$$ 

is a [[monomorphism]]. In that case, a morphism of simple graphs amounts to a [[natural transformation]] between such presheaves. 

### An aside on other notions of graph 

"Simple graph" as defined in the nLab (see [[graph]]) means that edges are 2-element subsets of $V$, but of course that doesn't preclude consideration of other types of graph. One option is to consider sets $V$ equipped with a collection of subsets of $V$ of cardinality either 1 or 2, i.e., allowing some but not necessarily all loops as edges. We don't call those "simple graphs" (at [[graph]] they are called "loop graphs"), but nevertheless they form a respectable category under the straightforward notion of morphism $f$ (if $\{x, y\}$ is an edge of the domain, possibly with $x = y$, then $\{f(x), f(y)\}$ is an edge of the codomain). 


## Properties of $SimpGph$ 

The category $SimpGph$ has very good properties. For example,  

+-- {: .num_theorem} 
###### Theorem 
$SimpGph$ is a [[Grothendieck quasitopos]]. In particular, it is a [[regular category]] and even a [[logos]], and $SimpGph^{op}$ is also regular. It is also $\infty$-[[extensive category|extensive]]. 
=-- 

+-- {: .proof} 
###### Proof 
(See also [Adamek and Herrlich](#AdamHerr).) As above, let $C$ be the category of sets $1$ and $2$ and functions between them, and regard the category of simple graphs as a full subcategory of the presheaf [[topos]] $Set^{C^{op}}$. For this presheaf topos, there is just one nontrivial $\neg\neg$-dense sieve, namely the inclusion 

$$(s, t): C(-, 1) + C(-, 1) \to C(-, 2)$$ 

(where $s$ is shorthand for $C(-, \ast \mapsto s)$ and similarly for $t$) and so the category of $\neg\neg$-[[separated presheaves]] is equivalent to the category of presheaves $X$ such that the induced map 

$$X(2) \cong Set^{C^{op}}(C(-, 2), X) \stackrel{(s, t)^\ast}{\to} Set^{C^{op}}(C(-, 1) + C(-, 1), X) \cong X(1) \times X(1),$$ 

which is the source-target pairing $\langle d_0, d_1 \rangle: X(2) \to X(1) \times X(1)$, is monic. In other words, a simple graph in this language is exactly a separated presheaf. On the other hand, a Grothendieck quasitopos is, essentially by definition, the category of separated presheaves for a topology on a presheaf topos, in this case the $\neg\neg$-topology. 

Being a quasitopos with small coproducts, it is $\infty$-extensive provided that coproducts are disjoint. However, this is trivial to check (it even suffices to check, according to [[Elephant]] 2.6.5, that $0 \to 1$ is a [[regular monomorphism]], or that $1 + 1$ is a disjoint coproduct, which it obviously is). 
=-- 

It is easy to describe [[monomorphism|monos]] and [[epimorphism|epis]] in $SimpGph$. For, let $\Gamma = \hom(1, -): SimpGph \to Set$ be the underlying vertex-set [[forgetful functor]]. 

+-- {: .num_prop #specificEmbeddingOfSimpGphIntoSet} 
###### Proposition 
The forgetful functor $\Gamma = \hom(1, -): SimpGph \to Set$ is faithful, in fact exhibits $SimpGph$ as a [[topological concrete category]]. 
=-- 

We omit the easy proof. Next we have two easy results:  

+-- {: .num_prop} 
###### Proposition 
$\Gamma$ [[reflected limit|reflects]] monos and epis (because $\Gamma$ is faithful). 
=-- 

+-- {: .num_prop} 
###### Proposition 
$\Gamma$ [[preserved limit|preserves]] [[limits]] and [[colimits]] (because it has a [[left adjoint]] $\Delta$ and a [[right adjoint]] $\nabla$). 
=-- 

It follows that $\Gamma: SimpGph \to Set$ both preserves and reflects monos and epis. As a result, we can prove various simple exactness results in $SimpGph$. For instance: 

+-- {: .num_lemma}
###### Lemma 
In $SimpGph$, the [[pushout]] of any mono is a mono. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose we have a pushout diagram in $SimpGph$: 

$$\array{
G & \to & H \\
 ^\mathllap{mono} \downarrow & & \downarrow^\mathrlap{k} \\ 
G' & \to & H'
}$$ 

Since $\Gamma$ preserves both pushouts and monos, and since the pushout of a mono in $Set$ is a mono, we have that $\Gamma(k)$ is monic in $Set$. Since $\Gamma$ reflects monos, this means $k$ is monic in $SimpGph$. 
=-- 

As already observed, there is a chain of adjoint functors $\Delta \dashv \Gamma \dashv \nabla: Set \to SimpGph$. But in fact there is a fourth functor in the chain: $\Delta$ has a left adjoint $\Pi: SimpGph \to Set$, the [[connected object|connected components]] functor. If $E$ is the simple graph consisting of two vertices $a, b$ with an edge between them, then there is a reflexive fork 

$$a, b: 1 \rightrightarrows E \stackrel{!}{\to} 1$$ 

and $\Pi$ is formed as a [[reflexive coequalizer]] of the induced diagram: 

$$SimpGph(1, -) \to SimpGph(E, -) \rightrightarrows SimpGph(1, -) \to \Pi$$ 

+-- {: .num_prop} 
###### Proposition 
$\Pi \dashv \Delta$, and $\Pi$ preserves products. 
=-- 

+-- {: .proof} 
###### Proof 
$\Pi$ preserves products because being a reflexive coequalizer, it is a [[sifted colimit]] of product-preserving functors. For graphs $G$, there is a natural map $u G: G \to \Delta \Pi G$ which at the underlying vertex-set level sends a vertex to its connected component; if $S$ is any set, then a graph map $f: G \to \Delta S$ must send any two vertices with an edge between them to the same point, and so $f$ factors as $G \stackrel{u G}{\to} \Delta \Pi G \stackrel{\Delta g}{\to} \Delta S$ for a unique map $g: \Pi G \to S$, and this establishes the adjunction $\Pi \dashv \Delta$. 
=-- 

### Equalizers and coequalizers

If $f, g \colon G \stackrel{\to}{\to} H$ are maps in $SimpGph$, then their [[equalizer]] $Eq(f, g) = i \colon K \to G$ is given at the vertex level by 

$$\Gamma(i) = Eq(\Gamma(f), \Gamma(g))$$ 

and at the edge level by $K(x, y) \Leftrightarrow G(i(x), i(y))$; in other words, if $x, y$ belong to $K$ and there is an edge between them in $G$, then that edge lies in $K$. To express this last condition, we say the subgraph $i$ is _full_ (at the edge level). 

Thus, $i$ is a regular mono in $SimpGph$ iff both $\Gamma(i)$ is monic in $Set$ and $i$ is full at the edge level. 

The [[coequalizer]] of $f$ and $g$, say $Coeq(f, g) = q \colon H \to Q$, is given at the vertex level by 

$$\Gamma(q) = Coeq(\Gamma(f), \Gamma(g))$$ 

and at the edge level by taking the image of the composite $E_H \hookrightarrow Vert(H)^2 \stackrel{q^2}{\to} Vert(Q)^2$, so that 

$$Q(x, y) \Leftrightarrow \exists_{u, v} H(u, v) \wedge q(u) = x \wedge q(v) = y.$$ 

Thus, $q$ is a [[regular epimorphism]] if it is surjective at both the vertex and edge levels. 


### Ternary factorization 

The category of simple graphs has a [[ternary factorization system]] as follows: each morphism $f \colon G \to H$ factors as 

$$G \stackrel{q}{\to} G' \stackrel{a}{\to} H' \stackrel{i}{\to} H$$ 

where 

* $q$ is a surjection between vertex-sets and at the edge level, i.e., is a [[regular epi]]; 

* $a$ induces an identity between vertex-sets (hence is [[bimorphism|jointly monic and epic]]), but without necessarily being full at the edge level; 

* $i$ is given by an injection between vertex-sets and is full at the edge level, and (thus) is a [[regular mono]]. 

The factorization of $f$ into $q$ followed by $i \circ a$ is the (regular epi)-mono factorization, while the factorization of $f$ into $a \circ q$ followed by $i$ is the epi-(regular mono) factorization. To round out
the discussion, we prove that regular monos are stable under pushout (which ensures that the epi-(regular mono) factorization is an [[orthogonal factorization system]]). 

### Three wide subcategories of $SimpGph$

In this section we will analyse and compare three wide subcategories of SimpGph. 
Each is a [[left cancellative category]]. 

In this section,  SimpGph has the same meaning as in the other sections, but there are slight notational variations, and a few other conventions, which we now list: 

* $\rotatebox{180}{\textsf{T}}$ denotes falsity
* $\textsf{T}$ denotes truth
* $E$ is used like an infix relation-symbol, 
* the sequent-notation $\vdash$, sometimes possibly with [[context]]s given in subscripts, is used for implications. (No ambiguity with regard to the symbol $\mathsf{T}$ for truth, nor with regard the usual symbol $\leftvdash$ to indicate left adjoints will arise.)
* the usual graph-theoretic distance-function is denoted by $\mathrm{dist}_{(V,E)}\colon V\times V\rightarrow\omega$, where $\omega$ denotes the natural numbers and $(V,E)$ is usually abbreviated by the name of the graph $(V,E)$,
* we use the taditional subobjects-are-isomorphism-classes-of-monos-convention, as in [[subobject]].


We recall that, by Section(reftodo), for any objects $G_0=(V_0,E_0)$ and $G_1=(V_1,E_1)$ of SimpGph, 

* there is the hom-set SimpGph$(G_0,G_1)$ $=$ $\{$ all set-maps $V_0\overset{f_0}{\rightarrow}V_1$ with $u_{0,0}$ $E$ $u_{0,1}$ $\vdash$ $f(u_{0,0})$ $E$ $f(u_{0,1})$ $\}$, 
* this hom-set is never empty, except if $G_1$ is the empty graph $(\emptyset,\emptyset)$; therefore, _every_ object of SimpGph except its initial object is [[weakly terminal]]

We now define three wide subcategories of SimpGph: 

SimpGph.WeakEmbeddings, 

SimpGph.StrongEmbedding, 

SimpGph.IsometricEmbedding.

It suffices to specify hom-sets of each, because closedness under composition of the three subclasses of $\mathrm{Mor}(SimpGph)$ will be evident from the respective definitions. 

SimpGph.WeakEmbeddings($G_0,G_1$) $:=$  $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: $f$ is  injective, as a set-map $\}$

SimpGph.StrongEmbeddings($G_0,G_1$) $:=$  $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: $f$ is a graph-isomorphism onto its image $\}$

SimpGph.IsometricEmbeddings($G_0,G_1$) $:=$ $\{$ $f$ $\in$ SimpGph$(G_0,G_1)$: $f$ is a graph-isomorphism onto its image, and $\mathsf{T}\vdash_{x,y:V_0}$ $\mathrm{dist}_{\mathrm{im}(f)}(f(x),f(y))=\mathrm{dist}_{G_1}(f(x),f(y))$\}$.


##### Remarks on motivation. 

Analyzing the above subcategories has natural connections with other parts of category theory and graph theory. For example (to be systematic and to take the [[nPOV]]), we will always choose the category-theoretic term, i.e., not write _strong embedding_, but _regular mono_, and not _isometric embedding_ but rather _isometric regular mono_).

* Large parts of category theory are about specified subclasses of the class of morphisms of a category. (Example: the study of [[weak equivalence]]s in [[homotopy theory]]). And, roughly and intuitively, both the regular monos of SimpGph, and the still smaller class of isometric regular monos of SimpGrph, can be seen as some sort of weakly invertible morphism. Analysing the above classes can be seens as an exercise in systematically analyzing some composition-closed class of morphisms that mathematical practice happens to throw at you.

* Comparing the three classes can be instructive with regard to better understanding logicall aspects of 1-category theory. We will compare axiomatizability of the three above composition-closed classes w.r.t. first-order logic of category theory.

* Isometric regular monos of SimpGph have several uses in graph theory. For example: 
* * A given graph class can often be organized, put in context, and provided with some sort of _canonical representation_, by proving that each of its members admits an isometric regular mono to some member of a larger, yet more symmetric, graph class. An example is that every for finite [[median graph]] $G$ there exists an isometric regular mono into a suitably high-dimensional finite [[hypercube]] graph. (The median graphs are not characterized by this property though, there are non-median graphs which can be so embedded) Cf. e.g. (#ImrichKlavzar), (#BandeltChepoi2008) (#Chepoi))
* * Isometric regular monos are used (though not so named) in proofs of [[zero-one-law]]s for graph classes, and in proofs of non-axiomatizability of certain graph-classes (defined by given higher-order conditions). Briefly, the method of proof is the following: under favorable circumstances there exist _universal representatives_ of an elementary-equivalence-class, i.e., for a (higher-order-definition-defined) graph class $\mathbb{K}$ there exists a single graph $T_{\mathrm{elling}}\in\mathbb{K}$ such that for _every_ graph $G\in\mathbb{K}$, 

* * * (tellingly.shaped) if the hom-set Mor(SimpGph.IsometricEmbeddings($T_{\mathrm{elling}}$,G$))$ is non-empty, then $T_{\mathrm{elling}}$ and $G$ are elementarily-equivalent.

Intuitively: if we can prove that the graph $G$ has a $T_{\mathrm{elling}}$ly-shaped generalized point, then we know it to be in the equivalence class we are interested in. 
This is one more example of the well-known principle of characterizing some property (here: _being elementarily equivalent_) by the existence of at least one good morphism in an suitable category.

(There are versions of this for the full subcategory $\mathsf{SimpGph}_{<\omega}$ of finte graphs, in which of course, elementary equivalence is the same as isomorphism and thus is often weakened to equivalence up to some [[quantifier-rank]].)

The reason for the importance of isometric regular monos for the implication (tellingly.shaped) is the use of [[Gaifman normal forms]] (GNF) of first-order formulas in its proof. Roughly speaking, isometric regular monos are guaranteed to respect a GNF, while moving along regular monos, let alone monos, may invalidate a GNF.

 To sum up, 

* while [[isometric regular monos]] have several uses, they should not only be _used_ but also be _reflected on_, in terms of their mapping properties. Category theory provides the tools for this. 

##### Evident properties of the wide subcategories

We start with pointing out evident properties. 

* Each of SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, SimpGph.IsometricEmbedding are [[concrete categories]], because by Proposition\ref{speicificEmbeddingOfSimpGphIntoSet} SimpGph is one.


*  There are class inclusions

Mor(SimpGph.IsometricEmbeddings) $\subset$ Mor(SimpGph.StrongEmbeddings) $\subset$ Mor(SimpGph.WeakEmbeddings) $=$ Monos(SimpGph).

* Because of the latter equality, each of SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, SimpGph.IsometricEmbedding is a [[left cancellative category]].

* None on SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, SimpGph.IsometricEmbedding is a [[groupoid]], nor a [[preorder]].


* The relation $(\emptyset,\emptyset)$ is the (only) initial object of each of SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, SimpGph.IsometricEmbedding. (Note that the relation $(\emptyset,\emptyset)$ is symmetric and reflexive.) 

* None of SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, SimpGph.IsometricEmbedding has any [[terminal object]].


#### Which of the wide subcategories has all finite products

(under construction)

 
#### Using the concept of categories-having-images

For further reference, we now recall a few basic concepts. 

A category $\mathsf{C}$ _having images_ means 

* for every object $O$ of $\mathsf{C}$ the canonical inclusion functor of the poset $\mathrm{Sub}(O)$ of subobjects of $O$ (as a posetal category) into the slice category $\mathsf{C}/O$ has a left adjoint. 

If so, the left-adjoint is denoted by $\mathrm{im}$.

If $\mathsf{C}$ has images, and if, moreover, $\mathsf{C}$ has all pullbacks, then 

* for every morphism $O_0\overset{f}{\longrightarrow}O_1$ of $\mathsf{C}$ the pullback $\mathrm{Sub}(O_1)\overset{f^\ast}{\rightarrow}\mathrm{S}(O_0)$ has a left adjoint. 

This left adjoint is often denoted by $\exists_f\leftvdash f^\ast$.

With regard to the three wide subcategories $\mathsf{C}$, we hasten to note that, of course, 

* [[left cancellative category|each of their morphisms is monic]], hence each $\mathrm{Sub}(O)$ arises from $\mathsf{C}/O$ just by identifying all isomorphic objects of the slice-category, and hence, just as in _any_ left cancellative category, 
* * for each $\mathsf{C}$ $=$ SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, 
SimpGph.IsometricEmbedding, and for each $O$bject of $\mathsf{C}$,
$$\array{\mathrm{Sub}(O) = \mathrm{Skeleton}(\mathsf{C}/O)}$$


We will now analyse systematically whether SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, 
SimpGph.IsometricEmbedding,

(images) have images, 
(pullbacks) have pullbacks.



As to (images), we argue from the general to the specific. We recall that because of Proposition \ref{specificEmbeddingOfSimpGphIntoSet}, 
* each of the categories in question is a [[concrete category]],

and now ask, in general: 

* Under which hypotheses does a concrete category have images?

Moreover, we ask: 

* If $\textsf{C}$ is a category and $U\colon\mathsf{C}\rightarrow\textsf{Set}$ is a faithful functor, under what hypotheses on the _pair_ $(\mathsf{C},U)$ does it follow that $\textsf{C}$ has images _and_ for each morphism $f$ of $\mathsf{C}$ we have $\mathrm{im}(f)=\mathrm{SetMapImage}(U(f))$?

We will then specialize to SimpGph.WeakEmbeddings, SimpGph.StrongEmbedding, 
SimpGph.IsometricEmbedding. 

(under construction)

#### A remark on epi-mono-factorizations


We recall:

* (epi.mono) Every morphism of SimpGph has an epi-mono-factorization. That is, for each $f\in$Mor(SimpGph)t here is a $m$ono and an $e$pi of $SimGph$ with $f=m\circ e$.

We note the following evident implication:

* _if_ there is a morphism $\mathrm{dom}(f)\overset{h}{\rightarrow}\mathrm{dom}(f)$ of SimpGph with 

(twosided) $h\circ e=1_{\mathrm{dom}(f)}$ and $e\circ h = 1_{\mathrm{cod}(f)}$

then
$f\in\mathsf{SimpGph.StrongEmbeddings}$.

<sub> 
Proof. Let $\Gamma:\mathsf{SimpGph}\rightarrow \mathsf{Set}$ be the embedding from Proposition \ref{specificEmbeddingOfSimpGphIntoSet}. 
By definition, $e = (Gamma(f))|_{im(f)}$, and, since $\Gamma$ is a functor, (twosided) implies
$(\Gamma(h))\circ(\Gamma(e))=1_{\Gamma(\mathrm{dom}(f))}$
and
$(\Gamma(e))\circ(\Gamma(h))=1_{\Gamma(\mathrm{cod}(f))}$
hence $\Gamma(h)$ is a graph-isomorphism $O_0\rightarrow {\rm im}(f)$, i.e. $f\in \mathsf{SimpGph.StrongEmbeddings}$.
</sub>



##### Example of an epi-mono-factorication of a non-isometric regular monomorphism in SimpGph

The following is an epi-mono-factorization $f=m\circ e$ of the non-isometric strong embedding, i.e., non-isometric regular mono $f$ given by $f u_i = v_i$ for each $i\in4$.

[[!include nonisometricregular20170614]]


##### Example of a non-[[regular monomorphism]] in SimpGph

The morphism $f$ of SimpGph defined by the illustration on the left is a non-regular mono in SimpGph; graph-theoretically speaking, it is not a strong embedding. 


<div style="float:left;width:4em;height:25em;margin: 10px 10px 10px 0;">
  <svg xmlns="http://www.w3.org/2000/svg"
       xmlns:xlink="http://www.w3.org/1999/xlink"
       width="100%" height="100%" viewBox="0 0 400 300" >
    <g>
[[!include nonregularmono20170614]]
    </g>
  </svg>
</div>


#### Characterizing the classes of morphisms of the three wide subcategories

##### Mor(SimpGph.WeakEmbeddings) 

The weak isomorphisms are precisely the monos in SimpGph. 
Therefore, Mono(SimpGph) is an [[elementary class]], even a [[finitely axiomatizable]] class, and even axiomatizable by [[Horn]] sequents, w.r.t. the usual first-order theory of (1-)category theory. We recall that its signature is $\circ,\mathrm{cod},\mathrm{dom}$, where $\circ$, $\mathrm{cod}$ and $\mathrm{dom}$ are function symbols with the usual semantics. As usual, we treat $=$ not a as relation symbol, but as a logical symbol. Moreover, we invariably write the variables as $f_i$ with some $i\in\omega$. Since the usual fist-order language of category theory has one sort only (treating objects as identity-morphisms), we do not specify the sort when we use the sequent notation; as an example of this convention, let us take the time to spell out the definition of monos: 
Mor(SimpGph.WeakEmbeddings) $=$ Mono(SimpGph) $=$ $\{ f_0:\quad (f_0\circ f_1 = f_0\circ f_2) \vdash_{f_0,f_1,f_2} (f_1 = f_2)   \}$.
Here, no sort for the $f_i$ has been specified, since there is only one. 

##### Mor(SimpGph.StrongEmbeddings) 

(under construction)

##### Mor(SimpGph.IsometricEmbeddings) 

The definition of the class of morphisms makes use of the distance-function, hence is not a definition in the language of category theory. Needless to say, this does not mean that it could not perhaps be axiomatized nevertheless in that language. We will now prove that it cannot.

(under construction)


## References 

* [[Jiří Adámek]] and Horst Herrlich, _Cartesian closed categories, quasitopoi, and topological universes_. Comm. Math. Univ. Carol., Vol. 27, No. 2 (1986), 235-257. ([web](http://dml.cz/handle/10338.dmlcz/106447))
{#AdamHerr} 

* [[Hans-J&uuml;rgen Bandelt, Victor Chepoi]], Metric graph theory and geometry: a survey. Contemporary Mathematics, Volume 453, 2008, 
{#BandeltChepoi2008}

* Reinhard Diestel, Graph Theory (Second Edition), Graduate Texts in Mathematics 173, Springer (2000). 
{#Diestel}


category: category

[[!redirects category of simple graphs]]
[[!redirects Simp Gph]]
[[!redirects SimpGph]]

[[!redirects simple graph]]
[[!redirects simple graphs]]
