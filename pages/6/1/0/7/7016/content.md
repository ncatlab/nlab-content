
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
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
 {#InSetTheory}

In [[set theory]], there are two equivalent notions of function extensionality:

* for all sets $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, $f = g$ if and only if for all elements $x \in A$ $f(x) = g(x)$. 

* for all sets $A$ and $B$ and elements of the [[function set]] $f \in B^A$ and $g \in B^A$, $f = g$ if and only if for all elements $x \in A$ $\mathrm{ev}(f, x) = \mathrm{ev}(g, x)$. 

While the former is the one most commonly found in most foundations of [[categorical set theories]] as the [[axiom of extensionality]], the latter is the set theoretic analogue of the axiom of function extensionality found in [[dependent type theories]], where functions are elements of function types, the type theoretic analogue of function sets. Nonetheless, the two notions of function extensionality are equivalent to each other by [[currying]] and the [[universal property]] of [[function sets]]. 

### In category theory

There are two natural ways to extend the set-theoretic definition of function extensionality from the category of sets to more general categories by using either the external notion of quantifying over points as morphisms from the terminal object $x : 1 \to C$ or by interpreting the logical formulation of function extensionality in the [[internal language]] of the category. These notions are *not* equivalent and it is the latter form that would usually be intended when saying that a category “satisfies function extensionality” as it means that the category can be used as a model of a logic where function extensionality is provable.

The “external” formulation of function extensionality corresponds to the statement that the [[terminal object]] is an [[extremal generator]] in [[category]], and is one of the conditions for making a [[pretopos]] a [[well-pointed pretopos]]. This definition is satisfied in any [[concrete category]] $\mathcal{C}$.

The “internal” formulation can be interpreted in a category with a rich enough [[internal language]]. For instance, function extensionality can be stated in the [[Mitchell-Benabou language]] and is true in any [[topos]]. So every topos *internally* satisfies function extensionality despite the fact that toposes do not generally satisfy the external notion of being well-pointed. This is because the quantifier $\forall x:X$ in the internal language is interpreted as a quantification over all [[generalized elements]] $I \to X$ rather than merely the global elements $1 \to X$. Then the statement when quantifying over generalized elements is true as a consequence of the definition of an [[exponential]].

Although the internal logic of a locally cartesian closed category is a dependent type theory, a category satisfying function extensionality is not the same as a dependent type theory satisfying function extensionality, the latter corresponds to well-pointedness. This is because there is always an [[equivalence of types]] between the type $X$ and the [[function type]] $1 \to X$ from the [[unit type]] to $X$, and the quantifier $\forall x:X$ defined as the [[propositional truncation]] of the dependent product $\prod_{x:X}$ is interpreted element-wise in dependent type theory, which, by the above equivalence, is quantified over the global elements rather than over the generalized elements. 

### In type theory
 {#InTypeTheory}

In [[intensional type theory]], the notion of [[equality]] $a = a'$ is replaced by [[identifications]], these being [[terms]] of [[identity type]] $Id_A(a,a')$. Since such [[identity type]] are in general not [[mere propositions]], care needs to be exercised in stating function extensionality in intensional type theory:

For [[types]] $A, B \,\colon\, Type $ and [[parallel morphisms|parallel]] [[function type|functions]] $f, g  \,\colon\, A \to B$, there are the following two canonical functions (from [[identity types]] of [[function types]] to [[dependent products]] of pointwise identity types), which one may use for expressing function extensionality (eq:FunctionExtensionalityInTypeTheory), both defined via [[path induction]] (see at *[[function application to identifications]]*) as shown now:

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

{#TheseTwoDefinitions} (These two definitions of $\mathrm{happly}$ become the same under [[singleton contractibility]]. The second definition behaves better with the [[function application to identifications]].)

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
 {#Properties}

### Relation to weak function extensionality

Function extensionality is equivalent to [[weak function extensionality]] -- see at *[References -- General](#ReferencesGeneral)*.

### Relation to the univalence axiom

In [[homotopy type theory]], the [[univalence axiom]] implies type-theoretic function extensionality (eq:FunctionExtensionalityInTypeTheory) -- see at *[References -- in HoTT](#ReferencesInHomotopyTypeTheory)*.

### Relation to interval types

Postulating an [[interval type]] with [[judgmental equality|judgmental]] [[computation rules]] for the point constructors of the interval type implies function extensionality. 

The proof assumes a typal [[uniqueness rule]] for [[function types]]. Let $\mathrm{ap}_f \colon Id_{\mathbb{I}}(0, 1) \to Id_A(f(0),f(1))$ be the [[function application to identities]], $\mathrm{concat}_{a, b, c}: Id_A(a , b) \times Id_A(b , c) \to Id_A(a , c)$ be concatenation of identities (i.e. [[transitivity]]), and $\mathrm{inv}_{a, b}: Id_A(a , b) \to Id_A(b , a)$ be the inverse of identities (i.e. [[symmetry]]).

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



### Categorical semantics 
 {#CategoricalSemantics}

Under the standard [[relation between type theory and category theory]], the [[categorical semantics]] of the [[type]]
$
  \underset{x \colon X}{\prod} Id_Y\big( f(x),\, g(x) \big)
$
of pointwise [[identity type|identifications]] between a [[pair]] of [[parallel morphism|parallel]] [[functions]] $f,g \;\colon\; X \to Y$ is the [[space of sections]] over (hence the right [[base change]] along) $X$ of the [[pullback]]

\begin{tikzcd}[sep=30pt]
  (f,g)^\ast \mathrm{Paths}(Y)
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{\lrcorner}"{pos=.1}]
  &
  \mathrm{Paths}(Y)
  \ar[d, "{ (\mathrm{ev}_0, \mathrm{ev}_1) }"]
  \\
  X
  \ar[r, "{(f,g)}"]
  &
  Y \times Y
  \mathrlap{\,,}
\end{tikzcd}

where 

* $X,Y$ now denote [[objects]] in any given ambient [[categorical model of dependent types]] which serve as the [[categorical semantics]] for the [[types]] of the same name,

* $Paths(Y)$ denotes any "very good" [[path space object]] (see [there](path+space+object#InModelCategories)) of $Y$.

Since the right [[base change]] is [[right adjoint]] to [[pullback]], this means that the [[categorical semantics]] of [[global elements]] of $\underset{x \colon X}{\prod} Id_Y\big( f(x),\, g(x) \big)$, whose immediate categorical semantics is as [[maps]] out of the [[terminal object]] (to be denoted "$\ast$"):

\begin{tikzcd}[sep=20pt]
  \ast 
  \ar[r, dashed]
  &
  \underset{x \colon X}{\prod} 
  (f,g)^\ast \mathrm{Paths}(X)
  \mathrlap{\,,}
\end{tikzcd}

is [equivalently](adjoint+functor#InTermsOfHomIsomorphism) given by [[maps]] of the form

\begin{tikzcd}[sep=30pt]
  X 
  \ar[rr, dashed] 
  \ar[dr, equals]
  && 
  (f,g)^\ast \mathrm{Paths}(Y)
  \ar[dl]
  \\
  & 
  X
  \mathrlap{\,.}
\end{tikzcd}

These in turn (now by the defining [[universal property]] of the [[pullback]]) are equivalent to maps of the form

\begin{tikzcd}[sep=30pt]
  X 
  \ar[rr, dashed] 
  \ar[dr, "{(f,g)}"{swap}]
  && 
  \mathrm{Paths}(Y)
  \ar[dl, "{(\mathrm{ev}_0, \mathrm{ev}_1)}"]
  \\
  & 
  Y \times Y
  \mathrlap{\,,}
\end{tikzcd}

hence to [[lifts]] of $(f,g)$ through the [[path fibration]] [[display map]].

In contrast, the [[categorical semantics]] of the global type of identifications $Id_{(X \to Y)}(f,g)$ is by maps of the form

\begin{tikzcd}[
  column sep=-30pt,
  row sep=30pt
]
  \ast
  \ar[rr, dashed]
  \ar[dr, "{(f,g)}"{swap}]
  &&
  \mathrm{Paths}\big(\mathrm{Maps}(X,Y)\big)
  \ar[dl, "{(\mathrm{ev}_0, \mathrm{ev}_1)}"]
  \\
  & 
  \mathrm{Maps}(X,Y)
  \times
  \mathrm{Maps}(X,Y)
  \,,
\end{tikzcd}

where 

* $Maps(X,Y)$ denotes the [[internal hom]] in the ambient [[categorical model of dependent types]] ---

  if one assumes a [[cartesian closed category|cartesian closure]], then this is equivalently denoted as an [[exponential objects]]: $Y^X$.

So the [[categorical semantics]] of function extensionality (eq:FunctionExtensionalityInTypeTheory) says in particular that there is a map

$$
  \phi
  \;\colon\;
  Paths\big(Maps(X,Y)\big)
  \longrightarrow 
  Maps\big(X, Paths(Y) \big)
$$

which serves to lift [[global elements]] as above.

Of course we are not just interested in [[global element|global elements]] here. What we really want is an actual [[section]] $Maps\big(X, Paths(Y)\big) \to Paths\big(Maps(X,Y)\big)$ of $\phi$ in the [[slice category|slice]] over $Maps\big(X, (Y \times Y)\big)$ (although this can be derived from the global element formulation by using the [[Yoneda lemma]] together with [[currying]] and uncurrying tricks), such that this exhibits a [[weak equivalence]].

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



## See also

* [[extensionality]]

* [[homotopy]]

* [[concrete category]]

* [[prefunction]]

* [[weak function extensionality]]

* [[sequence extensionality]]

* [[equivalence extensionality]]

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

[[!redirects external function extensionality]]
[[!redirects external functional extensionality]]

[[!redirects internal function extensionality]]
[[!redirects internal functional extensionality]]

[[!redirects FunExt]]

[[!redirects morphism extensionality]]
