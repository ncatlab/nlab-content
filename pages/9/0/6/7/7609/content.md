
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

Syntactic _substitution_ of/for [[variables]] is one of the basic operations in formal mathematics, such as in [[formal logic]] and [[type theory|type theories]], where it is part of the *[[structural rules]]*.


## Syntactic substitution

Substitution is usually defined as an *operation* on expressions (such [[strings (computer science)|strings]] of letters from an [[alphabet]] and representing [[terms]], [[formulas]], [[propositions]], [[dependent types]], etc.) containing [[variables]].    

Suppose that $P$ is an expression in the [[context]] of a [[variable]] $x \,\colon\, X$ of [[type]], and that $t \colon X$ is an expression which has the same [[type]] as $x$.  Then one denotes by 

$$ 
  P[t/x] 
$$

the result of **substituting** $t$ for all occurrences of $x$ in $P$.

For example, if $P$ is $x^2 + 2x y + 3$ and $t$ is $(y+z)$, then $P[t/x]$ is $(y+z)^2 + 2(y+z)y + 3$.

\begin{remark}
**(substitution is a meta-operation on syntax)**
\label{AsOperationOnSyntax}
In this approach, substitution is an *operation on syntax*, not an element of [[syntax]] itself. In particular, the bracket notation $[t/x]$ is part of "meta-syntax", not the syntax in question.  

That is, the literal string of symbols "$P[t/x]$" is not itself an expression in the language under consideration, but *denotes* such an expression, in the same way that "$2+2$" is not literally an [[integer]] but *denotes* the [[numeral]] "$4$".

Compare also Rem. \ref{TypesettingByActualSubstitution} below.
\end{remark}

### Simultaneous substitution

Substitution for multiple variables does not, in general, commute.  That is, the expressions

$$
  P[t/x][s/y] 
  \qquad\text{and}\qquad 
  P[s/y][t/x]
$$

are not in general the same: The former substitutes $s$ for occurrences of $y$ in $t$, but not $t$ for occurrences of $x$ in $s$, while the latter has the opposite behavior.  We also write

$$ P[t,s/x,y] $$

to denote the *simultaneous substitution* of $t$ for $x$ and $s$ for $y$, in which *neither* occurrences of $x$ in $s$ nor occurrences of $y$ in $t$ are substituted for; this is generally not the same as either iterated substitution.


### Avoiding variable capture

If the language in question contains variable [[bound variable|binders]], then there is a subtlety to substitution: if $t$ contains free variables that are bound in $P$, then we cannot simply textually substitute $t$ for $x$ and obtain an expression with the desired meaning.

For instance, if $P$ is $\exists y (x + y = 1)$, and $t$ is the free variable $y$, then a literal interpretation of $P[t/x]$ would produce $\exists y (y + y = 1)$.  But $P$ is true (universally in its free variables) if the variables have type $\mathbb{Z}$, while $\exists y (y + y = 1)$ is not.  The free variable $y$ in $t$ has been "captured" by the binder $\exists y$ in $P$.

We say that $t$ is **substitutable** for $x$ in $P$ if performing a literal textual substitution as above would not result in undesired variable capture.  If $t$ is not substitutable for $x$ in $P$, then we can always replace $P$ by an [[alpha-equivalent]] expression in which $t$ *is* substitutable for $x$.  Since we often consider formulas only up to $\alpha$-equivalence anyway, one usually defines the notation "$P[t/x]$" to include an $\alpha$-conversion of $P$, if necessary, to make $t$ substitutable for $x$.

In computer implementations of type theories, however, the issue of variable binding and capture is one of the trickiest things to get right.  Performing $\alpha$-conversions is difficult and tedious, and other solutions exist, such as using [[de Bruijn indices]] to represent bound variables.


### As an admissible type inference rule

A general property of [[type theories]] (and other formal mathematics) is that *substitution is an admissible rule*.  

Roughly, this means that if $P$ is an [[term|expression]] of some [[type]], then so is the result $P[t/x]$ of substitution (as long as $t$ and $x$ have the same type).  This is generally not a rule "put into" the theory, but rather a property one *proves* about the theory; type theorists say that substitution is an [[admissible rule]] rather than a [[derivable rule]].

