
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

An [[elementary topos]] $E$ is **well-pointed** if

1. the [[terminal object]] 1 is a [[separator|generator]];

   * equivalently: the [[global section]] functor $\Gamma : E \to Set = E(1, -)$
   is a [[faithful functor]];

   * equivalently: if $f, g: a \rightarrow b$ are morphisms such that $f x = g x$ for all [[global element]]s $x: 1 \to a$, then $f = g$;

   * equivalently: the family of all global elements $x: 1 \to a$ is a [[jointly epimorphic family]].

2. and $E$ is nondegenerate, i.e., 1 is not an [[initial object]].


## Examples

* The category [[Set]].  Here the [[global section]] functor is even (isomorphic to) the identity functor.

* Any model of [[ETCS]].


## Properties

### Strong generation

In a well-pointed topos, the terminal object is even a [[strong generator]],

  * equivalently: the global section functor $E(1,-)$ is a [[conservative functor]].
  * equivalently: if $f:A\to B$ induces a bijection $E(1,A) \cong E(1,B)$, then $f$ is an isomorphism.
  * equivalently: if $m:A\rightarrowtail B$ is a [[monomorphism]] such that every global element $1\to B$ factors through $A$, then $m$ is an isomorphism.

To prove the last version, let $\chi_A : B\to \Omega$ be the classifying map of $A$, and let $\top : B\to \Omega$ be the classifying map of the maximal subobject.  If every global element $b:1\to B$ factors through $A$, then $\chi_A b = \top b$ for all such $b$.  Hence $\chi_A = \top$ by well-pointedness, so $A$ is isomorphic to the maximal subobject.

Note that in any category with [[equalizers]], a strong generator is automatically a generator, since the equalizer of two parallel morphisms is the maximal subobject just when the two morphisms are equal.  So the above statements are also equivalent to well-pointedness.

### Boolean properties

Assuming that one accepts [[excluded middle]] in one\'s metalogic, a well-pointed topos is also [[Boolean topos|Boolean]].  To see this, let $U\rightarrowtail A$ be a subobject and $\neg U$ its [[Heyting algebra|Heyting complement]].  Then by definition, the global elements of $\neg U$ are precisely the global elements of $A$ that do not factor through $U$.  But then every global element of $A$ factors through $U \cup \neg U$, hence by strong generation $U\cup \neg U = A$.

Similarly, a well-pointed topos is [[two-valued topos|two-valued]].  In other words, that is, the only [[global element|global elements]] of the [[subobject classifier]] are $\top$ and $\bot$ (and these are distinct, by nondegeneracy) -- or equivalently, the only [[subterminal objects]] are $0$ and $1$.  To see this, note by strong generation a subobject of any object is uniquely determined by the global elements that factor through it.  But $1$ has only one global element, so it only has two possible global elements.

Finally, a well-pointed topos has [[split supports]].  For the support of any object $A$ must be either $0$ or $1$ by two-valuedness.  If it is $0$ then $A\cong 0$ also and its support is split.  Otherwise, $A\ncong 0$; now consider the two coproduct inclusions $inl, inr : A \rightrightarrows A+A$.  Their pullback is $0$ by disjointness.  Since $A\ncong 0$, we have $inl\neq inr$, hence by well-pointedness there is a global element $a:1\to A$ such that $inl a \neq inr a$.  Thus $a$ splits the support of $A$.

Conversely, we have the following:

