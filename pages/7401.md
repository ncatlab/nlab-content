
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

As for the [[Reedy model structure|Reedy model structures]], the generalized Reedy model structure typically models [[geometric shapes for higher structures]]. The crucial generalization is that the basic shapes here may have non-trivial [[automorphisms]].

## Definition

Let $S$ be a (Berger-Moerdijk) [[generalized Reedy category]].
Let $\mathcal{C}$ be a category with small [[limits]] and [[colimits]].

### The model structure

+-- {: .num_defn #FirstNotation}
###### Definition

For every [[object]] $s \in S$, every [[functor]] $X : S \to \mathcal{C}$ and every [[natural transformation]] $\phi : X \to Y$ 

* $S^+(s)$ for the [[full subcategory]] of the [[slice category]] $S^+/s$ on the non-invertible morphisms into $s$;

* $S^-(s)$ for the [[full subcategory]] of the [[under category]] $s/S^-$ on the non-invertible morphisms out of $s$;

* write

  $$Latch_s(X) := {\lim_{\underset{(r \to s) \in S^+(s)}{\to}}} X(r)$$ 

  for the [[colimit]] of $X$ over $S^+(s)$, called the **latching object** of $X$ at $s$;

* write

  $$Match_s(X) := {\lim_{\underset{(s \to r) \in S^-(s)}{\leftarrow}}} X(r)$$ 
 
  for the [[limit]] of $X$ over $S^-(s)$, called the **matching object** of $X$ at $s$.

* write

  $$X_s \coprod_{Latch_s(X)} Latch_s(Y) \to Y_s$$ 

  for the universal morphism induced from the morphism $L_s(X) \to X_s$, called the **relative latching map** of $\phi$ at $s$;

* write

  $$X_s \to Match_s(X) \prod_{Match_s(Y)} Y_s$$ 

  for the dual universal morphism, called the **relative matching map** of $\phi$ at $s$.

=--

See _[[Joyal-Tierney calculus]]_ for more on these kinds of objects and morphisms.

+-- {: .num_remark}
###### Remark

In the above situation, the [[automorphism]] group $Aut_S(s)$ of $s$ canonically acts on all objects that appear, and all morphisms that appear respect this action.

Equivalently this means that for all $s$ the above objects and morphisms take place in the presheaf category $[B Aut(s), \mathcal{C}]$.

=--

+-- {: .proof}
###### Proof

Since limits and colimits in [[presheaf categories]] are computed objectwise.

=--


Choose now once and for all on all on $[\coprod_{s \in S} B Aut(s), \mathcal{C}]$ either the projective or the injective [[model structure on functors]] (if they exist). We will use the subscript "${}_{proj/inj}$", as in $[\coprod_{s \in S} B Aut(s), \mathcal{C}]_{proj/inj}$, to indicate some fixed choice. 


+-- {: .num_defn #ReedyModelStructure}
###### Definition

Let $S$ be a (Berger-Moerdijk)-[[generalized Reedy category]]. 

And $\mathcal{C}$ be a [[model category]] such that the [[model structure on functors]] $[\coprod_{s \in S} B Aut(s), \mathcal{C}]_{proj/inj}$ exists (sufficient for the projective structure is that $\mathcal{C}$ is a [[cofibrantly generated model category]] and sufficient for the injective structure is that it is a [[combinatorial model category]]). 

Write $[S, \mathcal{C}]$ for the [[category of presheaves]] on $S^{op}$ with values in $\mathcal{C}$.

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

  is a fibration in $[B Aut(s), \mathcal{C}]_{proj/inj}$;

* a **Reedy weak equivalence** if for each $s \in S$ the morphism

  $$
    f_s : X_s \to Y_s
  $$

  is a weak equivalence in $\mathcal{C}$.

=--

### Degreewise latching and matching objects
 {#GlobalLatchingObjects}

We discuss here an alternative way of speaking about the latching and matching objects, one where all indices at a given _degree_ $n \in \mathbb{N}$ are collected.

Recall from def. \ref{FirstNotation} that for $s \in S$ we write $S^+(s)$
for the category of non-invertible degree-increasing morphisms into $s$. We introduce the union of these categories over all objects of a fixed degree.

+-- {: .num_defn #SecondNotation}
###### Definition

For $n \in \mathbb{N}$ write

* $S^+(n) = \coprod_{s \in S \atop d(s) = n} S^+(s)$;

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

where the vertical morphisms are (non-full) inclusions and the square is a [[pullback]] (in the 1-category [[Cat]]) of an [[opfibration]].  Therefore it satisfies the [[Beck-Chevalley condition]] (see the discussion there) so that we have a [[natural isomorphism]]

$$
  (cod_n)_! i_n^* \simeq i_n^* (cod_n)_!
  \,,
$$

where $(cod_n)_!$ denotes left [[Kan extension]] along $cod_n$.

=--

+-- {: .num_remark #RestrictedCodomainIsOpfibration}
###### Remark

The restricted [[codomain fibration|codomain opfibration]] $cod_n : S^+((n)) \to G_n$ is indeed still an [[opfibration]]: it is the [[Grothendieck construction]] of the [[pseudofunctor]]

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
    Latch_n(X) := (cod_n)! dom_n^* X \in [G_n(S), \mathcal{C}]
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
$(cod_n)_!$ is the left [[Kan extension]] along an [[opfibration]]. By a standard fact (see [here](http://ncatlab.org/nlab/show/Kan+extension#AlongFibrations) at _[[Kan extension]]_) these are computed at any object by the colimit over the fiber over that object.

By definition, that fiber is 

$$
  cod_n^{-1}(s)
  = 
  \left\{
    \array{
      a &&\stackrel{\in S^+}{\to}&& b
      \\
      & \searrow^{\mathrlap{\in S^+}} && \swarrow_{\mathrlap{\in S^+}}  && non\; invertible
      \\
      && s
    }
  \right\}
  \,.
$$

This is indeed $S^+(s)$ (by the essential uniqueness of the $S^+\circ S^-$-factorization, this necessarily has the morphisms $a \to b$ in $S^+$, too.)

So 

$$
  \begin{aligned}
  ((cod_n)_! dom_n^* X)(s)
  & \simeq
  \lim_{\underset{S^+(s)}{\to}} (X \circ dom)
  \\
  & \simeq
  =: Latch_s(X)
  \end{aligned}
  \,.
$$
=--

An entirely dual discussion gives the degreewise matching objects: we have a diagram of categories

$$
  \array{
    S &\stackrel{cod_n}{\leftarrow}& S^-((n)) &\stackrel{dom_n}{\to}& G_n(S)
    &\stackrel{j_n}{\hookrightarrow}& S
    \\
    &&
    {}^{\mathllap{i_n}}\uparrow && \uparrow^{\mathrlap{i_n}}
    \\
    && S^+(n) &\stackrel{dom_n}{\to}& Obj(S)_n
  }  
  \,,
$$

and 

$$
  Match_n X := (dom_n)_* cod_n^* X
  \,,
$$

where $(dom_n)_*$ is the right [[Kan extension]] along $dom_n$.

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

+-- {: .num_remark }
###### Remark

Here $(t_n)_!$ and $(t_n)_*$ are indeed [[full and faithful functors]], as indicated.

=--

+-- {: .proof}
###### Proof

Since $t_{n-1}$ is a [[full and faithful functor]], so is its left Kan extension
(see [here](Kan+extension#LeftKanOnRepresentables) at _[[Kan extension]]_). Moreover in an [[adjoint triple]] the leftmost functor is full and faithful if and only if the rightmost one is.

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

For all $n \in \mathbb{N}$, the $n$th latching object, def. \ref{GlobalLatching}, is isomorphic to the $(n-1)$-skeleton in degree $n$, and dually, the degree-$n$ matching object is isomorphic to the $(n-1)$-coskeleton in degree $n$. Under these identifications the canonical morphisms on both sides match

$$
  Latch_n(X) \simeq (sk_{n-1}(X))_n
$$

$$
  Match_n(X) \simeq (cosk_{n-1}(X))_n
  \,.
$$


=--

This is ([Ber-Moer, lemma 6.2](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

Observe that for any $s \in S$ of degree $n$, the canonical inclusion

$$
  i_s : S^+(s) \hookrightarrow t_{n-1}/ s
$$

into the [[comma category]] is a [[cofinal functor]]: 

* for $d \to s$ any object in $t_{n-1}/s$ it factors essentially uniquely as $d \stackrel{\in S^-}{\to} \stackrel{\in S^+}{\to} s$, and hence the [[comma category ]] $d/i_s$ is non-empty;

* similarly, since every morphism factors essentially uniquely in $S$, there is a zig-zag between any two objects in $d / i_s$ constructed from the isomorphisms that exhibit the essentially unique factorization.

With this the statement follows from the fact that restriction along cofinal functors preserves colimits and the pointwise description of left [[Kan extension]] by [[colimits]] over comma categories:

$$
  \begin{aligned}
    sk_{n-1}(X)_n(s)
    & :=
    (j_n^* (t_{n-1})_! t_{n-1}^* X )(s)
    \\
    & \simeq 
    ((t_{n-1})_! t_{n-1}^* X )(s)
    \\
    & \simeq
    \lim_{\underset{t_{n-1}/ s }{\to}} X \circ t_{n-1}
    \\
    & \simeq 
    \lim_{\underset{S^+(s)}{\to}} X \circ dom_n
    \\
    & \simeq 
    Latch_n X
  \end{aligned}
  \,.
$$


=--

+-- {: .num_lemma #coSkeletonTower}
###### Lemma

The tower of inclusions

$$
  S_{0} \hookrightarrow S_{\leq 1} \hookrightarrow \cdots \hookrightarrow S_{\leq n-1}
  \stackrel{q_{n-1}}{\hookrightarrow} S_{\leq n} \hookrightarrow \cdots
$$

induces towers of [[natural transformations]]

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

The morphisms in the tower come from the [[unit of an adjunction|adjunction units and counits]]: the morphism 

$$
  sk_n X \to sk_{n+1} X
$$

is

$$
   (t_{n+1})_! (q_n)_! q_n^* t_{n+1}^*X \to  (t_{n+1})_! t_{n+1}^* X
  \,.
$$

Therefore a [[cocone]] under this morphism

$$
  \array{
    sk_{n-1} X &&\to& sk_n X
    \\
    & \searrow && \swarrow
    \\
    && Y
  }
$$

is equivalently a diagram

$$
  \array{
    (q_{n})_! q_{n}^* t_{n+1} X &&\to& t_{n+1}^* X
    \\
    & \searrow && \swarrow
    \\
    && t_{n+1}^* Y
  }
  \,,
$$

which in turn is equivalently just a morphism $t_n^* X \to t_n^* Y$. So 
a cocone under the whole tower is an object $Y$ equipped for each $n$ with 
a morphism $t_n^* X \to t_n^* Y$. Clearly $X$ itself is the [[initial object|inital]]
such object.

=--

+-- {: .num_lemma #IdempotenceOfCoSkeleta}
###### Lemma

For every $X \in [S, \mathcal{C}]$ and for all pairs $k,l \in \mathbb{N}$ with $k \leq l$, we have [[natural isomorphisms]]

$$
  sk_k sk_l \simeq sk_l sk_k \simeq sk_k
$$

and

$$
  cosk_k cosk_l \simeq cosk_l cosk_k \simeq cosk_k
  \,.
$$

=--

+-- {: .proof}
###### Proof

With the above notation we have $t_k = t_l \circ q_k$. Therefore for instance

$$
  sk_k sk_l X 
  \simeq
  (t_l)_! (q_k)_! q_k^* t_l^* (t_l)_! t_l^* X
  \,.
$$

Since the left adjoints here are [[full and faithful functors]] we have $t_l^* (t_l)_! \simeq id$ and hence

$$
  \cdots \simeq
  (t_l)_! (q_k)_! q_k^* t_l^* (t_l)_! t_l^* X
  \simeq
  sk_k X
  \,.
$$

Similarly for all the other cases.

=--

The following is a useful tool for inductively creating objects by adding higher degree components.

+-- {: .num_lemma #SkeletalExtension}
###### Lemma

Given 

* an object $X_{\leq (n-1)} \in [S_{\leq (n-1)}, \mathcal{C}]$;

* and an object $X_n \in [G_n(S), \mathcal{C}]$;

the choices of $X_{\leq n} \in [S_{\leq (n-1)}, \mathcal{C}]$
such that 

* $X_{\leq (n-1)} = t^*_{n-1} X_{\leq n}$ 

* $X_n = j_n^* X$;

are in bijection with choices of morphisms

$$
  Latch_n(X_{\leq (n-1)}) \to X_n \to Match_n(X_{\leq (n-1)})
$$

in $[G_n(S), \mathcal{C}]$.

Accordingly, given morphisms $f_{\leq (n-1)} : X_{\leq (n-1)} \to Y_{\leq (n-1)}$ and $f_n : X_n \to Y_n$, then choice of extensions to a morphism $f_{\leq n} : X_{\leq n} \to Y_{\leq n}$ are in bijection with choices of vertical morphisms in commuting diagrams

$$
  \array{
     Latch_n(X_{\leq (n-1)}) &\stackrel{Latch_n(f_{\leq (n-1)})}{\to}& Latch_n(Y_{\leq (n-1)})
     \\
     \downarrow && \downarrow
     \\
     X_n &\stackrel{f_n}{\to}& Y_n
     \\
     \downarrow && \downarrow
     \\
     Match_n(X_{\leq (n-1)})
     &\stackrel{Match_n(f_{\leq (n-1)})}{\to}&
     Match_n(Y_{\leq (n-1)})
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

If the object exists, then the morphisms do, by the above definitions/discussion. Conversely, given these morphisms, we take $X_{\leq n} : S \to \mathcal{C}$ to be given by $X_{\leq (n-1)}$ on morphism of degree $\leq (n-1)$, to be given by $X_n$ on morphisms between objects of degree $n$, and need to define it on the degree-changing morphisms to and from objects of degree $n$. This information is provided precisely by the co-cone components of $Latch_n(X) \to X_n$ and by the cone-components of $X_n \to Match_n(X)$.

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
  X_n \coprod_{Latch_n(X)} Latch_n(Y) \to Y_n
$$

is a cofibration in $[G_n(S), \mathcal{C}]_{proj/inj}$.

=--

+-- {: .proof}
###### Proof

The pushout in the presheaf category $[G_n(S), \mathcal{C}]$ is computed objectwise, so that the component of the $n$th relative latching morphism at $s \in S$ is the relative latching morphism at $s$, by prop. \ref{GlobalLatchingContainsLocalLatchings}.

The [[groupoid]] $G_n(S)$ is equivalent to the disjoint union $\coprod_{[r] \in \pi_0 G_n(S)} B Aut_S(s)$ of the automorphism groupoids of one representative in each isomorphism class. A morphism in $[G_n(S), \mathcal{C}]_{proj/inj}$ is a cofibration precisely if its restriction to all of the $[B Aut_{\mathcal{C}}(s), \mathcal{C}]_{proj/inj}$ is. 


=--

+-- {: .num_lemma #LiftingLemma}
###### Lemma

In the generalized Reedy structure, def. \ref{ReedyModelStructure}, the following holds.

* Acyclic Reedy cofibrations $f$ such that for all $n \in \mathbb{N}$ the morphism $Latch_n(f)$ is an objectwise acyclic cofibration have the [[left lifting property]] against fibrations;

* Reedy cofibration have the left lifting property against acyclic Reedy fibrations $g$ with the special property that all $Latch_n(g)$ are objectwise acyclic fibrations.

=--

This is ([Ber-Moer, lemma 5.2, lemma 5.4](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

We show the first clause. The second is dual. So let $f : X \to Y$ be an acyclic cofibration with the above extra property, and let $g : Y \to X$ be a fibration.
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

by stepwise constructing lifts in the skeletal filtration, lemma \ref{coSkeletonTower}.

At $n = 0$, observe that since $L_0(X) = \emptyset$ for all $X$, the fact that 

$$
  A_0 \coprod_{L_0(A)} L_0(B) \to B_0
$$

is a cofibration in $[G_0, \mathcal{C}]_{proj/inj}$ by assumption, means that in fact $f_0 : A_0 \to B_0$ is an acyclic cofibration here. Similarly $Y_0 \to X_0$ is a fibration there. But $G_0(S) = S_{\leq 0}$ and so the restriction of the lifting problem along $t_0$

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

has been found. By lemma \ref{LatchingIsSkeleton} this induces maps $Latch_n(B) \to Latch_n (Y)$ and $Match_n(B) \to Match_n(Y)$ from which we can build the commuting diagram

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
\]

in $[G_n(S), \mathcal{C}]$.

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

We observe now that finding a lift in (eq:MainLiftingDiagram) will complete the induction step. To see this in more detail, notice that in the top left the lift

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
       \downarrow & \nearrow_{\mathrlap{\gamma_n}}
       \\
       B_n
    }
  $$

* such that it makes

  $$
    \array{
      Latch_n(B) &\to& Latch_n(Y)
      \\  
      \downarrow && \downarrow
      \\
      B_n &\stackrel{\gamma_n}{\to}& Y_n
    }
  $$
  
  commute;

and in the bottom right the lift

$$
  \array{
     && Y_n
     \\
     & {}^{\mathllap{\gamma_n}}\nearrow & \downarrow
     \\
     B_n &\to& X_n \prod_{Match_n X} Match_n Y
  }
$$

is

* a lift in 

  $$
    \array{
      && Y_n
      \\
      & {}^{\mathllap{\gamma_n}}\nearrow & \downarrow
      \\
      B_n &\to& X_n
    }
  $$

* such that it makes 

  $$
    \array{
       B_n &\stackrel{\gamma_n}{\to}& Y_n
       \\
       \downarrow && \downarrow
       \\
       Match_n(B) &\to& Match_n(Y)
    }
  $$
 
  commute.


By lemma \ref{SkeletalExtension}, this is precisely the data that characterizes an extension of $\gamma_{\leq (n-1)}$ to $\gamma_{\leq n}$.


By assumption, the left vertical morphism in (eq:MainLiftingDiagram) is a cofibration in $[G_n, \mathcal{C}]_{proj/inj}$, and the right vertical morphism is a fibration there. Therefore to get the lift and hence complete the induction step, it is now sufficient to show that the left morphism is also a weak equivalence, hence is a weak equivalence in $\mathcal{C}$ over each $s \in S$.

Also by assumption we have that $Latch_n(f)_s$ is an acyclic cofibration in $\mathcal{C}$ for all $s$. Hence so is its pushout $A_s \to 
(A_s \coprod_{Latch_n(A)_s} Latch_n(B)_s)$. The morphism $v_n(s)$ finally sits in the diagram

$$
  \array{
    Latch_n(A)_s
    &\to&
    A_s &\underoverset{\simeq}{f_s}{\to}& B_s
    \\
    \downarrow^{\mathrlap{\simeq}} &&
    \downarrow^{\mathrlap{\simeq}}  & \nearrow_{\mathrlap{v_n(s)}}
    \\
    Latch_n(B)_s &\to& (A_s \coprod_{Latch_n(A)_s} Latch_n(B)_s)
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

is a pullback (in the 1-category [[Cat]]). Then for each $X \in [S, \mathcal{C}]$, there is a [[natural isomorphism]]

$$
  Latch_k(\phi^*(X)) \stackrel{\simeq}{\to} \phi_k^*(Latch_k X)
  \,,
$$


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

whose rows define, by prop. \ref{DiagramOfRestrictions}, the latching objects by pull-push. Since the pullback square, being the pullback of an [[opfibration]] (the [[codomain opfibration]]), satisfies the [[Beck-Chevalley condition]] (by the fact discussed [here](http://ncatlab.org/nlab/show/Beck-Chevalley+condition#PullbacksOfOpfibrations)), we find the intertwining isomorphism as follows:

$$
  \begin{aligned}
     Latch_k \phi^* X 
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
     Latch_k X
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
    t &\stackrel{\in S^+}{\to}& t'
    \\
    \downarrow^{\mathrlap{\in S^+}} && \downarrow^{\mathrlap{\in S^+}} && non\; invertible
    \\
    s &\stackrel{\simeq}{\to}& s' && deg = k
    \\
    \downarrow^{\mathrlap{\in S^+}} && \downarrow^{\mathrlap{\in S^+}} && non \; invertible
    \\
    r &\stackrel{id}{\to}& r  && deg = n
  }
  \right\}
  \,,
$$

where on the right the vertical sequences in $S$ indicate objects in $(S^+(m))^+((k))$ and the whole diagram on the right indicates a morphism there. 

One sees that this is indeed the fiber product as claimed.


=--

We now show that the extra condition in prop. \ref{LiftingLemma} is in fact automatic.

+-- {: .num_lemma #ExtraPropertyOfAcyclicCofibrations}
###### Lemma

Let $f : X \to Y$ in $[S, \mathcal{C}]$ be a Reedy cofibration, which is a weak equivalence on all objects of degree $\lt n$. Then the morphism $ Latch_n(f) :  Latch_n(X) \to  Latch_n(Y)$ is over each $s \in S$ an acyclic cofibration in $\mathcal{C}$


=--

This is ([Ber-Moer, lemma 5.3](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

We show this by induction over $n$, using the skeletal filtration def. \ref{SkeletaByAdjunction}. For $n = 0$ we have for all $X$ that
$Latch_n X = sk_{-1} X = \emptyset$, and hence the condition is trivially satisfied. 

So assume now that the statement has been shown for all $(k \lt n)$, then we need to show that $i_n^* Latch_n f$ is an acyclic cofibration in $[Obj(S)_n, \mathcal{C}]$, hence that every square of the form

$$
  \array{   
    i_n^* Latch_n A &\to& Y
    \\
    \downarrow^{\mathrlap{i_n^* Latch_n f}} && \downarrow^{g}
    \\
    i_n^* Latch_n B &\to& X
  }
$$

with $g$ a fibration in $[Obj(S)_n, \mathcal{C}]_{proj/inh}$ (hence over every object of degree $n$) has a lift. Since by lemma \ref{DiagramOfRestrictions} we have

$$
  i^*_n Latch_n := i_n^* cod_! dom_n^* \simeq cod_! i_n^* dom_n^*
$$

such a filler is equivalently a filler in 

\[
  \label{SomeLiftingDiagram}
  \array{
     i_n^* dom_n^* A &\to& cod_n^* Y
     \\
     {}^{\mathllap{i_n^* dom_n^*}}{}\downarrow && \downarrow
     \\
     i_n^* dom_n^* B &\to& cod_n^* X
  }
\]

being a diagram in $[S^+(n), \mathcal{C}]$.

We now establish such a filler by using lemma \ref{LiftingLemma} with the Reedy category in question being now $S^+(n)$. This has only $+$-morphisms and hence Reedy fibrations here are objectwise fibrations, so the morphism on the right is a Reedy fibration over $S^+(n)$.

Moreover, $i_n^* dom_n^* f$ is a Reedy weak equivalence in this structure, since all its objects have degree $\lt n$. It is now sufficient to show that the assumptions of lemma \ref{LiftingLemma} are satisfied over $S^+(n)$, to obtain the lift.

By lemma \ref{LatchingIntertwiner} the functor

$$
  (dom_n i_n)^* : [G_k(S), \mathcal{C}] \to [G_k(S^+(n)), \mathcal{C}]
$$

intertwines the latching objects on both sides. Therefore we have an isomorphism between the relative latching morphism of interest

$$
  (dom_n i_n)^* A \coprod_{Latch_k (dom_n i_n)^* A} Latch_k (dom_n i_n)^* k \to (dom_n i_n)^* B
$$

and the morphism

$$
  (dom_n i_n)_k^*\left(
    A_k \coprod_{Latch_k(A)} Latch_k(B)
    \to
    B_k
  \right)
  \,.
$$

Since $(dom_n i_n)_k$ is a [[faithful functor]] between groupoids, $(dom_n i_n)_k^*$ preserves cofibrations in the projective structure (and trivially does so always in the injective structure), and so the above relative latching morphism is a cofibration, hence $(dom_n i_n)^*(f)$ is a Reedy cofibration.
Similarly, since $Latch_k(f)$ is an acyclic cofibration by induction hypothesis, so is $Latch_k((dom_n i_n)_k^* f)$. This way the assumption of lemma \ref{LiftingLemma} are checked for (eq:SomeLiftingDiagram) and so we do have a lift.

=--

+-- {: .num_lemma #ExtraPropertyOfAcyclicFibrations}
###### Lemma

Dually, let $f : X \to Y$ in $[S, \mathcal{C}]$ be a Reedy fibration which is a weak equivalence over all objects of degree $\lt n$. Then the morphism $Match_n(f) :  Match_n(X) \to  Match_n(Y)$ is over each $s \in S$ an acyclic fibration in $\mathcal{C}$.

=--

This is ([Ber-Moer, lemma 5.4](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

(Essentially the dual proof to that above. 
Except for one slight difference in the last part. Here -- and only here --
do we need the last clause in the definition of [[generalized Reedy category]], the one that says that isomorphisms see the maps in $S_-$ as epimorphisms.)

=--

We can finally conclude:

+-- {: .num_prop }
###### Proposition

In the generalized Reedy model structure, def. \ref{ReedyModelStructure}, 

* acyclic cofibrations have the [[left lifting property]] against fibrations;

* cofibrations have the [[left lifting property]] against acyclic fibrations.


=--

+-- {: .proof}
###### Proof

By lemma \ref{ExtraPropertyOfAcyclicCofibrations} every acyclic Reedy cofibration induces a weak equivalence under $Latch_n$. By lemma \ref{LiftingLemma} this implies the left lifting property against Reedy fibrations. Dually for the second statement.

=--



### Factorization
 {#Factorization}

We demonstrate the factorization axiom in the Reedy model structure, def. \ref{ReedyModelStructure}.

+-- {: .num_lemma #AcyclicCoFibrationsByLatchingMatching}
###### Lemma

A morphism $f : X \to Y$ in $[S, \mathcal{C}]$ is both a cofibration and a weak equivalence according to def. \ref{ReedyModelStructure} precisely if the $n$th relative latching morphism (def. \ref{GlobalLatching})

$$
  X_n \coprod_{Latch_n(X)} Latch_n(Y) \to Y_n
$$

is an acyclic cofibration in $[G_n(S), \mathcal{C}]_{proj/inj}$ for all $n \in \mathbb{N}$.

Dually, a morphism $f : X \to Y$ in $[S, \mathcal{C}]$ is both a fibration and a weak equivalence according to def. \ref{ReedyModelStructure} precisely if the $n$th relative matching morphism (def. \ref{GlobalLatching})

$$
  X_n \to Y_n \prod_{Match_n(X)} Match_n(Y) 
$$

is an acyclic fibration in $[G_n(S), \mathcal{C}]_{proj/inj}$ for all $n \in \mathbb{N}$.

=--

This is ([Ber-Moer, prop. 5.6](#BergerMoerdijk)).

+-- {: .proof}
###### Proof


By definition, the morphisms $f_n : X_n \to Y_n$ factor as

$$
  f_n : 
  X_n 
   \stackrel{u_n}{\to}
  X_n
  \coprod_{Latch_n(X)} Latch_n (Y)
   \stackrel{v_n}{\to}
  Y_n 
  \,.
$$

If now $f$ is an acyclic Reedy cofibration, then by lemma \ref{ExtraPropertyOfAcyclicCofibrations} the morphism $Latch_n(X) \to Latch_n(Y)$ is over each object an acyclic cofibration in $\mathcal{C}$ and then so is $u_n$ above, being the pushout of this morphism. It follows by [[two-out-of-three]] that also $v_n$ is a weak equivalence for all $n$.

Conversely, assume that all $v_n$ here are weak equivalences. We show by induction on $n$ that then also the $u_n$ are weak equivalences, and hence that $f$ is a Reedy weak equivalence.

For $n = 0$ we have $u_0 = id$, and so this case is satisfied. So assume now that all $u_k$ for $k \lt n$ are weak equivalences. Then the assumptions of 
lemma \ref{ExtraPropertyOfAcyclicCofibrations} are again satisfied, and it follows that $Latch_n(f) : Latch_n(X) \to Latch_n(Y)$ is over each object an acyclic cofibration. Accordingly, so is $u_n$, being its pushout. Therefore, by induction, all $u_n$ are, in particular, weak equivalences.

The argument for fibrations is dual to this.

=--

+-- {: .num_prop }
###### Proposition

Every morphism in $[S, \mathcal{C}]$ factors as an acyclic Reedy cofibration (according to def. \ref{ReedyModelStructure}) followed by a Reedy fibration, and it factors as a Reedy cofibration followed by an acyclic Reedy fibration

=--

This is ([Ber-Moer, page 18](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

Let $f : X \to Y$ be any morphism in $[S, \mathcal{C}]$. 
We construct a factorization into an acyclic cofibration followed by a fibration by induction on the degree, i.e. by induction over the restrictions along $t_n^* : [S, \mathcal{C}] \to [S_{\leq n}, \mathcal{C}]$. The other case (cofibration followed by acyclic fibration) works dually.

For $n = 0$ we have $S_{\leq 0} = G_0(S)$ and we factor $f_0$ in the model structure $[G_0(S), \mathcal{C}]_{proj/inj}$

$$
  f_0 : X_0 \stackrel{\simeq}{\to} A_0 \to Y_0
  \,.
$$

Now assume for some $n \in \mathbb{N}$ that a factorization of 

$$
  f_{\leq (n-1)}
 : 
  X_{\leq (n-1)}
  \stackrel{\simeq}{\to}
  A_{\leq (n-1)}
  \to
  Y_{\leq (n-1)}
$$ 

has been found. This induces the commutative diagram

$$
  \array{
    Latch_n(X) &\to & Latch_n(A) &\to& Latch_n(Y)
    \\
    \downarrow && && \downarrow
    \\
    X_n && && Y_n
    \\
    \downarrow && && \downarrow
    \\
    Match_n(X) &\to & Match_n(A) &\to& Match_n(Y) 
  }
  \,.
$$


This diagram in turn induces a morphism

$$
  X_n \coprod_{Latch_n(X)} Latch_n(A)
  \to 
  Y_n \prod_{Match_n(Y)} Match_n(A)
$$

in $[G_n(S), \mathcal{C}]$, which we may factor as a trivial cofibration followed by a fibration 

$$
  X_n \coprod_{Latch_n(X)} Latch_n(A)
   \stackrel{\simeq}{\to}
   A_n
  \to 
  Y_n \prod_{Match_n(Y)} Match_n(A)
$$

in $[G_n(S), \mathcal{C}]_{proj/inj}$.

By lemma \ref{SkeletalExtension}, the "righmost component" of this data defines an extension of $A_{\leq (n-1)}$ to $A_{\leq n}$. The "leftmost component" defines a factorization of $f_n$ and the "middle component" says that this consistently extends the previously obtained factorization of $f_{\leq n}$.  With this, finally the two morphisms say that this new factorization is by an acyclic Reedy cofibration (by lemma \ref{AcyclicCoFibrationsByLatchingMatching}) followed by a Reedy fibration (by definition).


=--


## Properties

### Homotopy skeletal filtration and coskeleton tower
 {#HomotopySkeletalFiltration}

We discuss conditions on an object $X$ such that the skeletal/coskeletal towers
discussed [above](#SkeletaAndCoskeleta) are "homotopy good" in that they exhibit $X$ not just as the colimit/limit over the tower, but as the [[homotopy colimit]]/[[homotopy limit]].

+-- {: .num_lemma #QuillenPropertyOfCoSkeleta}
###### Lemma

For all $n \in \mathbb{N}$

1. The left Kan extension

   $$
     (t_n)_! : [S_{\leq n}, \mathcal{C}]_{gReedy} \to [S,\mathcal{C}]_{gReedy}
   $$

   is a [[left Quillen functor]].

1. The right Kan extension

   $$
     (t_n)_* : [S_{\leq n}, \mathcal{C}]_{gReedy} \to [S,\mathcal{C}]_{gReedy}
   $$

   is a [[right Quillen functor]].

1. The restriction functor

   $$
     (t_n)^* : [S, \mathcal{C}]_{gReedy} \to [S_{\leq n},\mathcal{C}]_{gReedy}
   $$

   is both a left and a right Quillen functor.

=--

This is ([Ber-Moer, lemma 6.4](#BergerMoerdijk)).


+-- {: .num_prop #ReedyCoFibrantImpliesCoFibrantTowers}
###### Proposition

1. If $X \in [S, \mathcal{C}]$ is Reedy cofibrant according to def. \ref{ReedyModelStructure}, then all $sk_n X$ are Reedy cofibrant and the canonical morphisms $sk_k X \to sk_l X$ are Reedy cofibrations. 

1. If $X \in \mathcal{C}$ is Reedy fibrant according to def. \ref{ReedyModelStructure} then all $cosk_n X$ are Reedy fibrant and the canonical morphisms $cosk_l X \to cosk_k X$ are Reedy fibrations. 


=--

This is ([Ber-Moer, prop. 6.5](#BergerMoerdijk)).

+-- {: .proof}
###### Proof

We discuss the skeleta. The case of coskeleta is dual.

By lemma \ref{IdempotenceOfCoSkeleta} it is sufficient to consider the
case $sk_n X \to sk_\infty X = X$.

To check that this is a Reedy cofibration if $X$ is Reedy cofibrant, consider the diagram that induces the relative latching object for this morphism

$$
  \array{
    Latch_k(sk_n X) &\to& Latch_k (X)
    \\
    \downarrow && \downarrow
    \\
    sk_n(X)_k &\to& X_k
  }
  \,.
$$ 

For $k \leq n$,  the horizontal morphisms are both isomorphisms. Because by lemma \ref{LatchingIsSkeleton} the top morphism is 

$$
  (sk_{k-1} sk_n(X))_k \to (sk_{k-1} X)_k
$$

and this is an iso by lemma \ref{IdempotenceOfCoSkeleta}. The bottom morphism is isomorphic to $(t_k^* sk_{n}(X))_k \to (t_k^* X)_k$ which is isomorphic to the identity by the kind of argument in lemma \ref{IdempotenceOfCoSkeleta}.

Therefore also the relative latching morphism is an isomorphism in this case (use that pushouts of isos are isos and use 2-out-of-3 for isos), hence in particular a cofibration. 

Similarly, for $k \gt n$ the left vertical map is an isomorphism, so that the relative latching morphism in this case is $Latch_k(X) \to X_k$, which is a cofibration by the assumption that $X$ is Reedy cofibrant.

Finally, that $sk_n X$ is cofibrant follows directly from lemma \ref{QuillenPropertyOfCoSkeleta}.

=--

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
