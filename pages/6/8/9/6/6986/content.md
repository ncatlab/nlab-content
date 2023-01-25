
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc} 

## Idea

In [[type theory]] the _empty type_ is the [[type]] with no [[term]].

In a [[model]] by [[categorical semantics]], this is an [[initial object]]. In [[set theory]], it is an [[empty set]]. In [[logic]], especially via the [[propositions as types]] interpretation of type theory, it represents [[falsehood]]; and constructing a [[term]] of an empty type represents a [[contradiction]]; thus [[functions]] into the empty type are regarded as the [[negation]] of their [[domain]] [[proposition]]. 

## Definition

Like all [[type formation|type constructors]] in [[type theory]], to characterize the empty type we must specify how to build it, how to [[term introduction|construct elements]] of it, how to [[term elimination|use such elements]], and the [[computation rules]].

To start with, since the empty type is not [[dependent type|dependent]], its [[type formation]] rule just says that it exists:

$$\frac{ }{\emptyset\colon Type}$$

### As a positive type

The empty type is most naturally presented as a [[positive type]], so that the [[term introduction|constructor rules]] are primary.  However, since the empty type is supposed to contain no elements, there *are* no constructor rules.

The [[term elimination|eliminator rules]] are derived from the constructor rules in the usual way: to use a term $e \,\colon\, \varnothing$, it suffices to specify what should be done for all the ([[zero]]) ways that $e$ could have been constructed.  Thus, we don't need any hypotheses:

$$
  \frac{ }
  {
    e \,\colon\, \varnothing 
    \;\; \vdash \;\; 
    abort_C(e) \,\colon\, C
  }
$$

That is, given a [[term]] of $\varnothing$, we can construct a [[term]] of any [[type]] $C$.  

More generally, in [[dependent type theory]] the elimination rule involves any $\varnothing$-[[dependent type]]:

{#InferenceRules} The full positive [[inference rules]] for the [[empty type]] are as follows:


* **[[type formation rule]]:**

  $$
    \frac{
    }{
      \mathclap{\phantom{\vert^{\vert}}}
      \varnothing \,\colon\, Type
    }
  $$

\linebreak


* **[[term introduction rule]]:**

  $$
  \text{--- none ---}
  $$

\linebreak

* **[[term elimination rule]]:**

  $$
    \frac{
      x \,\colon\, \varnothing
      \;\vdash\;\;
      D(x) \,:\, Type
    }{
      \mathclap{\phantom{\vert^{\vert}}}
      ind_{(D)}
      \,\colon\,
      \underset{x \colon \varnothing}{\prod}
      D(x)
    }
  $$

\linebreak

* **[[computation rule]]:**

  $$
  \text{--- none ---}
  $$

In fact these are the rules of the *[[inductive type]]* given by *no constructors*. Therefore, in [[programming languages]] supporting a [[calculus of constructions]], such as *[[Coq]]*,  the empty type may be defined by the following [[syntax]] for [[inductive type|inductive]] [[data types]] using literally an [[empty set|empty]] [[string (computer science)|string]] of constructors on the right:

    Inductive empty : Type :=

\linebreak

Notice that there is no [[beta-reduction]] rule for the positive empty type, since there are no constructors to compose with the eliminator.  

However, one may consider an [[eta-conversion]] rule, which says that for any term $e \,\colon\, \varnothing \;\;\vdash\;\; c \,\colon\, C$ in a context including a term of type $\emptyset$, we have

$$ 
  abort_C(e) 
  \;\;\;
    \leftrightarrow_\eta 
  \;\;\; 
  c
  \,.
$$

As with the [[eta-conversion|$\eta$-conversion]] rule for the negative presentation of the [[unit type]], this is ill-defined as a *reduction* (since we cannot determine $c$ from $abort_C(e)$), but makes sense as an *expansion*.
   .
Notice that [[Coq]] implements the [[beta reduction]] rule, but not the [[eta conversion]] (although eta equivalence is provable for the inductively defined [[identity types]], using the dependent eliminator mentioned above).


### As a negative type

As for binary [[sum types]], it is possible to present the empty type as a [[negative type]] as well, but only if we allow [[sequents]] with multiple conclusions.  This is common in [[sequent calculus]] presentations of [[classical logic]], but not as common in type theory and almost unheard of in [[dependent type theory]].

The two definitions are provably equivalent, but only using the [[contraction rule]] and the [[weakening rule]].  Thus, in [[linear logic]] they become distinct; the positive empty type is "zero" $\mathbf{0}$ and the negative one is "bottom" $\bot$.


## Related concepts

[[!include empty objects -- contents]]

* [[falsehood]]

* [[sum type]]

* [[unit type]], [[contractible type]]

## References

* {#UFP13} [[Univalent Foundations Project]], §1.7 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Egbert Rijke]], Def. 4.3.1 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;


[[!redirects bottom type]]
[[!redirects bottom types]]

[[!redirects empty type]]
[[!redirects empty typpe]]
[[!redirects empty types]]
