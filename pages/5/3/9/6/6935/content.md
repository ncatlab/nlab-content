
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
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


#Contents#
* table of contents
{:toc}

## Idea

An _inductive type_ is...

In terms of [[categorical semantics]], an _inductive type_ is a type whose interpretation is given by an [[initial algebra of an endofunctor]].

This has the usual meaning in ordinary [[category theory]]. In applications to [[(∞,1)-category theory]], the uniqueness clause in the notion of initial object is modified to allow for a [[contractible space]] of choices (as discussed at _[[initial object in an (∞,1)-category]]_), and this difference is reflected accordingly in the type-theoretic set-up. The [[syntax]] will give back the traditional meaning whenever equality is interpreted [[extensional type theory|extensionally]].

## Definition

There are two _equivalent_ ways of defining the [[judgement]] rules for inductive types. The first describes [[term elimination|elimination]] on [[dependent types]] over the given type. This is the formalization of the notion of [[induction]], and discussed below in 

* [Induction: dependent elimination, computation](#InductionRules).

The second describes [[term elimination|elimination]] on absolute types. This is the formalization of the notion of [[recursion]], and discussed below

* [Recursion: elimination, computation](#RecursionRules)


### Induction: dependent elimination, computation
 {#InductionRules}

(...)

### Recursion: elimination, computation
 {#RecursionRules}

(...)

### Categorical semantics
 {#CategoricalSemantics}

We discuss the [[categorical semantics]] of inductive types.


+-- {: .num_defn #InterpretationOfTheRules}
###### Definition

The categorical interpretation of [[induction]], hence of the _dependent elimination_ and computation rules from [above](#InductionRules) are the following. 

Let $\mathcal{C}$ be the [[ambient category]].

1. **[[term introduction rule]]** 

   The interpretation of inductive term introduction is by an [[endofunctor]] $F : \mathcal{C} \to \mathcal{C}$ and an [[algebra over an endofunctor]], exhibited by a [[morphism]] in $\mathcal{C}$ of the form

   $$
     F(W) \to W
     \,.
   $$


1. **[[term elimination rule]]** 

   The interpretation of the dependent elimination rule says that given a [[display map]] $B \to W$, where $B$ is given an $F$-[[algebra over an endofunctor|algebra structure]] and the display map is an $F$-algebra [[homomorphism]], the dependent eliminator is interpreted as a specified [[section]] $\sigma : W \to B \in \mathcal{C}_{/W}$, hence as a [[commuting diagram]] of the form

   $$
     \array{
       W 
       &&
       \overset{\sigma}{\longrightarrow}
       && 
       B
       \\
       & 
       {}_{\mathllap{id}}\searrow 
       && 
       \swarrow_{\mathrlap{}}
       \\
       && 
       W
     }
   $$

   in $\mathcal{C}$.

1. **[[computation rule]]** 

   The interpretation of the dependent computation rules is that the section $\sigma$ from above is required to be an [[algebra for an endofunctor|algebra]] [[homomorphism]].

=--

+-- {: .num_defn #InterpretationOfTheSimpleRules}
###### Definition

The categorical interpretation of [[recursion]], hence of the absolute elimination rules from [above](#RecursionRules) in a suitable [[category]] $\mathcal{C}$ is the following

1. **[[term introduction rule]]** 

   The interpretation of inductive term introduction is by an [[endofunctor]] $F : \mathcal{C} \to \mathcal{C}$ and an [[algebra over an endofunctor]], exhibited by a [[morphism]] in $\mathcal{C}$ of the form

   $$
     F(W) \to W
     \,.
   $$

1. **[[term elimination rule]]**

   The interpretation of the absolute elimination rule is that for $A$ any other $F$-[[algebra of an endofunctor|algebra]], there is a morphism $W \to A$ in $\mathcal{C}$.

1. **[[computation rule]]**

   The interpretation of the absolute computation rule says that the morphism $W \to A$ from above is an algebra [[homomorphism]] and is unique as such.

In summary this says that the recursion rules are interpreted as an [[initial algebra of an endofunctor]].

=--



+-- {: .num_prop #BothFormulationsOfInitialityAreEquivalent}
###### Proposition

When interpreted in a category $\mathcal{C}$ of [[homotopy type|homotopy 0-types]] = sets,
definition \ref{InterpretationOfTheRules}
and
definition \ref{InterpretationOfTheSimpleRules}
are indeed equivalent.

=--

+-- {: .proof}
###### Proof

First suppose that $W$ is an initial $F$-algebra as in def. \ref{InterpretationOfTheSimpleRules}. Then since [[initial object|initiality]] entails first of all the existence of a morphims to any other object it follows that with $B$ another $F$-algebra there is a homomorphism $W \to B$, and since secondly initiality entails uniqueness of this morphism, it follows that given a homomorphism $B \to W$ the composite $W \to B \to W$ has to equal the identity $id_W$, hence that $B \to W$ has a section, and uniquely so.

Conversely, assume that $W$ satisfies definition \ref{InterpretationOfTheRules}.
For $A$ any other $F$-algebra we can form the trivial display map $W \times A \to W$ by [[projection]] and a [[section]] of this is equivalently just a morphism $W \to A$,  so we have a homomorphism from $W$ to any other $F$-algebra $A$. Therefore to show that $W$ is an initial $F$-algebra it remains to show that for $f, g : W \to A$ two algebra homomorphism, they are necessarily equal.

To that end, notice that by the assumption of 0-truncation, the [[diagonal]]  $\delta \colon A \to A \times A$ is a display map / fibration. 

Form its [[pullback]] $P$ 

$$
  \array{
    P & \to & A 
    \\
    \downarrow & & \downarrow^\mathrlap{\delta} 
    \\
    W & \underset{\langle f, g \rangle}{\to} & A \times A,
  }
  \,,
$$ 

which is also an algebra homomorphism. Therefore by the interpretation of the elimination rule it has a (specified) [[section]] $\sigma : W \to P$. But $P \to W$ is the pullback of a [[monomorphism]] and therefore itself a monomorphism, and so the section forces it to be in fact an [[isomorphism]]. This in turn means that $f$ and $g$ are equal. 

=--


+-- {: .num_remark }
###### Remark

In [[intensional type theory]], where the diagonal is not a display map, we can perform the same argument using a [[path object]] $P A \to A \times A$ (represented in type theory by an [[identity type]]), showing thereby that $f$ and $g$ are homotopic.  A fancier version of this argument enables us to show that the space of algebra maps $W\to A$ is actually contractible. In other words, the axioms for an inductive type still imply that algebra maps out of $W$ are essentially unique, even though the axioms do not state this explicitly. 

=--


## Properties

### Homotopy initiality

Any inductive type $W$ is a homotopy initial F-[[algebra over an endofunctor|algebra]]: 
the space
of $F$-[[algebra for an endofunctor|algebra]] maps $W \to X$ is 
[[contractible]].

&lbrack;[Awodey, Gambino & Sojakova (2012)](#AwodeyGambinoSojakova12)&rbrack;

## Examples
 {#Examples}

> In the first examples to follow, the [[computation rules]] are written with ordinary equality signs "=". At least for extensional inductive types these are [[judgemental equalities]].

\linebreak 

### Empty type
 {#ExamplesEmptyType}


The inductive [[inference rules]] for the [[empty type]]:


**[[type formation rule]]:**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \varnothing \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]:**

$$
\text{--- none ---}
$$

\linebreak

**[[term elimination rule]]:**

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

**[[computation rule]]:**

$$
\text{--- none ---}
$$


### Unit type
 {#UnitType}

The inductive [[inference rules]] for the [[unit type]]:


**[[type formation rule]]:**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \ast \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]:**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    pt \,\colon\, \ast
  }
$$

\linebreak

**[[term elimination rule]]:**

$$
  \frac{
    x \,\colon\, \ast
    \;\vdash\;\;
    D(x) \,:\, Type
    \;;
    \;\;\;
    pt_D \,\colon\, D(pt)
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{(D,\,pt_D)}
    \,\colon\,
    \underset{x \colon \ast}{\prod}
    D(x)
  }
$$

\linebreak

**[[computation rule]]:**

$$
  ind_{(D,\,pt_D)}(pt)
  \;=\;
  pt_D
$$


\linebreak


### Booleans
 {#Booleans}

The [[inference rules]] for the [[type of booleans]]:

\linebreak

**[[type formation rule]]:**

$$
  \frac{
  }{
    Bit \,\colon\, Type
  }
$$

\linebreak

**[[term introduction rule]]:**

$$
  \frac{ 
  }{
    0 \,\colon\, Bit
  }
  \;\;\;\;\;
  \frac{ 
  }{
    1 \,\colon\, Bit
  }
$$

\linebreak

**[[term elimination rule]]:**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    ind_{(P,\,0_P,\,1_P)} 
      \,\colon\, 
    \underset{b \colon Bit}{\prod} P(b)
  }
$$

\linebreak

**[[computation rules]]:**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    \begin{array}{l}
    ind_{(P,\,0_P,\,1_P)}(0) \;=\; 0_P
    ;\;
    \\
    ind_{(P,\,0_P,\,1_P)}(1) \;=\; 1_P
    \end{array}
  }
$$

See at *[[type of booleans]]*


\linebreak


### Natural numbers
 {#NaturalNumbers}

The inductive [[inference rules]] for the [[natural numbers type]]:

\linebreak

1. **[[type formation rule]]**:

   $$
     \frac{}{
       \mathclap{\phantom{\vert^{\vert}}}
       \mathbb{N} \,\colon\, Type
     }
   $$

2. **[[term introduction rules]]**:

   $$
     \frac{}{
       \mathclap{\phantom{\vert^{\vert}}}
       0 \,\colon\, \mathbb{N}
     }
     \;\;\;\;\;\;\;\;
     \frac{
       n \,\colon\, \mathbb{N}
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       succ(n) \,\colon\, \mathbb{N}
     }
   $$

3. **[[term elimination rule]]**:

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
         \;\vdash\; 
       P(n) \,\colon\, Type
       \;;
       \;\;\;\;
       \vdash\; 0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,,
       \; 
       p \,\colon\, P(n) 
         \;\vdash\; 
       succ_P(n,\,p) \,\colon\, P\big(succ(n)\big)
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       n \,\colon\, \mathbb{N}
       \;\vdash\;
       ind_{(P, 0_P, succ_P)}(n)
        \,\colon\, 
       P(n)
     }
   $$
   
4. **[[computation rules]]**:

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
        \;\vdash\;  
       P(n) \,\colon\, Type
       \;;
       \;\;\;\;
         \vdash\; 
       0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,, 
       \;
       p \,\colon\, P(n) 
         \;\vdash\; 
       succ_P(n,p) \,\colon\, P\big(succ(n)\big)
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       ind_{(P, 0_P, succ_P)}(0)
        \,=\, 
       0_P 
     }
   $$

   and

   $$
     \frac{
       n \,\colon\, \mathbb{N} 
         \;\vdash\;  
       P(x) \,\colon\, Type
       \;;
       \;\;\;\;
       \vdash\; 0_P \,\colon\, P(0)
       \;;
       \;\;\;\;
       n \,\colon\, \mathbb{N}
       \,, 
       \;
       p \,\colon\, P(n) 
         \;\vdash\; 
       succ_P(n,p) \,\colon\, P(s n)
       \;;
       \;\;\;\;
       \vdash\; n \,\colon\, \mathbb{N}
       \mathclap{\phantom{\vert_{\vert}}}
     }{
       \mathclap{\phantom{\vert^{\vert}}}
       ind_{(P, 0_P, succ_P)}\big(succ(n)\big)
       \,=\, 
       succ_P\big(n,\, ind_{(P, 0_P, succ_P)}(n) \big) 
     }
   $$


\linebreak

### Lists

If $X$ is any set, then the inductive type $L X$ of [[lists]] of elements of $X$ has $|X|+1$ constructors:

* $nil$ of arity zero, and
* $cons(x,-)$ of arity one, for each $x\in X$.

Therefore, $nil$ is a list, $cons(x,\ell)$ is a list for any list $\ell$ and $x\in X$, and all lists are generated in this way.


### Identity types
 {#IdentityTypes}

The introduction, elimination and computation rules for _[[identity types]]_ are discussed there.

In [[Coq]]-[[syntax]] the [[identity types]] are the inductive types (or more precisely, the _[[inductive family]]_) defined by

    Inductive id {A} : A -> A -> Type := 
      idpath : forall x, id x x.

#### Categorical semantics

We may [[categorical semantics|interpret]] identity types in suitable categories $\mathcal{C}$ such as a [[type-theoretic model category]].

+-- {: .num_example #EndofunctorForIdentityTypes}
###### Example

The [[categorical semantics|categorical interpretation]] of identity types in a category $\mathcal{C}$ is as  the [[initial algebra of an endofunctor|initial algebra]] for the [[endofunctor]] 

$$
  F : \mathcal{C}_{/A \times A} \to 
  \mathcal{C}_{/A \times A}
$$

of the [[slice category]] $\mathcal{C}_{/A \times A}$ over $A\times A$ which is constant at the [[diagonal]] $A\to A\times A$:

$$
  F (\langle E \to A \times A\rangle) = \langle A \stackrel{\Delta}{\to} A \times A\rangle
  \,.
$$

=--

So an [[algebra for an endofunctor|algebra]] for this endofunctor is a morphism

$$
  \array{
    A &&\to&& E
    \\
    & {}_{\mathllap{\Delta}}\searrow && \swarrow
    \\
    && A \times A
  }
$$

and the [[initial object|initial]] such is the [[path space object]] $A^I \to A \times A$.

#### Path induction
 {#PathInduction}


+-- {: .num_example}
###### Example

We spell out in detail how the the [[induction principle]] def. \ref{InterpretationOfTheRules} for identity types is the [[principle of substitution of equals for equals]].

To have an $F$-algebra $\langle E \to A\times A\rangle$ over $\langle A^I \to A \times A\rangle$ means precisely to have a diagram

$$
  \array{
    && E 
    \\
    & \nearrow& \downarrow
    \\
    A &\to& A^I
    \\
    &\searrow& \downarrow
    \\
    && A \times A
  }
$$
 
in $\mathcal{C}$.

This is the interpretation of the elimination rule: $E \to A^I$ is the interpretation of a type 

$$
  a,b \in A , p : (a = b) \vdash E(a,b,p)
$$

and the lift $A \to E$ is a [[section]] of the [[pullback]] of $E$ to $A$, hence an interpretation of a [[term]] in the [[substitution]]

$$
  s : E(a,a,r_a)
  \,.
$$

The elimination rule then says that this extends to a section $A^I \to E$, hence a "proof of $E$ over all identifications" $a = b$.

=--

#### Path recursion
 {#PathRecursion}

+-- {: .num_example}
###### Example

We spell out how the the [[recursion principle]] def. \ref{InterpretationOfTheSimpleRules} for [[identity types]] is related to the _[[complete Segal space|Segal-completeness condition]]_ and in particular to _[[univalence]]_. 

Notice that an [[algebra for an endofunctor|algebra over the endofunctor]] that defines identity types, example \ref{EndofunctorForIdentityTypes},

$$
  \array{
     X_0 &&\stackrel{\sigma_0}{\to}&& X_1
     \\
     & \searrow && \swarrow_{\mathrlap{\delta_0, \delta_1}}
     \\
     && X_0 \times X_0
  }
$$

constitutes the [[simplicial skeleton|1-skeleton]] of a [[simplicial object]]

$$
  \array{
     X_1
     \\
     {}^{\mathllap{\delta_0}}\downarrow \uparrow^{\mathrlap{\sigma_0}} \downarrow^{\mathrlap{\delta_1}}
     \\   
     X_0
  }
  \,.
$$

The [[recursion principle]] says that the [[simplicial identities|degeneracy map]] $\sigma_0$ factors through the [[path space object]] of $X_0$ as a lift $\hat \sigma_0$ in the diagram

$$
  \array{
     X_0 &\stackrel{\sigma_0}{\to}& X_1
     \\
     \downarrow &\nearrow_{\hat \sigma_0}& \downarrow
     \\
     X_0^I &\to& X_0 \times X_0
  }
  \,.
$$

[[categorical semantics|Semantically]], this lift exists because $X_0 \to X_0^I$ is an [[acyclic cofibration]] by definition of [[path space object]], and $X_1 \to X_0 \times X_0$ is a [[fibration]] ([[display map]]) by the interpretation rule for [[dependent types]].

This morphism 

$$
  \hat \sigma_0 : X_0^I \to X_1
$$

lifts paths/[[morphisms]] that exist in $X_0$ to the morphisms exhibited by $X_1$, if we think of the above as the 1-skeleton of a simplicial object that represents an [[internal category in an (infinity,1)-category]].

Suppose this exists, then there will be a notion of _equivalences_ in $X_1$, those morphisms that are invertible with respect to the given composition operation. In good situations this will give the [[core]] inclusion

$$
  Core(X_1) \hookrightarrow X_1
  \,.
$$

In this case the [[complete Segal space|Segal-completeness condition]] in degree 1 says that the path recursion $\hat \sigma_0$ exhibits this inclusion

$$
  \hat \sigma_0 : X_0^I \simeq Core(X_1) \to X_1
  \,.
$$

In the case that $X_\bullet$ is the classifier of the [[codomain fibration]], then this is called the _[[univalence]]-condition_.

=--



### W-types

* [[W-type]]


## Related concepts

* [[initial algebra of an endofunctor]]

* [[inductive-inductive type]]

* [[inductive family]]

* [[positive type]], [[negative type]]

* [[higher inductive type]], [[initial algebra of a presentable ∞-monad]]

* [[coinductive type]]



## References
 {#References}




[[!include history of inductive types -- references]]




### Introduction and review
    
Textbook accounts:

* [[Simon Thompson]], §4.10 in: *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)&rbrack;

* [[Adam Chlipala]], §3 of: _Certified programming with dependent types_, MIT Press 2013 &lbrack;[ISBN:9780262026659 ](https://mitpress.mit.edu/books/certified-programming-dependent-types), [pdf](http://adam.chlipala.net/cpdt/cpdt.pdf),  [book webpage](http://adam.chlipala.net/cpdt/)&rbrack;

  > (discussion for the *[[Coq]]* [[proof assistant]])

* [[Robert Harper]], §15 in: _[[Practical Foundations for Programming Languages]]_, Cambridge University Press (2016) &lbrack;[ISBN:9781107150300](http://www.cambridge.org/us/academic/subjects/computer-science/programming-languages-and-applied-logic/practical-foundations-programming-languages-2nd-edition?format=HB), [pdf](https://www.cs.cmu.edu/~rwh/pfpl/2nded.pdf)&rbrack;


See also:

* Wikipedia, *[Inductive types](https://en.wikipedia.org/wiki/Inductive_type)*

Exposition with an eye towards explaining [[identity types]] in [[Martin-Löf type theory]]/[[homotopy type theory]]:

* [[Mike Shulman]], _Induction on equality_ (2011) &lbrack;[pdf](http://home.sandiego.edu/~shulman/papers/induction.pdf), [[Shulman-Induction.pdf:file]]&rbrack;


Formalization in [[proof assistants]]:

in [[Coq]]:

* Eduardo Gim&#233;nez, Pierre Cast&#233;ran, _A Tutorial on [Co-]Inductive Types in Coq_ (1998, 2005) &lbrack;[pdf](http://flint.cs.yale.edu/cs428/coq/pdf/RecTutorial.pdf), [[GimenezCasteran-InductiveTypes.pdf:file]]&rbrack;

in [[Lean]]:

* [Inductive types](https://leanprover.github.io/theorem_proving_in_lean/inductive_types.html), §7 in: *[Theorem Proving in Lean](https://leanprover.github.io/theorem_proving_in_lean/index.html)*

On inductive types in the context of [[linear type theory]]:

* St&#233;phane Gimenez, _Towards Generic Inductive Constructions in Systems of Nets_ &lbrack;[pdf](https://www.imn.htwk-leipzig.de/~waldmann/WST2013/papers/paper_16.pdf)&rbrack;


Expositions with an eye towards [[higher inductive types]]:

* [[Mike Shulman]], _Homotopy type theory IV_ ([web](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html))

* [[Peter LeFanu Lumsdaine]], _Higher inductive types, a tour of the menagerie_ ([blog post](http://homotopytypetheory.org/2011/04/24/higher-inductive-types-a-tour-of-the-menagerie/))

* [[Mike Shulman]], _Inductive and higher inductive types_, talk slides (2012) ([pdf](http://www.sandiego.edu/~shulman/hottminicourse2012/04induction.pdf))

Discussion of homotopy-initiality of inductive types in [[homotopy type theory]] (cf. also at *[[higher inductive type]]*):

* {#AwodeyGambinoSojakova12} [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], *Inductive types in homotopy type theory*, LICS'12: (2012) 95–104 &lbrack;[arXiv:1201.3898](http://arxiv.org/abs/1201.3898), [doi:10.1109/LICS.2012.21](https://doi.org/10.1109/LICS.2012.21), [Coq code](https://github.com/HoTT/HoTT/tree/master/Coq/IT)&rbrack;
 
  \linebreak
 
  Exposition: 

  [[Steve Awodey]], *Inductive types in HoTT* (Jan 2012) &lbrack;[blog post](http://homotopytypetheory.org/2012/01/19/inductive-types-in-hott/)&rbrack;





[[!include semantics of W-types -- references]]





 

[[!redirects inductive type]]
[[!redirects inductive types]]
[[!redirects inducive type]]

