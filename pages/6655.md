+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Martin-L&#246;f dependent type theory#
* table of contents
{:toc}

##Idea

[[Per Martin-Lof|Per Martin-Löf]]'s **[[dependent type theory]]**, also known as **[[intuitionistic logic|intuitionistic]] type theory** ([Martin-Löf 75](#MartinLof75)), or **constructive type theory** is a specific form of [[type theory]] developed to support [[constructive mathematics]].  (Note that both "dependent type theory" and "intuitionistic type theory" may refer more generally to [[type theories]] that contain [[dependent types]] or are [[intuitionistic mathematics|intuitionistic]], respectively.)

Martin-L&#246;f's dependent type theory is notable for several reasons: 

* One can construct an interpretation of first-order [[intuitionistic logic]] by interpreting [[propositions as types]] (this is true of most any dependent type theory).

* It has a version of a variant of the [[axiom of choice]] _as a theorem_ (because of the properties of the above interpretation), see the discussion [below](#AxiomOfChoice).

* In its [[intensional type theory|intensional]] form, it has sufficient computational content to function as a programming language. At the same time, it then has [[identity types]] whose presence shows that one is really dealing with a form of [[homotopy type theory]].

## Syntax
If $t$ is a term, and $A$ a type, then $t : A$ is a **typing declaration** asserting that $t$ is a term of type $A$. We will define the forms of valid terms and types below; to begin with, we assume we have a stock of variables, atomic types, and parametrised types.

A **context** is a [[finite set|finite]] ordered list of typing declarations, defined [[inductive definition|inductively]] as follows:

* The empty list is a valid context.
* If $\Gamma$ is a valid context, $x$ is a variable not appearing in $\Gamma$, and $A$ is a valid type in the context $\Gamma$, then the context obtained by appending $x : A$ to $\Gamma$ is also valid.

Note that this must be considered a *mutual* inductive definition along with the definition of when a type is valid in a given context, which is to be given below in terms of type constructors.

We write $\Gamma \vdash t : A$ to assert that $t : A$ is a valid typing declaration in the context of $\Gamma$, and by abuse of notation we may write $\Gamma \vdash A : \mathrm{Type}$ to assert that $A$ is a valid type in the context of $\Gamma$.

For any context $\Gamma$, if $A$ is an atomic type, $\Gamma \vdash A : \mathrm{Type}$.

If $x : A$ is a typing declaration in $\Gamma$, then we have $\Gamma \vdash x : A$.

###Binary product types
If $\Gamma \vdash A : \mathrm{Type}$ and $\Delta \vdash B : \mathrm{Type}$, then $\Gamma, \Delta \vdash A \times B : \mathrm{Type}$. 

If $\Gamma \vdash a : A$ and $\Delta \vdash b : B$ then $\Gamma, \Delta \vdash \langle a, b \rangle : A \times B$.

If $\Gamma \vdash c : A \times B$, then $\Gamma \vdash \pi_0(c) : A$ and $\Gamma \vdash \pi_1(c) : B$.

###Unit type
There is an atomic type called $\top$.

For any context $\Gamma$ we have $\Gamma \vdash \mathrm{tt} : \top$.

###Dependent product types
If $\Gamma, x : X \vdash A(x) : \mathrm{Type}$, then $\Gamma \vdash (\Pi x : X) A(x) : \mathrm{Type}$.

If $\Gamma, x : X \vdash a(x) : A(x)$, then $\Gamma \vdash (\lambda x : X) a(x) : (\Pi x : X) A(x)$.

If $\Gamma \vdash f : (\Pi x : X) A(x)$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}(f, t) : A(t)$.

###Function types
Function types may be regarded as a special case of dependent product types, where $A(x)$ does not depend on $x$ at all.  When we write out the rules for dependent products in this case, they become the following.

Firstly, if $\Gamma \vdash X : \mathrm{Type}$ and $\Gamma \vdash A : \mathrm{Type}$, then $\Gamma \vdash X \to A : \mathrm{Type}$.

If $\Gamma, x : X \vdash a(x) : A$, then $\Gamma \vdash (\lambda x : X) a(x) : X \to A$.

If $\Gamma \vdash f : X \to A$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}(f, t) : A$.

###Binary sum types
If $\Gamma \vdash A : \mathrm{Type}$ and $\Gamma \vdash B : \mathrm{Type}$, then $\Gamma \vdash A + B : \mathrm{Type}$. 

If $\Gamma \vdash a : A$ and $\Gamma \vdash A + B : \mathrm{Type}$, then $\Gamma \vdash \sigma_0 (a) : A + B$; and if $\Gamma \vdash b : B$ and $\Gamma \vdash A + B : \mathrm{Type}$, then $\Gamma \vdash \sigma_1(b) : A + B$.

