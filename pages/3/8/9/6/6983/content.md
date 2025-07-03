
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

In [[type theory]] the _unit type_ is the [[type]] with a unique [[term]].  It is the special case of a [[product type]] with no factors. 

In a [[model]] by [[categorical semantics]], this is a [[terminal object]]. In [[set theory]], it is a [[singleton]].


## Definition

Like any [[type]] in [[type theory]], the unit type is specified by rules saying when we can [[type formation|introduce it as a type]], how to  [[term introduction|introduce terms]] of that type, how to use or [[term elimination|eliminate terms]] of that type, and how to [[computation rule|compute]] when we combine the constructors with the eliminators. 

The unit type, like the binary [[product type]], can be presented both as a [[positive type]] and as a [[negative type]]. There are typically two foundations in which the unit type is specified in, [[natural deduction]] and [[lambda-calculus]]. 

### In natural deduction

We assume that our unit types have typal [[conversion rules]], as those are the most general of the conversion rules. Both the propositional and judgmental conversion rules imply the typal conversion rules by the structural rules for propositional and judgmental equality respectively. 

For both the positive unit type and the negative unit type, the formation and introduction rules are the same. 

The [[formation rule]] for the unit type is given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

and the [[introduction rule]] for the unit type is given by

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash *:\mathbb{1}}$$

The positive unit type says that $\mathbb{1}$ satisfies [[singleton induction]]. The negative unit type says that the element $*:\mathbb{1}$ is the [[center of contraction]] of $\mathbb{1}$. 

#### As a positive type

[[singleton induction|Singleton induction]] for a type $\mathbb{1}$ and term $*:\mathbb{1}$ states that the type has the following [[elimination rule]], [[computation rule]], and [[uniqueness rule]]:

* given a type family $C(x)$ indexed by $\mathbb{1}$, for all elements $x:\mathbb{1}$ and $c:C(*)$, there is an element $\mathrm{ind}_\mathbb{1}^C(x, c):C(x)$. 

$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type}}{\Gamma, x:\mathbb{1}, c:C(*) \vdash \mathrm{ind}_\mathbb{1}^C(x, c):C(x)}$$

* given a type family $C(x)$ indexed by $\mathbb{1}$, for all elements $c:C(*)$, the element $\mathrm{ind}_\mathbb{1}^C(*, c)$ derived from the elimination rule is equal to $c$ with witness $\beta_\mathbb{1}^C(c)$. 

$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type}}{\Gamma, c_*:C(*) \vdash \beta_\mathbb{1}^C(c):\mathrm{ind}_\mathbb{1}^C(*, c) =_{C(*)} c}$$

* given a type family $C(x)$ indexed by $\mathbb{1}$ and a family of elements $u(x):C(x)$ indexed by $\mathbb{1}$, for all elements $x:\mathbb{1}$ there is a witness $\eta_\mathbb{1}^C(x, u(x))$ that $u(x)$ is equal to $\mathrm{ind}_\mathbb{1}^{C}(x, u(*))$ in $C(x)$.

$$\frac{\Gamma, x:\mathbb{1} \vdash C(x) \; \mathrm{type} \quad \Gamma, x:\mathbb{1} \vdash u(x):C(x)}{\Gamma, x:\mathbb{1} \vdash \eta_\mathbb{1}^C(x, u(x)):u(x) =_{C(x)} \mathrm{ind}_\mathbb{1}^{C}(x, u(*))}$$

Thus, the unit type satisfies [[singleton induction]]. 

In type theories with a separate type judgment where not all types are elements of universes, one has to additionally add the following elimination and computation rules:

Elimination rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:\mathbb{1} \vdash \mathrm{typerec}_{\mathbb{1}}^{A}(x) \; \mathrm{type}}$$

Computation rules:

* judgmental computation rules

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{typerec}_{\mathbb{1}}^{A}(*) \equiv A \; \mathrm{type}}$$

* typal computation rules
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \beta_{\mathbb{1}}^{A}:\mathrm{typerec}_{\mathbb{1}}^{A}(*) \simeq A}$$

#### As a negative type

As a negative type, there are no [[elimination rules]] or [[computation rules]] for $\mathbb{1}$. The [[uniqueness rule]] states that $*$ is the [[center of contraction]] of $\mathbb{1}$ and is given by:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, p:\mathbb{1} \vdash \eta_\mathbb{1}(p):* =_\mathbb{1} p}$$

Thus, the unit type is a [[contractible type]]. 

#### Positive versus negative

\begin{theorem}
Let $\mathbb{1}$ denote the positive unit type, and let $p:\mathbb{1}$ and $q:\mathbb{1}$ be elements of $\mathbb{1}$. Then the identity type $q =_\mathbb{1} p$ is a [[contractible type]]. 
\end{theorem}

