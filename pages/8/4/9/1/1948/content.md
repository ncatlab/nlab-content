
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

The [[model category]] structures on [[functor category|functor categories]] are models for [[(∞,1)-category of (∞,1)-functors|(∞,1)-categories of (∞,1)-functors]].

For $C$ a [[model category]] and $D$ any [[small category]] there are two "obvious" ways to put a [[model category]] structure on the [[functor category]] $[D,C]$, called the _projective_ and the _injective_ model structures.  For completely general $C$, neither one need exist.  The projective model structure exists as long as $C$ is [[cofibrantly generated model category|cofibrantly generated]], while the injective model structure exists as long as $C$ is [[combinatorial model category|combinatorial]].

A related kind of model structure is the [[Reedy model structure]]/[[generalized Reedy model structure]] on functor categories, which applies for *any* model category $C$, but requires $D$ to be a very special sort of category, namely a [[Reedy category]]/[[generalized Reedy category]].
  
In the special case that $C = $ [[SSet]] is the standard [[model structure on simplicial sets|model category of simplicial sets]] the projective and injective model structure on the functor categories $[D,SSet]$ are described in more detail at [[global model structure on simplicial presheaves]].

## Definition

+-- {: .num_defn #ProjectiveAndInjectiveStructure}
###### Definition

For $C$ a [[combinatorial model category]] or, in the projective case, just a [[cofibrantly generated model category]], and $D$ a [[small category]] there exist the following two (combinatorial) model category structures on the [[functor category]] $[D,C]$:

* the **projective** structure $[D,C]_{proj}$: weak equivalences and fibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. 

* the **injective** structure $[D,C]_{inj}$: weak equivalences and cofibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. 

More generally, if $C$ is in addition a [[simplicial model category]] and $D$ a smooth [[sSet]]-[[enriched category]], then the [[sSet]]-[[enriched functor category]], also denoted $[D,C]$, carries the above two model strutures.

=--



## Properties

In all of the following, let $\mathbf{S}$ be an [[excellent model category]]. The standard example is the [[model structure on simplicial sets]], $sSet_{Quillen}$. 

Let $D$ (and $D_1$, $D_2$, ...) be a [[combinatorial model category|combinatorial]] $\mathbf{S}$-[[enriched model category]].

Moreover, $C$ in the following is assumed to be either an ordinary [[small category]], or, more generally, it is a small $\mathbf{S}$-[[enriched category]].

If $\mathbf{S} = $ [[sSet]]${}_{Quillen}$ and $C$ is an ordinary small category, then then model structures discussed here are instances of the [[model structure on simplicial presheaves]]. If $C$ is itself $sSet$-enriched, then they are instances of the [[model structure on sSet-enriched presheaves]].

### General 

+-- {: .num_prop}
###### Proposition

The projective and injective structures $[D,C]_{proj}$ and $[D,C]_{inj}$, def. \ref{ProjectiveAndInjectiveStructure}

* are indeed [[model category]] structures;

* are themselves [[combinatorial model category|combinatorial model categories]];

* are right or left [[proper model categories]] if $C$ is right or left proper, respectively.

* are $\mathbf{S}$-[[enriched model categories]] (e.g.[[simplicial model categories]]) with respect to the $\mathbf{S}$-[[enriched category|enrichment]] for which the $\mathbf{S}$-[[tensoring]] is objectwise that of $C$.

=--


The existence of the unenriched model structure apears as [[Higher Topos Theory|HTT, prop. A.2.8.2]]
The enriched case is [[Higher Topos Theory|HTT, prop. A.3.3.2]] and the remarks following that.
The statement about properness appears as [[Higher Topos Theory|HTT, remark A.2.8.4]].

### Cofibrant generation

+-- {: .num_prop}
###### Proposition


Let $C$ be an ordinary [[small category]].

The cofibrations in $[C, A]_{proj}$ are generated from (i.e. are the [[weakly saturated class of morphisms]] defined by) the morphisms of the form

$$
  Id_{C(c,-)}\cdot i :  C(c,-)\cdot a \to C(c,-) \cdot b
$$

for all $c \in C$ and $i : a \to b$ a generating cofibration in $A$. Here the dot denotes the tensoring of $A$ over sets, i.e. $C(c,-)\cdot a$ is the functor that sends $c' \in C$
to the [[coproduct]] $\coprod_{C(c,c')} A$ of $|C(c,c')|$ copies of $A$.

In particular, every cofibration if $[C,A]_{proj}$ is in particular a cofibration in $[C,A]_{inj}$. Similarly, every fibration in $[C,A]_{inj}$ is in particular a fibration in $[C,A]_{proj}$

=--

This is argued in the beginning of the proof of [[Higher Topos Theory|HTT, lemma A.2.8.3]].


### Relation to other model structures

+-- {: .num_cor}
###### Corollary

The [[identity]] [[functor]]s

$$
  [D,C]_{inj}   
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{proj}
$$

form a [[Quillen equivalence]] (with $Id : [D,C]_{proj} \to [D,C]_{inj}$ being the left Quillen functor).

If $D$ is a [[Reedy category]] this factors through the [[Reedy model structure]]

$$
  [D,C]_{inj}   
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{Reedy}
    \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{proj}
$$

=--

### Functoriality in domain and codomain

+-- {: .num_prop #QuillenFunctorialityInCodomain}
###### Proposition

The functor model structures depend [[Quillen adjunction|Quillen-functorially]] on their [[codomain]], in that for

$$
  D_1 \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D_2
$$

a $\mathbf{S}$-[[enriched Quillen adjunction]] between [[combinatorial model categories|combinatorial]] $\mathbf{S}$-[[enriched model categories]], postcomposition induces $\mathbf{S}$-[[enriched Quillen adjunctions]]

$$
  [C,D_1]_{proj} \stackrel{\overset{[C,L]}{\leftarrow}}{\underset{[C,R]}{\to}} [C,D_2]_{proj}  
$$

and

$$
  [C,D_1]_{inj} \stackrel{\overset{[C,L]}{\leftarrow}}{\underset{[C,R]}{\to}} [C,D_2]_{inj}  
  \,.
$$

Moreover, if $(L \dashv R)$ is a [[Quillen equivalence]], then so is $([C,L] \dashv [C,R])$.

=--

For the case that $C$ is a small category this is ([Lurie, remark A.2.8.6](#Lurie)), for the enriched case this is ([Lurie, prop. A.3.3.6](#Lurie)).



The Quillen-functoriality on the domain is more asymmetric. 

+-- {: .num_prop}
###### Proposition

For $p : C_1 \to C_2$ a functor between small categories or an $\mathbf{S}$-[[enriched functor]] between $\mathbf{S}$-[[enriched categories]], let 

$$
  (p_! \dashv p^* \dashv p_*) :  [C_2,D] 
  \stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^*}{\to}}{\underset{p_*}{\leftarrow}}}
 [C_1,D]
$$ 

be the [[adjoint triple]] where $p^*$ is precomposition with $p$ and where $p_!$ and $p_*$ are left and right [[Kan extension]] along $p$, respectively.

Then we have [[Quillen adjunctions]]

$$
  (p_! \dashv p^*) :
  [C_1,D]_{proj} \stackrel{\overset{p_!}{\to}}{\underset{p^*}{\leftarrow}}
  [C_2,D]_{proj}
$$

and

$$
  (p^* \dashv p_*) :
  [C_1,D]_{inj} \stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}}
  [C_2,D]_{inj}
  \,.