If $\Gamma \vdash s : A + B$, $\Delta, x : A \vdash c(x) : C(\sigma_0(x))$ and $E, y : B \vdash c'(y) : C(\sigma_1(y))$, then $\Gamma, \Delta, E \vdash \mathrm{cases}(s, (\lambda x : A) c(x), (\lambda y : B) c'(y)) : C(s)$.

###Empty type
There is an atomic type called $\bot$.

If $\Gamma \vdash A : \mathrm{Type}$, then $\Gamma, x : \bot \vdash \mathrm{abort} : A$.

###Dependent sum types
If $\Gamma, x : X \vdash A(x) : \mathrm{Type}$, then $\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{Type}$.

If $\Gamma \vdash t : X$, $\Gamma \vdash a : A(t)$ and $\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{Type}$, then $\Gamma \vdash (t, a) : (\Sigma x : X) A(x)$.

If $\Gamma \vdash s : (\Sigma x : X) A(x)$ and $\Delta, x : X, y : A(x) \vdash b(x, y) : B((x, y))$, then $\Gamma, \Delta \vdash \mathrm{cases}(s, (\lambda x : X)(\lambda y : A(x)) b(x, y)) : B(s)$.

Note that just as function types can be defined to be dependent products where $A(x)$ does not depend on $x$, binary product types (above) can be defined to be dependent sums where $A(x)$ does not depend on $x$.

###Finite types
Martin-L&#246;f also includes in his type theory a type $\mathbb{N}_n$ with exactly $n$ elements, for every *external* [[natural number]] $n$.  The types $\bot$ and $\top$ can then be defined as $\mathbb{N}_0$ and $\mathbb{N}_1$, respectively.  On the other hand, with $\bot$ and $\top$ given as above, one may define $\mathbb{N}_2 = \top + \top$, $\mathbb{N}_3 = \top+\top+\top$, and so on (by [[recursion]] on the external natural number $n$).

Note that we have not included any [[axiom of infinity]], however.

### Propositions as types

Under the [[Curry-Howard isomorphism]], we may identify propositions with certain atomic types and predicates with certain parametrised types.  

An inhabitant of such a [[propositions as types|proposition-as-a-type]] is interpreted as a 'proof' of that proposition.

We write $\Gamma \vdash A : \mathrm{true}$ for the judgement that $A$ is [[inhabited set|inhabited]]: that is, if $\Gamma \vdash a : A$, then $\Gamma \vdash A : \mathrm{true}$. The type-formation rules above are then seen to be the rules of inference for (a fragment of) [[intuitionistic logic|intuitionistic]] [[first-order logic]]. Indeed, we have:

* [[logical conjunction|Conjunction]] introduction:
$$\frac{\Gamma \vdash A : \mathrm{true} ; \Delta \vdash B : \mathrm{true}}{\Gamma, \Delta \vdash A \times B : \mathrm{true}}$$
* Conjunction elimination:
$$\begin{aligned}
\frac{\Gamma \vdash A \times B : \mathrm{true}}{\Gamma \vdash A : \mathrm{true}} \,\, &
\frac{\Gamma \vdash A \times B : \mathrm{true}}{\Gamma \vdash B : \mathrm{true}} 
\end{aligned}$$
* [[truth|Truth]] introduction
$$\frac{}{\Gamma \vdash \top : \mathrm{true}}$$
* [[universal quantifier|Universal]] generalisation:
$$\frac{\Gamma, x : X \vdash A(x) : \mathrm{true}}{\Gamma \vdash (\Pi x : X) A(x) : \mathrm{true}}$$
* Universal instantiation:
$$\frac{\Gamma \vdash (\Pi x : X) A(x) : \mathrm{true} ; \Delta \vdash t : X}{\Gamma, \Delta \vdash A(t) : \mathrm{true}}$$
* Conditional proof ([[implication]] introduction):
$$\frac{\Gamma, X : \mathrm{true} \vdash A : \mathrm{true}}{\Gamma \vdash X \to A : \mathrm{true}}$$
* Modus ponens ([[implication]] elimination):
$$\frac{\Gamma \vdash X \to A : \mathrm{true} ; \Delta \vdash X : \mathrm{true}}{\Gamma, \Delta \vdash A : \mathrm{true}}$$
* [[disjunction|Disjunction]] introduction:
$$\begin{aligned}
\frac{\Gamma \vdash A : \mathrm{true}}{\Gamma \vdash A + B : \mathrm{true}} \,\, &
\frac{\Gamma \vdash B : \mathrm{true}}{\Gamma \vdash A + B : \mathrm{true}}
\end{aligned}$$
* Disjunction elimination:
$$\frac{\Gamma \vdash A + B : \mathrm{true} ; \Delta, A : \mathrm{true} \vdash C : \mathrm{true} ; E, B : \mathrm{true} \vdash C : \mathrm{true}}{\Gamma, \Delta, E \vdash C : \mathrm{true}}$$
* [[false|False]] elimination:
$$\frac{\Gamma \vdash \bot : \mathrm{true}}{\Gamma \vdash A : \mathrm{true}}$$
* [[existential quantifier|Existential]] generalisation:
$$\frac{\Gamma \vdash t : X ; \Gamma \vdash A(t) : \mathrm{true}}{\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{true}}$$
* Existential instantiation:
$$\frac{\Gamma \vdash (\Sigma x : X) A(x) : \mathrm{true} ; \Delta, x : X, A(x) : \mathrm{true} \vdash B : \mathrm{true}}{\Gamma, \Delta \vdash B : \mathrm{true}}$$

