
# Contents
* table of contents
{: toc}

## Idea

What is known as _(Grothendieck's) six operations_ is a formalization of structure that 

* assigns to every [[morphism]] $f$ of suitable [[spaces]] a [[direct image]]/[[inverse image]] [[adjunction]] $(f^\ast \dashv f_*)$;

* assigns to every [[separated morphism]] a [[direct image with compact support]]/[[Verdier duality|Verdier dual]] [[adjunction]] $(f_! \dashv f^!)$.

These are _four operations_ and together with

* a [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] [[tensor product]]/[[internal hom]] [[adjunction]] $(\otimes X \dashv [X,-])$ 

form _six operations_. 

(All this is usually interpreted as [[derived functors]]/[[(infinity,1)-functors]] so that for instance in the usual application to [[derived categories]] of [[abelian sheaves]] the last two operations are really [[Tor]] and [[Ext]].) 

With a list of compatibility conditions between these (for instance ([Cisinski-D&#233;glise 09, p. x](#CisinskiDelglise09)) this is a structure of _Grothendieck's six operations_.

These consistency conditions include the following:

1. The addjunctions are functorial, hence form [[2-functors]] $f \mapsto f_*$, $f \mapsto f_!$:

1. There is a [[natural transformation]]  $f_! \to f_*$ which is a [[natural equivalence]] when $f$ is a [[proper map]]. 

1. [[Beck-Chevalley condition]]: given a ([[homotopy pullback|homotopy]]) [[pullback]] [[diagram]]

   $$
     \array{
       && Q_1 \underset{X}{\times} Q_2
       \\
       & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
       \\
       Q_1 && && Q_2
       \\
       & {}_{\mathllap{f}}\searrow && \swarrow_{\mathrlap{g}}
       \\
       && X
     }
   $$

   such that $f$ is a [[separated morphism]], then there are [[natural equivalences]]

   $$
     g^\ast \circ f_! \simeq (p_2)_! \circ (p_1)^\ast
   $$

   $$
     f^! \circ g_\ast \simeq (p_1)_\ast\circ (p_2)^!
     \,. 
   $$

1. ...

([Cisinski-D&#233;glise 09, p. x](#CisinskiDelglise09))

Morover one imposes a formalization of [[Verdier duality]] with [[dualizing object]]...

([Cisinski-D&#233;glise 09, p. xi](#CisinskiDelglise09))

## Properties

### Relation to motives

According to [CisinskiD&#233;lglise 09](#CisinskiDelglise09) the [[initial object]] in the [[(infinity,2)-category]] of functors to [[stable (infinity,1)-categories]] which satisfy the _six  operations_ formalism (and a bit more, such that [[A1-homotopy theory|A1-locality]]) is the _[[motive]]_ category. See there for more.

## Related concepts

* [[Grothendieck duality]], [[Verdier duality]]

## References

A general abstract discussion is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_ ([pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))

The traditional applications are discussed in

* Yves Laszlo, Martin Olsson, _The six operations for sheaves on Artin stacks I: Finite Coefficients_ ([arXiv:math/0512097](http://arxiv.org/abs/math/0512097))

* [[Yoseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescants dans le monde motivique_ PhD thesis, Paris ([pdf](http://www.math.uiuc.edu/K-theory/0761/THESE.pdf))

A quick list of the axioms with a  Grothendieck's six operations with an eye towards the definition of [[motives]] is in section A.5 of 

* [[Denis-Charles Cisinski]], Fr&#233;d&#233;ric D&#233;glise, _Triangulated categories of mixed motives_ ([arXiv:0912.2110](http://arxiv.org/abs/0912.2110))
 {#CisinskiDelglise09}


[[!redirects six operations]]
[[!redirects Grothendieck's six operations]]
[[!redirects Grothendieck\'s six operations]]
[[!redirects Grothendieck's six operations]]
[[!redirects yoga of six functors]]
[[!redirects yoga of six operations]]
