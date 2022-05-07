
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
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

The notion of a [[category]] can be formulated [[internalization|internal]] to any other category with enough [[pullback|pullbacks]]. 

By regarding [[group|groups]] as [[pointed object|pointed]] [[n-connected object of an (infinity,1)-topos|connected]] ([[delooping]]) [[groupoid|groupoids]], this generalizes the notion of [[internal groups]].

An ordinary [[small category]] is a category internal to [[Set]].

There is a more general notion of an [[internal category in a monoidal category]], where the [[pullbacks]] are replaced by cotensor products.

## Definition

### Internal category

Let $A$ be a [[category]] with [[pullbacks]]. A **category internal to $A$** consists of 

* an [[object]] _of objects_ $C_0 \in A$;

* an [[object]] _of morphisms_ $C_1 \in A$;

together with

* [[source]] and [[target]] [[morphisms]] $s,t: C_1 \to C_0$;

* an [[identity-assigning morphism]] $e: C_0 \to C_1$;

* a [[composition]] morphism $c: C_1 \times_{C_0} C_1 \to C_1$;


such that the following [[diagrams]] [[commuting diagram|commute]], expressing the usual category laws:

* laws specifying the source and target of identity morphisms:

$$
\array{
C_0 & \stackrel{e}{\to} & C_1 \\
{}  & 1\searrow         & \darr s \\
{}  & {}                & C_0
}
\quad\quad\quad\quad
\array{
C_0 & \stackrel{e}{\to} & C_1 \\
{}  & 1\searrow         & \darr t \\
{}  & {}                & C_0
}
$$

* laws specifying the source and target of composite morphisms:

$$
\array{
C_1 \times_{C_0} C_1 & \stackrel{c}{\to} & C_1 \\
{}^{p_1}\downarrow   & {}                & \downarrow^{s} \\
C_1                  & \stackrel{s}{\to} & C_0
}
\quad\quad\quad\quad
\array{
C_1 \times_{C_0} C_1 & \stackrel{c}{\to} & C_1 \\
{}^{p_2}\downarrow   & {}                & \downarrow^{t} \\
C_1                  & \stackrel{t}{\to} & C_0
}
$$

* the associative law for composition of morphisms:

$$
\array{
C_1 \times_{C_0} C_1 \times_{C_0} C_1 & \stackrel{c\times_{C_0} 1}{\to} & C_1 \times_{C_0} C_1 \\
{}^{1\times_{C_0}c}\downarrow         & {}                              & \downarrow^{c} \\
C_1 \times_{C_0} C_1                  & \stackrel{c}{\to}               & C_1
}
$$

* the left and right unit laws for composition of morphisms:

$$
\array{
C_0 \times_{C_0} C_1  & \stackrel{e \times_{C_0} 1}{\to} &
 C_1 \times_{C_0} C_1 & \stackrel{1 \times_{C_0} e}{\leftarrow} & C_1 \times_{C_0} C_0 \\
{}                    & {}^{p_2}\searrow                 & \downarrow^{c}       & \swarrow^{p_1}                          & {} \\
{}                    & {}                               & C_1                  & {}                                      & {}
}
$$

Here, the [[pullback]] $C_1 \times_{C_0} C_1$ is defined via the square
$$
\array{
C_1 \times_{C_0} C_1 & \stackrel{p_2}{\to} & C_1 \\
{}^{p_1}\downarrow   & {}                  & \downarrow^{s} \\
C_1                  & \stackrel{t}{\to}   & C_0
}
$$

Notice that inherent to this definition is the assumption that the [[pullbacks]] involved actually exist. This holds automatically when the [[ambient category]] $A$ has finite [[limit|limits]], but there are some important examples such as $A =\,$ [[Diff]] where this is not the case.  Here it is helpful to assume simply that $s$ and $t$ have all [[pullbacks]]; in the case of $Diff$ this occurs if they are submersions.

### Internal groupoid

A [[groupoid]] internal to $A$ is all of the above 

 * with a morphism
  $$
     C_1 \stackrel{i}{\to} C_1
  $$

 * such that
  $$
