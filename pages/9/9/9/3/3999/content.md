# Idea #

[[compact space|Compactness]] is an extremely useful concept in [[topology]].  The basic idea is that a topological space is compact if it isn't "fuzzy around the edges".

Whilst one can study a topological space by itself, it is often useful to probe it with known spaces.  A common choice for topological spaces, and in particular metric spaces, is to use the natural numbers, and the 1-point compactification of the natural numbers.  This is more traditionally known as studying the topology using sequences and convergent sequences.

Thus one can ask, "Can I detect compactness using probes from $\mathbb{N}$, and $\mathbb{N} \cup \{*\}$?".  The short answer to this is "No", but that just reveals that the question was too restrictive.  Rather, one should ask "What does compactness look like if all I'm allowed to use are probes from $\mathbb{N}$ and $\mathbb{N} \cup \{*\}$?".  The answer to that question is "sequential compactness".

Thus **sequential compactness** is what [[compact space|compactness]] looks like if all one has to test it are sequences.

# Definition #

+-- {: .num_defn #seqcpt}
###### Definition ######
A topological space is **sequentially compact** if every [[sequence]] in it has a [[convergence|convergent]] [[subsequence]].
=--

## Relationship to Compactness ##

Compactness does not imply sequentially compactness, nor does sequentially compactness imply compactness, without further assumptions (see for example wikipedia: [compact spaces] (href="http://en.wikipedia.org/wiki/Compact_space")). 
In [[metric spaces]] for example both notions coincide.

This is _not_ a contradiction to the statement that compact is equivalent to every [[net]] having a convergent subnet: Given a sequence in a compact space, its convergent _subnet_ need not be a _subsequence_ (see [[net]] for a definition of subnet).

### a Compact Space that is not Sequentially Compact ###
A famous example of a space that is compact, but not sequentially compact, is the product space
$$
    I^{I} := [0, 1]^{[0, 1]}
$$
with the [[product topology]]. It is compact by the [[Tychonoff theorem]]. 

Points of $I^{I}$ are functions $I \to I$, and the product topology is the topology of pointwise convergence.

Define a sequence $(a_n)$ in $I^{I}$ with $a_n(x)$ being the nth digit in the binary expansion of $x$.  Let $a \coloneqq (a_{n_k})$ be a subsequence and define $p_a \in I$ by the binary expansion that has a $0$ in the $n_k$th position if $k$ is even and a $1$ if $k$ is odd (and, for definiteness, define it to be $0$ elsewhere).  Then the projection of $(a_{n_k})$ at the $p_a$th coordinate is $1, 0, 1,0,...$ which is not convergent.  Hence $(a_{n_k})$ is not convergent.

(Basically that's the diagonal trick of [[Cantor's theorem]]).

However, as $I^I$ is compact, $a$ has a convergent subnet.  An explicit construction of a convergent subset, given a cluster point $a$, is as follows.  A function $a \colon I \to I$ is a cluster point of $(a_n)$ if, for any $p_1, \dots, p_n \in I$ the set

$$
A(p_1,\dots,p_n) \coloneqq \{k \in \mathbb{R} : a_k(p_i) = a(p_i) \forall i\}
$$

is infinite.  We index our subnet by the family of finite subsets of $I$ and define the subnet function $\mathcal{F}(I) \to \mathbb{N}$ to be

$$
\{p_1,\dots,p_n\} \mapsto \min A(p_1,\dots,p_n)
$$

This is a convergent subnet.

# Properties #

The following is a list of properties of and pertaining to sequentially compact spaces.


1. For a [[metric space]], the notions of sequential compactness and compactness coincide.

2. The [[Eberlein–Šmulian theorem]] states that in a [[Banach space]], for a subset with regard to the [[weak topology]], compactness and sequentially compactness are both equivalent to the weaker notion of [[countable compactness]].

[[!redirects sequentially compact]]
[[!redirects sequential compactness]]
[[!redirects sequentially compact space]]