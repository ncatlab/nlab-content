
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
* automatic table of contents goes here
{:toc}

## Idea 

A _Reedy model structure_ is a [[global model structure on functors]]:

given a [[Reedy category]] $R$ and a [[model category]] $C$ the **Reedy model structure** is a [[model category]] structure on the [[functor category]] $[R,C] = Func(R,C)$.

As opposed to the [[global model structure on functors|projective and injective model structure]] on functors this does not require any further structure on $C$, but instead makes a strong assumption on $R$.

There is a refinement to a notion of $V$-[[enriched Reedy category]] such that if $C$ is a $V$-[[enriched model category]] -- in particular when it is a [[simplicial model category]] for $V = $ [[SSet]] -- the [[enriched functor category]] $[R,C]$ is itself a $V$-[[enriched model category]]. (Reference _Ang_ below.)



In the case that we do have extra assumptions on the codomain in that

* $C$ a [[combinatorial simplicial model category]] 

* with  $C^\circ$ the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by $C$ 

* and with the [[Reedy category]] $R$ an ordinary category regarded as a [[SSet]]-[[enriched category]], 

the Reedy model structure, having the same weak equivalences as the [[global model structure on functors]], presents similarly the [[(∞,1)-category of (∞,1)-functors]] $Func_\infty(R,C^\circ)$, from $C$ into the [[(∞,1)-category]] [[presentable (∞,1)-category|presented by]] $C$.


## Definition

