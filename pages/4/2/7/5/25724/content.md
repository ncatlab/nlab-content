
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
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

## Idea

Both [[quasi-categories]] as well as [[sSet-enriched categories]] serve as models for [[(infinity,1)-categories|$(\infty,1)$-categories]] (exhibited by the [[Joyal model structure for quasi-categories]] and the [[Dwyer–Kan–Bergner model structure on sSet-enriched categories]], respectively) and in fact as [[Quillen equivalence|Quillen equivalent]] models (see the *[[relation between quasi-categories and simplicial categories]]*) whose [[right Quillen functor]] is the [[homotopy coherent nerve]]-operation. Its [[left adjoint]]
$$
  \mathfrak{C} 
     \;\colon\; 
  sSet \longrightarrow sSet\text{-}Cat
$$
&lbrack;[Lurie (2009), pp. 20](#Lurie09)&rbrack; thus encodes any [[quasi-category]] equivalently in an [[sSet]]-[[enriched category]]. Since in the latter model, but not in the former, [[horizontal composition]] is a strictly [[associativity|associative]] and [[unitality|unital]] operation, one may think of $\mathfrak{C}(-)$ as (partially) "rigidifying" the data in a quasi-category, in the sense of [[semi-strict infinity-category|semi-strictification of $\infty$-categories]], whence it is also known as the operation of *rigidification of quasi-categories* &lbrack;[Dugger & Spivak (2011a)](#DuggerSpivak11a)&rbrack;.

## Definition

### The Joyal rigidification functor

The __Joyal rigidification functor__ $\mathscr{C}$ is defined as the [[left adjoint]] of the Cordier–Vogt [[homotopy coherent nerve functor]] $N$:

\[
  \label{RigidificationAsLeftAdjointToHomotopyCoherentNerve}
  sSet
  \underoverset
    {\underset{N}{\longleftarrow}}
    {\overset{\mathfrak{C}}{\longrightarrow}}
    {\;\;\; \bot \;\;\;}
  sSet\text{-}Cat
\]

This notion is briefly mentioned and attributed to [[André Joyal]] by [Bergner (2007), above Theorem 7.8](#Bergner07); the first detailed account is due to [Lurie (2009), §1.1.5 and §2.2](#Lurie09).


### The Dugger–Spivak rigidification functor

The __Dugger–Spivak rigidification functor__ &lbrack;[Dugger & Spivak (2011a)](#DuggerSpivak11a)&rbrack;
provides a more explicit model for the same [[(∞,1)-functor]], by virtue of writing down an explicit formula that does not use colimits.
The resulting functor is connected to the Joyal functor by a zigzag of natural weak equivalences.

Specifically, given a [[simplicial set]] $S$ (not necessarily fibrant in the [[Joyal model structure]]),
we construct the Dugger–Spivak rigidification $\mathfrak{C}^{\mathrm{nec}}S$ as the following [[simplicial category]]:

Objects are vertices of $S$.

The [[simplicial set]] of morphisms $x\to y$ is the nerve of the category of __necklaces__ in $S$ (introduced by [[Hans-Joachim Baues]]).
A necklace is a simplicial map
$$\Delta^{n_1}\vee \cdots \vee \Delta^{n_k}\to S,$$
where $\vee$ glues the final vertex of the preceding simplex to the initial vertex of the following simplex.
Morphisms are commutative triangles of simplicial maps that preserve the initial and final vertex of the entire necklace.

Composition is defined by concatenating necklaces.
The resulting functor from simplicial sets admits
a zigzag of weak equivalences to the Joyal rigidification functor.


## Properties
 {#Properties}

### Respect for products

The rigidification operation does not strictly preserve [[Cartesian products]] (cf. *[[products of simplicial sets]]*) but it does so up to equivalence:

\begin{proposition}\label{PreservationOfProducts}
For $S,\, S' \,\in\, sSet$, the [[natural transformation]]
$$
  \mathfrak{C}(S \times S')
  \overset{
    \big(
      \mathfrak{C}(pr_S)
      ,\,
      \mathfrak{C}(pr_{S'})
    \big)
  }{\longrightarrow}
  \mathfrak{C}(S) \times \mathfrak{C}(S')
$$
(induced from the [[projections]] $S \overset{pr_S}{\leftarrow} S \times S' \overset{pr_{S'}}{\rightarrow} S'$)
is a [[Dwyer-Kan equivalence]].
\end{proposition}
&lbrack;[Lurie (2009), Cor. 2.2.5.6](#Lurie09); [Dugger & Spivak (2011a), Prop. 6.2](#DuggerSpivak11a)&rbrack;


### Relation to Dwyer-Kan groupoids

Let 
\[
  \label{LocalizationOfsSetCategoriesToSSetGroupoids}
  L 
    \,\colon\,
  sSet\text{-}Cat
  \longrightarrow
  sSet\text{-}Grp
\]
denote the functor from [[sSet-enriched categories]] to [[sSet]]-[[enriched groupoids]] (Dwyer-Kan [[simplicial groupoids]]) which is degreewise given by the [[localization]] operation [[left adjoint]] to the [[full subcategory]] inclusion [[Grpd]] $\hookrightarrow$ [[Cat]].

Let
\[
  \label{DwyerKanFundamentalGroupoid}
  \mathcal{G}
  \,\colon\,
  sSet 
    \longrightarrow
  sSet\text{-}Grpd
    \hookrightarrow
  sSet\text{-}Cat
\]
denote the [[Dwyer-Kan fundamental simplicial groupoid]]-construction with values in [[sSet]]-[[enriched groupoids]] (Dwyer-Kan [[simplicial groupoids]]), here to be regarded among [[sSet-enriched categories]].

\begin{proposition}\label{ComparisonWithDKGroupoids}
  For $S \,\in\, sSet$ there is a [[natural transformation]] 
$$
  L \circ \mathfrak{C}(S)
  \longrightarrow
  \mathcal{G}(S)
$$
which is a [[Dwyer-Kan equivalence]]
(from the localization (eq:LocalizationOfsSetCategoriesToSSetGroupoids) of the rigidification (eq:RigidificationAsLeftAdjointToHomotopyCoherentNerve) to the Dwyer-Kan fundamental groupoid (eq:DwyerKanFundamentalGroupoid)).
\end{proposition}
&lbrack;[Minichiello, Rivera & Zeinalian (2023), Thm. 1.1 (Cor. 4.2)](#MinichielloRiveraZeinalian23)&rbrack;


## Related concepts

* [[homotopy coherent nerve]]

* [[relation between quasi-categories and simplicial categories]]

* [[Dwyer-Kan fundamental simplicial groupoid]]


## References

The construction is briefly mentioned and attributed to [[André Joyal]] in:

* {#Bergner07} [[Julie Bergner]], Theorem 7.8 in: *A survey of $(\infty,1)$-categories*, in: [[John Baez]], [[Peter May]] (eds.),  _[[Towards Higher Categories]]_ The IMA Volumes in Mathematics and its Applications **152**, Springer (2007) &lbrack;[arXiv:math/0610239](http://arxiv.org/abs/math/0610239), [doi:10.1007/978-1-4419-1524-5_2](https://doi.org/10.1007/978-1-4419-1524-5_2)&rbrack; 

First detailed discussion (not using a name beyond the symbol "$\mathfrak{C}$") is due to:

* {#Lurie09} [[Jacob Lurie]], §1.1.5 and §2.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;

Further discussion and the terminology "rigidification" is due to

* {#DuggerSpivak11a} [[Dan Dugger]], [[David Spivak]], *Rigidification of quasi-categories*, Algebr. Geom. Topol. **11** (2011) 225-261 &lbrack;[arXiv:0910.0814](http://arxiv.org/abs/0910.0814), [doi:10.2140/agt.2011.11.225](http://dx.doi.org/10.2140/agt.2011.11.225)&rbrack;

aimed at discussing [[quasi-categorical hom-spaces]]:

* {#DuggerSpivak11b} [[Dan Dugger]], [[David Spivak]], *Mapping spaces in quasi-categories*, Algebr. Geom. Topol. **11** (2011) 263-325 &lbrack;[arXiv:0911.0469](http://arxiv.org/abs/0911.0469), [doi:10.2140/agt.2011.11.263](http://dx.doi.org/10.2140/agt.2011.11.263)&rbrack;

See also:

* [[Emily Riehl]], *On the structure of simplicial categories associated to quasi-categories*, Math. Proc. Camb. Phil. Soc. **150** (2011) 489-504 &lbrack;[arXiv:0912.4809](https://arxiv.org/abs/0912.4809), [doi:10.1017/S0305004111000053](https://doi.org/10.1017/S0305004111000053)&rbrack;


* {#MinichielloRiveraZeinalian23} [[Emilio Minichiello]], [[Manuel Rivera]], [[Mahmoud Zeinalian]], §3.2 in: *Categorical models for path spaces*, Advances in Mathematics **415** (2023) 108898 &lbrack;[arXiv:2201.03046](https://arxiv.org/abs/2201.03046), [doi:10.1016/j.aim.2023.108898](https://doi.org/10.1016/j.aim.2023.108898)&rbrack;