\begin{proof}
Given an element $p:\mathbb{1}$, we can define the family of types $C(q) \coloneqq q =_\mathbb{1} p$ for all $q:\mathbb{1}$. The elimination and computation rules for the positive unit type imply that $* =_\mathbb{1} p$ is a [[contractible type]] with [[center of contraction]] $c_*(p):* =_\mathbb{1} p$ which is equal to $\mathrm{ind}_\mathbb{1}^{(-) =_\mathbb{1} p}(p, c_*(p))$. 

The uniqueness rule for the positive unit type states that given a family of terms $u(p):q =_\mathbb{1} p$ indexed by $p:\mathbb{1}$ and $q:\mathbb{1}$, for all elements $c_*(p):* =_\mathbb{1} p$, elements $q:\mathbb{1}$, and witnesses $i_*(u(p))$ that $u(p)(*)$ is equal to $c_*(p)$ in $* =_\mathbb{1} p$, there is a witness $\eta_\mathbb{1}^{(-) =_\mathbb{1} p}(c_*(p), q, u(p), i_*(u(q)))$ that $u(p)$ is equal to $\mathrm{ind}_\mathbb{1}^{(-) =_\mathbb{1} p}(p, c_*(p))$ in $C(p)$.

Thus, the identity type $q =_\mathbb{1} p$ is a [[contractible type]] for all elements $p:\mathbb{1}$ and $q:\mathbb{1}$, with element $\eta_\mathbb{1}^{(-) =_\mathbb{1} p}(c_*(p), q, u(p), i_*(u(q))):q =_\mathbb{1} p$. 
\end{proof}

\begin{lemma}
The positive unit type is a contractible type. 
\end{lemma}

\begin{proof}
Since the identity type $q =_\mathbb{1} p$ is a [[contractible type]] for all elements $p:\mathbb{1}$ and $q:\mathbb{1}$, with element $\eta_\mathbb{1}^{(-) =_\mathbb{1} p}(c_*(p), q, u(p), i_*(u(q))):q =_\mathbb{1} p$, it follows that $\mathbb{1}$ is an [[h-proposition]]. Since $\mathbb{1}$ is also pointed with element $*:\mathbb{1}$, it is thus a [[contractible type]]. 
\end{proof}

\begin{theorem}
There is an [[equivalence of types]] between two [[contractible types]] $S$ and $T$. 
\end{theorem}

\begin{proof}
By the definition of [[contractible type]], there are elements $p_S:\sum_{a:S} \prod_{b:S} a =_S b$ and $p_T:\sum_{a:T} \prod_{b:T} a =_T b$, and thus, an element $\pi_1(p_S)$ and a witness $\pi_2(p_S)$ that $\pi_1(p_S)$ is a [[center of contraction]] of $S$, and an element $\pi_1(p_T)$ and a witness $\pi_2(p_T)$ that $\pi_1(p_T)$ is a [[center of contraction]] of $T$. By the uniqueness principle of contractible types, it suffices to define a function $f:S \to T$ at $\pi_1(p_S)$. We define it as $f(\pi_1(p_S)) \coloneqq \pi_1(p_T)$. Now, all that's left is to prove that the fiber of $f$ at all elements $a:T$ is contractible. But by the uniqueness principle of contractible types, it suffices to prove it for the center of contraction $\pi_1(p_T)$. The canonical element $*$ is in the fiber of $f$ at $\pi_1(p_T)$, and since $\pi_1(p_S)$ is the center of contraction of $S$, the fiber of $f$ at $\pi_1(p_T)$ is contractible, and thus the fiber of $f$ at every element $a:T$ is contractible. Thus, $f$ is an equivalence of types between the contractible types $S$ and $T$. 
\end{proof}

\begin{lemma}
The positive and negative unit types are equivalent to each other. 
\end{lemma}

\begin{proof}
Since the negative unit type is contractible by definition, and the positive unit type is contractible, they are equivalent to each other. 
\end{proof}

#### Extensionality principle

Then we could derive the extensionality principle for the unit type:

\begin{lemma}
Given elements $x:\mathbb{1}$ and $y:\mathbb{1}$, there is an [[equivalence of types]] $(x =_\mathbb{1} y) \simeq \mathbb{1}$ between the [[identity type]] $x =_\mathbb{1} y$ and $\mathbb{1}$ itself. 
\end{lemma}

\begin{proof}
Since every identity type $x =_\mathbb{1} y$ is contractible for elements $x:\mathbb{1}$ and $y:\mathbb{1}$, and $\mathbb{1}$ itself is contractible, this implies that every identity type $x =_\mathbb{1} y$ is equivalent to $\mathbb{1}$. 
\end{proof}

#### The unit type as a univalent universe

