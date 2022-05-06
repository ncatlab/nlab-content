# Initiality Project - Raw Syntax


This page is part of the [[Initiality Project]].

* table of contexts
{:toc}

## Idea

Here we define the "raw syntax" for our type theory.  These are sets whose elements are called "raw terms" and "raw types".  They are obtained by putting together operations like "$\Sigma$-types" and "$\lambda$-abstraction" in a way that "makes sense locally" but not necessarily globally.

In traditional approaches to logic, one often defines the raw terms (or "well-formed formulas") as a subset of the set of all "strings", i.e. finite lists of elements of some "alphabet" set such as $\{\Sigma,\Pi,\lambda,(,),:,\dots \}$.  Note that parentheses, colons, commas, and so on are all symbols in the alphabet.  In addition, this point of view requires us to alter some of the clauses to include extra parentheses, e.g. we have to write $(A\times B)$ so that $((A\times B)\times C)$ has an unambiguous meaning.

However, a more modern perspective is to regard this as defining an [[inductive type]] (in the metatheory), with each clause as a constructor.  In this case, the raw terms themselves are not lists of symbols with some property, but rather *trees* whose nodes are labeled with appropriate symbols.  This way we obtain automatically an induction principle for defining functions by recursion and proving theorems by induction over the set of terms, which in the strings-of-symbols approach one has to prove by hand.  The strings of symbols we write on the page like $(A\times B)\times C$ are then regarded as just a *notation* for these "abstract syntax trees".

It's true that to be completely precise about the *entire* passage from "mathematics written on the page" to its meaning, one would want to also define the strings of symbols and prove that they faithfully represent the syntax trees.  This is analogous to how a compiler for a programming language must start out by "parsing" and "lexing" the code written by the programmer (which is a string of symbols) into an internal "abstract syntax tree" representation.  However, such things are well-understood and extremely uninteresting, so much so that programmers often use "parser generator" programs to *write parsers for them*; the interesting and nontrivial mathematics starts once we have an abstract syntax tree.

## Variables and meta-variables

Experts will know that there are many ways to deal with variable binding in type theory, including "named variables", "de Bruijn indices", "de Bruijn levels", "locally nameless variables", and so on.  We will use "named variables".  The reason is that our goal is expositional and sociological, and named variables keep the syntax as close as possible to what "users" of type theory are familiar with (e.g. with named variables we write $\lambda x. \lambda y. App(x,y)$, whereas with de Bruijn indices one has to write instead $\lambda. \lambda. App(2,1)$).  Since we are humans writing for humans to read, we don't want to deal explicitly with de Bruijn indices, and neither do we want to pretend that we are using de Bruijn indices when we aren't *really* using them.

Thus, we suppose given an infinite set $Var$, whose elements we call *variables*.  [[constructive mathematics|Constructivists]] should assume that $Var$ has [[decidable equality]].  In addition we assume given an operation $fr : Var \times P_{fin}(Var) \to Var$ which replaces a variable with another one that is "fresh for", i.e. distinct from all of, a given finite set of variables.  That is, we assume that $fr(x,V) \notin V$.  We also assume for simplicity that if already $x\notin V$ then $fr(x,V) = x$.  We will also write $fr(x,V)$ as $x^{[V]}$, and if $X = \{x_1,\dots,x_n\}$ is a linearly ordered set of variables we will write
$$X^{[V]} = \{ x_1^{[V]}, x_2^{[V\cup \{x_1^{[V]}\}]}, \dots, x_n^{[V \cup \{x_1,\dots,x_{n-1}\}^{[V]}]}\}$$
for the result of freshening each element of $X$ in succession, ensuring that they remain distinct not only from $V$ but also from each other.

We will also frequently use *meta-variables*.  These are simply ordinary mathematical variables in the "metatheory", i.e. the ordinary informal mathematics we are using in which to define and prove things about type theory.  Single upper-case roman letters will usually be meta-variables ranging over raw terms or raw types.  Single lower-case roman letters will usually be meta-variables ranging over variables (i.e. elements of $Var$).

