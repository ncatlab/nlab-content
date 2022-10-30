
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

* $L_s(X) := {\lim_\to}_{(r \to s) \in S^+(s)} X(r)$ for the [[colimit]] of $X$ over $S^+(s)$, called the **latching object** of $X$ at $s$;

* $M_s(X) := {\lim_\leftarrow}_{(s \to r) \in S^-(s)} X(r)$ for the [[limit]] of $X$ over $S^-(s)$, called the **matching object** of $X$ at $s$.

* $X_s \coprod_{L_s(X)} L_s(Y) \to Y_s$ for the universal morphism induced from the morphism $L_s(X) \to X_s$, called the **relative latching map** of $\phi$ at $s$;

* $X_s \to M_s(X) \prod_{M_s(Y)} Y_s$ for the dual universal morphism, called the **relative matching map** of $\phi$ at $s$.

=--

See _[[Joyal-Tierney calculus]]_ for more on these kinds of objects and morphisms.

+-- {: .num_prop}
###### Proposition

In the above situation, the [[automorphism]] group $Aut_S(s)$ of $s$ canonically acts on all objects that appear, and all morphisms that appear respect this action.

Equivalently this means that for all $s$ the above objects and morphisms take place in the presheaf category $[B Aut(s), \mathcal{C}]$.

=--


+-- {: .num_defn #ReedyModelStructure}
###### Definition

Let $S$ be a (Cisinski-Moerdijk)-[[generalized Reedy category]]. And let $\mathcal{C}$ be a [[cofibrantly generated model category]]. Write $[S, \mathcal{C}]$ for the [[category of presheaves]] on $S^{op}$ with values in $\mathcal{C}$.

Call a morphism $f : X \to Y$ in $[S, \mathcal{C}]$

* a **Reedy cofibration** if for each $s \in S$ the relative latching map 

  $$
    X_s \coprod_{L_s(X)} L_s(Y) \to Y_s
  $$

  is a cofibration in $[B Aut(s), \mathcal{C}]_{proj}$;

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

where $[B Aut(r), \mathcal{C}]_{proj}$ is the projective [[model structure on functors]].

=--

### Global latching objects
 {#GlobalLatchingObjects}

We discuss here an alternative way of speaking about the latching objects, one where all indices at a given degree $n \in \mathbb{N}$ are unified.

Recall from def. \ref{FirstNotation} that for $s \in S$ we write $S^+(s)$
for the category of non-invertible degree-increasing morphisms into $s$. We introduce the union of these categories over all objects of a fixed degree.

+-- {: .num_defn #SecondNotation}
###### Definition

For $n \in \mathbb{N}$ write

* $S^+(n) = \coprod_{d(r) = n} S^+(r)$;

* $d_ n : S^+((n)) \to S$ for the restriction of the [[domain opfibration]] to objects that are non-invertible morphisms in $S^+$ with codomain in degree $n$ and to morphisms whose codomain is invertible, i.e. to diagrams of the form

  $$
    \array{
       a &\to& b
       \\
       \downarrow^{\mathrlap{\in S^+}} && \downarrow^{\mathrlap{\in S^+}} & not\, invertible
       \\
       s & \stackrel{\simeq}{\to} & s' & deg = n
    }
    \,;
  $$

* $k_n : S^+(n) \hookrightarrow S^+((n))$ for the [[full subcategory]] inclusion on constant codomains;

* $G_n(S) \subset Core(S)$ for the [[groupoid]] of objects of dgree $n$ and [[isomorphisms]] between them.

=--

+-- {: .num_prop }
###### Proposition

The above categories and functors arrange into a [[diagram]]

$$
  \array{
    S &\stackrel{d_n}{\leftarrow}& S^+((n)) &\stackrel{cod}{\to}& G_n(S)
    &\stackrel{j_n}{\to}& S
    \\
    &&
    {}^{\mathllap{i_n}}\uparrow && \uparrow^{\mathrlap{i_n}}
    \\
    && S^+(n) &\stackrel{cod}{\to}& Obj(S)_n
  }  
  \,,
$$

where the vertical morphisms are (non-full) inclusions and the square is a [[pullback]] of an [[opfibration]].  Therefore it satisfies the [[Beck-Chevalley condition]] so that we have a [[natural isomorphism]]

$$
  cod_! i^* \simeq i^* cod_!
  \,.
$$


=--

+-- {: .num_defn #GlobalLatching}
###### Definition

For $n \in \mathbb{N}$, let $X \in [S, \mathcal{C}]$. Write 

* $X_n := j_n^* X \in [G_n(S), \mathcal{C}]$;

* the **$n$th latching object** is 

  $$
    L_n(X) := cod_! d_n^* X \in [G_n(S), \mathcal{C}]
    \,.
  $$

=--

+-- {: .num_prop }
###### Proposition

For $s \in Obj(S)_n$ we have

$$
  L_n(X) : s \mapsto L_s(X)
  \,.
$$

=--

(...)

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

+-- {: .num_prop }
###### Observation

A morphism $f : X \to Y$ in $[S, \mathcal{C}]_{gReedy}$ is a cofibration
precisely if for all $n \in \mathbb{N}$ the global relative latching morphism, def. \ref{GlobalLatching}

$$
  X_n \coprod_{L_n(X)} L_n(Y) \to Y_n
$$

is a cofibration in $[G_n(S), \mathcal{C}]$.

=--

+-- {: .num_lemma }
###### Lemma

(...)

=--

(...)

### Factorization
 {#Factorization}

(...)

## Properties

### General

+-- {: .num_theorem }
###### Theorem

Let $S$ be a (Cisinski-Moerdijk)-[[generalized Reedy category]]. And let $\mathcal{C}$ be a [[cofibrantly generated model category]].

Then with cofibrations, fibrations and weak equivalences as in def. \ref{ReedyModelStructure}, $[S, \mathcal{C}]$ is a [[model category]].

=--

This is ([Berger-Moerdijk, theorem 1.6](#BergerMoerdijk)).


### Relation to other model structures

(...)

## Examples

* Every ordinary [[Reedy category]] is a generalized Reedy category, and in this case the above model structure reduces to the traditional [[Reedy model structure]].

* The [[model structure for dendroidal complete Segal spaces]] is a [[Bousfield localization of model categories|left Bousfield localization]] of the generalized Reedy model structure over the [[tree category]].

## Related concepts

* [[Joyal-Tierney calculus]]

## References 

* [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_, Math. Z. (2008) ([arXiv:0809.3341](http://arxiv.org/abs/0809.3341))
 {#BergerMoerdijk}
