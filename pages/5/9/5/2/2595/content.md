
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Since a [[topos]] is a [[cartesian monoidal category]], the notion of a unital [[ring]] and commutative unital ring can be defined [[internalization|internal]] to it.

A _ringed topos_ $(X,\mathcal{O}_{X})$ is a topos $X$ equipped with a choice of ring object $\mathcal{O}$. If $X$ is a [[sheaf topos]] over a [[site]] $C$ then $\mathcal{O}_X$ is a [[sheaf]] of rings on $C$: a [[structure sheaf]].

The notion of ringed topos makes sense for the theory of rings replaced by any [[Lawvere theory]]. Moreover, it makes sense for higher toposes such as [[(∞,1)-topos]]es. This is described at [[structured (∞,1)-topos]].

## Definition


+-- {: .num_defn}
###### Definition

A **ringed topos** $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is 

* a [[topos]] $\mathcal{X}$ 

* equipped with a distinguished unital [[ring object]] $\mathcal{O}_{\mathcal{X}} \in \mathcal{X}$: a [[ring]] [[internalization|internal to]] the topos.

If all [[stalk]]s of $\mathcal{O}_{\mathcal{X}}$ are [[local ring]]s, $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is a called a **[[locally ringed topos]]**.

A morphism of ringed toposes $(f, \eta) : (\mathcal{X}, \mathcal{O}_{\mathcal{X}}) \to (\mathcal{Y}, \mathcal{O}_{\mathcal{Y}})$ is

* a [[geometric morphism]]

  $$
    (f^* \dashv f_*) : \mathcal{X} \to \mathcal{Y}
  $$

* and a morphism of ring objects in $\mathcal{X}$

  $$
    \eta : f^* \mathcal{O}_{\mathcal{Y}} \to \mathcal{O}_{\mathcal{X}}
  $$

  which is equivalently, by the $(f^* \dashv f_*)$-[[adjunction]], a morphism of ring objects

  $$ 
    \tilde \eta : \mathcal{O}_{\mathcal{Y}} \to f_* \mathcal{O}_{\mathcal{X}}
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

The usual variants apply: we can speak of toposes equipped with, specifically, commutative ring objects, unital/nonunital ring objects, ring objects under other ring objects, hence [[associative algebra]] objects.

=--

+-- {: .num_remark}
###### Remark

Let $PSh((CRing^{fg})^{op})$ be the [[classifying topos]] for the [[Lawvere theory]] of [[ring]]s.  Then 

* a ringed topos $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is a [[geometric morphism]]

  $$
    \mathcal{O}_{\mathcal{X}} : \mathcal{X} \to PSh((CRing^{fg})^{op})
    \,,
  $$

* a morphism $(f,\eta) : (\mathcal{X}, \mathcal{O}_{\mathcal{X}}) \to (\mathcal{Y}, \mathcal{O}_{\mathcal{Y}})$ is a [[diagram]]

  $$
    \array{
      \mathcal{X} &&\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}&& \mathcal{Y}
      \\
      & {}_{\mathllap{}}\searrow \nwarrow^{\mathrlap{\mathcal{O}_{\mathcal{X}}}}
      &\swArrow_{\eta}&
     \swarrow \nearrow_{\mathcal{O}_{\mathcal{Y}}}
      \\
      && PSh((CRing^{fg})^{op})
    }
  $$

  in the [[2-category]] [[Topos]].

So the [[2-category]] of ringed toposes is the [[lax slice 2-category]] $Topos/PSh((CRing^{fp})^{op})$.


=--

More generally:

+-- {: .num_defn}
###### Definition

For $T$ a [[Lawvere theory]], a $T$-ringed topos is a [[topos]] $X$ together with a [[product]]-preserving [[functor]] $\mathcal{O}_X : T \to X$.

=--

See [[locally algebra-ed topos]] for more on this.

In order to say what _locally_ $T$-ringed means, one needs the extra structure of a [[geometry (for structured (infinity,1)-toposes)|geometry]] on $T$. See there for details.


## Examples

* A [[ringed space]] $(X,\mathcal{O})$ induces the ringed [[localic topos]] $(Sh(X),\mathcal{O})$ of [[sheaf|sheaves]] on the [[category of open subsets]] of the [[topological space]] $X$. 

  Similarly but more generally a  [[ringed site]] $(S, \mathcal{O})$ induces the ringed [[Grothendieck topos]] $(Sh(S), \mathcal{O})$.

* In some applications the ringed topos is refined to a [[lined topos]] when instead of a [[ring]] object an [[algebra]]-object is required.

* For $A \in Alg$ any (possibly non-commutative) algebra, let $\mathcal{C}(A)$ be its [[poset of commutative subalgebras]]. The [[presheaf topos]] $[\mathcal{C}(A), Set]$ naturally carries the commutative ring object $\underline A : (C \in \mathcal{C}(A)) \mapsto C$. This example appears in the description of [[state]]s in [[quantum mechanics]] after "[[Bohrification]]".


