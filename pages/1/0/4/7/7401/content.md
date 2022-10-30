
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

Generalized Reedy model structures are a class of [[model categories]] that generalize the [[Reedy model structures]] when the underlying [[site]] is generalized from a [[Reedy category]] to a [[generalized Reedy category]].

So these model structures serve to present [[(∞,1)-categories of (∞,1)-functors]] on generalized Reedy categories.

## Definition

Let $S$ be a (Cisinski-Moerdijk) [[generalized Reedy category]].
Let $\mathcal{C}$ be a category with small [[limits]] and [[colimits]].

### The model structure

+-- {: .num_defn #FirstNotation}
###### Definition

For every [[object]] $s \in S$, every [[functor]] $X : S \to \mathcal{C}$ and every [[natural transformation]] $\phi : X \to Y$ write 

* $S^+(s)$ for the [[full subcategory]] of the [[slice category]] $S^+/s$ on the non-invertible morphisms into $s$;

* $S^-(s)$ for the [[full subcategory]] of the [[under category]] $s/S^-$ on the non-invertible morphisms out of $s$;

* $Latch_s(X) := {\lim_\to}_{(r \to s) \in S^+(s)} X(r)$ for the [[colimit]] of $X$ over $S^+(s)$, called the **latching object** of $X$ at $s$;

* $Match_s(X) := {\lim_\leftarrow}_{(s \to r) \in S^-(s)} X(r)$ for the [[limit]] of $X$ over $S^-(s)$, called the **matching object** of $X$ at $s$.

* $X_s \coprod_{Latch_s(X)} Latch_s(Y) \to Y_s$ for the universal morphism induced from the morphism $L_s(X) \to X_s$, called the **relative latching map** of $\phi$ at $s$;

* $X_s \to Match_s(X) \prod_{Match_s(Y)} Y_s$ for the dual universal morphism, called the **relative matching map** of $\phi$ at $s$.

=--

See _[[Joyal-Tierney calculus]]_ for more on these kinds of objects and morphisms.

+-- {: .num_prop}
###### Proposition

In the above situation, the [[automorphism]] group $Aut_S(s)$ of $s$ canonically acts on all objects that appear, and all morphisms that appear respect this action.

Equivalently this means that for all $s$ the above objects and morphisms take place in the presheaf category $[B Aut(s), \mathcal{C}]$.

=--

Choose now once and for all a [[model structure on functors]] on all $[B Aut(r), \mathcal{C}]$, for instance the projective or the injective one. We will write $[B Aut(r), \mathcal{C}]_{proj/inj}$ to indicate some fixed choice. 


+-- {: .num_defn #ReedyModelStructure}
###### Definition

Let $S$ be a (Cisinski-Moerdijk)-[[generalized Reedy category]]. And let $\mathcal{C}$ be a [[cofibrantly generated model category]]. Write $[S, \mathcal{C}]$ for the [[category of presheaves]] on $S^{op}$ with values in $\mathcal{C}$.

Call a morphism $f : X \to Y$ in $[S, \mathcal{C}]$

* a **Reedy cofibration** if for each $s \in S$ the relative latching map 

  $$
    X_s \coprod_{L_s(X)} L_s(Y) \to Y_s
  $$

  is a cofibration in $[B Aut(s), \mathcal{C}]_{proj/inj}$;

* a **Reedy fibration** if for each $s \in S$ the relative matching map 

  $$
    X_s \to M_s(X) \prod_{M_s(Y)} Y_s
  $$

  is a fibration in $\mathcal{C}$;

* a **Reedy weak equivalence** if for each $s \in S$ the morphism

  $$
    f_s : X_s \to Y_s
  $$

  is a weak equivalence in $\mathcal{C}$;

where $[B Aut(r), \mathcal{C}]_{proj/inj}$ is the projective [[model structure on functors]].

=--

### Global latching objects
 {#GlobalLatchingObjects}

We discuss here an alternative way of speaking about the latching objects, one where all indices at a given degree $n \in \mathbb{N}$ are collected.

Recall from def. \ref{FirstNotation} that for $s \in S$ we write $S^+(s)$
for the category of non-invertible degree-increasing morphisms into $s$. We introduce the union of these categories over all objects of a fixed degree.

+-- {: .num_defn #SecondNotation}
###### Definition

For $n \in \mathbb{N}$ write

* $S^+(n) = \coprod_{d(s) = n} S^+(s)$;

* $d_ n : S^+((n)) \to S$ for the restriction of the [[domain opfibration]] to objects that are non-invertible morphisms in $S^+$ with codomain in degree $n$ and to morphisms whose codomain is invertible, i.e. to diagrams of the form

  $$
    \array{
       a &\stackrel{\in S^+}{\to}& b
       \\
       \downarrow^{\mathrlap{\in S^+}} && \downarrow^{\mathrlap{\in S^+}} & not\, invertible
       \\
       s & \stackrel{\simeq}{\to} & s' & deg = n
    }
    \,;
  $$

* $i_n : S^+(n) \hookrightarrow S^+((n))$ for the [[full subcategory]] inclusion on constant codomains;

* $G_n(S) \subset Core(S)$ for the [[groupoid]] of objects of degree $n$ and [[isomorphisms]] between them.

=--

+-- {: .num_prop #DiagramOfRestrictions}
###### Proposition

The above categories and functors arrange into a [[diagram]]

$$
  \array{
    S &\stackrel{dom_n}{\leftarrow}& S^+((n)) &\stackrel{cod_n}{\to}& G_n(S)
    &\stackrel{j_n}{\hookrightarrow}& S
    \\
    &&
    {}^{\mathllap{i_n}}\uparrow && \uparrow^{\mathrlap{i_n}}
    \\
    && S^+(n) &\stackrel{cod_n}{\to}& Obj(S)_n
  }  
  \,,
$$

where the vertical morphisms are (non-full) inclusions and the square is a [[pullback]] of an [[opfibration]].  Therefore it satisfies the [[Beck-Chevalley condition]] so that we have a [[natural isomorphism]]

$$
  (cod_n)_! i_n^* \simeq i_n^* (cod_n)_!
  \,.
$$


=--

+-- {: .num_remark #RestrictedCodomainIsOpfibration}
###### Remark

The restricted [[codomain fibration|codomain opfibration]] $cod_n : S^+((n)) \to G_n$ is still an [[opfibration]]: it is the [[Grothendieck construction]] of the [[pseudofunctor]]

$$
  S^+(-) : G_n(S) \to Cat
$$

$$
  s \mapsto S^+(s)
  \,.
$$

=--


+-- {: .num_defn #GlobalLatching}
###### Definition

For $n \in \mathbb{N}$, let $X \in [S, \mathcal{C}]$. Write 

* $X_n := j_n^* X = X|_{G_n(S)} \in [G_n(S), \mathcal{C}]$;

* the **$n$th latching object** is 

  $$
    L_n(X) := cod_! dom_n^* X \in [G_n(S), \mathcal{C}]
    \,.
  $$

* the **$n$th latching morphism**

  $$
    Latch_n(X) \to X_n
  $$

  is the [[adjunct]] to the canonical functor

  $$  
    dom_n^* X \to (j_n cod_n)^* X
    \,.
  $$

=--

The following proposition says that the "global" latching objects indeed contain all the ordinary latching objects in the given degree. 

+-- {: .num_prop #GlobalLatchingContainsLocalLatchings}
###### Proposition

For $s \in Obj(S)_n$ we have

$$
  Latch_n(X) : s \mapsto Latch_s(X)
$$

and the component of the $n$th latching morphism on $s$ is the canonical $Latch_s(X) \to X(s)$.

=--

+-- {: .proof}
###### Proof

By remark \ref{RestrictedCodomainIsOpfibration} 
$(cod_n)_!$ is the left Kan extension along an [[opfibration]]. By a standard fact (see [here](http://ncatlab.org/nlab/show/Kan+extension#AlongFibrations) at _[[Kan extension]]_) these are computed at any object by the colimit over the fiber over that object.


=--

### Skeleta and coskeleta
 {#SkeletaAndCoskeleta}

Over any generalized Reedy category there is an anlog of the notion of [[simplicial skeleton]] and [[simplicial coskeleton]].

For $n \in \mathbb{N}$, write 

$$
  t_n : S_{\leq n}  \hookrightarrow S
$$ 

for the [[full subcategory]]
on the objects of degree $\leq n$.

+-- {: .num_defn #SkeletaByAdjunction}
###### Definition

Left and right [[Kan extension]] along $t_n$ defines an [[adjoint triple]]

$$
  ((t_n)_! \dashv t_n^* \dashv (t_n)_*)
  :
   [S_{\leq n},\mathcal{C}] \stackrel{\overset{(t_n)_!}{\hookrightarrow}}{\stackrel{\overset{t_n^*}{\leftarrow}}{\underset{(t_n)_*}{\hookrightarrow}}}
  [S,\mathcal{C}]
  \,.
$$


The induced [[monads]]

$$
  (sk_n \dashv cosk_n)
  : 
  [S,\mathcal{C}]
    \stackrel{\overset{(t_n)_!}{\leftarrow}}{\underset{t_n^*}{\to}}
  [S_{\leq n},\mathcal{C}]
    \stackrel{\overset{t_n^*}{\leftarrow}}{\underset{(t_n)_*}{\to}}
  [S,\mathcal{C}]
$$

are the **$n$-[[skeleton]]** and **$n$-[[coskeleton]]** functors, respectively.

Define for all $X \in [S, \mathcal{C}]$ the notation $sk_{-1}X$ to denote the [[initial object]] and $cosk_{-1}X$ the [[terminal object]].

=--

The $((t_n)_! \dashv t_n^*)$-[[unit of an adjunction|counit]] and the $(t_n^* \dashv (t_n)_*)$-unit induces [[natural transformations]]

$$
  sk_n \to id
$$

$$
  id \to cosk_n
  \,.
$$

+-- {: .num_lemma #LatchingIsSkeleton}
###### Lemma

The degree-$n$th latching object, def. \ref{GlobalLatching}, is isomorphic to the $(n-1)$-skeleton, and dually, the degree-$n$ matching object is isomorphic to the $(n-1)$-coskeleton. Under these identifications the canonical morphisms on both sides match

$$
  Latch_n(X) \simeq sk_{n-1}(X) 
$$

$$
  Match_n(X) \simeq cosk_{n-1}(X)
$$


=--

This is ([Ber-Moer, lemma 6.2](#BergerMoerdijk)).

+-- {: .num_lemma #coSkeletonTower}
###### Lemma

There are towers of [[natural transformations]]

$$
  \emptyset \to sk_0 X \to sk_1 X \to sk_2 X \to \cdots \to X
  \,,
$$

and

$$
  X \to \cdots \to cosk_2 X \to cosk_1 X \to cosk_0 X \to *
  \,,
$$

that exhibit $X$ as the [[colimit]] of its skeleton tower and as the [[limit]] of its coskeleton tower.

=--

This is ([Ber-Moer, lemma 6.3](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

The morphisms in the tower come from the [[unit of an adjunction|adjunction units and counits]]. To see that for instance the first diagram is colimiting, 
consider a cocone $\{sk_n X \to Y\}$. By adjointness this is equivalently
a system of morphisms $\{X_{\leq n} \to Y_{\leq n}\}$. Hence there is a unique morphism
$X \to Y$ that factors the original cocone.

=--


## Proof of the model category axioms

We discuss that for $S$ a Berger-Moerdijk-[[generalized Reedy category]] and $\mathcal{C}$ a [[cofibrantly generated model category]], def. \ref{ReedyModelStructure} indeed defines a [[model category]] structure on the [[functor category]] $[S,\mathcal{C}]$.

+-- {: .num_theorem }
###### Theorem 

Def. \ref{ReedyModelStructure} indeed defines a [[model category|model structure]].

=--

+-- {: .proof}
###### Proof

It is clear that $[S,\mathcal{C}]$ has all limits and colimits (as for any [[category of presheaves]] they are computed objectwise in $\mathcal{E}$) and that the weak equivalences satisfy [[two-out-of-three]], since the weak equivalences in $\mathcal{E}$ do. Also, all three classes of morphisms are closed under [[retracts]], since, for instance, the relative latching morphism of a retract is the retract of a relative latching morphism and so the property follows with the retract-closure of the classes of morphisms in $\mathcal{E}$.

It remains to show that the relevant lifting and factorization properties hold. This we discuss in a list of lemmas below in _[Lifting](#Lifting)_ and _[Factorization](#Factorization)_.

=--

### Lifting 
 {#Lifting}

We work with the "global" latching objects from [above](#GlobalLatchingObjects).

+-- {: .num_remark }
###### Remark

A morphism $f : X \to Y$ in $[S, \mathcal{C}]_{gReedy}$ is a Reedy cofibration
precisely if for all $n \in \mathbb{N}$ the global relative latching morphism, def. \ref{GlobalLatching}

$$
  X_n \coprod_{L_n(X)} L_n(Y) \to Y_n
$$

is a cofibration in $[G_n(S), \mathcal{C}]_{proj/inj}$.

=--

+-- {: .proof}
###### Proof

The coproduct in the presheaf category $[G_n(S), \mathcal{C}]$ is computed objectwise, so that the component of the $n$th relative latching morphism at $s \in S$ is the relative latching morphism at $s$, by prop. \ref{GlobalLatchingContainsLocalLatchings}.

The [[groupoid]] $G_n(S)$ is equivalent to the disjoint union $\coprod_{[r] \in \pi_0 G_n(S)} B Aut_S(s)$ of the automorphism groupoids of one representative in each isomorphism class. A morphism in $[G_n(S), \mathcal{C}]_{proj/inj}$ is a cofibration precisely if its restriction to all of the $[B Aut_{\mathcal{C}}(s), \mathcal{C}]_{proj/inj}$ is. 


=--

+-- {: .num_lemma #LiftingLemma}
###### Lemma

In the generalized Reedy model structure, def. \ref{ReedyModelStructure}, 

* Reedy cofibrations $f$ such that for all $n \in \mathbb{N}$ the morphism $Latch_n(f)$ is an objectwise weak equivalence have the [[left lifting property]] against fibrations;

* Reedy cofibrations have the [[left lifting property]] against Reedy fibrations $f$ with the special property that for all $n \in \mathbb{N}$ the morphism $Match_n(f)$ is an objectwise weak equivalence.


=--

This is ([Ber-Moer, lemma 5.2, lemma 5.4](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

We show the first clause. The second is dual. So let $f : X \to Y$ be an acyclic cofibration and let $g : Y \to X$ be a fibration.
We will exhibit a lift in any commuting diagram

$$
  \array{
    A &\stackrel{}{\to}& Y
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{}}
    \\
    B &\stackrel{}{\to}& X
  }
$$

by stepwise constructing lifts in in the skeletal filtration, lemma \ref{coSkeletonTower}.

At $n = 0$, observe that since $L_0(X) = \emptyset$ for all $X$, the fact that 

$$
  A_0 \coprod_{L_0(A)} L_0(B) \to B_0
$$

is a cofibration in $[G_0, \mathcal{C}]$ by assumption, means that in fact $f_0 : A_0 \to B_0$ is an acyclic cofibration here. Similarly $Y_0 \o X_0$ is a fibration there. But $G_0(S) = S_{\leq 0}$ and so the restriction of the lifting problem along $t_0$

$$
  \array{
    A_0 &\stackrel{}{\to}& Y_0
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{}}
    \\
    B_0 &\stackrel{}{\to}& X_0
  }
$$

is a lifting problem in $[G_0(S), \mathcal{C}]_{proj/inj}$ of an acyclic cofibration against a fibration, and hence has a filler $\gamma_0 : B_0 \to Y_0$ there.

Now assume that a filler $\gamma_{\leq (n-1)}$ in 

$$
  \array{
    A_{\leq (n-1)} &\stackrel{}{\to}& Y_{\leq (n-1)}
    \\
    \downarrow^{\mathrlap{}} && \downarrow^{\mathrlap{}}
    \\
    B_{\leq (n-1)} &\stackrel{}{\to}& X_{\leq (n-1)}
  }
$$

has been found. By lemma \ref{LatchingIsSkeleton} this induces maps $Latch_n(B) \to Latch_{Y}$ and $Match_n(B) \to Match_n(Y)$ from which we can build the commuting diagram

\[
  \label{MainLiftingDiagram}
  \array{
    A_n \coprod_{Latch_n A} Latch_n B
    &\to&
    Y_n
    \\
    \downarrow^{\mathrlap{v_n}} && \downarrow^{\mathrlap{w_n}}
    \\
    B_n &\to& X_n \times_{Match_n X} Match_n Y
  }
  \,.
\]

Here for instance the top horizontal morphism comes from the commutativity of the square

$$
  \array{
    Latch_n A &\to& Latch_n B &\to& Latch_n Y
    \\
    \downarrow && && \downarrow
    \\
    A_n &\to& &\to& Y_n
  }
$$

by naturality of the $(sk_{n-1} \dashv t_{n-1}^*)$-counit.

We observe now that a lift in (eq:MainLiftingDiagram) in $[G_n, \mathcal{C}]_{proj/inj}$ completes the induction step. For instance in the top left the lift

$$
  \array{
    A_n \coprod_{Latch_n A} Latch_n B
    &\to&
    Y_n
    \\
    \downarrow &\nearrow_{\gamma_n}& 
    \\
    B_n 
  }
$$

is 

* a lift in 

  $$
    \array{
       A_n &\to& Y_n
       \\
       \downarrow & \nearrow
       \\
       B_n
    }
  $$

* which is compatible with the previously chosen $\gamma_{\leq (n-1^)}$

By assumption the left vertical morphism is a cofibration in $[G_n, \mathcal{C}]_{proj/inj}$, and the right vertical morphism is a fibration there. It is now sufficient to show that the left morphism is also a weak equivalence, hence is a weak equivalence in $\mathcal{E}$ over each $s \in S$.

By assumption we know that $L_n(f)_s$ is an acyclic cofibration in $\mathcal{C}$ for all $s$. Hence so is its pushout $A_s \to 
(A_s \coprod_{L_n(A)_s} L_n(B)_s)$. The morphism $v_n(s)$ finally sits in the diagram

$$
  \array{
    A_r &\stackrel{f_r}{\to}& B_r
    \\
    \downarrow  & \nearrow_{\mathrlap{v_n(s)}}
    \\
    (A_s \coprod_{L_n(A)_s} L_n(B)_s)
  }
$$ 

and so is a weak equivalence by [[two-out-of-three]].

=--


+-- {: .num_lemma #LatchingIntertwiner}
###### Lemma

Suppose $\phi : R \to S$ is a morphism of 
[[generalized Reedy categories]] such that the induced square (see prop. \ref{DiagramOfRestrictions})

$$
  \array{
    R^+((k)) &\stackrel{cod_k^R}{\to}& G_k(R)
    \\
    \downarrow^{\mathrlap{\phi_k^+}} && \downarrow^{\mathrlap{\phi_k}}
    \\
    S^+((k)) &\stackrel{cod_k^S}{\to}& G_k(S)
  }
$$ 

is a pullback. Then for each $X \in [S, \mathcal{C}]$, the natural comparison functor

$$
  L_k(\phi^*(X)) \to \phi_k^*(L_k X)
$$

is an isomorphism.

Given a Reedy category $S$, examples of $\phi$ satisfying this condition include

1. $\phi := dom_n \circ i_n : S^+(n) \to S$;

1. $\phi := : S_{\leq n} \hookrightarrow S$.

=--

This is ([Ber-Moer, lemma 4.4](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

The pullback square is part of the diagram 

$$
  \array{
    R
     &\stackrel{dom_k^R}{\leftarrow}&
    R^+((k)) &\stackrel{cod_k^R}{\to}& G_k(R)
    \\
    \downarrow^\phi
     &&
    \downarrow^{\mathrlap{\phi_k^+}} && \downarrow^{\mathrlap{\phi_k}}
    \\
    S
     &\stackrel{dom_k^S}{\leftarrow}&
    S^+((k)) &\stackrel{cod_k^S}{\to}& G_k(S)
  }
$$ 

whose rowes define, by prop. \ref{DiagramOfRestrictions}, the latching objects by pull-push. Since the pullback square satisfies the [[Beck-Chevalley condition]], we find the intertwining isomorphism as follows

$$
  \begin{aligned}
     L_k \phi^* X 
     & \simeq 
     (cod^R_k)_! (dom^R_k)^* \phi^* X
     \\
      & \simeq 
      (cod^R_k)_! (\phi^+_k)^* (dom^S_k)^* X
     \\
     & \simeq
     (\phi_k)^* (cod^R_k)_! (dom^S_k)^* X
     \\
     & \simeq
     (\phi_k)^*
     L_k X
  \end{aligned}
  \,.
$$

Now concerning the two examples.

By definition we have

$$
 (S^+(n))^+((k))
 \simeq
  \left\{
  \array{  
    t &\stackrel{deg \; raising}{\to}& t'
    \\
    \downarrow && \downarrow && deg\; raising
    \\
    s &\stackrel{\simeq}{\to}& s' && deg = k
    \\
    \downarrow && \downarrow && deg \; raising
    \\
    r &\stackrel{id}{\to}& r  && deg = n
  }
  \right\}
  \,,
$$

where on the right the vertical sequences in $S$ indicate objects in $(S^+(m))^+((k))$ and the whole diagram on the right indicates a morphism there. 

One sees that this is indeed the fiber product as claimed.


=--

+-- {: .num_lemma #ExtraPropertyOfAcyclicCofibrations}
###### Lemma

Let $f : X \to Y$ in $[S, \mathcal{C}]$ be a Reedy cofibration, which is a weak equivalence on all objects of degree $\lt n$. Then the morphism $ Latch_n(f) :  Latch_n(X) \to  Latch_n(Y)$ is over each $s \in S$ an acyclic cofibration in $\mathcal{C}$

Dually, let $f : X \to Y$ in $[S, \mathcal{C}]$ be a Reedy fibration which is a weak equivalence over all objects of degree $\lt n$. Then the morphism $Match_n(f) :  Match_n(X) \to  Match_n(Y)$ is over each $s \in S$ an acyclic fibration in $\mathcal{C}$.


=--

This is ([Ber-Moer, lemma 5.3 and lemma 5.5](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

We show this by induction over $n$, using the skeletal filtration def. \ref{SkeletaByAdjunction}. For $n = 0$ we have for all $X$ that
$L_n X = sk_{-1} X = \emptyset$, and hence the condition is trivially satisfied. 

So assume now that the statement has been shown for all $(k \lt n)$-skeleta, then we need to show that $i_n^* L_n f$ is an acyclic cofibration, hence that every square of the form

$$
  \array{   
    i_n^* L_n A &\to& Y
    \\
    \downarrow^{\mathrlap{i_n^* L_n f}} && \downarrow^{g}
    \\
    i_n^* L_n B &\to& X
  }
$$

with $g$ a fibration in $[Obj(S)_n, \mathcal{C}]_{proj/inh}$ (hence over every object of degree $n$) has a lift. Since by lemma \ref{DiagramOfRestrictions} we have

$$
  i^*_n L_n = i_n^* cod_! dom_n^* = cod_! i_n^* dom_n^*
$$

such a filler is equivalently a filler in 

$$
  \array{
     i_n^* dom_n^* A &\to& cod^* Y
     \\
     {}^{\mathllap{}}\downarrow && \downarrow
     \\
     i_n^* dom_n^* B &\to& cod^* X
  }
$$

being a diagram in $[S^+(n), \mathcal{C}]$

We now establish such a filler by using lemma \ref{LiftingLemma} with the Reedy category in question being $S^+(n)$. This has only $+$-morphisms and hence Reedy fibrations here are objectwise fibrations, so the morphism on the right is a Reedy fibration over $S^+(n)$.

Moreover, $i_n^* dom_n^* f$ is a Reedy weak equivalence in this structure, since all its objects have degree $\lt n$. It remains to be shown that the assumptions of lemma \ref{LiftingLemma} are satisfied. 

By lemma \ref{LatchingIntertwiner} the functor

$$
  (d_k i_k)^* : [G_k(S), \mathcal{C}] \to [G_k(S^+(n)), \mathcal{C}]
$$

intertwines the latching objects on both sides. Therefore the above morphism on the left is the image under $(dom_n i_n)^*$ of the $k$th relative latching morphism of $A \to B$. Since $(d_k i_k)$ is a faithful functor between groupoids, $(d_k i_k)^*$ preserves cofibrations, and so the left morphism above is a Reedy cofibration. Similarly, since $L_k(f)$ is an acyclic cofibration by assumption, so is $L_k((d_k i_k)^* f)$.

(...)

=--


+-- {: .num_prop }
###### Proposition

In the generalized Reedy model structure, def. \ref{ReedyModelStructure}, 

* acyclic cofibrations have the [[left lifting property]] against fibrations;

* cofibrations have the [[left lifting property]] agains acyclic fibrations.


=--

+-- {: .proof}
###### Proof

By lemma \ref{ExtraPropertyOfAcyclicCofibrations} every Reedy cofibration induces a weak equivalence under $L_n$. By lemma \ref{LiftingLemma} this implies the left lifting property against Reedy fibrations. Dually for the second statement.

=--



### Factorization
 {#Factorization}

(...)

## Properties

### Skeletal filtration and coskeleton tower

+-- {: .num_prop }
###### Proposition

Let $S$ be a Berger-Moerdijk-[[generalized Reedy category]] and $\mathcal{C}$ any [[model category]]. Let $X \in [S, \mathcal{C}]$ and let $n \in \mathbb{N}$ and $k \lt l \leq \infty$. Recall the skeleta/coskeleta towers from lemma \ref{coSkeletonTower}.

1. If $X$ is Reedy cofibrant according to def. \ref{ReedyModelStructure} then all $sk_n X$ are Reedy cofibrant and the canonical morphisms $sk_k X \to sk_l X$ are Reedy cofibrations. 

1. If $X$ is Reedy fibrant according to def. \ref{ReedyModelStructure} then all $cosk_n X$ are Reedy fibrant and the canonical morphisms $cosk_l X \to cosk_k X$ are Reedy fibrations. 


=--

This is ([Ber-Moer, prop. 6.5](#BergerMoerdijk)).

### Relation to other model structures

(...)

## Example

* Every ordinary [[Reedy category]] is a generalized Reedy category, and in this case the above model structure reduces to the traditional [[Reedy model structure]].

* The [[model structure for dendroidal complete Segal spaces]] is a [[Bousfield localization of model categories|left Bousfield localization]] of the generalized Reedy model structure over the [[tree category]].

## Related concepts

* [[Joyal-Tierney calculus]]

## References 

* [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_, Math. Z. (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 {#BergerMoerdijk}