## Sorts, operators, and constants

Overall, we are not attempting in this project to treat "all type theories" at any level of generality, instead simply dealing with individual type formers one by one (though attempting to be as "modular" as possible).  However, at the level of *raw* syntax we can easily be fully general, thereby saving ourselves some additional work in each case.  Thus, we will work with a variant of what in [[Practical Foundations for Programming Languages]] are called *abstract binding trees*, parametrized by a set of *sorts* and a set of *operators*.

For us the set of **sorts** is $Sort = \{ tm, ty \}$.  That is, there are two classes of raw syntactic objects: raw terms and raw types.  The only function of the notion of "sort" is to avoid writing exactly the same things twice in the two cases.

The set of **operators** $Op$ is a parameter of the theory; the rules for each type former begin by specifying some relevant operators.  For instance, the operators associated to $\Pi$-types are $\{ \Pi, \lambda, App\}$.

Each operator is furthermore associated with a **signature** or **generalized arity**, which consists of:

0. A sort (i.e. either $tm$ or $ty$).
1. A natural number $n$, the **argument arity**.
2. A [[function]] from $[n]=\{1,\dots,n\}$ to $Sort$, the **argument sorts**.
3. A natural number $m$, the **binding arity**.
4. A decidable [[relation]] $\lhd$ between $[n]$ and $[m]$ called **scoping**.  If $j\lhd k$ we say that the $j^{th}$ argument is *in the scope of* the $k^{th}$ binder.

