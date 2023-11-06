
> This page is about adjunctions in general [[2-categories]]. Specifically for the common case of adjunctions in [[Cat]] see at *[[adjoint functors]]*. For the notion of "adjunction of a set to a field" in [[field theory]], see [[field extension]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A [[pair]] of [[1-morphisms]] in a [[2-category]] form an **adjunction** if they are **dual** to each other ([Lambek (1982)](#Lambek82), cf. [here](geometry+of+physics+--+categories+and+toposes#CategoryTheoryIsTheoryOfDuality)) in a precise sense.

There are two archetypical classes of examples:

* If $A$ is a [[monoidal category]] and $\mathbf{B}A$ denotes the [[singleton|one-]][[object]] 2-category whose single [[hom-category]] is $A$ (the [[delooping]] of $A$), then the notion of adjoint morphisms in $\mathbf{B}A$ coincides precisely with the notion of [[dualizable object|dual objects]] in $A$, subsuming, in turn, classical examples such as [[dual vector spaces]] in the case that $A =  $ [[FinDimVect]].

* Adjunctions in the [[2-category]] [[Cat]] of [[categories]] are  _[[adjoint functors]]_.

  * Notice that essentially everything that makes [[category theory]] nontrivial and interesting, beyond [[groupoid]]-theory, is governed by the concept of [[adjoint functors]]. In particular [[universal constructions]] such as [[limit|limits and colimits]], [[Kan extensions]], ([[coend|co]])[[ends]] are examples of adjunctions in [[Cat]].

  * Similarly, for $V$ any [[cosmos for enrichment]], adjunctions in the 2-category [[VCat]] of $V$-[[enriched categories]] are equivalently [[enriched adjoint functors]]. Already in simple cases such $V = $ [[truth values]] this subsumes classical concepts such as that of [[Galois connections]].

  * Remarkably, even adjunctions in the [[homotopy 2-category]] of [[(infinity,1)-categories|$(\infty,1)$-categories]] are equivalent to [[adjoint (infinity,1)-functors|adjoint $\infty$-functors]], see the examples [below](#AdjointInfinityOneFunctors). 

  These classes of examples make adjunctions a key notion in *[[formal category theory]]*.

      
Finally, the notion of *adjunction* may usefully be thought of as a generalization of the notion of *[[equivalence in a 2-category]]*: an adjoint [[1-morphism]] need not be [[invertible morphism|invertible]] (even up to [[2-isomorphism]]) but it does have, in a precise sense, _a left inverse from below_ or _a right inverse from above_. 

If an adjoint 1-morphisms happens to be a genuine [[equivalence in a 2-category]], then the adjunction is called an *[[adjoint equivalence]]*.



## Definition
 {#Definition}

\begin{defn} \label{DefinitionAdjunction} 
An _adjunction_ in a [[2-category]] is 

* a [[pair]] of [[objects]] $C$ and $D$ 

* a [[pair]] of [[1-morphisms]] 

  $L \colon C \longrightarrow D$ (the *[[left adjoint]]*) 

  $R \colon D \longrightarrow C$ (the *[[right adjoint]]*)

* a [[pair]] of [[2-morphisms]] 

  $\eta \colon 1_C \longrightarrow R \circ L$ (the *[[adjunction unit]]*)

  $\epsilon \colon L \circ R \longrightarrow 1_D$ (the *[[adjunction counit]]*)

such that the following equivalent conditions hold:

* **[[triangle identity]]** the following [[commuting diagram|diagrams commute]] in the [[hom-categories]] (where "$\cdot$" denotes [[whiskering]]):

\begin{centre}
  \begin{tikzcd} 
    L \ar[r, "L \cdot \eta"] 
    \ar[dr, swap, "\mathrm{id}"] 
    & L \circ R \circ L \ar[d, "\epsilon \cdot L"] 
    \\ & L 
  \end{tikzcd}
\end{centre}

\begin{centre}
  \begin{tikzcd} 
    R \ar[r, "\eta \cdot R"] \ar[dr, swap, "id"] & R \circ L \circ R \ar[d, "R \cdot \epsilon"] 
   \\ & R 
  \end{tikzcd}
\end{centre}

* **[[zig-zag law]]** the following [[equality]] of [[2-morphisms]]:

\begin{tikzcd}[row sep=10pt]
  C
  \ar[rr, bend left=40, "{\mathrm{id}}", 
      "{\ }"{name=s1, swap}
  ]
  \ar[r, "L"{description}, "{\ }"{name=t1, pos=.9}]
  \ar[
    from=s1,
    to=t1,
    Rightarrow,
    "{ \eta }"{swap}
  ]
  &
  D
  \ar[rr, bend right=40, "{\mathrm{id}}"{swap},
    "{\ }"{name=t2}
  ]
  \ar[r, "R"{description}]
  &
  C
  \ar[r, "L"{description}, "{\ }"{swap, name=s2, pos=.1}]
  \ar[
    from=s2,
    to=t2,
    Rightarrow,
    "{ \epsilon }"
  ]  
  &
  D
  &=&
  C
  \ar[r, bend left=40, "{L}", "{\ }"{name=s3, swap}]
  \ar[r, bend right=40, "{L}"{swap}, "{\ }"{name=t3}]
  \ar[from=s3, to=t3, Rightarrow, "{\mathrm{id}}"]
  &
  D
\end{tikzcd}

\begin{tikzcd}[row sep=10pt]
  D
  \ar[rr, bend right=40, "{\mathrm{id}}"{swap}, 
      "{\ }"{name=s1}
  ]
  \ar[r, "R"{description}, "{\ }"{name=t1, pos=.9, swap}]
  \ar[
    from=t1,
    to=s1,
    Rightarrow,
    "{ \epsilon }"{swap, pos=.3}
  ]
  &
  C
  \ar[rr, bend left=40, "{\mathrm{id}}",
    "{\ }"{name=t2, swap}
  ]
  \ar[r, "L"{description}]
  &
  D
  \ar[r, "R"{description}, "{\ }"{name=s2, pos=.1}]
  \ar[
    from=t2,
    to=s2,
    Rightarrow,
    "{ \eta }"{pos=.8}
  ]  
  &
  C
  &=&
  D
  \ar[r, bend left=40, "{R}", "{\ }"{name=s3, swap}]
  \ar[r, bend right=40, "{R}"{swap}, "{\ }"{name=t3}]
  \ar[from=s3, to=t3, Rightarrow, "{\mathrm{id}}"]
  &
  C
\end{tikzcd}

{#InTermsOfStringDiagrams} In terms of [[string diagrams]] the above data entering the definition looks like

[[adjunction-L.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-R.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-unit.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-co-unit.png:pic]]

(where 1-cells read from right to left and 2-cells from bottom to top), and the [[zig-zag identities]] appear as moves "pulling zigzags straight" (hence the name):

[[adjunction-up-string.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string.png:pic]]

Often, arrows on strings are used to distinguish $L$ and $R$, and most or all other labels are left implicit; so the zigzag identities, for instance, become:

[[adjunction-up-string-minimal.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string-minimal.png:pic]]


\end{defn}




## Properties

### Relation to monads

See at _[monad -- Relation to adjunctions](monad#RelationToAdjunctionsAndMonadicity)_.



## Examples

### Adjoint functors
  {#AdjointFunctors}

\begin{proposition}\label{AdjunctionsInCatAreAdjointFunctors}
An adjunction in the 2-category [[Cat]] of [[categories]], [[functors]] and [[natural transformations]] is equivalently a pair of [[adjoint functors]].
\end{proposition}
See also the proof [here](adjoint+functor#AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat) at *[[adjoint functor]]*.
\begin{proof}
Suppose given functors $L \,\colon\, C \to D$, $R: D \to C$ and the structure of a pair of [[adjoint functors]] in the form of a natural isomorphism of [[hom-sets]] ([here](adjoint+functor#InTermsOfHomIsomorphism))

$$
  \Psi_{c, d}
  \;\colon\; 
  \hom_D(L(c), d) \cong \hom_C(c, R(d))
$$ 

Now the idea is that, in the spirit of the (proof of the) [[Yoneda lemma]], we would like $\Psi$ to be determined by what it does to [[identity morphisms]]. With that in mind, define the [[adjunction unit]] $\eta \colon 1_C \to R L$ by the formula $\eta_c = \Psi_{c, L(c)}(1_{L(c)})$. Dually, define the counit $\varepsilon \,\colon\, L R \to 1_D$ by the formula
$$
  \varepsilon_d 
  \,\coloneqq\, \Psi^{-1}_{R(d), d}(1_{R(d)})
  \,.
$$

Then given $g \,\colon\, L(c) \to d$, the claim is that 

$$
  \Psi_{c, d}(g) 
    \,=\, 
  (c \stackrel{\eta_c}{\to} R(L(c)) \stackrel{R(g)}{\to} R(d))
  \,.
$$ 

This may be left as an exercise in the yoga of the Yoneda lemma, applied to $\hom_D(L(c), -) \to \hom_C(c, R(-))$. By [[formal duality]], given $f \,\colon\, c \to R(d)$, 

$$
  \Psi^{-1}_{c, d}(f) = (L(c) \stackrel{L(f)}{\to} L(R(d)) \stackrel{\varepsilon_d}{\to} d)
  \,.
$$ 

(We spell out the Yoneda-lemma proof of this dual form [below](#YonedaLemmaArgument).)

Finally, these operations should obviously be mutually inverse, but that can again be entirely encapsulated Yoneda-wise in terms of the effect on identity maps. Thus, if $\eta_c \coloneqq \Psi_{c, L(c)}(1_{L(c)})$, via the recipe just given for $\Psi^{-1}$ we recover 

$$1_{L(c)} = (L(c) \stackrel{L(\eta_c)}{\to} L R L(c) \stackrel{\varepsilon_{L(c)}}{\to} L(c))$$ 

and this is one of the famous [[triangle identities]]: $1_L = (L \stackrel{L \eta}{\to} L R L \stackrel{\varepsilon L}{\to} L)$.  Here, juxtaposition of functors and natural transformations denotes neither functor application, nor vertical composition, nor horizontal composition, but [[whiskering]]. By duality, we have the other [[triangle identity]] $1_R = (R \stackrel{\eta R}{\to} R L R \stackrel{R \varepsilon}{\to} R)$. These two triangular equations are enough to guarantee that the recipes for $\Psi$ and $\Psi^{-1}$ indeed yield mutual inverses. 

In conclusion it is perfectly sufficient to define an adjoint pair of functors in $Cat$ as given by unit and counit transformations $\eta: 1_C \to R L$, $\varepsilon: L R \to 1_D$, satisfying the triangle identities above. 
\end{proof}

\begin{remark}
The definition of adjunctions via [[unit of an adjunction|units]] and [[counit of an adjunction|counits]] is an "elementary" definition (so that by implication, the formulation in terms of [hom-isomorphisms](adjoint functor#InTermsOfHomIsomorphism) is not elementary) in the sense that while the [[hom-functor]] formulation relies on some notion of [[hom-set|hom-*set*]], the formulation in terms of units and counits is purely in the [[first-order logic|first-order]] [[language]] of [[categories]] and makes no reference to a model of [[set theory]]. The definition via (co)units therefore gives us a definition of adjunctions even if an assumption of  [[locally small|local smallness]] is not made.
\end{remark}

\begin{proof}\label{YonedaLemmaArgument}
**(Yoneda-lemma argument)**
\linebreak
We claim that $\Psi^{-1}_{c, d} \,\colon\, \hom_C(c, R(d)) \to \hom_D(L(c), d)$ can be defined by the formula 

$$\Psi^{-1}_{c, d}(f: c \to R(d)) = (L(c) \stackrel{L(f)}{\to} L(R(d)) \stackrel{\varepsilon_d}{\to} d)$$ 

where $\varepsilon_d \coloneqq \Psi^{-1}_{R(d), d}(1_{R(d)})$. This is by appeal to the proof of the Yoneda lemma applied to the transformation 

$$\Psi^{-1}_{-, d}: \hom_C(-, R(d)) \to \hom_D(L(-), d)$$ 

For the naturality of $\Psi^{-1}$ in the argument $(-)$ would imply that given $f: c \to R(d)$, we have a commutative square 

$$\array{
  \hom_C(R(d), R(d)) 
  & 
  \stackrel{\Psi^{-1}_{R(d), d}}{\to} 
  & \hom_D(L(R(d)), d) 
  \\
  \hom_C(f, R(d)) 
  \big\downarrow 
  & & 
  \big\downarrow \hom_D(L(f), d) 
  \\
  \hom_C(c, R(d)) 
  & 
  \underset{\Psi^{-1}_{c, d}}{\to} 
  & 
  \hom_D(L(c), d)
}$$ 

Chasing the element $1_{R(d)}$ down and then across, we get $f: c \to R(d)$ and then $\Psi^{-1}_{c, d}(f)$. Chasing across and then down, we get $\varepsilon_d$ and then $\varepsilon_d \circ L(f)$. This completes the verification of the claim.
\end{proof}

\begin{corollary}
An adjunction in its [[core]] [[2-groupoid]] $Core(Cat)$ is an [[adjoint equivalence]].
\end{corollary}

### Enriched adjoint functors

Similarly one sees:
\begin{example}\label{EnrichedAdjointFunctors}
  For $V$ a [[cosmos for enrichment]], an adjunction in the [[2-category]] [[VCat]] of $V$-[[enriched categories]] is equivalently a pair $V$-[[enriched functors]].
\end{example}

\begin{example}
Let $U \,\colon\, Grp \to Set$ from [[Grp]] to [[Set]] denote the usual [[forgetful functor]] from [[Grp]] to [[Set]]. When we say "$F(X)$ is the [[free group]] generated by a set $X$", we mean there is a function $\eta_X \,\colon\, X \to U(F(X))$ which is universal among functions from $X$ to the underlying set of a group, which means in turn that given a function $f: X \to U(G)$, there is a unique group homomorphism $g \colon F(X) \to G$ such that 

$$
  f = (X \stackrel{\eta_X}{\to} U(F(X)) \stackrel{U(g)}{\to} U(G))
$$

Here $\eta_X$ is a component of what we call the [[unit of an adjunction|unit of the adjunction]] $F \dashv U$, and the equation above is a recipe for the relationship between the map $g: F(X) \to G$ and the map $f: X \to U(G)$ in terms of the unit. 
\end{example}



### Adjoint $(\infty,1)$-functors
 {#AdjointInfinityOneFunctors}

\begin{proposition}
\label{AdjointInfinityFunctorsInHomotopy2Category}
  An adjunction in the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $(\infty,1)$-categories]] is equivalently a pair of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]].
\end{proposition}
([Riehl & Verity 2015, Rem. 4.4.5](adjoint+infinity1-functor#RiehlVerity15); [Riehl & Verity 2022, Prop. F.5.6](adjoint+infinity1-functor#RVElements); see [there](adjoint+infinity1-functor#InTheHomotopy2Category) for more).


\begin{remark}
  In view of Prop. \ref{AdjunctionsInCatAreAdjointFunctors},
  the remarkable aspect of Prop. \ref{AdjointInfinityFunctorsInHomotopy2Category} is that the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $\infty$-categories]] is sufficient to detect adjointness of [[(infinity,1)-functors|$\infty$-functors]], which would, *a priori*, be defined as a kind of [[higher homotopy]]-[[coherence law|coherent]] adjointness in the full [[(infinity,2)-category|$(\infty,2)$-category]] [[(infinity,1)Cat|$Cat_{(\infty,1)}$]]. For more on this reduction of homotopy-coherent adjunctions to plain adjunctions see [Riehl & Verity 2016, Thm. 4.3.11, 4.4.11](adjoint+infinity1-functor#RiehlVerity16).
\end{remark}


## Related concepts

* [[adjoint functor]], [[adjoint (∞,1)-functor]]

* [[left adjoint]], [[right adjoint]]

* [[duality]]

* [[adjunct]]

* [[dual adjunction]], [[Galois connection]]

* [[monoidal adjunction]]

* [[enriched adjunction]]

* [[derived adjunction]]

* [[adjoint monad]]

* [[heteromorphism]]

* [[adjoint string]]

  * [[adjoint triple]], [[adjoint quadruple]]

* [[ambidextrous adjunction]]

* [[adjoint cylinder]]

* [[adjoint logic]]


## References

Adjunctions in 2-categories were introduced (together with the notion of [[strict 2-categories]] itself) in:

* [[Jean-Marie Maranda]], pp. 762 in: *Formal categories*, Canadian Journal of Mathematics **17** (1965) 758-801 &lbrack;[doi:10.4153/CJM-1965-076-0](https://doi.org/10.4153/CJM-1965-076-0), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/A7C463460EB8CAC64C2CA340F870CF80/S0008414X00039729a.pdf/formal-categories.pdf)&rbrack;

Though see also the following, which uses more modern terminology:

* [[Max Kelly]], §2 in: *Adjunction for enriched categories*, in: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106**, Springer (1969) &lbrack;[doi:10.1007/BFb0059145](https://doi.org/10.1007/BFb0059145)&rbrack;

Review:

* [[Saunders MacLane]], §XII.4 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


* {#Lack10} [[Steve Lack]], §2.1 in: *A 2-categories companion*,  in: *[[Towards Higher Categories]]*, The IMA Volumes in Mathematics and its Applications **152** Springer (2010) &lbrack;[arXiv:math.CT/0702535](http://arxiv.org/abs/math.CT/0702535), [doi:10.1007/978-1-4419-1524-5_4](https://doi.org/10.1007/978-1-4419-1524-5_4)&rbrack;

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Chapter 6 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

Fr the special case of [[adjoint functors]] see any text on [[category theory]] (and see the references at _[[adjoint functor]]_), for instance:

* {#Borceux94} [[Francis Borceux]], Vol 1, Section 3 of _[[Handbook of Categorical Algebra]]_
 
* _[[geometry of physics -- categories and toposes]] -- [Adjunctions](https://ncatlab.org/nlab/show/geometry+of+physics+--+categories+and+toposes#Adjunctions)_

For some early history and illustrative examples see

* {#Lambek82} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co. (1982) ([doi:10.1007/978-94-009-8462-2_6](https://link.springer.com/chapter/10.1007/978-94-009-8462-2_6))

  (more along these lines at _[[objective logic]]_).

The fundamental role of [[adjoint functors]] in [[logic]]/[[type theory]] originates with the observaiton that [[substitution]] forms an [[adjoint triple]] with [[existential quantification]] and [[universal quantification]]:

* {#Lawvere69} [[William Lawvere]], _Adjointness in Foundations_, ([tac:16](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

* [[William Lawvere]], _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf))

Adjunctions in [[programming languages]] (though mainly again just [[adjoint functors]]):

* {#Hinze12} Ralf Hinze, _Generic Programming with Adjunctions_,  In: J. Gibbons  (ed.) _Generic and Indexed Programming_ Lecture Notes in Computer Science, vol 7470. Springer 2012 ([pdf](http://www.cs.ox.ac.uk/ralf.hinze/LN.pdf), [slides](http://www.cs.ox.ac.uk/ralf.hinze/SSGIP10/Slides.pdf) [doi:10.1007/978-3-642-32202-0_2](https://doi.org/10.1007/978-3-642-32202-0_2))

* Jeremy Gibbons, Fritz Henglein, Ralf Hinze, Nicolas Wu, _Relational Algebra by Way of Adjunctions_, Proceedings of the ACM on Programming Languages archive Volume 2 Issue ICFP, September 2018 Article No. 86  ([pdf](https://www.cs.ox.ac.uk/jeremy.gibbons/publications/reladj.pdf), [doi:10.1145/3236781](https://dl.acm.org/citation.cfm?doid=3243631.3236781))

See also

* Wikipedia, *[Adjoint Functors](http://en.wikipedia.org/wiki/Adjoint_functors)*

* Catsters, _Adjunctions_ ([YouTube](http://www.youtube.com/watch?v=loOJxIOmShE&feature=channel_page))

-

[[!redirects adjoint pair]]
[[!redirects adjoint pairs]]
[[!redirects adjunctions]]