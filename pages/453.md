
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}


## Idea

A _regular category_ is a [[finitely complete category]] which admits a good notion of [[image]] factorization. A primary _raison d'&#234;tre_ behind regular categories $C$ is to have a decently behaved _calculus of [[relations]]_ in $C$.  

Regular categories also provide a natural [[semantics|semantic]] environment to [[interpretation|interpret]] a particularly well behaved positive [[fragment]] of [[first order logic]] having connectives $\top$, ${\wedge}$, $\exists$; in other words, their [[internal logic]] is [[regular logic]].

## Definition

+-- {: .num_defn}
###### Definition

A [[category]] $C$ is called **regular** if 

1. it is [[finitely complete category|finitely complete]]; 

1. the [[kernel pair]] 

   $$
     \array{
       d\times_c d &\stackrel{p_1}{\to}& d
       \\
       {}^{\mathllap{p_2}}\downarrow && \downarrow^{\mathrlap{f}}
       \\
       d &\stackrel{f}{\to}& c
     }
   $$

   of any [[morphism]] $f: d \to c$ admits a [[coequalizer]] $d \times_c d \,\rightrightarrows\, d \to coeq(p_1,p_2)$;  

1. the [[pullback]] of a [[regular epimorphism]] along any morphism is again a regular epimorphism.

=--

We make the following remarks:

* The kernel pair is always a [[congruence]] on $d$ in $C$; informally, $\ker(f) = d\times_c d$ is the [[subobject]] of $d \times d$ consisting of pairs of elements which have the same value under $f$ (sometimes called the "kernel" of a function in [[Set]]). The coequalizer above is supposed to be the "object of equivalence classes" of $\ker(f)$ as an internal [[equivalence relation]].

* A map which is the coequalizer of a parallel pair of morphisms is called a _[[regular epimorphism]]_. In fact, in any category satisfying the first two conditions above, every regular epimorphism is the coequalizer of its kernel pair. (See for instance Lemma 5.6.6 in _[[Practical Foundations]]_.)

* The last condition may equivalently be stated in the form "coequalizers of kernel pairs are stable under pullback". However, it is not generally true in a regular category that the pullback of a general coequalizer diagram 

  $$e \;\rightrightarrows\; d \to c$$ 

  along a morphism $c' \to c$ is again a coequalizer diagram (nor need a regular category have coequalizers of all parallel pairs).

In fact, an equivalent definition is:

+-- {: .num_defn}
###### Definition

A **regular category** is a finitely complete category with pullback-stable [[image]] factorizations.

=--

Here we are using "image" in the sense of "the smallest monic through which a morphism factors."  See [[familial regularity and exactness]] for a generalization of this approach to include [[coherent category|coherent]] categories as well.


## Examples

Examples of regular categories include the following:

* [[Set]] is a regular category. 

* More generally, any [[topos]] is regular. 

* Even more generally, a [[locally cartesian closed category]] with [[coequalizers]] is regular, and so any [[quasitopos]] is regular. 

* The category of [[algebra over a Lawvere theory|models]] of any finitary [[algebraic theory]] (i.e., [[Lawvere theory]]) $T$ is regular. This applies in particular to the category [[Ab]] of [[abelian group]]s. 

