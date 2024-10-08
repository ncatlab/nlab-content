+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


* table of contents
{: toc}

## Idea

A **promonoidal category** is like a [[monoidal category]] in whose structure (namely, [[tensor product]] and [[unit object]]) we have replaced [[functors]] by [[profunctors]].

## Definition

A **promonoidal category** is a [[pseudomonoid]] in the [[monoidal bicategory]] [[Prof]].  This means that it is a [[category]] $A$ together with

* A [[profunctor]] $P \colon A\times A &#8696; A$.
* A profunctor $J\colon 1$ &#8696; $A$.
* [[associator|Associativity]] and [[unitor|unit isomorphisms]] $P \odot (P\times 1) \cong P\odot (1\times P)$, $P\odot (J\times 1) \cong 1$, and $P\odot (1\times J) \cong 1$.
* The usual [[pentagon identity|pentagon]] and unit conditions hold, as in a [[monoidal category]].

Recalling that a profunctor $A$ &#8696; $B$ is defined to be a functor of the form $B^{op}\times A \to Set$, we can make this more explicit.  We can also generalize it by replacing [[Set]] by a [[Benabou cosmos]] $V$ and $A$ by a $V$-[[enriched category]]; then a profunctor is a $V$-[[enriched functor]] $B^{op}\times A \to V$.

Thus, we obtain the following as an explicit definition of **promonoidal $V$-category**: 

We have the following data

1. A $V$-[[enriched category]] $A$.

1. A $3$-ary [[enriched functor]] $P:A^\op \otimes A \otimes A\to V$.  For notational clarity, we may write $P(a,b,c)$ as $P(a,b \diamond c)$.

1. A $V$-functor $J:A^{op}\to V$.

and [[enriched natural isomorphisms]]

1. $\lambda_{ab}:\int^x (J(x) \otimes P(b,a \diamond x))\to A(b,a)$

1. $\rho_{ab}: \int^x ( J(x)\otimes P(b,x \diamond a))\to A(b,a)$

1. $\alpha_{abcd}: \int^x (P(x,a\diamond b)\otimes P(d,x\diamond c)) \to \int^x(P(x,b\diamond c)\otimes P(d,a\diamond x))$

satisfying the pentagon and unit axioms for promonoidal categories. Explicitly, writting $P^{A}_{B,C}$ for $P(A,B;C)$, $\mathsf{h}^{A}_{B}$ for $\mathrm{Hom}_{A}(A,B)$, $J^X$ for $J(X)$, and $\diamond$ for composition of profunctors, we require the following conditions to hold:

1. **The triangle identity for promonoidal categories.** For each $A,B,C\in\mathrm{Obj}(A)$, the [[diagram]]

   \begin{imagefromfile}
       "file_name": "pro-triangle-corrected.svg"
   \end{imagefromfile}

   [[commuting diagram|commutes]];

1. **The pentagon identity for promonoidal categories.** For each $A,B,C,D,E\in\mathrm{Obj}(A)$, the [[diagram]]

   \begin{imagefromfile}
       "file_name": "pro-pentagon.svg"
   \end{imagefromfile}

   [[commuting diagram|commutes]].


## Properties

### Versus monoidal categories

Since any functor induces a representable profunctor, any monoidal category can be regarded as a promonoidal category.  A given promonoidal category arises in this way if and only if the profunctors $P$ and $J$ are representable.

### Day convolution

A promonoidal structure on $A$ suffices to induce a monoidal structure on $V^{A^{op}}$ by [[Day convolution]].  In fact, given a small $V$-category $A$, there is an equivalence of categories between

1. the category of pro-monoidal structures on $A$, with strong pro-monoidal functors between them, and 

1. the category of biclosed monoidal structures on $V^{A^{op}}$, with strong monoidal functors between them.

### Versus multicategories

A promonoidal structure on $A$ can be identified with a particular sort of [[multicategory]] structure on $A^{op}$, i.e. with a co-multicategory structure on $A$.  The set $P(x, y, z)$ is regarded as the set of co-multimorphisms $x \to (y,z)$.

More generally, we define a co-multicategory $\bar A$ as follows.  The objects of $\bar A$ are the objects of $A$.  The co-multimorphisms $b\to a_1\dots a_n$ in $\bar A$ are defined by induction on $n$ as follows: $\bar A(b;)=Jb$, and $\bar A(b;a_1,\dots,a_{n+1})=\int^x\bar A(x;a_1,\dots,a_n)\otimes P(b,x\diamond a_{n+1})$.

Not every co-multicategory arises from a promonoidal one in this way.  Roughly, a promonoidal category is a co-multicategory whose $n$-ary co-multimorphisms are determined by the binary, unary, and nullary morphisms.  In general, co-multicategories can be identified with a certain sort of "lax promonoidal category".

In fact, promonoidal categories correspond exactly to the [[exponentiable]] multicategories: see [[multicategory]] for more information.

## Notes

[[Brian Day]] introduced the notion of a "premonoidal" category in [(Day 1970)](#Day70), and later renamed this to a "promonoidal" category in [(Day 1974)](#Day74) while reformulating the identity and associativity isomorphisms $\lambda,\rho,\alpha$ explicitly in terms of profunctor composition.  However, note that his definition is op'd from the definition used in this article, in the sense that a Day-promonoidal structure on a category $C$ corresponds to a pseudomonoid structure on $C^{op}$ in [[Prof]].  In particular, one example Day considers is that of a [[closed category]], which is actually a co-promonoidal category in the sense used here (analogous to the co-promonoidal structure on a multicategory described above).

Regarding monoidal categories as promonoidal is useful in order to express extra structure on them, such as [[closed monoidal category|closedness]], [[star-autonomous category|$\ast$-autonomy]], or [[compact closed category|compact closedness]], in abstract bicategorical terms: these notions can be defined by adding extra structure to a [[pseudomonoid]] in the [[monoidal bicategory]] [[Prof]] (i.e. a promonoidal category), but the extra structure does not lie inside the sub-monoidal bicategory [[Cat]].

## Related pages

* [[monoidal category]], [[multicategory]]
* [[Day convolution]]
* A (co-)promonoidal [[poset]] is called a [[ternary frame]], when its Day convolution monoidal category is used to model [[substructural logic]].

## References

* {#Day70} [[Brian Day]], On closed categories of functors, _Lecture Notes in Mathematics_ 137 (1970), 1-38.

* {#Day74} [[Brian Day]], An embedding theorem for closed categories, _Lecture Notes in Mathematics_ 420 (1974), 55-64.

* Day, Panchadcharam and Street, *On centres and lax centres for promonoidal categories*.

The relationship between [[multicategories]], [[promonoidal categories]], [[lax monoidal categories]], and [[monoidal categories]] is exposited in:

* [[Brian Day]] and [[Ross Street]], _Lax monoids, pseudo-operads, and convolution_, Contemporary Mathematics 318 (2003): 75-96.

[[!redirects promonoidal categories]]
[[!redirects pro-monoidal category]]
[[!redirects pro-monoidal categories]]
[[!redirects promonoidal structure]]
[[!redirects pro-monoidal structure]]
[[!redirects promonoidal structures]]
[[!redirects pro-monoidal structures]]
