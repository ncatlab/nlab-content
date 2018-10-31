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

We suppose given an infinite set $Var$, whose elements we call *variables*.

Experts will know that there are many ways to deal with variable binding in type theory, including "named variables", "de Bruijn indices", "de Bruijn levels", "locally nameless variables", and so on.  We are using "named variables" (the set $Var$ is the names).  The reason is that our goal is expositional and sociological, and named variables keep the syntax as close as possible to what "users" of type theory are familiar with.  Since we are humans writing for humans to read, we don't want to deal explicitly with de Bruijn indices, and neither do we want to pretend that we are using de Bruijn indices when we aren't *really* using them.

We will also frequently use *meta-variables*.  These are simply ordinary mathematical variables in the "metatheory", i.e. the ordinary informal mathematics we are using in which to define and prove things about type theory.  Single upper-case roman letters will usually be meta-variables ranging over raw terms or raw types, such as in the inductive clauses below like "if $A$ and $B$ are raw types, so is $A\times B$."  Single lower-case roman letters will usually be meta-variables ranging over variables (i.e. elements of $Var$), as in inductive clauses below such as "if $A,B$ are raw types, $M$ is a raw term, and $x$ is a variable, then $\lambda (x:A.B). M$ is a raw term."

## Constants

We suppose given two sets $TyCst$ and $TmCst$, whose elements we call *type constants* and *term constants* (sometimes also called "atomic terms" or "axiomatic terms").  We will usually use single upper-case typewriter font letters like $\mathtt{C},\mathtt{D}$ for meta-variables ranging over constants.

## Raw terms

Given the set $Var$ of variables and the sets $TyCst$ and $TmCst$ of constants, the sets $RawTm$ and $RawTy$ of **raw terms** and **raw types** are defined mutually inductively as follows.  This can be read as saying that $RawTm$ and $RawTy$ are sets of well-founded rooted trees in which each node is labeled by one of the following clauses.  The children of such a node must correspond to the raw terms or types assumed to be given in that clause, and any other data (such as variables) must be associated to the node as well.

We divide up the clauses according to the type forming operations that may be present in the theory.

### Variables and constants

* Every variable is a raw term.
* If $\mathtt{C}$ is a term constant and $M_1,\dots,M_n$ are raw terms, then $\mathtt{C}(M_1,\dots, M_n)$ is a raw term.
* If $\mathtt{C}$ is a type constant and $M_1,\dots,M_n$ are raw terms, then $\mathtt{C}(M_1,\dots, M_n)$ is a raw type.

That is, there is a node label called $variable$, and every node labeled $variable$ has no children but comes with an additional associated element of $Var$.  Similarly, there are node labels called $tmconst$ and $tyconst$, and every node with these labels has an arbitrary finite number of children and comes with an additional associated element of $TmCst$ or $TyCst$.

Note that there are no "type variables"; later on we may introduce universes.  Similarly, the arguments of a constant are always terms, not types.

The above clauses also introduce notation for these trees: we will write simply "$x$" for the tree consisting of a single $variable$ node with associated variable $x$, and $\mathtt{C}(M_1,\dots, M_n)$ for the tree whose root is a constant node with associated constant $\mathtt{C}$ and subtrees $M_1,\dots,M_n$.  (These are the "linear" syntaxes that have to be "parsed" into an abstract syntax tree if implementing type theory on a computer.)  Thus, for instance, $\mathtt{C}(\mathtt{D}(x),y)$ represents a tree with four nodes: a root with two children, one of which itself has two children.

### $\Pi$-types

[[!include Initiality Project - Raw Syntax - Pi-types]]

### Others

to be added later...

## Structural induction

The principle of structural induction on raw terms and types says that to prove something about all of them, it suffices to consider raw terms and types constructed according to each of the above clauses (i.e. consider all possible labels for the root of an abstract syntax tree), assuming as an inductive hypothesis that the desired statement holds of all subtrees.  This is a basic property of an inductive type; if our metatheory is set-theoretic then it can be proven from the definition of well-founded tree.

Similarly, there is a structural recursion principle for defining pairs of functions with domains $RawTm$ and $RawTy$: to define such a function it suffices to say, for each inductive clause, how to construct the value of the function on a tree with that root, assuming given its values on all the subtrees.

## Substitution and $\alpha$-equivalence

If $M$ is a raw term or type, $N$ is a raw term, and $x$ is a variable, we will write $M[N/x]$ for the raw term or type obtained by "substituting $N$ for all occurrences of $x$ in $M$".  Note that the square brackets are *not* one of the inductive clauses defining the sets $RawTm$ and $RawTy$; there are no nodes in the abstract syntax tree labeled by them.  Instead they are an *operation* on these sets, i.e. a function $RawTm \times RawTm \times Var \to RawTm$ and similarly for types.

In terms of abstract syntax trees, $M[N/x]$ should be obtained by replacing every $variable$ node in the tree $M$ that is labeled by $x$ with a copy of the tree $N$.  Such a "naive substitution operation" can be defined quite easily by structural recursion on $M$, with clauses such as the following:

* $x[N/x] = N$.
* $y[N/x] = y$ if $y\neq x$.
* $(\mathtt{C}(M_1,\dots,M_n))[N/x] = \mathtt{C}(M_1[N/x],\dots,M_n[N/x])$.
* $(\Pi(y:A).B)[N/x] = \Pi(y:A[N/x]).B[N/x]$.
* $(\lambda(y:A.B). M)[N/x] = \lambda(y:A[N/x].B[N/x]).M[N/x]$.
* $(App^{y:A.B}(M,P))[N/x] = App^{y:A[N/x].B[N/x]}(M[N/x],P[N/x])$.