\begin{theorem}\label{BooleanTwovaluedSupportssplit}
If $E$ is nondegenerate (i.e. $1\ncong 0$), Boolean, two-valued, and split supports, then it is well-pointed.
\end{theorem}
\begin{proof}
This is Proposition 9.33 on p. 314 of [Johnstone, Topos Theory](#Johnstone77), attributed there to [Freyd](#Freyd70).  Let $A\rightarrowtail B$ be a monomorphism such that every global element of $B$ factors through it.  Then $\forall_B A$ is a subterminal object, hence either $1$ or $0$.  If it is $0$, then its complement $\neg\forall_B A = \exists_B \neg A$ is $1$, which is to say that $\neg A$ is well-supported.  Hence, since supports split, $\neg A$ has a global element, which is impossible since every global element of $B$ factors through $A$.  Hence it must be that $\forall_B A = 1$, which implies $A=B$.
\end{proof}

Thus, in external classical logic, a topos is well-pointed if and only if it is nondegenerate, Boolean, two-valued, and has split supports.  In particular, a nondegenerate two-valued topos satisfying the external [[axiom of choice]] is well-pointed.

### Logical properties

The main point of a well-pointed topos in logic is the equivalence of *external* and *internal* properties. In particular, a statement in the [[internal logic]] of the topos will be satisfied if and only if it holds for all global terms. (For the 'only if' part, it is necessary that the topos be nondegenerate.)


## Generalizations
{#general}

### In constructive mathematics

To maintain this logical result in [[constructive mathematics]] (that is, without excluded middle in the metalogic), one must add  the following requirements:

3. the terminal object is [[indecomposable object|indecomposable]], and
4. the terminal object is [[projective object|projective]].

These are analogues, for [[disjunction]] and [[existential quantification]], of the nondegeneracy requirement (which is about [[falsehood]]).  Classically, they follow from the two conditions given above.

Incidentally, a well-pointed topos in a constructive metalogic is still "two-valued" in the sense that a global element of the subobject classifier is false if and only if it is not true.  However, it is not two-valued in the (classically equivalent) sense that every global element of the subobject classifier is either true or false.


### In a pretopos or coherent category

If $E$ is only a [[pretopos]] or a [[coherent category]], we have to strengthen the condition that 1 is a generator to the condition that 1 is a [[separator|extremal generator]], i.e. for any monomorphism $m:A\to B$, if every global element $1\to B$ factors through $m$, then $m$ is an isomorphism.  In a category with a subobject classifier (such as a topos), any generator is a extremal generator.

This strengthening is important in [[predicative mathematics]], where the category of sets (and in general, a [[Grothendieck topos|category of sheaves]]) is a pretopos but need not be a topos. But of course, the same applies whenever one is studying an arbitrary pretopos, not just a predicative version of $Set$.

### In a lextensive category

If $E$ is only a [[lextensive category]], such as in a [[category of sets]] without [[quotient sets]] (as commonly found in the [[syntactic category]] of an [[extensional type theory]]), then $1$ is only a [[initial object|noninitial]] [[indecomposable object|indecomposable]] [[extremal epimorphism|extremal]] [[generator]]. 

### In more general categories

Do we know what these should be in any more general situations?

[[Mike Shulman]]: Well, the pretopos version makes sense in any [[coherent category]], and I would bet that it's the right notion in that generality.  In a [[regular category]] one might just want to assert that $1$ is a (regular-)projective extremal generator, which would probably be enough for regular logic.  And in a category with mere finite limits, being a extremal generator is all one could ask for, and that'd probably be enough for finite-limit logic.


### Well-pointed $(\infty,1)$-toposes {#Infty1Version}

> [[Urs Schreiber|Urs]]: an attempt

One might like to say that "[[∞Grpd]] is essentially the unique [[(∞,1)-topos]] with all small limits and colimits that is well-pointed ."

Possibly one should say: an $(\infty,1)$-topos $\mathbf{H}$ is _well-pointed_ if the terminal object is not the initial one and the  [[global section]] [[(∞,1)-functor]] $\Gamma : \mathbf{H} \to \infty Grpd$ is faithful...

...which should mean that on hom-$\infty$-groupoids it is a [[monomorphism in an (∞,1)-category]]...

...which should mean that for all $X,Y \in \mathbf{H}$ the image of the morphism $\Gamma_{X,Y} : \mathbf{H}(X,Y) \to Func(\Gamma(X),\Gamma(Y))$ in the [[homotopy category]] identifies $\mathbf{H}(X,Y)$ as a [[direct sum]]mand of $Func(\Gamma(X),\Gamma(Y))$.

## Related entries

* [[ETCS]]

## References

* {#MM} [[Sheaves in Geometry and Logic]], Sections VI.1 and 10. Thm. \ref{BooleanTwovaluedSupportssplit} in this article is a strengthening of SGL's Prop. VI.1.7. SGL's Section VI.10 is a comparison of well-pointed toposes to RZC (Restricted Zermelo with Choice).

* {#Freyd70} [[Peter Freyd]], _Aspects of Topoi_, Bull. Austral. Soc. Math. no.7 pp.1-76,467-480 (1970).
 
* {#Johnstone77} [[Peter Johnstone]], _Topos Theory_, Academic Press New York 1977. (also available as Dover reprint, Minneola 2014).  See Section 9.3.


[[!redirects well-pointed topos]]
[[!redirects well-pointed toposes]]
[[!redirects well-pointed topoi]]
[[!redirects well pointed topos]]
[[!redirects well pointed toposes]]
[[!redirects well pointed topoi]]

[[!redirects well-pointed pretopos]]
[[!redirects well-pointed pretoposes]]
[[!redirects well-pointed pretopoi]]
[[!redirects well pointed pretopos]]
[[!redirects well pointed pretoposes]]
[[!redirects well pointed pretopoi]]

[[!redirects well-pointed category]]
[[!redirects well-pointed categories]]
[[!redirects well pointed category]]
[[!redirects well pointed categories]]
