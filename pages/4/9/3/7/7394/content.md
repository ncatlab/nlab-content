
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A [[model category]] structure whose fibrant objects are [[Segal categories]]. This is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category]] [[(∞,1)Cat]] from the point of view of (weakly) [[∞Grpd]]-[[enriched categories]].

## Definition

Write $PreSegalCat \hookrightarrow [\Delta^{op}, sSet]$ for the full [[subcategory]] on those bisimplicial sets $X$ for which $X_0$ is a discrete simplicial set (the "precategories").

The [[nerve]] functor 

$$
  N : Cat \to PreSegalCat
$$

has a [[left adjoint]] ("fundamental category" functor)

$$
  \tau_1 : PreSegalCat \to Cat
  \,.
$$

+-- {: .num_defn}
###### Definition

Say a morphism $f : X \to Y$ in $PreSegalCat$ is

* [[full and faithful functor|full and faithful]] if for all $a,b \in X_0$ the induced morphism

  $$
    X(a,b) \to X(f(a),f(b))
  $$

  is a [[weak homotopy equivalence]] of simplicial sets;

  * _essentially surjective_ if $\tau_1(f)$ is [[essentially surjective functor|essentially surjective]].

  * a _categorical equivalence_ if it is both full and faithful as well as essentially surjective.

=--

There is a completion functor

$$
  compl : PreSegalCat \to PreSegalCat
$$

which [[free construction|freely completes]] a pre-Segal category to a [[Segal category]]. (...)

+-- {: .num_defn #CofibrationsAndEquivalences}
###### Definition

Say a morphism $f : X \to Y$ in $PreSegalCat$ is

* a cofibration precisely if it is a [[monomorphism]];

* a weak equivalence precisely if its completion $compl(f)$ is a categorical equivalence.

=--

(...)

## Properties

### General 

+-- {: .num_prop }
###### Proposition

Equipped with the classes of maps defined in def. \ref{CofibrationsAndEquivalences}, $PreSegalCat$ is a [[model category]] which is 

* [[left proper model category|left proper]];

* [[cartesian monoidal category|cartesian]] [[monoidal model category|monoidal]];

* a [[Cisinski model structure]].

=--

Cartesian closure is shown in ([Pellissier](#Pellissier)). The fact that it is a Cisinski model structure follows from the result in ([Bergner](#Bergner)).


### Relation to other model structures

See _[[table - models for (infinity,1)-categories]]_.


## Related concepts

* [[model structure for Segal operads]]

## References

The model structure for Segal categories was introduced in

* [[André Hirschowitz]], [[Carlos Simpson]], _Descente pour les $n$-champs (Descent for $n$-stacks)_ ([arXiv:9807049](http://arxiv.org/abs/math/9807049))
 {#HS}

(even for [[Segal n-categories]]). An alternative proof of the existence of this model structure is given in section 5 of 

* [[Julie Bergner]], _Three models for the homotopy theory of homotopy theories_ ([arXiv:math/0504334](http://arxiv.org/abs/math/0504334))

The cartesian closure of the model structure was established in 

* Regis Pellissier. Cat&#233;gories enrichies faibles. Th&#232;se, Universit&#233; de Nice-Sophia Antipolis (2002), ([arXiv:math/0308246](http://arxiv.org/abs/math/0308246))
 {#Pellissier}

The fact that the fibrant Segal categories in this model structure are precisely the [[Reedy model structure|Reedy fibrant]] bisimplicial sets is due to

* [[Julie Bergner]], _A characterization of fibrant Segal categories_, Proceedings of the AMS (2007) ([arXiv:0603400](http://arxiv.org/abs/math/0603400), [pdf](http://www.math.ucr.edu/~jbergner/ReedyFib.pdf))
 {#Bergner}

