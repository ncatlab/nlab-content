
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

The [[model category]] structures on [[functor category|functor categories]] are models for [[(∞,1)-category of (∞,1)-functors|(∞,1)-categories of (∞,1)-functors]].

For $C$ a [[model category]] and $D$ any [[small category]] there are two "obvious" ways to put a [[model category]] structures on the [[functor category]] $[D,C]$, called the _projective_ and the _injective_ model structure.  For completely general $C$, neither one need exist.  The projective model structure exists as long as $C$ is [[cofibrantly generated model category|cofibrantly generated]], while the injective model structure exists as long as $C$ is [[combinatorial model category|combinatorial]].

A related kind of model structure is the [[Reedy model structure]] on functor categories, which applies for *any* model category $C$, but requires $D$ to be a very special sort of category.  See the link for further information.

In the special case that $C = $ [[SSet]] is the standard [[model structure on simplicial sets|model category of simplicial sets]] the projective and injective model structure on the functor categories $[D,SSet]$ are described in more detail at [[global model structure on simplicial presheaves]].

## Definition


+-- {: .un_defn}
###### Definition

For $C$ a [[combinatorial model category]] (or, in the projective case, merely cofibrantly generated) and $D$ a [[small category]] there exists the following two (combinatorial) model category structures on the [[functor category]] $[D,C]$:

* the **projective** structure $[D,C]_{proj}$: weak equivalences and fibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. 

* the **injective** structure $[D,C]_{inj}$: weak equivalences and cofibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. 

More generally, if $C$ is in addition a [[simplicial model category]] and $D$ a smooth [[sSet]]-[[enriched category]], then the [[sSet]]-[[enriched functor category]], also denoted $[D,C]$, carries the above two model strutures.

=--



## Properties


+-- {: .un_prop}
###### Proposition

For $C$ a [[combinatorial model category]] and $D$ a [[small category]] the projective and injective structures $[D,C]_{proj}$ and $[D,C]_{inj}$ 

* are indeed [[model category]] structures;

* are themselves [[combinatorial model category|combinatorial model categories]];

* are right or left [[proper model categories]] of $C$ is right or left proper, respectively.

* are [[simplicial model categories]] if $C$ is a [[simplicial model category]], with respect to the [[sSet]]-[[enriched category|enrichment]] for which the [[sSet]]-[[copower|tensoring]] is objectwise that of $C$.

The cofibrations in $[C, A]_{proj}$ are generated from (i.e. are the [[weakly saturated class of morphisms]] defined by) the morphisms of the form

$$
  Id_{C(c,-)}\cdot i :  C(c,-)\cdot a \to C(c,-) \cdot b
$$

for all $c \in C$ and $i : a \to b$ a generating cofibration in $A$. Here the dot denotes the tensoring of $A$ over sets, i.e. $C(c,-)\cdot a$ is the functor that sends $c' \in C$
to the [[coproduct]] $\coprod_{C(c,c')} A$ of $|C(c,c')|$ copies of $A$.

In particular, every cofibration if $[C,A]_{proj}$ is in particular a cofibration in $[C,A]_{inj}$. Similarly, every fibration in $[C,A]_{inj}$ is in particular a fibration in $[C,A]_[proj}$

So the identity functors

$$
  [D,C]_{proj} \stackrel{\overset{Id}{\leftarrow}}{\underset{Id}{\to}}
  [D,C]_{inj}
$$

form a [[Quillen equivalence]] (with $Id : [D,C]_{proj} \to [D,C]_{inj}$ being the right Quillen functor).

The functor model structures depend Quillen-functorially on their codomain, in that for

$$
  C_1 \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} C_2
$$

a [[Quillen adjunction]] between [[combinatorial model categories]], composition induces [[Quillen adjunction]]s

$$
  [D,C_1]_{proj} \stackrel{\overset{[D,L]}{\leftarrow}}{\underset{[D,R]}{\to}} [D,C_2]_{proj}  
$$

and

$$
  [D,C_1]_{inj} \stackrel{\overset{[D,L]}{\leftarrow}}{\underset{[D,R]}{\to}} [D,C_2]_{inj}  
  \,.
$$

If $(L \dashv R)$ is [[sSet]]-enriched, then so is $([D,L] \dashv [D,R])$.

The Quillen-functoriality on the domain is more asymmetric: for $p : D_1 \to D_2$ a morphism of small categories, and $p^* = [p,C] : [D_2,C] \to [D_1,C]$, we have [[Quillen adjunction]]s

$$
  (p_! \dashv p^*) :
  [D_1,C]_{proj} \stackrel{\overset{p_!}{\to}}{\underset{p^*}{\leftarrow}}
  [D_2,C]_{proj}
$$

and

$$
  (p^* \dashv p_*) :
  [D_1,C]_{inj} \stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}}
  [D_2,C]_{inj}
  \,.
$$

In the $sSet$-enriched case, if $p : D_1 \to D_2$ is an equivalence in the [[model structure on sSet-categories]], then these two Quillen adjunctions are both [[Quillen equivalence]]s.

=--

+-- {: .proof}
###### Proof

For the unenriched case this is [[Higher Topos Theory|HTT, prop A.2.8.2]] and the following remarks. The enriched case is [[Higher Topos Theory|HTT, prop. A.3.3.2]] and the remarks following that.

=--



+-- {: .un_prop}
###### Proposition

For $C$ a [[combinatorial simplicial model category]], the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $[D,C]_{proj}$ and $[D,C]_{inj}$ under the above assumptions is the [[(∞,1)-category of (∞,1)-functors]] $Func(D,C^\circ)$ from the ordinary category $D$ to the $(\infty,1)$-category presented by $C$.

=--

+-- {: .proof}
###### Proof

See [[(∞,1)-category of (∞,1)-functors]] for details.

=--

## Relation to homotopy Kan extensions/limits/colimits

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

## References

The plain situation is the topic of section A.2.8 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The enriched situation is section A.3.3 there.

[[!redirects model structures on functors]]
[[!redirects injective model structure]]
[[!redirects projective model structure]]
[[!redirects global model structures on functor categories]]
[[!redirects global model structure on functors]]