t = ( C_1 \stackrel{i}{\to} C_1 \stackrel{s}{\to} C_0 ),\;\;\;\;
s = ( C_1 \stackrel{i}{\to} C_1 \stackrel{t}{\to} C_0 ).
  $$

 * and
   $$
     \array{
     C_1 &\stackrel{diag}{\to}& C_1\;{}_t \times_{C_0}{}_t C_1 &\stackrel{Id \times i}{\to}& C_1\;{}_t \times_{C_0}{}_s C_1
     \\
     \downarrow^s &&&& \; \downarrow^c
     \\
     C_0 &&\stackrel{e}{\to}&& C_1
     }
   $$

 * and
   $$
     \array{
     C_1 &\stackrel{diag}{\to}& C_1\;{}_s \times_{C_0}{}_s C_1 &\stackrel{i \times Id}{\to}& C_1\;{}_t \times_{C_0}{}_s C_1
     \\
     \downarrow^t &&&& \; \downarrow^c
     \\
     C_0 &&\stackrel{e}{\to}&& C_1
     }
   $$

### Internal functors

[[functor|Functors]] between internal categories are defined in a similar fashion. See [[functor]].  But if the ambient category does not satisfy the [[axiom of choice]] it is often better to use [[anafunctor|anafunctors]] instead; this makes sense when $C$ is a [[superextensive site]].


### Alternative definition

If $A$ has all [[pullbacks]], then we can form the bicategory $Span(A)$ of [[span|spans]] in $A$.  A category in $A$ is precisely a [[monad]] in $Span(A)$.  The underlying 1-cell is given by the span $(s,t) : C_0 \leftarrow C_1 \to C_0$, and the [[pullback]] $C_1 \times_{C_0} C_1$ is the vertex of the composite span $(s,t) \circ (s,t)$.  The morphisms $e$ and $c$ are required to be morphisms of spans, which is equivalent to imposing the source and target axioms above.  Finally the unit and associativity axioms for monads imply those above.

This approach makes it easy to define the notion of [[internal profunctor]].

### Internal nerve

The notion of [[nerve]] of a [[small category]] can be generalised to give an *internal nerve* construction. For a small category, $D$, its [[nerve]], $N(D)$, is a simplicial set whose set of $n$-simplices is the set of sequences of composable morphisms of length $n$ in $D$. This set can be given by a (multiple) [[pullback]] of copies of $D_1$.  That description will carry across to give a nerve construction for an internal category.  

If $C$ is an internal category in some category $A$, (which thus has, at least, the [[pullbacks]] required for the constructions to make sense),its nerve $N(C)$ (or if more precision is needed $N_{int}(C)$, or similar) is the [[simplicial object]] in $A$ with 

 * $N(C)_0 = C_0$, the 'object of objects' of $C$;
 * $N(C)_1  = C_1$, the 'object of arrows' of $C$;
 * $N(C)_2 = C_1 \times_{C_0} C_1$ the object of [[composable pairs]] of arrows of $C$;
* $N(C)_3 = C_1 \times_{C_0} C_1\times_{C_0} C_1$, the object of composable triples of arrows;

and so on.  Face and degeneracy morphisms are induced from the structural moprhisms of $C$ in a fairly obvious way.

Internal functors between internal categories induce simplicial morphisms between the corresponding nerves.

### Internal category in homotopy type theory

Discussion in [[homotopy type theory]] is at _[[internal category in homotopy type theory]]_.

### Higher internal categories

One can also look at this in [[higher category theory]] and consider internal [[n-category|n-categories]]. See

* [[n-fold category]]

* [[internal infinity-groupoid]]

* [[internal (infinity,1)-category]]

* [[internal (infinity,n)-category]]

The general concept is that of an [[n-by-k category|$(n \times k)$-category]], which is an $n$-category internal to a $k$-category.


## Examples

A [[small category]] is a category internal to [[Set]].  In this case, $C_0$ is a set of objects and $C_1$ is a set of morphisms and the [[pullback]] is a [[subset]] of the [[Cartesian product]].

Historically, the motivating example was (apparently) the notion of [[Lie groupoids]]: a small Lie groupoid is a [[groupoid]] internal to the category [[Diff]] of [[smooth manifolds]]. This generalises immediately to a [[smooth category]]. Similarly, a [[topological groupoid]] is a groupoid internal to [[Top]]. (Warning: the term 'topological category' usually means a [[topological concrete category]], an unrelated notion. Sometimes a 'topological category' is defined to be a $Top$-[[enriched category]], which is a special case of the internal definition if it is interpreted [[strict category|strictly]] and the collection of objects is small.)  In these examples, $C_0$ is a "space of objects" and $C_1$ a "space of morphisms".

