
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 
  {#Idea}

In [[category theory]] and [[universal algebra]], a *monadicity theorem* serves to characterize/recognize whether a given [[functor]] is a [[monadic functor]].


## Statement

+-- {: .num_defn #CreationOfCoequalizersOfuSplitPairs}
###### Definition

Given a [[functor]] $U \colon D \rightarrow C$, then a [[parallel pair]] $f,g : a \rightarrow b$ in $D$ is called **$U$-split** if the pair $U f, U g$ has a [[split coequalizer]] in $C$.  Specifically, this means that there is a diagram in $C$: 

$$U a \;\underoverset{U f}{U g}{\rightrightarrows}\; U b \;\overset{h}{\rightarrow}\; c$$
such that $h \cdot U f = h \cdot U g$, and $h$ and $U f$ have respective [[sections]] $s$ and $t$ satisfying $U g \cdot t = s \cdot h$.  This implies that the arrow $h$ is necessarily a coequalizer of $U f$ and $U g$.  

The functor $U$ is said to *create coequalizers of $U$-split pairs* if for any such $U$-split pair, there exists a coequalizer $e$ of $f,g$ in $D$ which is preserved by $U$, and moreover any [[fork]] in $D$ whose image in $C$ is a split coequalizer must itself be a coequalizer (not necessarily split).

=--


\begin{theorem}
\label{BeckMonadicityTheorem}
**(Beck's monadicity theorem,  tripleability theorem)** 
\linebreak
A [[functor]] $U \colon D \rightarrow C$ is [[monadic]] (or tripleable) if and only if

1. $U$ has a [[left adjoint]], and

1. $U$ [[created limit|creates]] [[coequalizers]] of $U$-split pairs, def. \ref{CreationOfCoequalizersOfuSplitPairs}.

\end{theorem}

The proof is reproduced for instance in ([MacLane, p. 147-150](#MacLane), [Riehl 2017, 5/5/](#Riehl17)).


An equivalent, and sometimes easier, way to state these conditions is to say that

\begin{theorem}
\label{BeckMonadicityTheoremAlternative}
**(Beck's monadicity theorem -- alternative formulation)** 
\linebreak
A functor $U \colon D \to C$ is monadic precisely if

1. $U$ has a [[left adjoint]],

1. $U$ reflects [[isomorphisms]] (i.e. it is [[conservative functor|conservative]]), and

1. if for a [[parallel pair]] $(f,g)$ in $D$ the [[image]] $\big(U(f),\, U(g)\big)$ has a [[split coequalizer]] in $C$ then $(f,g)$ has a [[coequalizer]] in $D$ which is [[preserved colimit|preserved]] by $U$.

\end{theorem}

(e.g. [Borceux, vol 2, Thm. 4.4.4](#Borceux))

These conditions are equivalent to those in Thm. \ref{BeckMonadicityTheorem},
because a conservative functor [[reflected limit|reflects]] any limits or colimits which exist in its domain and which it [[preserved limit|preserves]] (by [this Prop.](conservative+functor#ConservativeFunctorsReflectLimitsWhichTheyPreserve)), while monadic functors are always conservative.

## Variants

### The crude monadicity theorem
 {#CrudeMonadicityTheorem}

The __crude monadicity theorem__ gives a *sufficient*, but not necessary, condition for a functor to be monadic.  It states that a functor $U : D \rightarrow C$ is [[monadic]] if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $D$ has and $U$ preserves coequalizers of [[reflexive coequalizer|reflexive pairs]].

(Recall that a parallel pair $f,g : a \rightarrow b$ is __reflexive__ if $f$ and $g$ have a common [[section]].)  This sufficient, but not necessary, condition is sometimes easier to verify in practice.  In contrast to the crude monadicity theorem, the necessary and sufficient condition above is sometimes called the __precise monadicity theorem__.

A further advantage of crude monadicity is this: while in general the composite of monadic functors need not be monadic, if $U_1\colon D \to C$ satisfies the hypotheses of the crude monadicity theorem and $U_2\colon C \to B$ is any monadic functor then $U_2 \circ U_1$ is monadic.   Furthermore, if both $U_1$ and $U_2$ both obey the hypotheses of the crude monadicity theorem, so does $U_2 \circ U_1$.  See ([BarrWells](#BarrWells), Proposition 3.5.1) for these and further results.  

### Duskin's monadicity theorem

Duskin's monadicity theorem gives a different sufficient, but not necessary, condition which refers only to quotients of [[congruences]].  


\begin{theorem}\label{DuskinMonadicityTheorem}
**(Duskin monadicity theorem)**
\linebreak
A functor $U \colon D \to C$ is [[monadic functor|monadic]] if

1. $U$ has a [[left adjoint]],

1. $D$ and $C$ are [[finitely complete category|finitely 
complete]],

1. $U$ [[created limit|creates]] [[coequalizers]] for [[congruences]] in $D$ whose [[images]] in $C$ have [[split coequalizers]].

\end{theorem}

We can weaken the hypothesis a bit further to obtain the theorem:

* A [[right adjoint]] between finitely complete categories is monadic if it creates [[quotients]] for [[congruences]].

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

### Actions over sets

\begin{example}
\label{BaseChangeOfPresheavesAlongFullyFaithfulFunctor}
**([[base change]] of [[presheaves]] along [[essentially surjective functor]])**
\linebreak
Let 
$$
  F 
    \,\colon\, 
  \mathcal{S} 
    \overset{\phantom{---}}{\longrightarrow}
  \mathcal{S}'
$$ 
be a [[functor]] between [[small categories]] which is [[essentially surjective]]. Then for $\mathcal{C}$ any [[bicomplete category]] (e.g. [[Set]]), the corresponding [[precomposition]]-functor on [[category of presheaves|categories of]] $\mathcal{C}$-valued [[presheaves]] 
\[
  \label{BaseChangeOfPresheavesAsMonadicFunctor}
  PSh
  \big(
    \mathcal{S}
    ;\,
    \mathcal{C}
  \big)
  \overset{\;\; F^\ast \;\;}{\longleftarrow}
  PSh
  \big(
    \mathcal{S}'
    ;\,
    \mathcal{C}
  \big)
\]

is [[monadic functor|monadic]]. To see this, we check the conditions in Thm. \ref{BeckMonadicityTheoremAlternative}:

1. By the assumption that $\mathcal{C}$ is [[bicomplete category|bicomplete]], the left and right [[Kan extensions]] of presheaves along $F$ exist and exhibit $F^\ast$ as the middle part of a ("[[base change]]") [[adjoint triple]] :

   $$
     F_! \,\dashv\, F^\ast \,\dashv\, F_\ast
     \;\;
     \colon
     \;\;
     PSh
     \big(
       \mathcal{S}
       ;\,
       \mathcal{C}
     \big)
     \overset{\phantom{----}}{\leftrightarrow}
     PSh
     \big(
       \mathcal{S}'
       ;\,
       \mathcal{C}
     \big)
     \,.
   $$

   This shows that $F^\ast$ has a left adjoint. In addition, it *is* a left adjoint and [[left adjoints preserve colimits|as such preserves all colimits]], hence in particular all [[coequalizers]].

1. The assumption that $F$ is [[essentially surjective functor|essentially surjective]] implies that $F^\ast$ is [[conservative functor|conservative]] (because [[isomorphisms]] of presheaves are [[natural transformation]] of the underlying functors which are [[natural isomorphisms]], which is the case iff their component [[morphisms]] for each [[object]] is an isomorphism.)

\end{example}



\begin{example}\label{GroupActions}
**([[group actions]]/[[G-sets]])**
\linebreak
Specializating Ex. \ref{BaseChangeOfPresheavesAlongFullyFaithfulFunctor} to the case (where $\mathcal{C} = $ [[Sets]], just for definiteness and) where $F \,\colon\,\mathcal{S} \longrightarrow \mathcal{S}'$ is the [[terminal category|point]]-inclusion
$$
  pt_{\mathbf{B}G}
  \,\colon\,
  \ast 
  \overset{\phantom{---}}{\hookrightarrow}
  \mathbf{B}G
  \,.
$$
into the [[delooping groupoid]] of a ([[discrete group|discrete]]) [[group]], and observing that 

1. $PSh\big(\ast \big) \;\simeq\;$ [[Sets]],

1. $PSh\big(\mathbf{B}G \big) \;\simeq\;$ [[G-set|$G$Sets]]

   is the category [[G-sets]], i.e. of $G$-[[group actions]] with [[equivariant functions]] between them,

gives that (eq:BaseChangeOfPresheavesAsMonadicFunctor) is the [[forgetful functor]]

$$
  (pt_{\mathbf{B}G})^\ast
  \,\colon\,
  G Sets \overset{\phantom{--}}{\longrightarrow} Sets
$$

which is hence [[monadic functor|monadic]]. This is of course the [[forgetful functor]] on the [[algebra over a monad|algebras]] of the [[monad]]

$$
  T \,\coloneqq\, G \times (-)
  \;\colon\;
  Sets \longrightarrow Sets
$$

which forms the [[Cartesian product]] with (the [[underlying]] [[set]]) of $G$, and whose monad product is 

$$
  T \circ T 
    \,=\, 
  G \times G \times (-)
  \longrightarrow 
  G \times (-)
    \,=\,
  T
$$

is given by the group operation.
\end{example}

\begin{example}\label{MonoidActions}
**([[monoid actions]] and monoid-oid actions)**
\linebreak
In generalization of Ex. \ref{GroupActions}, if $A$ is a [[monoid]] and $F \,\colon\, \mathcal{S} \longrightarrow \mathcal{S}'$ in Ex. \ref{BaseChangeOfPresheavesAlongFullyFaithfulFunctor} is the point inclusion 
$$
  pt \,\colon\,\ast \longrightarrow \mathbf{B}A
$$ 
into the corresponding 1-object category (see [there](monoid#AsAOneObjectCategory)), then the monadic functor (eq:BaseChangeOfPresheavesAsMonadicFunctor)

$$
  (pt_{\mathbf{B}A})^\ast
  \;\colon\;
  A Sets \longrightarrow Sets
$$
is the [[forgetful functor]] on [[monoid actions]], which are the [[algebra over a monad|algebras]] of the monad $A \times (-)$.

In this sense, the general situation of Ex. \ref{BaseChangeOfPresheavesAlongFullyFaithfulFunctor} may be understood as monadicity of [[modules]] for a [monoid-oid](horizontal+categorification#Monoidoid) $\mathcal{S}'$ defined over a [monoid-oid](horizontal+categorification#Monoidoid) $\mathcal{S}$.
\end{example}


### Groups over sets
 {#GroupsOverSets}

We will use Duskin's monadicity theorem (Thm. \ref{DuskinMonadicityTheorem}) to prove that the [[forgetful functor]] 
$$
  U
  \,\colon\,
  Grps
  \overset{\phantom{---}}{\longrightarrow}
  Sets
$$

from [[Groups]] to their underlying [[Sets]] is [[monadic functor|monadic]].  
Of course, this is also easy to show by explicit computation, but it serves as a useful example of how to use a monadicity theorem.  

We first need it to have a [[left adjoint]]: this is easy to show by a direct construction of [[free groups]], but we could also invoke the [[adjoint functor theorem]].  

It is also easy to show that it is [[conservative functor|conservative]] (a [[bijection|bijective]] [[group homomorphism]] is a group isomorphism).

So it remains to consider congruences:

Since [[limits]] in $Grp$ are [[created limit|created]] in $Set$, a [[congruence]] in $Grp$ on a group $G$ is an [[equivalence relation]] on $G$ which is also a [[subgroup]] of $G\times G$.  This latter condition means that if $g_1\sim g_2$ and $h_1\sim h_2$, then also $g_1^{-1}\sim g_2^{-1}$ and $g_1 h_1 \sim g_2 h_2$.  Since $g\sim g$ for all $g$, it follows that $g\sim h$ if and only if $1\sim h g^{-1}$, so $\sim$ is determined by the subset $H\subseteq G$ of those $h\in G$ such that $1\sim h$.  This $H$ is clearly a [[subgroup]] of $G$, and moreover a [[normal subgroup]], since if $h\in H$ and $g\in G$ we have $1 = g^{-1} g \sim g^{-1} h g$, so $g^{-1} h g\in H$.  Conversely, it is easy to construct a congruence from any normal subgroup, so the two notions are equivalent.  It remains only to observe that the quotient of a group by a normal subgroup is, in fact, a quotient of its associated congruence in $Grp$, which is preserved by $U$.  

Thus, by Duskin's monadicity theorem (Thm. \ref{DuskinMonadicityTheorem}), $U$ is monadic.


### Categories over computads

The monadicity theorem becomes more important when the base category $C$ is more complicated and harder to work with explicitly, and when the objects of $D$ are not obviously defined as "objects of $C$ with extra structure."  For instance, the category of [[strict 2-categories]] is monadic over the category of 2-[[globular sets]], essentially by definition, but it is much less trivial to show that it is *also* monadic over the category of [[2-computads]].  This latter fact can, however, be proven using the monadicity theorem.

### Monadic descent

The monadicity theorem also plays a central role in [[monadic descent]].

## In $(\infty,1)$-categories
 {#InInfinityCategories}

There is a version of the monadicity theorem for [[(∞,1)-monads]] in [section 3.4](http://arxiv.org/PS_cache/math/pdf/0702/0702299v5.pdf#page=107) of

* [[Jacob Lurie]], _Noncommutative algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))

There is also a 2-categorical approach using quasicategories in

* [[Emily Riehl]], [[Dominic Verity]] _The 2-category theory of quasi-categories_ ([arXiv](http://arxiv.org/abs/1306.5144)), _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv](http://arxiv.org/abs/1310.8279))


## Related concepts

* [[monadic functor]], [[comonadic functor]]

* [[functor of descent type]]

* [[monadic decomposition]]

* [[Bénabou-Roubaud's theorem]]

* [[monadic descent]]



## References

The original reference for the (crude and precise) monadicity theorems is an untitled manuscript of [[Jon Beck]] that was distributed around 1966 -- 1968. The following is a scan of a copy distributed at the *Conference Held at the Seattle Research Center of the Battelle Memorial Institute* in June -- July 1968, provided by John Kennison:

* {#Beck68} [[Jon Beck]], untitled manuscript, 1968 ([[Beck_MonadicityTheorem.pdf:file]])

see also:

* [[Michael Barr]], *Coalgebras in a category of algebras*, in: *Category Theory, Homology Theory and their Applications I*, Lecture Notes in Mathematics **86**, Springer (1969) 1-12 &lbrack;[doi:10.1007/BFb0079381](https://doi.org/10.1007/BFb0079381)&rbrack;

Textbook accounts:

* {#MacLane71} [[Saunders MacLane]], §VI.7 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Borceux} [[Francis Borceux]], Section 4 in volume 2 of  _[[Handbook of Categorical Algebra]]_, in 3 vols. 


* {#BarrWells} Chapter 3 of [[Michael Barr]], [[Charles Wells]], _[[Toposes, Triples, and Theories]]_  Grundlehren der math. Wissenschaften 278, Springer-Verlag 1983.  Available as [TAC Reprint 12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html).

Further references:


* [[FGA explained]], [[SGA 1]], 


* [[Fred Linton]], _Some aspects of equational categories_, Proceedings of the Conference on Categorical Algebra. Springer 1966.


* {#BenabouRoubaud70} [[Jean Bénabou]], [[Jacques Roubaud]], _Monades et descente_, C. R. Acad. Sc. Paris, Ser. A **270**  (1970) 96-98 &lbrack;[gallica:12148/bpt6k480298g/f100](http://gallica.bnf.fr/ark:/12148/bpt6k480298g/f100), [[BenabouRoubaud-MonadesEtDescente.pdf:file]],   English translation (by [[Peter Heinig]]): [MO:q/279152](https://mathoverflow.net/q/279152)&rbrack;


* [[Duško Pavlović]], Categorical interpolation: descent and the Beck-Chevalley condition without direct images,  Category theory Como 1990, pp. 306--325, Lecture Notes in Mathematics 1488, Springer 1991

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_ , Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp. 111-195.

* Wikipedia: [monadicity theorem](http://en.wikipedia.org/wiki/Beck%27s_monadicity_theorem)

* John Bourke, _Two dimensional monadicity_, [arxiv/1212.5123](http://arxiv.org/abs/1212.5123)


* {#Riehl17} [[Emily Riehl]], §5.5 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/context.pdf), [book website](http://www.math.jhu.edu/~eriehl/context/)&rbrack;
  

There is a version for [[Morita contexts]] instead of monads:

* [[Tomasz Brzezinski]], Adrian Vazquez Marquez, Joost Vercruysse, _The Eilenberg-Moore category and a Beck-type theorem for a Morita context_, Appl. Categ. Structures __19__ (2011), no. 5, 821&#8211;858 [MR2836546](http://www.ams.org/mathscinet-getitem?mr=2836546) [doi](http://dx.doi.org/10.1007/s10485-009-9217-0)

On Beck's theorem for [[pseudomonads]] ([[higher monadic descent]]):

* I. J. Le Creurer, [[Francisco Marmolejo]], [[Enrico M. Vitale]], _Beck's theorem for pseudo-monads_, J. Pure Appl. Algebra **173** 3 (2002) 293-313 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00038-5">doi:10.1016/S0022-4049(02)00038-5</a>&rbrack;


Discussion for [[(infinity,1)-monads]]:

* [[Jacob Lurie]], section 4.7 of _[[Higher Algebra]]_

and realized in the context of [[quasi-categories]]:

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], section 7.2 of _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 

[[!redirects monadicity theorems]]

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