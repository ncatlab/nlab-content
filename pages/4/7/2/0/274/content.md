
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

The notion of _Segal category_ is one of the models for that of _[[(∞,1)-category]]_, given by regarding an $(\infty,1)$-category as an [[∞Grpd]]-[[enriched (∞,1)-category]].

So the notion can be understood as modelling the notion of an [[sSet]]-[[enriched category|enrichment]] _up to [[coherence|coherent]] [[homotopy]]_, i.e. a _weak_ enrichment. As such it is closely related to the notion of [[complete Segal space]], which models the notion of an [[internal category in an (∞,1)-category|internal category]] in [[sSet]].

Indeed, Segal categories may be considered with enrichment not just over [[sSet]], but over other suitable [[model categories]]. In particular, an iterated enrichment over itself gives rise to the notion of _[[Segal n-category]]_ which is a model for _[[(∞,n)-categories]]_.

Since the major difference between ([[small category|small]])
$\mathcal{V}$-[[enriched categories]] and $\mathcal{V}$-[[internal categories]] is that in the first case the [[objects]] (as opposed to all the [[hom objects]]) form an ordinary [[set]], while in the second these form an object of $\mathcal{V}$, too, accordingly the definition of _Segal category_ is like that of _([[complete Segal space|complete]]) [[Segal space]]_, only that the simplicial set of objects is required to be an ordinary set (a [[discrete object|discrete]] simplicial set).

## Definition

+-- {: .num_def}
###### Definition

A **Segal category** is 

* a [[simplicial object|simplicial]] [[simplicial set]] ($\simeq$ [[bisimplicial set]]) $X \in [\Delta^{op}, sSet]$, 

  where we call $X_0$ the _simplicial set of [[objects]]_, $X_1$ the _simplicial set of [[morphisms]]_;  and $X_k$ for $k \geq 2$ the _simplicial set of sequences of composable morphisms of length $k$_;

* such that $X_0$ is a [[discrete object|discrete]] (= constant) simplicial set;

* and such that the [[Segal maps]]

  $$ 
    X^{Sp[k] \hookrightarrow \Delta[k]}
     :
     X_k 
       \stackrel{\simeq}{\to}    
     X_1 \times_{X_0} \cdots \times_{X_0} X_1 \;\;(k factors)
  $$

(With the defintion of X_k, shouldn't X_k be equal to X_1 \times_{X_0}... X_1?)

  induced by the [[spine]] inclusions $Sp[k] \hookrightarrow \Delta[k]$ are [[model structure on simplicial sets|weak equivalences of simplicial sets]] for $k \geq 2$.

=--

+-- {: .num_remark}
###### Remark

There is _no_ condition that a Segal category be [[fibrant object|fibrant]] with respect to the [[Reedy model structure]] on bisimplicial sets. 

=--

+-- {: .num_remark}
###### Remark

For $X$ a Segal category, the [[fiber product]] simplicial set $X_1 \times_{X_0} X_1$ is manifestly the space of pairs of composable 1-[[morphism]]s in $X$, and the [[weak equivalence]] 

$$
  (d_0,d_2) 
    :  
  X_2 \stackrel{\simeq}{\to} X_1 \times_{X_0} X_1 
$$ 

given by the above definition together with the remaining face map $d_1 : X_2 \to X_1$ constitutes an [[∞-anafunctor]]

$$
  \circ : X_1 \times_{X_0} X_1 &#8696; X_1
$$

given by the [[span]]

$$
  \array{
    X_2 &\stackrel{d_1}{\to}& X_1
    \\
    {}^{\mathllap{\simeq}}\downarrow
    \\
    X_1 \times_{X_0} X_1
  }
  \,.
$$

This encodes the [[composition]] operation in the Segal category $X$. 

Accordingly, the analogous spans out of $X_k$ for $k \geq 3$ encode the [[associativity]] of this composition as well as all its [[coherence|coherences]].

=--

## Properties

### Model category structure

The category of [[bisimplicial sets]] carries a [[model category]] structure whose [[fibrant objects]] are the [[Reedy model structure|Reedy fibrant]] Segal categories. This _[[model structure for Segal categories]]_ is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-categories]].

### Operadic version

