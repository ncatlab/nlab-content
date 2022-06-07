
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Functor categories
* table of contents
{: toc}

## Definition

Given [[category|categories]] $C$ and $D$, the **functor category** -- written $D^C$ or $[C,D]$ -- is the category whose

* [[object]]s are [[functor|functors]] $F: C \to D$  

* [[morphism]]s are [[natural transformation|natural transformations]] between these functors.

### In homotopy type theory
Note: the HoTT book calls a [[category]] a "precategory" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

For [[categories]] $A,B$, there is a [[category]] $B^A$, called the **functor category**, defined by

* $(B^A)_0$ is the type of [[functors]] from $A$ to $B$.
* $hom_{B^A}(F,G)$ is the type of [[natural transformations]] from $F$ to $G$.

**Proof.** We define $(1_F)_a \equiv 1_{F a}$. Naturality follows by the unit axioms of a [[category]]. For $\gamma : F \to G$ and $\delta : G \to H$, we define $(\delta \circ \gamma)_a \equiv \delta_a \circ \gamma_a$. Naturality follows by associativity. Similarly, the unit and associativity laws for $B^A$ follow from those for $B$. $\square$

We define a **natural isomorphism** to be an [[isomorphism]] in $B^A$.


## Usage
 
Functor categories serve as the [[hom-category|hom-categories]] in the [[strict 2-category]] [[Cat]].

In the context of [[enriched category theory]] the functor category is generalized to the [[enriched functor category]].

In the absence of the [[axiom of choice]] (including many [[internal category|internal]] situations), the appropriate notion to use is often instead the [[anafunctor category]].

## Properties

###  Limits and colimits and closure

If $D$ has [[limits]] or [[colimits]] of a certain shape, then so does $[C,D]$ and they are computed pointwise.  (However, if $D$ is not complete, then other limits in $[C,D]$ can exist "by accident" without being pointwise.)

If $C$ is small and $D$ is [[cartesian closed category|cartesian closed]] and [[complete category|complete]], then $[C,D]$ is cartesian closed.  See at _[[cartesian closed category]]_ for a proof.

