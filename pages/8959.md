
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The meaning explanations of type theory

* table of contents
{: toc}

## Idea

[[Per Martin-Löf]]'s **meaning explanations of type theory** provide a way to justify the correctness of the rules of [[type theory]].  The meaning of the [[judgements]] of type theory are defined by [[computation]] of closed [[terms]] to [[canonical form]] in some untyped notion of [[computation]], such as a [[lambda calculus]] extended with constants for the [[term introduction|constructors]] and [[term elimination|eliminators]] of type theory.

From a technical/mathematical point of view, the meaning explanations give rise to a [[realizability model]] of type theory, where realizers are terms in some untyped notion of computation, such as an extended lambda calculus.  That is, it can be regarded as a description of how types are assigned to untyped computations.  However, the term "meaning explanations" also refer to the "philosophical" or "pre-mathematical" component, which regards this as an "explanation" of the "constructive validity" of the [[judgements]] of the type theory.

The standard meaning explanations validate not just the rules of [[intensional type theory]] but also the stronger rules of [[extensional type theory]].  Thus, if one regards it as the "intended [[semantics]]" then one may believe in the extensional theory.  However, like any particular semantics for a formal theory, the meaning explanation also validates many other "rules" as well which are not usually added to type theories, so it is not so clear that meaning explanations in their own right argue for extensionality.  They can also be modified so as to no longer satisfy extensionality.

Martin-L&#246;f has been quoted as saying

> Some people feel that when I have presented my meaning explanations I have said nothing.  And this is how it should be. The standard semantics should be just that: standard. It should come as no surprise.


## Definition

Suppose we have given some collection of computational objects which we call "terms", with an *untyped* notion of "reduction" or "[[computation]]".  These could be terms in a [[lambda calculus]], or elements of a [[partial combinatory algebra]], or even programs in a real-world programming language such as C, Java, or Python.
We write $x\Rightarrow y$ to mean that $x$ computes or reduces to $y$ (in some number of steps).
We then define simultaneously the following [[predicates]], where $a,b,A$ are [[terms]]:

* $A$ is a type, often written $A\;type$.
* $a$ has type $A$, written $a:A$.
* $a$ and $b$ are equal elements of type $A$, written $a=b:A$.

The definition is by [[induction-recursion]].  We define the property "$A$ is a type" *inductively*, and simultaneously we define *recursively* two functions on such $A$, one giving the collection of terms of type $A$, and the other giving the collection of pairs of terms considered equal as elements of $A$.  Note that each such collection may itself be a prior inductive definition.

The definition is intended to satisfy some properties:

* Equality:
  * $a:A$ if and only if $a=a:A$. (Reflexivity)
  * If $a=b:A$ then $b=a:A$. (Symmetry)
  * If $a=b:A$ and $b=c:A$ then $a=c:A$. (Transitivity)

* Reverse reduction:
  * If $V\;type$ and $A \Rightarrow V$ then $A\;type$.
  * The other judgment forms similarly respect reverse reduction in all positions.

By reflexivity, the specification of which terms have a type is technically redundant. It is just reiterating the reflexivity instances of equality. So for this meaning explanation, the recursive part of the definition is assigning types their meaning as [[partial equivalence relations]] (PERs) on terms.

We expect $a:A$ *if and only if* $a=a:A$, rather than just the one, usual direction because we want equality to only be defined on elements. By symmetry and transitivity, $a=b:A$ implies $a=a:A$ and $b=b:A$, so then by the unusual direction, $a:A$ and $b:A$.

The reverse reduction properties are saying that the relevant information about a term comes from the value it reduces to. Meaning explanations provide a sense in which type theory is about computational behavior. For this system, the computational behavior of a term is to return a value. Note however that not all terms reduce to a value, for example, the $\Omega$ combinator: $(\lambda x.x\,x) (\lambda x.x\,x)$.

The clauses we should include in the inductive-recursive definition depend on what type constructors we want to put into our type theory; in each case the base notion of untyped computation must include corresponding operators.  Here are three paradigmatic examples.

### Natural numbers

