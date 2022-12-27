
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Equivalences in type theory
* table of contents
{:toc}

## Idea

We discuss the correct (operational) notion of [[equivalence]] in [[type theory]].

In [[dependent type theory]] with [[axiom K]] or [[uniqueness of identity proofs]], the notion of **equivalence** corresponds roughly to the notion of [[bijection]] or [[one-to-one correspondence]] in [[set theory]]. 

In the context of dependent type theories without [[axiom K]] or [[uniqueness of identity proofs]], such as [[homotopy type theory]], **equivalence** corresponds to the notion of [[equivalence of categories|equivalence]] in [[groupoid|groupoid theory]] and, more generally, the notion of [[homotopy equivalence]] in [[homotopy theory]]. 

In [[point-set topology]] and generally in the context of [[homotopical category|homotopical]] [[1-category]]-[[category theory|theory]], these are called *[[weak equivalences]]*, since without suitable [[resolution]] they may not be [[homotopy equivalences]]. However, via the [[categorical semantics]] of [[homotopy type theory]] in [[type-theoretic model categories]], the required [[resolutions]] are all implicit (essentially since all objects are assumed to be [[cofibrant object|cofibrant]] and [[identity types]] are interpreted as [[fibrant resolution]] of [[diagonal maps]]) so that all (weak) equivalences are actually homotopy equivalences.



