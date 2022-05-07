
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

Two [[morphisms]] $C \stackrel{L}{\to} D$ and $D \stackrel{R}{\to} C$ in a [[2-category]] $\mathcal{C}$ form an **adjunction** if they are **dual** to each other ([Lambek 82](#Lambek82)).

There are two archetypical examples:

*  If $A$ is a [[monoidal category]] and $\mathcal{C} = \mathbf{B}A$ is the one-object 2-category incarnation of $A$ (the [[delooping]] of $A$), so that the morphisms in $\mathcal{C}$ correspond to the objects of $A$, then the notion of adjoint morphisms in $\mathcal{C}$ coincides precisely with the notion of [[dualizable object|dual objects]] in $A$.

*  If $\mathcal{C}$ is the $2$-category [[Cat]], so that the morphisms in $\mathcal{C}$ are [[functors]], then the notion of adjoint morphisms in $\mathcal{C}$ coincides precisely with the notion of _[[adjoint functors]]_.



The notion of adjunction may usefully be thought of as a weakened version of the notion of [[equivalence]] in a [[2-category]]: a morphism in an adjunction need not be invertible, but it has in some sense _a left inverse from below_ and _a right inverse from above_. If the morphism in an adjunction does happen to be a genuine equivalence, then we speak of the adjunction being an [[adjoint equivalence]].

Essentially everything that makes category theory nontrivial and interesting beyond [[groupoid]] theory can be derived from the concept of adjoint functors. In particular [[universal constructions]] such as [[limit|limits and colimits]] are examples of certain adjunctions.  Adjunctions are already interesting (but simpler) in [[2-posets]], such as the $2$-poset [[Pos]] of [[posets]].





## Definition

### Directly

\begin{defn} \label{DefinitionAdjunction} An _adjunction_ in a [[2-category]] is a pair of [[objects]] $C,D$ together with [[morphisms]] $L: C \to D$, $R : D \to C$ and [[2-morphisms]] $\eta: 1_C \to R \circ L$, $\epsilon: L \circ R \to 1_D$ such that the following diagrams commute, where $\cdot$ denotes [[whiskering]].

\begin{centre}
  \begin{tikzcd} 
    L \ar[r, "L \cdot \eta"] \ar[dr, swap, "id"] & L \circ R \circ L \ar[d, "\epsilon \cdot L"] \\
                                                     & L 
  \end{tikzcd}
\end{centre}

\begin{centre}
  \begin{tikzcd} 
    R \ar[r, "\eta \cdot R"] \ar[dr, swap, "id"] & R \circ L \circ R \ar[d, "R \cdot \epsilon"] \\
                                                     & R 
  \end{tikzcd}
\end{centre}

\end{defn}

\begin{rmk} The diagrams in Definition \ref{DefinitionAdjunction} are sometimes referred to as the [[triangle identities]] or the _zig-zag identities_. \end{rmk}

\begin{terminology} Given an adjunction as in Definition \ref{DefinitionAdjunction}, we refer to $L$ as the [[left adjoint]] (of $R$), and to $R$ as the [[right adjoint]] (of $L$). We refer to $\eta$ as the [[unit of the adjunction]], and to $\epsilon$ as the [[counit of the adjunction]]. \end{terminology}

\begin{rmk} When interpreted in the prototypical 2-category [[Cat]] of categories, $C$ and $D$ are [[categories]], $L$ and $R$ are [[functors]], and $\eta$ and $\epsilon$ are [[natural transformations]].  In this case (which was of course the first to be defined) there are a number of equivalent definitions of an adjunction, which can be found on the page [[adjoint functor]]. 

The general notion is obtained by [[internalization]] from the definition in [[Cat]]. \end{rmk}


### In terms of string diagrams

The definition of an adjunction may be nicely expressed using [[string diagrams]]. The data $L: C \to D$, $R : D \to C$ and 2-cells $\eta: 1_C \to R \circ L$, $\epsilon: L \circ R \to 1_D$ are depicted as

[[adjunction-L.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-R.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-unit.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-co-unit.png:pic]]

(where 1-cells read from right to left and 2-cells from bottom to top), and the zigzag identities are expressed as "pulling zigzags straight" (hence the name):

[[adjunction-up-string.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string.png:pic]]

Often, arrows on strings are used to distinguish $L$ and $R$, and most or all other labels are left implicit; so the zigzag identities, for instance, become:

[[adjunction-up-string-minimal.png:pic]] &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; [[adjunction-down-string-minimal.png:pic]]

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

\begin{corollary}
An adjunction in its [[core]] [[2-groupoid]] $Core(Cat)$ is an [[adjoint equivalence]].
\end{corollary}


\begin{example}
Let $U \,\colon\, Grp \to Set$ from [[Grp]] to [[Set]] be the usual [[forgetful functor]]. When we say "$F(X)$ is the [[free group]] generated by a set $X$", we mean there is a function $\eta_X \,\colon\, X \to U(F(X))$ which is universal among functions from $X$ to the underlying set of a group, which means in turn that given a function $f: X \to U(G)$, there is a unique group homomorphism $g: F(X) \to G$ such that 

$$f = (X \stackrel{\eta_X}{\to} U(F(X)) \stackrel{U(g)}{\to} U(G))$$

Here $\eta_X$ is a component of what we call the [[unit of an adjunction|unit of the adjunction]] $F \dashv U$, and the equation above is a recipe for the relationship between the map $g: F(X) \to G$ and the map $f: X \to U(G)$ in terms of the unit. 
\end{example}


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
The definition of adjunctions via units and counits is an "elementary" definition (so that by implication, the formulation in terms of hom-functors is not elementary) in the sense that while the hom-functor formulation relies some notion of hom-_set_, the formulation in terms of units and counits is purely in the first-order language of categories and makes no reference to a model of set theory. (Cf. [[first-order logic]] and [[second-order logic]].) The definition via (co)units therefore gives us a definition of adjunctions even if an assumption of  [[locally small|local smallness]] is not made.
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


### Adjoint $(\infty,1)$-functors
 {#AdjointInfinityOneFunctors}

\begin{proposition}
\label{AdjointInfinityFunctorsInHomotopy2Category}
  An adjunction in the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $(\infty,1)$-categories]] is equivalently a pair of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]].