Suppose that we have terms $N$, $0$, and $s(x)$, along with a [[recursion|recursor]] $rec(n,z_0,x\,r. z_s)$ such that
$$\frac{n \Rightarrow 0 \qquad z_0 \Rightarrow v}
{rec(n,z_0,x\,r.z_s) \Rightarrow v}$$
and
$$\frac{n' \Rightarrow s(n) \qquad z_s[n/x,rec(n,z_0,x\,r.z_s)/r] \Rightarrow v}
{rec(n',z_0,x\,r. z_s) \Rightarrow v}.$$
The term $rec(n,z_0,x\,r. z_s)$ is intended to denote the value at $n$ of a recursively defined function specified to be $z_0$ at zero and $z_s$ at successors.  Here $x$ and $r$ are [[variables]] which may occur free in $z_s$ but are bound in $rec(n,z_0,x\,r. z_s)$, representing the predecessor and the result of the last recursive call, respectively.

Then to explain the [[natural numbers type]], we include a clause in the [[inductive definition]] of "$A$ is a type" which says

* if $A\Rightarrow N$, then $A$ is a type.

The corresponding clause for elements is

* if $A\Rightarrow N$, then the collection of terms $a$ such that $a:A$ is defined inductively by the clauses:
  * if $a\Rightarrow 0$, then $a:A$.
  * if $a\Rightarrow s(b)$ and $b:A$, then $a:A$.

Note that the recurrence in this inductive definition doesn't go via the overall recursive definition of $a:A$. In other words, to put the above clause more pedantically, we first define

* an inductive predicate $IsNat$:
  * if $a\Rightarrow 0$, then $IsNat(a)$.
  * if $a\Rightarrow s(b)$ and $IsNat(b)$, then $IsNat(a)$.

Then say

* if $A\Rightarrow N$, then the collection of terms $a$ such that $a:A$ is those such that $IsNat(a)$.

The clause for equality is

* if $A\Rightarrow N$, then the collection of pairs $a,b$ such that $a=b:A$ is defined inductively by the clauses:
  * if $a\Rightarrow 0$ and $b\Rightarrow 0$, then $a=b:A$.
  * if $a\Rightarrow s(a')$ and $b\Rightarrow s(b')$ and $a'=b':A$, then $a=b:A$.

With a similar separation of the inductive definition.

### Function types

Suppose that we have a term constructor yielding "$A\to B$" for terms $A$ and $B$, and similarly $app(f,a)$ and $\lambda x.t$, such that
$$\frac{f \Rightarrow \lambda x.t \qquad t[a/x] \Rightarrow v}
{app(f, a) \Rightarrow v}.$$
Then to explain the [[function type]], we include a clause in the inductive definition of "$A$ is a type" which says

* if $A$ is a type and $B$ is a type and $C\Rightarrow (A\to B)$, then $C$ is a type.

The clause for elements is:

* if $C\Rightarrow (A\to B)$ for types $A$ and $B$, and for any $a=a':A$ we have $app(f,a)=app(f,a'):B$, then $f:C$.  In other words, the collection of elements of type $A\to B$ is the collection of terms $f$ such that for any $a=a':A$ we have $app(f,a)=app(f,a'):B$.

For equality, we have:

* if $C\Rightarrow (A\to B)$ for types $A$ and $B$, and for any $a=a':A$ we have $app(f,a)=app(g,a'):B$, then $f=g:C$.

These are not inductive definitions as we had for the natural numbers; they are merely simple definitions.  On the other hand, we are now using the fact that the function mapping types to their collections of element pairs is recursively defined, since in order to make this definition, we must invoke it at $A$ and $B$. The negative occurrence of $a=a':A$ in this clause (and similar occurrences in other clauses for higher order types) is the reason why the whole explanation cannot just be defined by mutual induction.

This clause for function types is not the one Martin-Löf proposed. Unlike all of Martin-Löf's clauses, this one gives *all* terms of a function type directly; it doesn't just give the canonical terms first, with the rest defined via reduction. This is because it defines the elements in reference to the elimination form, $app$, instead of the introduction form, $\lambda$, as Martin-Löf did. Here's Martin-Löf's clause for elements (adapting for this non-dependent case):

* if $C\Rightarrow (A\to B)$ for types $A$ and $B$, $f \Rightarrow \lambda x.b$ for some (variable $x$ and term) $b$, and for any $a=a':A$ we have $b[a/x]=b[a'/x]:B$, then $f:C$.

The element equality clause gets an analogous change. (Exercise!)

Both styles of function type validate all the usual function rules of extensional type theory.

### Identity types

Suppose we have a term constructor yielding $Id_A(a,b)$ for terms $A,a,b$, and similarly some term $refl$.
Then to explain the [[identity type]], we add to the inductive definition of "$A$ is a type" the clause

* If $A$ is a type, $a:A$ and $b:A$, and $C \Rightarrow Id_A(a,b)$, then $C$ is a type.

Here we are finally using the fact that typehood and elements are defined by induction-recursion: this clause in the *inductive* definition of typehood refers to the value of the *recursive* elementhood function at some smaller type.

The clause for elements is:

* If $A$ is a type, $a:A$, $b:A$, and $C \Rightarrow Id_A(a,b)$, then $p:C$ just if $a=b:A$ and $p \Rightarrow refl$.  So, the collection of elements of $\Id_A(a,b)$ contains something only if $a=b:A$, in which case it contains precisely those terms which reduce to refl.

The clause for equality is:

* If $A$ is a type and $a:A$, $b:A$, and $C \Rightarrow Id_A(a,b)$, then $p=q:C$ just if $a=b:A$, $p\Rightarrow refl$, and $q\Rightarrow refl$.

Because we have deliberately only put $refl$ (and terms reducing to it) into the identity type, this definition of identity types will validate [[axiom UIP|uniqueness of identity proofs]] (UIP). Moreover, because $Id_A(a,b)$ is inhabited if and only if $a=b:A$, it validates the "equality reflection" rule of [[extensional type theory]].

There are simple ways to modify the meaning explanation so as to no longer validate the extensional rules.  For instance, if we add to the semantics additional "free variables", so that there are "neutral terms" which do not compute to any canonical form, and modify the rules of the interpretation so as to say that any normalizable neutral term inhabits every type, then extensionality will no longer hold, since the identity type (like any type) will contain all the variables.  This is maybe not a particularly compelling model of intensionality, but there are proposals for better ways to expand the meaning explanation to deal with [[intensional type theory]].

### Other judgements

#### Type equality

The easy way is to say that

* $A=B$ means that
  * $A\;type$ and $B\;type$, and
  * for all $a$, $a:A$ if and only if $a:B$, and
  * for all $a$ and $b$, $a=b:A$ if and only if $a=b:B$.

This validates the conversion rules. It's extensional in a manner similar to [[material set theory]], which seems appealing, given the rest of the setup. But it turns out to be inconvenient in this case, because for technical reasons, many rules will require more premises in order to be valid. So it's a trade-off. [[Nuprl]] uses a more intensional type equality, inductively defining $A=B$ along with $A\;type$, to simplify the rules.

#### Hypothetical judgements

TODO!

Intuitively, open terms are multi-argument dependent functions. The hypothetical judgements are defined in terms of the basic judgements on closed terms by substituting a lot of appropriate closed terms. Respect for equality is enforced in a manner to agree with the function type constructor.

### The rules of type theory

The claim is that by inspecting these definitions, one can arrive at the formal rules of [[type theory]] for manipulating judgments such as "$A$ is a type", "$a:A$", and "$a=b:A$", which no longer refer to any given notion of computation.  However, Martin-L&#246;f famously wrote

> ...there are ... certain limits to what verbal explanations can do when it comes to justifying axioms and rules of inference.  In the end, everybody must understand for himself.

Moreover, as mentioned above, the meaning explanation (like any particular semantics) validates many other "rules" which are not usually added to type theories, such as
$$ x : Id_N(0,1)  \vdash  5 : N \to N $$
(However in [[Nuprl]] rules such as these are, in fact, included.)  Thus, some discrimination is required, as well as some choices (e.g. whether to add the extensionality rule for identity types).


## References

* [[Per Martin-Löf]], _Intuitionistic Type Theory_ (Notes by Giovanni Sambin of a series of lectures given in Padua, June 1980). Napoli, Bibliopolis, 1984. ([pdf](http://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf))

* [[Per Martin-Löf]], _Constructive mathematics and computer programming_ ([pdf](http://www.cs.tufts.edu/~nr/cs257/archive/per-martin-lof/constructive-math.pdf))

* [[Per Martin-Löf]]. _On the Meanings of the Logical Constants and the Justifications of the Logical Laws_, Nordic Journal of Philosophical Logic, 1(1): 11–60, 1996 ([pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))

* [[UF-IAS-2012]], _[Meaning Explanations](https://ncatlab.org/ufias2012/published/Meaning%20Explanations)_

* [[Jonathan Sterling]], _Type Theory and its Meaning Explanations_, [arxiv](https://arxiv.org/abs/1512.01837)


Proposal for [[homotopy type theory]]:

* {#Tsementzis17} [[Dimitris Tsementzis]], _A Meaning Explanation for HoTT_ ([philsci-archive.pitt.edu/12824](http://philsci-archive.pitt.edu/12824/)))

[[!redirects meaning explanation]]
[[!redirects meaning explanations]]
[[!redirects the meaning explanation]]
[[!redirects the meaning explanations]]
[[!redirects meaning explanation of type theory]]
[[!redirects meaning explanation of type theories]]
[[!redirects meaning explanations of type theory]]
[[!redirects meaning explanations of type theories]]
[[!redirects the meaning explanation of type theory]]
[[!redirects the meaning explanations of type theory]]
[[!redirects the meaning explanation of type theories]]
[[!redirects the meaning explanations of type theories]]