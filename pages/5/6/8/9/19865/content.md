# Initiality Project - Raw Syntax

This page is part of the [[Initiality Project]].

* table of contexts
{:toc}

## Idea

Here we define the "raw syntax" for our type theory.  This is a set whose elements are called "raw terms".  They are obtained by putting together operations like "$\Sigma$-types" and "$\lambda$-abstraction" in a way that "makes sense locally" but not necessarily globally.  For instance, $\lambda (x:y.z) .x$, $\Sigma(x:y.z) \Pi(u:x.w) u$, and $\Sigma(x:\lambda(y:x.z).w).u$ are raw terms, even though the latter cannot make any sense globally because $\lambda(y:x.z).w$ can never be a type.  On the other hand, something like $\Sigma(\lambda.:x)()\lambda\Pi$ is not even a raw term, just a meaningless string of tokens.

In traditional approaches to logic, one often defines the raw terms (or "well-formed formulas") as a subset of the set of all "strings", i.e. finite lists of elements of some "alphabet" set such as $\{\Sigma,\Pi,\lambda,(,),:,\dots \}$.  Note that parentheses, colons, commas, and so on are all symbols in the alphabet.  In addition, this point of view requires us to alter some of the clauses to include extra parentheses, e.g. we have to write $(A\times B)$ so that $((A\times B)\times C)$ has an unambiguous meaning.

However, a more modern perspective is to regard this as defining an [[inductive type]] (in the metatheory), with each clause as a constructor.  In this case, the raw terms themselves are not lists of symbols with some property, but rather *trees* whose nodes are labeled with appropriate symbols.  This way we obtain automatically an induction principle for defining functions by recursion and proving theorems by induction over the set of terms, which in the strings-of-symbols approach one has to prove by hand.  The strings of symbols we write on the page like $(A\times B)\times C$ are then regarded as just a *notation* for these "abstract syntax trees".

It's true that to be completely precise about the *entire* passage from "mathematics written on the page" to its meaning, one would want to also define the strings of symbols and prove that they faithfully represent the syntax trees.  This is analogous to how a compiler for a programming language must start out by "parsing" and "lexing" the code written by the programmer (which is a string of symbols) into an internal "abstract syntax tree" representation.  However, such things are well-understood and extremely uninteresting, so much so that programmers often use "parser generator" programs to *write parsers for them*; the interesting and nontrivial mathematics starts once we have an abstract syntax tree.

## Variables and meta-variables

We suppose given an infinite set $Var$, whose elements we call *variables*.

We will also frequently use *meta-variables*.  These are simply ordinary mathematical variables in the "metatheory", i.e. the ordinary informal mathematics we are using in which to define and prove things about type theory.  Single upper-case roman letters will usually be meta-variables ranging over raw terms, such as in the inductive clauses below like "if $A$ and $B$ are raw terms, so is $A\times B$."  Single lower-case roman letters will usually be meta-variables ranging over variables (i.e. elements of $Var$), as in inductive clauses below such as "if $A,B,M$ are raw terms and $x$ is a variable, then $\lambda (x:A.B). M$ is a raw term."

## Constants

We suppose given a set $Cst$, whose elements we call *constants* (sometimes also called "atomic terms" or "axiomatic terms").  We will usually use single upper-case typewriter font letters like $\mathtt{C},\mathtt{D}$ for meta-variables ranging over constants.

## Raw terms

Given the set $Var$ of variables and the set $Cst$ of constants, the set $RawTm$ of **raw terms** is defined inductively as follows.  This can be read as saying that $RawTm$ is a set of well-founded rooted trees in which each node is labeled by one of the following clauses.  The children of such a node must correspond to the raw terms assumed to be given in that clause, and any other data (such as variables) must be associated to the node as well.

We will not distinguish at this stage between raw terms that "should be types", such as $\Pi(x:A). B$, and those that "should be terms", such as $\lambda(x:A.B). M$.  That will come later with the judgments: only certain raw terms can be judged to be types, and others can be judged to be terms.  This is simply a choice; instead of one inductive set $RawTm$ we could define two mutually inductive sets, say $RawTm$ and $RawTy$.  But combining them, as we do here, may be convenient later on if we want to consider universes a la Russell, in which the same syntax is used to represent a term in a universe and its corresponding type.

