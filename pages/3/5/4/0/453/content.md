
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


\begin{definition}\label{RegularCategory}
**(regular category)**
\linebreak

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

\end{definition}

\begin{remark}
The kernel pair is always a [[congruence]] on $d$ in $C$; informally, $\ker(f) = d\times_c d$ is the [[subobject]] of $d \times d$ consisting of pairs of elements which have the same value under $f$ (sometimes called the "kernel" of a function in [[Set]]). The coequalizer above is supposed to be the "object of equivalence classes" of $\ker(f)$ as an internal [[equivalence relation]].
\end{remark}

\begin{remark}
A map which is the coequalizer of a parallel pair of morphisms is called a _[[regular epimorphism]]_. In fact, in any category satisfying the first two conditions in Def. \ref{RegularCategory}, every regular epimorphism is the coequalizer of its kernel pair. (See for instance Lemma 5.6.6 in _[[Practical Foundations]]_.)
\end{remark}

\begin{remark}
The last condition in Def. \ref{RegularCategory} may equivalently be stated in the form "coequalizers of kernel pairs are stable under pullback". However, it is not generally true in a regular category that the pullback of a general coequalizer diagram 

  $$e \;\rightrightarrows\; d \to c$$ 

  along a morphism $c' \to c$ is again a coequalizer diagram (nor need a regular category have coequalizers of all parallel pairs).
\end{remark}

In fact, a definition equivalent to Def. \ref{RegularCategory} is:

\begin{definition}
A **regular category** is a [[finitely complete category]] with [[pullback]]-stable [[image]] factorizations.
\end{definition}

Here we are using "image" in the sense of "the smallest [[monomorphism]] through which a morphism factors."  See *[[familial regularity and exactness]]* for a generalization of this approach to include [[coherent category|coherent]] categories as well.


## Examples

Examples of regular categories include the following:

\begin{example}
[[Set]] is a regular category. 
\end{example}

\begin{example}
More generally, any [[topos]] is regular. 
\end{example}

\begin{example}
Even more generally, a [[locally cartesian closed category]] with [[coequalizers]] is regular, and so any [[quasitopos]] is regular. 
\end{example}

\begin{example}
The category of [[algebra over a Lawvere theory|models]] of any finitary [[algebraic theory]] (i.e., [[Lawvere theory]]) $T$ is regular. This applies in particular to the category [[Ab]] of [[abelian groups]].
\end{example}

\begin{example}\label{CategoryOfGroupsIsRegular}
  The category [[Grp]] of all [[groups]] (including [[non-abelian groups]]) is regular.
