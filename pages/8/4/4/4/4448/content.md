
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Freyd cover** $\overline{\mathcal{T}}$ of a [[topos]] $\mathcal{T}$, or more generally of a [[category]] with a [[terminal object]],  is a  way to turn $\mathcal{T}$, viewed as an 'abstract' category, into a 'concrete' category of structured sets by sewing it together with [[Set]] along the [[global section functor]].

As $\overline{\mathcal{T}}$ comes equipped with two well-behaved projection functors the resulting category has many good logical properties making the construction an important tool in [[type theory]] and theoretical computer science. 

The Freyd cover is sometimes known as the **Sierpinski cone** or **scone**, because in [[topos theory]] it behaves similarly to the [[cone]] on a space, but with the [[interval]] $[0,1]$ replaced by the [[Sierpinski space]].

## Definition

Let $\mathcal{T}$ be a category with a terminal object and $\Gamma = \mathcal{T} (1, -)$ the global section functor . The **Freyd cover** of $\mathcal{T}$ is the category  $\overline{\mathcal{T}}$ whose objects are triples $(X, \xi, U)$ where:

* $X$ is a set
* $U$ is an object of $\mathcal{T}$
* $\xi$ is a function $X \to \Gamma (U)$

A morphism from $(X,\xi, U)$ to $(Y,\eta , V)$ is a pair of morphisms $(\varphi :X\to Y, t:U\to V)$ with $\varphi\in Set$ and $t\in \mathcal{T}$ such that $\eta\varphi=\Gamma(t)\xi$.

### Remark

The construction is a special case of [[Artin gluing]]: i.e.  $\overline{\mathcal{T}}$ is the [[comma category]] $Set \downarrow \Gamma$ with $\Gamma = \mathcal{T} (1, -)$.

## Properties

### Relation to the initial topos

One of the first applications of the Freyd cover was to deduce facts about the initial topos (initial with respect to [[logical morphism|logical morphisms]] --- also called the [[free topos]]). They were originally proved by syntactic means; the conceptual proofs of the lemma and theorem below are due to Freyd. 

+-- {: .num_lemma}
###### Lemma 
For any category $C$ with a [[terminal object]] $\mathbf{1}$, the terminal object of the Freyd cover $\widehat{C}$ is [[small-projective]], i.e., the representable $\Gamma = \widehat{C}(1, -) \colon \widehat{C} \to Set$ preserves any colimits that exist. 
=-- 

+-- {: .proof} 
###### Proof 
To check that $\Gamma^{op} \colon \widehat{C}^{op} \to Set^{op}$ preserves limits, it suffices to check that the composite 

$$\widehat{C}^{op} \stackrel{\Gamma^{op}}{\to} Set^{op} \stackrel{2^-}{\to} Set$$ 

preserves limits, because the contravariant power set functor $P = 2^-$ is monadic. But it is easily checked that this composite is the contravariant representable given by $(2, \mathbf{1}, 2 \to \Gamma(\mathbf{1}))$. 
=-- 

+-- {: .num_theorem}
###### Theorem 
The terminal object in the initial topos $\mathcal{T}$ is [[connected object|connected]] and [[projective object|projective]] in the sense that $\Gamma = \hom(1, -) \colon \mathcal{T} \to Set$ preserves finite colimits. 
=-- 

+-- {: .proof} 
###### Proof 
We divide the argument into three segments: 

* The hom-functor preserves finite limits, so by general properties of Artin gluing, the Freyd cover $\widehat{\mathcal{T}}$ is also a topos. Observe that $\mathcal{T}$ is equivalent to the slice $\widehat{\mathcal{T}}/M$ where $M$ is the object $(\emptyset, \mathbf{1}, \emptyset \to \Gamma(\mathbf{1}))$. Since pulling back to a slice is a logical functor, we have a logical functor 
$$\pi \colon \widehat{\mathcal{T}} \to \mathcal{T}$$ 
Since $\mathcal{T}$ is initial, $\pi$ is a retraction for the unique logical functor $i \colon \mathcal{T} \to \widehat{\mathcal{T}}$. 