\end{proposition}
([Riehl & Verity 2015, Rem. 4.4.5](adjoint+infinity1-functor#RiehlVerity15); [Riehl & Verity 2022, Prop. F.5.6](adjoint+infinity1-functor#RVElements); see [there](adjoint+infinity1-functor#InTheHomotopy2Category) for more).


\begin{remark}
  In view of Prop. \ref{AdjunctionsInCatAreAdjointFunctors},
  the remarkable aspect of Prop. \ref{AdjointInfinityFunctorsInHomotopy2Category} is that the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $\infty$-categories]] is sufficient to detect adjointness of [[(infinity,1)-functors|$\infty$-functors]], which would, *a priori*, be defined as a kind of homotopy-coherent adjointness in the full [[(infinity,2)-category|$(\infty,2)$-category]] [[(infinity,1)Cat|$Cat_{(\infty,1)}$]]. For more on this reduction of homotopy-coherent adjunctions to plain adjunctions see [Riehl & Verity 2016, Thm. 4.3.11, 4.4.11](adjoint+infinity1-functor#RiehlVerity16).
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

For the basics, see any text on [[category theory]] (and see the references at _[[adjoint functor]]_), for instance:

* {#Borceux94} [[Francis Borceux]], Vol 1, Section 3 of _[[Handbook of Categorical Algebra]]_

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Chapter 6 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

 
* _[[geometry of physics -- categories and toposes]] -- [Adjunctions](https://ncatlab.org/nlab/show/geometry+of+physics+--+categories+and+toposes#Adjunctions)_

For some early history and illustrative examples see

* {#Lambek82} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co. (1982) ([doi:10.1007/978-94-009-8462-2_6](https://link.springer.com/chapter/10.1007/978-94-009-8462-2_6))

  (more along these lines at _[[objective logic]]_).

The fundamental role of adjunctions in [[logic]]/[[type theory]] originates with the observaiton that [[substitution]] forms an [[adjoint triple]] with [[existential quantification]] and [[universal quantification]]:

* {#Lawvere69} [[William Lawvere]], _Adjointness in Foundations_, ([tac:16](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

* [[William Lawvere]], _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf))

Adjunctions in [[programming languages]]:

* {#Hinze12} Ralf Hinze, _Generic Programming with Adjunctions_,  In: J. Gibbons  (ed.) _Generic and Indexed Programming_ Lecture Notes in Computer Science, vol 7470. Springer 2012 ([pdf](http://www.cs.ox.ac.uk/ralf.hinze/LN.pdf), [slides](http://www.cs.ox.ac.uk/ralf.hinze/SSGIP10/Slides.pdf) [doi:10.1007/978-3-642-32202-0_2](https://doi.org/10.1007/978-3-642-32202-0_2))

* Jeremy Gibbons, Fritz Henglein, Ralf Hinze, Nicolas Wu, _Relational Algebra by Way of Adjunctions_, Proceedings of the ACM on Programming Languages archive Volume 2 Issue ICFP, September 2018 Article No. 86  ([pdf](https://www.cs.ox.ac.uk/jeremy.gibbons/publications/reladj.pdf), [doi:10.1145/3236781](https://dl.acm.org/citation.cfm?doid=3243631.3236781))

See also

* Wikipedia, [Adjoint Functors](http://en.wikipedia.org/wiki/Adjoint_functors)

* Catsters, _Adjunctions_ ([YouTube](http://www.youtube.com/watch?v=loOJxIOmShE&feature=channel_page))

-

[[!redirects adjoint pair]]
[[!redirects adjoint pairs]]
[[!redirects adjunctions]]