For instance, in the language of [[dependent type theory]] the following *substitution rule* (one of the [[structural rules]]) is an [[admissible rule]]:

\[
  \label{SubstitutionRuleInDependentTypeTheory} 
  Sub
  \frac{
    \Gamma,\; (x:A) \vdash P \;type
    \qquad 
    \Gamma \vdash (t:A) 
  }{
   \Gamma \vdash P[t/x] \;type
  } 
  \,.
\]

Here "admissibility" means that if there exist derivations of $\Gamma \vdash (t:A)$ and $(x:A) \vdash P \;type$, then there also exists a derivation of $\Gamma \vdash P[t/x] \;type$.  By contrast, saying that this is a derivable rule would mean that it can occur itself as *part* of a derivation, rather than being a meta-statement *about* derivations.

The substitution rule is closely related to the [[cut rule]], and admissibility of such rules is generally proven by [[cut elimination]].

\begin{remark}
\label{TypesettingByActualSubstitution}
**(alternative typesetting of substitution rule)**
\linebreak
In view of Remark \ref{AsOperationOnSyntax} we may re-express the substitution rule (eq:SubstitutionRuleInDependentTypeTheory) by using actual syntactic substitutions instead of the meta-instruction "[t/x]" to perform these, if only we make explicit the [[variable]] [[dependent type|dependency]] of all [[terms]], say by a subscript:

$$
  Sub
  \frac{
      \gamma \colon \Gamma
      ,\;\;
      a_\gamma \colon A_\gamma
      \;\;\;
      \vdash
      \;\;\;
      P_{a_\gamma} \;type
      \;\;\;\;\;\;\;\;\;\;\;
      \gamma \colon \Gamma
      \;\;\;
      \vdash
      \;\;\;
      t_\gamma \colon A
  }{
    \gamma \colon \Gamma
    \;\;\;
      \vdash
    \;\;\;
    P_{t_\gamma} \;type
  }
$$

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>


\end{remark}

## Explicit substitution

An alternative approach to substitution is to make substitution part of the object language rather than the metalanguage.  That is, the notation

$$P[t/x]$$

is now actually itself a string of the language under consideration.  One then needs reduction or equality rules describing the relationship of this string $P[t/x]$ to the result of actually substituting $t$ for $x$ as in the usual approach.  See [[explicit substitution]] for more details.


