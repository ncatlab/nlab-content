
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **Freyd category** is one way to axiomatize models of [[call-by-value]] [[programming languages]].
It abstracts the structure of the [[Kleisli category]] of a [[monad in computer science|monad]], consisting of a [[category]] $\mathbb{V}$ that models values and another category with the same [[objects]] $\mathbb{C}$ that models computations.

Freyd categories thus provide a [[categorical semantics]] for typed [[programming languages]] with [[side effects]] such as memory access or printing. This is in the spirit of the discussion at [[relation between type theory and category theory]], except that page is for non-side-effecting languages. The types of the programming language are interpreted as objects of the categories. A [[type|typed]] term (i.e., program expression) $\Gamma\vdash t \colon X$ is interpreted as a morphism $\Gamma \to X$ in $\mathbb{C}$. Among the terms, it is often very important to identify those that are "values", which in particular have no side effects, and these are interpreted as morphisms in $\mathbb{V}$. Freyd categories are based around premonoidal categories, which captures the fact that reordering the execution of side effects is often subtle. 

Freyd categories resolve the following complaint about using [[monads]] and [[Kleisli category|Kleisli categories]] to model impure effects in programming languages. The Kleisli category for a monad presumes the existence of some slightly higher-order types, since if $X$ is an object then so is $T(X)$, and yet it is surely possible to understand the nature of effectful computation without also assuming the existence of certain types. Freyd categories make sense even for purely first order programming languages, and the object $T(X)$, if it exists, has a universal property, thus decoupling this relationship. 

## Definition