+-- {: .num_theorem #model}
###### Theorem
If $R$ is a [[Reedy category]] and $C$ is a [[model category]], then there is a canonical induced [[model category|model structure]] on the [[functor category]] $C^R$ in which the weak equivalences are the objectwise weak equivalences in $C$.
=--

The basic idea is as follows.  Given a diagram $X:R\to M$ and an object $r\in R$, define its **latching object** to be

$$ 
  L_r X = \colim_{s \overset{+}{\to} r} X_s
$$

where the colimit is over the full subcategory of $R_+/r$ containing all objects except the identity $1_r$.  Dually, define its **matching object** to be

$$ 
  M_r X = \lim_{r \overset{-}{\to} s} X_s
$$

where the limit is over the full subcategory of $r/R_-$ containing all objects except $1_r$.  There are evident canonical, and natural, morphisms
$$L_r X\to X_r \to M_r X.$$
Note that $L_0 X = 0$ is the initial object and $M_0 X$ is the terminal object, since there are no objects of degree $\lt 0$.

In the case $R=\Delta^{op}$, the latching object $L_n X$ can be thought of as the object of _degenerate_ $n$-simplices sitting inside the object $X_n$ of all $n$-simplices.  When $R=\alpha$ is an ordinal, then $L_{n+1} X = X_n$ and $M_n X = 1$, and dually for $R=\alpha^{op}$.

We now define a morphism $f:X\to Y$ in $M^R$ to be a cofibration or trivial cofibration if for all $r$, the map
$$L_r Y \amalg_{L_r X} X_r \to Y_r$$
is a cofibration or trivial cofibration in $M$, respectively, and to be a fibration or trivial fibration if for all $r$, the map
$$ X_r \to M_r X \times_{M_r Y} Y_r$$
is a fibration or trivial fibration in $M$, respectively.  Define $f$ to be a weak equivalence if each $f_r$ is a weak equivalence in $M$.

One then verifies that this defines a model structure; the details can be found in (for instance) Hovey and Hirschhorn's books.  In particular, to factor a morphism $f:X\to Y$ in either of the two necessary ways, we construct the factorization $f_r = g_r h_r$ inductively on $r$, by factoring the induced morphism
$$ L_r Z \amalg_{L_r X} X_r \to M_r Z \times_{M_r Y} Y_r$$
in the appropriate way in $M$.

## Remarks

* Any Reedy cofibration or fibration is, in particular, an objectwise one, but the converse does not generally hold.

* An object $X$ is Reedy cofibrant if and only if each map $L_r X \to X_r$ is a cofibration in $M$.  In particular, this implies that each $X_r$ is cofibrant in $M$.

* For some $M$, $M^R$ also admits a [[projective model structure|projective]] or [[injective model structure|injective]] model structures.  For instance for $M = $ [[SSet]] this is the [[global model structure on simplicial presheaves]]. 

  In general the Reedy structure will not be the same as either, but will be a kind of mixture of both. If $R = R_+$ then the Reedy model structure coincides with the [[projective model structure]], if $R = R_-$ it coincides with the [[injective model structure]].

  For a detailed comparison of Reedy and global projective/injective model structures see around example A.2.9.22 in [[Higher Topos Theory|HTT]].

* In addition to its existing for all $C$, another advantage of the Reedy structure is the explicit nature of its cofibrations, fibrations, and factorizations.

* If $R$ admits more than one structure of Reedy category, then $C^R$ will have more than one Reedy model structure.  For instance, if $R = (\cdot\to\cdot)$ is the [[walking arrow]], then we can regard it as either the ordinal $2$ or its opposite $2^{op}$, resulting in two different Reedy model structures on $C^2$.

* For a general Reedy category $R$, the diagonal functor $C\to C^R$ need not be either a right or a left [[Quillen adjunction|Quillen functor]] (although, of course, it has left and right adjoints given by colimits and limits over $R$).  One can, however, characterize those Reedy categories for which one or the other is the case, and in this case one can construct [[homotopy limit|homotopy limits]] and colimits using the derived functors of these Quillen adjunctions.

## Properties {#Properties}

+-- {: .un_prop }
###### Observation

Let $C$ be a [[combinatorial model category]] and $R$ a [[Reedy category]].


The identity functors provide left [[Quillen equivalence]]s

$$
  [R,C]_{proj} \stackrel{\simeq_{Quillen}}{\to}
  [R,C]_{Reedy}
  \stackrel{\simeq_{Quillen}}{\to}
  [R,C]_{inj}
  \,.
$$


=--

See also [[Higher Topos Theory|HTT, remark A.2.9.23]]



## Examples 

### Over the arrow category 

The simplest nontrivial example is obtained for 

$$
  R = I = \{1 \to 0\}
$$ 

the [[interval category]]. 

In this case the [[functor category]] $[I,C]$ is the [[arrow category]] $C$.

We take the degree on the objects to be as indicated. Then $R_- = R$ and $R_+$ contains only the identity morphisms.

For $F : I \to C$ a functor, i.e. a morphism $F(1) \to F(0)$ in $C$, we find  


* the latching object $latch_0 F = colim_{(s \stackrel{+}{\to} 0)} F(s) = \emptyset$;

* the latching object 
  $latch_1 F = colim_{(s\stackrel{+}{\to}1)} F(s) = \emptyset$;

* the matching object $match_0 F = lim_{(0 \stackrel{-}{\to} 0)} F(s) = {*}$

* the matching object $match_1 F = lim_{(1 \stackrel{-}{\to}s)} F(s) = F(0)$

where $\emptyset$ denotes the [[initial object]] and ${*}$ the [[terminal object]] (being the [[colimit]] and [[limit]] over the empty [[diagram]],  respectively).

From this we find that for a [[natural transformation]] $\eta : F \to G$

  $$
    \array{
      F(1) &\stackrel{\eta_1}{\to}& G(1)
      \\
      \downarrow && \downarrow
      \\
      F(0) &\stackrel{\eta_0}{\to}& G(0)
    }
  $$

that 

* it is a Reedy cofibration in $[I,C]$ of

  * $\eta_0 : F(0) \coprod_{\emptyset} \emptyset = F(0) \to G(0)$ is a cofibration

  and

  * $\eta_1 : F(1) \coprod_{\emptyset} \emptyset = F(1) \to G(1)$ is a cofibration


* it is a Reedy fibration in $[I,C]$ if

  * $\eta_0 : F(0) \to G(0) \times_{*} {*} = G(0)$ is a fibration

  * the universal morphism $F(1) \to G(1) \times_{G(0)} F(0)$ 
   
    $$
    \array{
      F(1)
      \\
      & \searrow
      \\
      && F(0) \times_{G(0)} G(1) 
      &\stackrel{\eta_1}{\to}& G(1)
      \\
      && \downarrow && \downarrow
      \\
      && F(0) &\stackrel{\eta_0}{\to}& G(0)
    }
    $$

    is a fibration.

  Notice that since fibrations are preserved by pullbacks and under composition with themselves, it follows that also $\eta_1 : F(1) \to F(0)$ is a fibration.

* The cofibrant objects in $[I,C]$ are those arrows $F(1) \to F(0)$ in $C$ for which $F(1)$ and $F(0)$ are cofibrant;

* The fibrant objects in $[I,C]$ are those arrows $F(1) \to F(0)$ in $C$ that are fibrations between fibrant objects in $C$.

So in accord with the proposition above one finds that this Reedy model structure on $[I,C]$ coincides with the _injective_ [[global model structure on functors]] on $I$.


### Over the tower category 

Let $R = \mathbb{N}^{op} = \{\cdots \to 2 \to 1 \to 0\}$ be the natural numbers regarded as a [[poset]] using the great-than  relation.

With the degree as indicated, this is a Reedy category with $R_- = R$ and $R_+$ containing only identity morphisms.

Now the [[functor category]] $[R,C]$ is the category of _towers_ of morphisms in $C$. 

The analysis of the Reedy model structure on this involves just a repetition of the steps invoilved in the analysis of the arrow category in the above example. One finds:

* a natural transformation $\eta : F \to G$ is a fibration precisely if

  * all components $\eta_n : F(n) \to G(n)$ are fibrations

  * all universal morphisms $F(n) \to F(n-1) \times_{G(n-1)} G(n)$ are fibrations.

* the fibrant objects are the towers of fibrations on fibrant objects in $C$.


### Over the simplex category {#SimplexCategory}

The motivating and central example of [[Reedy categories]] is the 
[[simplex category]] $\Delta$.

Recall that

* a map $[k] \to [n]$ is in $\Delta_+$ precisely if it is an injection;

* a map $[n] \to [k]$ is in $\Delta_-$ precisely if it is a surjection.

Dually, for the [[opposite category]] $\Delta^{op}$

* a morphism $[n] \leftarrow [k]$ is in $\Delta_-^{op}$ precisely if the map underlying it is an injection;

* a morphism $[k] \leftarrow [n]$ is in $\Delta^{op}_+$ precisely if the map underlying it is a surjection.


Let $C = sSet_{Quillen}$ be the category [[sSet]] equipped with the standard [[model structure on simplicial sets]] and consider the Reedy model structures on $[\Delta^{op}, sSet_{Quillen}]$ $[\Delta,sSet_{Quillen}]$. 

#### Properties 

We record some useful facts.

+-- {: .un_prop}
###### Observation


Every simplicial set $X$ regarded as a simplicial diagram

$$
  X : \Delta^{op} \to Set \hookrightarrow sSet
$$

is Reedy cofibrant in $[\Delta^{op}, sSet]$.

=--

+-- {: .proof}
###### Proof
 
The latching object of $X$ at $n$ is

$$
  L_n(X)
  =
  \lim_{\to} \left( 
    ([n]\to [k]\;surj.\;in\;\Delta)
    \mapsto
    X_k
  \right)
  \,.
$$

The canonical map 

$$
  L_n(X) \to X_n
$$

identifies  $X_k$ along $X([n] \to [k]) :  X_k \to X_n$ in $X_n$ as a bunch of degenrate $n$-cells. In total, $L_n(X)$ is identified as the set of all degenerate $n$-cells of $X$.

Therefore $L_n(X) \to X_n$ is clearly an injection of sets, hence a monomorphism of (constant) simplicial sets. Monomorphisms are the cofibrations in $sSet_{Quillen}$.

=--



+-- {: .un_prop}
###### Observation

The canonical cosimplicial simplicial set

$$
  \Delta[-] : \Delta \to sSet
$$

is Reedy cofibrant in $[\Delta,sSet_{Quillen}]$.

=--

+-- {: .proof}
###### Proof

The latching object at $n$ is

$$
  L_n(\Delta[-]) = 
  \lim_\to
  \left(
    ([k] \to [n]\; inj.\in\;\Delta) \mapsto
    \Delta[k]
  \right)
  \,.
$$

This is $\partial \Delta[n]$. The inclusion $\partial \Delta[n] \to \Delta[n]$ is a monomorphism, hence a cofibration in $sSet_{Quillen}$ (in fact these are the generating cofibrations).


=--


+-- {: .un_prop}
###### Corollary

Every [[simplicial set]] is the [[homotopy colimit]] over its diagram of simplices (with values in the constant simplicial set on the sets of simplicies $X_n$):

$$
  X \simeq hocolim ( [n] \mapsto const X_n)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Because $X_{(-)} : \Delta^{op} \to sSet$ is Reedy cofibrant by the above, by the discussion at [[homotopy colimit]] we can compute the hocolim by the [[coend]]

$$
  \int^{[n]} Q(*)_n \cdot X_n
  \,,
$$

where $Q(*) : \Delta \to sSet$ is a cofibrant [[resolution]] of the point in $[\Delta, sSet_{Quillen}]_{Reedy}$. Using the above observation, we can take this to be $\Delta[-]$ since this is cofibrant by the above observation and clearly $\Delta[-] \to *$ is objectwise a weak equivalence in $sSet_{Quillen}$.

Therefore the hocolim is (up to equivalence) represented by the simplicial set

$$
  \int^{[n]} \Delta[n] \cdot X_n
  \,.
$$

But by the [[co-Yoneda lemma]] this is in fact [[isomorphism|isomorphic]] to $X$, hence in particular weakly equivalent to $X$.

=--

+-- {: .un_remark}
###### Remark

This kind of argument has many immediate generalizations. For instance for $C = [K^{op}, sSet_{Quillen}]_{inj}$ the injective [[model structure on simplicial presheaves]] over any small category $K$, or any of its left [[Bousfield localization of model categories|Bousfield localizations]], we have that the cofibrations are objectwise those of simplicial sets, hence objectwise monomorphisms, hence it follows that every simplicial presheaf $X$ is the hocolim over its simplicial diagram of component presheaves.

=--

For the following write $\mathbf{\Delta} : \Delta \to sSet$ for the [[fat simplex]].  

+-- {: .un_prop}
###### Observation

The fat simplex is Reedy cofibrant.

=--


+-- {: .proof}
###### Proof

By the discussion at [[homotopy colimit]], the fat simplex is cofibrant in the projective [[model structure on functors]] $[\Delta, sSet_{Quillen}]_{proj}$. By the [general properties](#Properties) of Reedy model structures, the identity functor $[\Delta, sSet_{Quillen}]_{proj} \to [\Delta, sSet_{Quillen}]_{Reedy}$ is a [[Quillen adjunction|left Quillen functor]], hence preserves cofibrant objects.

=--


+-- {: .un_prop}
###### Corollary

For $X \in [\Delta^{op}, C]$ a Reedy cofibrant object, the [[Bousfield-Kan map]]

$$
  \int^{[n]} \mathbf{\Delta}[n] \cdot X_n
  \to
  \int^{[n]} \Delta[n] \cdot X_n  
$$

is a weak equivalence in $C$.

=--

+-- {: .proof}
###### Proof

The [[coend]] over the [[copower|tensor]] is a left [[Quillen bifunctor]]

$$
  \int (-)\cdot (-) : [\Delta,sSet_{Quillen}]_{Reedy} \times
    [\Delta^{op}, C]_{Reedy}
$$

(as discussed there). Therefore with its second argument fixed and cofibrant it is a [[Quillen adjunction|left Quillen functor]] in the remaining argument. As such, it preserves weak equivalences between cofibrant objects (by the [[factorization lemma]]). By the above discussion, both $\mathbf{\Delta}[n]$ and $\Delta[-]$ are indeed cofibrant in $[\Delta,sSet_{Quillen}]_{Reedy}$. Clearly the functor $\mathbf{\Delta}[-] \to \Delta[-]$ is objectwise a weak equivalence in $sSet_{Quillen}$, hence is a weak equivalence.

=--



## References 

A review of Reedy model structures is in section A.2.9 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The discussion of enriched Reedy model structures is in

* Vigleik Angeltveit, _Enriched Reedy categories_ ([arXiv](http://arxiv.org/abs/math/0612137))

The main statement is theorem 4.7 there.