The [[operad|operadic]] generalization of Segal category is that of _[[Segal operad]]_. Segal categories are precisely those Segal operads whose only [[inhabited set|inhabited]] operations-spaces are those of unary operations.

## Examples

### Inclusion of ordinary categories

Let $C$ be an ordinary [[small category]] and write $N(C) \in sSet$ for its [[nerve]]. Regard this as a bisimplicial set under the inclusion $sSet \simeq [\Delta^{op}, Set] \hookrightarrow [\Delta^{op}, sSet]$. 
 
Then $N(C)$ is a Segal category. Each simplicial set $N(C)_k$ is discrete, for all $k \in \mathbb{N}$, and all the morphisms

$$
  N(C)_k \to Mor(C) \times_{Obj(C)} \cdots \times_{Obj(C)} Mor(C)
$$

are in fact [[isomorphisms]] / [[bijections]] of sets. This property of the [[nerve]] of an ordinary category goes by the name _Segal condition_ and is what gave Segal categories its name.

One may also form the $n$-fold [[comma object]]-fiber product of a choice of base points $\pi_0(C) \to C$ with itself. This yields a Segal category incarnation of $C$ where in degree 1 we have the [[groupoid]] [[core]] of the [[arrow category]] of $C$. For more on this see at _[Segal space -- Examples - From a category](Segal+space#ConstructionFromACategory)_.

## Related concepts

* [[complete Segal space]]

* [[Gamma space]]

* [[Segal operad]]

* [[table - models for (infinity,1)-operads]]


## References

The idea of Segal categories goes back (implicitly) to

* [[Graeme Segal]], _Categories and cohomology theories_, Topology **13** 3 (1974) 293-312 &lbrack;<a href="https://doi.org/10.1016/0040-9383(74)90022-6">doi:10.1016/0040-9383(74)90022-6</a>&rbrack;

and is explicit in

* {#DwyerKanSmith89} [[William Dwyer]], [[Daniel Kan]], [[Jeff Smith]], *Homotopy-commutative diagrams and their realizations*, Journal of Pure and Applied Algebra **57** 1 (1989) 5-24 &lbrack;<a href="https://doi.org/10.1016/0022-4049(89)90023-6">doi:10.1016/0022-4049(89)90023-6</a>&rbrack;

as kind of bisimplicial sets "which are 'special' in the sense that they satisfy a slight variation on a condition of Segal" (But the terminology "*Segal category*" is not used in [Dwyer, Kan & Smith 1989](#DwyerKanSmith89).)

Discussion in the broader context of *[[Segal n-categories|Segal $n$-categories]]*:

* [[André Hirschowitz]], [[Carlos Simpson]], *Les $n$-catégories de Segal*, §2 in: _Descente pour les $n$-champs (Descent for $n$-stacks)_ &lbrack;[arXiv:9807049](http://arxiv.org/abs/math/9807049)&rbrack;

Discussion with emphasis on the comparison of the various [[model category]] presentations of [[(infinity,1)-categories|$(\infty,1)$-categories]]:

* [[Julie Bergner]], *Segal Categories*, §5 in: _A survey of $(\infty,1)$-categories_, In: [[John Baez]], [[Peter May]] (eds.),  _[[Towards Higher Categories]]_, The IMA Volumes in Mathematics and its Applications **152**, Springer (2007) &lbrack;[arXiv:math/0610239](http://arxiv.org/abs/math/0610239), [doi:10.1007/978-1-4419-1524-5_2](https://doi.org/10.1007/978-1-4419-1524-5_2)&rbrack;

* {#Joyal08} [[André Joyal]], pp 164-169 in: *[[The Theory of Quasi-Categories and its Applications]]*, lectures at *[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)*, CRM (2008) &lbrack;[pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]]&rbrack;


Discussion in the context of [[enriched (∞,1)-categories]]:

* [[Carlos Simpson]], _[[Homotopy Theory of Higher Categories]]_ ([arXiv:1001.4071](http://arxiv.org/abs/1001.4071))

* {#Lurie} [[Jacob Lurie]], section 2 of: _(Infinity,2)-Categories and the Goodwillie Calculus I_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 


[[!redirects Segal categories]]

[[!redirects Segal groupoid]]
[[!redirects Segal groupoids]]