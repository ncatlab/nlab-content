
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
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

# Contents
* table of contents
{: toc}

## Idea

The principle of functional extensionality states that two [[functions]] are [[equal]] if their values are equal at every argument.

## Definition

### In set theory

In [[set theory]], function extensionality states that for all sets $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, if, for all elements $x \in A$, $f(x) = g(x)$, then $f = g$. 

There is another definition of function extensionality: for all sets $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, if, for all elements $x \in A$ and $y \in A$ such that $x = y$, $f(x) = g(y)$, then $f = g$. 

### In category theory

Since sets and functions form a [[category]], the set theory definition of function extensionality could be generalized to any [[category]] with a [[terminal object]]. Function extensionality corresponds to the fact that the [[terminal object]] is an [[extremal generator]] in [[category]], and is one of the conditions for making a [[pretopos]] a [[well-pointed pretopos]]. 

In additon, function extensionality in category theory is true in any [[concrete category]] $\mathcal{C}$. The axiom could be called "morphism extensionality"; however, in all concrete categories, the morphisms are functions between sets. 

### In type theory
 {#InTypeTheory}

In [[intensional type theory]], the notion of [[equality]] $a = a'$ is replaced by [[identifications]], these being [[terms]] of [[identity type]] $Id_A(a,a')$. Since such [[identity type]] are in general not [[mere propositions]], care needs to be exercised in stating function extensionality in intensional type theory:

For [[types]] $A, B \,\colon\, Type $ and [[parallel morphisms|parallel]] [[function type|functions]] $f, g  \,\colon\, A \to B$, there are the following two canonical functions (from [[identity types]] of [[function types]] to [[dependent products]] of pointwise identity types), which one may use for expressing function extensionality (eq:FunctionExtensionalityInTypeTheory), both defined via [[path induction]] as shown now:

