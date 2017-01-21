
# MacNeille real numbers
* table of contents
{: toc}

## Idea

The MacNeille real numbers are a version of [[real numbers]] defined by forming the [[MacNeille completion]] of the [[rational numbers]].  In [[classical mathematics]], the MacNeille real numbers consist of the [[real numbers]], $\infty$, and $-\infty$; thus, they are the same as the [[extended real numbers]].  However, in [[constructive mathematics]], they are different (and less well behaved); it is not a constructive theorem that every bounded MacNeille number is located (hence a real number in the usual sense of constructive mathematics).


## Definition

Let $\mathbb{Q}$ be the [[poset]] of [[rational numbers]] with its usual [[Archimedean order]].  A pair $(L,U)$ of [[subsets]] of $\mathbb{Q}$ is called a __Dedekind--MacNeille cut__ in $\mathbb{Q}$ if:

* $U$ is the set of [[upper bounds]] of $L$: that is, $s \in U$ iff for all $r \in L$, $s \geq r$; and
* $L$ is the set of [[lower bounds]] of $U$: that is, $r \in L$ iff for all $s \in U$, $r \leq s$.

Given two such cuts, define $(L_1, U_1) \leq (L_2, U_2)$ to mean:

* $L_1 \subseteq L_2$; and
* $U_1 \supseteq U_2$.

(Actually, either of these assertions alone implies the other.)

Then the set of such cuts becomes a [[poset]], in fact a [[complete lattice]].


[[!redirects MacNeille real number]]
[[!redirects MacNeille real numbers]]
[[!redirects MacNeille real]]
[[!redirects MacNeille reals]]
[[!redirects MacNeille number]]
[[!redirects MacNeille numbers]]
