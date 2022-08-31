
#Contents#
* table of contents
{:toc}

##Idea

A well generated [[triangulated category]] is a generalization of the notion of [[compactly generated triangulated category]] which was introduced by [Neeman, 2001](#Neeman).  The following definition is from ([Krause](#Krause)) and is somewhat shorter and more natural than Neeman's original definition.

##Definition

+-- {: .num_defn}
###### Definition

Let $T$ be a [[triangulated category]] with arbitrary [[coproducts]]. Then $T$ is **well-generated** in the sense of Neeman if and only if there exists a [[set]] $S_0$ of [[objects]] satisfying:

1. an object $X$ of $T$ is [[zero object|zero]] if $[S,X]=0$ for all $S\in S_0$;

1. for every set of maps $X_i\to Y_i$ in $T$, the induced map $[S,\coprod_I X_i]\to[S,\coprod_I Y_i]$ is surjective for all $S\in S_0$ whenever $[S,X_i]\to[S,Y_i]$ is surjective for all $i$ and all $S\in S_0$. 

1. the objects of $S_0$ are $\alpha$-[[compact object|small]] for some [[cardinal]] $\alpha$.  

=--

We recall that an object $S$ in a triangulated category is $\alpha$-small if every map $S\to\coprod_J X_j$ factors through $\coprod_I X_j$ for some $I \subseteq J$ with $\vert I\vert \lt \alpha$.

##References

* [[Henning Krause]], _On Neeman's well generated triangulated categories_, Documenta Mathematica __6__ (2001) ([pdf](https://www.math.uni-bielefeld.de/documenta/vol-06/07.pdf)).
 {#Krause}

* Henning Krause, _Localization theory for triangulated categories_, [arXiv:0806.1324](https://arxiv.org/abs/0806.1324)

* [[Amnon Neeman]], _Triangulated Categories_, Annals of Mathematics Studies 148, Princeton University Press (2001).
 {#Neeman}

[[!redirects well generated triangular category]]
[[!redirects well-generated triangulated categories]]