In [[set theory]], regular and inaccessible cardinals are useful in determining [[size issues]] in [[strongly predicative]] and [[weakly predicative]]/[[impredicative]] mathematics respectively. Some definitions of regular and inaccessible cardinals do not have a requirement that the cardinals be infinite; thus finite cardinals such as $0$ and $1$ could be considered to be regular and inaccessible cardinals. Univalent universes in type theory which are closed under [[dependent sum types]] are the type theoretic equivalent of [[regular cardinals]], and univalent universe which are additionally closed under [[power sets]] are the type theoretic equivalent of [[inaccessible cardinals]]. 

We [[inductive definition|inductively define]] the type family $x:\mathbb{1} \vdash \mathrm{El}_\mathbb{1}(x) \; \mathrm{type}$ by defining 
$$\mathrm{El}_\mathbb{1}(*) \coloneqq \mathbb{1}$$
The extensionality principle for the unit type then is simply the [[univalence axiom]]:
$$\mathrm{ext}_\mathbb{1}:\prod_{x:\mathbb{1}} \prod_{y:\mathbb{1}} (x =_\mathbb{1} y) \simeq (\mathrm{El}_\mathbb{1}(x) \simeq \mathrm{El}_\mathbb{1}(y))$$
The unit type $\mathbb{1}$ represents the trivial universe, the universe with only one element up to identification, where every type in the universe is a [[contractible type]] and thus every contractible type is [[essentially small type|essentially $\mathbb{1}$-small]]. The [[equivalence type]] between the two contractible types $\mathrm{El}_\mathbb{1}(x)$ and $\mathrm{El}_\mathbb{1}(y)$ is itself contractible and thus equivalent to $\mathbb{1}$ itself. As proven in the previous section, $\mathbb{1}$ is equivalent to $x =_\mathbb{1} y$ for any $x:\mathbb{1}$ and $y:\mathbb{1}$. Thus the univalence axiom for $\mathbb{1}$ is true. 

In addition, given any type $A$, functions into the unit type $A \to \mathbb{1}$ are families of [[contractible types]]. The universe $(\mathbb{1}, \mathrm{El}_\mathbb{1})$ is also closed under [[dependent sum types]], as for any family of contractible types $p:B \to \mathbb{1}$,
$$\left(\sum_{x:\mathbb{1}} \mathrm{El}_\mathbb{1}(B(x))\right) \simeq \mathbb{1}$$
This makes the unit type into a [[Tarski universe]] representing a finite regular cardinal. 

If the [[dependent type theory]] also has [[weak function extensionality]], then the universe above is also closed under [[dependent product types]], as weak function extensionality states that for any family of contractible types $p:B \to \mathbb{1}$,
$$\left(\prod_{x:\mathbb{1}} B(x)\right) \simeq \mathbb{1}$$
making the unit type into a [[Tarski universe]] representing a finite [[product-regular cardinal]]. 

As a universe, the unit type also satisfies [[propositional resizing]]: the type of all $\mathbb{1}$-small propositions is simply the unit type itself as a [[weakly Tarski universe]], which is essentially $\mathbb{1}$-small. Thus, in the context of [[weak function extensionality]], [[power sets]] exist in the unit type, making the unit type impredicative: power sets are just [[function types]] into the unit type. This makes the unit type into a [[Tarski universe]] representing a finite [[inaccessible cardinal]]. 

The unit type is also the only universe which contains itself, as any univalent universe which contains the [[empty type]] and itself makes the entire [[dependent type theory]] inconsistent. 

### In lambda-calculus 

In lambda-calculus, for both the positive unit type and the negative unit type, the rule for building the unit type is the same, namely "it exists":

$$ \frac{ }{1\colon Type} $$

#### As a positive type

Regarded as a [[positive type]], we give primacy to the constructors, of which there is exactly one, denoted $()$ or $tt$.

$$ \frac{ }{() \colon 1 } $$

The eliminator now says that to use something of type $1$, it suffices to say what to do in the case when that thing is $()$.

$$ \frac{\vdash c\colon C}{u\colon 1 \vdash let () = u in c \;\colon C}$$

Obviously this is not very interesting, but this is what we get from the general rules of type theory in this degenerate case.  In [[dependent type theory]], we should also allow $C$ to depend on the unit type $1$.

We then have the [[∞-reduction]] rule:

$$ let () = () in c \;\to_\beta\; c$$

and (if we wish) the [[∞-reduction]] rule:

$$ let () = u in c[()/z] \;\to_\eta\; c[u/z]. $$

The $\beta$-reduction rule is simple.  The $\eta$-reduction rule says that if $c$ is an expression involving a variable $z$ of type $1$, and we substitute $()$ for $z$ in $c$ and use that (with the eliminator) to define a term involving another term $u$ of type $1$, then the result is the same as what we would get by substituting $u$ for $z$ in $c$ directly.

The positive presentation of the unit type is naturally expressed as an [[inductive type]].  In [[Coq]] syntax:

    Inductive unit : Type :=
    | tt : unit.

