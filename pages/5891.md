[[!redirects functorial perspective]]
[[!redirects functorial semantics]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One may interpret mathematical _[[logic]]_ as being a formal language for talking about the collection of [[monomorphisms]] into a given [[object]] of a given [[category]]: the [[poset of subobjects]] of that object.

More generally, one may interpret [[type theory]] and notably [[dependent type theory]] as being a formal language for talking about [[slice categories]], consisting of all morphisms into a given object. 

Conversely, starting with a given theory of logic or a given type theory, we say that it has a _categorical semantics_ if there is a category such that the given theory is that of its slice categories, if it is the _[[internal logic]]_ of that category.



## Definition

For the general idea, for the moment see at _[[type theory]]_ the section _[An introduction for category theorists](type+theory#CategoricalSemantics)_ and see at _[[relation between type theory and category theory]]_.

### Of dependent type theory

We discuss how to interpret judgements of [[dependent type theory]] in a given [[category]] $\mathcal{C}$ with [[finite limits]]. For more see _[[categorical model of dependent types]]_.

Write $cod : \mathcal{C}^I \to \mathcal{C}$ for its [[codomain fibration]], and write 

$$
  \chi : \mathcal{C}^{op} \to Cat
$$ 

for the corresponding [[Grothendieck construction|classifying functor]], the self-[[indexed category|indexing]]

$$
  \chi : \Gamma \mapsto \mathcal{C}_{/\Gamma}
$$ 

that sends an [[object]] of $\mathcal{C}$ to the [[slice category]] over it, and sends a morphism $f : \Gamma \to \Gamma'$ to the [[pullback]]/[[base change]] functor 

$$
  f^\ast : \mathcal{C}_{/\Gamma'} 
  \to 
  \mathcal{C}_{/\Gamma}
  \,.
$$

We give now rules for choices "$[x y z]$" that associate with every string "$x y z$" of symbols in [[type theory]] objects and morphisms in $\mathcal{C}$. A collection of such choices following these rules is _an interpretation_ / a choice of _categorical semantics_ of the type theory in the category $\mathcal{C}$.

#### Contexts and type judgements
 {#ContextsAndTypeJudgements}

1. The empty [[context]] $()$ in [[type theory]] is interpreted as the [[terminal object]] of $\mathcal{C}$

   $$
     [ () ] := *
     \,.
   $$

1. If $\Gamma$ is a context which has already been given an interpretation $[\Gamma] \in Obj(\mathcal{C})$, then a judgement of the form

   $$
     \Gamma \vdash A : Type
   $$

   is interpreted as an object in the slice over $\Gamma$

   $$
     [\Gamma \vdash A : Type] \in Obj(\mathcal{C}_{/\Gamma})
     \,,
   $$

   hence as a choice of morphism

   $$   
     \array{
       [(\Gamma, x : A)]
       \\
       \downarrow^{\mathrlap{[\Gamma \vdash A : Type]}}
       \\
       [\Gamma]
     }
   $$

   in $\mathcal{C}$.

1. If a judgement of the form $\Gamma \vdash A : Type$ has already found an interpretation, as above, then an extended [[context]] of the form $(\Gamma, x : A)$ is interpreted as the domain object $[(\Gamma, x : A)]$ of the above choice of morphism.

 

#### Terms

Assume for a context $\Gamma$ and a judgement $\Gamma \vdash A : Type$ we have already chosen an interpretation  $[\Gamma, x : A] \stackrel{[\Gamma \vdash A : Type]}{\to} [\Gamma]$ as above.

A judgement of the form $\Gamma \vdash a : A$ (a [[term]] of [[type]] $A$) is to be interpreted as a [[section]] of this morphism, equivalently as a morphism in $\mathcal{C}_{/\Gamma}$ 

$$   
  [\Gamma \vdash : a : A] : * \to [\Gamma, x : A]
$$

from the [[terminal object]] to $[\Gamma \vdash A : Type]$, which in $\mathcal{C}$ is a [[commuting diagram|commuting triangle]]

$$
  \array{
    [\Gamma] &&\stackrel{[(\Gamma \vdash a : A)]}{\to}&&
    [\Gamma, x : A]
    \\
    & {}_\mathllap{[\Gamma]}\searrow
    &&
    \swarrow_{\mathrlap{[\Gamma \vdash A : Type]}}
    \\
    && [\Gamma]
  }
  \,.
$$

#### Variables

For a term $\Gamma \vdash  a : A$ the context $\Gamma$ is the collection of [[free variables]] in $a$. 

(...)


#### Substitution 

Assume that interpretations for judgements 

$$
  \Gamma , x : A \vdash B(x) : Type
$$

and

$$
  \Gamma \vdash  a : A
$$

have been given as above. Then the substitution judgement

$$
  \Gamma  \vdash B[a/x] : Type
$$

is to be interpreted as follows. The interpretation of the first two terms corresponds to a diagram in $\mathcal{C}$ of the form

$$
  \array{
    &&&& [(\Gamma, x : A, y : B(x))]
    \\
    &&&&
    \downarrow^{\mathrlap{[\Gamma, x : A \vdash B(x) : Type]}}
    \\
    [\Gamma] &&\stackrel{[\Gamma \vdash a : A]}{\to}&&
     [(\Gamma, x : A)]
    \\
    & {}_{id}\searrow && \swarrow_{\mathrlap{[\Gamma \vdash A : Type]}}
    \\
    && [\Gamma]
  }
$$

The interpretation of the substitution statement is then [[generalized the|the]] [[pullback]]

$$
  [\Gamma \vdash B[a/x] : Type]
  :=
  [\Gamma \vdash a : A]^* [\Gamma, x : A \vdash B(x) : Type]
  \,,
$$

hence the morphism in $\mathcal{C}$ that universally completes the above diagram as

$$
  \array{
    [(\Gamma, y : B[x/a])]
    &&\to&& [(\Gamma, x : A, y : B(x))]
    \\
    {}^{\mathllap{[\Gamma \vdash B[a/x] : Type]
}}\downarrow
    &&&&
    \downarrow^{\mathrlap{[\Gamma, x : A \vdash B(x) : Type]}}
    \\
    [\Gamma] &&\stackrel{[\Gamma \vdash a : A]}{\to}&&
     [(\Gamma, x : A)]
    \\
    & {}_{id}\searrow && \swarrow_{\mathrlap{[\Gamma \vdash A : Type]}}
    \\
    && [\Gamma]
  }
$$

### Of homotopy type theory

See _[[categorical semantics of homotopy type theory]]_.

## Examples

* [[models in presheaf toposes]]

## Terminology
 {#Terminology}

Most usage in [[mathematics]] of the adjective "categorical" in relation to [[category theory]] is a shorthand, and arguably an unfortunate one, for "category theoretic", i.e. for  "as seen through the lens of, hence as treated with the concepts and tools of category theory". 

Compare to "numerical" versus "number theoretic": The interest of number theory is not in numerical methods! Numerical statements are made by engineers. For category theorists it's worse: Their profession is not to do _categorical arguments_, not in the dictionary sense of "categorical" as "unambiguous, absolute, unqualified". 

While the careful dictionaries list a secondary sense of "categorical", as "relating to a category", they hardly have the categories of Kant in mind here, much less those of Eilenberg & MacLane; instead they refer to _catagegorization_: Merriam-Webster [offers](https://www.merriam-webster.com/dictionary/categorical) "categorical systems for classifying books" as an example for what "categorical" could refer to, in this secondary sense, in common language. Therefore it does not seem to help much that this secondary common sense of "categorical"  is [offered](https://www.merriam-webster.com/dictionary/categorial) as the primary sense of "categorial" (without the second "c"!). But this is probably the rationale behind a more widespread use of "categorial semantics" over "categorical semantics" in the field of formal logic.

All this notwithstanding, the use in mathematics of "categorical", as in _[[categorical semantics]]_ is wide-spread, even standard. Since unfortunate choice of terminology in mathematics is rather common (compare "perverse schobers"!), and since the primary purpose of mathematical terminology is communication rather than, yes, proper categorization, there may not be much gain in opposing this trend, and not much success to doing so by replacing unfortunate terminology with something that looks like the same unfortunate terminology but with a typo in it.




## Related pages

* [[relation between type theory and category theory]]

* [[categorical model of dependent types]]

* [[initiality conjecture]]

* [[Awodey's conjecture]]




## References

A standard textbook reference for categorical semantics of logic is section D1.2 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


The categorical semantics of [[dependent type theory]] in [[locally cartesian closed categories]] is essentially due to

* [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))
  {#Seely}

For more references on this see at _[[relation between category theory and type theory]]_.

Lecture notes on this include for instance.

* [[Martin Hofmann]], _Syntax and semantics of dependent types_, Semantics and Logics of Computation (P. Dybjer and A. M. Pitts, eds.), Publications of the Newton Institute, Cambridge University Press, Cambridge, (1997) pp. 79-130. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985), )

* Roy Crole, _Categories for types_

See also section B.3 of 

* [[Michael Warren]], _Homotopy Theoretic Aspects of Constructive Type Theory_ ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))

A comprehensive definition of semantics of [[homotopy type theory]] in [[type-theoretic model categories]] is in section 2 of 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))

