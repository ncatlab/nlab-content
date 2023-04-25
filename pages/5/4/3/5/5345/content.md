

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


Before we start, beware the usual terminology issue with "[[simplicial groupoids]]":

\begin{remark}
**(terminology)**
This entry is concernd with  _[[simplicial groupoids]]_ as traditionally understood (following [Dwyer & Kan (1984)](#DwyerKan84)), referring to [[simplicial objects]] in the [[category]] [[Grpd]] of [[groupoids]] with the special property that their [[simplicial set]] of objects is simplicially constant. Any such "Dwyer-Kan simplicial groupoid" is equivalently an [[sSet-enriched category]] that is a [[groupoid]] in the [[enriched category theory|enriched]] sense: an *[[sSet]]-[[enriched groupoid]]*. Therefore, and since in applications it is often this [[sSet]]-[[enriched category|enriched]] [[structure]] which matters, a more accurate term would be *simplicially enriched groupoids*, but this terminology is not at all standard. See the corresponding discussion at *[[simplicial groupoid]]* ([here](simplicial+groupoid#Definition)).
\end{remark}


## Definition

Write $sGrpd_{DK}$ for the [[category]] of [[simplicial groupoids]] (whose [[simplicial sets]] of [[objects]] are understood to be constant, see the discussion [there](simplicial+groupoid#Definition)).

\begin{definition}\label{FreeMorphismsOfSimplicialGroupoids}
**(free morphisms of simplicial groupoids)**
\linebreak
  Say that a [[morphism]] $f \colon X \to Y$ of [[simplicial groupoids]] is *free* iff:

1. it is degreewise [[injective]] (i.e. on the [[sets]] of [[objects]] and on the sets of [[morphisms]] in each degree);

1. there is a [[subset]] $\Gamma \subset Y$ of [[morphisms]] in $Y$ (of any degree) with the following properties:

   1. $\Gamma$ contains no [[identity morphisms]];

   1. $\Gamma$ is closed under forming degenerate cells;

   1. every non-[[identity morphism]] in $Y$ is *uniquely* a [[composition]] of those sequences of morphisms in $\Gamma$ and their [[inverse morphisms|inverses]] which are *reduced* in that:

      1. no morphism in the sequences is consecutive with its [[inverse morphisms|inverse]],

      1. no two non-[[identity morphisms]] in the [[image]] of $f$ are consecutive.
\end{definition}
&lbrack;[Dwyer & Kan 1984, §2.3](#DwyerKan84)&rbrack;


\begin{proposition}\label{TheModelStructure}
**(Dwyer-Kan model structure on simplicial groupoids)**
\linebreak
There is a [[model category]] structure on $sGrpd_{DK}$ whose

* [[weak equivalences]] are the [Dwyer-Kan equivalences](model+structure+on+sSet-categories#DwyerKanEquivalences), hence those morphisms $f \colon H \to K$ such that

  1. $f$ induces in [[isomorphism]] on [[connected components]] $\pi_0 f \colon \pi_0 H \to \pi_0 K$;

  1. for each object $x$ of $H$ the induced morphism $H(x,x) \to K(f(x), f(x))$ is a weak equivalence in the [[model structure on simplicial groups]] or equivalently in the [[classical model structure on simplicial sets]].

* [[fibrations]] are the "[[essentially surjective (infinity,1)-functor|essentially surjective]] [[iso-fibrations]]", namely those morphisms $f \colon H \to K$ such that 

  1. for every [[object]] $x$ of $H$ and every [[morphism]] $\omega \colon f(x) \to y$ in $K_0$ there is a morphism $\hat \omega : x \to z$ of $H_0$ such that $f(\hat \omega) = \omega$;

  1. for every object $x$ in $H$ the induced morphism $f \colon H(x,x) \to K(f(x), f(x))$ is a [[Kan fibration]].

* [[cofibrations]] are the [[retracts]] (in the [[arrow category]]) of the free maps from Def. \ref{FreeMorphismsOfSimplicialGroupoids}.

\end{proposition}

This is due to [Dwyer & Kan (1984), §1.1, §1.2, Thm. 2.5](#DwyerKan84), reviewed in [Goerss & Jardine (2009), p. 316 and after cor V.7.3](#GoerssJardine09).

\begin{remark}\label{RelationToModelStructureOnSimplicialGroups}
**(relation to model structure on simplicial groups)**
\linebreak
  An $X \in sGrpd_{DK}$ for which $X_0 = \ast$ is the [[terminal groupoid]] is, when regarded as a [[pointed object]], equivalently the ([[delooping]] of the) [[simplicial group]] which is its unique [[hom-object]]. Restricted to such "simplicial [[delooping groupoids]]" of simplicial groups and under this identitificaiton, the fibrations and weak equivalences in Prop. \ref{FreeMorphismsOfSimplicialGroupoids} are those of the [[model structure on simplicial groups]].
\end{remark}



## Properties

### Extra model category properties
 {#ExtraModelCategoryProperties}

We write $sSet\text{-}Grpd$ for the category of Dwyer-Kan simplicial groupoids.

\begin{definition}\label{SimplicialIntervalGroupoid}
**(simplicial interval groupoid)**
\linebreak
 Write
$$
  \mathcal{F}
  \;\colon\;
  sSet
   \overset{\mathcal{I}}{\longrightarrow}
  sSet\text{-}Cat
    \longrightarrow
  sSet\text{-}Grpd
$$
for the [[functor]] which sends a [[simplicial set]] $S$ to the [[sSet]]-[[enriched groupoid]] $\mathcal{F}(S)$ which has precisely two objects $0,1$, no non-trivial [[endomorphisms]] and isomorphisms between $0$ and $1$ freely generated from the cells of $X$.
\end{definition}
This is [Dwyer & Kan (1984), §2.8](#DwyerKan84), related to the [[Milnor construction]] in [Goerss & Jardine (2009), pp. 314](#GoerssJardine09). (Beware that in [Bergner (2008), p. 4](#Bergner08) the statement of free generation is missing.)

\begin{example}
  The construction of Def. \ref{SimplicialIntervalGroupoid} applied to the [[terminal object|terminal]]  ([[0-simplex]], "[[singleton]]") [[simplicial set]] $\Delta[0]$ is the [[interval groupoid]]:
$$
  \mathcal{F}(\ast) \,=\,
  \big\{
    0 \overset{\sim}{\leftrightarrows} 1
  \big\}
  \,.
$$
\end{example}

\begin{proposition}
  The model structure on simplicial groupoids from Prop. \ref{TheModelStructure} is [[cofibrantly generated model category|cofibrantly generated]] with generating (acyclic) cofibrations the images under the simplicial interval functor (Def. \ref{SimplicialIntervalGroupoid}) of the generating (acyclic) cofibrations in the [[classical model structure on simplicial sets]] (see [there](classical+model+structure+on+simplicial+sets#AsACofibrantlyGeneratedModelCategory)), hence of the [[boundary]]- and [[horn]]-inclusions of [[simplices]], respectively:

$$
  \begin{array}{l}
  I 
    \,\coloneqq\,
  \Big\{
    \mathcal{F}(i_n) 
      \,\colon\, 
    \mathcal{F}\big(\partial \Delta[n]\big)
     \hookrightarrow
    \mathcal{F}\big(\Delta[n]\big)
  \Big\}_{n \in \mathbb{N}}
  \\
  J 
    \,\coloneqq\,
  \Big\{
    \mathcal{F}(j^k_n) 
      \,\colon\, 
    \mathcal{F}\big(\Lambda_k[n]\big)
     \hookrightarrow
    \mathcal{F}\big(\Lambda_k[n]\big)
  \Big\}_{n \in \mathbb{N}_+, 0 \leq k \leq n}
  \end{array}
$$

\end{proposition}
This is essentially [Dwyer & Kan (1984), Prop. 2.9, 2.10](#DwyerKan84), made more explicit in [Bergner (2008), Thm. 2.2](#Bergner08).

\begin{proposition}
  The model structure on simplicial groupoids from Prop. \ref{TheModelStructure} is [[right proper model category|right proper]].
\end{proposition}
This is [Bergner (2008), Prop. 2.5](#Bergner08).


### Relation to simplicial sets

\begin{proposition}
\label{QuillenEquivalenceWithSimplicialSets}

The 

* [[Dwyer-Kan loop groupoid]]-construction $\mathcal{G}$ ([[left adjoint]])

* [[simplicial classifying space]]-construction  $\overline{W}$ ([[right adjoint]], see [here](simplicial+classifying+space#BarWForSimplicialGroupoid))

constitute a [[Quillen equivalence]]

$$
  sGrpd_{DK}
  \underoverset
    {\underset{\overline{W}}{\longrightarrow}}
    {\overset{\mathcal{G}}{\longleftarrow}}
    {\;\;\;\; \simeq_{_{\mathrlap{Qu}}} \;\;\;\;}
  sSet_{Qu}  
$$

between the model structure on $sGrpd_{DK}$ from Prop. \ref{TheModelStructure} and the [[classical model structure on simplicial sets]].

In addition both $\mathcal{G}$ and $\overline W$ preserve all [[weak equivalences]].

\end{proposition}

This is due to [Dwyer & Kan (1984), Thm. 3.3](#DwyerKan84), reviewed in [Goerss & Jardine (2009), Thm. 7.8](#GoerssJardine).


+-- {: .num_remark}
###### Remark

When restricted to simplicial groupoids of the form $(\mathbf{B} G)_\bullet$ for $G_\bullet$ a [[simplicial group]] and $\mathbf{B} G_n$ its [[delooping groupoid]] this produces a standard presentation of [[looping and delooping]] for [[infinity-groups]]. See there and at *[[model structure on simplicial groups]]* for more.

=--

\begin{lemma}\label{AcyclicFibrationsSurjectiveOnObjects}
Any [[acyclic fibration]] $f \in Fib \cap \mathrm{W}$ of simplicial groupoids is [[surjective]] on objects. 
\end{lemma}
One lazy way to see this:
\begin{proof}
For $f_\bullet \in Fib \cap \mathrm{W}$ an acyclic Kan fibration, notice that:

1. Since the [[simplicial classifying space]] functor on simplicial groupoids ([here](simplicial+classifying+space#BarWForSimplicialGroupoid)) is a [[right Quillen functor]] by Prop. \ref{QuillenEquivalenceWithSimplicialSets} it follows that $\overline{W}(f) \in Fib \cap \mathrm{W}$ is an [[acyclic Kan fibration]]

1. All acylic fibrations in the [[classical model structure on simplicial sets]] are degreewise surjective (see [this Prop.](acyclic+Kan+fibration#AcyclicKanFibrationsAreSurjective)). 

But since $\overline{W}$ is the identity on the sets of objects/vertices (by its definition [here](simplicial+classifying+space#BarWForSimplicialGroupoid)), the claim follows.
\end{proof}

Also useful to notice is:

\begin{proposition}
\label{sGrpdCofibrationIsObjectwiseSSetCofibration}
  A (acyclic) cofibration of simplicial groupoids is objectwise an (acyclic) injection, hence a [[classical model structure on simplicial sets|Kan-Quillen]] (acyclic) cofibation, of simplicial [[hom-sets]].
\end{proposition}
\begin{proof}
  By Def. \ref{FreeMorphismsOfSimplicialGroupoids} and Prop. \ref{TheModelStructure} these cofibrations of simplicial groupoids are, in particular, retracts of monomorphisms of simplcial set. Since [[sSet]] is a [[topos]], its [[epi-mono factorization system]] implies that monomorphisms are preserved under retracts. And of course also the Kan-Quillen weak equivalences are preserved under retract.
\end{proof}

## Related concepts

* [[Dwyer-Kan loop groupoid]]

* [[model structure on simplicial groups]]

* [[model structure on simplicial sets]]

* [[model structure on presheaves of simplicial groupoids]]


## References

The original article:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]],  *Homotopy theory and simplicial groupoids*, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;

A textbook account:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], after corollary 7.3 in chapter V of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack; 

A proof of the model structure closer to that establishing the [[model structure on simplicial categories]] and making explicit the [[cofibrantly generated model category|cofibrant generation]]:

* {#Bergner08} [[Julia E. Bergner]], Section 2 of: *Adding inverses to diagrams II: Invertible homotopy theories are spaces*, Homology, Homotopy Appl. **10** 2 (2008) 175-193 &lbrack;[doi:10.4310/HHA.2008.v10.n2.a9](https://dx.doi.org/10.4310/HHA.2008.v10.n2.a9), [doi:0710.2254](https://arxiv.org/abs/0710.2254), erratum:[doi:10.4310/HHA.2012.v14.n1.a15](https://dx.doi.org/10.4310/HHA.2012.v14.n1.a15)&rbrack;

See also:

* A. R. Garzon, J. G. Miranda and R. Osorio, *A simplicial description of the homotopy category of simplicial groupoids*, Theory and Applications of Categories **7**  14  (2000)263-283 &lbrack;[tac:](http://www.tac.mta.ca/tac/volumes/7/n14/7-14abs.html)&rbrack;


[[!redirects model category of simplicial groupoids]]