\[
  \label{happlyDefinition}
  \begin{array}{ll}
     \mathrm{happly}(f, g)
     &\colon&
     Id_{(A \to B)} 
     (f ,\, g) 
     &
     \longrightarrow
     &
     \underset{
       a \colon A
     }
     {\prod} 
     Id_B
     \big(
       f(a)
       ,\,
       g(a)
     \big)
   \\
     \mathrm{happly}(f,f)
     &\colon& 
     \mathrm{refl}_{(A \to B)}(f)
     &\mapsto&
     \lambda (a \colon A).
     \mathrm{refl}_B
     \big(f(a)\big)
     \\
     \phantom{-}
     \\
    \mathrm{happly}(f, g)  
    &\colon&
    Id_{(A \to B)}(f, g) 
    &
    \longrightarrow 
    &
    \underset{a \colon A}{\prod}
    \;
    \underset{a' \colon A}{\prod}
    \prod_{p \colon Id_A(a,a')} 
    Id_B
    \big(
      f(a) ,\, g(a')
    \big)
    \\
    \mathrm{happly}(f,f)
    &\colon& 
    \mathrm{refl}_{A \to B}(f)
    &\mapsto&
    \lambda (a \colon A).
      \lambda (a \colon A).
        \lambda \big(
           \mathrm{refl}_A(x) 
            \colon 
            Id_A(a, a)
        \big).
        \mathrm{refl}_B\big(f(a)\big)
  \end{array}
\]

(These two definitions of $\mathrm{happly}$ become the same under [[singleton contractibility]]. The second definition behaves better with the [[action on identifications]].)

In general, both functions $\mathrm{happly}(f, g)$ are not [[equivalences of types]] in [[intensional type theory]]: two functions could be defined in different ways, and thus be intensionally different, yet produce the same values on all inputs (i.e. be extensionally the same).

Function extensionality is then the statement that the function $\mathrm{happly}(f, g)$ (eq:happlyDefinition) is an [[equivalence of types]] after all, for all functions $f, g \,\colon\,A \to B$:

\[
  \label{FunctionExtensionalityInTypeTheory}
  \mathrm{funext}(f, g)
  \;\colon\;
  \mathrm{isEquiv}
  \big(
    \mathrm{happly}(f, g)
  \big)
\]

\linebreak

### Judgmental function extensionality

One could replace the equivalences of types above with [[judgmental equality]] of types, which results in **judgmental function extensionality**. Applied to each definition, judgmental function extensionality states that for all all types $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$

$$
  Id_{(A \to B)}(f, g) 
  \;\;\equiv\; 
  \prod_{x:A} 
  id_B\big(
    f(x)
    ,\,
    g(x)
  \big)
$$

and 

$$
  Id_{(A \to B)}
  (f ,\, g) 
  \;\equiv\; 
  \prod_{x:A} 
  \prod_{y:A} 
  \prod_{p \colon Id_A(x, y)} 
  Id_B\big(
    f(x) ,\, g(y)
  \big)
$$

respectively. 

### For judgmental equality of sections

Suppose that given functions $f:A \to B$ and $g:A \to B$, for all $x:A$, $f(x)$ and $g(x)$ are [[judgmentally equal]] to each other $f(x) \equiv g(x):B$. Then it follows that $f$ and $g$ are judgmentally equal to each other, $f \equiv g:A \to B$, and thus function extensionality holds. This result is crucial in the proof of function extensionality from an [[interval type]] with judgmental computation rules. 

## Properties

### Relation to weak function extensionality

Function extensionality is equivalent to [[weak function extensionality]] -- see at *[References -- General](#ReferencesGeneral)*.

### Relation to the univalence axiom

In [[homotopy type theory]], the [[univalence axiom]] implies type-theoretic function extensionality (eq:FunctionExtensionalityInTypeTheory) -- see at *[References -- in HoTT](#ReferencesInHomotopyTypeTheory)*.


### Categorical semantics 
 {#CategoricalSemantics}

Translating the type theoretic definition (eq:FunctionExtensionalityInTypeTheory) into its [[categorical semantics]], the term $\eta$ gives a map 

$$
  1 \to \Pi_{X \to 1} [f x = g x]
$$ 

into the [[dependent product]], which (as discussed there), in turn corresponds to a [[section]] $\sigma \colon X \to [f x = g x]$ of the [[display map]] on the left side of the [[pullback]] 

$$
  \array{
    [f x = g x] 
    & \longrightarrow & 
    P(Y) 
    \\
    \big\downarrow & & \big\downarrow 
    \\
    X 
    & 
     \underset{\langle f, g \rangle}{\to} 
    & 
    Y \times Y
  }
  \,,
$$ 

where $P(Y)$ is the [[identity type]] or [[path space]] in $Y$. Such a section is tantamount to a lift $X \to P(Y)$ of $\langle f, g \rangle \colon X \to Y \times Y$. From this we would like to deduce an actual path $p \colon 1 \to P(Y^X)$. 

So, very simply, function extensionality means we are able to lift elements $h \colon 1 \to P(Y)^X$ through a canonical map $\phi \colon P(Y^X) \to P(Y)^X$ that is obtained from a [[dependent eliminator]]. 

Of course we are not just interested in [[global element|global elements]] here. What we really want is an actual section $P(Y)^X \to P(Y^X)$ of $\phi$ in the [[slice category|slice]] over $(Y \times Y)^X$ (although this can be derived from the global element formulation by using the [[Yoneda lemma]] together with [[currying]] and uncurrying tricks). This condition may be called "naive" or "weak" function extensionality, in view of an apparently stronger condition that this section (and therefore also $\phi$) be _equivalences_. This latter condition might be called "strong function extensionality". 

Under reasonable assumptions on the type theory, it turns out that these and other versions of function extensionality are equivalent; for now see ([Lumsdaine](#Lumsdaine)) below. In any case, if the type theory has an extra [[axiom]] that implies some such version, one says that **function extensionality** holds. 

### Homotopy categorical semantics
 {#HomotopyCategoricalSemantics}

+-- {: .num_prop #FunExtInFibrationCat}
###### Proposition

Function extensionality holds in the [[internal language|internal]] [[type theory]] of a [[type-theoretic fibration category]] precisely if [[dependent products]] (i.e. right [[base change]]) along [[fibrations]] preserve [[acyclic fibrations]].

=--

([Shulman 12, lemma 5.9](#Shulman12))

+-- {: .num_example #EveryPresentableLocallyCartesinClosedInfinityCatInterpretsHoTTPlusFunExt}
###### Example

The condition in prop. \ref{FunExtInFibrationCat} holds in particular in [[right proper model category|right proper]] [[Cisinski model structures]], since in these right [[base change]] along fibrations is a [[right Quillen functor]] (see e.g. the proof <a href="https://ncatlab.org/nlab/show/locally+cartesian+closed+(infinity,1)-category#PresentationTheorem">here</a>). 

Notice that every [[presentable (∞,1)-category|presentable]] [[locally Cartesian closed (∞,1)-category]] (by the discussion <a href="locally+cartesian+closed+(infinity,1)-category#PresentationTheorem">there</a>) has a presentation by a [[right proper model category|right proper]] [[Cisinski model category]]. Accordingly we may say that every [[presentable (∞,1)-category|presentable]] [[locally Cartesian closed (∞,1)-category]] interprets [[HoTT]]+FunExt.

=--

### Relation to interval types

Postulating an [[interval type]] with [[judgmental equality|judgmental]] [[computation rules]] for the point constructors of the interval type implies function extensionality. 

The proof assumes a typal [[uniqueness rule]] for [[function types]]. Let $\mathrm{ap}_f \colon Id_{\mathbb{I}}(0, 1) \to Id_A(f(0),f(1))$ be the [[action on identities]], $\mathrm{concat}_{a, b, c}: Id_A(a , b) \times Id_A(b , c) \to Id_A(a , c)$ be concatenation of identities (i.e. [[transitivity]]), and $\mathrm{inv}_{a, b}: Id_A(a , b) \to Id_A(b , a)$ be the inverse of identities (i.e. [[symmetry]]).

First the proof constructs a function $k:A \to (\mathbb{I} \to B)$ from a dependent function $h:\prod_{x:A} Id_B\big(f(x) , g(x)\big)$, inductively defined by

* $\beta_{k(x)}^0 : Id_B\big(k(x)(0) , f(x)\big)$

* $\beta_{k(x)}^1 : Id_B\big( k(x)(1) , g(x) \big)$

* $\beta_{k(x)}^p : Id_{Id_B\big(k(x)(0) , k(x)(1)\big)}\big(\mathrm{ap}_{k(x)}(p) , \mathrm{concat}_{k(x)(0), f(x), k(x)(1)}(\mathrm{concat}_{k(x)(0), f(x), g(x)}(\beta_{k(x)}^0, h(x)), \mathrm{inv}_{k(x)(1), g(x)}(\beta_{k(x)}^1))\big)$

Then it uses the properties of function types, product types, currying, uncurrying, and the symmetry of products $A \times B \simeq B \times A$, to construct a function $k':\mathbb{I} \to (A \to B)$, inductively defined by

* $\beta_{k'}^0(x): Id_B\big( k'(0)(x) , f(x)\big)$

* $\beta_{k'}^1(x): Id_B\big( k'(1)(x) , g(x) \big)$

* $\beta_{k'}^p(x):\mathrm{ap}_{k'}(p)(x) =_{Id_B\big( k'(0)(x) , k'(1)(x) \big)} \mathrm{concat}_{k'(0)(x), f(x), k'(1)(x)}(\mathrm{concat}_{k'(0)(x), f(x), g(x)}(\beta_{k'}^0(x), h(x)), \mathrm{inv}_{k'(1)(x), g(x)}(\beta_{k'}^1(x)))$

If the interval type has judgmental computation rules for the point constructors, then $k'(x)(0) \equiv f(x)$ and $k'(x)(1) \equiv g(x)$ for all $x:A$, which implies that $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$, and subsequently that $k'(0) \equiv f$ and $k'(1) \equiv g$. This means that there are identities $\beta_{k'}^0:k'(0) =_{A \to B} f$ and $\beta_{k'}^1:k'(1) =_{A \to B} g$, and an identity 

$$\mathrm{concat}_{f, k'(1), g}(\mathrm{concat}_{f, k'(0), k'(1)}(\mathrm{inv}_{k'(0), g}(\beta_{k'}^0), \mathrm{ap}_{k'}(p), \beta_{k'}^1): Id_{(A \to B)}(f , g)$$

thus proving function extensionality. 

An interval type with only typal computation rules for the point constructors does not imply function extensionality. This is because the proof with the judgmental computation rules uses the fact that $k'(0)(x) \equiv f(x)$ and $k'(1)(x) \equiv g(x)$ for all $x:A$ implies that $k'(0) \equiv f$ and $k'(1) \equiv g$. However, if the computation rules are typal, then the equivalent statement is that having identities $\beta_{k'}^0(x): Id_B\big(k'(0)(x) , f(x)\big)$ and $\beta_{k'}^1(x): Id_B\big(k'(1)(x) , g(x)\big)$ for all $x:A$ implies that there are identities $\beta_{k'}^0: Id_{(A \to B)}\big(k'(0) , f\big)$ and $\beta_{k'}^1 : Id_{A \to B}\big(k'(1) , g\big)$, which is precisely function extensionality, and so cannot be used to prove function extensionality. 


## See also

* [[extensionality]]

* [[homotopy]]

* [[concrete category]]

* [[prefunction]]

* [[weak function extensionality]]


## References
 {#References}

### General
 {#ReferencesGeneral}

Discussion of variants of function extensionality in [[Martin-Löf type theory]], and their relation:

* [[Richard Garner]], *On the strength of dependent products in the type theory of Martin-Löf*, Annals of Pure and Applied Logic **160** 1 (2009) 1-12 &lbrack;[arXiv:0803.4466](https://arxiv.org/abs/0803.4466), [doi:10.1016/j.apal.2008.12.003](https://doi.org/10.1016/j.apal.2008.12.003)&rbrack;

* [[Peter LeFanu Lumsdaine]], *Strong functional extensionality from weak* (2011) &lbrack;[blog post](http://homotopytypetheory.org/2011/12/19/strong-funext-from-weak)&rbrack;

* [Rijke (2022), §13.1](#Rijke22)

Proofs of function extensionality from an [[interval type]] with [[judgmental equality|judgmental]] [[computation rules]]:

* {#Shulman11} [[Mike Shulman]], _An interval type implies functional extensionality_ (2011) &lbrack;[blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/)&rbrack;


### In homotopy type theory
 {#ReferencesInHomotopyTypeTheory}

Discussion of function extensionality in [[homotopy type theory]] and proof that it is implied by [[univalence]]:

Original announcement in:

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 8 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

Textbook accounts:

* [[Univalent Foundations Project]], §2.9 & §4.9 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], §13 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;

Exposition:

* {#Angiuli11} [[Carlo Angiuli]], *Univalence implies function extensionality* (2011) &lbrack;[blog post](http://homotopytypetheory.org/2011/12/05/hott-in-prose/), [pdf](http://hottheory.files.wordpress.com/2011/12/hott2.pdf)&rbrack;

Tutorial for formalization in [[Coq]]:

* {#BauerLumsdaine} [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], *[[Oberwolfach HoTT-Coq tutorial]]* (2011)

Formalization in cubical [[Agda]]:

* [[1lab]], *[$\Pi$-types and function extensionality](https://1lab.dev/HoTT.html#%CF%80-types-and-function-extensionality)*

Discussion of the [[categorical semantics]] in the context of [[homotopy type theory]]:

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))
  

On definitional function extensionality in [[higher observational type theory]]:

* [[Mike Shulman]], *Towards Third-Generation HOTT -- Part 1* (2022) &lbrack;[slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA)&rbrack;



[[!redirects function extensionality]]
[[!redirects functional extensionality]]

[[!redirects FunExt]]

[[!redirects morphism extensionality]]