## Properties
 {#Properties}

### Limits and colimits
 {#LimitsAndColimits}

+-- {: .num_prop}
###### Proposition

Let $J \to RingedTopos$ be a [[diagram]] of ringed toposes. Its [[limit]] exists and is given by

* the limiting topos 

  $$
    {\lim_\leftarrow}_j (\mathcal{X}_j, \mathcal{O}_{\mathcal{X}_j})    
    \stackrel{p_j}{\to}
    (\mathcal{X}_j, \mathcal{O}_{\mathcal{X}_j})
  $$

  of the underlying diagram $J \to RingedTopos \stackrel{}{\to} $ [[Topos]];

* equipped with the [[colimit]]ing [[ring object]] of all the [[inverse image]] rings

  $$
    {\lim_\to}_j p_j^* \mathcal{O}_{\mathcal{X}_j}
    \in
    {\lim_\leftarrow}_j \mathcal{X}_j
    \,.
  $$

=--

In more detail: let

$$
  \array{
    && (\mathcal{Y}, \mathcal{O}_{\mathcal{Y}})
    \\
    & {}^{\mathllap{f_i}}\swarrow &{}^{\mathllap{\simeq}}\swArrow_{\rho}& \searrow^{\mathrlap{f^j}}
    \\
   (\mathcal{X}_i, \mathcal{O}_{\mathcal{X}_i})
   &&\underset{h_{i j}}{\to}&&
   (\mathcal{X}_j, \mathcal{O}_{\mathcal{X}_j})
  }
$$

be a [[cone]] in $RingedTopos$, then this induces the cocone of ring objects in $\mathcal{Y}$

$$
  \array{
     f_i^* \mathcal{O}_{\mathcal{X}_i}
     &
      \stackrel{f_i^*(h_{i j}^* \mathcal{O}_{\mathcal{X}_j} \to \mathcal{O}_{\mathcal{X}_i} )}{\leftarrow}
     &
     f_j^* h_{i j}^* \mathcal{O}_{\mathcal{X}_j}
     &\underoverset{\simeq}{\rho_{\mathcal{O}_{\mathcal{X}_j}}}{\leftarrow}&
     f_j^* \mathcal{O}_{\mathcal{X}_j}
     \\
     & \searrow && \swarrow
     \\
     && \mathcal{O}_{\mathcal{Y}}
  }
$$

whose commutativity may be understood as being the 2-commutativity of the prism in [[Topos]] over the [[classifying topos]] $PSh(CRing_{fg}^{op})$ with rear side faces $\eta_i$ and $\eta_j$, with front face $\eta_{i j}$ (corresponding to $h_{i j}$) and top face $\rho$.

+-- {: .proof}
###### Proof

We check the [[universal property]] of the [[limit]]:

for $(\mathcal{Y}, \mathcal{O}_{\mathcal{Y}}) \stackrel{f_i}{\to} (\mathcal{X}_i, \mathcal{O}_{\mathcal{X}_i})$ any [[cone]] over the given diagram, we have by the definition of morphisms of ringed toposes:

1. an essentially unique [[geometric morphism]] 

   $$
     h : \mathcal{Y} \to {\lim_\leftarrow}_j (\mathcal{X}_j, \mathcal{O}_{\mathcal{X}_j});
   $$

1. a unique morphism of ring objects 

   $$
     h^* {\lim_\to}_j p_j^* \mathcal{O}_{\mathcal{X}_j}
     \simeq
     {\lim_\to}_j h^* p_j^* \mathcal{O}_{\mathcal{X}_j}
     \to
     \mathcal{O}_{\mathcal{Y}}
   $$

   induced from the fact that the [[inverse image]] $h^*$ preserves [[colimit]]s and that the morphisms

   $$
      f_j^* \mathcal{O}_{\mathcal{X}_j} \to \mathcal{O}_{\mathcal{Y}}
   $$

   form a cocone under the diagram of ring objects $f_j^* \mathcal{O}_{\mathcal{X}_j} \in \mathcal{Y}$.

=--


## Related concepts

* [[ringed space]], [[locally ringed space]]

* [[ringed site]], [[locally ringed site]]  

* **ringed topos**, [[locally ringed topos]], 

* [[locally algebra-ed topos]]

* [[structured (∞,1)-topos]]

## References

An original reference is

* [[SGA]] IV 

A systematic development of [[geometry]] internal to a ringed topos is discussed in

* [[Monique Hakim]], _Topos annel&#233;s et sch&#233;mas relatifs_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 64, Springer, Berlin, New York (1972). 

A textbook source is section 16.7 of 

* [[Aise Johan de Jong]],  _[[The Stacks Project]]_ ([pdf](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf)) ([project website](http://www.math.columbia.edu/algebraic_geometry/stacks-git/))
{#deJong}

The generalization to [[structured (infinity,1)-toposes]] is due to

* [[Jacob Lurie]], _[[Structured Spaces]]_

See also

* [[eom]], _[Ringed spaces](http://eom.springer.de/R/r082460.htm)_


[[!redirects ringed toposes]]
[[!redirects ringed topoi]]