* Actually, any category that is [[monadic functor|monadic]] over [[Set]] is regular. For example, the category of [[frames]] $Frm \simeq Loc^{op}$ is regular, and the category of [[compact Hausdorff spaces]] is regular. A proof may be found [here](/nlab/show/colimits+in+categories+of+algebras#exact). 

* Any [[abelian category]] is regular. 

* If $C$ is regular, then so is the [[functor category]] $C^D$ for any category $D$. 

* If $C$ is regular and $T$ is a [[Lawvere theory]], then the category $Mod(T, C)$ of $T$-models in $C$ is also regular. See Theorem 5.11 in Barr's [Exact Categories](#Barr). 

* A [[slice]] of a regular category is also regular; cf. [[locally regular category]]. So is any [[co-slice]]. (Source: [[Borceux-Bourn]], Appendix section 5.) 

* If $Q$ is a quasitopos, then $Q^{op}$ is regular. Source: A2.6.3(i) in the [[Elephant]]. 

* [[Top]]$^{op}$ is regular. The key facts are that [[regular monomorphisms]] in $Top$ are the same as [[subspace]] inclusions, and that the [[pushout]] of a subspace inclusion is a subspace inclusion as proven [here](/nlab/show/subspace+topology#pushout). 

* The category of ([[Hausdorff space|Hausdorff]]) [[Kelley spaces]] is regular (but is not, however, locally cartesian closed, nor is it [[exact category|exact]]) ([Cagliari-Matovani-Vitale 95](#CagliariMatovaniVitale95)) 


Examples of categories which are **not regular** include 

* [[Cat]], [[Pos]], and [[Top]]. 

The following example proves failure of regularity in all three cases: let $A$ be the poset $\{a, b\} \times (0 \to 1)$; let $B$ be the poset $(0 \to 1 \to 2)$, and let $C$ be the poset $(0 \to 2)$. There is a regular epi $p: A \to B$ obtained by identifying $(a, 1)$ with $(b, 0)$, and there is the evident inclusion $i: C \to B$. The pullback of $p$ along $i$ is the inclusion $\{0, 2\} \to (0 \to 2)$, which is certainly an epi but not a regular epi. Hence regular epis in $Pos$ are not stable under pullback. 

Interpreting the posets as categories, the same example works for $Cat$, and also for preorders. On the other hand, the category of finite preorders is equivalent to the category of finite topological spaces, so this example serves to show also that $Top$ is not regular. 

However: 

* If $T$ is a [[Mal'cev theory]] (e.g., the theory of groups), then the category $Top^T$ of $T$-models in [[Top]] is regular. This is because for $T$ Mal'cev, coequalizer maps in $Top^T$ are necessarily open surjections, and open surjections are stable under pullback. 

## Properties

### Epimorphisms
 {#Epimorphisms}

\begin{prop}
For a [[morphism]] $f$ in a [[regular category]], the following conditions are all equivalent:

1. $f$ is an [[effective epimorphism]];

1. $f$ is a [[regular epimorphism]];

1. $f$ is a [[strong epimorphism]];

1. $f$ is an [[extremal epimorphism]].

\end{prop}


### Factorization properties 


+-- {: .num_prop}
###### Proposition
**image factorization**

In a regular category, every morphism $f : x\to y$ can be factored -- uniquely up to [[isomorphism]] -- through its [[image]] $im(f)$ as

$$
  f : x \stackrel{e}{\to} im(f) \stackrel{i}{\to} y
  \,,
$$

where $e$ is a [[regular epimorphism]] and $i$ a [[monomorphism]]. 

=--

+-- {: .proof}
###### Proof

Let $e : x \to im(f)$ be the [[coequalizer]] of the [[kernel pair]] of $f$. Since $f$ coequalizes its kernel pair, there is a unique map $i: im(f) \to y$ such that $f = i e$. It may be shown from the regular category axioms that $i$ is monic and in fact represents the [[image]] of $f$, i.e., the smallest subobject through which $f$ factors.  

A proof is spelled out on p. 30 of ([vanOosten](#vanOosten)).

=--


+-- {: .num_prop}
###### Proposition

The classes of [[regular epimorphism]], [[monomorphism]]s in a regular category $C$ form a [[orthogonal factorization system|factorization system]].

=--


### Embedding properties 

+-- {: .num_barrembeddingtheorem}
###### Proposition

If a regular category is small, it admits particularly nice embeddings into presheaf categories. See [[Barr embedding theorem]] for more. 


### Axiomatizability properties 

Roughly speaking, regular categories tend to be relatively well-behaved when it comes to desribing them in formalized logics.

#### Regular functors over a small regular category 

##### A result of Makkai 


###### Proposition (Makkai)

If a regular category $\mathcal{R}$ is small, then the full subcategory of the functor category $[\mathcal{R},\mathsf{Set}]$ consisting of the [[regular functors]] only is an [[elementary class]] w.r.t. the signature given by (the underlying graph) of $\mathcal{R}$.


=--

## Stronger conditions

### Exactness

If a regular category additionally has the property that every [[congruence]] is a kernel pair (and hence has a quotient), then it is called a (Barr-) [[exact category]].  Note that while regularity implies the existence of some coequalizers, and exactness implies the existence of more, an exact category need not have all coequalizers (only coequalizers of congruences), whereas a regular category can be [[cocomplete category|cocomplete]] without being exact.

Regularity and exactness can also be phrased in the language of [[Galois connection]]s, as a special case of the notion of [[generalized kernels]].


### Higher arity

As exactness properties go, the ones possessed by general regular categories are fairly moderate; the main condition is of course stability of regular epis under pullback.  A natural generalization is to include (finite or infinite) unions of subobjects, or equivalently images of (finite or infinite) families as well as of single morphisms.  This leads to the notion of [[coherent category]].

Just as regularity implies the existence of certain coequalizers, coherence implies the existence of certain [[coproducts]] and [[pushouts]], but not all.  A [[lextensive category]] has all (finite or infinite) coproducts that are disjoint and stable under pullback.  It is easy to see that a lextensive regular category must actually be coherent.


## The regular topology

Any regular category $C$ admits a [[subcanonical site|subcanonical]] [[Grothendieck topology]] whose covering families are generated by single [[regular epimorphisms]]: the [[regular coverage]].  If $C$ is [[exact category|exact]] or has pullback-stable [[reflexive coequalizer]]s, then its [[codomain fibration]] is a [[stack]] for this topology (the necessary and sufficient condition is that any pullback of a kernel pair is again a kernel pair).


## Making categories regular

Any category $C$ with [[finite limits]] has a **reg/lex completion** $C_{reg/lex}$ with the following properties:

* There is a [[full and faithful functor]] $C\hookrightarrow C_{reg/lex}$
* Each object of $C$ becomes [[projective object|projective]] in $C_{reg/lex}$
* Each left-exact functor $C\to D$, where $D$ is regular, extends to an essentially unique [[regular functor]] $C_{reg/lex}\to D$.

In particular, the reg/lex completion is a left adjoint to the [[forgetful functor]] from regular categories to lex categories (categories with finite limits).  The reg/lex completion can be obtained by "formally adding images" for all morphisms in $C$, or by "closing up" $C$ under images in its [[presheaf category]] $[C^{op},Set]$; see [[regular and exact completions]].  In general, even if $C$ is regular, $C_{reg/lex}$ is larger than $C$ (that is, it is a [[free cocompletion]] rather than merely a [[completion]]), although if $C$ satisfies the [[axiom of choice]] (in the sense that all [[regular epimorphisms]] are split), then $C\simeq C_{reg/lex}$.

Regular categories of the form $C_{reg/lex}$ for a lex category $C$ can be characterized as those regular categories in which every object admits both a regular epi from a projective object and a monomorphism into a projective object, and the projective objects are closed under finite limits.  In this case $C$ can be recovered as the subcategory of projective objects.  In fact, the construction of $C_{reg/lex}$ can be extended to categories having only [[weak finite limits]], and the regular categories of the form $C_{reg/lex}$ for a "weakly lex" category $C$ are those satisfying the first two conditions but not the third.

When the reg/lex completion is followed by the [[ex/reg completion]] which completes a regular category into an [[exact category|exact one]], the result is unsurprisingly the [[ex/lex completion]].  See [[regular and exact completions]] for more about all of these operations.
 
## Related entries

* [[exact category]], [[coherent category]], [[pretopos]]

* [[regular 2-category]], [[regular derivator]], [[regular (∞,1)-category]]

* [[regular logic]]

* [[Barr embedding theorem]]

## References

Regular categories were introduced in three different articles in LNM **236** by Barr, Grillet and Van Osdool, respectively:

* [[Michael Barr]],  _Exact categories_,  Lec. Notes in Math. __236__, Springer-Verlag 1971, 1-119. ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.732.4603&rep=rep1&type=pdf)) 
 {#Barr}

* P. A. Grillet, _Regular Categories_ , pp.121-222.

* D. H. Van Osdool, _Sheaves in Regular Categories_ , pp.223-239.

Some of the historical context is provided in the introduction of

* [[Peter Johnstone]], _Topos Theory_ (1977)

A nice textbook treatment can be found in chapter 2 of

* [[Francis Borceux]], _Handbook of Categorical Algebra 2: Categories and Structures_ , Cambridge UP 1994.

More streamlined are

* [[Peter Freyd]], Andre Scedrov, _Categories, Allegories_ , North-Holland Amsterdam 1990. (chap. 1.5. pp.68ff)

* [[Peter Johnstone]], _Sketches of an Elephant I_ , Oxford UP 2002. (section A1.3. pp.18ff)

* [[Dominique Bourn]], [[Marino Gran]], _Regular, Protomodular, and Abelian Categories_ , chap. IV pp.165-211 in Pedicchio, Tholen (eds.), _Categorical Foundations_ , Cambridge UP 2004.

A concise introductory monograph is

* [[Carsten Butz]], _Regular Categories and Regular Logic_ , BRICS LS-98-2 Aarhus 1998. ([brics](http://www.brics.dk/LS/98/2/))

The following set of course notes has a section on regular categories 

* {#vanOosten}[[Jaap van Oosten]], _Basic category theory_ , BRICS LS-95-1 Aarhus 1995. ([Section 4.1](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf#page=30)) ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

An application of the regularity condition[^knop] is found in:

* F. Knop, _Tensor envelopes of regular categories_, ([arXiv:math/0610552v2](http://arxiv.org/abs/math/0610552))

[^knop]: Knop's condition for regularity is slightly different from that presented here; he works with categories that when augmented by an absolutely initial object are regular in the terminology here.  In the paper, Knop generalizes a construction of Deligne by showing how to construct a symmetric pseudo-abelian [[tensor category]] out of a regular category through the calculus of relations.

Enriched generalization of regular categories:

* [[Brian Day]], [[Ross Street]], _Localisation of locally presentable categories_, J. Pure and Appl. Algebra __58__ (1989) 227-233.

* Dimitri Chikhladze, _Barr's embedding theorem for enriched categories_, J. Pure Appl. Alg. __215__, n. 9 (2011) 2148-2153, [arxiv/0903.1173](http://arxiv.org/abs/0903.1173), [doi](http://dx.doi.org/10.1016/j.jpaa.2010.12.004)

Regularity of (Hausdorff) [[compactly generated topological spaces]]:

* {#CagliariMatovaniVitale95} F. Cagliari, S. Mantovani, [[Enrico Vitale]], *Regularity of the category of Kelley spaces*, Applied Categorical Structures volume 3, pages 357–361 (1995) ([doi:10.1007/BF00872904](https://link.springer.com/article/10.1007/BF00872904), [pdf](http://www.dm.unibo.it/~cagliari/articoli/Regularkelley.pdf))


[[!redirects regular categories]]