## Definition
 {#Definition}

Notice that there are several ways to define a [[bijection]] in [[set theory]]: 

1. as a map which admits a *two sided* [[inverse morphism]] --

   in [[homotopy type theory]] this leads to the notion of *[[quasi-inverse functions]]* or *[[homotopy equivalence]]* 

   (Def. \ref{FunctionWithTwoSidedInverse} below);

1. as a map which admits a [[left inverse]] and a [[right inverse]] --

   in [[homotopy type theory]] this leads to the notion of *left/right quasi-invertible maps* or *homotopy isomorphisms* 

   (Def. \ref{FunctionsWithLeftAndRightInverse} below);

1. as a function which is both an [[injection]] (whose fibers are [[subsingletons]]) and a [[surjection]] (whose fibers are [[inhabited]]) --

   in [[homotopy type theory]] this leads to the definition of equivalence as a function with contractible fibers 

   (Def. \ref{FunctionWithContractibleFiber} below).

1. as a [[relation]] which is an injective and surjective [[anafunction]].  --

   in [[homotopy type theory]] this leads to the definition of equivalence as a one-to-one correspondence

   (Def. \ref{OneToOneCorrespondence} below).

\linebreak

{#OutlookOnEquivalenceOfDefinitions} As (eventually to be) discussed in the *[Properties](#Properties)*-section below,
the evident types formed by these definitions are co-inhabited: we have a function from any one of them to any of the others.  Moreover, at least if we assume [[function extensionality]], the evident types of "homotopy isomorphisms" and of functions with contractible fibers are equivalent and are [[h-propositions]].
This is not true for the evident type of homotopy equivalences (as discussed [below](#TheIssueWithQuasiInverses)) which is not in general an h-prop even with function extensionality. However, often the most convenient way to show that $f$ is an equivalence is by exhibiting it as a term of the type of homotopy equivalences.


\linebreak

Throughout, we work in [[intensional type theory|intensional]] [[type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]]. 

In all of the following we consider:

* [[types]] $\;$ $A$ and $B$, 

* a [[term]] of [[function type]] $f \colon A \to B$, 

* a [[term]] $b \colon B$.

\linebreak

Most of the following claims may be found proven in [UFP13, §2.4 & §4](#UFP13).

\linebreak

> {#WarningOnFunctionExtensionality} **Warning.** The following discussion is still suffering from not saying where [[function extensionality]] is used, and not otherwise distinguishing between pointwise and global homotopy.

\linebreak

### As functions with two-sided quasi-inverse
 {#AsFunctionsWithTwoSidedInverse}

\begin{definition}\label{FunctionWithTwoSidedInverse}
**(function with two-sided inverse, up to homotopy)**
\linebreak
A function $f \,\colon\, A \to B$ is said to be [[quasi-inverse function|quasi invertible]] if it has a *two-sided* inverse, up to homotopy (hence also called a *[[homotopy equivalence]]*):

$$
  qinv(f)
  \;\coloneqq\;
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
$$

\end{definition}

([Hofmann & Streicher (1998), §5.4](#HofmannStreicher98))

This definition may seem the most obvious, but it suffers from a subltety in the construction of the type of all such functions, see [below](#TheIssueWithQuasiInverses).



### As functions with a left and a right quasi-inverse

In variation of Def. \ref{FunctionWithTwoSidedInverse}, we need not presuppose that the left and right inverse are already identified (this circumvents the [issue with two-sided inverses](#TheIssueWithQuasiInverses)):

\begin{definition}\label{FunctionsWithLeftAndRightInverse}
**(function with left and right inverse, up to homotopy)**
\linebreak

$$
  \mathrm{hasLeftRightInv}(f) 
  \;\coloneqq\; 
  \left(
    \sum_{g \colon B \to A} 
    \;
    \prod_{b:B} 
    \;
    f(g(b)) =_B b
  \right) 
   \;\times;\ 
  \left(
    \sum_{h \colon B \to A} 
    \;
    \prod_{a:A} 
    \;
    a =_A h(f(a))
  \right)
$$

\end{definition}

This is also called a *homotopy isomorphism* by [[André Joyal]] (2011), see [Kapulkin & Lumsdaine (2012, 2021), Def. 3.1.1](#KapulkinLumsdaine21).
 


### As functions with contractible fibers
 {#AsFunctionsWithContractibleFibers}


Recall that:

1. the ([[homotopy fiber|homotopy]]) [[fiber type]] of $f$ at $b$ is the [[dependent sum type]] 

   $$
     \mathrm{fiber}(f,b) 
     \;\coloneqq\; 
     \sum_{a:A} 
       \; f(a) = b
     \,,
   $$

1. the [[proposition]] that any type $C$ is a [[contractible type]] is

   $$
     \mathrm{isContr}(C) 
     \;\coloneqq\; 
     \sum_{a:C} \prod_{b:C} a =_C b
     \,,
   $$

1. so that the [[proposition]] that $f$ has *contractible fibers* is

   $$
     \mathrm{hasContrFibers}(f) 
     \;\coloneqq\; 
     \prod_{b:B} 
      \mathrm{isContr}
      \big(
        \mathrm{fiber}(f,b)
      \big)
     \,.
   $$

\begin{definition}\label{FunctionWithContractibleFiber}
**(functions with contractible fibers)**
\linebreak
We say $f$ is an **equivalence** if it comes with a witness $p \colon \mathrm{hasContrFibers}(f)$; that is, a function is an equivalence if all of its [[fiber types]] are [[contractible types]].
\end{definition}

Given two types $A$ and $B$, the **type of equivalences** from $A$ to $B$ is the [[dependent sum type]]

$$
  A \simeq B 
  \;\coloneqq\; 
  \sum_{f:A \to B} 
    \mathrm{hasContrFibers}(f)
  \,.
$$

This definition originates with [Voevodsky (2010), p. 8, 10](#Voevodsky10).

### As one-to-one correspondences
  {#OneToOneCorrespondences}

Let $\mathcal{U}$ be a [[universe]] and $A:\mathcal{U}$ and $B:\mathcal{U}$ be terms of the universe, and $R :A \times B \to \mathcal{U}$ be a [[correspondence]] between $A$ and $B$. We define the property of $R$ being **one-to-one** as follows:

$$isOneToOne(R) \coloneqq \left(\prod_{a:A} \mathrm{isContr}\left(\sum_{b:B} R(a,b)\right)\right) \times \left(\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} R(a,b)\right)\right)$$

\begin{definition}\label{OneToOneCorrespondence}
\linebreak
We say $R$ is an **equivalence** if it comes with a witness $p:isOneToOne(R)$. 
\end{definition}

We define the type of equivalences from $A$ to $B$ in $\mathcal{U}$ as 

$$(A \simeq_\mathcal{U} B)  \equiv \sum_{R : (A \times B) \to \mathcal{U}} isOneToOne(R)$$

By the [[type theoretic axiom of replacement]], the image of $R$ is $\mathcal{U}$-small, and thus $A \simeq_\mathcal{U} B$ is $\mathcal{U}$-small as well. 

### As adjoint equivalences

(...) like for a homotopy equivalence above, but in addition requiring the [[triangle identity]] for $f$ and $g$ -- as in an [[adjoint equivalence]] (...)

### Coinductive definition

Given two types $A$ and $B$ and two functions $f:A \to B$ and $g:B \to A$, $f$ and $g$ are inverses of each other if for every element $a:A$ and $b:A$, there is an equivalence of types between $f(a) =_B b$ and $a =_A g(b)$:

$$\mathrm{isInv}(f, g) \coloneqq \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

This leads to a coinductive definition of the type of equivalences

$$A \simeq B \coloneqq \sum_{f:A \to B} \sum_{g:B \to A} \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

### Strict equivalences

There is also a notion of **strict equivalence** between two types $A$ and $B$, where given functions $f:A \to B$ and $g:B \to A$ instead of having identity types between $g(f(a)) =_A a$ and similarly $b =_B f(g(b))$ making the pair of functions into [[quasi-inverse functions]], there are [[judgmental equalities]] $g(f(a)) \equiv a:A$ and $b \equiv f(g(b)):B$ or [[propositional equalities]] $g(f(a)) \equiv_A a \; \mathrm{true}$ and $b \equiv_B f(g(b)) \; \mathrm{true}$, making them into **judgmentally strict equivalences** and **propositionally strict equivalences** respectively. 

Judgmentally strict equivalences are used in defining [[Shulman univalent universes]] in [[higher observational type theory]]. 

## Properties
 {#Properties}

### Functions with contractible fibers and one-to-one correspondences

We define an [[anafunction]] to be a type family $R :A \times B \to \mathcal{U}$ with a witness

$$p:\prod_{a:A} \mathrm{isContr}\left(\sum_{b:B} R(a,b)\right)$$

The [[principle of unique choice]] holds in [[dependent type theory]]. This means that given any anafunction $R :A \times B \to \mathcal{U}$, there is function $f:A \to B$. Similarly, for any function $f:A \to B$, there is an anafunction $R :A \times B \to \mathcal{U}$ defined by $R(a,b) \coloneqq f(a) =_B b$. 

A function with contractible fibers comes with a witness 

$$q:\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_A b\right)$$

while an one-to-one correspondence is an anafunction which comes with a witness 

$$q:\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} R(a, b)\right)$$

Since we established that the types $f(a) =_A b$ and $R(a, b)$ are the same for function $f$ and anafunction $R$, functions with contractible fibers are equivalent to one-to-one correspondences. 

### The issue with two-sided quasi-inverses
 {#TheIssueWithQuasiInverses}

The possibly most evident definition of equivalences as two-sided [[quasi-inverse functions]] (Def. \ref{FunctionWithTwoSidedInverse}) suffers from the drawback that the type 

$$
  f \colon A \to B
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  qinv(f)
  \coloneqq
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \,,
$$

which may naively look like it merely detects whether $f$ is an equivalence, is in fact *not* a [[mere proposition]] ([UFP13, Thm. 4.1.3](#UFP13)).

This means that the type

\[
  \label{TheSubtlyWrongTypeOfEquivalences}
  \underset{
    f \colon A \to B
  }{\sum}  
  \;
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
\]

is --- despite its possible superficial appearance (cf. &lbrack;[Hofmann & Streicher (1998),  §5.4](#HofmannStreicher98)&rbrack;) -- *not* in fact equivalent to the correct type of equivalences $Equiv(A,B)$, which is instead obtained from this expression by including a [[0-truncation]] $[-]_{0}$:

$$
  Equiv(A,B)
  \;\simeq\;
  \underset{
    f \colon A \to B
  }{\sum}  
  \Bigg[
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \Bigg]_0
  \,.
$$

\linebreak


### Constructing the inverse function
 {#ConstructingTheInverseFunction}

For every function $f \colon A \to B$ with contractible fibers (Def. \ref{FunctionWithContractibleFiber}), 
there exists a function $g \colon B \to A$ which is an [[inverse function]]. 

The [[principle of unique choice]] implies that given a function $f:A \to B$, if for all $b:B$ the fiber of $f$ at $b$ is contractible, then for all $b:B$ there is an element $g(b):\mathrm{fiber}(f, b)$. 

$$\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_A b\right) \to \prod_{b:B} \sum_{a:A} f(a) =_A b$$

The [[type theoretic axiom of choice]] then states that for all elements $b:B$ one has the structure of an element $a:A$ such that $f(a) =_A b$, then one has a function $g:B \to A$ such that $f(g(b)) =_A b$. 

$$\prod_{b:B} \sum_{a:A} f(a) =_A b \to \sum_{g:B \to A} \prod_{b:B} f(g(b)) =_A b$$

There is also another definition of contractible type, which uses the notion of [[center of contraction]]; namely, that a type $A$ is a contractible type if it comes with a element $a:A$ and a witness that for all elements $b:A$, $a =_A b$

$$\prod_{b:A} a =_A b$$

Since the fiber of $f$ at $b$ is contractible, $g(b)$ is the [[center of contraction]] for the fiber of $f$ at $b$. 

Thus, for all elements $a:A$ and $b:B$ and a witness $q(a, b):f(a) =_B b$, there is a witness $r(a, b, q(a, b)):a =_A g(b)$. Since the type $a =_A g(b)$ doesn't depend on $q(a, b)$, by the rules of [[function types]], the latter condition is the same as for all elements $a:A$ and $b:B$, a function $r(a, b):f(a) =_B b \to a =_A g(b)$. 

...

still to prove: that the function above is an equivalence of types for all $a:A$ and $b:B$. 

## Semantics
 {#Semantics}

We discuss the [[categorical semantics]] of equivalences in homotopy type theory.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] which is a [[model category]], in which the (acyclic cofibration, fibration) [[weak factorization system]] has [[stable path objects]], and acyclic cofibrations are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of coherence, which are not important for this discussion.) For instance $\mathcal{C}$ could be a [[type-theoretic model category]].

### Of $hasContrFibers(-)$

+-- {: .num_prop }
###### Proposition

For $A, B$ two [[cofibrant object|cofibrant]]-[[fibrant objects]] in $\mathcal{C}$,
a morphism $f\colon A\to B$ is a [[weak equivalence]] or equivalently a [[homotopy equivalence]] in $\mathcal{C}$ precisely when the interpretation of $hasContrFibers(f)$ has a [[generalized element|global point]] $* \to hasContrFibers(f)$.

=--

+-- {: .proof}
###### Proof

For $f\colon A\to B$, the [[categorical semantics]] of the [[dependent type]]

$$
  b\colon B 
   \;\vdash\; 
  hfiber(f,b)\colon Type
$$ 

is by the rules for the [[categorical semantics|interpretation]] of [[identity types]] and [[substitution]]
the [[mapping path space]] construction $P f$, given by the [[pullback]]

$$
  \array{
    [b : B \vdash  hfiber(f,b)] &\coloneqq & P f  &\to& A
    \\
    && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    && B^I &\to& B
    \\
    && \downarrow
    \\
    && B
  }
$$

which, by the [[factorization lemma]], is one way to factor $f$ as an [[acyclic cofibration]] followed by a [[fibration]]

$$
  f : A \stackrel{\simeq}{\to} P f \to B
  \,.
$$

By definition and the semantics of [[contractible types]], therefore, if $A$ and $B$ are cofibrant, then $isEquiv(f)$ has a [[global element]] 

$$
  * \to \prod_{b} isContr(hfiber(f,b))
$$


precisely when in this factorization, the fibration $P f \to B$ is an acyclic fibration.  (See for instance ([Shulman, page 49](http://www.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49)) for more details.)


But by the [[2-out-of-3 property]], this is equivalent to $f$ being a weak equivalence --- and hence a homotopy equivalence, since it is a map between fibrant-cofibrant objects.


=--

+-- {: .num_remark #InterpretationIfIsEquivAsDependentType}
###### Remark

In the above we fixed one function $f : A \to X$. But the type $hasContrFibers$ is actually a [[dependent type]]

$$
  f : A \to B \vdash hasContrFibers(f)
$$

on the [[function type|type of all functions]]. To obtain the [[categorical semantics]] of this general dependent $hasContrFibers$-construction, first notice that the interpretation of

$f : A \to B,\; a : A,\; b : B \;\vdash\; (f(a) = b)  \colon Type$

is by the rules for interpretation of [[identity types]], [[evaluation]] and [[substitution]] the left vertical morphism in the [[pullback]] [[diagram]]

$$
  \array{  
    Q &\to&  B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
  }
  \,,
$$

where $eval : [A, B] \times A \to B$ is the [[evaluation map]] for the [[internal hom]].
This means that the interpretation of further [[dependent sum]] yielding $hfib$

$$
  f : A \to B,\; b : B 
   \; \vdash \;  
  \left(
    \sum_{a : A } (f(a) = b) 
  \right)
  \colon Type
$$

is the composite left vertical morphism in

$$
  \array{  
    Q &\to& B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
    \\
    \downarrow^{\mathrlap{p_{1,3}}}
    \\
    [A,B] \times B
  }
$$

=--

### Of $Equiv(-)$


(...)


## Related concepts

* **isEquiv**

* [[isContr]]

* [[isProp]]

* [[homotopy equivalence]]

  * [[weak homotopy equivalence]]

  * [[stable weak homotopy equivalence]]

* [[equivalence type]]

## References
 {#References}

The notion of two-sided homotopy equivalence of types in [[homotopy type theory]] appears (together with the formulation of the [[univalence axiom]]) already in

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]], §5.4 of:  _The groupoid interpretation of type theory_, in: [[Giovanni Sambin]] et al. (eds.), *Twenty-five years of constructive type theory*, Proceedings of a congress, Venice, Italy, October 19-21, 1995. Oxford: Logic Guides. **36**, Clarendon Press (1998) 83-111 &lbrack;[ISBN:9780198501275](https://global.oup.com/academic/product/twenty-five-years-of-constructive-type-theory-9780198501275), [ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz), [[HofmannStreicherGroupoidInterpretation.pdf:file]]&rbrack;

except that these authors refer to the subtly incorrect type (eq:TheSubtlyWrongTypeOfEquivalences) of all such equivalences.

The notion of equivalences as [[function type|functions]] with [[contractible type|contractible]] [[fiber type|homotopy fibers]] (and thereby the fix of the [[univalence axiom]] of [Hofmann & Streicher (1998), §5.4](#HofmannStreicher98)) is due to:

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 10 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

The notion of "homotopy isomorphisms" (functions with left- and right-quasi inverses) was proposed by [[André Joyal]] in a 2011 Oberwolfach meeting, recorded in:

* {#KapulkinLumsdaine21} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], Def. 3.1.1 in: *The Simplicial Model of Univalent Foundations (after Voevodsky)*, Journal of the European Mathematical Society **23** (2021) 2071–2126  &lbrack;[arXiv:1211.2851](https://arxiv.org/abs/1211.2851), [doi:10.4171/jems/1050](https://doi.org/10.4171/jems/1050)&rbrack;


Introduction and exposition:

* [[Andrej Bauer]], *HoTT equivalences*, talk (2011) &lbrack;[webpage](https://math.andrej.com/2011/12/07/hott-equivalences/), [video](https://www.youtube.com/watch?v=V3YUsZx_fmo)&rbrack;

* {#Shulman} [[Mike Shulman]], from [slide 60 of part 2](https://home.sandiego.edu/~shulman/hottminicourse2012/02hott.pdf#page=60), [slide 49 of part 3](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49) in: _Minicourse in homotopy type theory_ (2012) &lbrack;[web](https://home.sandiego.edu/~shulman/hottminicourse2012/)&rbrack;

* [[Andrej Bauer]], *Equivalences* &lbrack;[video](https://www.youtube.com/watch?v=BuI62-o3Ds8)&rbrack;, Part 4 of: *[Introduction to homotopy type theory](https://www.youtube.com/playlist?list=PL-47DDuiZOMCRDiXDZ1fI0TFLQgQqOdDa)*, lecture series (2019)


Textbook account:

* {#UFP13} [[Univalent Foundations Project]], §2.4 and §4 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


Implementation of equivalences in [[proof assistants]]:

in [[Coq]]:

* [github.com/HoTT/HoTT/blob/master/theories/Basics/Equivalences.v](https://github.com/HoTT/HoTT/blob/master/theories/Basics/Equivalences.v)

in [[Agda]]:

* [agda.github.io/agda-stdlib/v1.1/Function.Equivalence.html](https://agda.github.io/agda-stdlib/v1.1/Function.Equivalence.html)

On equivalences as one-to-one correspondences in homotopy type theory:

* Mike Shulman, *Towards a Third-Generation HOTT* Part 1 &lbrack;[slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA)&rbrack;


[[!redirects equivalence of types]]
[[!redirects equivalences of types]]

[[!redirects strict equivalence]]
[[!redirects strict equivalences]]

[[!redirects judgmentally strict equivalence]]
[[!redirects judgmentally strict equivalences]]

[[!redirects propositionally strict equivalence]]
[[!redirects propositionally strict equivalences]]

[[!redirects isEquiv]]

[[!redirects equivalence in homotopy type theory]]
[[!redirects equivalences in homotopy type theory]]
[[!redirects equivalence in type theory]]
[[!redirects equivalences in type theory]]
[[!redirects equivalence in HoTT]]
[[!redirects equivalences in HoTT]]

[[!redirects adjoint equivalence in homotopy type theory]]
[[!redirects adjoint equivalences in homotopy type theory]]
[[!redirects adjoint equivalence in type theory]]
[[!redirects adjoint equivalences in type theory]]
[[!redirects adjoint equivalence in HoTT]]
[[!redirects adjoint equivalences in HoTT]]

[[!redirects weak equivalence in homotopy type theory]]
[[!redirects weak equivalences in homotopy type theory]]
[[!redirects weak equivalence in type theory]]
[[!redirects weak equivalences in type theory]]
[[!redirects weak equivalence in HoTT]]
[[!redirects weak equivalences in HoTT]]

[[!redirects strict equivalence in homotopy type theory]]
[[!redirects strict equivalences in homotopy type theory]]
[[!redirects strict equivalence in type theory]]
[[!redirects strict equivalences in type theory]]
[[!redirects strict equivalence in HoTT]]
[[!redirects strict equivalences in HoTT]]

[[!redirects judgmentally strict equivalence in homotopy type theory]]
[[!redirects judgmentally strict equivalences in homotopy type theory]]
[[!redirects judgmentally strict equivalence in type theory]]
[[!redirects judgmentally strict equivalences in type theory]]
[[!redirects judgmentally strict equivalence in HoTT]]
[[!redirects judgmentally strict equivalences in HoTT]]

[[!redirects propositionally strict equivalence in homotopy type theory]]
[[!redirects propositionally strict equivalences in homotopy type theory]]
[[!redirects propositionally strict equivalence in type theory]]
[[!redirects propositionally strict equivalences in type theory]]
[[!redirects propositionally strict equivalence in HoTT]]
[[!redirects propositionally strict equivalences in HoTT]]

[[!redirects homotopy isomorphism]]
[[!redirects h-isomorphism]]