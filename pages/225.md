
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
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


## Size issues

If $C$ and $D$ are [[small category|small]], then $[C,D]$ is also small.

If $C$ is small and $D$ is [[locally small category|locally small]], then $[C,D]$ is still locally small.

Even if $C$ and $D$ are locally small, if $C$ is not small, then $[C,D]$ will usually not be locally small.

As a partial converse to the above, if $C$ and $[C,Set]$ are locally small, then $C$ must be [[essentially small category|essentially small]]; see [Freyd & Street (1995)](http://tac.mta.ca/tac/volumes/1995/n9/1-09abs.html).


## Related concepts

* [[2-functor 2-category]]

* [[(infinity,1)-category of (infinity,1)-functors]]

[[!redirects functor category]]
[[!redirects functor categories]]
[[!redirects diagram category]]
[[!redirects diagram categories]]

[[!redirects category of functors]]
[[!redirects categories of functors]]

[[!redirects functor groupoid]]
[[!redirects functor groupoids]]