$$


=--

For $C$ not enriched this appears as ([Lurie, prop. A.2.8.7](#Lurie)), for the enriched case it appears as ([Lurie, prop. A.3.3.7](#Lurie)).

+-- {: .num_remark } 
###### Remark

In the $sSet$-enriched case, if $p : D_1 \to D_2$ is an [[weak equivalence]] in the [[model structure on sSet-categories]], then these two Quillen adjunctions are both [[Quillen equivalence]]s.

=--

+-- {: .num_prop #PresentationOfInfinityFunctors} 
###### Proposition

For $C$ a [[combinatorial simplicial model category]], the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $[D,C]_{proj}$ and $[D,C]_{inj}$ under the above assumptions is the [[(∞,1)-category of (∞,1)-functors]] $Func(D,C^\circ)$ from the ordinary category $D$ to the $(\infty,1)$-category presented by $C$.

=--

See [[(∞,1)-category of (∞,1)-functors]] for details.


### Relation to homotopy Kan extensions/limits/colimits

Often functors $D \to C$ are thought of as [[diagram]]s in the model category $C$, and one is interested in obtaining their [[homotopy limit]] or [[homotopy colimit]] or, generally, for $p : D \to D'$ any functor, their left and right [[homotopy Kan extension]].

These are the left and right [[derived functor]]s $HoLan := \mathbb{L} p_1$ and $HoRan := \mathbb{R} p_*$ of

$$
  [D,C]_{proj} \stackrel{p_!}{\to}  [D',C]_{proj}
$$

and

$$
  [D,C]_{inj} \stackrel{p_*}{\to} [D',C]_{inj}
$$

respectively.

For more on this see [[homotopy Kan extension]]. For the case that $D' = *$ this reduces to [[homotopy limit]] and [[homotopy colimit]].

## Examples

Examples of cofibrant objects in the projective model structure are discussed at 

* [[projectively cofibrant diagram]].

## Related concepts

* [[Reedy model structure]], [[generalized Reedy model structure]],

* [[model structure on homotopical presheaves]], [[model structure on simplicial presheaves]]

## References

The plain situation is the topic of section A.2.8 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

The enriched situation is section A.3.3 there.

See also 

* [[David White]], _Modified projective model structure_ ([MO comment](http://mathoverflow.net/questions/76160/acyclic-models-via-model-categories/104423#104423))

[[!redirects model structures on functors]]

[[!redirects injective model structure]]
[[!redirects projective model structure]]
[[!redirects projective model structure on functors]]

[[!redirects projective model structure on functors]]


[[!redirects global model structures on functor categories]]
[[!redirects global model structure on functors]]