The only traditional rule of inference we are missing is the rule of [[excluded middle]], so this logic is [[intuitionistic logic|intuitionistic]].

The above interpretation justifies the use of the symbols $\forall$, $\exists$, $\wedge$, $\vee$ instead of $\Pi$, $\Sigma$, $\times$, $+$, when we are using types to represent propositions.

### Equality types

We may introduce a family of equality types for each type and each pair of terms of that type: if $\Gamma \vdash a : A$ and $\Delta \vdash a' : A$, then $\Gamma \vdash a = a' : \mathrm{Type}$.

These are not the intensional [[identity types]] which Martin-L&#246;f later introduced as a particular sort of [[inductive type|inductive family of types]], but instead an extensional notion of equality defined by [[induction]] *over* the class of all types (regarded as inductively defined by the above type-formation clauses).  Note that it is essential, for a purpose such as this, that the type-formation clauses be regarded as an inductive definition, rather than as "operations" defined on some pre-existing collection of types: in order to define equality in the way we are about to do, we have to be able to inspect a given type and decide uniquely which rule was used to construct it.

The equality type is reflexive, symmetric, and transitive. That means, for example, if $\Gamma \vdash a : A$, $\Gamma \vdash b : A$, $\Gamma \vdash c : A$, $\Gamma \vdash a = b : \mathrm{true}$ and $\Gamma \vdash b = c : \mathrm{true}$ then $\Gamma \vdash a = c : \mathrm{true}$.

+--{: .query}
[[Mike Shulman]]: Is that (reflexivity, symmetry, and transitivity) a rule we are giving, or an assertion we are making about derivability?  I'm a little unsure because the presentation here is slightly different from that in the reference: there Martin-L&#246;f uses both a propositional equality and a judgmental one.
=--

### Finite product types

If $\Gamma \vdash a : A$, and $\Gamma \vdash b : B$, then $\Gamma \vdash a = \pi_0 (\langle a, b \rangle) : \mathrm{true}$ and $\Gamma \vdash \pi_1 (\langle a, b \rangle) = b : \mathrm{true}$.

If $\Gamma \vdash c : A \times B$, then $c = \langle \pi_0 (c), \pi_1 (c) \rangle : \mathrm{true}$.

### Unit type
If $\Gamma \vdash a : \top$, then $\Gamma \vdash a = \mathrm{tt} : \mathrm{true}$.

### Dependent product types

If $\Gamma, x : X \vdash a(x) : A(x)$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}((\lambda x : X) a(x), t) = a(t) : \mathrm{true}$.

If $\Gamma \vdash f : (\Pi x : X) A(x)$, then $\Gamma \vdash f = (\lambda x : X) \mathrm{apply}(f, x) : \mathrm{true}$.

### Function types
If $\Gamma, x : X \vdash a(x) : A$ and $\Delta \vdash t : X$, then $\Gamma, \Delta \vdash \mathrm{apply}((\lambda x : X) a(x), t) = a(t) : \mathrm{true}$.

If $\Gamma \vdash f : X \to A$, then $\Gamma \vdash f = (\lambda x : X) \mathrm{apply}(f, x) : \mathrm{true}$.

### Binary sum types

If $\Gamma \vdash a : A$ and $\Gamma \vdash A + B : \mathrm{Type}$, $\Delta, x : A \vdash c(x) : C(\sigma_0(x))$ and $E, y : B \vdash c'(y) : C(\sigma_1(y))$, then $\Gamma, \Delta, E \vdash \mathrm{cases}(a, (\lambda x : A) c(x), (\lambda y : B) c(y)) = c(a) : \mathrm{true}$ and $\Gamma, \Delta, E \vdash \mathrm{cases}(b, (\lambda x : A) c(x), (\lambda y : B) c'(y)) = c'(b) : \mathrm{true}$

