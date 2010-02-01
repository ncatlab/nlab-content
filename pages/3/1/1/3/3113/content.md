# Weak multilimits
* table of contents
{: toc}


## Idea

A *weak multilimit* is a common generalization of [[multilimits]] and [[weak limits]].


## Definition 

If $F\colon D\to C$ is a diagram in a [[category]] $C$, then a **weak multilimit** of $F$ is a (small) set $L$ of [[cones]] over $F$ such that any other cone over $F$ factors (not necessarily uniquely) through some (not necessarily unique) element of $L$.  If the factorization, and the cone factored through, are unique, then $L$ is a multilimit, whereas if $L$ is a singleton, then it is a *weak limit*.

The existence of weak multilimits is a "pure size condition" on $C$, in the sense that if $C$ is a [[small category]], then every small diagram in $C$ (that is, every functor $F\colon D\to C$ where $D$ is also small) has a weak multilimit, namely the set of *all* cones over $F$.

Of course, weak multilimits in $C^{op}$ are called **weak multicolimits** in $C$.


## Examples

* A weak multilimit of the empty diagram is a *weak multi-terminal-object*, also called a **weakly terminal set**: a small set $T$ of objects such that every object admits a morphism to some object in $T$.  The dual concept is a **weakly initial set**.  These notions play a role in some statements of the [[adjoint functor theorem]].


[[!redirects weak multilimit]]
[[!redirects weak multicolimit]]
[[!redirects weakly initial set]]
[[!redirects weakly terminal set]]
