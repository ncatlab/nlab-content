
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **double functor** is a [[functor]] between [[double categories]].  Since if $C$ and $D$ are double categories, the only possible sort of functor $C\to D$ is a double functor, it is unambiguous to leave off the adjective and simply speak about "functors" between double categories.

However, just like [[2-functors]], double functors do come in different flavors: strict, pseudo/strong, lax, and oplax.  Moreover, these various flavors can be chosen more or less independently in the two directions of a double category (vertical and horizontal).  Thus we can have functors which are strict in both directions, strict in one direction and pseudo in the other, pseudo in both directions, strict in one direction and lax in the other, and so on.  (It's not clear whether lax+lax or lax+oplax are sensible, though.)

## Definitions

If $\mathcal{C}$ and $\mathcal{D}$ are strict double categories, i.e. [[internal categories]] in $\mathbf{Cat}$, then a strict double functor $\mathcal{C} \to \mathcal{D}$ is by definition an internal functor in $\mathbf{Cat}$.  Thus, it takes objects, arrows of both sorts, and squares in $\mathcal{C}$ to the same structures in $\mathcal{D}$, preserving sources and targets and also preserving all identities and composites.

In explicit terms:

\begin{definition}
   Let $\mathcal{C}$ and $\mathcal{D}$ be double categories. Denote by $v\mathcal{C}$ (resp. $v\mathcal{D}$) and $h\mathcal{C}$ (resp. $h\mathcal{D}$) the horizontal and vertical categories, respectively, underlying $\mathcal{C}$ (resp. $\mathcal{D}$). Moreover, let us denote by $\vert$ the horizontal composition of squares and by $\frac{\phantom{xx}}{\phantom{xx}}$ the horizontal one.

A double functor $F: \mathcal{C} \to \mathcal{D}$ consists of the following data:

* a function $F : Ob \mathcal{C} \to Ob \mathcal{D}$, called the *object part*,
* a functor $vF : v\mathcal{C} \to v\mathcal{D}$, called the *vertical part*, coinciding with $F$ on objects,
* a functor $hF : h\mathcal{C} \to h\mathcal{D}$, called the *horizontal part*, coinciding with $F$ on objects,
* for every square
$$\array{& X & \overset{f}\rightarrow & Z & \\
          g & \downarrow & \alpha &\downarrow & g'\\
          &Y & \underset{f'}\rightarrow& W & \\
}$$
in $\mathcal{C}$, a square
$$\array{& FX & \overset{hF(f)}\rightarrow & FZ & \\
          hF(g) & \downarrow & \square F\alpha &\downarrow & vF(g')\\
          &FY & \underset{hF(f')}\rightarrow& FW & \\
}$$
in $\mathcal{D}$,

obeying the following axioms:

* $\square F(\alpha \vert \beta) = \square F(\alpha) \vert \square F(\beta)$,
* $\square F\left(\frac{\alpha}{\beta}\right) = \frac{\square F(\alpha)}{\square F(\beta)}$,
* For each horizontal map $f : X \to Z$, $\square F(1^h_f) = 1^h_{hF(f)}$ ($\square F$ preserves horizontal identity squares),
* For each vertical map $g : X \to Y$, $\square F(1^v_g) = 1^v_{vF(g)}$ ($\square F$ preserves vertical identity squares)

\end{definition}

In practice, $vF$, $hF$ and $\square F$ are all denoted with the same symbol $F$ and the correct assignment is deduced from the type of object it is applied to.

## References

Definitions of double categories, double functors and more can be found in

* {#Myers21} [[David Jaz Myers]], _Categorical Systems Theory_, book in preparation, [github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book)

Double pseudofunctors are discussed in 

* {#Shulman07} [[Michael Shulman]], section 6 of _Comparing composites of left and right derived functors_, New York Journal of Mathematics 17 (2011), 75-125 ([arXiv:0706.2868](https://arxiv.org/abs/0706.2868))


[[!redirects double pseudofunctor]]
[[!redirects double pseudofunctors]]

[[!redirects pseudo double functor]]
[[!redirects lax double functor]]
[[!redirects oplax double functor]]
[[!redirects double functors]]
[[!redirects pseudo double functors]]
[[!redirects lax double functors]]
[[!redirects oplax double functors]]