Often (e.g. in [[PFPL]]) the scoping relation is a [[function]] from $[m]$ to $[n]$, i.e. each binder has exactly one subterm in its scope.  However, it is convenient to be more general; e.g. in a fully-annotated $\lambda$-abstraction $\lambda(x:A.B).M$ it is natural to consider $B$ and $M$ to be both in the scope of the variable $x$, rather than requiring this to be desugared to a form such as $\lambda(A,x.B,x'.M)$ in which potentially-different variables are bound in $B$ and $M$.  Thus, we will represent $\lambda$ as an operator with 3 arguments, two of sort $ty$ and one of sort $tm$, with binding arity 1, and scoping relations $2\lhd 1$ and $3\lhd 1$.

Fully general abstract binding trees also allow each *binder* to be associated to a sort.  However, in our type theories all variables will range only over terms (not types).

Finally, in addition to the operators arising from type formers, we assume a collection of **constants**, each of which is an operator with binding arity $0$ and all arguments having sort $tm$.

We will usually use single upper-case typewriter font letters like $\mathtt{C},\mathtt{D}$ for meta-variables ranging over operators, including constants.

## Raw terms

Our raw syntax, though untyped, will be *strongly scoped*.  By this we mean that each raw term or type is indexed by a finite set of variables that may occur in it freely.  To be precise, we define inductively a family of sets $Raw$ indexed by $P_{fin}(Var) \times Sort$; we call their elements **raw terms/types with variables from $V$**.  Since we are in such generality, there are only two constructors of this inductive family:

* For any $V\in P_{fin}(Var)$ and any $x\in V$, we have $x\in Raw(V,tm)$.

* Suppose $\mathtt{C}$ is an operator of sort $s$, argument arity $n$ and binding arity $m$.  Suppose also $V, X\in P_{fin}(Var)$, with $V\cap X = \emptyset$, ${|X|} = m$, and $X = \{x_1,\dots, x_m\}$ totally ordered.  Given $j\in [n]$, write $X_j = \{x_k \mid j \lhd k \}$ for the variables bound in argument $j$, and suppose furthermore that for each $j\in [n]$ we have $M_j\in Raw(V\cup X_j, t_j)$, where $t:[n] \to Sort$ gives the argument sorts of $\mathtt{C}$.  Then we have an element $\mathtt{C}(X;\vec{M}) \in Raw(V,s)$.

This can be read as saying that each set $Raw(V,s)$ consists of well-founded rooted trees containing nodes of two kinds:

* Nodes labeled by a variable (element of $Var$) that is either in $V$ or is bound in some parent of that node and scopes over that node.  Such a node has no children and is of sort $tm$.

* Nodes labeled by an operator and a list of variables of its binding arity that are *not* in $V$ or bound in some parent of that node.  Such a node has a number of children equal to the argument arity of its operator label, of appropriate sorts, and each of its variables scopes over the subtrees of those children specified by the scoping relation of its operator label, while its sort is that of its operator label.

The above clauses also introduce notation for these trees: we will write simply "$x$" for the tree consisting of a single variable node with associated variable $x$, and $\mathtt{C}(X;\vec{M})$ for the tree whose root is an operator node with associated operator $\mathtt{C}$, bound variables $X$, and subtrees $\vec{M}$.  (These are the "linear" syntaxes that have to be "parsed" into an abstract syntax tree if implementing type theory on a computer.)  For instance, a fully annotated abstraction $\lambda(x:A.B).M$ is desugared as $\lambda(x;A,B,M)$, a node labeled by $\lambda$ and $x$ with three subtrees, two of which are in the scope of $x$.

The requirement that $V\cap X= \emptyset$ amounts to a "local [[Barendregt convention]]" that the names of bound variables can never clash with (or "shadow") any free variables, where the set of "free variables" is *declared* for each raw term or type (the set $V$) rather than extracted by syntactic analysis.  Maintaining this convention requires "freshening" when we weaken by adding new unused free variables; see below.


## Operators

For each type former, we describe its binding arity, argument arity and sorts, and scoping relation in a hopefully more readable form, by giving arbitrary names to its bound variables and arguments.  We also give the "sugared" or "traditional" syntax that we will usually use for it.

For instance, the $\lambda$ row below means that $\lambda$ is an operator of sort $tm$, it has two arguments of sort $ty$ and one of sort $tm$, and one binder that scopes over the second type argument and the term argument.

### $\Pi$-types

[[!include Initiality Project - Raw Syntax - Pi-types]]

### Others

to be added later...

## Structural induction

The principle of structural induction on raw terms and types says that to prove something about all of them, it suffices to consider raw terms and types constructed according to each of the above clauses (i.e. consider all possible labels for the root of an abstract syntax tree), assuming as an inductive hypothesis that the desired statement holds of all subtrees.  This is a basic property of an inductive type; if our metatheory is set-theoretic then it can be proven from the definition of well-founded tree.

Similarly, there is a structural recursion principle for defining pairs of functions with domains $RawTm$ and $RawTy$: to define such a function it suffices to say, for each inductive clause, how to construct the value of the function on a tree with that root, assuming given its values on all the subtrees.

## $\alpha$-equivalence

We want to identify raw terms and types that differ only according to a renaming of bound variables.  However, in defining this inductively, we end up having to also rename *free* variables in the terms where the variables are bound.  We do this all together by defining a relation $M \sim_\rho M'$, where $M\in Raw(V,s)$, $M'\in Raw(V',s)$, and $\rho$ is a bijection $V\cong V'$, by recursion on $M$ and $M'$ as follows:

* If $x\in V$ and $y\in V'$, then $x \sim_\rho y$ if and only if $\rho(x)=y$.

* For ordered sets $X,X'$ of the same cardinality, let $\xi:X\cong X'$ be the unique order-preserving bijection between them, and with $X_j = \{x_k \mid j \lhd k \}$ and $X'_j = \{x'_k \mid j \lhd k \}$ as before we have similarly $\xi_j : X_j \cong X'_j$.  Then $\mathtt{C}(X;\vec{M}) \sim_{\rho} \mathtt{C}(X';\vec{M'})$ if and only if $M_j \sim_{\rho \cup \xi_j} M'_j$ for all $j$.

* In all other cases (e.g. one of $M$ and $M'$ is a variable and the other is an operator, or they are distinct operators), $M\sim_\rho M'$ is false.

It is easy to prove by induction that:

* For any $M\in Raw(V,s)$ we have $M\sim_{id} M$.
* If $M\sim_\rho M'$ then $M' \sim_{\rho^{-1}} M$.
* If $M\sim_\rho M'$ and $M' \sim_{\rho'} M''$, then $M\sim_{\rho'\circ\rho} M''$.

In particular, each $\sim_{id}$ is an equivalence relation on $Raw(V,s)$.

## Weakening, exchange, and contraction

For any function $\sigma :V\to W$, we define a function $Raw(V,s) \to Raw(W,s)$, written $M \mapsto M[\sigma]$, by induction on $M$.  When $\sigma$ is a subset inclusion, this is "weakening": adding a new unused free variable.  But to define weakening inductively, we will need to involve $M[\sigma]$ when $\sigma$ is an injection that is not a subset inclusion, and it is no extra trouble to define it for any function $\sigma$ at all.

* If $M=x\in V$, we define $x[\sigma] = \sigma(x)$.

* If $M=\mathtt{C}(X;\vec{M})$, we would like to define $M[\sigma]$ to be "$\mathtt{C}(X;\vec{N})$" where $N_j = M_j[\sigma]$.  But this is not allowed by our definitions, since $X$ may not be disjoint from $W$ (though it is disjoint from $V$).  Thus, recall that we have the successive freshening $X^{[W]}$ that is disjoint from $W$ and an order-preserving bijection $\xi :X \cong X^{[W]}$.  Let $\xi_j:X_j \cong X^{[W]}_j$ be the restriction of $\xi$ to the variables bound in argument $j$; then recursively we have $M_j[\sigma\cup \xi_j] \in Raw(W\cup X^{[W]}_j,s_j)$.  If we write $N_j = M_j[\sigma\cup \xi_j]$, then we can define $\mathtt{C}(X;\vec{M})[\sigma] = \mathtt{C}(X^{[W]};\vec{N})$.

It is easy to prove by induction that if $\rho,\rho'$ are bijections and $\rho' \circ \sigma = \sigma'\circ \rho$, then $M\sim_\rho M'$ implies $M[\sigma] \sim_{\rho'} M'[\sigma']$.  That is, the structural rules respect $\alpha$-equivalence.

## Substitution

Let $N\in Raw(V,tm)$ and $M\in Raw(V\cup \{x\},s)$ where $x\notin V$; we want to define $M[N/x] \in Raw(V,s)$ by induction on $M$.

* If $M=x$, then $x[N/x] = N$; this is well-typed since in this case $s=tm$.

* If $M=y$ for some variable $y\in V$, then $y[N/x] = y$.

* If $M = \mathtt{C}(X;\vec{M})$, we want to recursively substitute $N$ for $x$ in each $M_j$.  But recall that $M_j \in Raw(V\cup \{x\} \cup X_j,s_j)$, so in order to write "$M_j[N_j/x]$" we need $N_j \in Raw(V\cup X_j,tm)$, whereas we are given only $N\in Raw(V,tm)$.  Thus, we define $N_j = N[\sigma_j]$, where $\sigma_j:V\to V\cup X_j$ is the obvious inclusion.  Then we can define $P_j = M_j[N[\sigma_j]/x]$ and hence $M[N/x] = \mathtt{C}(X;\vec{P})$.

Note that substitution is automatically "capture-avoiding" because of our "strong scoping" and local Barendregt convention.  Before we can write $M[N/x]$, strong scoping requires $M$ and $N$ to have the same free variables (except for $x$, which only $M$ has), and no bound variables in $M$ can coincide with these free variables; thus no free variables in $N$ can get "captured" when it is substituted under binders in $M$.  If $M$ and $N$ are not "given" with the same free variables, we need to explicitly weaken them first in order to substitute, and the definition of weakening was forced by strong scoping to rename all bound variables to keep them distinct from the newly added free ones; in particular, the bound variables in $M$ must get renamed to differ from any free variables in $N$.  Finally, the definition of substitution is also forced by strong scoping to rename *bound* variables in $N$ (using the weakening $[\sigma_j]$) to keep them distinct from any bound variables in $M$ under which they are substituted, ensuring that $M[N/x]$ still satisfies the Barendregt convention.

category: Initiality Project
