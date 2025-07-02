
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


# W-types
* table of contents
{: toc}


## Idea
 {#Idea}

In [[type theory]], by a *$\mathcal{W}$-type* &lbrack;[Martin-Löf (1982), pp. 171](#Martin-Löf82), [(1984)](#Martin-Löf84), [pp. 43](https://ncatlab.org/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=49)&rbrack; one means a [[type]] which is defined [[induction|inductively]] in a *[[well-founded relation|$\mathcal{W}$ell-founded]]* way based on a type $C$ of "*c*onstructors" and a type of $A$ of "*a*rities". As such, $\mathcal{W}$-types are special kinds of [[inductive types]] (see [below](#WTypesInTypeTheory)).

The same terminology "$\mathcal{W}$-type" is used &lbrack;[Moerdijk & Palmgren (2000)](MoerdijkPalmgren00)&rbrack; for [[objects]] in (suitable [[pretopos|pre]]-)[[toposes]] which provide [[categorical semantics]] for the type-theoretic notion (see [further below](#WTypesInCategories)).

Concretely, the [[terms]]/[[elements]] of a $\mathcal{W}$-type may be thought of as "rooted well-founded [[trees]]" with a certain branching type; different $\mathcal{W}$-types are distinguished by their branching signatures: In [[categorical semantics]] in [[Sets]], a branching signature is represented by a [[family of sets]] $\{A_c\}_{c \in C}$ such that

* each *node* of the tree is labeled with an element $c \colon C$ -- referring to a *constructor*;

* if a node is labeled by $c$ then it has exactly ${|A_c|}$ outgoing edges, each labeled by some $a \colon A_c$ -- the *arity* of the constructor $c$.  

If one discards the requirement that the trees be well-founded, then the notion of $\mathcal{W}$-type becomes that of a [[coinductive type]] called an *[[M-type]]* (presumably since "M" is like a "W" upside down).

In practice, $\mathcal{W}$-types are used to:

1. provide a [[constructive mathematics|constructive]] counterpart of the [[classical logic|classical]] notion of a [[well-ordering]] 

1. uniformly define a variety of well-behaved [[inductive types]]. 

More complex [[inductive types]], with multiple constructors that are assumed only to be strictly [[positive type|positive]], can be reduced to $\mathcal{W}$-types, at least in the presence of other structure such as [[sum types]] and [[function extensionality]]; see for instance [Abbott, Altenkirch & Ghani (2004)](#AbbottAltenkirchGhani04). This can even be extended to [[inductive families]].

{#InMost} In most [[set theory|set theoretic]] [[mathematical foundations]], $\mathcal{W}$-types can be proven to exist, but in [[predicative mathematics]] and in [[type theory]], where this is not the case, they are often introduced [[axiom|axiomatically]] (as usual for [[inductive types]] more generally). 



## Definition
 {#Definition}

There are two slightly different formulations of W-types:

1. [$\mathcal{W}$-types in type theory](#WTypesInTypeTheory)

1. [$\mathcal{W}$-types in categories](#WTypesInCategories)





### $\mathcal{W}$-types in type theory
 {#WTypesInTypeTheory}

\begin{definition}\label{WTypeInferenceRules}
**([[inference rules]] for $\mathcal{W}$-types)**
\linebreak

(1) **[[type formation rule]]:**

$$
  \frac
    { 
      C \,\colon\, Type
      \;; 
      \;\;\;
      c \,\colon\, C
      \;\;\vdash\;\; 
      A(c) \,\colon\,Type
      \mathclap{\phantom{\vert_{\vert}}}
    }
    {
      \mathclap{\phantom{\vert^{\vert}}}
      \underset{c \colon C}{\mathcal{W}}\, A(c) 
        \,\colon\, 
      Type 
    }
$$

(2) **[[term introduction rule]]:**

$$
  \frac{
    \vdash\; root \,\colon\, C
    \;;
    \;\; 
    subtr 
      \,\colon\, 
    A(root) \to \underset{c \colon C}{\mathcal{W}}\, A(c)
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    tree\big(root ,\, subtr\big) 
      \,\colon\, 
    \underset{c \colon C}{\mathcal{W}}\, A(c)
  }
$$

(3) **[[term elimination rule]]:**

$$
  \frac{
    \begin{array}{l}
      t \,\colon\, \underset{c \colon C}{\mathcal{W}}\, A(c)
      \;\vdash\; 
      D(t) \,\colon\, Type
      \;;
      \\
      root \,\colon\, C
      \,,
      \; 
      subt
        \,\colon\, 
      A(root) \to \underset{c \colon C}{\mathcal{W}}\, A(c)
      \,, 
      \;
      subt_D 
        \,\colon\, 
      \underset{a \colon A(root)}{\prod} 
        D\big(subt(a)\big)
      \\
      \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
      \;\;\vdash\;\;
      tree_D\big(root,\,subt ,\, subt_D\big) 
        \,\colon\, 
      D\big(tree(root,\, subt)\big)
      \mathclap{\phantom{\vert_{\vert}}}
    \end{array}  
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    t
      \,\colon\, 
    \underset{c \colon C}{\mathcal{W}}\, A(c) 
    \;\vdash\; 
    wrec_{(D,tree_D)}(t) \,\colon\, D(t)
  }
$$

(4) **[[computation rule]]:**

$$
  \frac{
    \begin{array}{l}
      t
        \,\colon\, 
      \underset{c \colon C}{\mathcal{W}}\, A(c)
      \;\vdash\; 
      D(t) \,\colon\, Type
      \;;
      \\
      root \,\colon\, C
      \,,\; 
      subt
        \,\colon\, 
      A(root) \to \underset{c \colon C}{\mathcal{W}}\, A(c)
      \,,
      \; 
      subt_D
        \,\colon\, 
      \underset{a\colon A(c)}{\Pi} D\big(subt(a)\big)
      \\
      \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
      \;\;\vdash\;\;
      tree_D\big(root,\,subt,\,subt_D\big) 
        \,\colon\, 
      D\big(tree(root,\, subt)\big)
      \mathclap{\phantom{\vert_{\vert}}}
    \end{array}
  }{
    \begin{array}{l}
    \mathclap{\phantom{\vert^{\vert}}}
    root \,\colon\, C
    \,,
    \;\; 
    subtr
      \,\colon\, 
    A(root) \to \underset{c \colon C}{\mathcal{W}}\, A(c)
    \\
    \;\;\;\;\;\;\;\;\;\;\;
    \;\;\vdash\;\; 
    wrec_{(D,tree_D)}\big( tree(root, \, subtr) \big)
    \;=\;
    tree_D
    \Big(
      root
      ,\, 
      subtr
      ,\,
      \lambda a . wrec_{(D,tree_D)}\big(subtr(a)\big)
    \Big)
    \end{array}
  }
$$

\end{definition}

(due to [Martin-Löf (1984)](#Martin-Löf84), [pp. 43](https://ncatlab.org/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=49); streamlined review e.g. in [Awodey, Gambino & Sojakova (2012, §2)](#AwodeyGambinoSojakova12))


\begin{remark}
 If the type theory is *[[extensional type theory|extensional]]*, i.e. [[identity type|identities]] have unique proofs and (dependent) [[function types]] are [[function extensionality|extensional]] ($f=g$ if and only if $f(x)=g(x)$ for all $x$), then this is more or less equivalent to the [[1-category]]-[[category theory|theoretic]]  definition [below](#WTypesInCategories). The type theories that are the [[internal logic]] of familiar kinds of categories are all extensional in this sense.

The main distinction from the naive categorical theory below is that the map $f$ (eq:TheDisplayMap) must be assumed to be a [[display map]], i.e. to exhibit $A$ as a [[dependent type]] over $C$, in order that the dependent product $\Pi_f$ be defined.

In the case of dependent polynomial functors, it seems that $q$ must also be a display map, in order to define $\Sigma_q$.  However, using [[adjunction|adjointness]], one can still define the W-type even if $q$ is not a display map.  This more general version is what in type theory is called an *indexed W-type*; if $q$ is a display map then one sometimes refers to *non-uniform parameters* instead of *indices*.  (By contrast, *uniform parameters* are the kind discussed above where $g f = h$, so that the entire construction takes place in a single slice category  This is an instance of the [[red herring principle]], since non-uniform parameters are not really parameters at all, but a special kind of indices.)  For example, [[identity type]]s are indexed W-types but not parametrized ones (even non-uniformly); see [this blog post](http://homotopytypetheory.org/2011/04/18/whats-special-about-identity-types/).)

\end{remark}

\begin{remark} In [[intensional type theory]], a $\mathcal{W}$-type is only an initial algebra with respect to [[propositional equality]], not [[definitional equality]].  In particular, the constructors are injective only propositionally, not definitionally.  This applies already for the [[natural numbers type]] (Exp. \ref{NaturalNumbersAsWType}).

\end{remark}











### $\mathcal{W}$-types in categories
 {#WTypesInCategories}

#### Plain version

We discuss the [[categorical semantics]] of $\mathcal{W}$-types, due to [Moerdijk & Palmgren (2000)](#MoerdijkPalmgren00).

Here one describes a $\mathcal{W}$-type as an [[initial algebra|initial]] [[algebra for an endofunctor]] on an ambient category $\mathcal{C}$. The family $\{A_c\}_{c\in C}$ can be thought of as a [[morphism]] 

\[
  \label{TheDisplayMap}
  \array{
    A
    \\
    \big\downarrow\mathrlap{^{f}}
    \\ 
    C
  }
\]


in some [[category]] $\mathcal{C}$ (such that the [[fiber]] over $c\in C$ is $A_c$), and the [[endofunctor]] in question is the [[composition|composite]]

$$ 
  \mathcal{C} 
    \overset{A^*}{\longrightarrow} 
  \mathcal{C}_{/A} 
    \overset{\Pi_f}{\longrightarrow} 
  \mathcal{C}_{/C} 
    \overset{\Sigma_C}{\longrightarrow} 
  \mathcal{C}
  \,,
$$

where 

* $A^*$ denotes [[context extension]], hence the [[pullback]] functor (a.k.a. $A\times -$);

* $\Pi_f$ denotes the interpretation of the [[dependent product]], i.e. the right [[base change]] along $f$; 


* $\Sigma_C$ the denotes the interpretation of the [[dependent sum]], i.e. the left [[base change]] given by the  [[forgetful functor]] from $\mathcal{C}_{/C}$ to $\mathcal{C}$.  

Equivalently, it is the composite

$$
  \mathcal{C}
    \overset{C^*}{\longrightarrow}
  \mathcal{C}_{/C}
    \overset{\bigcirc_f}{\longrightarrow}
  \mathcal{C}_{/C}
    \overset{\Sigma_C}{\longrightarrow}
  \mathcal{C}
  \,,
$$

where $\bigcirc_f$ is the [[reader monad]] $\Pi_f \circ f^*$. In other words, the dependent product is not actually dependent.

Such a composite is called a _[[polynomial endofunctor]]_. Explicitly, it is the functor $X \mapsto \sum_{c : C} X^{A_c}$.

This definition makes sense in any [[locally cartesian closed category]], although the W-type (the initial algebra) may or may not exist in any given such category.  (A non-elementary construction of them is given by the [[transfinite construction of free algebras]].)

The above definition is most useful when the category $\mathcal{C}$ is not just 
[[locally cartesian closed category|locally cartesian closed]] but is a [[Π-pretopos]], since often we want to use at least [[coproducts]] in constructing $A$ and $C$.  For example, a [[natural numbers object]] (Exp. \ref{NaturalNumbersAsWType}) is a $\mathcal{W}$-type specified by one of the coproduct inclusions $1\to 1+1$, and the [[list object]] $L X$ is a $\mathcal{W}$-type specified by $X\to X+1$.  More generally, endofunctors that look like [[polynomials]] in the traditional sense:
$$ 
F(Y) = A_n \times Y^{\times n}  + \dots + A_1 \times Y  + A_0 
$$
can be constructed as [[polynomial endofunctors]] in the above sense for any [[lextensive category]], and hence in any $\Pi$-pretopos.  A $\Pi$-pretopos in which all W-types exist is called a **[[ΠW-pretopos]]**.

In a [[topos]] with a [[natural numbers object]] (NNO), W-types for any polynomial endofunctor can be constructed as certain sets of well-founded trees; thus every topos with a NNO is a [[ΠW-pretopos]].  This applies in particular in the topos [[Set]] (unless one is a [[predicative mathematics|predicativist]], in which case $Set$ is not a topos and W-types in it must be postulated explicitly).


#### Dependent $\mathcal{W}$-types
 {#DependentWTypesCategoricalSemantics}

The above has a natural generalization to [[dependent type|dependent]] or *indexed* W-types ([Gambino & Hyland (2004)](#GambinoHyland04)) with a type $C$ of *indices*: 

given a [[diagram]] of the form

$$
  \array{
    A &\stackrel{f}{\longrightarrow}& B
    \\
    \downarrow^{\mathrlap{h}} && \downarrow^{\mathrlap{g}}
    \\
    C && C
  }
$$

there is the _[[dependent polynomial functor]]_

$$ 
  \mathcal{C}_{/C} \overset{h^\ast}{\longrightarrow} 
  \mathcal{C}_{/A} 
    \overset{\Pi_f}{\longrightarrow} 
  \mathcal{C}_{/B} 
    \overset{\Sigma_g}{\longrightarrow} 
  \mathcal{C}_{/C}
  \,,
$$

This reduces to the above for $C = \ast$ the [[terminal object]].

Notice that we do not necessarily have $g f = h$, so this is not just a [[polynomial endofunctor]] of $\mathcal{C}/_{C}$ considered as a lccc in its own right.  If we *do* have $g f = h$, then $C$ is called a type of *parameters* instead of indices.


## Examples

\begin{example}\label{NaturalNumbersAsWType}
**([[natural numbers type]] as a [[W-type|$\mathcal{W}$-type]])**
\linebreak
The [[natural numbers type]] $(\mathbb{N},\, 0,\, succ)$ is equivalently the [[W-type|$\mathcal{W}$-type]] (Def. \ref{WTypeInferenceRules}) with

* $C \,\coloneqq\, \{0, succ\} \,\simeq\, \ast \sqcup \ast$;

* $A_0 \,\coloneqq\, \varnothing$ ([[empty type]]);

  $A_{succ} \,\coloneqq\, \ast$ ([[unit type]])

\end{example}
&lbrack;[Martin-Löf (1984)](#Martin-Löf84), [pp. 45](/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=51), [Dybjer (1997, p. 330, 333)](#Dybjer97)&rbrack;


## Properties
 {#Properties}

\begin{proposition}
**([Danielsson (2012)](#Danielsson12))**
\linebreak
In [[homotopy type theory]], if $C$ has [[h-level]] $n\geq -1$, then any $\mathcal{W}$-type of the form $\underset{C}{\mathcal{W}} B$ has h-level $n$ (as it should be for [[(infinity,1)-colimits|$\infty$-colimits]]). 
\end{proposition}

## Related concepts

* [[M-type]]

* [[predicative topos]]

[[!include notions of type]]


## References

### General

The original definition in [[type theory]] is due to

* {#Martin-Löf82} [[Per Martin-Löf]], pp. 171 of: *Constructive Mathematics and Computer Programming*, in: *Proceedings of the Sixth International Congress of Logic, Methodology and Philosophy of Science (1979)*, Studies in Logic and the Foundations of Mathematics **104** (1982) 153-175 $[$<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>, [ISBN:978-0-444-85423-0](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/104/suppl/C)$]$


* {#Martin-Löf84} [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), [pp. 43](https://ncatlab.org/nlab/files/MartinLofIntuitionisticTypeTheory.pdf#page=49) of: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;
 

In [[homotopy type theory]]:

* [[Jasper Hugunin]], *Why Not W?*, Leibniz International Proceedings in Informatics (LIPIcs) **188** (2021) &lbrack;[doi:10.4230/LIPIcs.TYPES.2020.8](https://doi.org/10.4230/LIPIcs.TYPES.2020.8), [pdf](https://jashug.github.io/papers/whynotw.pdf)&rbrack; 

On the [[h-level]] of W-types:

* {#Danielsson12} Nils Anders Danielsson, _Positive h-levels are closed under W_ (2012) &lbrack;[web](https://homotopytypetheory.org/2012/09/21/positive-h-levels-are-closed-under-w/)&rbrack;

* [[Jasper Hugunin]], _IWTypes_, <https://github.com/jashug/IWTypes>

which also computes the [[identity types]] of W-types (and more generally [[indexed W-types]]).
 
W-types in [[Coq]]: [wiki](https://coq.inria.fr/cocorico/WTypeInsteadOfInductiveTypes)


[[!include semantics of W-types -- references]]


[[!redirects W-types]]