\end{example}
(e.g. [Borceux 1994 II, Ex. 2.4.3](#Borceux94))

\begin{example}
Actually, any category that is [[monadic functor|monadic]] over [[Set]] is regular. For example, the category of [[frames]] $Frm \simeq Loc^{op}$ is regular, and the category of [[compact Hausdorff spaces]] is regular. A proof may be found [here](/nlab/show/colimits+in+categories+of+algebras#exact). 
\end{example}

\begin{example}
Any [[abelian category]] is regular. 
\end{example}

\begin{example}
If $C$ is regular, then so is the [[functor category]] $C^D$ for any category $D$. 
\end{example}

\begin{example}
If $C$ is regular and $T$ is a [[Lawvere theory]], then the category $Mod(T, C)$ of $T$-models in $C$ is also regular. See Theorem 5.11 in Barr's [Exact Categories](#Barr). 
\end{example}

\begin{example}
A [[slice]] of a regular category is also regular; cf. [[locally regular category]]. So is any [[co-slice]]. (Source: [[Borceux-Bourn]], Appendix section 5.) 
\end{example}

\begin{example}
If $Q$ is a quasitopos, then $Q^{op}$ is regular. Source: A2.6.3(i) in the [[Elephant]]. 
\end{example}

\begin{example}
The [[opposite category]] [[Top]]$^{op}$ is regular. The key facts are that [[regular monomorphisms]] in $Top$ are the same as [[subspace]] inclusions, and that the [[pushout]] of a subspace inclusion is a subspace inclusion as proven [there](subspace+topology#pushout). 
\end{example}

\begin{example}
The category of ([[Hausdorff space|Hausdorff]]) [[Kelley spaces]] is regular (but is not, however, locally cartesian closed, nor is it [[exact category|exact]]) ([Cagliari-Matovani-Vitale 95](#CagliariMatovaniVitale95)) 
\end{example}

\begin{example}
**(counter-examples)**
Examples of categories which are **not regular** include 

* [[Cat]], [[Pos]], and [[Top]]. 

The following example proves failure of regularity in all three cases: l

Let $A$ be the poset $\{a, b\} \times (0 \to 1)$; let $B$ be the poset $(0 \to 1 \to 2)$, and let $C$ be the poset $(0 \to 2)$. There is a regular epi $p: A \to B$ obtained by identifying $(a, 1)$ with $(b, 0)$, and there is the evident inclusion $i: C \to B$. The pullback of $p$ along $i$ is the inclusion $\{0, 2\} \to (0 \to 2)$, which is certainly an epi but not a regular epi. Hence regular epis in $Pos$ are not stable under pullback. 

Interpreting the posets as categories, the same example works for $Cat$, and also for preorders. On the other hand, the category of finite preorders is equivalent to the category of [[finite topological spaces]], so this example serves to show also that the category [[Top]] of *all* topological spaces is not regular. 
\end{example}

However: 

\begin{example}
\label{CompactlyGeneratedHausdorffSpacesAreRegular}
**(compactly generated Hausdorff spaces form a regular category)**
\linebreak
  The [[convenient category of topological spaces|convenient]] [[full subcategories]]
$$
  kTop
    \xhookrightarrow{\;} 
  kHaus
    \xhookrightarrow{\;}
  Top
$$
of 
[[compactly generated Hausdorff spaces]]
and of
[[compactly generated weakly Hausdorff spaces]] 
are regular 
([Cagliari, Matovani & Vitale 1995, p. 3](#CagliariMatovaniVitale95)).
\end{example}

\begin{example}
\label{CompactlyGeneratedGSpacesFormARegularCategory}
**(compactly generated $G$-spaces form a regular category)**
For $G \,\in\, Grp(kTop)$ a [[compactly generated weakly Hausdorff space|compactly generated weak Hausdorff]] [[topological group]], its category of [[internal actions]], hence the category of CGWH-[[topological G-spaces]] $G Act(kTop)$ is a regular category.
\end{example}
\begin{proof}
  The [[forgetful functor]] $G Act(kTop) \xrightarrow{\;} kTop$
[[created limit|creates]] all [[limits]] and [[colimits]] ([this Prop.](topological+G-space#ForgetfulFunctorCreatesLimitsAndColimits)). Since regularity is entirely a condition on limits and colimits ([this Def.](regular+category#RegularCategory)) the statement follows from Ex. \ref{CompactlyGeneratedHausdorffSpacesAreRegular}.
\end{proof}

\begin{example}
If $T$ is a [[Mal'cev theory]] (e.g., the theory of groups), then the category $Top^T$ of $T$-models in [[Top]] is regular. This is because for $T$ Mal'cev, coequalizer maps in $Top^T$ are necessarily open surjections, and open surjections are stable under pullback. 
\end{example}

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


### Pullback and pasting law

In a [[regular category]], the usual [[pasting law]] implication also applies along [[regular epimorphisms]] also in the reverse direction, :

\begin{proposition}
\label{WrongWayPastingLawInRegularCategory}
  In a [[regular category]], consider a [[commuting diagram]] of the form
\begin{tikzcd}
  {}
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  {}
  \ar[r]
  \ar[d]
  &
  {}
  \ar[d]
  \\
  {}
  \ar[r, ->>]
  &
  {}
  \ar[r]
  &
  {}  
\end{tikzcd}
where 

1. the left square is a [[pullback]];

1. the bottom left morphism is an [[regular epimorphism]].

Then right right square is a pullback iff the total rectangle is.
\end{proposition}
(e.g. [Gran 2020, Lem. 1.15](regular+category#Gran20))




### Factorization properties 


+-- {: .num_prop}
###### Proposition
**image factorization**

In a regular category, every morphism $f : x\to y$ can be factored -- uniquely up to [[isomorphism]] -- through its [[coimage]] $coim(f)$ as

$$
  f : x \stackrel{e}{\to} coim(f) \stackrel{i}{\to} y
  \,,
$$

where $e$ is a [[regular epimorphism]] and $i$ a [[monomorphism]]. 

=--

+-- {: .proof}
###### Proof

Let $e : x \to coim(f)$ be the [[coequalizer]] of the [[kernel pair]] of $f$. Since $f$ coequalizes its kernel pair, there is a unique map $i: coim(f) \to y$ such that $f = i e$. It may be shown from the regular category axioms that $i$ is monic and in fact represents the [[coimage]] of $f$, i.e., the smallest subobject through which $f$ factors.  

This is the mere definition of first isomorphism theorem.

A proof is spelled out on p. 30 of ([vanOosten](#vanOosten)).

=--


+-- {: .num_prop}
###### Proposition

The classes of [[regular epimorphism]], [[monomorphism]]s in a regular category $C$ form a [[orthogonal factorization system|factorization system]].

=--


### Embedding properties 

\begin{remark}
\label{barrembeddingtheorem}
If a regular category is small, it admits particularly nice embeddings into presheaf categories. See *[[Barr embedding theorem]]* for more. 
\end{remark}

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

The notion of regular categories was introduced in:

* {#BarrGrilletvonOsdol} [[Michael Barr]],  [[Pierre Grillet]], [[Donovan van Osdol]], *Exact Categories and Categories of Sheaves*,  Lec. Notes in Math. __236__, Springer 1971, ([doi:10.1007/BFb0058579](https://link.springer.com/book/10.1007/BFb0058579)) 
 
Historical context:

* [[Peter Johnstone]], Introduction of: _Topos Theory_ (1977)

Introduction:

* [[Carsten Butz]], _Regular Categories and Regular Logic_ , BRICS LS-98-2 Aarhus 1998. ([brics](http://www.brics.dk/LS/98/2/))

* {#Gran20} [[Marino Gran]], *An introduction to regular categories*, in: New Perspectives in Algebra, Topology and Categories,  Coimbra Mathematical Texts ([arXiv:2004.08964](https://arxiv.org/abs/2004.08964), [ISBN:978-3-030-84319-9](https://www.springerprofessional.de/en/new-perspectives-in-algebra-topology-and-categories/19764096))

Textbook accounts:

* [[Peter Freyd]], [[Andre Scedrov]], Chapter 1.5 of: _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990. (chap. 1.5. pp.68ff)

* {#Borceux94} [[Francis Borceux]], Chapter 2 of: *[[Handbook of Categorical Algebra]]*, Vol. 2: *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) ([doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865))

* [[Peter Johnstone]], Section A1.3. pp.18ff of _[[Sketches of an Elephant]] I_ , Oxford UP 2002. 

* [[Dominique Bourn]], [[Marino Gran]], _Regular, Protomodular, and Abelian Categories_, Chapter IV, pp.165-211 in: Maria Pedicchio, [[Walter Tholen]] (eds.), _Categorical Foundations_, Cambridge University Press 2004 ([doi:10.1017/CBO9781107340985.007](https://doi.org/10.1017/CBO9781107340985.007))



The following set of course notes has a section on regular categories 

* {#vanOosten}[[Jaap van Oosten]], _Basic category theory_ , BRICS LS-95-1 Aarhus 1995. ([Section 4.1](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf#page=30)) ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

An application of the regularity condition[^knop] is found in:

* F. Knop, _Tensor envelopes of regular categories_, ([arXiv:math/0610552v2](http://arxiv.org/abs/math/0610552))

[^knop]: Knop's condition for regularity is slightly different from that presented here; he works with categories that when augmented by an absolutely initial object are regular in the terminology here.  In the paper, Knop generalizes a construction of Deligne by showing how to construct a symmetric pseudo-abelian [[tensor category]] out of a regular category through the calculus of relations.

Generalization of the notion of regular categories to [[enriched category theory]]:

* [[Brian Day]], [[Ross Street]], _Localisation of locally presentable categories_, J. Pure and Appl. Algebra __58__ (1989) 227-233.

* Dimitri Chikhladze, _Barr's embedding theorem for enriched categories_, J. Pure Appl. Alg. __215__, n. 9 (2011) 2148-2153, [arxiv/0903.1173](http://arxiv.org/abs/0903.1173), [doi](http://dx.doi.org/10.1016/j.jpaa.2010.12.004)

Regularity of (Hausdorff) [[compactly generated topological spaces]]:

* {#CagliariMatovaniVitale95} F. Cagliari, S. Mantovani, [[Enrico Vitale]], *Regularity of the category of Kelley spaces*, Applied Categorical Structures volume 3, pages 357–361 (1995) ([doi:10.1007/BF00872904](https://link.springer.com/article/10.1007/BF00872904), [pdf](http://www.dm.unibo.it/~cagliari/articoli/Regularkelley.pdf))


[[!redirects regular categories]]