Further examples:

* A category internal to [[Set]] is a [[small category]]
* A groupoid internal to [[definable sets]] is a [[definable groupoid]].

* A groupoid internal to a [[category of presheaves]] is a [[presheaf of groupoids]].

* A groupoid internal to the [[opposite category|opposite]] of [[CRing]] is a [[commutative Hopf algebroid]].

* A pointed one-object category internal to [[Ho(Top)]] is an [[H-monoid]].

* A pointed one-object groupoid internal to [[Ho(Top)]] is an [[H-group]]. 

* A [[cocategory]] in $C$ is a category internal to $C^{op}$.
* A [[double category]] is a category internal to [[Cat]]. 
* A [[double bicategory]] is a category internal to [[Bicat]] (in a suitably weak sense).
* A [[crossed module]] is equivalent to a category internal to [[Grp]].
* A [[Baez-Crans 2-vector space]] is a category internal to [[Vect]].


* A [[2-group]] is an internal category in [[Grp]] and so has an internal nerve, which is a simplicial object in [[Grp]], that is  a [[simplicial group]].  If the 2-group corresponds to a [[crossed module]], $(C\stackrel{\delta}{\to}P)$, then the simplicial group nerve of $(C\stackrel{\delta}{\to}P)$ has [[Moore complex]] having $P$ in dimension 0, and $C$ in dimension 1, with the trivial group in all other dimensions. The only possible non-trivial boundary map from dimension 1 to dimension 0 is then the boundary $\delta$ of the crossed module. 