(These $=$ signs are literal equalities between raw terms or types, i.e. between elements of the sets $RawTm$ and $RawTy$.  [[Initiality Project - Type Theory|Later on]] we will also have judgmental equality and identity types.)

However, this simple definition is not quite what we want $M[N/x]$ to mean, because it can result in *variable capture*.  For instance, if $M$ is $\lambda (y:A.A). x$ (the constant function with value $x$, which is a free variable) and $N$ is $y$ (a free variable), then $M[N/x]$ ought to represent the constant function with value $y$; but this naive kind of substitution would produce $\lambda (y:A.A).y$, which represents the *identity* function.  The problem is that the variable $y$ in $M$ is "bound" and should not "capture" the free variable $y$ in $N$.

A correct definition of substitution must, therefore, distinguish between free
and bound variables.  We define the set $FV(M)$ of free variables of a raw term or type $M$ by structural recursion on $M$:

* $FV(x) = \{x\}$
* $FV(\mathtt{C}(M_1,\dots,M_n)) = FV(M_{1}) \cup \dots \cup FV(M_{n})$
* $FV(\Pi(y:A).B) = FV(A) \cup (FV(B) \setminus \{y\})$
* $FV(\lambda(y:A.B). M) = FV(A) \cup (FV(B) \cup FV(M) \setminus \{y\})$
* $FV(App^{y:A.B}(M,P)) = FV(A) \cup (FV(B) \setminus \{y\}) \cup FV(M) \cup FV(P)$

The substitution operation should do nothing to bound variables, and it should avoid substitutions that put a free variable into a context where it will become bound.  Imposing these constraints gives the definition

* $x[N/x] = N$.
* $y[N/x] = y$ if $y\neq x$.
* $(\mathtt{C}(M_1,\dots,M_n))[N/x] = \mathtt{C}(M_1[N/x],\dots,M_n[N/x])$.
* $(\Pi(y:A).B)[N/x] = \Pi(y:A[N/x]).B$ if $y = x$.
* $(\Pi(y:A).B)[N/x] = \Pi(y:A[N/x]).B[N/x]$ if $y \neq x$ and $y$ is not in $FV(N)$.
* $(\lambda(y:A.B). M)[N/x] = \lambda(y:A[N/x].B).M$ if $y = x$.
* $(\lambda(y:A.B). M)[N/x] = \lambda(y:A[N/x].B[N/x]).M[N/x]$ if $y \neq x$ and $y$ is not in $FV(N)$.
* $(App^{y:A.B}(M,P))[N/x] = App^{y:A[N/x].B}(M[N/x],P[N/x])$ if $y = x$.
* $(App^{y:A.B}(M,P))[N/x] = App^{y:A[N/x].B[N/x]}(M[N/x],P[N/x])$ if $y \neq x$ and $y$ is not in $FV(N)$.

This definition of substitution avoids capture, but it does so at the cost of making substitution a partial function $RawTm \times RawTm \times Var \rightharpoonup RawTm$.  For example, suppose that $M$ is $\lambda(x : A.B). App^{x : A.B}(f, x)$, which is the [[η-expansion]] of some variable $f$, and that $N$ is $App^{z: C.(\Pi(x:A).B)}(x, z)$.  Then $M[N/f]$ isn't defined: on the one hand $x \neq f$,  but on the other $x$ is a free variable in $N$.  So neither of the two structural recursion cases involving $\lambda$ abstractions applies.

To make substitution a total function, we identify any two terms that differ only in the names of their bound variables.  That is, we define equivalence relations $\sim_{\alpha}$ on $RawTm$ and $RawTy$ generated by the requirements

* $\Pi(x:A).B \sim_{\alpha} \Pi(y:A).B[y/x]$ if $y\notin FV(B)$.
* $\lambda(x:A.B). M \sim_{\alpha} \lambda(y:A.B[y/x]).M[y/x]$ if $y\notin FV(B) \cup FV(M)$.
* $App^{x:A.B}(M,P) \sim_{\alpha} App^{y:A.B[y/x]}(M,P)$ if $y\notin FV(B)$.

This is the relation of [[alpha equivalence|$\alpha$-equivalence]] on the raw terms and types.  We consider $RawTm$ and $RawTy$ to be [[setoids]], i.e. [[thin category|thin]] [[groupoids]], under these equivalence relations.  Thus all operations on raw terms and types must respect $\alpha$-equivalence, and need only be defined up to $\alpha$-equivalence.

This enables us to extend substitution (uniquely up to unique isomorphism) to a functor, i.e. a setoid morphism, $RawTm \times RawTm \times Var \to RawTm$ and similarly for types: for substitutions that didn't used to be defined, modify the term along an $\alpha$-equivalence to eliminate possible variable captures and then do the substitution.

In particular, the substitution $(\lambda(x : A.B). App^{x:A.B}(f, x))[App^{z:C.(\Pi(x:A).B)}(x, z)/f]$ is now defined.  It is equivalent to $(\lambda(w : A.B[w/x]). App^{x:A.B}(f, w))[App^{z:C.(\Pi(x:A).B)}(x, z)/f]$, where $w \notin FV(B)$, by the second condition on $\sim_{\alpha}$, and now the nontrivial case of substitution applies, giving $M[N/f] = \lambda(w : A.B[w/x]). App^{x:A.B}(App^{z:C.(\Pi(x:A).B)}(x, z), w)$.

category: Initiality Project