###Dependent sum types
If $\Gamma \vdash t : X$, $\Gamma \vdash a : A(t)$ and $\Delta, x : X, y : A(x) \vdash b(x, a) : B((x, a))$, then $\Gamma, \Delta \vdash \mathrm{cases}((t, a), (\lambda x : X)(\lambda y : A(x)) b(x, y)) = b(t, a) : \mathrm{true}$.

The other equality rule for dependent sum types is derivable from the above.

## Properties

### Models and categorical semantics

The [[models]] of ML type theory depend crucially on whether one considers
the variant of [[extensional type theory]] or that of [[intensional type theory]].

The models of the extensional version are (just) [[locally cartesian closed categories]].

The faithful models of the intensional version with [[identity types]] are however certain [[(∞,1)-categories]], notably [[(∞,1)-toposes]], presented by [[simplicial model categories]] ([Warren](#Warren)). For this reason one speaks of _[[homotopy type theory]]_.

For a more detailed discussion of these matters see at _[[relation between type theory and category theory]]_.


### Axiom of choice
 {#AxiomOfChoice}

In dependent type theory we can verify the following "logical form of the [[axiom of choice]]" ([Bell](#Bell), [Tait](#Tait)), see also ([Rijke, section 2.5.1](#Rijke)).

+-- {: .num_theorem }
###### Theorem 
**(ACL)**

$$
  x : A, y : B(x) \vdash C(x, y) : Type
  \;
  \vdash 
  \;
  acl
  :
  (\forall x : A) (\exists y : B(x)) C(x, y) \to (\exists f : (\Pi x : A)B(x) )(\forall x : A) C(x, \mathrm{apply}(f, x)) 
  \,.
$$

=--

One should note carefully that this "is" only "the axiom of choice" under the above propositions-as-types interpretation of the quantifiers $\forall$ and $\exists$.  

+-- {: .num_remark}
###### Remark

In the [[categorical semantics]] of this expression, using the 
[[propositions-as-types]] logic corresponds roughly to working with the [[subobject lattices]] in the [[ex/lex completion]] of a [[locally cartesian closed category]]; the ACL then follows since every object of the original category becomes [[projective object|projective]] in its ex/lex completion.

=--

+-- {: .num_remark}
###### Remark

If we use instead a different logic over the same type theory, such as [[bracket types]] to model the actual subobject lattices in an arbitrary 
[[locally cartesian closed category|lccc]] (not necessarily the ex/lex completion of anything), or the 
[[hProp]] logic in [[homotopy type theory]], then the ACL in that logic will not be derivable.

=--


## Related concepts

* [[initiality conjecture]]

[[!include notions of type]]

## References

See also the references at _[[type theory]]_.

The original articles:

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80** Pages 73-118,  Elsevier 1975 (<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

* [[Per Martin-Löf]] (notes by Giovanni Sambin), _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) ([pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]])

As a [[programming language]]:

* [[Per Martin-Löf]], *Constructive Mathematics and Computer Programming*, Studies in Logic and the Foundations of Mathematics Volume 104, 1982, Pages 153-175 (<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>)

* Bengt Nordström, Kent Petersson, Jan M. Smith, *Programming in Martin-Löf's Type Theory*, Oxford University Press 1990 ([webpage](http://www.cse.chalmers.se/research/group/logic/book/), [pdf](http://www.cse.chalmers.se/research/group/logic/book/book.pdf))


A philosophical examination:

* [[Göran Sundholm​]], _Proof Theory and Meaning_ (1986), ([pdf](https://openaccess.leidenuniv.nl/bitstream/handle/1887/11978/9_05?sequence=1))

An introduction and survey (with an eye towards [[homotopy type theory]]) is in chapter 1 of

* {#Warren} [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))
 

as well as

* {#Rijke} Egbert Rijke, _Homotopy type theory_ (2012) ([pdf](http://hottheory.files.wordpress.com/2012/08/hott2.pdf))
 

A discussion of ML dependent type theory as the [[internal language]] of [[locally cartesian closed categories]] is in 

* [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

Discussion of the logical [[axiom of choice]] in dependent type theory is in 

* {#Bell} John Bell, _The Axiom of choice in type theory_, Stanford Encyclopedia of philosophy, 2008 ([web](http://plato.stanford.edu/entries/axiom-choice/choice-and-type-theory.html)) 
 

* {#Tait} Tait (1994)
 

[[!redirects Martin-Lof dependent type theory]]
[[!redirects Martin-Löf dependent type theory]]
[[!redirects Martin-Lof type theory]]
[[!redirects Martin-Löf type theory]]
[[!redirects Martin-Löf type theories]]
[[!redirects constructive type theory]]
[[!redirects intuitionistic type theory]]

[[!redirects Martin-Löf's dependent type theory]]
[[!redirects Martin-Löf's dependent type theories]]