We divide up the clauses according to the type forming operations that may be present in the theory.

### Variables and constants

* Every variable is a raw term.
* If $\mathtt{C}$ is a constant and $M_1,\dots,M_n$ are raw terms, then $\mathtt{C}(M_1,\dots, M_n)$ is a raw term.

That is, there is a node label called $variable$, and every node labeled $variable$ has no children but comes with an additional associated element of $Var$.  Similarly, there is a node label called $constant$, and every node labeled $constant$ has an arbitrary finite number of children and comes with an additional associated element of $Cst$.

The above clauses also introduce notation for these trees: we will write simply "$x$" for the tree consisting of a single $variable$ node with associated variable $x$, and $\mathtt{C}(M_1,\dots, M_n)$ for the tree whose root is a $constant$ node with associated constant $\mathtt{C}$ and subtrees $M_1,\dots,M_n$.  (These are the "linear" syntaxes that have to be "parsed" into an abstract syntax tree if implementing type theory on a computer.)  Thus, for instance, $\mathtt{C}(\mathtt{D}(x),y)$ represents a tree with four nodes: a root with two children, one of which itself has two children.

### $\Pi$-types

[[!include Initiality Project - Raw Syntax - Pi-types]]

### Others

to be added later...

## Structural induction

The principle of structural induction on raw terms says that to prove something about all raw terms, it suffices to consider terms constructed according to each of the above clauses (i.e. consider all possible labels for the root of an abstract syntax tree), assuming as an inductive hypothesis that the desired statement holds of all subtrees.  This is a basic property of an inductive type; if our metatheory is set-theoretic then it can be proven from the definition of well-founded tree.

Similarly, there is a structural recursion principle for defining functions with domain $RawTm$: to define such a function it suffices to say, for each inductive clause, how to construct the value of the function on a tree with that root, assuming given its values on all the subtrees.

## Substitution and $\alpha$-equivalence

If $M$ and $N$ are raw terms and $x$ is a variable, we will write $M[N/x]$ for the raw term obtained by "substituting $N$ for all occurrences of $x$ in $M$".  Note that the square brackets are *not* one of the inductive clauses defining the set $RawTm$; there are no nodes in the abstract syntax tree labeled by them.  Instead they are an *operation* on this set, i.e. a function $RawTm \times RawTm \times Var \to RawTm$.

In terms of abstract syntax trees, $M[N/x]$ should be obtained by replacing every $variable$ node in the tree $M$ that is labeled by $x$ with a copy of the tree $N$.  Such a "naive substitution operation" can be defined quite easily by structural recursion on $M$, with clauses such as the following:

* $x[N/x] = N$.
* $y[N/x] = y$ if $y\neq x$.
* $(\mathtt{C}(M_1,\dots,M_n))[N/x] = \mathtt{C}(M_1[N/x],\dots,M_n[N/x])$.
* $(\Pi(y:A).B)[N/x] = \Pi(y:A[N/x]).B[N/x]$.
* $(\lambda(y:A.B). M)[N/x] = \lambda(y:A[N/x].B[N/x]).M[N/x]$.
* $(App^{y:A.B}(M,P))[N/x] = App^{y:A[N/x].B[N/x]}(M[N/x],P[N/x])$.

(These $=$ signs are literal equalities between raw terms, i.e. elements of the set $RawTm$.  Later on we will also have judgmental equality and identity types.)

However, this simple definition is not quite what we want $M[N/x]$ to mean, because it can result in *variable capture*.  For instance, if $M$ is $\lambda (y:A.A). x$ (the constant function with value $x$, which is a free variable) and $N$ is $y$ (a free variable), then $M[N/x]$ ought to represent the constant function with value $y$; but this naive kind of substitution would produce $\lambda (y:A.A).y$, which represents the *identity* function.  The problem is that the variable $y$ in $M$ is "bound" and should not "capture" the free variable $y$ in $N$.

TODO: Define $\alpha$-equivalence and capture-avoiding substitution.
