
# Strongly extensional functions
* table of contents
{: toc}

## Idea

In [[constructive mathematics]], one sometimes calls a [[function]] 'extensional' to stress that it preserves [[equality]] (as opposed to a [[prefunction]], which need not do so).  A function is _strongly_ extensional if it also reflects inequality in a relevant sense.  One usually employs this in a context where the principle of [[excluded middle]] is enough to prove that every function is strongly extensional.


## Definitions

This is probably not the only context where the term 'strongly extensional' is used, but it\'s the one that I know.

Let $X$ and $Y$ be [[sets]], each equipped with a [[tight apartness]] $\ne$.  Let $f$ be a [[function]] from $X$ to $Y$.  Then $f$ is __strongly extensional__ if $a \ne b$ whenever $f(a) \ne f(b)$.

Note that if $f$ is only a [[prefunction]] (in a [[foundation]] where this makes sense) and we impose the condition of strong extensionality, it follows (upon taking the [[contrapositive]], since [[equality]] is the [[negation]] of any tight apartness) that $f$ is extensional (and so a function).  Conversely, if $\ne$ is also the [[negation]] of [[equality]] (which is always the unique tight apartness in [[classical mathematics]]), then any extensional $f$ is also strongly extensional.  In this way, strong extensionality is a constructively stronger but classically equivalent variation of extensionality.

We have a [[category]] $Set_{\ne}$ whose [[objects]] are sets equipped with tight apartnesses and whose [[morphisms]] are strongly extensional functions.

A strongly extensional function is __strongly [[injective function|injective]]__ if it also preserves $\ne$.  (These are the [[regular monomorphisms]] of $Set_{\ne}$, the [[monomorphisms]] being merely injective in the usual sense of reflecting equality.)


## Examples

If $X$ has [[decidable equality]] and [[negation]] of [[equality]] is an [[apartness relation]], then the negation of equality is a (in fact the unique) [[decidable tight apartness relation]] on $X$, and any function from $X$ to any set $Y$ with a tight apartness relation on $Y$ must be strongly extensional.

Any pointwise-[[continuous function]] between [[metric spaces]] is strongly extensional.  Using [[countable choice]] and [[Markov's principle]] (or actually weak versions thereof), it follows that any function to a metric space from a [[complete metric space]] (regardless of continuity!?) is strongly extensional.

A weak counterexample:  [[internal logic|Internal to]] the [[topos of sheaves]] on the [[unit interval]] $\mathbb{I}$, where an internal [[real number]] is (externally) a [[continuous map]] from $\mathbb{I}$ to the [[real line]] $\mathbb{R}$, consider the internal number $c$ given by the function $(t \mapsto t - t^2)$.  Then the [[subspace]] $\{0,c\}$ of the internal real line is an internal complete metric space (as proved by [Richman](#Richman)), we may define an internal continuous map $f\colon \{0,c\} \to \mathbb{R}$ by $f(0) = 0$ and $f(c) = 1$, and of course we have $f(0) \ne f(c)$ internally.  But the internal [[truth value]] $\{0 \ne c\}$ is only the open interval $]0,1[$, not all of $[0,1]$, so it\'s not completely true that $f$ is strongly extensional.  (However, this $f$ is [[double negation|not not]] strongly extensional, so a stronger counterexample would be nice.)


## References

* [[Fred Richman]]; Weak Markov\'s principle, strong extensionality, and countable choice; available from [Fred Richman\'s documents](http://math.fau.edu/richman/html/docs.htm).
{#Richman}


[[!redirects strongly extensional]]
[[!redirects strongly extensional function]]
[[!redirects strongly extensional functions]]
[[!redirects strongly extensional map]]
[[!redirects strongly extensional maps]]
[[!redirects strongly extensional mapping]]
[[!redirects strongly extensional mappings]]
