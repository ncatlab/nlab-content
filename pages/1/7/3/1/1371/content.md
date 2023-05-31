
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

\tableofcontents

## Idea

As a model for an [[(∞,1)-categories]], [[sSet-enriched categories]] ("[[simplicial categories]]") may be thought of as a [[semi-strict infinity-category|semi-strictification]] of a [[quasi-category]], where [[composition]] along [[objects]] is strictly [[associativity|associative]] and [[unitality|unital]].

The equivalence between [[quasi-categories]] and [[sSet-enriched categories]] as models for [[(∞,1)-categories]] is exhibited by the operation of sending an $sSet$-category $\mathbf{C}$ to the [[simplicial set]] $N(\mathcal{C})$ called its *[[homotopy-coherent nerve]]* (in generalization of the [[simplicial nerve]] of an ordinary [[category]]). Together with its [[left adjoint]] operation $\mathfrak{C}$ ("[[rigidification of quasi-categories]]") this constitutes a [[Quillen equivalence]] between the two models.


## The Quillen equivalence

Our notation partly follows [Bergner (2018)](#Bergner18).

\begin{proposition}
\label{TheQuillenEquivalence}
There is a [[Quillen equivalence]]:

$$
 sSet\text{-}Cat
 \underoverset
   {\underset{\tilde N}{\longrightarrow}}
   {\overset{\mathfrak{C}}{\longleftarrow}}
   {\;\;\; \bot \;\;\;} 
 sSet.
$$

where:

* $SC$ denotes the category of [[sSet-enriched categories]]
equipped with the [[Dwyer–Kan–Bergner model structure]],

* $sSet$ denotes the [[Joyal model structure]] on [[simplicial sets]],

* $\tilde N$ denotes the [[homotopy coherent nerve]] functor,

* $\mathfrak{C}$ denotes [[rigidification of quasi-categories]].

In particular, for $C$ a fibrant [[SSet]]-[[enriched category]], the canonical morphism

$$
  \mathfrak{C}\big(\tilde N(C)\big) 
  \longrightarrow 
  C
$$

given by the [[adjunction counit|counit]] of the above adjunction is [[derived functor|derived]], hence a [[Dwyer–Kan weak equivalence]] of [[simplicial categories]].

For $S$ any [[simplicial set]], the canonical morphism

$$
  S 
  \longrightarrow
  \tilde N\Big(
    R\big(
      \mathfrak{C}(S)
    \big)
  \Big)
$$

is a [[model structure for quasi-categories|categorical equivalence]] of simplicial sets,
where $R$ denotes a [[fibrant replacement]] functor in the [[Dwyer–Kan–Bergner model structure]].
\end{proposition}
This was claimed and credited to [[André Joyal|Joyal]] in [Bergner (2007), Thm. 7.8](#Bergner07); detailed proof was produced in [Lurie (2009), Thm. 2.2.5.1 & p. 91](#Lurie09).

For more details on the [[rigidification of quasi-categories]] see also [Dugger & Spivak (2009a)](#DuggerSpivak.Rigidification), [(2009b)](#DuggerSpivak.Mapping).


## Relations

### Via $\bar W$-construction

We have an evident inclusion 
$$sSet Cat \hookrightarrow Cat^{\Delta}$$
of [[simplicially enriched categories]]
into [[simplicial objects in Cat]].

On the latter the $\bar W$-functor is defined as the composite
$$
  \bar W 
   \colon
  Cat^\Delta
   \stackrel{N^\Delta}{\to}
  sSet^\Delta
   \stackrel{}{\to}
  sSet
$$
where first we degreewise form the ordinary [[nerve]] of categories and then take the total simplicial set of [[bisimplicial sets]] (the [[right adjoint]] of pullback along the [[diagonal]] $\Delta^n \to \Delta^n \times \Delta^n$).

+-- {: .num_prop}
###### Proposition

For $C$ a [[simplicial groupoid]] there is a [[weak homotopy equivalence]]
$$\mathcal{N}(C) \to \bar W(C)$$
from the [[homotopy coherent nerve]]

=--

([Hinich](#Hinich))


## Related concepts

* [[straightening and unstraightening]]

* [[simplicial category]]

  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[simplicial groupoid]]

There is an [[operad|operadic]] analog of the relation between quasi-categories and simplicial categories, involving, correspondingly, [[dendroidal sets]] and [[simplicial operads]].


## References

The notion of the [[homotopy coherent nerve]] (see there for more) goes back to [Cordier (1982)](homotopy+coherent+nerve#Cordier82); [Cordier & Porter(1986)](homotopy+coherent+nerve#CordierPorter86).

The [[Quillen equivalence]] between the [[model structure for quasi-categories]] and the [[model structure on sSet-categories]] is described in

* {#Lurie09} [[Jacob Lurie]], §1.1.5 and §2.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;

after an unpublished proof by [[André Joyal]] was announced in:

* {#Bergner07} [[Julie Bergner]], Theorem 7.8 in: *A survey of $(\infty,1)$-categories*, in: [[John Baez]], [[Peter May]] (eds.),  _[[Towards Higher Categories]]_ The IMA Volumes in Mathematics and its Applications **152**, Springer (2007) &lbrack;[arXiv:math/0610239](http://arxiv.org/abs/math/0610239), [doi:10.1007/978-1-4419-1524-5_2](https://doi.org/10.1007/978-1-4419-1524-5_2)&rbrack; 

Further discussion of [[rigidification of quasi-categories]] $\mathfrak{C}$:

* {#DuggerSpivak.Rigidification} [[Dan Dugger]], [[David Spivak]], *Rigidification of quasi-categories*, Algebr. Geom. Topol. **11** (2011) 225-261 &lbrack;[arXiv:0910.0814](http://arxiv.org/abs/0910.0814), [doi:10.2140/agt.2011.11.225](http://dx.doi.org/10.2140/agt.2011.11.225)&rbrack;

* {#DuggerSpivak.Mapping} [[Dan Dugger]], [[David Spivak]], *Mapping spaces in quasi-categories*, Algebr. Geom. Topol. **11** (2011) 263-325 &lbrack;[arXiv:0911.0469](http://arxiv.org/abs/0911.0469), [doi:10.2140/agt.2011.11.263](http://dx.doi.org/10.2140/agt.2011.11.263)&rbrack;


More along these lines is in 

* [[Emily Riehl]], *On the structure of simplicial categories associated to quasi-categories*, Math. Proc. Camb. Phil. Soc. **150** (2011) 489-504 &lbrack;[arXiv:0912.4809](https://arxiv.org/abs/0912.4809), [doi:10.1017/S0305004111000053](https://doi.org/10.1017/S0305004111000053)&rbrack;


An expository account is in Section 7.8

* {#Bergner18} [[Julie Bergner]], _The homotopy theory of (∞,1)-categories_, London Mathematical Society Student Texts 90, 2018.


See also

* {#Hinich} [[Vladimir Hinich]], _Simplicial nerve in Deformation theory_ ([arXiv:0704.2503](http://arxiv.org/abs/0704.2503))
 
[[!redirects relation between quasi-categories and sSet-enriched categories]]


[[!redirects relation between sSet-enriched categories and quasi-categories]]