A **Freyd category** (following [Levy 04](#Levy04)) may be defined as

* a [[category]] $\mathbb{V}$ with [[finite products]];
* a category $\mathbb{C}$, that has the same objects as $\mathbb{V}$[^sameObjs];
* an [[action]] of $\mathbb{V}$ on $\mathbb{C}$ (with the finite products providing a [[symmetric monoidal category|symmetric monoidal structure]] for $\mathbb{V}$)
* an [[identity-on-objects functor]] $J: \mathbb{V} \to \mathbb{C}$ that preserves the actions.

[^sameObjs]: Having the same objects is required or implied by having an identity-on-objects functor from $\mathbb{V}$ to $\mathbb{C}$.

An alternative but equivalent definition is as follows (following [Power, Thielecke](#PH99)):

A Freyd category is given by 

* a category $\mathbb{V}$ with finite products;
* a symmetric [[premonoidal category]] $\mathbb{C}$, that has the same objects as $\mathbb{V}$;
* an identity-on-objects functor $J: \mathbb{V} \to \mathbb{C}$ strictly preserving symmetric premonoidal structure, whose image lies in the centre of $\mathbb{C}$. 

## Properties

### Relation to strong monads. 

If $T$ is a [[strong monad]] on a category $\mathbb{V}$ with finite products, then the Kleisli category of $T$ forms a Freyd category and $J$ has a right adjoint. 

Conversely, if $(\mathbb{V},\mathbb{C},J)$ is a Freyd category and $J$ has a right adjoint $R$, then the Freyd category arises as the [[Kleisli category]] of the monad $RJ$.

In more detail, the passage from a strong monad to a Freyd category is as follows. If $T$ is a strong monad on a category $\mathbb{V}$ with finite products, then the Kleisli category $\mathbb{C}$ has a premonoidal structure given by $X\otimes Y=X\times Y$ on objects and where for a morphism $f:Y\to Z$ in $\mathbb{C}$ (i.e. $f:Y\to T(Z)$ in $\mathbb{V}$) then the right tensor $(X\rtimes f):X\otimes Y\to X\otimes Z$ is given by the composite
$X\times Y\xrightarrow f X\times T(Z) \xrightarrow {\mathrm{str}} T(X\times Z)$ in $\mathbb{V}$. The left tensor $(f\ltimes X):Y\otimes X\to Z\otimes X$ is given by the composite
$Y\times X\xrightarrow f T(Z)\times X \xrightarrow {\mathrm{str}} T(Z\times X)$ in $\mathbb{V}$. This is a premonoidal structure, and it is monoidal if and only if the monad $T$ is a [[commutative monad]]. 

### Relation to Lawvere theories and PROPs

To give a small Freyd category is to give an [[enriched Lawvere theory]] relative to the empty [[sound doctrine]] where the enriching category is [[cartesian closed category|cartesian closed]].

For example, if ($\mathrm{FinSet}^{\mathrm{op}}\to \mathbb{T}$) is an ordinary [[Lawvere theory]], then its dual ($\mathrm{FinSet}\to \mathbb{T}^{\mathrm{op}}$) is a Freyd category.  

The Lawvere theory is [[commutative algebraic theory|commutative]] if and only if the premonoidal category $\mathbb{T}^{\mathrm{op}}$ is in fact monoidal. 

A minor generalization of Freyd category allows $\mathbb{V}$ to be symmetric monoidal rather than cartesian monoidal. Then a commutative Freyd category
$\mathrm{FinSet}_{\mathrm{bij}}\to \mathbb{C}$ is the same thing as a [[PROP]]. 

### Relation to monads on presheaf categories

This relates to the situation with monads as follows. If $T$ is a strong monad on the [[presheaf]] category $\hat{\mathbb{V}}$ then the 
Kleisli category $\hat{\mathbb{V}}\to (\hat{\mathbb{V}})^T$ is a Freyd category. 
But also the identity-on-objects/full-and-faithful factorization of the composite $\mathbb{V}\to \hat{\mathbb{V}}\to (\hat{\mathbb{V}})^T$
yields a Freyd category over $\mathbb{V}$. 

Every Freyd category arises in this way, giving a correspondence between colimit-preserving strong monads on $\hat{\mathbb{V}}$ and Freyd categories over a category $\mathbb{V}$ with products. 

On the other hand, a colimit-preserving monad on $\hat{\mathbb{V}}$ is the [same thing as](profunctor#FuncsOnPresheaves) a monad in the category of profunctors whose carrier is $\mathbb{V}$. But this is the [same thing as](https://ncatlab.org/nlab/show/monad#other_examples) an identity on objects functor $\mathbb{V}\to\mathbb{C}$. And this is a Freyd category if and only if the monad is strong.

## Related Concepts

* [[monad in computer science]]
* [[Kleisli category]]
* [[thunk-force category]]

## References

Freyd categories were first used in

* [[John Power]] and Hayo Thielecke "Environments, Continuation Semantics and&#160;Indexed Categories",  Theoretical Aspects of Computer Software, Third International Symposium, TACS '97

and named Freyd categories in

* {#PH99} John Power and Hayo Thielecke, "Closed Freyd- and $\kappa$-Categories", Automata, Languages and Programming, 26th International Colloquium, ICALP'99

and the longer journal version of that paper has more discussion:

* Paul Blain Levy, John Power and Hayo Thielecke, "Modelling environments in call-by-value programming languages",  Inf. Comput. 185(2): 182-210, 2003 [preprint pdf](https://www.cs.bham.ac.uk/~hxt/research/envcbv.pdf).

The definition with monoidal actions appears in 

* {#Levy04} Paul Blain Levy, "Call-by-Push-Value. A Functional/Imperative Synthesis," Semantic Structures in Computation 2, Springer, 2004; appendix B* 

The idea of extending Freyd categories to monads on presheaf categories appears in

* [[John Power]], "Generic models for computational effects",  Theor. Comput. Sci. 364(2): 254-269 (2006)

This also contains the observation that enriched Lawvere theories are examples of Freyd categories, but the precise correspondence between the concepts is given in

* {#Staton14} [[Sam Staton]], 2014. *Freyd categories are Enriched Lawvere Theories*. Electronic Notes in Theoretical Computer Science, Proceedings of the Workshop on Algebra, Coalgebra and Topology (WACT 2013) 303, 197&#8211;206. [doi:10.1016/j.entcs.2014.02.010](https://doi.org/10.1016/j.entcs.2014.02.010) (free). 

The connection with monads in the category of profunctors is discussed in

* [[Bart Jacobs]], [[Chris Heunen]], Ichiro Hasuo, "Categorical semantics for arrows". J. Funct. Program. 19(3-4): 403-438. 2009.
[preprint pdf](http://homepages.inf.ed.ac.uk/cheunen/publications/2008/arrows/arrows.pdf)

and 

* Kazuyuki Asada. "Arrows are strong monads". Proceedings of MSFP '10. [preprint pdf](http://www-kb.is.s.u-tokyo.ac.jp/~asada/papers/arrStrMnd.pdf)

[[!redirects Freyd categories]]
[[!redirects Freyd-categories]]
[[!redirects Freyd-category]]