## Categorical semantics
 {#CategoricalSemantics}

### Definition

In the [[categorical semantics]] of [[type theory]]:

* Recalling that [[terms]] are interpreted by [[morphisms]], substitution of a term into another term is interpreted by [[composition]] of the relevant morphisms.

* Recalling that [[propositions]] are interpreted by [[subobjects]], substitution of a term $t$ into a proposition $P$ is interpreted by [[pullback]] or [[inverse image]] of the subobject interpreting $P$ along the morphism interpreting $t$.

* Recalling that [[dependent types]] are interpreted by [[display maps]], substitution of a term $t$ into a dependent type $B$ is interpreted by [[pullback]] of the display map interpreting $B$ along the morphism interpreting $t$.

* Or else, since [[dependent types]] are also given by [[classifying morphisms]] into a [[type of types]], substitution corresponds to [[composition]] of these classifying morphisms with the given morphism.

In the third case, there is a [[coherence]] issue: syntactic substitution in the usual approach is strictly [[associativity|associative]], whereas pullback in a category is not.  One way to deal with this is by using explicit substitution as described above.  Another way is to strictify the category before modeling type theory; see _[[categorical model of dependent types]]_. For literature see ([Curien-Garner-Hofmann](#CurienGarnerHofmann), [Lumsdaine-Warren 13](#LumsdaineWarren13)).


### Examples

Let $\mathcal{C}$ be a suitable ambient [[category]] in which we are [[categorical semantics|interpreting]] [[logic]]/[[type theory]].

Suppose $X$ and $Y$ are [[types]], hence interpreted as [[objects]] of $\mathcal{C}$. Then a [[term]] of [[function type]] $f : X \to Y$ is interpreted by a [[morphism]], going by the same symbols.

Now a [[proposition]] about [[terms]] of [[type]] $Y$

$$
  y : Y \vdash P(y)
$$

is interpreted as an [[object]] of the [[slice category]] $\mathcal{C}_{/Y}$, specifically as a [[truncated object of an (infinity,1)-category|(-1)-truncated]] object if it is to be a [[proposition]], hence by a [[monomorphism]]

$$
  \array{
    P 
    \\
    \downarrow
    \\
    Y
  }
  \,.
$$

For instance if $\mathcal{C} = $ [[Set]] then this is the inclusion of the [[subset]] of elements of $Y$ on which $P$ is true. And generally we may write

$$
  P = \{y : Y | isInhab(P(y)) \}
  \,.
$$

Now finally the **substitution** of $f(x)$ for $y$ in $P$, hence the proposition 

$$
  \array{
    P(f(-))
    \\
    \downarrow
    \\
    X
  }  
$$

is interpreted as the [[pullback]]

$$
  \array{
    P(f(-)) \coloneqq & f^* P &\to& P
    \\
    & \downarrow && \downarrow
    \\
    & X &\stackrel{f}{\to}& Y
  }
  \,.
$$

Notice that [[monomorphisms]] are preserved by pullback, so that this is indeed again the correct interpretation of a proposition.

Specifically, if $X$ is the [[unit]] type it is interpreted as a [[terminal object]] of $\mathcal{C}$, and then the [[function]] $f$ is identified simply with a [[term]] $y_0 \coloneqq f(*) $. In this case the substitution is _evaluation_ of the proposition at $y_0$, the resulting monomorphism

$$
  \array{
    P(y_0) 
    &\longrightarrow& 
    P
    \\
    \big\downarrow 
      && 
    \big\downarrow
    \\
    \ast 
    &
    \overset
      {y_0}
      {\longrightarrow}
    & 
    Y
  }
$$

over the terminal object is a [[truth value]]: the truth value of $P$ at $y_0$.


## Related concepts

[[!include substitution natural deduction - table]]

* [[structural rules]]

  * [[contraction rule]]

  * [[weakening rule]]

  * [[exchange rule]]

  * [[variable rule]]

  * [[substitution rule]]

* [[explicit substitution]]

* [[context extension]]

* [[telescope]]

* [[dependent product]], [[universal quantifier]]

* [[dependent sum]], [[existential quantifier]]

## References
 {#References}

Discussion of the substitution rule in [[intuitionistic type theory|intuitionistic]] [[dependent type theory]]:

* {#Jacobs98} [[Bart Jacobs]], p. 123 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], p. 423 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])

* {#Rijke18} [[Egbert Rijke]], p. 4 of: *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])


The observation that substitution forms an [[adjoint pair]]/[[adjoint triple]] with [[quantifiers]] is due to

* [[Bill Lawvere]], _Adjointness in Foundations_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

and further developed in 

* [[Bill Lawvere]], _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.

Exposition of the interpretation of substitution as pullback:

* [[Andrej Bauer]], _[Substitution is pullback](http://math.andrej.com/2012/09/28/substitution-is-pullback/)_, 2012

The [[coherence]] issue involved in making this precise is discussed in 

* {#CurienGarnerHofmann} [[Pierre-Louis Curien]], [[Richard Garner]], [[Martin Hofmann]], _Revisiting the categorical interpretation of dependent type theory_ ([[CurienGarnerHofmann.pdf:file]])

* {#LumsdaineWarren13} [[Peter LeFanu Lumsdaine]], [[Michael Warren]], _An overlooked coherence construction for dependent type theory_, CT2013  ([[LumsdaineWarren2013.pdf:file]])


[[!redirects substitution]]
[[!redirects substitutions]]
[[!redirects variable substitution]]
[[!redirects variable substitutions]]

[[!redirects variable capture]]
[[!redirects variable captures]]

[[!redirects substitution rule]]
[[!redirects substitution rules]]