(Coq then implements beta-reduction, but not eta-reduction. However, eta-equivalence is provable with the internally defined [[identity type]], using the dependent eliminator mentioned above.)

#### As a negative type

A [[negative type]] is characterized by its eliminators, which is a little subtle for the unit type.  But by analogy with binary [[product types]], which have two eliminators $\pi_1$ and $\pi_2$ when presented negatively, the negative unit type (a [[zero|nullary]] product) should have *no eliminators at all*.

To derive the constructors from this, we follow the general rule for negative types that to construct an element of $1$, it should suffice to specify how that element behaves under all the eliminators.  Since there *are* no eliminators, this means we have nothing to do; thus we have exactly one way to construct an element of $1$, by doing nothing:

$$\frac{ }{()\colon 1}$$

There is no $\beta$-reduction rule, since there are no eliminators to compose with the constructor.  However, there *is* an $\eta$-conversion rule.  In general, an $\eta$-[[redex]] consists of a constructor whose inputs are all obtained from eliminators.  Here we have a constructor which has no inputs, so it is not a problem that we have no eliminators to fill them in with.  Thus, the term $()\colon 1$ is an "$\eta$-redex", and it "reduces" to *any* term of type $1$ at all:

$$ () \;\to_\eta\; u$$

This is obviously not a well-defined "operation", so in this case it is better to view $\eta$-conversion in terms of *expansion*:

$$ u \;\to_\eta\; ().$$

#### Positive versus negative

In ordinary "nonlinear" type theory, the positive and negative unit types are equivalent.  They manifestly have the same constructor, while we can define the positive eliminator in a trivial way as

$$ let () = u in c  \quad \coloneqq\quad c $$

Note that just as for binary [[product types]], in order for this to be a well-typed definition of the *dependent* eliminator in dependent type theory, we need to assume the $\eta$-conversion rule for the assumed negative unit type (at least, [propositionally](/nlab/show/eta-conversion#Propositional)).

Of course, the positive $\beta$-reduction rule holds by definition for the above defined eliminator.

For the $\eta$-conversion rules, if we start from the negative presentation and define the positive eliminator as above, then $let () = u in c[()/z]$ is precisely $c[()/z]$, which is convertible to $c[u/z]$ by the negative $\eta$-conversion rule $() \;\leftrightarrow_\eta\; u$.

Conversely, if we start from the positive presentation, then we have

$$
  ()
  \;\leftrightarrow_\eta\; let () = u in ()
  \;\leftrightarrow_\eta\; u
$$

where in the first conversion we use $c \coloneqq ()$ and in the second we use $c\coloneqq z$.

As in the case of binary [[product types]], these translations require the [[contraction rule]] and the [[weakening rule]]; that is, they duplicate and discard terms.  In [[linear logic]] these rules are disallowed, and therefore the positive and negative unit types become different.  The positive product becomes "one" $\mathbf{1}$, while the negative product becomes "top" $\top$.

## Categorical semantics

There are two interpretations of the unit type, corresponding to the positive and negative unit types. Namely:

* The negative unit type corresponds to a [[terminal object]] in a category

* The positive unit type with both $\beta$-conversion and $\eta$-conversion corresponds to an [[initial object]] with a point, a morphism from some unit object $I$ to the object corresponding to the unit type, in a category. 

These two conditions are the same if the [[syntactic category]] is a [[cartesian monoidal category]], where the points are the [[global elements]] and the [[unit]] is the [[terminal object]]. In general, however, the points may not be defined out of the terminal object. In [[linear logic]], therefore, the categorical terminal object interprets "top" $\top$, while the unit object of an additional [[monoidal category|monoidal structure]] interprets "one" $\mathbf{1}$.


## Related concepts

* [[product type]]
* [[empty type]]
* [[contractible type]]

## References

On the unit type as an [[inductive type]] satisfying [[singleton induction]]:

* [[Univalent Foundations Project]], p. 30 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Egbert Rijke]], Def. 3.1.1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;


[[!include homotopy n-types - table]]



[[!redirects unit type]]
[[!redirects unit types]]

[[!redirects strict unit type]]
[[!redirects strict unit types]]

[[!redirects weak unit type]]
[[!redirects weak unit types]]

[[!redirects positive unit type]]
[[!redirects positive unit types]]

[[!redirects positive strict unit type]]
[[!redirects positive strict unit types]]

[[!redirects positive weak unit type]]
[[!redirects positive weak unit types]]

[[!redirects negative unit type]]
[[!redirects negative unit types]]

[[!redirects negative strict unit type]]
[[!redirects negative strict unit types]]

[[!redirects negative weak unit type]]
[[!redirects negative weak unit types]]

[[!redirects trivial type]]
[[!redirects trivial types]]