## Properties
 {#Properties}

### In a cartesian closed category
 {#CartesianClosure}

If the ambient (finitely complete) category $\mathbf{E}$ is a [[cartesian closed category]], then the category $Cat(\mathbf{E})$ of categories internal to $\mathbf{E}$ is also cartesian closed. This was [proved](#BastianiEhresmann_69) [twice](#BastianiEhresmann_72) by [[Ehresmann|Charles]] and [[Andree Ehresmann|Andrée]] (under her maiden name Bastiani) Ehresmann using generalised sketches, or may be proven directly as follows (see also [Johnstone, remark after B2.3.15](#Johnstone)): 

+-- {: .num_theorem} 
###### Theorem 
Let $\mathbf{E}$ be a finitely complete cartesian closed category. Then the category $Cat(\mathbf{E})$ of internal categories in $E$ is also finitely complete and cartesian closed. 
=-- 

+-- {: .proof} 
###### Proof 
First suppose $\mathbf{E}$ is finitely complete. Then the category of directed graphs $\mathbf{E}^{\bullet \stackrel{\to}{\to} \bullet}$ is also finitely complete, and since $Cat(\mathbf{E})$ is monadic over $\mathbf{E}^{\bullet \stackrel{\to}{\to} \bullet}$, it follows that $Cat(\mathbf{E})$ is also finitely complete. 

Now suppose that $\mathbf{E}$ is finitely complete and cartesian closed. Let $\Delta_3$ denote the category of nonempty ordinals up to and including the ordinal with 4 elements. We have a full and faithful embedding 

$$N \colon Cat(\mathbf{E}) \to \mathbf{E}^{\Delta_3^{op}}$$ 

where the codomain category is cartesian closed. Indeed, the exponential of two objects $F$, $G$ in $\mathbf{E}^{\Delta_3^{op}}$ may be computed as an $\mathbf{E}$-enriched end 

$$G^F(m) = \int_n \prod_{f \colon n \to m} G(n)^{F(n)}$$ 

when evaluated at $m \in Ob(\mathbf{E}^{\Delta_3^{op}})$, as is easily checked (see for instance [here](http://ncatlab.org/nlab/show/cartesian+closed+category#exponentials_of_cartesian_closed_categories_30)); note that this end is a finite limit diagram since $\Delta_3$ is finite.  

If $C$, $D$ are internal categories in $\mathbf{E}$, seen as functors $\Delta_3^{op} \to \mathbf{E}$, the exponential $N C^{N D}$ defines the exponential in $Cat(\mathbf{E})$. To see this, it suffices to check that $N C^{N D}$, as defined by the end formula above, is a category $B$, i.e., is in the essential image of the nerve functor. For in that case, we have natural isomorphisms 

$$\frac{ 
\frac{F \times D \to C \;\;\;\text{in}\; Cat(\mathbf{E})}
{N F \times N D \cong N(F \times D) \to N C \;\;\;\text{in}\; \mathbf{E}^{\Delta_3^{op}}}}
{\frac{N F \to N C^{N D} \;\;\;\text{in}\; \mathbf{E}^{\Delta_3^{op}}}
{F \to B \;\;\;\text{in}\; Cat(\mathbf{E})}}$$ 

whence $B$ satisfies the universal property required of an exponential. 

Objects in the essential image of the nerve $N$ are characterized as functors $\Delta_3^{op} \to \mathbf{E}$ which take intervalic joins in $\Delta_3$ to [[pullbacks]] in $\mathbf{E}$, as given precisely by the [[Segal conditions]]. The remainder of the proof is then finished by the following lemma. 
=-- 

+-- {: .num_lemma} 
###### Lemma 
If $C \colon \Delta_3^{op} \to \mathbf{E}$ satisfies the [[Segal conditions]] and $X \colon \Delta_3^{op} \to \mathbf{E}$ is any functor, then $C^X$ also satisfies the Segal conditions. 
=-- 

+-- {: .proof} 
###### Proof 
For any $X$ we have the formula 

$$C^X(m) = \int_k Hom(X k, \prod_{f \colon n \to k} \prod_{g \colon n \to m} C(n)).$$ 

Since the enriched [[end]] and the internal hom-functor $Hom(X k, -)$ both [[preserved limit|preserve]] [[pullbacks]], we are reduced to checking that 

* If $C$ satisfies the [[Segal conditions]], then so does 
$$\prod_{f \colon n \to k} \prod_{g \colon n \to m} C(n)$$ 
as a functor $\Delta_3^{op} \to \mathbf{E}$ in the argument $m$ (for each fixed $k$). 

Note that the displayed statement is a proposition in the language of finitely complete categories (i.e., in finitary essentially algebraic logic). Since hom-functors $\mathbf{E}(e, -) \colon \mathbf{E} \to Set$ jointly preserve and reflect the validity of such propositions, it suffices to prove it for the case where $\mathbf{E} = Set$. But this is classical elementary category theory; it says precisely that if $C$ is a small (ordinary) category, then the usual functor categories $C^{\mathbf{2}}$, $C^{\mathbf{3}}$ are equivalently described by exponentials of (truncated) simplicial sets. This completes the proof. 
=-- 

### In a topos
 {#InATopos}

If the ambient category is a [[topos]], then with the right kind of notion of internal functor, the internal groupoids form the corresponding [[(2,1)-topos]] of [[groupoid]]-valued stacks and the internal categories form the corresponding [[2-topos]] of [[category]]-valued stacks/[[2-sheaves]].

For the precise statement see at _[2-topos -- In terms of internal categories](2-topos#InTermsOfInternalCategories)_

## Internal versus enriched categories
 {#InternalAndEnrichedCategories}

It is useful to contrast the notion of [[internal category]] with that of [[enriched category]], each of which may be considered as a generalization according to whether categories are [defined](category#definitions) (i) by a single collection of all morphisms or (ii) by a family of collections indexed by pairs of objects. In some cases, one of these generalizations is a special case of the other, but in general they are incomparable.

As described there, [[internalization]] is a quite general phenomenon, of which [[internal categories]] are a particular case. However, the distinction between "internalization" and "enrichment" becomes less clear in generality.  For example, in addition to categories enriched over a monoidal category, one can define categories enriched over a [[bicategory]] or an [[virtual double category]]. It then turns out that a category enriched over the bicategory (or virtual double category) of [[span|spans]] in a lex category $C$ _which has one object_ is precisely an _internal_ category in $C$.


## Related concepts

* [[weak equivalence of internal categories]]

* [2-Topos -- In terms of internal categories](2-topos#InTermsOfInternalCategories)

  * [[2-sheaf]]

  * [[2-congruence]]

* [[(n × k)-category]]

* [[internal site]]

* [[internal logic]]

* [[enriched category]]

* [[locally internal category]]



## References

Survey and introduction with an eye towards [[Lie theory]]:

* [[Jean Pradines]], _In [[Ehresmann]]'s footsteps: from Group Geometries to Groupoid Geometries_, Banach Center Publications, vol. 76, Warsawa 2007, 87-157 ([arXiv:0711.1608](http://arxiv.org/abs/0711.1608), [doi:10.4064/bc76-0-5 ](https://www.impan.pl/en/publishing-house/banach-center-publications/all/76/0/86184/in-ehresmann-s-footsteps-from-group-geometries-to-groupoid-geometries))

* [[John Baez]], [[Alissa Crans]], _[Higher-Dimensional Algebra VI: Lie 2-Algebras](http://arxiv.org/abs/math/0307263)_

Textbook accounts:

* [[Francis Borceux]], Chapter 8 in Vol 1 _Basic Category Theory_ of: _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)  ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

and with emphasis on [[topos theory]]:

* {#Johnstone} [[Peter Johnstone]], section B.2.3 of: _[[Sketches of an Elephant]]_
 
* [[Saunders MacLane]], [[Ieke Moerdijk]], section V.7 of: _[[Sheaves in Geometry and Logic]]_

The original concept of [[topological groupoids]] and [[Lie groupoids]] goes back to

* [[Charles Ehresmann]], _Catégories topologiques et categories différentiables_, Colloque de Géométrie différentielle globale, Bruxelles, C.B.R.M., (1959) pp. 137-150 ([[EhresmannCategoriesTopologiques.pdf:file]], [zbMath:0205.28202](https://zbmath.org/?q=an:0205.28202))

and their understanding as categories internal to [[TopologicalSpaces]] and to [[SmoothManifolds]] may originate around:

* [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure, Série 3, Tome 80 (1963) no. 4, pp. 349-426 ([numdam:ASENS_1963_3_80_4_349_0](http://www.numdam.org/item/ASENS_1963_3_80_4_349_0))

The original proofs that the category of internal categories is [[cartesian closed category|cartesian closed]] when the ambient category is [[finitely complete category|finitely complete]] and [[cartesian closed category|cartesian closed]] are in

* {#BastianiEhresmann_69} [[Andrée Bastiani]], [[Charles Ehresmann]], _Catégories de foncteurs structurés_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, 11 no. 3 (1969), p. 329-384 ([numdam:CTGDC_1969__11_3_329_0](http://www.numdam.org/item?id=CTGDC_1969__11_3_329_0))
 

and in 

* {#BastianiEhresmann_72} [[Andrée Bastiani]], [[Charles Ehresmann]], _Categories of sketched structures_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 13 no. 2 (1972), p. 104-214 ([Numdam](http://www.numdam.org/item?id=CTGDC_1972__13_2_104_0))


Discussion in terms of [[monads]] in [[spans]] is in 

* Renato Betti, _Formal theory of internal categories_, Le Matematiche Vol. LI (1996) Supplemento 35-52 [pdf](http://www.dmi.unict.it/ojs/index.php/lematematiche/article/view/456/427)

A detailed discussion with emphasis on the correct [[anafunctor]] morphisms between internal categories is in 

* [[David Roberts]], _Internal categories, anafunctors and localisations_, [[Theory and Applications of Categories]], Vol. 26, 2012, No. 29, pp 788-829, [journal version](http://www.tac.mta.ca/tac/volumes/26/29/26-29abs.html), [arXiv:1101.2363](http://arxiv.org/abs/1101.2363)
 

An old discussion on variants of internal categories, crossed modules and 2-groups is archived [here](http://nforum.mathforge.org/discussion/621/internal-category/?Focus=29967#Comment_29967).

[[!redirects internal categories]]
[[!redirects internal groupoid]]
[[!redirects internal groupoids]]
[[!redirects category internal]]
[[!redirects categories internal]]
[[!redirects groupoid internal]]
[[!redirects groupoids internal]]

[[!redirects category object]]
[[!redirects category objects]]
[[!redirects internal nerve]]