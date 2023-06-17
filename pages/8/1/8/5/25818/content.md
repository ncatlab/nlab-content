
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

Consider the statement:

> If $f$ is a fully faithful and essentially surjective functor, then it is an [[equivalence of categories]].

If we use a set-theoretic foundation for mathematics, then this statement is equivalent to the [[axiom of choice]].  However, as we now show, in the [[michaelshulman:internal logic of a 2-category|internal logic]] of a [[regular 2-category]], it is simply *true*.  Thus, it should really be regarded as a "functor comprehension principle" or an "axiom of non-choice," analogous for categories to the fact (true in any regular 1-category) that any injective and surjective function of sets is an isomorphism, or equivalently that one can always make "choices" when those choices are uniquely specified.

We start by characterizing full, faithful, and eso morphisms in the internal logic.

## Faithful morphisms

Consider first the following theory with two 1-types $A$ and $B$:

* $x:A \vdash f(x):B$
* $x:A, y:A, \alpha: hom_A(x,y), \beta : hom_A(x,y), f(\alpha)=f(\beta) \vdash \alpha = \beta$

Of course, the first axiom interprets by a morphism $f\colon A\to B$.  This induces a map from $ker(A) \to (f/f)$ over $A\times A$.  The context of the second axiom above is the kernel pair of this map (as a map between discrete objects in $K/A\times A$); thus the second axiom asserts that this kernel pair factors through the diagonal of $ker(A)$, and hence is monic.  But this is equivalent to saying that $f$ is faithful, so a model of this theory in a lex 2-category is precisely a faithful morphism.


## Full and ff morphisms

Now consider the following theory, again with two 1-types $A$ and $B$:

* $x:A \vdash f(x):B$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash \exists \bar{\gamma}:hom_A(x,y). f(\bar{\gamma})=\gamma$

In a regular 2-category, the truth of this axiom asserts that the map $ker(A) \to (f/f)$ is eso, which implies that $f$ is a [[michaelshulman:full morphism]].  The converse is true at least in an exact 2-category.  It is also true if $f$ is additionally faithful, since then $ker(A) \to (f/f)$ is ff, hence (if also eso) an equivalence, so that $f$ is ff (and in particular full).  Therefore, a model of the combined theory

* $x:A \vdash f(x):B$
* $x:A, y:A, \alpha: hom_A(x,y), \beta : hom_A(x,y), f(\alpha)=f(\beta) \vdash \alpha = \beta$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash \exists \bar{\gamma}:hom_A(x,y). f(\bar{\gamma})=\gamma$

in a regular 2-category is precisely a ff morphism.

In a merely lex 2-category, we can instead consider the theory

* $x:A \vdash f(x):B$
* $x:A, y:A, \alpha: hom_A(x,y), \beta : hom_A(x,y), f(\alpha)=f(\beta) \vdash \alpha = \beta$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash \bar{\gamma}:hom_A(x,y)$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash f(\bar{\gamma})=\gamma$

The first two axioms give a faithful morphism $f\colon A\to B$, as above, and now the third and fourth axioms supply a section of the map $ker(A) \to (f/f)$, which is thus both ff and split epic, hence an equivalence.  Thus, a model of this theory in a lex 2-category is also precisely a ff morphism.

I don't know whether there is a theory in lex 2-logic whose models in lex 2-categories are precisely full morphisms, but I suspect not.  I also don't know whether there is a theory in regular 2-logic whose models in non-exact regular 2-categories are precisely full morphisms.


## Eso morphisms

Now consider the regular 2-theory

* $x:A \vdash f(x):B$
* $y:B \vdash \exists x:A. \exists i:iso_B(f(x),y)$

Since $iso_B(f(x),y)$ in context $x:A,y:B$ is interpreted by $(1,f)\colon A\to A\times B$, the second axiom asserts that the image of the composite $A \overset{(1,f)}{\to} A\times B \to B$ is all of $B$, i.e. that this composite is eso.  But this composite is clearly just $f$, so a model of this theory is precisely an eso morphism.

Of course, we can then write the combined theory

* $x:A \vdash f(x):B$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash \exists \bar{\gamma}:hom_A(x,y). f(\bar{\gamma})=\gamma$
* $y:B \vdash \exists x:A. \exists i:iso_B(f(x),y)$

whose models in exact 2-categories are precisely the eso+full morphisms.


## Equivalences

It follows from the above considerations that a model of the following theory:

* $x:A \vdash f(x):B$
* $x:A, y:A, \alpha: hom_A(x,y), \beta : hom_A(x,y), f(\alpha)=f(\beta) \vdash \alpha = \beta$
* $x:A, y:A, \gamma: hom_B(f(x),f(y)) \vdash \exists \bar{\gamma}:hom_A(x,y). f(\bar{\gamma})=\gamma$
* $y:B \vdash \exists x:A. \exists i:iso_B(f(x),y)$

in a regular 2-category is precisely a morphism $f$ which is ff and eso, i.e. an equivalence.  Since this theory evidently asserts that $f$ is "faithful, full, and essentially surjective on objects" in the internal logic, this is the desired "functor comprehension principle."

Of course, in a [[Heyting 2-category]], the latter three axioms can equivalently be stated as

* $\vdash \forall x:A, \forall y:A, \forall \alpha: hom_A(x,y), \forall \beta : hom_A(x,y), f(\alpha)=f(\beta) \Rightarrow \alpha = \beta$
* $\vdash \forall x:A, \forall y:A, \forall \gamma: hom_B(f(x),f(y)), \exists \bar{\gamma}:hom_A(x,y). f(\bar{\gamma})=\gamma$
* $\vdash \forall y:B, \exists x:A. \exists i:iso_B(f(x),y)$

which have perhaps the most familiar form.

## References

The above definitions and observations are originally due to

* [[Michael Shulman]], _[[michaelshulman:functor comprehension principle]]_ 