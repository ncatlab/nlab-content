
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

In [[constructive mathematics]], a [[set]] $X$ has __decidable equality__ if any two elements of $X$ are either [[equality|equal]] or [[negation|not]] equal.  Equivalently, $X$ has decidable equality if its [[equality]] [[relation]] is a [[decidable subset]] of $X \times X$.  Sometimes one says that such a set $X$ is _discrete_, although of course this term has many meanings.  Of course, in [[classical mathematics]], every set has decidable equality.  But the concept generalises in [[sheaf and topos theory|topos theory]] to the notion of [[decidable object]].

## Examples

* Every [[finite set]] has decidable equality. 

* Every [[subfinite set]] has decidable equality, since finite sets have decidable equality and the canonical [[injection]] of a subfinite set into a finite set preserves and reflects both equality and the negation of equality by definition of injection. 

* The [[natural numbers]] have decidable equality. 

* Every [[countable set]] (a set that admits a [[bijection]] with a [[lower set|lower]] [[decidable subset]] of $\mathbb{N}$) has [[decidable equality]]. 

* Every [[subcountable set]] has decidable equality, since the natural numbers have decidable equality and the canonical [[injection]] of a subcountable set into the natural numbers preserves and reflects both equality and the negation of equality by definition of injection. 

* More generally, every [[subset]] of a set with [[decidable equality]] itself has decidable equality. 

There are other examples if we assume some principles which are not [[neutral constructive mathematics|neutrally constructive]]:

* [[Cantor space]] has decidable equality if and only if the [[weak limited principle of omniscience]] holds

* The [[Dedekind real numbers]] has decidable equality if and only if [[analytic WLPO]] holds

+--{: .un_remark}
###### Remark
These last two examples are examples of sets with [[decidable equality]] in constructive mathematics, but where the negation of equality is still not an [[apartness relation]], and so sets with decidable equality still do not behave as they do in [[classical mathematics]]. 

Assuming that [[Cantor space]] has decidable equality, negation of equality only becomes an apartness relation if and only if the [[limited principle of omniscience]] holds. Similarly, assuming that the [[Dedekind real numbers]] has decidable equality, negation of equality only becomes an apartness relation if and only if the [[analytic LPO]] holds. 

See [[decidable tight apartness]] for the stronger condition where the sets do actually behave as they do in [[classical mathematics]]. 
=--

Some non-examples include:

* Not all [[countably indexed sets]] necessarily have [[decidable equality]], where countably indexed means that the set admits a surjection from a decidable subset of the [[natural numbers]]. [BauerHanson24](#BauerHanson24) constructed a [[topos]] in which the [[Dedekind real numbers]] do not have [[decidable equality]] but which are still countably indexed; note that the authors used "countable" to mean countably indexed. 

* [[Cantor space]] does not have decidable equality if [[Brouwer's continuity principle]] for [[Cantor space]] holds

* The [[Dedekind real numbers]] does not have decidable equality if [[Brouwer's continuity principle]] for the [[Dedekind real numbers]] holds

## In type theory

In [[type theory|type-theoretic]] foundations, there are two different notions of decidable equality, depending on whether "or" is interpreted using [[sum types]] $\prod_{x,y\colon A} (x=y) + \neg (x=y)$ or [[disjunctions]] $\prod_{x,y\colon A} (x=y) \vee \neg (x=y)$, i.e. the [[bracket type]] of [[sum types]]. The former notion of decidable equality is called **untruncated decidable equality**, while the latter notion is called **truncated decidable equality**. Since every type maps to its bracket, untruncated decidable equality implies truncated decidable equality.

On the other hand, if truncated decidable equality holds and $A$ is an [[h-set]], i.e. it satisfies [[uniqueness of identity proofs]], then $(x=y)$ and $\neg (x=y)$ represent disjoint subobjects of $A\times A$.  Thus $(x=y) + \neg (x=y)$ is already a subobject of $A\times A$, so it is equivalent to its bracket, and untruncated decidable equality also holds.

The converse of this is also true: if untruncated decidable equality holds, then not only does truncated decidable equality also hold, but in fact $A$ is an h-set. This was first proven by Michael Hedberg; a proof can be found at [[Hedberg's theorem]] and in the references below. This fact is useful in [[homotopy type theory]] to show that many familiar types, such as the [[natural numbers]], are h-sets.

For non-h-sets, the difference between untruncated decidable equality and truncated decidable equality can be dramatic. For instance, if we model homotopy type theory in a [[Boolean topos|Boolean]] $(\infty,1)$-topos (such as $\infty Gpd$ constructed classically), then *every* type satisfies truncated decidable equality (which is what it means for the logic to be boolean), but only the h-sets satisfy untruncated decidable equality (in accordance with Hedberg\'s theorem).

### Using the type of booleans

There is also a few definitions of decidable equality in [[dependent type theory]], which rely on the [[type of booleans]] with its extensionality principle and the fact that that the decidable equality is always valued in the [[type of booleans]]. 

The first definition states that decidable equality on a type $A$ is a [[binary function]] $\mathrm{Eq}_A:A \times A \to \mathrm{Bit}$ which comes with a family of equivalences
$$x:A, y:A \vdash \delta(x, y):\mathrm{Id}_A(x, y) \simeq \mathrm{Id}_\mathbb{2}(\mathrm{Eq}_A(x, y), 1)$$

The second also relies on the fact that the [[type of booleans]] forms a [[univalent Tarski universe]] $(\mathrm{Bit}, \mathrm{El}_\mathrm{Bit})$. Here, decidable equality on a type $A$ is a [[binary function]] $\mathrm{Eq}_A:A \times A \to \mathrm{Bit}$ which comes with a family of equivalences 
$$x:A, y:A \vdash \delta(x, y):\mathrm{El}_\mathrm{Bit}(\mathrm{Eq}_A(x, y)) \simeq (x =_A y)$$

Either way, this is typically how the [[natural numbers type]] is proven to have decidable equality, by defining a binary function into the type of booleans called [[observational equality]] and using the extensionality principle of the natural numbers. 

### Properties

Every set with decidable equality is [[locally finite type|locally finite]]. 

## Related concepts

* [[decidability]]
* [[stable equality]]
* [[locally finite type]]
* [[classical set]]

## References

* Michael Hedberg, *A coherence theorem for Martin-L&#246;f's type theory*, J. Functional Programming, 1998

* Nicolai Kraus, *A direct proof of Hedberg's theorem*, [blog post](http://homotopytypetheory.org/2012/03/30/a-direct-proof-of-hedbergs-theorem/)

* {#BauerHanson24} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

[[!redirects decidable set]]
[[!redirects decidable sets]]

[[!redirects decidable equality]]
[[!redirects truncated decidable equality]]
[[!redirects untruncated decidable equality]]