* We have maps $\mathcal{T}(1, -) \to \widehat{\mathcal{T}}(i 1, i-) \cong \widehat{\mathcal{T}}(1, i-)$ (the isomorphism comes from $i 1 \cong 1$, which is clear since $i$ is logical), and $\widehat{\mathcal{T}}(1, i-) \to \mathcal{T}(\pi 1, \pi i-) \cong \mathcal{T}(1, -)$ since $\pi$ is logical and retracts $i$. Their composite must be the identity on $\mathcal{T}(1, -)$, because there is only one such endomorphism, using the Yoneda lemma and terminality of $1$. 

Finally, since $\mathcal{T}(1, -)$ is a retract of a functor $\widehat{\mathcal{T}}(1, i-)$ that preserves finite colimits (by the lemma, and the fact that the logical functor $i$ preserves finite colimits), it must also preserve finite colimits. 
=--

This is important because it implies that the [[internal logic]] of the free topos (which is exactly "intuitionistic higher-order logic") satisfies the following properties:

* The *disjunction property*: if "P [[or]] Q" is provable in the empty [[context]], then either P is so provable, or Q is so provable.  (Note that this clearly fails in the presence of [[excluded middle]].)

* The *existence property*: if "there exists an $x\in A$ such that $P(x)$" is provable in the empty context, then there exists a [[global element]] $x\colon 1\to A$ such that $P(x)$ is provable in the empty context.  (Again, this is clearly a [[constructive mathematics|constructivity]] property.)

* The *negation property*: False is not provable in the empty context. 

* All numerals in the free topos are "standard", i.e., the global sections functor $\Gamma = \hom(1, -): \mathcal{T} \to Set$ preserves the [[natural numbers object]] $N$ (because $N$ can be characterized in terms of finite colimits and $1$, by a theorem of Freyd). 

### As a local topos
 {#AsALocalTopos}

The Freyd cover of a [[topos]] is a [[local topos]], and in fact freely so. Every local topos is a [[retract]] of a Freyd cover.

See ([Johnstone, lemma C3.6.4](#Johnstone)).

### As a fibration

The Freyd cover $\overline{\mathcal{T}}$ is fibered over $\mathcal{T}$ as it arises equivalently by change of base of the [[codomain fibration]] of [[Set]] along the [[global section functor]] $\Gamma$.

See ([Jacobs, p.57](#Jacobs)).
 
## Related entries

* [[Artin gluing]]

* [[comma category]]

* [[Sierpinski topos]]

## References

Some of the above material is taken from 

* [[Tom Leinster]], [reply at MathOverflow](http://mathoverflow.net/questions/12136/freyd-cover-of-a-category)

The following two n-caf&#233; blog posts provide an introductory discussion of the scone construction from a geometric and a logical perspective:

* [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ , November 2011. ([link](https://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))

* [[Mike Shulman]], _Scones, Logical Relations, and Parametricity_ , April 2013. ([link](https://golem.ph.utexas.edu/category/2013/04/scones_logical_relations_and_p.html))

You can find more on [[Artin gluing]] in this important (and nice) paper:

* [[Aurelio Carboni]], [[Peter Johnstone]], _Connected limits, familial representability and Artin glueing_ , Mathematical Structures in Computer Science **5** (1995) pp.441-459.

plus

* [[Aurelio Carboni]], [[Peter Johnstone]], _Corrigenda to 'Connected limits...'_ , Mathematical Structures in Computer Science **14** (2004) pp.185-187.

See also section C3.6 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. 2_ . Oxford UP 2002.
  {#Johnstone}

* [[Bart Jacobs]], _Categorical Logic and Type Theory_ , Elsevier Amsterdam 1999. {#Jacobs}

The following paper studies logical properties of the Freyd cover:

* [[Ieke Moerdijk]], _On the Freyd Cover of a Topos_ , Notre Dame J. Formal Logic **24** no.4 (1983) pp.517-526. ([pdf](http://projecteuclid.org/download/pdf_1/euclid.ndjfl/1093870454))

The argument given above for the properties of the free topos is an amplification of

* [[Peter Freyd|P. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990.  (1.(10)31, p.192)

For more on the free topos and the first appearance in print of Freyd's observation see

* [[Joachim Lambek|J. Lambek]], P. J. Scott, _Intuitionist Type Theory and the Free Topos_ , JPAA **19** (1980) pp.215-257.

[[!redirects scone]]
[[!redirects Sierpinski cone]]