### Accessibility and local presentability
  {#LocalPresentability}

Functor categories enjoy the following accessibility
and local presentability properties, as explained
by [[Zhen Lin Low]] at [nForum](http://nforum.mathforge.org/discussion/6152).

* $\kappa$-[[accessible functors]] from a $\kappa$-[[accessible category]] to any accessible category form an accessible category.  (It is not so easy to say what the accessibility rank is here.)

* $\kappa$-accessible functors from a $\kappa$-accessible category to any locally $\lambda$-[[locally presentable category|presentable category]] form a locally $\lambda$-presentable category.

* Cocontinuous functors between [[locally presentable categories]] form a locally presentable category.  More precisely, if $C$&#160;and&#160;$D$ are locally $\kappa$-presentable, then so is&#160;$[C,D]$.

* Continuous accessible functors between locally presentable categories form the opposite of a locally presentable category.  More precisely, if $C$&#160;and&#160;$D$ are locally $\kappa$-presentable, then so is $[C,D]^{\rm op}$.

Indeed, the point is this: given a $\kappa$-[[accessible category]] $\mathcal{C} \simeq Ind^\kappa (\mathcal{A})$ ($\mathcal{A}$ essentially small), the category of $\kappa$-accessible functors $\mathcal{C} \to \mathcal{D}$ (for arbitrary $\mathcal{D}$; here by "$\kappa$-accessible" we mean simply "preserves $\kappa$-filtered colimits") is naturally equivalent to the category of all $\mathcal{A} \to \mathcal{D}$. It should be well known that:

1. If $\mathcal{D}$ is accessible, then so is $[\mathcal{A}, \mathcal{D}]$.

2. If $\mathcal{D}$ is locally $\lambda$-presentable, then so is $[\mathcal{A}, \mathcal{D}]$.

3. Colimit-preserving functors out of a locally $\kappa$-presentable category are $\kappa$-accessible. 

4. A right adjoint between locally $\kappa$-presentable categories is $\kappa$-accessible if and only if its left adjoint is strongly $\kappa$-accessible (i.e. preserves $\kappa$-presentable objects as well as $\kappa$-filtered colimits); and every limit-preserving accessible functor between locally presentable categories is a right adjoint.

Statements 1 and 2 are proved in [Adamek and Rosick&#253;, _Locally presentable and accessible categories_], statement 3 is obvious, and statement 4 is a straightforward exercise. Thus the claims follow.

In general, accessible functors between accessible
categories do not form an accessible category
due to size issues.
The best one can hope for is a [[class-accessible category]].
Let $\mathcal{C}$ be an accessible category that is _not_ essentially small.
Consider the category $\mathcal{A}$ of all accessible functors $\mathcal{C} \to \mathbf{Set}$.
This is the same as the smallest full replete subcategory of $[\mathcal{C}, \mathbf{Set}]$ containing all representable functors and closed under small colimits.
In particular, $\mathcal{A}$ is accessible if and only if $\mathcal{A}$ locally presentable.
We claim $\mathcal{A}$ is not accessible.

Indeed, suppose $\mathcal{A}$ has a small generating family, say $\mathcal{G}$.
Then for some regular cardinal $\kappa$, every member of $\mathcal{G}$ is $\kappa$-accessible.
So consider $\mathcal{C} (X, -)$ for some object $X$ that is _not_ $\kappa$-presentable.
(Such an $X$ exists because $\mathcal{C}$ is _not_ essentially small.)
Since $\mathcal{G}$ generates, there is a small diagram of $\kappa$-accessible functors whose colimit is $\mathcal{C} (X, -)$.
But then $\mathcal{C} (X, -)$ is a retract of a $\kappa$-accessible functor and hence $\kappa$-accessible: a contradiction.
That said, $\mathcal{A}$ is a [[class-locally presentable category]].

### In homotopy type theory

#### Lemma 9.2.4 ####
A natural transformation $\gamma : F \to G$ is an isomorphism in $B^A$ if and only if each $\gamma_a$ is an isomorphism in $B$.

**Proof.** If $\gamma$ is an [[isomorphism]], then we have $\delta : G \to F$ that is its inverse. By definition of composition in $B^A$, $(\delta \gamma)_a \equiv \delta_a \gamma_a$. Thus, $\delta \gamma = 1_F$ and $\gamma \delta=1_G$ imply that $\delta_a \gamma_a = 1_{F a}$ and $\gamma_a \delta_a = 1_{G a}$, so $\gamma_a$ is an isomorphism.

Conversely, suppose each $\gamma_a$ is an [[isomorphism]], with inverse called $\delta_a$. We define a [[natural transformation]] $\delta : G \to F$ with components $\delta_a$; for the naturality axiom we have 
$$F f \circ \delta_a=\delta_b \circ \gamma_b \circ F f \circ \delta_a = \delta_b \circ G f \circ \gamma_a \circ \delta_a = \delta_b \circ G f$$

Now since composition and identity of [[natural transformations]] is determined on their components, we have $\gamma \delta=1_G$ and $\delta \gamma 1_F.\ \square$

#### Theorem 9.2.5 ####
If $A$ is a [[category]] and $B$ is a [[univalent category]], then $B^A$ is a [[univalent category]].

**Proof.** Let $F,G:A\to B$; we must show that $idtoiso:({F}={G}) \to (F\cong G)$ is an [[equivalence]].

  To give an inverse to it, suppose $\gamma:F\cong G$ is a [[natural isomorphism]].
  Then for any $a:A$, we have an [[isomorphism]] $\gamma_a:F a \cong G a$, hence an [[identity]] $isotoid(\gamma_a):{F a}={G a}$.
  By [[function extensionality]], we have an [[identity]] $\bar{\gamma}:{F_0}=_{(A_0\to B_0)}{G_0}$.

  Now since the last two axioms of a [[functor]] are [[mere propositions]], to show that ${F}={G}$ it will suffice to show that for any $a,b:A$, the functions
  
  $$ F_{a,b}:hom_A(a,b) \to hom_B(F a,F b) $$
  $$ G_{a,b}:hom_A(a,b) \to hom_B(G a,G b) $$

  become equal when [[transported]] along $\bar\gamma$.
  By computation for [[function extensionality]], when applied to $a$, $\bar\gamma$ becomes equal to $isotoid(\gamma_a)$.
  
+--{.query}
This reference needs to be included. For now as transports are not yet written up I didn't bother including a reference to the page [[univalent category]]. -Ali
=--

But by [**INCLUDE ME**], [[transporting]] $F f:hom_B(F a,F b)$ along $isotoid(\gamma_a)$ and $isotoid(\gamma_b)$ is equal to the composite $\gamma_b\circ F f\circ \inv{(\gamma_a)}$, which by naturality of $\gamma$ is equal to $G f$.

  This completes the definition of a function $(F\cong G) \to (F =G)$.
  Now consider the composite
  $$ (F= G) \to (F\cong G) \to (F =G). $$
  Since hom-sets are [[sets]], their [[identity types]] are [[mere propositions]], so to show that two [[identities]] $p,q:F =G$ are equal, it suffices to show that $p =_{{F_0}={G_0}}{q}$.
  But in the definition of $\bar\gamma$, if $\gamma$ were of the form $idtoiso(p)$, then $\gamma_a$ would be equal to $idtoiso(p_a)$ (this can easily be proved by induction on $p$).
  Thus, $isotoid(\gamma_a)$ would be equal to $p_a$, and so by [[function extensionality]] we would have ${\bar\gamma}={p}$, which is what we need.

  Finally, consider the composite
  $$(F\cong G)\to  ( F = G) \to (F\cong G). $$
  Since identity of [[natural transformations]] can be tested componentwise, it suffices to show that for each $a$ we have ${idtoiso(\bar\gamma)_a}={\gamma_a}$.
  But as observed above, we have ${idtoiso(\bar\gamma)_a}={idtoiso((\bar\gamma)_a)}$, while ${(\bar\gamma)_a}={isotoid(\gamma_a)}$ by computation for [[function extensionality]].
  Since $isotoid$ and $idtoiso$ are inverses, we have ${idtoiso(\bar\gamma)_a}={\gamma_a}$ as desired. $\square$

## Size issues

If $C$ and $D$ are [[small category|small]], then $[C,D]$ is also small.

If $C$ is small and $D$ is [[locally small category|locally small]], then $[C,D]$ is still locally small.

Even if $C$ and $D$ are locally small, if $C$ is not small, then $[C,D]$ will usually not be locally small.

As a partial converse to the above, if $C$ and $[C,Set]$ are locally small, then $C$ must be [[essentially small category|essentially small]]; see [Freyd & Street (1995)](http://tac.mta.ca/tac/volumes/1995/n9/1-09abs.html).


## Related concepts

* [[2-functor 2-category]]

* [[(infinity,1)-category of (infinity,1)-functors]]

* [[simplicial mapping complex]]

* [[inertia groupoid]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects functor category]]
[[!redirects functor categories]]
[[!redirects diagram category]]
[[!redirects diagram categories]]

[[!redirects category of functors]]
[[!redirects categories of functors]]

[[!redirects functor groupoid]]
[[!redirects functor groupoids]]
